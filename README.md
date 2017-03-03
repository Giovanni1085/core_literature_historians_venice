# The Core Literature of the Historians of Venice

Repository to go with the article Colavizza Giovanni "The Core Literature of the Historians of Venice", submitted to Frontiers in Digital Humanities in 2017.

This publication is part of the [LinkedBooks project](http://dhlab.epfl.ch/page-127959-en.html). 

## Contents

* `LICENCE` MIT
* `README.md` this file
* `Descriptive statistics and plots.ipynb` TODO
* `Community explorative igraph.ipynb` TODO
* `Community metadata evaluation.ipynb` TODO
* `dataset/`
    * [citation_data.json](dataset/citation_data.json) the citation dataset among monographs on the history of Venice
    * [data_description.md](dataset/data_description.md) describes in detail the contents of `citation_data.json`
    * [directed_edges.csv](dataset/directed_edges.csv) the edgelist of the directed citation network. Sep. `;`, Quote `"`. Columns: `"Source";"Target";"Type";"Year"`
    * [directed_nodes.csv](dataset/directed_nodes.csv) the nodelist of the directed citation network. Sep. `;`, Quote `"`. Columns: `"Id";"Bid";"Title";"Author";"LB";"Year";"Consultation"`
    * [list_citing_monographs.csv](dataset/list_citing_monographs.csv) the list of parsed monographs, from which citations were extracted. Sep. `;`, Quote `"`. Columns: `"id";"bid";"title";"author";"year";"extracted unique citations"`
    * [node_stats.csv](dataset/node_stats.csv) the in and outdegree distribution of each node in the network. Sep. `;`, Quote `"`. Columns: `"id";"bid";"title";"author";"lb";"year";"consultation";"indegree";"outdegree";"degree"`
    * [territorio.csv](dataset/territorio.csv) basic information about all libraries in the Italian Library System (e.g. library code, coordinates. etc.). This data is openly available at <http://opendata.anagrafe.iccu.sbn.it/territorio.zip>.

## Running the notebooks

Assuming that Python is already installed (tested with version 3.5.0), the following dependencies need to be installed as well:

    scipy, numpy, seaborn, pandas, jupyter, igraph
    Vincent Traag's Louvain implementation: https://github.com/vtraag/louvain-igraph

Then launch the notebook server (from the main project folder) with:

    jupyter notebook

A new browser/tab will open pointing at Jupyter's starting page.

## Acknowledgements
The Linked Books team: Matteo Romanello, Martina Babetto, Silvia Ferronato, Laurent Bolli, Vincent Barbay.

This work would not have been possible without the help of several Italian institutions of culture. 
In alphabetical order: the Ca’Foscari University Library System and the Ca’Foscari University Humanities Library (BAUM), the Central Institute for the Union Catalogue of Italian Libraries and Bibliographic Information (ICCU), the European Library of Information and Culture (BEIC), the Istituto Veneto di Scienze Lettere ed Arti, the Marciana Library, the State Archive of Venice.

The project is supported by the Swiss National Fund, with grants 205121_159961 and P1ELP2_168489.

## Please cite as

Giovanni Colavizza. (2017). The Core Literature of the Historians of Venice, Frontiers in Digital Humanities, under review.

    @article{colavizza_core_2010,
      title = {{The Core Literature of the Historians of Venice}},
      journal = {Frontiers in Digital Humanities, under review},
      author = {Colavizza, Giovanni},
      year = {2017}
    }