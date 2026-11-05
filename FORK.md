# Temporary module publication

This root module follows upstream `tmaxmax/go-sse` master at
`fb578c33b9afebac952ff874bd6e422c094cf2c1`, with the EOF correction and regression
tests in [PR #61](https://github.com/tmaxmax/go-sse/pull/61).
Module and self-import paths are renamed to `github.com/CaliLuke/go-sse` so
ordinary Go module resolution can fetch the correction without replacements.

Only blank lines dispatch events. EOF discards incomplete final events, while
reader failures and the connection retry policy retain their error behavior.
Return to the upstream module when a stable release includes this correction
and passes the EOF, chunk-boundary, connection and reader-error regressions.
