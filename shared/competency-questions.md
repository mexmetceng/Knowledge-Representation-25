# Competency Questions

The questions **both** the OWL and the Datalog knowledge base must answer.
The comparison is only fair if both answer the same questions over the same data (the CSV files in `shared/`, described in `shared/README.md`).

Each question has an ID; reuse it as the query name in `owl/queries/` and `datalog/queries.dl`.
`X`, `Y`, `Z` are parameters (a restaurant, meal, ingredient or time).

## 1. Accessibility

| ID | Question | Expected answer |
|---|---|---|
| CQ1 | Which restaurants are available to the public? | |
| CQ2 | Which restaurants allow pets? | |
| CQ3 | Which restaurants are open at X am? | |

## 2. Social

| ID | Question | Expected answer |
|---|---|---|
| CQ4 | Is this restaurant owned by a woman? | |
| CQ5 | Is this restaurant LGBTQ+ friendly? | |

## 3. Restaurant type

| ID | Question | Expected answer |
|---|---|---|
| CQ6 | Is this a fast food restaurant or a seafood restaurant? | |
| CQ7 | Is this a Turkish restaurant or a Greek restaurant? | |

## 4. Dietary

| ID | Question | Expected answer |
|---|---|---|
| CQ8 | Which restaurant(s) offer vegetarian or vegan meals? | |
| CQ9 | Which restaurant(s) serve halal dishes? | |
| CQ10 | What kosher meals does restaurant Y serve? | |
| CQ11 | Is that meal aiming to satisfy your protein intake goal in one meal, including carbs or fats? | |

## 5. Allergen

| ID | Question | Expected answer |
|---|---|---|
| CQ12 | Do you have an allergy to ingredient X? | |
| CQ13 | Does this food contain the allergen you would like to avoid? | |

## 6. Price

| ID | Question | Expected answer |
|---|---|---|
| CQ14 | What is the price range of restaurant X? | |
| CQ15 | How do the prices of meal X vary between restaurants X, Y, Z...? | |
