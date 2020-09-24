###  amazon ses not authorized to send


[node.js - Can't send e-mail using AWS SES: didn't I configure it properly? - Stack Overflow](https://stackoverflow.com/questions/55250973/cant-send-e-mail-using-aws-ses-didnt-i-configure-it-properly "node.js - Can't send e-mail using AWS SES: didn't I configure it properly? - Stack Overflow")


 

```
Are you using credentials associated with an IAM user? If this is the case, you need to assign a policy(AmazonSESFullAccess) to the IAM user that will allow those specific actions in SES.

go to IAM
open user
on permissions tab click add permissions
attach new policy from existing
`AmazonSESFullAccess`


```
