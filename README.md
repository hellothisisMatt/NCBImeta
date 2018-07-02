[![GitHub (pre-)release](https://img.shields.io/badge/Release-v0.3.1-red.svg)](https://github.com/ktmeaton/NCBImeta/releases/tag/v0.3.1)
[![GitHub license](https://img.shields.io/dub/l/vibe-d.svg?style=flat)](https://github.com/ktmeaton/NCBImeta/blob/master/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/ktmeaton/NCBImeta.svg)](https://github.com/ktmeaton/NCBImeta/issues)


# NCBImeta
Creates a SQLite database of metadata from the NCBI database.  

<img src="https://github.com/ktmeaton/NCBImeta/blob/master/images/NCBImeta_screenshot.png" alt="NCBImeta_screenshot" width="500px"/> <img src="https://github.com/ktmeaton/NCBImeta/blob/master/images/NCBImeta_snapshot.jpg" alt="NCBImeta_snapshot" width="500px"/>

 
## Python Requirements
Python2.7+, Python3.4+  
SQLite3 (sqlite3 in Python3.4+, pysqlite in Python2.7+)     
BioPython 1.70    

```
pip install --user biopython 
```

## Version

Development - Version 0.3.2 (v0.3.2)  
Release - Version v0.3.1 (master)

## Installation

Release  
```
git clone https://github.com/ktmeaton/NCBImeta.git   
cd NCBImeta  
```
Development: 
```
git clone -b v0.3.2 https://github.com/ktmeaton/NCBImeta.git   
cd NCBImeta  
```
## Quick Start Example

### Run the program
```
python src/NCBImeta.py --config example/config.py
```

### Annotate the database with a curated tab-separated text file of metadata
```
python src/NCBImeta_Annotate.py --database example/my_organism_db.sqlite --annotfile example/my_organism_annot.txt --table BioSample
```

Note that the first column of your annotation file MUST be a column that is unique to each record. An Accession number or ID is highly recommended. The column headers in your annotation file must also match exactly the names of your columsn in the database.

### Export the database to tab-separated text files by table.
```
python src/NCBImeta_Export.py --database example/my_organism_db.sqlite --outputdir example/
```

## Currently Supported NCBI Tables  
Assembly  
BioProject  
BioSample  
Nucleotide  
SRA  

## Up-Coming Features
PubMed Table 
Any requested tables or metadata :)  

## Suggested Accessory Programs
### Database Browser
DB Browser for SQLite: https://sqlitebrowser.org/  

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

See CHANGELOG.md.

## License

This project is licensed under the MIT License - see the LICENSE file for details.    

## Credits

author: Katherine Eaton (ktmeaton@gmail.com)

## Helpful Development Commands  
Merging a development branch into master:  
        (on branch development)$ git merge master  
        (resolve any merge conflicts if there are any)  
        git checkout master  
        git merge --no-ff development (there won't be any conflicts now)  

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
