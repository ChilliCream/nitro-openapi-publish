# Nitro OpenAPI Publish

A GitHub Action that publishes OpenAPI documents to the Nitro registry.

## Usage

```yaml
- uses: ChilliCream/nitro-openapi-publish@v16
  with:
    tag: <tag>
    stage: <stage>
    openapi-collection-id: <openapi-collection-id>
    api-key: <api-key>
    # Optional
    force: false
    wait-for-approval: false
    cloud-url: <cloud-url>
```

## Inputs

| Name                    | Required | Description                                            |
| ----------------------- | -------- | ------------------------------------------------------ |
| `tag`                   | Yes      | The tag of the OpenAPI collection version              |
| `stage`                 | Yes      | The name of the stage                                  |
| `openapi-collection-id` | Yes      | The ID of the OpenAPI collection                       |
| `api-key`               | Yes      | API key for authentication                             |
| `force`                 | No       | Continue publishing even if breaking changes or validation errors are detected. |
| `wait-for-approval`     | No       | Require approval in the Nitro UI to continue publishing when breaking changes or validation errors are detected.                                      |
| `cloud-url`             | No       | The URL of the Nitro registry                          |

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
