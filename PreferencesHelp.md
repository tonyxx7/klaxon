# Introduction #

Below is a quick description of some of the options found in the Preferences menu.

## Preferences ##
  * **On Call** - if this is un-checked, klaxon will not process incoming messages.
  * **Alert Sound** - the sound klaxon will make when it receives a message.
  * **Use Alarm Volume** - Android has separate volume controls for Alarms and Notifications. Notifications are played at the current ringer volume, but alarms will be loud, even when other notifications are quiet. (unless your phone is in silent/vibration mode).

### SMS Settings ###
  * **Sender** - if this string is included in the sender's phone number (or email address, if this message was sent through an email to sms gateway), klaxon will act on this message. otherwise, it will not. If empty, klaxon will match all messages.
  * **Use Received Service Center** - This is most often needed when you are using a third-party email-to-sms gateway, like go2mobile. it is normally not necessary.
  * **Consume SMS Message** - Tries to prevent this message from being received by the default Messaging application. This will only work in android versions > 1.6.

### Reply Settings ###

  * **Send Destination** - Another setting for strange email-to-sms gateways. It seems to be required for Verizon, but not most others.
  * **Also match message body** - search for the 'Sender' string in the body of the message. this is sometimes needed for sms gateways that use strange formatting.

### Other Settings ###
  * **Edit Replies** - This will pop up the screen for editing the quick replies. you can add/remove or edit replies from here.
  * **Notification Interval** - How often the notification will repeat.
  * **Changelog** - Not really a preference, just a display of recent, notable changes.