# Description of the dataset
The file `citation_data.p` contains a list of dictionary items, each one corresponding to a monograph (citing, cited or both). THis file is the pickle version of `citation_data.p` to be found in the repository [LinkedBooksMonographs](https://github.com/dhlab-epfl/LinkedBooksMonographs) ([![DOI](https://zenodo.org/badge/79789632.svg)](https://zenodo.org/badge/latestdoi/79789632)).
The whole dataset comprises 37626 monographs, and contains 71650 citations among them. Citations are unique to two monographs, i.e. there are not multiple citations between the same two monographs.
Note that the age of every citation can be determined using the year of publication of the citing monograph. Both citing and cited monographs are all included in the dataset.

# Fields
   * `author` a string, the author
   * `available_at` a list of dict objects, containing the identifiers of the libraries which have the monographs in Italy, according to the Italian National Catalog
   * `bid` a string, the identifier of the monograph
   * `cited` a list of identifiers of citing monographs
   * `citing` a list of identifiers of citing monographs
   * `dewey_classifications` a list of dict objects, containing Dewey library classifications, if available
   * `id` an Integer, internal id of the monograph. This is the identifier used for graphs.
   * `is_cited` a boolean field, at True if the monograph has been cited at least once
   * `is_citing` a boolean field, at True if the list of references for the monograph has been extracted
   * `lb` a boolean field, at True if the monograph was digitised as part of the Linked Books project
   * `library_info` contains a dict with two fields (if available): `is_consultation`, a boolean field at True if the book is part of the consultation shelves of the library; `n_copies`, the number of copies held by the library
   * `place` a string, the place of publication
   * `publ_country` a string, the publication country (from a controlled vocabulary containing the following fields: `{'DD', 'UA', 'SM', 'JP', 'GB', 'BR', 'AT', 'ME', None, 'HR', 'IN', 'AL', 'BU', 'DZ', 'PL', 'VA', 'UN', 'MC', 'US', 'YU', 'DK', 'MX', 'CH', 'IL', 'SE', 'BG', 'AD', 'TN', 'LU', 'TR', 'BE', 'LK', 'MA', 'LY', 'CI', 'ES', 'FR', 'SU', 'IR', 'UY', 'CY', 'HK', 'VE', 'AR', 'SY', 'PT', 'GE', 'SI', 'NO', 'RS', 'NE', 'EG', 'BO', 'FI', 'NZ', 'LB', 'PE', 'MT', 'CN', 'HU', 'GA', 'GR', 'RO', 'IT', 'CA', 'AU', 'ZM', 'DE', 'SK', 'IE', 'GW', 'PY', 'CS', 'RU', 'CZ', 'LI', 'NL', 'UM'}`)
   * `publ_language` a string, the publication language (from a controlled vocabulary containing the following fields: `{'mlt', 'roh', 'enm', 'jpn', 'eng', 'grc', 'tur', 'mul', 'cze', None, 'fro', 'hrv', 'got', 'nor', 'und', 'rus', 'dut', 'guj', 'swe', 'dan', 'alb', 'gre', 'sla', 'ger', 'nap', 'lat', 'pol', 'mac', 'esp', 'ita', 'frm', 'chi', 'ara', 'srp', 'slv', 'spa', 'mis', 'bul', 'scr', 'por', 'scc', 'cat', 'tib', 'heb', 'rum', 'fre', 'slo', 'abs', 'hun', 'ira'}`)
   * `publisher` a string, the publisher
   * `title` a string, the title
   * `title_orig` a string, the original title information as provided by the Italian National Catalog

# Example
Monograph id: `IEI0084326`

`{'author': 'Loraux, Nicole',
 'available_at': [{'isil': 'RM0267'},
  {'isil': 'RM0210'},
  {'isil': 'RM0106'},
  {'isil': 'NA0070'},
  {'isil': 'PV0367'},
  {'isil': 'PD0370'},
  {'isil': 'RM1045'},
  {'isil': 'RM1337'},
  {'isil': 'TS0165'},
  {'isil': 'BO0442'},
  {'isil': 'BO0036'},
  {'isil': 'BO0451'},
  {'isil': 'BO0465'},
  {'isil': 'MC0166'},
  {'isil': 'MI1256'},
  {'isil': 'TO1203'}],
 'bid': 'IEI0084326',
 'cited': ['MIL0512166'],
 'citing': [],
 'dewey_classifications': [{'cdd': '305.40938',
   'dec': 'GRUPPI SECONDO IL SESSO. DONNE. GRECIA ANTICA',
   'ed': '19'},
  {'cdd': '305.40938', 'dec': 'DONNE. Grecia antica', 'ed': '20'}],
 'id': 20932,
 'is_cited': True,
 'is_citing': False,
 'lb': False,
 'library_info': None,
 'place': 'Paris',
 'publ_country': 'FR',
 'publ_language': 'fre',
 'publisher': 'F. Maspero',
 'title': "Les enfants d'Athéna : idées athéniennes sur la citoyenneté et la division des sexes",
 'title_orig': "Les enfants d'Athéna : idées athéniennes sur la citoyenneté et la division des sexes / Nicole Loraux",
 'year': 1981}`

# Future work
The most pressing tasks are the disambiguation of author names, and the expansion of the dataset.