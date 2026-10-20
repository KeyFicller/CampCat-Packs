# CampCat-Packs

Saved skill packs for [CampCat](https://github.com/KeyFicller/CampCat): each
pack is a set of `.ccat` bundles that drive an Android game — anchors, edges and
actions of one graph, plus their template PNGs.

**`main` is empty on purpose, and so is any other branch than a pack's.** A
branch is named after the graph it holds, so the pack for the `demo` graph lives
on the branch `demo`. A branch's root is the library directory itself: the
bundles sit at the top of the tree, not under a folder named after the branch.

```text
main      (this file only — no pack)
demo      demo.entry/, demo.map/, demo.map-city/, ...  + operator.md
stzb      stzb.entry/, stzb.map/, stzb.map-city/, ...  + operator.md
```

Where two branches hold the same graph, the newer one is the pack to use; the
older is the snapshot it was built from.

To read a pack, check out its branch or browse it on GitHub. To play one, put it
where CampCat looks for its library (`ccat_library/` beside `config.json`); when
the app repository carries this repo as a submodule, it pins a pack branch and
is fetched with:

```bash
git submodule update --init --checkout ccat_library
```

A pack is expected to change while the app explores a game — templates get
recut and scripts get rewritten — so commit after a run that works, not for
every tap. `CCAT.md` and `gold.ccat` are not here: the language belongs to the
interpreter and lives in the app repository.
