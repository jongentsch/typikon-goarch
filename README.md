# Experimental GOARCH tradition pack

[![CI](https://github.com/jongentsch/typikon-goarch/actions/workflows/ci.yml/badge.svg)](https://github.com/jongentsch/typikon-goarch/actions/workflows/ci.yml)

This is a runtime resource pack for the sibling `typikon-engine` project. It is
an engineering fixture, not an approved or complete GOARCH Typikon.

Two cases record observed Digital Chant Stand output for the civil evenings of
2026-07-25 (St Paraskevi) and 2026-08-01 (translation of St Stephen's relic).
Their authority records are deliberately typed `observed_behavior`: the
fixtures check whether the compiler reproduces production output, but they do
not claim that DCS explains the governing rubric.

Both records are categorized `dated_witness`, so their applicability is limited
to the stated liturgical date. This pack does not yet assert a reusable
`scoped_claim` for the arrangement.

No liturgical text is included. The materials are semantic specifications only.

```console
cd ../typikon-engine
cargo run -p typikon-cli -- validate ../typikon-goarch
cargo run -p typikon-cli -- compile-service --pack ../typikon-goarch \
  --date 2026-07-25 --service great_vespers --tone grave
```

License selection for this tradition pack is pending and independent of the
engine's license.

GitHub Actions validates the pack with the sibling engine's CLI and compiles
both dated observations on every push and pull request.
