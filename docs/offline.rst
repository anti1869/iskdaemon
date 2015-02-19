Offline processing
==================

When telling the daemon to index a file, you can either inform it a local file path with image data
(plenty of image formats are currently supported), or a remote HTTP URL, in which case it would download the
image to memory.

In both cases, as soon as the image is processed, it can be removed from disk or memory, thus removing copyright
concerns when storing images. The image similarity database will only store a signature of the image (which
is actually, just a few bytes long).

This signature can be seen merely as metadata describing the image, just like you probably already store image
dimensions, source url, source gallery url, etc.

The provided API enables the image processing (as part of the process to add it to the image database) to be
done on an adhoc basis (for example when user submits an image to your system) or in offline batches.