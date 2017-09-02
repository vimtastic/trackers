# Trackers

## Process

Edit the file and submit a pull request.


### Adding a new tracker

Append to the end of the file. Check existing entries before creating any new values for `Corp`, `Range`, `Model`, `Gen`, `Classes` or `SubClasses`. Always try to copy existing data wherever possible.


### Editing or creating a tracker

Edit the existing record.


### Company name change

Mark the old entries as `inactive` and create new entries. For example:

Old entry:

```
ID	PrevID	Status	DateCreated	DateUpdated	Parent	Corp	Range	Model	Gen	Classes	SubClasses	Functions
123	null	active	2017-09-01	2017-09-02	null	Withings	null	Body	1	scales	null	3
```

Updated and new entries:

```
ID	PrevID	Status	DateCreated	DateUpdated	Parent	Corp	Range	Model	Gen	Classes	SubClasses	Functions
123	null	inactive	2017-09-01	2017-09-03	null	Withings	null	Body	1	scales	null	3
124	123	active	2017-09-01	2017-09-03	null	Nokia	Health	Body	1	scales	null	3
```


## File format

The format is basically tab-separated values. However, some fields can contain comma-separated values. These fields are indicated by their names being plurals: `Classes`, `SubClasses`, and `Functions`. Leave no spaces before or after the commas. For example this is incorrect: `1, 2, 3`. The correct format would be: `1,2,3`.


### Fields and types


| Field  | Explanation | Type | Examples | Incorrect examples |
|--------|-------------|------|----------|--------------------|
| ID     | Unique, sequential. | Int  | 123     | "123"<br>Twelve<br> 7 (leading or trailing space) |
| PrevID | null or previous ID where a product or company has been replaced. | Int or null  | null | "123"<br>Twelve<br> 7 (leading or trailing space) |
| Status | Active if the product is currently available. Inactive if not. | active or inactive | active | null |
| DateCreated | Date of record creation (not of product creation). | ISO 8601 date string. | 2017-31-10 | 10/31/2017 |
| DateUpdated | Date of record update (not of product update). | ISO 8601 date string. | 2017-31-10 | 10/31/2017 |
| Parent | Parent company of `corp`. | String | null | "" |
| Corp | Corporation selling the product. | String | Apple | 1 |
| Range |  |  |  |  |
| Model |  |  |  |  |
| Gen |  |  |  |  |
| Classes |  |  |  |  |
| SubClasses |  |  |  |  |
| Functions | Comma-separated IDs referring to entries in `functions.tsv` | Comma-separated ints. | 1,2,3<br>null | 1, 2, 3 (do not insert spaces) |



## Examples

Insert a new tracker:

```
ID	PrevID	Status	DateCreated	DateUpdated	Parent	Corp	Range	Model	Gen	Classes	SubClasses	Functions
123	null	active	2017-09-01	2017-09-02	null	Withings	null	Body	1	scales	null	3
```

