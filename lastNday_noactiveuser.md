# notes


SOQL - last n days  
```
SELECT Id, LastLoginDate, User.LastName, User.Firstname, Profile.UserLicense.Name, Profile.Name, Username, Profile.UserLicense.LicenseDefinitionKey, IsActive, CreatedDate FROM User WHERE IsActive = true AND ((LastLoginDate < LAST_N_DAYS:7 AND LastLoginDate != NULL) OR (CreatedDate < LAST_N_DAYS:1 AND LastLoginDate = NULL)) 
AND Profile.UserLicense.LicenseDefinitionKey IN ('SFDC','AUL','AUL1','AULL_IGHT') ORDER BY LastLoginDate DESC

```
