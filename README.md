# Byways catalog

The published road catalog for [Byways](https://github.com/workwithnano/Byways), served by GitHub
Pages at **https://catalog.corduroying.com**.

**Generated. Do not edit by hand.** Everything here is written by `make catalog-deploy` and
`make catalog-promote` in the Byways repository, from `research/editorial-catalog.json`. See
`docs/PUBLISHING.md` there.

```text
production/manifest.json                      what shipping app builds read
production/releases/<catalogVersion>/catalog.json
staging/manifest.json                         what the app reads with the staging server picked in Debug settings
staging/releases/<catalogVersion>/catalog.json
```

A release directory is immutable once published. A deploy pushes the release first, waits until
it is served with the right SHA-256, and only then repoints `manifest.json`. The previous release
stays for rollback.
