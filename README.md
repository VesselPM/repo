# Vessel `main`
The main repo for the Vessel app runtime.

## Submission
- Fork this repo
- Add your `.ves` named exactly `app.ves`
- Submit a PR
- Wait for approval from [a maintainer](maintainers.txt). Please don't go and spam them.

## Submission Rules
To be filled in. We don't have rules right now, but eventually will. Just make sure you're authorized to publish the Vessel package for now.

## How does this work internally?
Depends. This is a vague question lol.

### The GitHub repo
There's a GitHub action that runs on PR review, checks if the reviewer is a maintainer, remotely accesses the server, updates [`index.toml`](https://files.obsidianos.xyz/~neo/vessel/index.toml), and pushes the `.ves` file.

### The Vessel repo itself
It contains an [`index.toml`](https://files.obsidianos.xyz/~neo/vessel/index.toml) file with general metadata for the Vessel package, and a bunch of `.ves` files.

Example `index.toml`:
```toml
[packages.com.example.something]
version = "1.0.0"
url = "https://example.com/hello-1.0.0.ves"
description = "prints a greeting"
vessel_deps = ["com.example.libfoo", "org.example.libbar"]
```
