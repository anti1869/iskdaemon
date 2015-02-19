Scalability
===========

Disk space usage for the image database grows linearly with the number of images. For a comparison, a database
with 162.000 images takes 230mb of disk space and RAM memory.

Adding images to a database has a constant complexity, ie, it always takes the same time, regardless of how
big is your collection.

And when it comes to querying for similar images, theoretically, the complexity is also linear with the size of
your collection. So, if your collection with 10.000 images takes 5 seconds to query, and you increase your
collection to 100.000 images, then it should take 50 seconds to query.