# blu_fms_ui

Frontend (OWL/JavaScript/XML/SCSS) sources for the Facility Management System Odoo 19 addons.

This repository is **not** a deployable Odoo addon tree by itself. Assets are published here for design review, CI, and mirroring; runtime deployment still requires the matching Python addons from the FMS backend repository with the same paths under each module's `static/` directory.

## Layout

```
ui/
  <module_name>/
    static/src/...     # mirrors fmss/<module_name>/static/
```

See [ui/README.md](ui/README.md) and [ui/BACKEND_COMPATIBILITY.md](ui/BACKEND_COMPATIBILITY.md) for module inventory, Odoo asset bundle declarations, client action tags, and RPC dependencies.

**Source of truth:** `/Users/palakboricha/fmss` (or the canonical FMS git remote).
