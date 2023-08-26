# govulncheck

Downgrade to a dependency with a known vulnerability:

```
go get golang.org/x/text@v0.3.5
```

Install `govulncheck`:

```
go install golang.org/x/vuln/cmd/govulncheck@latest
```

Run `govulncheck`:

```
govulncheck .
```

Output:

```
Scanning your code and 50 packages across 1 dependent module for known vulnerabilities...

Vulnerability #1: GO-2021-0113
    Out-of-bounds read in golang.org/x/text/language
  More info: https://pkg.go.dev/vuln/GO-2021-0113
  Module: golang.org/x/text
    Found in: golang.org/x/text@v0.3.5
    Fixed in: golang.org/x/text@v0.3.7
    Example traces found:
      #1: main.go:12:29: vuln.main calls language.Parse

=== Informational ===

Found 1 vulnerability in packages that you import, but there are no call
stacks leading to the use of this vulnerability. You may not need to
take any action. See https://pkg.go.dev/golang.org/x/vuln/cmd/govulncheck
for details.

Vulnerability #1: GO-2022-1059
    Denial of service via crafted Accept-Language header in
    golang.org/x/text/language
  More info: https://pkg.go.dev/vuln/GO-2022-1059
  Module: golang.org/x/text
    Found in: golang.org/x/text@v0.3.5
    Fixed in: golang.org/x/text@v0.3.8

Your code is affected by 1 vulnerability from 1 module.

Share feedback at https://go.dev/s/govulncheck-feedback.
```

Update vulnerable dependency:

```
go get golang.org/x/text@latest
```

Check vulnerabilities again:

```
govulncheck .
```

Output:

```
Scanning your code and 50 packages across 1 dependent module for known vulnerabilities...

No vulnerabilities found.

Share feedback at https://go.dev/s/govulncheck-feedback.
```