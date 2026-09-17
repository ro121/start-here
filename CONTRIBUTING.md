# Model and Editing Guide

## Canonical model

`curriculum.yaml` uses schema version 1. The hierarchy is `curriculum[] → subjects[] → topics[] → concepts[]`. Every domain, subject, and topic has a globally unique lowercase kebab-case `id`, readable `title`, and sibling-local `order`. Concept strings are scoped learning coverage, not independent graph nodes. Promote a concept to a topic only when it needs its own prerequisites, cross-domain references, or substantial explanation.

| Field | Meaning |
| --- | --- |
| Domain `path` | Repository-relative path to its README map |
| Domain `purpose` | Why the domain exists |
| Domain `prerequisites` | Topic IDs that orient entry; not inherited by every child |
| Topic `prerequisites` | Direct recommended prerequisites, all interpreted together |
| Topic `concepts` | Small concepts covered inside the topic |
| Topic `note` | Optional repository-relative path to an authored note |
| Topic `implements` | Canonical concepts this topic implements or applies |
| Topic `related` | Connections without prerequisite semantics |
| Root `references` | Reference records with `id`, `title`, `url`, and optional pinned `content_inventory` |
| Domain `references` | Reference IDs displayed in the domain map |

Prerequisites refer to topic IDs only, avoiding ambiguity about whether an entire domain must be mastered. Empty lists mark entry concepts. Do not infer edges from folder order or containment. `order` expresses editorial preference; the generator uses a topological sort with that preference to suggest a reading order. Domain reading lists filter that global ordering, so external prerequisites still require attention.

`dependencies.yaml` is a derived edge list: scalar `from` is the prerequisite, scalar `to` is the dependent. Multiple prerequisites become multiple edges, all required at an appropriate introductory depth. Related and implementation links are deliberately excluded. No second copy of the graph is edited manually.

External references inform coverage but do not define prerequisites automatically. See the [roadmap.sh review](references/roadmap-sh.md) for the six initial sources, the inspected snapshot, and scope decisions. Keep reference IDs unique and use only registered IDs in domain assignments.

Phase groupings in the renderer are navigation aids, not learning gates. For example, introductory identity precedes Linux permissions even though Security has a later folder number. The SRE map houses canonical reliability objectives; observability and operations refer to them.

## Edit and validate

Use Python 3.10 or newer:

```sh
python -m pip install -r requirements.txt
python scripts/curriculum.py build
python scripts/curriculum.py check
```

The build updates only domain maps, `CURRICULUM.md`, and `dependencies.yaml`. Check mode performs no writes and rejects duplicate IDs, invalid references, prerequisite cycles, stale generated artifacts, missing notes, mismatched note IDs, missing note prerequisites, and broken local Markdown or wiki targets. It checks link destinations rather than guaranteeing that external websites or Mermaid renderers are available.

Edit authored notes separately using [the topic template](templates/topic.md). Keep their prerequisite and relationship sections consistent with YAML. Run check after both model and prose changes. The validator checks required prerequisite links but does not fully interpret prose or prove pedagogical correctness; review those manually.

## Adding a messy topic list

1. Preserve the incoming list in a dated Markdown source document before restructuring it.
2. Map every meaningful entry to an existing topic, an in-topic concept, or a proposed new topic. Record equivalent names and any mergers in that document.
3. Choose one conceptual home. Put product-specific application details under an implementation topic, linked through `implements`.
4. Assign stable IDs, subjects, and direct prerequisites. Use `related` when learning order is not required. Avoid convenience edges that force unrelated branches to become serial.
5. Add substantive notes only where useful; remaining topics get navigable map sections automatically.
6. Regenerate and validate. Review coverage against the original list and explain major domain changes or merges.

Repeated vocabulary in concept lists indicates context, not duplicate canonical topics: HTTP mentions HTTPS while TLS owns transport security; Kubernetes mentions CoreDNS while DNS owns name-resolution fundamentals. Identity has one home in Security; Linux permissions, AWS IAM, and Kubernetes RBAC are applications. Idempotency lives in Distributed Systems but is introduced early for automation. Infrastructure as Code owns desired state and reconciliation. AWS and Kubernetes are implementation-rich domain views of the underlying concepts.

## Moving and expanding topics

Keep an ID stable when changing a title or category. Move the YAML topic to its new subject, update `note` if applicable, and regenerate. Review authored inbound links and note relationships; validation catches missing destinations but cannot migrate prose automatically. Retain a redirect note or alias for previously shared paths when useful. Do not silently remove meaningful incoming topics.

## Obsidian

Open the repository root as the vault so path-qualified wiki links resolve. Wiki links use actual headings for map sections and file paths for authored notes; Markdown links use explicit stable HTML anchors for GitHub. YAML IDs remain independent of both.

Note frontmatter contains only the stable ID and a readable alias. Mermaid works as a fenced diagram. Obsidian's native graph shows note-level links, so several map-only topics initially share one graph node; `dependencies.yaml` preserves the finer topic graph for future import or visualization. YAML is not automatically imported into Obsidian's graph. As topics gain substance, give them notes, update `note`, and regenerate the maps.

Keep `.obsidian` preferences local unless sharing them is intentional. No Obsidian plugin, task database, or scoring metadata is required.
