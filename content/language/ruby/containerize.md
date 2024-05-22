---
title: Containerize a Ruby application
keywords: Ruby, webrick, containerize, initialize
description: Learn how to containerize a Ruby application.
aliases:
  - /language/ruby/build-images/
  - /language/ruby/run-containers/
---

## Prerequisites

* You have a [git client](https://git-scm.com/downloads). The examples in this section use a command-line based git client, but you can use any client.

## Overview

This section walks you through containerizing and running a Ruby application.

## Get the sample application

Clone the sample application to use with this guide. Open a terminal, change directory to a directory that you want to work in, and run the following command to clone the repository:

```console
$ git clone https://github.com/vishalbidwe/ruby-docker.git
```

You should now have the following contents in your `ruby-docker`
directory.

```text
├── ruby-docker/
│ ├── server.rb
│ ├── Gemfile
│ ├── Gemfile.lock
│ ├── compose.yaml
│ ├── Dockerfile
│ └── README.md
```

To learn more about the files that `docker init` added, see the following:
 - [Dockerfile](../../reference/dockerfile.md)
 - [.dockerignore](../../reference/dockerfile.md#dockerignore-file)
 - [compose.yaml](../../compose/compose-file/_index.md)

## Run the application

Inside the `ruby-docker` directory, run the following command in a
terminal.

```console
$ docker compose up --build
```

Open a browser and view the application at [http://localhost:443](http://localhost:443). You should see a simple Ruby application.

In the terminal, press `ctrl`+`c` to stop the application.

### Run the application in the background

You can run the application detached from the terminal by adding the `-d`
option. Inside the `ruby-docker` directory, run the following command
in a terminal.

```console
$ docker compose up --build -d
```

Open a browser and view the application at [http://localhost:443](http://localhost:443).

You should see a simple ruby application.

In the terminal, run the following command to stop the application.

```console
$ docker compose down
```

For more information about Compose commands, see the [Compose CLI
reference](../../compose/reference/_index.md).

## Summary

In this section, you learned how you can containerize and run your Ruby
application using Docker.

Related information:
 - [Build with Docker guide](../../build/guide/index.md)
 - [Docker Compose overview](../../compose/_index.md)

## Next steps

In the next section, you'll learn how you can develop your application using
containers.

{{< button text="Develop your application" url="develop.md" >}}
