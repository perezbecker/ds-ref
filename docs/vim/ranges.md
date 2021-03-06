# ranges

[source](https://vim.fandom.com/wiki/Ranges)

A _range_ permits a command to be applied to a group of lines in the current buffer. For most commands, the default range is the current line. For example:

- `:s/old/new/g` changes all old to new in the current line
- `:11,15s/old/new/g` changes lines 11 to 15 inclusive
- `:%s/old/new/g` changes all lines

## Examples

|Range | Description | Example |
|--|--|--|
|`21`| line 21 |`:21s/old/new/g`|
|`1`| first line |`:1s/old/new/g`|
|`$`| last line |`:$s/old/new/g`|
|`.`| current line |`:.w single.txt`|
|`%`| all lines (same as 1,$) |`:%s/old/new/g`|
|`21,25`| lines 21 to 25 inclusive |`:21,25s/old/new/g`|
|`21,$`| lines 21 to end |`:21,$s/old/new/g`|
|`.,$`|	current line to end	|`:.,$s/old/new/g`|
|`.+1,$`| line after current line to end |`:.+1,$s/old/new/g`|
|`.,.+5`| six lines (current to current+5 inclusive) |`:.,.+5s/old/new/g`|
|`.,.5`| same (.5 is interpreted as .+5) |`:.,.5s/old/new/g`|