---
title: Keep a small manifest beside an image export batch
date: 2026-10-26
description: Map exported images to their sources, record the delivered dimensions, and keep the manifest with the handoff.
---

Give an image export batch a manifest that maps each output to its source. A recipient looking through square crops should be able to find the original for one image without having to decipher your naming convention. A plain JSON file kept beside the images can hold that information.

Record the source and output filenames. Add dimensions read from the exported file and a note identifying its intended placement. Paths relative to the handoff folder give the recipient a location they can follow.

This entry uses example names and dimensions:

```json
{
  "source": "input/shelf-07.jpg",
  "output": "web/shelf-07-square.jpg",
  "width": 800,
  "height": 800,
  "note": "Square crop for the article card"
}
```

Check each real output before writing its dimensions into the manifest. Keep the requested size in another field if someone needs to compare the request with the delivered result.

## Revise the entry after replacing an image

Check a replacement crop, then update the record to match it. If the manifest still points to an older output, the recipient has to work out which version you intended to send.

Mark failed exports explicitly or record them in a separate error list. A planned filename is not confirmation that a file was written. If an export job stops midway, compare the records of successful outputs with the files present in the folder.

## Open one output from its recorded path

Find its source, inspect the visible crop, and check the recorded dimensions. Following one entry through the folder gives you a way to review whether its structure and names will make sense to the recipient.

Include the manifest in the handoff and retain a copy with the delivered files. When a later request mentions one article-card image, the record can identify its source and the version you sent.

Published by [Morphio](https://morphio.online/) as part of our practical image workflow notes.
