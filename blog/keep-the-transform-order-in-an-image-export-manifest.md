# Keep the transform order in an image export manifest

A manifest can list every operation without saying which one ran first. A crop made before a resize can refer to different coordinates from a crop made afterward. Keep the sequence alongside the output it describes.

Give each operation a position in the record. For a simple export, write down the source image, the crop rectangle in that source, the resize dimensions, and the saved format in order. Name the image whose coordinate system each rectangle uses. Use the input of that step as the reference when the previous step produced a new image.

When the same source produces several outputs, keep a separate sequence for each branch. A small preview may use the whole frame while a delivery crop starts with a selected rectangle. Put the branch name beside the output file and keep its sequence with that output.

Choose an output at handoff and trace its listed steps back to the source. Check that the dimensions and references agree with the saved files. If you cannot reproduce a step because a setting was never recorded, mark that gap before the original working files are moved.
