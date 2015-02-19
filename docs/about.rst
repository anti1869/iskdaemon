About isk-daemon




Key features:

Query for images similar to one already indexed by the database, returning a similarity degree for the images on database that most resemble the target query image;
Query for images similar to one described by its signature. A client-side widget may generate such signature from what a user sketched and submit it to the daemon;
Network interface for easy integration with other web or desktop applications: XML-RPC, SOAP;
Fast indexing of images one-by-one or in batch;
Associate keywords to images and perform image-similarity queries filtering by keywords;
Remove images from database one-by-one or in batch;
Built-in web-based admin interface with statistics and ad-hoc maintenance commands/API testing;
Optimized image processing code (implemented in C++);
Sample API usage provided for Java, Python, PHP.
Sample applications:
image classification
enhance usability in image-related softwares by helping users find similar images faster
finding duplicate images in libraries
moderation (pictures sent by users on forums, wikis, etc). Pictures similar to other pictures that were previously banned can be signaled to moderators.