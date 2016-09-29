# Data Controller Registry

## Data

- Updated daily on ICO website
- Can be downloaded
- CSV format
- Huge horrible HTML block still exists
- Possibly singular form of data

## Parser

- Refine data
    + Use of OpenRefine to refine data
    + Clean data and determine formats
- Possibly build on existing java code? (most likely)
- New parser in python?
- Will have to change from XML handling to CSV handling


## Stats

- Keep current stats
- Think on what else to add?
    + Most referenced data class
    + Most used purpose
    + Most used data disclosee
    + Most Used data subject
    + Go per nature of work
    + Transfer rate

## Storage

- Possibly shift from MongoDB to SQL
- Or just keep current version
- Same for stats
- Would allow better indexing
- Is standard
- May not be slow especially if we cache data

### Classes

- Rethink classes
- Stats objects e.g.
- Data Controller seems mostly fine, maybe some refactoring

## Website

### Rest API

- Makes easy for others to request information
- Will have to think about what data queries or services that can be offered
- NodeJS?

### Website

- SPA
- Vue.js or Angular (not decided)
- D3 for charts and visualisation
- Material design theme
- Better search

## Extensions

### Linked Data

- Think about making this
- Revise ontologies
- Will have to use LODRefine for this possibly

### Interactive app

- Users add companies they work with
- Nice visualisation of data
    + Informations company will have on them
    + Whom it is shared with

### Grading companies on privacy policies

- Use some algorithm to give a grade
