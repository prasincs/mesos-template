# mesos-framework

A Leiningen template for building a mesos framework using Clojure.

## Usage

It hasn't been released, so you can't use `lein new mesos-framework` yet.

Instead, here's the current workflow:

1. Clone this repository
2. From the cloned repository's root directory, run Leiningen with the mesos-framework template
3. Start Vagrant from the resulting project directory 
4. Once all nodes have started, SSH into the master node
5. Go to the default project directory and start a Clojure REPL

Please be aware before kicking off step 3. that Vagrant will download and decompress a base image before starting the first time.   Also you can optionally supply a `MESOS_SLAVES=<count>` environment variable in step 3 to
create the desired number of slaves too. Default is 2.

```
git clone https://github.com/prasincs/mesos-template.git
cd mesos-template
lein new mesos-framework awesome-mix-vol2 --snapshot
cd awesome-mix-vol2
vagrant up
vagrant ssh master
cd /vagrant
lein repl
```

Now create your own Mesos framework!
```
(go)
```

## License

Copyright © 2015 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
