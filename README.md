# darkserver

This is simple web service which provides details of GNU build-ids
from various ELF files from the RPM packages. The service is divided into two
different parts.

## Fedora wiki URL

https://fedoraproject.org/wiki/Darkserver


## Requirements

* Clojure >= 1.3.0
* Leiningen >= 1.6.0
* Noir >= 1.2.1
* Python >= 2.6 (for Koji plugin)
* elf-utils
* koji
* rpmdevtools
* mysql server


## Web server

First setup the database details in access at /etc/darkserver/darkserverweb.conf

To start the server use the following command:

```bash
$ lein run
```

This will start the server at port 8080. If you want to start the server in a
different port you can provide it as a command line argument.


## Koji Plugin

You can setup the koji-plugin in the koji-hub. Provide the same database details
to populate the database.
