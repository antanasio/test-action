# AT - Random Number Generator

A composite GitHub Action that greets a user and generates a pseudo-random integer from 0 to 32767.

## Usage

```yaml
steps:
  - name: Generate a random number
    id: random
    uses: OWNER/test-action@v1
    with:
      user-name: Octocat

  - name: Display the result
    run: echo "Generated number: ${{ steps.random.outputs.generated-number }}"
```

Replace `OWNER` with your GitHub username or organization. Pinning the action to a full commit SHA is recommended for security-sensitive workflows.

## Inputs

| Name        | Required | Description                |
| ----------- | -------- | -------------------------- |
| `user-name` | Yes      | Name used in the greeting. |

## Outputs

| Name               | Description                            |
| ------------------ | -------------------------------------- |
| `generated-number` | Pseudo-random integer from 0 to 32767. |

## Publishing

This repository is structured as the action package. Make the repository public, create a release such as `v1`, and select **Publish this Action to the GitHub Marketplace** when drafting the release. GitHub requires the action name to be unique on Marketplace.

## License

MIT. See [LICENSE](LICENSE).