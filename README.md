
# Winnipeg Potholes API
This API returns a list of of completed pothole repairs within the City of Winnipeg, based on data from the [City of Winnipeg's Public Works Department](https://data.winnipeg.ca/Streets/Pothole-Repairs/4mat-mb3w). Using a simple GET request, repairs can be requested by street, neighbourhood, or date range.

Please note that although this API is **FREE**, we require attribution through a link to our repository.


## Parameters 

### Pothole Repair by Neighbourhood 
**neighbourhood_name**
- Name of the the neighborhood. For a list of neighbourhoods, refer to the [City of Winnipeg map](https://data.winnipeg.ca/City-Planning/Neighbourhood/fen6-iygi)
- Type: String
- Length Constraints: Minimum length of 1. Maximum length of 100
- Required: Yes

### Pothole Repair by Date Range 
Searches for pothole repairs by neighbourhood name.  
`/street/pothole-repairs/date-range`

- `from_date`: Beginning date for pothole repairs (Inclusive) (DD-MM-YYYY)
- `to_date`: End date for pothole repairs (Inclusive) (DD-MM-YYYY)

### Pothole Repair by Street 
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
  - `date`: The day that the potholes were filled on (DD-MM-YYYY).
  - `neighbourhood`: The neighbourhood that the potholes were in.
  - `location`: GPS coordinates of the exact location that the potholes were filled, using the format `latitude longitude`

**Example**
```json
{
   "result":[
      {
         "street":"Pembina St.",
         "potholes":7.0,
         "date":"07-10-2021",
         "neighbourhood":"St. Norbert",
         "location":"-97.041896292122 49.893670090447"
      },
      {
         "street":"McPhillips St",
         "potholes":1.0,
         "date":"12-11-2021",
         "neighbourhood":"Old Kildonan",
         "location":"-97.147539329009 49.953343390317"
      }
   ]
}
```


### Sample Requests  
  
  
**These are three sample requests for getting data from 3 endpoints**
```
https://api.data-winnipeg.org/street/pothole-repairs/date-range/json?from_date=10-01-2020&to_date=10-01-2021
```


### Example Response
```json
    {
       "result":[
        {
          "date":"07-10-2021",
          "potholes":"6.9",
          "street":"Cavalier Dr",
          "neighbourhood":"Pembina Strip",
          "location":"-97.300484251164 49.891202741272"
        },
    ],
    "status":"OK"
    }
```
