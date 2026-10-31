# Leave failed exports visible in an image batch manifest

Keep a manifest row for every requested input, including failed exports. An empty output field should have an explicit outcome beside it.

Give each input a working identifier and record its outcome separately from the output filename. For a failed export, leave the output field empty and keep a short error category without private paths or sensitive file contents.

Record a retry as another attempt associated with the same input. If it succeeds, name the delivered output and keep the earlier failure in the working record so the attempt history remains understandable.

Before delivery, reconcile the requested inputs with the manifest. Name any unresolved item in the handoff message and distinguish it from an input that the recipient deliberately withdrew.

I work on Morphio, our image project at [https://morphio.online/](https://morphio.online/). These notes describe image preparation and review; they do not require a particular editing tool.
