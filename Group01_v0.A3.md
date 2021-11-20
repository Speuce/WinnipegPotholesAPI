# Winnipeg Potholes API
This API returns a list of of completed pothole repairs within the City of Winnipeg, based on data from the [City of Winnipeg's Public Works Department](https://data.winnipeg.ca/Streets/Pothole-Repairs/4mat-mb3w). Using a simple GET request, repairs can be requested by street, neighbourhood, or date range.

## Endpoints

The following is a list of the API's endpoints.

### Pothole Repair by Neighbourhood 

**Path:** `api.data-winnipeg.org/street/pothole-repairs/neighbourhood`  
  
Searches for pothole repairs by neighbourhood name. For a list of neighbourhoods, refer to the [City of Winnipeg map](https://data.winnipeg.ca/City-Planning/Neighbourhood/fen6-iygi).  

**Parameters:**  
- `neighbourhood`: Name of neighborhood. Spaces must be replaced with underscores '`_`'.

### Pothole Repair by Date Range

**Path:** `api.data-winnipeg.org/street/pothole-repairs/date-range`  
  
Searches for pothole repairs by neighbourhood name.  

**Parameters:**  
- `from_date`: Beginning date for pothole repairs (Inclusive) (DD-MM-YYYY)
- `to_date`: End date for pothole repairs (Inclusive) (DD-MM-YYYY)

### Pothole Repair by Street

**Path:** `api.data-winnipeg.org/street/pothole-repairs/street`  
  
Searches for pothole repairs by street name.  

**Parameters:**  
- `street`: Name of street. Spaces must be replaced with underscores '`_`'.

## Resources

This API will provide a list of potholes repairs that fit the specified parameters.

Each pothole repair specifies:
  - `street`: The street whose potholes were filled.
  - `potholes`: The number of potholes that were filled.
  - `date`: The day that the potholes were filled on (DD-MM-YYYY).
  - `neighbourhood`: The neighbourhood that the potholes were in.
  - `location`: GPS coordinates of the exact location that the potholes were filled, using the format `latitude longitude`

**Example Resource**
```json
{
	"street":"Pembina St.",
	"potholes":7.0,
	"date":"07-10-2021",
	"neighbourhood":"St. Norbert",
	"location":"-97.041896292122 49.893670090447",
}
```


### Sample Request  
  
  
**This is a sample request for getting data from one of the API's endpoints**
```
https://api.data-winnipeg.org/street/pothole-repairs/date-range/json?from_date=10-01-2020&to_date=10-01-2021
```

**Sample Response**
```json
{
	"result":[
		{
			"date":"07-10-2021",
			"potholes":"6.0",
			"street":"Cavalier Dr",
			"neighbourhood":"Pembina Strip",
			"location":"-97.300484251164 49.891202741272",
		},
	],
}
```
