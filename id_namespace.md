Proposal: namespace-like string id for object metadata.

TTPG object templates have a "metadata" field containing a user-defined string.  Instead of JSON, I propose a simple namespace-like string.  

Finding objects can use the relatively efficient `string.startsWith()` and/or `string.includes()` to filter a world scan, the more expensive regex when needed.

When further metadata is useful, scripts can do table lookups from this id into internal state.

**`type.descriminator/name.descriminator`**

Card type descriminators describe the deck, name descriminators enumarate duplicates.

1. `card.action/reveal_prototype`
1. `card.action/sabotage.1`
1. `card.action/sabotage.2`
1. `card.secret/become_a_martyr`
1. `card.promissory.white/ceasefire`
1. `card.promissory.arborec/stymie.omega`
1. `card.technology.white/plasma_scoring`
1. `card.technology.arborec/letani_warrior_2`

Units:

1. `unit.white/dreadnought.1`
1. `unit.white/dreadnought.2`
1. `unit.white/flagship`
1. `unit.white/my_homebrew_thing`

Tokens:

1. `token/commodities_tradegoods_1`
1. `token.attachment/biotic_research_facility`
1. `token.attachment/terraform`
1. `token.necro/prediction`
1. `token.vuilraith/tear.vuilraith.1`
1. `token.vuilraith/tear.nekro.1`
