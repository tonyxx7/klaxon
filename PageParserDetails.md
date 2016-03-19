# Page Parser Details #

Page Parsers (coming shortly), are a new approach to extracting the relevant information from a received message. However, picking the best Page Parser for your particular case may be tricky.

The choice of page parser is in Preferences -> Sms Settings -> Page Parser Type

choices are the following:

## Standard ##
Based closely on the "default" options in the previous parser, this should work for most normal cases.

## Go2Mobile ##
go2mobile is a (seemingly) popular sms -> email gateway used in Europe. they use ':' as a separator between the sender, subject, and body.

## Labeled Fields ##
Some gateways use text labels like `Frm:`, `Subj:`, and `Msg:`. this parser strips those labels, and does the Right Thing with these fields. (setting them as the values of the appropriate field).

# But it doesn't work! #

If none of the above covers your particular case, please file a bug under the Issues tab above. be sure to include the full text of the received Sms message, and be sure to verify that the message is actually a text message, not an MMS (as describe in KnownIssues under Sms Matching).