# Bayesian Optimization for Experiments

A web app that helps researchers find the best conditions for their experiments.
You enter your parameters and past results, and the app suggests the next
experiment to run. Built in Summer 2025 for Lehigh University's Chemical and
Biomolecular Engineering department, as part of an NSF/CACHE-supported set of
teaching modules.

🔗 **Live app:** https://srrweb.cc.lehigh.edu/app/lab_bayesian_optimization

## My role
- **Built the web page** (`bayesian_optimization.html`): the layout, styling and
  tabbed teaching content that explains Bayesian optimization, surrogate models
  (Gaussian process, random forest, extra trees), acquisition functions (EI, LCB,
  GP Hedge) and sampling methods (random, Sobol, Latin hypercube), plus
  step-by-step instructions and guiding questions for students.
- **Tested the optimization model on real experimental data** to check that its
  suggestions made sense before release.


## How it works
The app uses scikit-optimize to fit a surrogate model (Gaussian process,
random forest or extra trees) to past results. An acquisition function then
picks the most promising next experiment.

## Tech
Python · Bokeh · scikit-optimize · NumPy · HTML/CSS

## Run it locally
```bash
pip install bokeh scikit-optimize numpy
bokeh serve --show General_Frontend.py
```
