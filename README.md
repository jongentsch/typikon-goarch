# Experimental GOARCH tradition pack

[![CI](https://github.com/jongentsch/typikon-goarch/actions/workflows/ci.yml/badge.svg)](https://github.com/jongentsch/typikon-goarch/actions/workflows/ci.yml)

This is an engineering fixture for `typikon-engine`, not an approved or
complete GOARCH Typikon.

The pack defines complete ordered structures for Vespers, Great Vespers,
Orthros, and Divine Liturgy. Fixed and changeable components are explicit;
Divine Liturgy exposes Chrysostom and Basil forms. Rank profiles define which
components a major feast or six-stichera saint must supply.

Observances own their date, rank, and service material directly. The two
ordinary dated witnesses—Saint Paraskevi on 2026-07-26 and the translation of
Saint Stephen's relics on 2026-08-02—demonstrate observance-owned Lord-I-Call
material. No global leaf-resource ID is required.

Twelve major feasts are selected from fixed dates or Paschal offsets without a
feast parameter. Their Digital Chant Stand evidence is retained, but dated
2026 output is not reused as perennial runtime data. Until each proper is
normalized by component, compiled feast plans truthfully report
`requires_review` and name every unresolved component.

```console
cd ../typikon-engine
cargo run -p typikon-cli -- validate ../typikon-goarch
cargo run -p typikon-cli -- compile-date --pack ../typikon-goarch --date 2026-12-25
```

License selection is pending.
