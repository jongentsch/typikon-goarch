# Observance organization

The engine recursively loads YAML beneath this directory. Every jurisdiction
pack uses the same maintenance taxonomy:

```text
observances/
|-- feasts/
|   |-- major/
|   |-- minor/
|   |-- forefeasts/
|   |-- afterfeasts/
|   `-- leavetakings/
|-- saints/
|   |-- apostles/
|   |-- confessors/
|   |-- equal-to-apostles/
|   |-- fools-for-christ/
|   |-- hierarchs/
|   |-- martyrs/
|   |-- monastics/
|   |-- prophets/
|   |-- righteous/
|   |-- synaxes/
|   `-- unmercenaries/
|-- angels/
|   |-- archangels/
|   `-- hosts/
|-- icons/
|   |-- christ/
|   |-- saints/
|   `-- theotokos/
|-- councils/
|   |-- ecumenical/
|   `-- local/
`-- commemorations/
    |-- dedications/
    |-- departed/
    `-- historical-events/
```

Use the primary liturgical title in this pack's official calendar when a saint
has several titles. `martyrs/` includes great, hiero-, monastic, new, virgin,
and other martyr titles; `monastics/` includes saints styled venerable. Keep a
saint-centered event such as the finding or translation of relics with that
saint's subtype. Add a new subtype only when official pack data cannot fit one
of these categories cleanly.

These paths do not carry engine semantics. A document's stable `id` is its
reference key, and its YAML fields determine liturgical behavior.
