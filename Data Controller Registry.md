# Data Controller Registry

## Data

- Updated daily on ICO website
- Can be downloaded
- CSV format
- Huge horrible HTML block still exists
- Possibly singular form of data
- Using OpenRefine to clean data

### Verdict

- OpenRefine not quite successful for this yet, regex doesn't work well and no need for it either as such since we have a rigid-ish parser present already
- Need to parse it and then run the parsed version through open refine since most of the important data is stuck in the HTML block
- Will need to normalise the data classes, subjects etc.
- Will need to find a way to extract this from the prose 
- **TODO**: Live chat or email about data quality

### Observations

- Format is a lot more strucutred now
- But can still use a lot more improvement

#### Data Controller Format

As per data controller

- Registration number
- Organisation Name
- Companies House Number *optional*
- Address (up to 5 lines)
- Postcode (optional)
- Country (not complete, but can complete)
- Freedom of information flag (being a public authority under FOI 2000)
- Start date registration
- End date registration
- Exempt processing flag ( processes some data which it does not have to notify about)
- Trading names (separated by `|`)
- Representative
    + Title (Mrs, Ms, Mr, Dr)
    + First Name
    + Last Name
    + Address (up to five lines)
    + Telephone
    + Postcode
    + Email
    + Job Title
    + *Notes*
        * If the address may not be provided, we should just use 
- Entry url (not needed since we can just add the registration number to the URL which we know : `https://ico.org.uk/ESDWebPages/Entry/` + registration)
- Nature of work (multiple, separated by `/` or `,` possibly more - all types available at https://ico.org.uk/for-organisations/register/nature-of-work/ but can make their own too)
- Reasons for processing information (mostly prose, sometimes list - will need filtering out as well as normalising)
- classes of information processed (mostly list form, sometimes prose - will need filtering out as well as normalising) - *Data classes*
- sensitive classes of information (mostly list form, sometimes prose - will need filtering out as well as normalising) *Sensitive data classes*
- whom the information is processed about (mostly list, sometimes prose - will need filtering out as well as normalising) - *Data subjects*
- whom the information may be shared with (mostly list, sometimes prose - will need filtering out as well as normalising) - *data recipients*
- Other purposes for collecting information
    + 5 types
        * Providing financial services and advice
        * Consulting and advisory services
        * Undertaking research
        * Consulation
        * Trading and sharing personal information
    + Each contains information about data classes, subjects and recepients, but generally in prose
- Transfer policy (outside the EEA or not)

## Parser

- Refine data
    + Use of OpenRefine to refine data
    + Clean data and determine formats
- Possibly build on existing java code? (most likely)
- New parser in python? C#?
- Will have to change from XML handling to CSV handling

### Verdict:
- No need for a new parser


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
- Open Data stuff to look at
    + Open data at soton
    + data.gov.uk
    + bbc things
    + FOAF

### Verdict

- Semantic web is around, but not sure how to incorporate with current data
- Personal knowledge is outdated
- Google search uses schema.org
- Recommended data structure is JSON-LD (JavaScript Object Notation for Linked Data)
    + This is where I can look into


### Interactive app

- Users add companies they work with
- Nice visualisation of data
    + Informations company will have on them
    + Whom it is shared with

### Grading companies on privacy policies

- Use some algorithm to give a grade

### Comparison of companies

- Compare similar companies or any type of company