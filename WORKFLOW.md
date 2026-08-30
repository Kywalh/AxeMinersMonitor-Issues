# Issue workflow

Axe Miners Monitor uses a simple Jira-style workflow for public issues.

## Main workflow

`To do` → `In analysis` → `Implementing` → `In review` → `In test` → `Closed`

## Side states

- `Postponed` — accepted but intentionally deferred; may later return to `To do` or `In analysis`.
- `Won't do` — intentionally not planned; terminal state.

## Status definitions

| Status | Meaning |
| --- | --- |
| **To do** | Newly accepted issue waiting to be analysed or scheduled. |
| **In analysis** | The issue is being investigated, reproduced, specified, or assessed for feasibility. |
| **Implementing** | Development work is actively in progress. |
| **In review** | Implementation is complete and is being reviewed, typically through a pull request. |
| **In test** | The change is available for validation or regression testing. |
| **Closed** | Work is complete and validated. The GitHub issue itself is closed. |
| **Won't do** | The request will not be implemented. The GitHub issue is closed as `Not planned`. |
| **Postponed** | The issue remains valid but is deferred to a later time. |

## GitHub representation

Open workflow states are represented with exactly one `status:` label at a time:

- `status: to-do`
- `status: in-analysis`
- `status: implementing`
- `status: in-review`
- `status: in-test`
- `status: postponed`

Terminal states use GitHub's native issue state:

- **Closed** → close the issue as completed.
- **Won't do** → close the issue as not planned.

This keeps the issue list compatible with GitHub while preserving a clear Jira-style development lifecycle.
