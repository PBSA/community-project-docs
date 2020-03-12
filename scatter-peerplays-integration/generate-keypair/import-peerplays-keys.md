# Import Peerplays Keys

The following outline the flow of importing keys into a Scatter account if the end-user opted for the "Login to Import Peerplays Account" button route.

#### Login to Import Peerplays Account

If you are choosing to import an existing Peerplays account, you will have opted for this route and will see this modal in front of you. Fill in this form with your Peerplays account name and password. If any errors exist within the form, they will be displayed \(Figure 3.4.2\). A valid form will look like Figure 3.4.3.

![Figure 3.4.1: Login to Import Peerplays Account \[empty\]](../../.gitbook/assets/image%20%288%29.png)

![Figure 3.4.2: Login to Import Peerplays Account \[filled - errors\]](../../.gitbook/assets/image%20%2812%29.png)

![Figure 3.4.3: Login to Import Peerplays Account \[filled\]](../../.gitbook/assets/image%20%2861%29.png)

Peerplays account importing into Scatter will appear the end-user like any other Peerplays dapp login form:

* account name input field
* account password input field
* form submit/login button

**Errors**

If any form component has an error, their appearance will change to match that of Figure 3.4.2.

**"Account Name" Field**

* string input field
* character limit of 52
* only lower-case characters
* username restrictions:
  * must start with a letter
  * must contain at least one dash, a number, or not contain any vowels

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.4.2 with the error text of:

* "Must start with a letter and contain at least one dash, a number, or no vowels"

**"Password" Field**

* string input field
* character limit of 52
* only lower-case alphanumeric characters

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.4.2 with the error text of:

* "Password should be at least 22 symbols \(alphanumeric\)"

**"Cancel" Button**

No change in behaviour or appearance for this button. Clicking this button will close the modal.

**"Login" Button**

When one or more of the form input fields ****have some content in them; the "Cancel" button will turn into a form submit button.

Only when all form fields are error free will clicking the "Login" button have an effect.

Once the form has been submitted, account authorization for the user supplied account name will begin. Peerplays account authorization flow is as follows and happens in the background \(programatically\):

1. supply a Peerplays account name and its matching password
2. request from Peerplays blockchain for account object by account name provided by user
3. generate owner, active, an memo keys from user provided account name and password
4. compare generated active and/or owner key with the blockchain returned public keys
   1. some legacy accounts had their owner and active keys swapped at one point during their registration procedure so it is necessary to swap and check so these accounts retain login access
5. if a match is found, the account that the end-user tried to authorize is authorized.

During this process,  keys required for Scatter are programatically generated and if the process above \(1-5\) completes successfully, those keys are stored by Scatter.

