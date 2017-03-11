# The Core Literature of the Historians of Venice

Repository to go with the article Colavizza Giovanni "The Core Literature of the Historians of Venice", submitted to Frontiers in Digital Humanities in 2017.

This publication is part of the [LinkedBooks project](http://dhlab.epfl.ch/page-127959-en.html). 

## Contents

* `LICENCE` MIT
* `README.md` this file
* `Descriptive statistics and plots.ipynb` Replicates most of the plots and tables in the article.
* `Community explorative igraph.ipynb` Allows to explore several different clustering techniques on the networks.
* `Community metadata evaluation.ipynb` Given a clustering, it explores it in depth, and considers the structural role of the core literature.
* `dataset/`
    * [citation_data.p](dataset/citation_data.p) the citation dataset among monographs on the history of Venice in pickle format.
    * [data_description.md](dataset/data_description.md) describes in detail the contents of `citation_data.json`
    * [citers_subjects.csv](dataset/citers_subjects.csv) the classification of citing monographs, including the original library classification for comparison. See Section 4 of the article for details. Sep. `;`. Quote `"`. Columns: `"Bid";"Author";"Year";"Title corrected";"General category";"Keywords";"Typology";"Period";"Subjects"`.
    * [core_classification.csv](dataset/core_classification.csv) the classification of the core literature in the age and type categories (includes all monographs, even outside of the core). Sep. `;`, Quote `"`. Columns: `"id";"bid";"title";"author";"lb";"year";"consultation";"indegree";"outdegree";"degree";"core_type";"core_age"`
    * [core_classification_core.csv](dataset/core_classification_core.csv) same as core_classification, just limited to the core literature. Sep. `;`, Quote ``. Columns: `id;bid;title;author;lb;year;consultation;indegree;outdegree;degree;core_type;core_age`
    * [metadata.df](dataset/metadata.df) the list of parsed monographs, from which citations were extracted. Sep. `;`, Quote `"`. Columns: `"id";"bid";"title";"author";"year";"extracted unique citations"`
    * [graphs/bibc_1.graphml](dataset/graphs/bibc_1.graphml) the bibliographic coupling network in graphml format, with minimum edge weight of 1 (thus no filtering).
    * [graphs/bibc_nodes.csv](dataset/graphs/bibc_nodes.csv) the node list of the bibliographic coupling network in csv format, with minimum edge weight of 1 (thus no filtering).
    * [graphs/bibc_edges.csv](dataset/graphs/bibc_edges.csv) the edge list of the bibliographic coupling network in csv format, with minimum edge weight of 1 (thus no filtering).
    * [graphs/cocit_2.graphml](dataset/graphs/cocit_2.graphml) the co-citation network in graphml format, with minimum edge weight of 2.
    * [graphs/cocit_nodes.csv](dataset/graphs/cocit_nodes.csv) the node list of the co-citation network in csv format, with minimum edge weight of 2.
    * [graphs/cocit_edges.csv](dataset/graphs/cocit_edges.csv) the edge list of the co-citation network in csv format, with minimum edge weight of 2.
    * [graphs/directed.graphml](dataset/graphs/directed.graphml) the directed network in graphml format, with minimum edge weight of 1 (thus no filtering).
    * [graphs/directed_nodes.csv](dataset/graphs/directed_nodes.csv) the node list of the directed network in csv format, with minimum edge weight of 1 (thus no filtering).
    * [graphs/directed_edges.csv](dataset/graphs/directed_edges.csv) the edge list of the directed network in csv format, with minimum edge weight of 1 (thus no filtering).
    

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

    @article{colavizza_core_2017,
      title = {{The Core Literature of the Historians of Venice}},
      journal = {Frontiers in Digital Humanities, submitted},
      author = {Colavizza, Giovanni},
      year = {2017}
    }