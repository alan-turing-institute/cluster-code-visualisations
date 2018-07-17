# Enabling Complex Analysis of Large Scale Digital Collections

This repository contains code, data, and other outputs from the first phase of '[Enabling Complex Analysis of Large Scale Digital Collections](http://figshare.com/articles/Enabling_Complex_Analysis_of_Large_Scale_Digital_Collections/1319482)', a project funded by the [Jisc Research Data Spring](http://opensource.org/licenses/MIT).

The core project team are:

- PI Melissa Terras (UCL)
- CI James Baker (British Library)
- CI David Beavan (UCL)
- CI James Hetherington (UCL)
- CI Martin Zaltz Austwick (UCL)

Associated researchers (without who research questions none of this could have happened!) are:
- Oliver Duke-Williams (UCL)
- Will Finley (Sheffield)
- Helen O'Neill (UCL)
- Anne Welsh (UCL)

All code, data, and other outputs are available for use and reuse under a [MIT Licence](http://opensource.org/licenses/MIT)

For more info on the project see the [UCL DH](http://blogs.ucl.ac.uk/dh/2015/05/07/bluclobber-or-enabling-complex-analysis-of-large-scale-digital-collections/) and [British Library Digital Scholarship](http://britishlibrary.typepad.co.uk/digital-scholarship/) blogs.

---

## UCL users

### Beware: epcc-master branch

The `epcc-master` branch has not been tested on UCL systems. 

---

## Urika users

These instructions assume you have configured your web browser and environment to access Urika's applications software. If you have not done so, see [Configure web browser to access Cray Urika’s applications software](http://ati-rescomp-service-docs.readthedocs.io/en/latest/cray/connecting.html#configure-web-browser-to-access-cray-urika-s-applications-software) in the [Connecting to the ATI Cray Urika](http://ati-rescomp-service-docs.readthedocs.io/en/latest/cray/connecting.html) documentation.

Visit the Urika home page: http://urika1.turing.ac.uk/home/

Click Jupyter

Enter your Urika username and password and click Sign In.

Click Files tab.

Browse to `cluster-code-visualisations/diseases`.

Double-click on `Diseases_1-LocalPackages.ipynb`.

Uncomment the first two lines to install PyYAML and matplotlib:

```
!pip install --user PyYAML
!pip install --user matplotlib
```

Select Cell => Run all.

### Visualising data from cluster-code

By default `Diseases_1-LocalPackages.ipynb` visualises data held in the repository in `diseases/data`. This notebook can be used for data created on Urika using the [epcc-master](https://github.com/alan-turing-institute/cluster-code/tree/epcc-master) branch of the [cluster-code](https://github.com/alan-turing-institute/cluster-code/) repository.

Assuming you put your results in a `~/cluster-code-results` directory, as suggested in the cluster-code documentation, copy the results to `diseases/data` e.g.:

```
cp ~/cluster-code-results/data_normaliser/* diseases/data/
cp ~/cluster-code-results/data_diseases/* diseases/data
``` 

Rerun the notebook.
