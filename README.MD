This repository compiles Mastodon into a ready-to-use deb package, all using github actions. The resulting deb is automatically published as a release asset (see https://github.com/laszlovl/mastodon-build/releases) and because github itself is not accessible over ipv6, the latest version is also published to github pages (see https://laszlovl.github.io/mastodon-build/mastodon-core_4.2.8_amd64.deb).

Installing this package will deploy Mastodon's source code and the compiled assets into `/opt/mastodon`, but it doesn't provide configuration or service definitions. For automated deployment of a full-fledged Mastodon environment, refer to https://github.com/laszlovl/mastodon-ansible-scalable.

Mastodon is compiled using:
  * Ubuntu 22.04
  * Ruby 3.0 (from the Ubuntu repositories)
  * Node.js 18
    
The deb built by this repository will only function properly on systems with these same software versions. Want to create your own build? Simply fork this repository, update `.github/workflows/mastodon-build.yml` accordingly, push a tag in the `vX.Y.Z` pattern, then github will automatically compile & publish it for you.
