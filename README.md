## Notes2Cloud

# Calendar Purpose

You want your work calendar stored in the work Lotus Notes system available to view
on your iPhone/iPad/Mac?

Notes2Cloud is a small java application that periodically reads you Lotus Notes calendar
(using standard Notes iNotes web APIs) and it pushes that calendar to iCloud - keeping a
dedicated iCloud calendar in sync with your Lotus Notes calendar.

It is a one-way push, Lotus Notes to iCloud.

You probably need to be a fiddler to get this to work for you, but it was a painful enough
itch for me that I built this to scratch it. Figured there are others that have same problem
(everyone that works at a place using Lotus Notes).

# Mail Export Purpose

Tired of the woeful Lotus Notes Client archive search capability?
Wish you could have a local copy of your mail?

Notes2Cloud also includes the ability to read messages from iNotes and write them to
a local filesystem in standard Unix/Mac Maildir format. Couple this with a local IMAP
server (like dovecot on Mac) and you have a full local replica of your messages and 
can use the searching capability in IMAP and your mail client.

# Other Notes

Decoding the Notes Calendar fields.

Use the following URL which will give you the design of the view, which includes
names for all fields in the calendar view.
https://company.com/mail/user.nsf/($Calendar)?ReadDesign

See calendar-design-sample.xml for what was returned in my case, and therefore
what this code assumes each field means.

To find the proper icloud URL.. go in to ~/Library/Calendars and walk through all
the directories. Open each Info.plist file. Look for the one that has a key
of Title with its value the name of your calendar. Then grab the Calendar Path
above.

Mac Jar Bundler is in /usr/share/java/Tools
