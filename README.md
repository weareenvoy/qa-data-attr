# Reference Sheet
## Custom data attributes used in automated tests.
This document defines the values used for the `data-test` attribute for respective HTML elements. This attribute will be used by automated tests to interact with page elements.

To learn more about using the attributes view the [Usage](https://github.com/weareenvoy/qa-data-attr#usage) section below.


### Reference Organization
Each attribute value will be listed under the web page or web page component where it would be visually rendered.

[General](https://github.com/weareenvoy/qa-data-attr#general)

&nbsp;&nbsp;&nbsp;&nbsp;[Header](https://github.com/weareenvoy/qa-data-attr#header)

&nbsp;&nbsp;&nbsp;&nbsp;[Privacy Terms Policies Pages](https://github.com/weareenvoy/qa-data-attr#privacy-terms-policies-pages)

&nbsp;&nbsp;&nbsp;&nbsp;[Navigation](https://github.com/weareenvoy/qa-data-attr#navigation)

&nbsp;&nbsp;&nbsp;&nbsp;[Notification Sign Up Form](https://github.com/weareenvoy/qa-data-attr#notification-sign-up-formsign-up-form)

[Login Page](https://github.com/weareenvoy/qa-data-attr#login-page)

[Create Account Page](https://github.com/weareenvoy/qa-data-attr#create-account-page)

[Checkout Page](https://github.com/weareenvoy/qa-data-attr#checkout-page)

&nbsp;&nbsp;&nbsp;&nbsp;[Billing Form](https://github.com/weareenvoy/qa-data-attr#billing-form)

&nbsp;&nbsp;&nbsp;&nbsp;[Credit Card Form](https://github.com/weareenvoy/qa-data-attr#credit-card-form)

[Product Page](https://github.com/weareenvoy/qa-data-attr#product-page)
<br>

### General

#### Header
Element          | Data attribute  
---------------- | ----------------
Announcement banner close | data-test="announcementBannerClose"

#### Privacy Terms Policies Pages
Element   | Data attribute  
---------------- | ----------------
Privacy terms copy container     | data-test="privacyPolicyCopy"
Subscription terms copy container | data-test="subscriptionTermsCopy"
Terms and conditions copy container | data-test="termsConditionsCopy"



#### Navigation

Element          | Data attribute  
---------------- | ----------------
Navigation menu items | data-test="navMenu"
Navigation logo | data-test="navLogo"
Login button | data-test="navLogin"
Account link | data-test="navAccount"
Cart | data-test="navCart"
Cart icon | data-test="navCartIcon"
Search link | data-test="navSearch"
Support link | data-test="navSupport"
Find a retailer link | data-test="navFindARetailer"

#### Footer
Element          | Data attribute  
---------------- | ----------------
Footer link contact us     | data-test="footerLinkContact"
Footer link FAQ | data-test="footerLinkFAQ"
Footer link Terms | data-test="footerLinkTerms"
Footer link Privacy | data-test="footerLinkPrivacy"
Footer email signup input | data-test="footerInputSignup"

#### Notification Sign Up Form

Element          | Data attribute  
---------------- | ----------------
Email signup form input | data-test="formInputSignup"
Email signup form submit button | data-test="formBtnSignup"
<br>

### Login Page

Element          | Data attribute  
---------------- | ----------------
Login username input     | data-test="loginInputUsername"
Login password input     | data-test="loginInputPass"  
Login submit | data-test="loginBtnSubmit"
Create account button | data-test="createAccountLink"
<br>

### Create Account Page

Element          | Data attribute  
---------------- | ----------------
Account firstname input | data-test="createAccountInputFirstname"
Account lastname input | data-test="createAccountInputLastname"
Account email input | data-test="createAccountInputEmail"
Account password input | data-test="createAccountInputPass"
Create submit       | data-test="createAccountBtnSubmit"
<br>

### Cart
Element   | Data attribute  
---------------- | ----------------
Cart items container | data-test="cartItems"
Cart item row | data-test="cartRow"
Checkout button     | data-test="cartBtnCheckout"


### Checkout Page

#### Billing Form

Element          | Data attribute  
---------------- | ----------------
Firstname input | data-test="checkoutFirst"
Lastname input | data-test="checkoutLast"
Address input | data-test="checkoutAddress"
City input | data-test="checkoutCity"
Postal code | data-test="checkoutPostal"

#### Credit Card Form
Element          | Data attribute  
---------------- | ----------------
CC number input | data-test="checkoutInputCC"
Exp month dropdown | data-test="checkoutSelectExpMonth"
Exp year dropdown | data-test="checkoutSelectExpYr"
CC security code | data-test="checkoutInputCSV"
<br>

### Product Page
Element   | Data attribute  
---------------- | ----------------
Add to cart button     | data-test="productBtnAddToCart"  


## Usage
The `data-test` attribute and values are used in attribute selectors to identify specific HTML elements. Specifically they will be used in CypressIO integration and end-to-end tests.

One method of reusability within the CypressIO framework is to include the attribute selectors in a fixture data file with a property name and a corresponding value of it's respective attribute selector.

In order to make the generation of this data fixture file simple, a utility program is included in this repository that will parse this README.md file and generate the corresponding .json file. The generated .json file can be included in any CypressIO project for use.

For more information on CypressIO fixture files you may find the [documentation here](https://docs.cypress.io/api/commands/fixture.html#Syntax).

### Generating the fixture json file
To run the included utility and generate the .json file from this README.md, from the projects root directory, run:

```
npm run generate-json
```

The .json will be written to `output/selectors.json`