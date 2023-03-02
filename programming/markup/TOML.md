[TOML](https://toml.io/en/) (Tom's Obvious Markup Language) is a [[markup]] language that is designed to be human readable and have un-ambiguous relations (looking at you [[YAML]]).


```TOML
key = "value"
regex = '\scool\s'
number = 5.3e5
# Comments
[dictionary]
	what = True
```

## Pros

- Easy to read and edit
- Strict definitions, unambiguous, looks very much like Python
- Like [[YAML]] works really well in small files, but it looks even better

## Cons
- No indenting guide, can lead to complex structures looking messy
- Nested dictionaries don't always look the best
- For large amounts of data it gets cluttered

## Further reading

- [Some TOML I've written that looks nice](https://github.com/DarkKronicle/Vibe/blob/main/sample-rules/filter.toml)