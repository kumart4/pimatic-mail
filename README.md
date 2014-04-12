pimatic mail plugin
=======================

Send mails from pimatic actions. It uses [nodemailer](https://www.npmjs.org/package/nodemailer) and so supports all common mail transports.

Configuration
-------------
You can load the backend by editing your `config.json` to include:

    {
      "plugin": "mail",
      "transport": "SMTP",
      "transportOptions": {
        service: "Gmail", // sets automatically host, port and connection security settings
        auth: {
            user: "gmail.user@gmail.com",
            pass: "userpass"
        }
      }
      "to": "gmail.user@gmail.com"
    }

in the `plugins` section. For all configuration options see [mail-config-schema](mail-config-schema.html)

The transport options are transport depenedent and listed at [nodemailer](https://www.npmjs.org/package/nodemailer),

Currently you can send mail message via action handler within rules.

Example:
--------

    if it is 08:00 send mail to: "gmail.user@gmail.com" subject:"Good morning!" text:"Good morning Dave!"
