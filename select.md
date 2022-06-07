# select
Select or deselect access points and/or stations for targeted attacks. You must provide a comma separated list of indices of the desired access points and/or stations from [listap](listap).  
Any specified indices which were **NOT** already `selected` will become `selected`. Any specified indices which were already `selected` will no longer be `selected`

## Usage
```select [-a <CSL of target indices>] | [-s <CSL of target indices>]```

#### Arguments
| Argument | Required/Optional | Description |
| -------- | ----------------- | ----------- |
| `-a <CSL of target indices>` | Optional | The index numbers of the access points shown with [listap](listap) |
| `-s <CSL of target indices>` | Optional | The index numbers of the stations shown with (TBD) |

#### Example
`select -a 1,3,5`
