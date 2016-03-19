## Version 21 ##
  * Added "Send Destination" sms setting, which allows klaxon to function with Verizon's SMS to Email gateway

## Version 20 ##
  * full re-write of incoming message parsing (Page parser)

## Version 18 ##
  * preference for vibration on notification
  * option to match the Sender string against the message Body
    * allows for use with go2mobile sms to email gateway

## Version 17 ##
  * a corrupt R.java led to some resources getting mixed up. sorry about that!
  * the (numeric) sender of a page is now displayed in PageView.
  * 'delete' now appears in context menus

## Version 15 ##
  * factored out strings, for localization
  * re-added support for android 1.5
    * "consume sms" preference is inactive on platforms < 1.6

## Version 14 ##
  * New Preference: "Consume Sms Message" - allows the user to determine if the Sms message should be delivered to other applications (like the standard Messaging app) or not.
  * Fixes the context menus so replies actually work.

## Version 13.2 ##
  * "Alert Sound" now picks from all available sounds, including notification, alarms, and ringtones
  * no more "stacking" of Listview activities when you click a notification icon from within PageViewer activity.
  * make "use alarm volume" preference actually work
  * stop using absolute pixels in layouts - this made list items tiny on the nexus one.
  * **consume** the `SMS_RECEIVED` intent. The message is no longer delivered to the regular Messaging app

## Version 12 ##
  * Reply directly from the ListView activity by longpressing on an item!
  * added a "delete all" menu item, so clearing out a busy shift is a breeze! (yes, there's a confirmation dialog)