-> Paper 1: "Impact of Categorical Variables Encoding on Property Mass Valuation"

- Simple Explanation

- What’s the Problem?  
  When valuing properties (like houses or land), we often describe them using categories—for example:

- "Neighborhood quality" (good, average, bad)
- "Transport access" (easy, medium, hard)

- converting categorical variables to numerical (standard method is one hot encoding)

1. One-Hot Encoding -> Turns each category into a yes/no (1 or 0) column.
   - Example: "Neighborhood: Good" -> [1, 0, 0]
2. Target Encoding -> Replaces categories with the average price for that group.
   - Example: If "good neighborhood" homes usually sell for $300K, it assigns 300,000.

- Ridge Regression (a simple math model)
- K-Nearest Neighbors (looks at similar properties)
- Random Forest (combines many mini-models)

- What Did They Find?

- Best Encoding Method: One-Hot Encoding and Target Encoding gave the most accurate prices.
- Best Model Random Forest worked best overall.
- Worst Method: CatBoost Encoding (a fancy but less reliable method).

- Why Does This Matter?

- Helps governments tax properties fairly.
- Helps banks and buyers estimate prices better.

---

-> Paper 2: "Categorical Variable Problem in Real Estate Submarket Determination with GWR Model"

- Simple Explanation

- What’s the Problem?  
  Property prices change based on location—a house in a trendy area costs more than the same house in a quiet area. But how do we map these hidden price zones (called 'submarkets')?

Also, many property features (like "neighborhood quality") are categories, not numbers, which makes it hard for computers to analyze.

- What Did They Do?

1. Combined All Categories into One "Super Score"
   - Instead of treating "good neighborhood" and "easy transport" separately, they merged them into a single number representing overall quality.
2. Used a Smart Map Tool (GWR)
   - This tool checks how prices vary street by street (not just city-wide).
3. Compared 3 Approaches:
   - No Submarkets (basic average price).
   - Expert-Drawn Submarkets (people guess zones).
   - GWR Submarkets (computer finds zones automatically).

- What Did They Find

- Best Method The GWR computer model was more accurate than expert guesses.
- Error Reduced: Cut pricing mistakes by ~20% compared to the basic method.

- Why Does This Matter?

- Helps city planners decide where to build schools or roads.
- Helps real estate agents price homes more accurately.
- Makes tax assessments fairer.

---

- One-Sentence Summaries

- Paper 1: Turning words (like 'good neighborhood') into numbers correctly helps computers predict property prices better.
- Paper 2: Mapping hidden price zones street-by-street leads to fairer taxes and smarter city planning.
