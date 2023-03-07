# TODO

TODO

You can read more about it on the blog post "[TODO](https://laurentkempe.com/)".

# Try

Using the `local` publish profile, defined in the file `Properties\PublishProfiles\local.pubxml`, you can publish the application to the local docker container.

```bash
dotnet publish --os linux --arch x64 -p:PublishProfile=local -c Release
```

