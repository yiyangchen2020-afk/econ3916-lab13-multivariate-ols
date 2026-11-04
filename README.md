# Multivariate OLS — What "Controlling For" Actually Does

## Objective

In this lab, I examined how adding control variables affects OLS regression estimates and why some controls can reduce bias while others can create it.

## Methodology

- Simulated wage data using education and ability to examine omitted variable bias.
- Compared regressions with and without ability and checked the omitted variable bias formula.
- Used the Frisch-Waugh-Lovell method to verify the coefficient from the full regression.
- Simulated a collider to examine how controlling for the wrong variable can create bias.
- Examined multicollinearity using VIF, standard errors, and a joint F-test.
- Estimated an interaction model to compare the return to experience for union and non-union workers.
- Used AI to create a specification-table function, revised the prompt, and checked the results against my own regressions.

## Key Findings

The estimated return to education was 5,126 when ability was omitted, compared with the true value of 2,500. After controlling for ability, the estimate decreased to 2,546. The predicted bias was 2,629, while the actual bias was 2,626.

The Frisch-Waugh-Lovell method produced the same education coefficient as the full regression, 2,546.4985.

Controlling for the collider changed the estimated effect from approximately zero to -0.596, with a p-value of 0.000. This shows that adding a control variable can create bias.

Multicollinearity made standard errors about 12 times larger. However, the sum of the two coefficients remained close to the true value, at 5.009.

In the interaction model, each additional year of experience increased estimated pay by about $903 for non-union workers and $504 for union workers.

The AI-generated specification table matched all four regressions in both coefficients and standard errors. Revising the prompt made the choice of conventional OLS standard errors explicit.
