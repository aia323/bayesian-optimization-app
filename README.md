# Bayesian Optimization for Experiments

A web app that helps researchers find the best conditions for their experiments.
You enter your parameters and past results, and the app suggests the next
experiment to run. Built in Summer 2025 for Lehigh University's Chemical and
Biomolecular Engineering department, as part of an NSF/CACHE-supported set of
teaching modules.

🔗 **Live app:** https://srrweb.cc.lehigh.edu/app/lab_bayesian_optimization

## My role
I built the user interface (`General_Frontend.py`, `bayesian_optimization.html`):
- Forms for parameter names, ranges and the objective (maximize or minimize)
- Manual data entry or CSV upload of past trials
- "Suggest Next Experiment" → "Submit Result & Update Model" loop
- Live results table and plots

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
