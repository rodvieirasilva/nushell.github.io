---
title: polars get-ordinal
categories: |
  dataframe
version: 0.94.0
dataframe: |
  Gets ordinal from date.
usage: |
  Gets ordinal from date.
feature: default
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# `polars get-ordinal` for [dataframe](/commands/categories/dataframe.md)

<div class='command-title'>Gets ordinal from date.</div>

## Signature

```> polars get-ordinal {flags} ```


## Input/output types:

| input | output |
| ----- | ------ |
| any   | any    |

## Examples

Returns ordinal from a date
```nu
> let dt = ('2020-08-04T16:39:18+00:00' | into datetime --timezone 'UTC');
    let df = ([$dt $dt] | polars into-df);
    $df | polars get-ordinal
╭───┬─────╮
│ # │  0  │
├───┼─────┤
│ 0 │ 217 │
│ 1 │ 217 │
╰───┴─────╯

```