# Configuring the email provider

To send the user's verificition code via email, an email provider has to be set up. The easiest way is to use mailer.
In this example we open an smpt server with gmail. To do that we have to add an app password from [here](https://support.google.com/accounts/answer/185833?hl=en).
Then save the created password and email associated to it in your `passwords.yaml`. 

We can now access them by calling `session.serverpod.getPassword` and pass the associated key to the values (i.e. 'gmailEmail' and 'gmailPassword').
