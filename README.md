# Reference Sheet
## Custom data attributes used in automated tests.
This document defines the values used for the `data-test` attribute for respective HTML elements. This attribute will be used by automated tests to interact with page elements.


### Reference Organization
Each attribute value will be listed under the web page or web page component where it would be visually rendered.



### Home Page

#### Navigation

Element          | Data attribute  
---------------- | ----------------
Navigation logo | data-test="navLogo"
Login button | data-test="btnLogin"



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

### General

Element          | Data attribute  
---------------- | ----------------
Email signup form input | data-test="formInputSignup"
Email signup form submit button | data-test="formBtnSignup"
