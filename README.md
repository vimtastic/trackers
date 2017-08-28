# Trackers


## Adding a tracker

The ID must be _unique_ and _sequential_.


## Removing a tracker

Do _NOT_ remove a tracker. Simply set its status to be `inactive`.


## Renaming a tracker

Create a new tracker, and set its `product [ { "previous_id": } ]` to point to the ID of the old tracker. Set the status of the old tracker to be `inactive`. Do _NOT_ delete the old tracker.
