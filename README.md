# Info
Project is provided by Loupe  
https://loupe.team  
info@loupe.team  
1-800-240-7042  

# Description
StarterAsProject is a minimal starter Automation Studio project used to bootstrap new application from a known starting point. It is used by LPM when creating new projects. 

# Installation
To install the project using the Loupe Package Manager (LPM), in an empty directory run `lpm init`, and when prompted confirm with yes. Alternately, you can run `lpm install starterasproject`. For more information about LPM, see https://loupeteam.github.io/LoupeDocs/tools/lpm.html

# Releasing a new version
Versions are published to npm by the [Publish Package](.github/workflows/publish.yml) workflow, which runs whenever a tag matching `v*` is pushed.

To cut a new release, use `npm version` to bump the version in `package.json` and create the matching git tag, then push the tag:

```sh
# pick one based on the change
npm version patch   # e.g. 2.0.0 -> 2.0.1
npm version minor   # e.g. 2.0.0 -> 2.1.0
npm version major   # e.g. 2.0.0 -> 3.0.0

git push --follow-tags
```

Pushing the tag triggers the workflow, which publishes the package to the [loupeteam GitHub Packages registry](https://github.com/orgs/loupeteam/packages) using the built-in `GITHUB_TOKEN`.

## Licensing

This project is licensed under the [MIT License](LICENSE).