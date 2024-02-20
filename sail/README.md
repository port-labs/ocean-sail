<!-- action-docs-header action="action.yml" -->

<!-- action-docs-header action="action.yml" -->

<!-- action-docs-description action="action.yml" -->
## Description

Runs the Ocean Sail command for a specific type of integration
<!-- action-docs-description action="action.yml" -->

Read more about the Ocean framework [here](https://ocean.getport.io/)

<!-- action-docs-inputs action="action.yml" -->
## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `type` | <p>The type of the integration to run</p> | `true` | `""` |
| `identifier` | <p>The identifier of the integration to run</p> | `false` | `""` |
| `port_client_id` | <p>The port client id</p> | `true` | `""` |
| `port_client_secret` | <p>The port client secret</p> | `true` | `""` |
| `initialize_port_resources` | <p>Should ocean try to create the default blueprints, pages &amp; integration config for the integration</p> | `false` | `true` |
| `event_listener_type` | <p>The type of the event listener to use</p> | `false` | `ONCE` |
| `config` | <p>The configuration for the integration</p> | `false` | `""` |
| `platform` | <p>The platform to run the integration on</p> | `false` | `linux/amd64` |
| `image` | <p>The image to run the integration from</p> | `false` | `""` |
| `version` | <p>The version of the integration to run</p> | `false` | `latest` |
<!-- action-docs-inputs action="action.yml" -->

<!-- action-docs-outputs action="action.yml" -->
## Outputs

| name | description |
| --- | --- |
| `exit_code` | <p>The exit code of the Ocean Sail command</p> |
<!-- action-docs-outputs action="action.yml" -->

## Available integration types

All available integration types are listed in the [Ocean documentation](https://ocean.getport.io/integrations-library/) and also can be found when trying to add a new Datasource in the Port UI.

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