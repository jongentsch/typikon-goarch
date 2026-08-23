# Observance organization

The engine recursively loads YAML beneath this directory.

- `feasts/major/` contains major feasts.
- `feasts/minor/` is reserved for minor feasts.
- `saints/<type>/` groups saints by a practical subtype such as `martyrs/`,
  `monastics/`, or `hierarchs/`.
- Other general types may use the same pattern when needed.

These paths are a maintenance taxonomy only. A document's stable `id` is its
reference key and its YAML fields determine liturgical behavior.
