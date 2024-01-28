# `ghcr.io/amp-buildpacks/move`

The Move Cloud Native Buildpack provides a set of collaborating buildpacks that
enable the building of a Move-based application.

## Included Buildpacks

- [`amp-buildpacks/aptos`](https://github.com/amp-buildpacks/aptos)
- [`paketo-buildpacks/procfile`](https://github.com/paketo-buildpacks/procfile)

## tl;dr

You can build your app with two steps:

1. Run `pack build <image-name> -b ghcr.io/amp-buildpacks/move`. An image will
   be generated that you can run.
2. Run the image with `docker run -it <image-name>`.

By default, the Move buildpack will add process types for all of the binary
projects in your workspace. You may optionally add a
[`Procfile`](https://paketo.io/docs/howto/configuration/#procfiles) though if
you need to customize the start command for your container.

## What's Included

### A Meta Buildpack

Included in this repo is a `buildpack.toml` that defines the Move meta
buildpack. It allows you to reference all of the Move related CNBs in one
convenient way & know that the order is set correctly.

This is available through a pre-built docker image on [Amphitheatre Buildpacks
Packages](https://github.com/orgs/amp-buildpacks/packages).

To use: `pack build <image-name> -b ghcr.io/amp-buildpacks/move`

## Contributing

If anything feels off, or if you feel that some functionality is missing, please
check out the [contributing
page](https://docs.amphitheatre.app/contributing/). There you will find
instructions for sharing your feedback, building the tool locally, and
submitting pull requests to the project.

## License

Copyright (c) The Amphitheatre Authors. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits

Heavily inspired by https://github.com/paketo-community/rust
