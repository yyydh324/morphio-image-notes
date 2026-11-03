# Store an image’s pixel dimensions in its manifest

A filename tells a script which image to open, but it does not establish whether that file still has the dimensions recorded in a handoff note. A replacement export can keep the same name while changing its width and height.

Give pixel width and height their own numeric manifest fields. State whether they describe the delivered encoded image or a particular decoded representation. Orientation handling can affect which dimensions a viewer reports, so keep that interpretation explicit rather than comparing unlabeled numbers.

Validate dimensions against the delivered file itself. If the manifest was prepared before the final export, compare it again after export. Report a mismatch with the filename and the observed values instead of silently rewriting the record to make the check pass.

Treat a matching size as one check only. Two different photographs can have identical dimensions, and the manifest says nothing about whether a crop contains the intended subject. Use a content identifier or another appropriate file check when the workflow needs to distinguish same-sized replacements.

I work on [Morphio](https://morphio.online/). For a batch handoff, I would keep the dimension fields beside the delivered filename and the validation result, including which interpretation of width and height the check used.
