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
uses an *append-only log* of *change events* as the single source of truth to keep distributed data sets in sync.

Vue apps "chat" their *changes*
in (multi-party end-to-end encrypted) matrix rooms
and derive their local *state* from that event log.
In case of network partition the matrix protocol makes sure
that all apps *eventually* arrive at the same *consistent shared state*.

### prerequisites

    npm install -g @vue/cli
    npm install -g @vue/cli-service-global
