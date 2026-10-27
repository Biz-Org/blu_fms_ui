# blu_fms_ui

Frontend (OWL/JavaScript/XML/SCSS) sources for the Facility Management System **Odoo 18** addons.

This repository is **not** a deployable Odoo addon tree by itself. Assets are published here for design review, CI, and mirroring; runtime deployment still requires the matching Python addons from **`blu_fms_backend`** (or `fmss`) with the same paths under each module's `static/` directory.

**Target platform:** Odoo **18.0** (not 19). Use an Odoo 18 source tree and a database created with that version.

## Layout

```
<module_name>/
  static/src/...     # mirrors fmss/<module_name>/static/
```

## Sync with backend

From the backend addon directory after UI changes:

```bash
rsync -a static/ /path/to/blu_fms_ui/<module>/static/
```

Into `fmss` for local Odoo:

```bash
rsync -a /path/to/blu_fms_ui/<module>/static/ /path/to/fmss/<module>/static/
```

## Local run (Odoo 18)

Run Odoo from your **18.0** checkout with `fmss` on `--addons-path`. See `run_setup` in the FMS backend repo (`FMSS=/Users/palakboricha/fmss`, database e.g. `fms_dev`, data dir `.odoo-data-18`). Open http://127.0.0.1:8072 after `odoo-bin` starts.

See [BACKEND_COMPATIBILITY.md](BACKEND_COMPATIBILITY.md) for module inventory, Odoo asset bundle declarations, client action tags, and RPC dependencies.

**Source of truth:** `/Users/palakboricha/fmss` (or the canonical FMS git remote).
