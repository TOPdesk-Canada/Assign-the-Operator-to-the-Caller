# Assign-the-Operator-to-the-Caller

Summary:
- assigns the operator to the caller, based on their matching Dynamic Name. The API looks up the operator list, and assigns an operator to the card, if they have the same name as the caller.

Use Case:
- Make a form in the self service portal that is only available to a persons group that contains your the same persons as your operator list. Then you can make form for your operators (as persons) in the Self Service Portal(SSP), which will automatically be assigned to their respective operator account. This may be required because they prefer the mobile interface of the SSP or because they want to answer a bunch of questions directly through the form. The event that triggers this action is usually a new card using a dropdown value that is preassigned to the form, such as "Type": "Operator Form"
  
Explanation of Steps:
- Step 1 - Get Operator list
- Step 2 - Get details of Incident (caller dynamicName)
- Step 3 - Enter Operator ID if the Caller's dynamicName equals an Operator dynamicName from Step 1

Permissions for API Operator:
-API
--- REST API - Read
--- Application Passwords - Write
-Incident Management
--- First line incidents - Read, Write
--- Second line incidents - Read, write
-Supporting Files
--- Operators - Read

Variables:
-topdesk_user: The Operator account used to perform this action (e.g. ADMIN).
-topdesk_applicationpassword: Application password configured for the API user/operator.
-topdesk_url: URL to your TOPdesk environment.
