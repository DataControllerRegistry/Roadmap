# Privacy Matters

## Data
- XML Formatted data
- Different forms of data

### Old Format
- Properly define XML for different data features
- Many purposes, defined correctly
- Defined form for data subjects, data classes and data disclosees
- Each purpose had its own data subjects, classes and disclosees

### New Format
- One big xml tag full of html version of what is on the website
- Purposes in prose (paragraph form separated commas)
- Similar for data classes etc. but rarely
- New data: Nature of work
- Pain to parse through

## Parser
- Written in java
- XML Parser
- Robust for edge cases
- Parses the big block of html

## Storage
- MongoDB
- Store as JSON objects
- Same for stats
- Repetition of data

## Stats

### General Stats

- Total companies
- Which companies contain optional data
    + Address
    + Postcode
    + Trading name
    + Companies House Number
- New format count
- Old format count
- Total different natures of work
- Total different (sensitive included) data classes, subjects, disclosees
- Median number of (sensitive too) data classes, subjects, disclosees

### Data Classes/Subjects/Disclosee stats

- Type/name of the item
- Company names and registration numbers
- Number of companies

### Old Purpose and Nature of Work stats

- Company names and registration numbers
- Number of companies
- Median number of (sensitive too) data classes, subjects, disclosees
    + Old purpose format does not have sensitive data

## Website

- Play Framework based web app
- Twitter bootstrap for look and feel
- MVC type applicaton
- No Rest api (umm)
    + Everything loaded server side and passed through to the page when it first loads
    + Values are hidden in the html and retrieved when needed
    + The values are static so this was okay to do
- Moris js charts for the stats
- Basic search by company names