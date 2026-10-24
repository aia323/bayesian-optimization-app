# Bayesian Optimization for Experiments

Two connected web apps, built in Summer 2025 for Lehigh University's Chemical and
Biomolecular Engineering department as part of an NSF/CACHE-supported set of
teaching modules:

1. **Teaching module**: students learn Bayesian optimization by optimizing a
   simulated photobioreactor that grows microalgae to produce lutein.
   🔗 https://srrweb.cc.lehigh.edu/app/bayesian_optimization
2. **Lab tool**: researchers enter their own parameters and past results, and the
   app suggests the next experiment to run.
   🔗 https://srrweb.cc.lehigh.edu/app/lab_bayesian_optimization

   <img width="1505" height="759" alt="Screenshot 2026-10-23 at 9 46 58 PM" src="https://github.com/user-attachments/assets/d2a86761-ba21-4176-ac10-d60e02fe3369" />


## My role
- **Built the teaching module's web page** (`bayesian_optimization.html`): the layout,
  styling and tabbed content that explains Bayesian optimization, surrogate models
  (Gaussian process, random forest, extra trees), acquisition functions (EI, LCB,
  GP Hedge) and sampling methods (random, Sobol, Latin hypercube), plus
  step-by-step instructions and guiding questions for students.
- **Helped design both tools**: how users move through the workflow and what
  options they can choose.
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
