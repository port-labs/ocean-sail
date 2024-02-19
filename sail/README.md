<!-- action-docs-header action="action.yml" -->

<!-- action-docs-header action="action.yml" -->

<!-- action-docs-description action="action.yml" -->
## Description

Runs the Ocean Sail command for a specific type of integration
<!-- action-docs-description action="action.yml" -->

<!-- action-docs-inputs action="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `type` | <p>The type of the integration to run</p> | `true` | `""` |
| `version` | <p>The version of the integration to run</p> | `false` | `latest` |
| `port_client_id` | <p>The port client id</p> | `true` | `""` |
| `port_client_secret` | <p>The port client secret</p> | `true` | `""` |
| `initialize_port_resources` | <p>Should ocean try to create the default blueprints, pages &amp; integration config for the integration</p> | `false` | `true` |
| `event_listener_type` | <p>The type of the event listener to use</p> | `false` | `ONCE` |
| `integration_config` | <p>Changing configuration between different integration types</p> | `false` | `{}` |
| `additional_env_vars` | <p>Additional environment variables to pass to the integration</p> | `false` | `{}` |
| `platform` | <p>The platform to run the integration on</p> | `false` | `linux/amd64` |
| `container_registry` | <p>The container registry to pull the image from</p> | `false` | `ghcr.io/port-labs` |
<!-- action-docs-inputs action="action.yml" -->

<!-- action-docs-outputs action="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `exit_code` | <p>The exit code of the Ocean Sail command</p> |
<!-- action-docs-outputs action="action.yml" -->

<!-- action-docs-runs action="action.yml" -->
## Runs

This action is a `composite` action.
<!-- action-docs-runs action="action.yml" -->