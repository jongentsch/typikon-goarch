# Experimental GOARCH tradition pack

This is a runtime resource pack for the sibling `typikon-engine` project. It is
an engineering fixture, not an approved or complete GOARCH Typikon.

The one case records observed Digital Chant Stand output for the civil evening
of 2026-07-25 (liturgical date 2026-07-26, St Paraskevi). Its authority record
is deliberately typed `observed_behavior`: the fixture checks whether the
compiler reproduces production output, but it does not claim that DCS explains
the governing rubric.

No liturgical text is included. The materials are semantic specifications only.

```console
cd ../typikon-engine
cargo run -p typikon-cli -- validate ../typikon-goarch
cargo run -p typikon-cli -- compile-service --pack ../typikon-goarch \
  --date 2026-07-25 --service great_vespers --tone grave
```

License selection for this tradition pack is pending and independent of the
engine's license.
