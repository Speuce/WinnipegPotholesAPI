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


## Endpoints

The following is a list of Winnipeg Potholes' current endpoints.

| Name                            | Path                                   | Description                                                     |
| ------------------------------- | -------------------------------------- | --------------------------------------------------------------- |
| Pothole Repair by Neighbourhood | /street/pothole-repairs/neighbourhood  | Searches for pothole repairs by neighbourhood name.             |
| Pothole Repair by Date Range    | /street/pothole-repairs/date-range     | Searches for pothole repairs by the date range (from - to).     |
| Pothole Repair by Street        | /street/pothole-repairs/street         | Search for pothole repairs by street name.                      |

## Resources
This API will provide a list of potholes repairs that fit the specified parameters.

Each pothole repair specifies:
  - `street`: The street whose potholes were filled.
  - `potholes`: The number of potholes that were filled.
  - `date`: The day that the potholes were filled on (DD/MM/YYYY).
  - `neighbourhood`: The neighbourhood that the potholes were in.
  - `location`: GPS coordinates of the exact location that the potholes were filled, using the format `latitude longitude`

**Example**
```json
{
   "result":[
      {
         "street":"Pembina St.",
         "potholes":7.0,
         "date":"07/10/2021",
         "neighbourhood":"St. Norbert",
         "location":"-97.041896292122 49.893670090447"
      },
      {
         "street":"McPhillips St",
         "potholes":1.0,
         "date":"12/11/2021",
         "neighbourhood":"Old Kildonan",
         "location":"-97.147539329009 49.953343390317"
      }
   ]
}
```
