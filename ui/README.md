# FMS UI modules

Published from Odoo 19 FMS addons. Path mapping:

| UI repo path | Odoo addon path (FMS) |
|--------------|------------------------|
| `ui/<module>/static/...` | `fmss/<module>/static/...` |
| `ui/community_communication/views/portal_templates.xml` | `fmss/community_communication/views/portal_templates.xml` |

## Modules

| Module | UI files (approx.) | Notes |
|--------|-------------------|--------|
| `ai_copilot` | 8 | Backend OWL app + systray |
| `community_communication` | 49 + portal XML | Includes `static/src/components`, `dashboard`, `analytics`, `views` not all listed in `__manifest__.py` assets |
| `compliance_audit_management` | 25 | |
| `fire_safety_community` | 1 (README only) | **No `static/`** — backend bridge addon |
| `fire_safety_management` | 22 | |
| `integration_iot_management` | 17 | |
| `mobile_application` | 10 | Uses HTTP JSON routes via `mobile_api.js`, not only `orm.call` |
| `reports_analytics` | 23 | |

## Shared patterns

- Shell components: `static/src/owl/ui/*_shell.{js,xml}` and `*_ui.{js,xml}`
- Design tokens: `static/src/scss/_tokens.scss` per module
- Client actions: registered in screen JS with `registry.category("actions").add("<module>.action_*", ...)`

## Deployment note

To load in Odoo, copy (or symlink) each `ui/<module>/static` tree back to `<addons_path>/<module>/static` and keep `__manifest__.py` `assets` entries pointing at `<module>/static/...` as in FMS.
