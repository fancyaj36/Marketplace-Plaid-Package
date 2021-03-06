[![](https://scdn.rapidapi.com/RapidAPI_banner.png)](https://rapidapi.com/package/Plaid/functions?utm_source=RapidAPIGitHub_PlaidFunctions&utm_medium=button&utm_content=RapidAPI_GitHub)
# Plaid Package
Our technology makes it easy to access high-quality transaction data, validate account ownership, and mitigate risks in a user-friendly way.
* Domain: [plaid.com](https://plaid.com)
* Credentials: clientId,publicKey,secret

## How to get credentials: 
1. Register on [plaid.com](https://plaid.com).
2. After creation your account you will see api clientId,api publicKey and secret.
3. To get the publicToken you need to create [Plaid link](https://blog.plaid.com/plaid-link/) with your api publicKey.
4. After authorization, your publicToken will be visible in the GET parameters.

## Custom datatypes:
  |Datatype|Description|Example
  |--------|-----------|----------
  |Datepicker|String which includes date and time|```2016-05-28 00:00:00```
  |Map|String which includes latitude and longitude coma separated|```50.37, 26.56```
  |List|Simple array|```["123", "sample"]```
  |Select|String with predefined values|```sample```
  |Array|Array of objects|```[{"Second name":"123","Age":"12","Photo":"sdf","Draft":"sdfsdf"},{"name":"adi","Second name":"bla","Age":"4","Photo":"asfserwe","Draft":"sdfsdf"}] ```
 
 
## Plaid.getAccessToken
Exchange a Link publicToken for an API accessToken.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| publicToken| String     | Short-lived API token.

## Plaid.getSingleItem
The getSingleItem endpoint returns information about the status of an Item: Available products; Billed products; Error status; Institution ID ;Item ID; Webhook;

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.getAuth
The getAuth endpoint allows you to retrieve the bank account and routing numbers associated with an Item’s checking and savings accounts, along with high-level account data and balances.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.
| accountIds | List       | A list of accountIds to retrieve for the Item.Note: An error will be returned if a provided accountId is not associated with the Item.

## Plaid.getAccountsBalance
The getAccountsBalance endpoint returns the real-time balance for each of an Item’s accounts.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.
| accountIds | List       | A list of accountIds to retrieve for the Item.Note: An error will be returned if a provided accountId is not associated with the Item.

## Plaid.getAllInstitutions
Returns response containing details on all financial institutions currently supported by Plaid.

| Field       | Type       | Description
|-------------|------------|----------
| clientId    | credentials| Private API key from user dashboard.
| secret      | credentials| Private API key from user dashboard.
| accessToken | String     | A rotatable API token unique to a single Item.
| count       | Number     | The total number of Institutions to return. The minimum is 0 and the maximum is 500.
| offset      | Number     | The number of Institutions to skip before returning results. The minimum is 1. There is no maximum.
| ProductsType| List       | A list of accountIds to retrieve for the Item.Note: An error will be returned if a provided accountId is not associated with the Item.

## Plaid.getSingleInstitution
Returns response containing details on a specified financial institution currently supported by Plaid.

| Field        | Type       | Description
|--------------|------------|----------
| publicKey    | credentials| Public API key from user dashboard.
| institutionId| String     | Single institution id.

## Plaid.getCategories
Send a request to the getCategories endpoint to get detailed information on categories returned by Plaid. This endpoint does not require authentication.

No arguments.

## Plaid.searchInstitution
Returns response containing details on a specified financial institution currently supported by Plaid.

| Field       | Type       | Description
|-------------|------------|----------
| publicKey   | credentials| Public API key from user dashboard.
| productsType| List       | Filter the Institutions based on whether they support all products listed in products.
| querySearch | String     | The search query.Institutions with names matching the query are returned.

## Plaid.createWebhook
The createWebhook allows you to create the webhook associated with an Item.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.
| webhookUrl | String     | The new webhookUrl to associate with the Item.

## Plaid.updateWebhook
The updateWebhook allows you to update the webhook associated with an Item.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.
| webhookUrl | String     | The new webhookUrl to associate with the Item.

## Plaid.getAccounts
The getAccounts endpoint returns information about accounts.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.getPublicToken
If you need your user to take action to restore or resolve an error associated with an Item, generate a public token with the getAccounts.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.getAccountsTransactions
The getAccountsTransactions endpoint allows developers to receive user-authorized transaction data for credit and depository-type Accounts.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.
| startDate  | DatePicker | Starting date of transaction processing.
| endDate    | DatePicker | Ending date of transaction processing.
| count      | Number     | The total number of transactions to return.
| offset     | Number     | The number of transaction to skip before returning results.

## Plaid.rotateAccessToken
You can use the rotateAccessToken endpoint to rotate the accessToken associated with an Item.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.getIncome
The getIncome endpoint allows you to retrieve information pertaining to a Item’s income.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.getIdentity
The getIdentity endpoint allows you to retrieve various account holder information on file with the financial institution, including names, emails, phone numbers, and addresses.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.deleteItem
The deleteItem endpoint allows you to delete an Item

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

## Plaid.resetItemLogin
The resetItemLogin endpoint allows you put an Item in an ITEM_LOGIN_REQUIRED error state.

| Field      | Type       | Description
|------------|------------|----------
| clientId   | credentials| Private API key from user dashboard.
| secret     | credentials| Private API key from user dashboard.
| accessToken| String     | A rotatable API token unique to a single Item.

