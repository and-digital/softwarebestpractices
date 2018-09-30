---
layout: page
title: How to delete Docker images, containers and volumes
permalink: /guides/how-to-delete-docker-images-containers-volumes
author_firstname: Miiro
author_lastname: Juuso
author_email: mjuuso@and.digital
author_picture: https://static.andigital.com/wp-content/uploads/2016/10/18133344/Mirro-300x300.png
author_role: Head of DevOps at AND Digital
---
**After you have worked with Docker for a while, you will notice that it eats disk space like a whale. This is especially true for build servers like Jenkins, where Docker images are often created for every code commit.**

Docker by default stores every image you build, every container you run and every volume you create. They are stored until you explicitly delete them. Therefore it's important to do a bit of housekeeping every now and then.

The one command to rule them all
------

This command will delete all stopped containers, all networks not used by at least one container, all images and all build cache:
```
docker system prune -a
```
Note that this command was introduced in Docker version 1.13.

_Pro tip: Add the `-f` argument to skip asking for confirmation._


## About the author
![{{ page.author_firstname}}]({{ page.author_picture }} "{{ page.author_firstname }} {{ page.author_lastname }}")

_**{{ page.author_firstname }} {{ page.author_lastname }}** works as {{ page.author_role }}. Reach {{ page.author_firstname }} at [{{ page.author_email }}](mailto:{{ page.author_email }})_