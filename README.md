# Paketo UBI9 Builders

## Paketo UBI 9 Buildpackless Builder

## `paketobuildpacks/ubi-9-buildpackless-builder`

This builder uses the [UBI 9 Base images](https://github.com/paketo-buildpacks/ubi-9-base-images) (a Red Hat UBI 9 base images) and contains **no buildpacks nor order groups**.
To use this builder, you must specify buildpacks and extensions at build time using whatever mechanisms your CNB platform of choice offers.

For example, with the `pack` CLI, use `--buildpack` or/and `--extension` as follows:

```
pack build nodejs-with-buildpackless-builder \
           --path ./app-dir \
           --buildpack paketobuildpacks/nodejs \
           --extension paketobuildpacks/ubi-nodejs-extension \
           --builder paketobuildpacks/ubi-9-buildpackless-builder
```

To see which versions of build and run images and the lifecycle are contained within a given builder version, see the [Releases](https://github.com/paketo-buildpacks/ubi-9-builder/releases) on this repo. This information is also available in the `builder.toml`.

For more information about this builder and how to use it, visit the [Paketo builder documentation](https://paketo.io/docs/builders/).
To learn about the stack included in this builder, visit the [Paketo stack documentation](https://paketo.io/docs/stacks/).
