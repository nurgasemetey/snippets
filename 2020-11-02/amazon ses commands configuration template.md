###  amazon ses commands configuration template


[How can we use Amazon SES template to send email in Node.js? | by Soni Pandey | Medium](https://medium.com/@pandeysoni/how-can-we-use-amazon-ses-template-to-send-email-in-node-js-fb162bd8152e "How can we use Amazon SES template to send email in Node.js? | by Soni Pandey | Medium")


[json - AWS SES template html part is multiple lines - Stack Overflow](https://stackoverflow.com/questions/50207457/aws-ses-template-html-part-is-multiple-lines "json - AWS SES template html part is multiple lines - Stack Overflow")


[Sending personalized email using the Amazon SES API - Amazon Simple Email Service](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-api.html#send-personalized-email-set-up-notifications "Sending personalized email using the Amazon SES API - Amazon Simple Email Service")


[aws ses send-templated-email --cli-input-json file://myemail.json](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-api.html "Sending personalized email using the Amazon SES API - Amazon Simple Email Service")


[Managing email templates - Amazon Simple Email Service](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/send-personalized-email-manage-templates.html "Managing email templates - Amazon Simple Email Service")


 

```
aws ses get-template --template-name simple-template
aws ses list-templates
aws ses create-template --cli-input-json file://simple-template.json
aws ses send-templated-email --cli-input-json file://myemail.json
aws ses update-template --cli-input-json file://reminder.json
aws ses send-bulk-templated-email --cli-input-json file://reminder-bulk.json


I created sns

then go to ses console and added some configuration set and connected to topic created in amazon sns
```
