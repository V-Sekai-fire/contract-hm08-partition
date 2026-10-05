# contract-hm08-partition

A Lean 4 proof that three of the hm08 body mesh's vertex groups partition every vertex, checked against the data it describes.

## What it is for

A mask built from the body, helper-geometry and joint-cube groups has no holes and no overlaps, and one built from the configuration's range groups does not. A Python checker re-derives every constant in the Lean file from the installed ANNY package, because a proof cannot notice a definition that disagrees with data it never reads. An exporter writes the topology and its groups to an OpenUSD layer whose subset family type enforces the partition. RFD 1121 owns the topic.

## Build and run

```sh
lake build
python check_hm08_claims.py
```

## Licence

Apache-2.0 OR MIT; see LICENSE-APACHE and LICENSE-MIT.
