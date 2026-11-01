# PocketMeta card data

The Pokémon TCG Pocket card data used by [PocketMeta](https://tcgpocketmeta.com), published as required by the
AGPL-3.0 licence of one of its sources. It is regenerated every day from the upstream projects below.

## Files

- `cards.json`: 4,547 card prints. Gameplay fields (HP, attacks, ability, weakness, retreat,
  stage, artist), rarity, pack membership, pack points, trade cost, and two fields we add:
  - `canonicalId`: the earliest playable print of the card; alternate arts point to it.
  - `printIds`: every print of the same card.
  Names are harmonised across prints (one print upstream had a typo).
- `sets.json`: sets with release dates, packs and localised names.

Meta statistics (play rates, decks, tiers) are not part of this bundle.

## Sources and licences

- [pokemon-tcg-pocket-cards](https://github.com/PocketDecks/pokemon-tcg-pocket-cards) by Leonid Dalin and Chase Manning,
  **AGPL-3.0**. This bundle is a modified version of its data and is therefore also released under AGPL-3.0 (`LICENSE`).
- [pokemon-tcg-pocket-database](https://github.com/flibustier/pokemon-tcg-pocket-database) by flibustier, **MIT**
  (`LICENSE-pokemon-tcg-pocket-database`).

Built from pokemon-tcg-pocket-cards@5.4.0 and pokemon-tcg-pocket-database@2.12.0 (or their newer main branches).

## How it is made

Both databases are joined on set and number (`a2-129`, `pa-007`), names are harmonised across prints, and each card
gets its canonical print. The code that does this lives in PocketMeta's data pipeline; this repository holds its output.

Pokémon and all card names and images are trademarks and copyrights of their respective owners. This is a fan project,
not affiliated with Nintendo, Creatures, GAME FREAK, The Pokémon Company or DeNA.
