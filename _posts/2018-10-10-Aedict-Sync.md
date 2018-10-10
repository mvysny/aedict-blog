---
layout: post
title: Aedict Sync
---

Starting with 3.50.6, Aedict now supports synchronization of all of your data across all of your devices. The devices do not have to be
tied to the same Google Play account, but they need to have Aedict Ultimate purchased in order to enable sync. The data is synchronized through the Aedict Online
server and a copy of the data is kept there. You can even view the data while logged in on [Aedict Online](https://aedict-online.eu) to your account.

The synchronization only works for the UMN type of the storage. It will never work for the old File-based storage (which will go away eventually).
In order to activate the synchronization, please create an account in the [Aedict Online](https://aedict-online.eu) server. Then,
make sure you have the newest Aedict installed on your phone (at least 3.50.6).

To enable synchronization, you need to perform this on all of your devices:

* Go to `Settings / Expert Settings / Storage Type` and select UMN. This will migrate all of your data from File-based storage (which causes Aedict to crash
  when it's too large) to the UMN storage (a very fast, database-backed storage which does not crash Aedict).
* If you already have data on Aedict Online and you don't want data on your phone to be mixed with that, go to
  `Settings / Expert Settings / Nuke User Data` and select that. That way, you will make sure there is no data cruft on your phone and all of your data will b
  exactly as it is on Aedict Online
* Go to `Settings / User Data / Aedict Online Settings` and fill in your Aedict Online username and password, then check "Synchronize with Aedict Online"
* After that's done, please wait a bit to have your data synchronized to your phone.

Note that the synchronization only works with Aedict Ultimate subscription.

* Q: Will there be a backup if I accidentally delete my data?
* A: No. It's very hard to back up database files properly, especially if they are also synced to other devices. The conflicts stemming from the restoration
  of the backup may be disastrous.

