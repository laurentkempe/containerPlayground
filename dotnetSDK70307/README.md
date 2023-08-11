# Publish container of Minimal .NET 7 web project using .NET SDK container built-in support

## Publish locally

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=local -c Release
```

## Publish to GitHub

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=github -c Release
```