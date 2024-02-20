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
| `platform` | <p>The platform to run the integration on</p> | `false` | `linux/amd64` |
| `container_registry` | <p>The container registry to pull the image from</p> | `false` | `ghcr.io/port-labs` |
<!-- action-docs-inputs action="action.yml" -->

## Integration configuration

To each integration type its specific configuration please use `env:` to set the configuration as environment variables.
Each environment variable should be prefixed with `OCEAN__INTEGRATION__CONFIG__` and the name of the variable in uppercase.

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

## Example usage

```yaml
- uses: ocean-github-action/sail@v1
  with:
    type: 'jira'
    port_client_id: ${{ secrets.PORT_CLIENT_ID }}
    port_client_secret: ${{ secrets.PORT_CLIENT_SECRET }}
    config: |
      jira_host: ${{ secrets.JIRA_HOST }}
      atlassian_user_email: ${{ secrets.ATLASSIAN_USER_EMAIL }}
      atlassian_user_token: ${{ secrets.ATLASSIAN_USER_TOKEN }}
```