---
layout: post
title: Aedict Reader and Android 10
---

Unfortunately, Android 10 and above doesn't allow apps to access the clipboard anymore.
This is intentional move from Google, because of increased security (otherwise all apps could monitor clipboard for passwords).
Details can be found at [Android 10 changelog](https://developer.android.com/about/versions/10/privacy/changes#clipboard-data).
You can also find more details at [Aedict Bug 889](https://github.com/mvysny/aedict/issues/889).

The [Google Translate app is affected by this as well](https://support.google.com/translate/thread/13539043?hl=en).

Aedict Reader therefore adapted two replacement ways of working:

1. Aedict Reader now integrates into the Android copy menu. When you start selecting text in any app, the "Copy"/"Select All" menu appears.
   Just press the "three dot" "more" menu, then select Aedict Reader. The Reader will then analyze
   selected text. See the [Aedict Reader in Android 10 video](https://www.youtube.com/watch?v=8Uz7k02nJIw).
2. Certain apps prevent the copy menu from appearing. In such case, follow the alternative route below.

In order to paste the text into Reader:

1. Make sure Aedict Reader is "Always Available" (first thing in Reader Settings).
2. Copy the text to the clipboard.
3. In the notification bar, find the "Aedict Reader" notification and press the "Analyze Clipboard" button.
   That will open the Reader in the text search mode.
4. Long-press/focus the text input field in the Reader Popup and paste the text contents there.

