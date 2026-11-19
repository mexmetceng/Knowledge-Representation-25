# How We Work

## Folders and owners

| Folder | Contents | Owner |
|---|---|---|
| `shared/` | Dataset (CSV files, see `shared/README.md`) and competency questions — the single source of truth both systems encode | Person C |
| `owl/` | Ontology (`.ttl`) and its queries | Person A |
| `datalog/` | `facts.dl`, `rules.dl`, `queries.dl` | Person B |
| `comparison/` | Metrics definition and results | Person D |

Mostly edit only your own folder; that is what keeps merges conflict-free.
Changes to `shared/` need agreement from both the OWL and Datalog owners, since both systems depend on it.

The report lives on Overleaf, not in this repo.

## Order of work

1. Agree on `shared/competency-questions.md` and the data columns in `shared/README.md`, merge to `main`.
2. Then OWL and Datalog are built in parallel against that shared data.

## Branches and pull requests

- Never push directly to `main`; every change goes through a pull request with one approval.
- Branch names: `<area>/<task>`, e.g. `owl/allergen-classes`, `datalog/vegan-rules`, `shared/add-desserts`.
- Keep branches small and merge within a few days.

```bash
git switch main && git pull                 # start from latest main
git switch -c owl/allergen-classes          # new branch
# ...work, commit...
git pull --rebase origin main               # catch up before opening the PR
git push -u origin owl/allergen-classes     # then open a PR on GitHub
```

Review PRs outside your own folder too, so everyone understands both systems.

## OWL files

- Save from Protégé as **Turtle (`.ttl`)** — RDF/XML reorders on every save and is unmergeable.
- Only one person edits a given `.ttl` file at a time. If two people need the ontology, split it into separate files joined with `owl:imports`.
