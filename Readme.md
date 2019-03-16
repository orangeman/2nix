# 2nix ToDo list

A [spike](https://en.wikipedia.org/wiki/Spike_(software_development))
*replicating* [Vue](https://vuejs.org) *apps*
via the [matrix](https://matrix.org) *protocol*
in a [kappa](https://kappa-architecture.com) *architecture*

### [Live Demo (todo List)](https://2nix.de)
-----

    git clone https://gitlab.com/orangeman/2nix.git
    cd 2nix
    npm i
    vue serve


Vuejs apps have local *state*.
Matrix is a *state* replication protocol.
Kappa architecture (aka *event sourcing*)
uses an *append-only log* of *change events*
to keep distributed data sets in sync.

Decoupled "apps" write data *changes*
in (multi-party e2e encrypted) matrix rooms.
In case of network partition the protocol makes sure
everyone *eventually* arrives at the same *consistent* log.
Apps derive their local *state* from that shared changelog history.

### prerequisites

    npm install -g @vue/cli
    npm install -g @vue/cli-service-global


