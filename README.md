
# Deployment Error Catalog

Error 01
---------
- [Profile Business User] Unknown User Permission: SendExternalEmailAvailable
- [Admin.profile] key replaced with value 1 time(s)
- [Profile Admin] Unknown user permission: ManageEntitlements
Solution
--------
To resolve the error, run the following query:

```xml
- (?ms)<userPermissions>.*?<name>SendExternalEmailAvailable</name>.*?</userPermissions>
- (?ms)<userPermissions>.*?<name>ManageEntitlements</name>.*?</userPermissions>
- (?ms)<userPermissions>.*?<name>ManageEntitlements</name>.*?</userPermissions>
