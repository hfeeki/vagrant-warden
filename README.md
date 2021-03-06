# Vagrant Warden

Install and run Cloud Foundry's [warden][warden] in [Vagrant][vagrant].

## Getting Started

Clone `vagrant-warden` and `cd` into it

    git clone git://github.com/silas/vagrant-warden.git
    cd vagrant-warden

Init and update the git submodules

    git submodule init
    git submodule update

`up` the box (this could take a very long time)

    vagrant up

`ssh` to the box and start the warden server

    vagrant ssh
    sudo warden-server

In another terminal `ssh` to the box again and start the warden repl

    vagrant ssh
    sudo warden-repl

Run some commands from the warden repl

    warden> create
    handle : 16bcqds1450
    warden> run --handle 16bcqds1450 --script 'uname -a'
    Linux 16bcqds1450 3.2.0-23-generic #36-Ubuntu SMP Tue Apr 10 20:39:51 UTC 2012 x86_64 GNU/Linux
    warden> destroy --handle 16bcqds1450

## License

This work is licensed under the MIT License (see the LICENSE file).

[warden]: https://github.com/cloudfoundry/warden
[vagrant]: http://vagrantup.com/
