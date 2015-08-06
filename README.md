## Basic Quake 1 Server In Docker

You need to supply your own id1 directory and then edit the dockerfile to tell docker where your id1 directory is.

Just change this line in the dockerfile:

    ENV ID1 id1

to:

    ENV ID1 <wherever you've put your id1 directory>

Now build the image:

    docker build -t quakeit .

And now run and create a container

    docker run -d -p 27510:27510/udp quakeit

And that should all work fine :)

If you want to change the server setup then edit ffa/server.cfg and rebuild the image. 
