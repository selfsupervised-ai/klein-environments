# Klein environments

Signed, content-addressed Klein environment packages (`klein.environment-index.v1`).

**Trust root (Ed25519 public key, pin it yourself):** `6f33dafb16eb437cf80f52167363de21264cd61b0909fd6196c68a58ef319d9b`

Index sequence: 1. Refuse anything lower than the last sequence you saw.

| Entry | Package digest |
|---|---|
| native-parser | sha256:3612900fac070ca71608e515f41f293b25495810b48c99b936230d67d3f6637e |

Verify a clone:

```
klein environment verify index.json --signature index.json.sig --trust-root 6f33dafb16eb437cf80f52167363de21264cd61b0909fd6196c68a58ef319d9b --min-sequence 1 --packages .
```

Layout: `index.json`, `index.json.sig`, `packages/<package digest>/` (`environment.json`,
`harbor/` the public part of the Harbor task; hidden tests are referenced by digest only). A Hugging Face dataset
repository or Prime Environments Hub mirror carries the same relative layout; see Klein's
`spec/registry/v1/README.md`.
