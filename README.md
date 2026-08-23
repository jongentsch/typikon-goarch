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

The pack also contains a 2026 evidence baseline for twelve major feasts: the
nine fixed feasts from the Nativity of the Theotokos through Dormition, plus
Palm Sunday, Ascension, and Pentecost. Each feast compiles a complete dated
Digital Chant Stand proper-bundle reference for Vespers or Vesperal Liturgy,
Orthros, and Divine Liturgy. The DCS output remains observed behavior; the
general claim is limited to DCS publishing those service bundles.

Fixed feasts and the three Paschal-cycle observances are discovered
automatically through the typed `date.fixed` and `date.paschal_offset` forms;
conformance tests separately prove their 2026 offsets from calculated Orthodox
Pascha.

No liturgical text is included. The materials are semantic specifications only.

```console
cd ../typikon-engine
cargo run -p typikon-cli -- validate ../typikon-goarch
cargo run -p typikon-cli -- compile-date --pack ../typikon-goarch \
  --date 2026-12-25
```

The pack maps the calculated eight-tone ordinal to Byzantine mode names; the
caller does not supply the mode.

License selection for this tradition pack is pending and independent of the
engine's license.

GitHub Actions validates the pack with the sibling engine's CLI and exercises
ordinary-Sunday and major-feast service bundles on every push and pull request.
