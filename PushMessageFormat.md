# C2DM message format #

This is an overview of the format of [C2DM messages](http://code.google.com/android/c2dm) that klaxon understands.


# Message contents #

In addition to the required fields for a c2dm message, klaxon depends on the following extras:

  * `from` - address of the original sender, used for display
  * `subject` - the subject line of the alert
  * `body` - some body text.
  * `url` - a url for viewing the full message content, and/or replying to the message.

The above are the names of the extras included in the Intent. when sending these fields via c2dm, they will need `data.` prepended to the field names, per the c2dm docs linked above.

Of particular note here is the 1K size limit on push messages. I recommend truncating the body, and making the full text available at the url included.


### Url? what's that for? ###

c2dm messages are a delivery mechanism, but in order to reply to them, there has to be a way to send something back to the original sender (not just the intermediate server). For this, i've created a general-purpose email-to-c2dm gateway that runs on appengine. code for this is forthcoming, once i fix up the error handling.

When replying from within klaxon, it will send an http request (currently GET, eventually POST) to the url included in push message, with a 'reply' argument. the value of 'reply' is the reply you wish to send back the the message sender.