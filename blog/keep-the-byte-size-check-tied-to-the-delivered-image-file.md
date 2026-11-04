# Keep the byte-size check tied to the delivered image file

An image manifest needs the byte count of the file that actually leaves the output folder. Measure after the final export; a replacement or another compression pass can make an earlier count stale.

Name an integer field, for example output_bytes, and define its unit as bytes. Keep any rounded megabyte display label separate. The displayed labels may agree even where exact counts differ.

Connect each measurement to the delivered filename or a stable identifier. When you make a later sharing copy, check that file and keep its own record. Copying a value from the earlier version loses that connection.

Record a read failure as a failed check. Neither a zero substituted for an unknown value nor an omitted row tells the recipient what happened to the file.

Matching byte counts do not establish that two images are the same. Use an appropriate content check where replacements must be distinguished. Visual review has its own job: the measured file can still show the wrong photograph or crop.

Compare the manifest with the final output directory before delivery. Retain the filename, byte count and check result together so a later question can be traced to the version that was measured.
