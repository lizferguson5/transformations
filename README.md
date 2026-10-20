# Transformation Lab

**Live app:** [https://lizferguson5.github.io/transformations/](https://lizferguson5.github.io/transformations/#overview)

An interactive lab for BIOL 200 (Violations of Assumptions). Students practise exponential and logarithmic transformations. They then log-transform a skewed medical dataset, check normality before and after, and back-transform their results into the original units. A scientific calculator stays beside the lesson the whole time, so students can see every number being made.

## What's inside

The app has five tabs:

| Tab | What students do |
|---|---|
| **Start here** | See why we transform data. Animated histograms of 400 simulated CRP values show how each transformation changes the shape and skewness. A normal curve is drawn over the bars for comparison. Includes definitions of linear and non-linear transformations and a table of which transformation to use for which problem. |
| **Exponential eˣ** | Calculate eˣ for x = 1, 1.5, 2 and 2.5. Each answer is plotted on the graph, with an arrow showing how far the transformation moved the starting value. Optional overlay compares 2ˣ and 10ˣ. |
| **Log base 10** | Calculate log₁₀(x) for x = 1 to 5 and see how logs compress large values. |
| **Natural log ln** | Calculate ln(x) for x = 1 to 5, compare it with log₁₀, and practise undoing ln with eˣ. |
| **Back-transform lab** | Work through C-reactive protein (CRP) data from 12 patients in five steps: check normality, transform with ln, average on the log scale, back-transform to the geometric mean, and build a 95% confidence interval. |

## Features

- **Built-in scientific calculator.** It has ln, log, eˣ, 10ˣ, x², √ and xʸ keys. The top line shows exactly what is being calculated, and a history of recent results can be reused.
- **"Show me" buttons.** Each question has one. It presses the keys on the calculator one at a time so students can follow along.
- **Key sequences shown three ways.** For this calculator, the Windows Scientific calculator and Excel (`=LN()`, `=EXP()`, `=LOG10()`).
- **Instant answer checking.** Answers are checked with a 4-decimal-place rounding rule. When an answer is wrong, the feedback names the likely mistake, such as using log₁₀ instead of ln, 10ˣ instead of eˣ, dividing by 12 instead of √12, or back-transforming the standard error.
- **"Show the calculation" panels.** They write out each step with the numbers filled in.
- **Shapiro-Wilk results** for the raw and transformed lab data. They pop in as students complete each stage.
- **Visual explanations of back-transformation:**
  - a two-scale diagram linking each patient's ln value to its mg/L value;
  - a slider showing why the geometric mean resists extreme values;
  - a diagram showing why back-transformed confidence intervals are asymmetric.
- **"Things to try" prompts** at the end of each tab for exploration and discussion.
- **Works on phones.** The calculator opens as a drawer from a button at the bottom of the screen. Supports light and dark mode.

## The data

**Start here tab:** 400 CRP values simulated from a log-normal distribution. The generator is seeded, so every student sees the same histogram.

**Back-transform lab:** 12 CRP values made up for practice, in a realistic range.

| | Value |
|---|---|
| Raw data (mg/L) | 0.4, 0.7, 0.9, 1.2, 1.5, 1.9, 2.4, 3.1, 4.2, 6.0, 9.8, 18.5 |
| Arithmetic mean | 4.22 mg/L |
| Geometric mean | 2.36 mg/L |
| 95% CI for the geometric mean | 1.16 to 4.80 mg/L |
| Shapiro-Wilk, raw data | W = 0.721, p = 0.001 |
| Shapiro-Wilk, ln-transformed | W = 0.988, p = 0.999 |

The results are read against common CRP risk groups: below 1 mg/L lower risk, 1 to 3 average, above 3 higher.

## Files

| File | Purpose |
|---|---|
| `index.html` | The complete app. All styles and scripts are included in this one file. |
| `README.md` | This file. |

There is no build step and nothing to install. The page loads its fonts from Google Fonts and falls back to system fonts when offline.
