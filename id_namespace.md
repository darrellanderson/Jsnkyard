Proposal: namespace-like string id for object metadata.

TTPG object templates have a "metadata" field containing a user-defined string.  Instead of JSON, I propose a simple namespace-like string.  

Finding objects can use the relatively efficient `string.startsWith()` and/or `string.includes()` to filter a world scan, then more expensive split or regex when needed.

When further metadata is useful, scripts can do table lookups from this id into internal state.

**`type.descriminator/name.descriminator`**

Card type descriminators describe the deck, name descriminators enumarate versions (omega).

1. `card.action/reveal_prototype`
1. `card.action/sabotage`
1. `card.action.codex1/war_machine`
1. `card.secret.pok/become_a_martyr`
1. `card.promissory.white/ceasefire`
1. `card.promissory.arborec/stymie.omega`
1. `card.technology.white/plasma_scoring`
1. `card.technology.arborec/letani_warrior_2`
1. `card.planet/vega_major`

Units:

1. `unit.white/dreadnought`
1. `unit.white/flagship`
1. `unit.white/my_homebrew_thing`

Tokens:

1. `token/commodities_tradegoods_1`
1. `token/custodians`
1. `token.attachment/biotic_research_facility`
1. `token.attachment/terraform`
1. `token.necro/prediction`
1. `token.vuilraith/tear.vuilraith`
1. `token.vuilraith/tear.nekro`
1. `token.white/control`
1. `token.white/command`

Misc:

1. `tile.system/23`
1. `tile.strategy/leadership`
1. `tile/scoreboard`

Bags are a little tricky.  Maybe prefix the content with bag:

1. `bag.unit.white/dreadnought`
1. `bag.token.attachment/*`
1. `bag.token/commodities_tradegoods_1`

Decks should not be given ids because they may exhaust and re-form.  If decks had an id inherited from a starting card both the deck and discard would share it.

Note the `unit.white/my_homebrew_thing`.  Homebrew could inject new unit types (whole new, second flagship, etc) to expand unit detection.
