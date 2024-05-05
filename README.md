# Diamond Regression Analysis Assignment

## Getting Started

- Clone this repository to get started with the assignment.
- The main file you will be working on is `diamonds.rmd`. Follow along in that file for instructions.

## Resources

- `diamonds.rmd`: Contains the assignment instructions, data exploration, and analysis sections.
- `diamond-data.txt`: The dataset file with diamond attributes and prices.

## Submission

After completing the analysis, commit your modified `diamonds.rmd` file to this repository. Ensure your final document is well-commented and clearly presents your findings.

## Feedback

Nice job on this, Drew, this is complete. You might be interested in comparing your results to the same model on `price` rather than `log(price)`. If you do that and add supplier as the final predictor in your model, you'll see that supplier is not significant. (And I generated the data to make it not significant, but I didn't do that in log scale.)

Your model, `d_small_model <- lm(log_price ~ carat + supplier + cut + clarity + color, data = d_small)`, should really be `d_small_model <- lm(log_price ~ carat + cut + clarity + color + supplier, data = d_small)` to test supplier accounting for the other covariates. Then call `anova(d_small_model)` to estimate the significance of the explanatory variables. Theoretically this should be enough to ask for a revision, but I know from experience that your conclusions won't change *and* I think you are justified in both your creation of `d_small` and the logging of price, so let's call it done. 
