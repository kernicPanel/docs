## Active Directory/LDAP Setup (Enterprise) 


### Enabling Active Directory/Lightweight Directory Access Protocol (AD/LDAP)

After installing Mattermost:

1. Create a team using email authentication
  1. Note: The account used to create a team receives the “System Administrator” role, used to configure settings for your Mattermost site.
  2. Go to **Main Menu** (the three dots at top left) > **System Console**
  3. Go to **LDAP Settings**
  4. Fill in the fields to set up Mattermost authentication with your LDAP server
  
  After LDAP has been enabled, users should be able to go to your Mattermost site and sign in using their LDAP credentials. The “LDAP username” will be the attribute set in the “Id Attribute” field. 

  **Note: If a user attribute changes on the LDAP server it will be updated the next time the user enters their credentials to log in to Mattermost. This includes if a user is made inactive or removed from an LDAP server. Synchronization with LDAP servers is planned in a future release.**

### Switching System Administrator account to LDAP authentication

If you would like to switch your System Administrator account to LDAP authentication, it is recommended you do the following:

1. Create a new account using LDAP
  1. Note: If your LDAP credentials use the same email address as your System Administrator account, it is recommended you change the email on your System Administrator account by going to Main Menu -> Account Settings -> General -> Email. This will free up the email address so it can be used by the LDAP account.
  2. Sign in to your email based System Administrator account
  3. Navigate to the System Console
  4. Go to **Teams** > **Team Name** > **Users**, and find your new LDAP user account
  5. Promote your LDAP account to “System Administrator” using the dropdown menu beside the username
  6. Log in with your LDAP account
  7. Navigate to the System Console
  8. Go to **Teams** > **Team Name** > **Users**, and find your old email based System Administrator account
  9. Make the email account “Inactive” using the dropdown beside the username

  **Note: If you make the email account inactive without promoting another account to System Administrator, you will lose your System Administrator privileges. This can be fixed by promoting another account to System Administrator using the command line.**

### Restrict authentication to Active Directory/LDAP

1. Switch your System Admin account to LDAP authentication per steps above
2. Go to **System Console** > **Email Settings** and set **Allow Sign Up With Email** to `false`.
3. Go to **System Console** > **Email Settings** and set **Allow Sign In With Email** to `false`.

This should leave Active Directory/LDAP as the only single-sign-in option. 

### Additional Active Directory/LDAP support

Improvements Active Directory/LDAP support for Mattermost Enterprise Edition be released monthly to subscribers following the official product release. 
