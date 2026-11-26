---
layout: post
title: "\"Failed to load kanji\": How to Fix the Stroke Order Error"
---

If Aedict suddenly shows **"StrokeOrderDiagram file is corrupted or missing: Failed to load kanji"**
instead of a kanji's stroke order, don't worry: your dictionaries are fine, and so is your data.
A restart fixes it.

# The quick fix

Close Aedict completely and open it again: Android Settings → Apps → Aedict → **Force stop**.

If the error is still there after the restart, the stroke order file itself got damaged; the
[FAQ](https://aedict.eu/faq.html#sod_corrupted) shows how to download it again. Deleting
dictionaries never touches your notepad, tags, recently viewed entries or SRS statistics.

# What happened

The dictionaries are updated every month, and the November 26 update refreshed the stroke order
diagrams too. Aedict downloads such updates in the background, while it's running. Aedict 3.55.0 and
older then kept using the old file's table of contents to read the new file, and so failed to find
the strokes, until Aedict was restarted.

The fix is in **Aedict 3.55.1**: it notices the new file and reads it from the start. Until 3.55.1
reaches you, the restart above is all it takes. [Aedict Online](https://aedict-online.eu) had the
same bug; it's fixed there already.

Thanks to the user who reported it! If you hit anything else, please let me know at the
[Aedict bug tracker](https://github.com/mvysny/aedict/issues).
