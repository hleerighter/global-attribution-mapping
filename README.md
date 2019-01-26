# GAM (Global Attribution Mapping)
Global Explanations for Deep Neural Networks

## Get Started
```Python
>>> gam = GAM(local_path="local_attributions.csv", 
                               distance="spearman", 
                               k=2)
>>> gam.generate()
>>> gam.explanations
[[('height', .6), ('weight', .3), ('hair color', .1)], 
 [('weight', .9), ('weight', .05), ('hair color', .05)]]
 
>>> gam.subpopulation_sizes
[90, 10]

>>> gam.subpopulations
# global explanation assignment
[0, 1, 0, 0,...]

>>> gam.plot()
# bar chart of feature importance with subpopulation size
```


# Development
* `Python 3.6`, `Pytest`, `requirements.txt` for dependencies
* Branching: master is protected (need one other reviewer to merge)
* Input/Output: csv (columns: features, rows: local/global attribution)
* Underlying data structures: `numpy arrays`

### Tests
To run tests:
```bash
$ python -m pytest tests/
```

### MVP
* assume local attributions are given
* K is a specified parameter
* accompany csv output with a simple visualization showing top 5 clusters and their top 5 features

### Post-MVP
* optimize k based on silouhette score
* generate local attributions (using appropriate local method)




## Contributors

We welcome Your interest in Capital One’s Open Source Projects (the
“Project”). Any Contributor to the Project must accept and sign an
Agreement indicating agreement to the license terms below. Except for
the license granted in this Agreement to Capital One and to recipients
of software distributed by Capital One, You reserve all right, title,
and interest in and to Your Contributions; this Agreement does not
impact Your rights to use Your own Contributions for any other purpose.

[Sign the Individual Agreement](https://docs.google.com/forms/d/19LpBBjykHPox18vrZvBbZUcK6gQTj7qv1O5hCduAZFU/viewform)

[Sign the Corporate Agreement](https://docs.google.com/forms/d/e/1FAIpQLSeAbobIPLCVZD_ccgtMWBDAcN68oqbAJBQyDTSAQ1AkYuCp_g/viewform?usp=send_form)


## Code of Conduct

This project adheres to the [Open Code of Conduct](https://developer.capitalone.com/single/code-of-conduct)
By participating, you are
expected to honor this code.
