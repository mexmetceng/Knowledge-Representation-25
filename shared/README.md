# Shared Data

The single dataset both the OWL and the Datalog knowledge base encode. Change it only with agreement from both owners.
IDs are lowercase snake_case (`r_harbour_grill`, `d_lentil_soup`, `i_milk`) so they map directly to OWL individuals and Datalog constants.
Booleans are `true` / `false`. Leave a cell empty when it does not apply.

| File | One row per | Columns | Answers |
|---|---|---|---|
| `restaurants.csv` | restaurant | `restaurant_type`: `fast_food`, `seafood`, `fine_dining`, ... <br> `cuisine`: `turkish`, `greek`, ... <br> `public_access`: `false` = hotel guests only <br> `opens`, `closes`: 24h `HH:MM` <br> `owner_gender`: `female`, `male`, ... | CQ1–CQ7 |
| `dishes.csv` | dish | Nutrition per serving in grams: `protein_g`, `carbs_g`, `fat_g` | CQ11 |
| `menu.csv` | dish on a restaurant's menu | `price_eur`. The same `dish_id` at several restaurants lets prices be compared. A restaurant's price range is derived from its rows, not stored. | CQ8–CQ10, CQ14, CQ15 |
| `ingredients.csv` | ingredient | `category`: `pork`, `beef`, `lamb`, `poultry`, `fish`, `shellfish`, `dairy`, `egg`, `honey`, `alcohol`, `plant` <br> `allergen`: one of the 14 EU allergens (`gluten`, `milk`, `egg`, `peanuts`, `nuts`, `fish`, `crustaceans`, `molluscs`, `soy`, `celery`, `mustard`, `sesame`, `sulphites`, `lupin`) or empty <br> `slaughter`: `halal`, `kosher` or empty, for meat only | CQ8–CQ10, CQ12, CQ13 |
| `dish-ingredients.csv` | ingredient in a dish | Links `dishes.csv` to `ingredients.csv` | CQ8–CQ13 |

Vegetarian, vegan, halal and kosher are **not** stored: each knowledge base must derive them from ingredient `category` and `slaughter`. That derivation is part of what we compare.
