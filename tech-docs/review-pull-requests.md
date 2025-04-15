---
hidden: true
---

# Review pull requests

## **Create a Webhook endpoint in SRE application**

1. In SRE application, click on the User initials on the top right and click ‘Settings’ in the options
2. In the Navigation, go to WebHooks
3. Click ‘Add webhook’
4. For App, select ‘GitHub’
5. Add a secret phrase and click Add
6. Copy the url

## **Add WebHook to the Repository:**

1. In GitHub for the Repository, click on the ‘Settings’ tab
2. Now go to ‘Webhooks’ from the left navigation
3. Click ‘Add Webhook’
4. For Payload URL, add the url copied from the previous step and note to add the domain to the url, ex. [https://acme-app.sre.ai/api/webhook/github/01cf0bdc-bd3a-4d16-a25c-ff85fcd30111](https://acme-app.sre.ai/api/webhook/github/01cf0bdc-bd3a-4d16-a25c-ff85fcd30111)
5. For Content Type, select application/json
6. Add the same secret phrase
7. For ‘Which events would you like to trigger this webhook?’ select ‘Let me select individual events.’
8. Check the ‘Pull requests’
9. Uncheck ‘Pushes’

## **Create Review Pull Request Flow**

1. In SRE application, click on the Flows in the navigation
2. Click ‘New’ and provide a name ex. review-pull-request
3. Click on the edit icon (pen)
4. Select the triggering event, in the left pane click on the card to select Webhook
5. For the App, click on the card to select ‘GitHub’
6. Now add a flow element by click on the plus icon (+)&#x20;
7. Select ‘Pull Request Exception’, and a flow element will be added
8. Click on the flow element to update the details
9. For Name, set ‘Check for Skip Test’
10. For Connection, select a GitHub connection
11. For Label, set ‘Skip Test’
12. For Criteria, set ‘Exclusive’
13. For Types, select the Metadata Types to be excluded for this Label
14. Now add a flow element by click on the plus icon (+) at the end
15. Select ‘Pull Request Exception’, and a flow element will be added
16. Click on the flow element to update the details
17. For Name, set ‘Check for Skip Reviews’
18. For Connection, select a GitHub connection
19. For Label, set ‘Skip Reviews’
20. For Criteria, set ‘Exclusive’
21. For Types, set the Metadata Types to be excluded for this Label
22. Click ‘Save’ or the ‘Check’ icon to save the flow
23. Now click on the ‘Circle’ icon besides the ‘Edit’ Icon to Activate the flow

\
\
