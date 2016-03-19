# Known Issues #

## Sms Matching ##

The Sender matching is a bit tricky at the moment. it is done using `String.contains()` on the `DisplaySender` field of an `SmsMessage`. the downside of this is that sometimes this is a phone number, and sometimes this is an email address. If matching does not work as you expect, verify the sender, and message type.

Details are available in the Messaging app, by selecting the relevant conversation, long-pressing on the message in question, and selecting "Show message details" from the context menu. Please include this information in any bug reports, or messages to klaxon-users about this issue.

## MMS messages do not work ##

Android does not allow access to MMS message contents through the api. As a result, messages that are converted to MMS (either because they are too long, or contain images, etc) cannot trigger klaxon notifications. see the above section regarding veriftying message type in the Messaging application.