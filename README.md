# lib-themes

Shared code for droidtop, Pythia, Enginehost and droidtop-agent: the ES-DE theme engine: parsing themes and mapping one onto the tokens, for droidtop's and Pythia's Gaming UIs (#920).

One of the shared libraries of Droidtop/tracker#867, in the split the owner approved on 2026-11-21
(Droidtop/tracker#960, step 1.0). Where its code comes from: new.

**Shared code, never built on its own** (owner, 2026-11-21: "these libraries aren't standalone. There's no reason
to build them at all. They're shared code"). This repository holds the source. It is compiled, tested and shipped only
inside the programs that pin it, by commit, and each program's CI is where a change here is checked. There is no build
pipeline, release build or platform target here.

- **Platform-neutral:** no Android-only code; an Android adapter, where one is needed, is a separate, marked module.
  The programs also target mobile Linux.
- **Replace in place:** code moves here in the change that deletes the copy it replaces in a program.
- Licence: GPL-3.0 (see `LICENSE`).
