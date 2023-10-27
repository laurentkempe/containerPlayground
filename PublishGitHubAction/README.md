# Publish .NET Docker images using .NET SDK and GitHub Actions

You can read more about it on the blog post "[Publish .NET Docker images using .NET SDK and GitHub Actions](https://laurentkempe.com/)".

# GitHub Actions

See [.github/workflows/publish-to-github-container-registry.yml](https://github.com/laurentkempe/containerPlayground/blob/main/PublishGitHubAction/.github/workflows/publish-to-github-container-registry.yml)


# Publish locally

Using the `local` publish profile, defined in the file `Properties\PublishProfiles\local.pubxml`, you can publish the application to the local docker container.

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=local -c Release
```

# Publish to GitHub Docker Container from CLI

Using the `github` publish profile, defined in the file `Properties\PublishProfiles\github.pubxml`, you can publish the application to [GitHub docker container](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry).

You will need to login to the GitHub docker registry using a [Personal Access Token](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-in-a-github-actions-workflow). To create one follow the instruction on [Creating a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token) specifying `write:packages`, `read:packages` and `delete:packages`.

```bash
docker login ghcr.io -u laurentkempe
```

Then you can publish the application to the GitHub docker container.

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=github -c Release
```

