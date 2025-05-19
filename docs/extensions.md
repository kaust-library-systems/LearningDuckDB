## Extensions

Checking the extensions available

```
D SELECT extension_name, loaded, installed
  from duckdb_extensions()
  ORDER BY installed DESC, loaded DESC;
┌──────────────────┬─────────┬───────────┐
│  extension_name  │ loaded  │ installed │
│     varchar      │ boolean │  boolean  │
├──────────────────┼─────────┼───────────┤
│ autocomplete     │ true    │ true      │
(...)
│ ui               │ false   │ false     │
│ vss              │ false   │ false     │
├──────────────────┴─────────┴───────────┤
│ 25 rows                      3 columns │
└────────────────────────────────────────┘
D
```

Loading the `httpfs` extension

```
D install httpfs;
100% ▕████████████████████████████████████████████████████████████▏
D
D load httpfs;
D SELECT extension_name, loaded, installed
  from duckdb_extensions()
  ORDER BY installed DESC, loaded DESC;
┌──────────────────┬─────────┬───────────┐
│  extension_name  │ loaded  │ installed │
│     varchar      │ boolean │  boolean  │
├──────────────────┼─────────┼───────────┤
│ autocomplete     │ true    │ true      │
(...)
│ httpfs           │ true    │ true      │
(...)
```
