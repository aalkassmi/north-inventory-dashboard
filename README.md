# North Region Inventory Performance

Twelve-store Canadian rollup of the inventory dashboard, same layout as the Wieland Regional page: Belleville (952), Brandon (953), Cambridge (954), Hamilton (961), London (968), Mississauga (971), Oshawa (977), Sarnia (983), St. Catharines (986), Steinbach (988), Windsor (993) and Winnipeg (994). Mississauga Parts Centre (972) has no vehicle inventory and is left out.

- `index.html`: the page. Location dropdown (All locations or one store), Type and Status filters, search, sortable columns.
- `data/inventory.json`: the data snapshot. A refresh replaces only this file.
- `scripts/build_inventory.py`: builds the data file from raw Motive + Mixpanel pulls in `raw/` (not committed).

Sources: Mixpanel project 3822144 for views, ad share, leads and calls (90-day window); Motive for live listings and price (CAD); days on lot from the listing's inventory age in Mixpanel, carried across stores when a truck transfers within the region.
