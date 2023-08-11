# Publish locally

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=local -c Release
```

# Publish to GitHub

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=github -c Release
```