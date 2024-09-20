# Dorfbräu Survey

## Content

An analysis of the Dorfbräu survey conducted with the start of issuing the first brewed beers of the company.

Analysis contains mean values of the rated beers per category (carbonization, taste, colour) and the ranking of the favourites.

## Technology

Repo is based on a Github action to automatically run and render the analysis whenever changes are merged to main branch. Therefore it is sufficient to just update the respective csv file in the data folder. After pushing and merging, you will automatically obtain new results at [Github pages](https://insilentio.github.io/DorfbraeuUmfrage/Umfrage.html).

## Caveats

Project uses [renv](https://rstudio.github.io/renv/) for creating a reproducible environment. However, if you need to render the document locally, you must deactivate renv first (`renv::deactivate()`). Also, when enhancing the code in a way that results in need of an additional package, be sure to include it in the *renv.lock* file by using `renv::snapshot`. Furthermore, in such a case you should clear the cache on [GitHub](https://github.com/insilentio/DorfbraeuUmfrage/actions/caches) to enforce the building of a fresh container with the correct environment. The same is true when you decide to update the R version in *publish.yml*.
