# Backend compatibility
Do not change model/method names or action tags without matching backend changes.

## Client actions & systray
- `ai_copilot.action_copilot` (ai_copilot)
- `systray:ai_copilot.Systray` (ai_copilot)
- `community_communication.action_analytics` (community_communication)
- `community_communication.action_announcements` (community_communication)
- `community_communication.action_dashboard` (community_communication)
- `community_communication.action_discussions` (community_communication)
- `community_communication.action_events` (community_communication)
- `community_communication.action_feedback` (community_communication)
- `community_communication.action_groups` (community_communication)
- `community_communication.action_notices` (community_communication)
- `community_communication.action_polls` (community_communication)
- `community_communication.action_registrations` (community_communication)
- `compliance_audit_management.action_activities` (compliance_audit_management)
- `compliance_audit_management.action_audits` (compliance_audit_management)
- `compliance_audit_management.action_calendar` (compliance_audit_management)
- `compliance_audit_management.action_dashboard` (compliance_audit_management)
- `compliance_audit_management.action_documents` (compliance_audit_management)
- `compliance_audit_management.action_reports` (compliance_audit_management)
- `fire_safety_management.action_dashboard` (fire_safety_management)
- `fire_safety_management.action_drills` (fire_safety_management)
- `fire_safety_management.action_emergency` (fire_safety_management)
- `fire_safety_management.action_equipment` (fire_safety_management)
- `fire_safety_management.action_incidents` (fire_safety_management)
- `fire_safety_management.action_inspections` (fire_safety_management)
- `fire_safety_management.action_reports` (fire_safety_management)
- `integration_iot_management.action_automation` (integration_iot_management)
- `integration_iot_management.action_dashboard` (integration_iot_management)
- `integration_iot_management.action_devices` (integration_iot_management)
- `integration_iot_management.action_energy` (integration_iot_management)
- `integration_iot_management.action_systems` (integration_iot_management)
- `mobile_application.action_mobile_app` (mobile_application)
- `reports_analytics.action_alerts` (reports_analytics)
- `reports_analytics.action_builder` (reports_analytics)
- `reports_analytics.action_cross_module` (reports_analytics)
- `reports_analytics.action_dashboard` (reports_analytics)
- `reports_analytics.action_financial` (reports_analytics)
- `reports_analytics.action_kpis` (reports_analytics)
- `reports_analytics.action_library` (reports_analytics)
- `reports_analytics.action_management` (reports_analytics)
- `reports_analytics.action_operational` (reports_analytics)
- `reports_analytics.action_predictive` (reports_analytics)
- `reports_analytics.action_preview` (reports_analytics)
- `reports_analytics.action_reports` (reports_analytics)
- `reports_analytics.action_scheduled` (reports_analytics)
- `reports_analytics.action_trends` (reports_analytics)

## `orm.call` targets (unique model.method per module)
- `ai.copilot.service.ask` — ai_copilot
- `ai.copilot.service.cancel_action` — ai_copilot
- `ai.copilot.service.confirm_action` — ai_copilot
- `ai.copilot.service.get_bootstrap` — ai_copilot
- `ai.copilot.service.get_conversation` — ai_copilot
- `ai.copilot.service.get_settings` — ai_copilot
- `ai.copilot.service.list_conversations` — ai_copilot
- `ai.copilot.service.list_documents` — ai_copilot
- `ai.copilot.service.save_document` — ai_copilot
- `ai.copilot.service.save_settings` — ai_copilot
- `ai.copilot.service.set_feedback` — ai_copilot
- `community.communication.discussion.action_follow` — community_communication
- `community.communication.discussion.action_post_comment` — community_communication
- `community.communication.discussion.action_react` — community_communication
- `community.communication.discussion.action_unfollow` — community_communication
- `compliance.dashboard.get_calendar_events` — compliance_audit_management
- `compliance.dashboard.get_compliance_reports` — compliance_audit_management
- `compliance.dashboard.get_dashboard_data` — compliance_audit_management
- `fire.safety.dashboard.compute_compliance` — fire_safety_management
- `fire.safety.dashboard.get_dashboard_data` — fire_safety_management
- `integration.iot.automation.execution.action_manual_override` — integration_iot_management
- `integration.iot.dashboard.get_automation_data` — integration_iot_management
- `integration.iot.dashboard.get_dashboard_data` — integration_iot_management
- `integration.iot.dashboard.get_devices_data` — integration_iot_management
- `integration.iot.dashboard.get_energy_data` — integration_iot_management
- `integration.iot.dashboard.get_lookups` — integration_iot_management
- `integration.iot.dashboard.get_systems_data` — integration_iot_management
- `integration.iot.device.action_archive` — integration_iot_management
- `integration.iot.device.action_set_fire_condition` — integration_iot_management
- `integration.iot.device.action_set_hvac` — integration_iot_management
- `integration.iot.energy.opportunity.action_apply` — integration_iot_management
- `integration.iot.reading.ingest_reading` — integration_iot_management
- `integration.iot.schedule.action_create_from_ui` — integration_iot_management
- `analytics.alert.action_acknowledge` — reports_analytics
- `analytics.alert.action_create_from_ui` — reports_analytics
- `analytics.alert.ui_row` — reports_analytics
- `analytics.dashboard.action_create_from_ui` — reports_analytics
- `analytics.dashboard.service.get_analytics_dashboard` — reports_analytics
- `analytics.dashboard.service.get_bootstrap` — reports_analytics
- `analytics.dashboard.service.get_cross_module` — reports_analytics
- `analytics.dashboard.service.get_financial_analytics` — reports_analytics
- `analytics.dashboard.service.get_management_dashboard` — reports_analytics
- `analytics.dashboard.service.get_operational_analytics` — reports_analytics
- `analytics.dashboard.service.get_predictive_analytics` — reports_analytics
- `analytics.dashboard.service.get_trend_analysis` — reports_analytics
- `analytics.dashboard.service.run_analysis` — reports_analytics
- `analytics.dashboard.service.search_reports` — reports_analytics
- `analytics.kpi.get_dashboard_payload` — reports_analytics
- `analytics.query.engine.get_source_schema` — reports_analytics
- `analytics.report.action_generate` — reports_analytics
- `analytics.report.action_preview_config` — reports_analytics
- `analytics.report.action_save_draft` — reports_analytics
- `analytics.report.ui_detail` — reports_analytics
- `analytics.report.execution.ui_payload` — reports_analytics
- `analytics.report.schedule.action_create_from_ui` — reports_analytics

## Manifest `assets` (FMS)

### ai_copilot

```python
"assets": {
        "web.assets_backend": [
            "ai_copilot/static/src/scss/_tokens.scss",
            "ai_copilot/static/src/scss/ai_copilot.scss",
            "ai_copilot/static/src/owl/ui/**/*",
            "ai_copilot/static/src/owl/screens/**/*",
        ],
    },
}
```

### community_communication

```python
"assets": {
        "web.assets_backend": [
            "community_communication/static/src/scss/_tokens.scss",
            "community_communication/static/src/scss/community_communication.scss",
            "community_communication/static/src/owl/utils.js",
            "community_communication/static/src/owl/cc_action.js",
            "community_communication/static/src/owl/ui/**/*",
            "community_communication/static/src/owl/screens/**/*",
        ],
        "web.assets_frontend": [
            "community_communication/static/src/portal/portal.scss",
        ],
    },
}
```

### compliance_audit_management

```python
"assets": {
        "web.assets_backend": [
            "compliance_audit_management/static/src/scss/_tokens.scss",
            "compliance_audit_management/static/src/scss/compliance_audit.scss",
            "compliance_audit_management/static/src/owl/ui/**/*",
            "compliance_audit_management/static/src/owl/screens/**/*",
        ],
    },
}
```

### fire_safety_management

```python
"assets": {
        "web.assets_backend": [
            "fire_safety_management/static/src/scss/_tokens.scss",
            "fire_safety_management/static/src/scss/fire_safety.scss",
            "fire_safety_management/static/src/owl/ui/**/*",
            "fire_safety_management/static/src/owl/screens/**/*",
        ],
    },
}
```

### integration_iot_management

```python
"assets": {
        "web.assets_backend": [
            "integration_iot_management/static/src/scss/_tokens.scss",
            "integration_iot_management/static/src/scss/integration_iot.scss",
            "integration_iot_management/static/src/owl/ui/**/*",
            "integration_iot_management/static/src/owl/screens/**/*",
        ],
    },
}
```

### mobile_application

```python
"assets": {
        "web.assets_backend": [
            "mobile_application/static/src/mobile_app.scss",
            "mobile_application/static/src/utils/**/*.js",
            "mobile_application/static/src/services/**/*.js",
            "mobile_application/static/src/components/**/*.js",
            "mobile_application/static/src/components/**/*.xml",
            "mobile_application/static/src/screens/**/*.js",
            "mobile_application/static/src/screens/**/*.xml",
            "mobile_application/static/src/mobile_app.xml",
            "mobile_application/static/src/screens/mobile_screens.xml",
            "mobile_application/static/src/mobile_app.js",
        ],
    },
}
```

### reports_analytics

```python
"assets": {
        "web.assets_backend": [
            "reports_analytics/static/src/scss/_tokens.scss",
            "reports_analytics/static/src/scss/reports_analytics.scss",
            "reports_analytics/static/src/owl/ui/**/*",
            "reports_analytics/static/src/owl/screens/ra_screen.js",
            "reports_analytics/static/src/owl/screens/**/*",
        ],
    },
}
```

### fire_safety_community

No `assets` key (backend-only).
