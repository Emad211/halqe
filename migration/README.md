# Accounting source import

The current accounting application is imported from the `webapp/` tree of `Emad211/clinic_managment` into `accounting/`.

## Import policy

The import intentionally preserves the current Flask/SQLite source, tests, templates, static assets, scripts, and packaging configuration while excluding operational and generated material:

- production or local SQLite databases
- environment files and secrets
- caches and logs
- backups
- `build/` and `dist/` outputs

The exact source commit is pinned in `accounting-source.ref`. The read-only boundary between the future Halqe clinical platform and accounting remains an architectural invariant; moving the accounting source into this repository does not permit the clinical side to write into the accounting database.
