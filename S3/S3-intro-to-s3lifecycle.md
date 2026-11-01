## Definition
S3 Lifecycle allows you to automate the storage class changes, archival or deletion of objects
- Can be used together with versioning
- Can be applied to both current and previous versions


There are two type of actions:
- Transition actions
- Expiring actions 
*example*: we can write a rule that goes "objects after 7 days move to glacier" and then "after 365 days permanently delete the object"


Lifecycle Rule Actions
- Move current versions of objects between storage classes
- Move noncurrent versions of objects between storage classes
- Expire current versions of objects
- Permanently delete noncurrent versions of objects