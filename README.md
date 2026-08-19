# cos-wpt-remote.github.io

A cross-origin mirror of [tomayac/cos-wpt](https://github.com/tomayac/cos-wpt), which
runs the Cross-Origin Storage web platform tests.

Those tests need origins other than the one serving the runner —
`HTTPS_REMOTE_ORIGIN` and `HTTPS_NOTSAMESITE_ORIGIN` — and a GitHub account
gets one origin. Hence this organisation, whose only purpose is to be a
different one. Serving from an organisation site rather than a project page
matters too: only a service worker scoped at `/` can answer the root-absolute
paths a couple of the tests hard-code.

This repository holds no copy of the site. [`sync.yml`](.github/workflows/sync.yml)
publishes the source repository directly, hourly and on demand.
