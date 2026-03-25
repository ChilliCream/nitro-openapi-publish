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
```

## Inputs

| Name                    | Required | Description                                            |
| ----------------------- | -------- | ------------------------------------------------------ |
| `tag`                   | Yes      | The tag of the OpenAPI collection version              |
| `stage`                 | Yes      | The name of the stage                                  |
| `openapi-collection-id` | Yes      | The ID of the OpenAPI collection                       |
| `api-key`               | Yes      | API key for authentication                             |
| `force`                 | No       | Will not ask for confirmation on deletes or overwrites |
| `wait-for-approval`     | No       | Wait for approval                                      |
| `cloud-url`             | No       | The URL of the Nitro registry                          |

If you self-host Nitro or use a dedicated hosted instance, you can specify the `cloud-url` input to point to your instance.
