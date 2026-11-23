# econ3916-lab19-random-forest
# Tree-Based Models: Random Forests

## Objective
I used California Housing to see how a single tree, linear models and a random forest compare, how impurity and permutation importance disagree, and how to tune a forest by cross-validation.

## Methodology
- Compared a single decision tree, OLS, Ridge and a random forest on the same training and test rows, and read the forest's out-of-bag score beside its test score.
- Compared impurity (MDI) and permutation importance for the forest, ranking the features under each.
- Tuned the forest's maximum depth and number of features per split by 3-fold cross-validation.
- Wrote my own prompt asking an AI for a function that charts a model's permutation importances and returns them as a table, went [YOUR VALUE] rounds, and checked it against my numbers: [YOUR RESULT].

## Key Findings
- The single tree had a test R² of 0.6161, Ridge had 0.5758, and the random forest had 0.8044. The tree memorised the training rows, and the forest gained 0.23 over Ridge with the same eight features.
- Latitude scored 0.0889 by MDI but 0.4465 by permutation, so the two measures rank the features differently.
- Cross-validation chose no depth limit and half of the features per split, and the tuned forest had a test R² of 0.8116.
