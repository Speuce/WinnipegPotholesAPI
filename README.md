# WinnipegPotholesAPI
Winnipeg Potholes API

## Parameters 
### ENDPOINT 1 NAME
**neighbourhood_name**
- Name of the the neighborhood. For a list of neighbourhoods, refer to the [City of Winnipeg map](https://data.winnipeg.ca/City-Planning/Neighbourhood/fen6-iygi)
- Type: String
- Length Constraints: Minimum length of 1. Maximum length of 100
- Required: Yes

### ENDPOINT 2 NAME
**from_date**
- Beginning date for pothole repairs (Inclusive)
- Type: String
- Length Constraints: Must be of length 10
- Pattern: DD-MM-YYYY
- Required: Yes

**to_date**
- End date for pothole repairs (Inclusive)
- Type: String
- Length Constraints: Must be of length 10
- Pattern: DD-MM-YYYY
- Required: Yes

### ENDPOINT 3 NAME
**street_name**
- Name of the the street
- Type: String
- Length Constraints: Minimum length of 1. Maximum length of 100
- Required: Yes