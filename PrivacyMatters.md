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

## Storage
- MongoDB
- Store as JSON objects
- Same for stats
- Repetition of data

### Classes

#### Data Controllers

- Data Controller Class
    + Regisration number
    + Org name
    + Trading name    
    + Companies House Number
    + Address 
    + Postcode
    + Country
    + Exemption flag
    + Freedom of Information Flag
    + Uk Contact
    + Format type (old or new)
    + Start and end date of controller
- New Format
    + List format of 
        * Purposes
        * Data classes
        * Sensitive data classes
        * Data subjects
        * Data Disclosees
        * Other Purpose object
            - A statement and purpose string (generally 4 types like CCTV and protection etc.)
- Old Format
    + List of Purpose objects
        * Name of purpose
        * Description of purpose
        * List of
            - Data Classes
            - Data Subjects
            - Data Disclosees

#### Statistics

- Generat Statistics
    + Total controllers
    + Count for those which had
        * Address
        * Companies House Number
        * Trading name
    + Count for (unique)
        * Natures of work
        * Old format
        * New Format
        * Purposes
        * Data classes
        * Sensitive Data classes
        * Data Subjects
        * Data Disclosees
    + Median for count of (for each controller)
        * Data classes
        * Sensitive data classes
        * Data Subjects
        * Data Disclosees
- Statistic Object
    + Used for
        * Data Classes
        * Sensitive Data
        * Data Subjects
        * Data Disclosees
    + Type property (like the data class etc.)
    + Number of companies using this type
    + List of companies (registry list item object)
- Registry List Item
    + Comany name and registration number
    + For quick access and small information to store
- Advanced Statistic Object
    + Used for purposes
    + Extends Statistic Object
    + Extra addition: Median amount of (for each purpose)
        * Data Classes
        * Data Subjects
        * Data Disclosees
- Nature of work object
    + Used for nature of work
    + Extends Advanced Statistic Object
    + Extra addition: Median amount for (for each nature of work)
        * Sensitive Data Classes

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