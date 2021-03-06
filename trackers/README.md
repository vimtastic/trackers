# Trackers

## Process

Edit the file and submit a pull request.


### Adding a new tracker

Append to the end of the file. Check existing entries before creating any new values for any field other than `ProdID` or `ProdName`. Always try to copy existing data wherever possible.

The easiest way might be to copy-and-paste this file into a new spreadsheet in Excel, then copy and paste the whole thing back again. Excel should understand the tabs, and put everything into columns for you.

### Editing or creating a tracker

Edit the existing record.


### Company name change

In the old entries, update the `ProdActive` field to be empty, and create new entries. For example:

Old entry:

|ProdID|	ProdPrevID|	ProdName|	ProdRange|	ProdGen|	ProdActive|ProdPriceMin|ProdPriceMax|ProdDateCreated|	ProdDateUpdated|	CorpID|	CorpParentID|	CorpName|	Classes|	SubClasses|	Functions|
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
|1	|  |Body| | |TRUE|80|120|2017-09-01|2017-09-07|1|		|Withings|appliance|scales|1,2,3|

Updated and new entries:

|ProdID|	ProdPrevID|	ProdName|	ProdRange|	ProdGen|	ProdActive|ProdPriceMin|ProdPriceMax|	ProdDateCreated|	ProdDateUpdated|	CorpID|	CorpParentID|	CorpName|	Classes|	SubClasses|	Functions|
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
|1	|  |Body| | | |80|120|2017-09-01|2017-09-07|1|		|Withings|appliance|scales|1,2,3|
|2	|1 |Body| | |TRUE|80|120|2017-09-09|2017-09-09|2|		|Nokia|appliance|scales|2,3,4|


## File format

The format is basically tab-separated values. However, some fields can contain comma-separated values. These fields are indicated by their names being plurals: `Classes`, `SubClasses`, and `Functions`.

#### Classes and subclasses

To be refined. For now, there are only a few valid options:

| Class | Valid subclasses |
|--|--|
| `appliance` | `scales` |
| `device`    | `phone`  |
| `wearable`  | `watch`<br>`wristband` |
| `software`  | `app`<br>`web`<br>`desktop` |
