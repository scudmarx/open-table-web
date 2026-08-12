# T'au — For the Greater Good (OpenTable export)

This export was generated from `Tau40k.txt` using the OpenTable Magic authoring kit v2.

## Contents

- `decklists/tau40k.json` — native OpenTable Magic deck schema v3.
- `set.json` — OpenTable record-package entrypoint used by the Magic card-set catalogue.
- `cards/tau40k_cards.json` — custom card-printings payload, format version 2.
- `collections.json` and `package.json` — deck content-package metadata.
- `schemas/` — the schemas supplied with the authoring kit.

## Import

Install this `.otpkg` as a normal OpenTable package. The package exposes both its
`collections` and `record_package` entrypoints, so the custom card records are
registered before the deck resolves its `record_id` references. No separate card
record import is required.

## Deck construction

- Commander: Aun'va, Master of the Undying Spirit.
- 99-card mainboard.
- Five copies each of Plains, Island and Mountain.
- The three art records for each basic are allocated 2/2/1 copies.
- Gun Drone, XV-8 Crisis Suit and Treasure are included in a nonstandard `tokens`
  section and in the card record package; they are not counted in the 100 cards.

## Requested update

The Killing Blow is exported with mana cost `{2}{W}{U}{R}`. No other card text
or characteristics were deliberately changed from the supplied source file.

## Images

This export contains definitions only. It does not assign `front_image` paths,
because the supplied deck source does not define an authoritative card-to-image map.

## 1.0.2

Corrects the six Prepared spell records: prepared-spell rules text is stored in `oracle_text` rather than `flavor_text`, and card rarity is no longer emitted as Prepared spell rules text.

