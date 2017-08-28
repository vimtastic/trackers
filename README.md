# Trackers


## Adding a tracker

The ID must be _unique_ and _sequential_.


## Removing a tracker

Do _NOT_ remove a tracker. Simply set its status to be `inactive`.


## Renaming a tracker

Create a new tracker, and set the old tracker's `product [ { "previous_id": } ]` to point to the ID of the new tracker. Do _NOT_ remove the old tracker, simply set its status to be `inactive`.
