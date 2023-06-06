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

Error 02
---------
- [Deployment 'a813j00000000jhAAE': Changes detected in target branch 'uat' after creation of the promotion branch     'promotion/P08316- DeployP08316UAT2', auto merge successfully performed to incorporate the last changes to the deployment.
- [FlowDefinition PolicyCreatePolicyStatusChangeEvent] Flow Definition will be used to Activate the Flow.
- [FieldSet Quote.vlocity_ins__QuoteDetail] In field: IQC1PolicyId_c no CustomField named Quote.IQC1PolicyId_c found   [MatchingRule Account. DuplicateBusinessAccountRule] Change the matching rule status separately from other changes.
- [MatchingRule PersonAccount. Duplicate PersonAccountRule] The filter logic 1 AND 2 AND 3 AND 4 AND 5 AND 6 AND 7 AND 8 AND 9 AND 10 is invalid.
- [DuplicateRule Account. BusinessAccount DuplicateCheck] The filter logic 1 AND 2 AND 3 AND 4 AND 5 AND 6 AND 7 AND 8 AND 9 AND 10 is invalid.
- [DuplicateRule PersonAccount. PersonAccount] The filter logic 1 AND 2 AND 3 AND 4 AND 5 AND 6 AND 7 AND 8 AND 9 AND 10 is invalid.

Solution
--------
To resolve the matching rule and duplicate rule errors, follow these steps:

1. Deactivate the rules in both the target and source org:
   - Navigate to the setup area of your org.
   - Search for "Matching Rules" and "Duplicate Rules".
   - Locate the rules mentioned in the error messages: "DuplicateBusinessAccountRule", "Duplicate PersonAccountRule", "BusinessAccount DuplicateCheck", and "PersonAccount".
   - Deactivate these rules by modifying their status or disabling them.

2. Add the "IQC1PolicyId__c" field in the commits:
   - Identify the relevant object or field where the "IQC1PolicyId__c" field should be added.


