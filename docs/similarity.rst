Similarity details
==================

Visual image similarity considers the basic shape and color information of the query when looking through the
database for potential matches.

*isk-daemon* uses wavelet algorithms, metric and query ideas based on the paper
`“Fast Multiresolution Image Querying” <http://salesin.cs.washington.edu/abstracts.html>`_ by
Charles E. Jacobs, Adam Finkelstein and David H. Salesin.

The core image similarity algorithm uses a multi-resolution wavelet decomposition approach for solving the problem
of determining the top-k similar images to a target among a pre-indexed database. Among some of it’s advantages,
this approach allows queries to be specified at any resolution (possibly different from that of the target); moreover,
the running time and storage of our method are independent of the resolutions of the database images.

The signature information for each image computed by isk-daemon can be extracted from a wavelet-compressed version
of the image directly, allowing the signature database to be created conveniently from a set of compressed
(low-resolution) images.

Why using wavelets: Wavelet decompositions allow for very good image approximation with just a few coefficients.
As such, this property has been exploited for lossy image compression. Typically, in these schemes, just the wavelet
coefficients with the largest magnitude are used. Wavelet decompositions can be used to extract and encode edge
information. When doing query-by-sketches, edges from user drawn strokes are likely to be among the key features.
The coefficients of a wavelet decomposition provide information that is independent of the original image resolution.
Thus, a wavelet-based scheme allows the resolutions of the query and the target to be effectively decoupled.
Wavelet decompositions are fast and easy to compute, requiring linear time in the size of the image and very
little code. See more :doc:`scalability` details.