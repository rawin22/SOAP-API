# SOAP API Service Definition

This repository contains the WSDL (Web Services Description Language) definition for the `GPWebService`. This service provides a comprehensive set of SOAP endpoints for managing customers, payments, FX deals, and user settings.

## Service Information

* **Service Name:** `GPWebService`
* **Target Namespace:** `http://tradesolutionsgroup.com/services`
* **WSDL File:** `IGPWebService1.xml`

## Available Endpoints

The service exposes the following operations:

### Event Notifications

* **`EventNotificationGetAllForItem`**: Retrieves all event notifications associated with a specific item.
* **`EventNotificationAddNotification`**: Adds a new event notification.
* **`EventNotificationDeleteNotification`**: Deletes an existing event notification.

### Customer Management

* **`CustomerGetSingle`**: Retrieves details for a single customer.
* **`CustomerGetSingleFromAlias`**: Retrieves details for a single customer using an alias.
* **`CustomerCreate`**: Creates a new customer record.
* **`CustomerCreateFromTemplate`**: Creates a new customer based on an existing template.
* **`CustomerUpdate`**: Updates an existing customer's information.

### Customer Account Aliases

* **`CustomerAccountAliasCreate`**: Creates a new alias for a customer account.
* **`CustomerAccountAliasListGet`**: Retrieves a list of aliases for a customer account.
* **`CustomerAccountAliasDelete`**: Deletes a customer account alias.
* **`CustomerAccountAliasSetDefault`**: Sets a specific alias as the default for a customer account.
* **`CustomerAccountAliasDoesAliasExist`**: Checks if a specific account alias already exists.
* **`GetCustomerAccountAliasList`**: Retrieves the list of customer account aliases.

### Bank & Directory

* **`BankDirectorySearch`**: Searches the bank directory for bank details.

### Item Attributes

* **`ItemAttributeCreateOrUpdate`**: Creates a new item attribute or updates it if it already exists.
* **`ItemAttributeGetAllForItem`**: Retrieves all attributes associated with a specific item.
* **`ItemAttributeDelete`**: Deletes a specific item attribute.

### Liquidation Preferences

* **`CustomerLiquidationPreferencesGetAll`**: Retrieves all liquidation preferences for a customer.
* **`CustomerLiquidationPreferencesUpdateAll`**: Updates all liquidation preferences for a customer.
* **`CustomerLiquidationPreferencesAddOrUpdateCurrency`**: Adds or updates a currency within the customer's liquidation preferences.
* **`CustomerLiquidationPreferencesRemoveCurrency`**: Removes a currency from the customer's liquidation preferences.

### Item Notes

* **`ItemNoteCreate`**: Creates a new note for an item.
* **`ItemNoteUpdate`**: Updates an existing item note.
* **`ItemNoteGetSingle`**: Retrieves a single item note.
* **`ItemNoteGetAllForItem`**: Retrieves all notes associated with a specific item.
* **`ItemNoteDelete`**: Deletes a specific item note.

### Incoming Payments

* **`IncomingPaymentCreate`**: Creates a record for an incoming payment.
* **`IncomingPaymentValidate`**: Validates the details of an incoming payment.
* **`IncomingPaymentGetSingle`**: Retrieves details of a single incoming payment.
* **`IncomingPaymentPost`**: Posts an incoming payment to the system.
* **`IncomingPaymentVerify`**: Verifies the status or details of an incoming payment.
* **`IncomingPaymentDelete`**: Deletes an incoming payment record.
* **`IncomingPaymentSearch`**: Searches for incoming payments based on criteria.

### Instant Payments

* **`InstantPaymentCreate`**: Creates a new instant payment.
* **`InstantPaymentPost`**: Posts an instant payment.
* **`InstantPaymentSearch`**: Searches for instant payments.
* **`InstantPaymentGetSingle`**: Retrieves details of a single instant payment.

### Deposits

* **`DepositCreate`**: Creates a new deposit record.

### User Management & Security

* **`UserSettingsGetSingle`**: Retrieves settings for a single user.
* **`UserPasswordReset`**: Resets a user's password.
* **`UserPasswordChange`**: Changes a user's password.
* **`UserUsernameChange`**: Changes a user's username.
* **`UserAccessRightTemplateApply`**: Applies an access right template to a user.
* **`UserAccessRightTemplateLink`**: Links a user to an access right template.
* **`UserAccessRightTemplateUnLink`**: Unlinks a user from an access right template.
* **`CustomerUserCreate`**: Creates a new user associated with a customer.
* **`BankUserSearch`**: Searches for bank users.
* **`CustomerUserSearch`**: Searches for customer users.
* **`UserDoesUsernameExist`**: Checks if a specific username already exists.
* **`UserAccessRightAddOrUpdate`**: Adds or updates specific access rights for a user.
* **`UserAccessRightDelete`**: Deletes specific access rights from a user.
* **`Authenticate`**: Authenticates a user (login).

### Account Information & Holds

* **`CustomerAccountStatementGetSingle`**: Retrieves a single account statement for a customer.
* **`CustomerAccountBalancesGet`**: Retrieves account balances for a customer.
* **`AccountHoldCreate`**: Creates a hold on an account.
* **`AccountHoldApply`**: Applies a hold to an account.
* **`AccountHoldRelease`**: Releases a hold from an account.
* **`AccountHoldDelete`**: Deletes an account hold record.
* **`GetCustomerAccountBalances`**: Retrieves customer account balances.
* **`AccountHoldGetSingle`**: Retrieves details of a single account hold.
* **`AccountHoldSearch`**: Searches for account holds.

### FX (Foreign Exchange) Deals

* **`FXDealQuoteCreate`**: Creates a quote for an FX deal.
* **`FXDealQuoteBook`**: Books an FX deal based on a quote.
* **`FXDealQuoteBookAndInstantDeposit`**: Books an FX deal and creates an instant deposit in one step.
* **`FXDealInstantDepositCreateAndPost`**: Creates and posts an instant deposit related to an FX deal.
* **`FXDealQuoteSearch`**: Searches for FX deal quotes.
* **`FXDealQuoteGetSingle`**: Retrieves a single FX deal quote.
* **`FXRatesGetTableRate`**: Retrieves the table rate for FX.
* **`FXRatesGetTableRateFromSymbol`**: Retrieves the table rate for FX using a currency symbol.
* **`FXDealSearch`**: Searches for booked FX deals.
* **`FXDealGetSingle`**: Retrieves details of a single FX deal.
* **`FXDealDelete`**: Deletes an FX deal.
* **`FXDealGetInstructionList`**: Retrieves the list of instructions for an FX deal.

### Currencies & Lists

* **`CurrencyListGetFXBuyCurrencies`**: Retrieves a list of currencies available for FX buying.
* **`CurrencyListGetFXSellCurrencies`**: Retrieves a list of currencies available for FX selling.
* **`CurrencyListGetPaymentCurrencies`**: Retrieves a list of currencies available for payments.
* **`CountryListGetPaymentCountries`**: Retrieves a list of countries available for payments.
* **`StateOrProvinceListGetAllForCountry`**: Retrieves all states or provinces for a specific country.
* **`NationalCodeListGetAll`**: Retrieves a list of all national codes.
* **`NationalCodeListGetAllForCurrency`**: Retrieves national codes relevant to a specific currency.
* **`ReasonsForPaymentGetAllForCountry`**: Retrieves valid reasons for payment for a specific country.

### File Attachments

* **`FileAttachmentAddFile`**: Uploads and adds a file attachment.
* **`FileAttachmentUpdateFileInfo`**: Updates information about an existing file attachment.
* **`FileAttachmentGetFileData`**: Retrieves the actual data (content) of a file attachment.
* **`FileAttachmentGetFileListForObject`**: Retrieves a list of files attached to a specific object.
* **`FileAttachmentDeleteFile`**: Deletes a file attachment.

### Outgoing Payments

* **`PaymentCreate`**: Creates a new outgoing payment.
* **`PaymentValidate`**: Validates an outgoing payment.
* **`PaymentSubmit`**: Submits an outgoing payment for processing.
* **`PaymentApproveFunds`**: Approves funds for a payment.
* **`PaymentVerify`**: Verifies an outgoing payment.
* **`PaymentAcceptWKYCMatches`**: Accepts WKYC (Watch List KYC) matches for a payment.
* **`PaymentRelease`**: Releases a payment.
* **`PaymentDelete`**: Deletes an outgoing payment.
* **`PaymentSearch`**: Searches for outgoing payments.
* **`PaymentGetSingle`**: Retrieves details of a single outgoing payment.
* **`PaymentGetSettlementHistory`**: Retrieves the settlement history for a payment.
* **`PaymentMarkAsTransmitted`**: Marks a payment as transmitted.

### White Label & System

* **`WhiteLabelProfileGetSingle`**: Retrieves a single white label profile.
* **`WhiteLabelProfileSearch`**: Searches for white label profiles.
* **`WKYCResultGetAllForItem`**: Retrieves all WKYC results for a specific item.
* **`WKYCResultDetailGetAll`**: Retrieves detailed WKYC results.
* **`GetLibraryVersion`**: Retrieves the version of the service library.
