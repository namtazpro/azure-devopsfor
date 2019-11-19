# Logic Apps deployment

## Logic App deployment

## Connectors deployment

* azureblob
  * accountName
  * accessKey
 
* azurequeues
  * storageaccount
  * sharedkey
 
* keyvault
  * vaultName
  * token
  * token:clientId
  * token:clientSecret
  * token:TenantId
  * token:resourceUri
  * token:grantType
 
* sftp
  * hostName
  * userName
  * password
  * sshPrivateKey
  * sshPrivateKeyPassphrase
  * portNumber
  * giveUpSecurityAndAcceptAnySshHostKey
  * sshHostKeyFingerprint
  * disableUploadFilesResumeCapability
 
* azuretables
  * Storageaccount
  * sharedkey
 
* servicebus
  * connectionString
 
* sql
  * server
  * database
  * authType (windows, basic)
  * username
  * password
  * gateway (server, database)
  * sqlConnectionString
 
* outlook
  
```
   "connectionParameters": {
      "token": {
        "type": "oauthSetting",
        "oAuthSettings": {
          "identityProvider": "outlook",
          "clientId": "4ebc1e7f-42cf-4b43-b3bf-6b83dba126ea",
          "scopes": [
            "https://outlook.office.com/mail.readwrite https://outlook.office.com/mail.send https://outlook.office.com/contacts.readwrite https://outlook.office.com/calendars.readwrite"
          ],
          "redirectMode": "Direct",
          "redirectUrl": "https://logic-apis-westeurope.consent.azure-apim.net/redirect",
          "properties": {
            "IsFirstParty": "False"
          },
          "customParameters": {
            "loginUriAAD": {
              "value": "https://login.microsoftonline.com"
            }
          }
        },
```
 
* office365
```
"connectionParameters": {
      "token": {
        "type": "oauthSetting",
       "oAuthSettings": {
          "identityProvider": "aadcertificate",
          "clientId": "7ab7862c-4c57-491e-8a45-d52a7e023983",
          "scopes": [],
          "redirectMode": "Direct",
          "redirectUrl": "https://logic-apis-westeurope.consent.azure-apim.net/redirect",
          "properties": {
            "IsFirstParty": "True",
            "AzureActiveDirectoryResourceId": "https://graph.microsoft.com"
          },
          "customParameters": {
            "loginUri": {
              "value": "https://login.windows.net"
            },
            "loginUriAAD": {
              "value": "https://login.windows.net"
            },
            "resourceUri": {
              "value": "https://graph.microsoft.com"
            }
          }
        },
```