### Sample Requests  
  
  
**These are three sample requests for getting data from 3 endpoints**
```
https://api.data-winnipeg.org/pothole-required-by-neighbourhood/json?neighbourhood_name=st%20vital
https://api.data-winnipeg.org/pothole-repair-by-date-range/json?from_date=10/1/2020&to_date=10/1/2021
https://api.data-winnipeg.org/pothole-repair-by-street/json?street_name=wellington%20st
```
Note: '%20' means space character


### Example Response
```
    {
      "results":
      {
        "task_date":"2021 Feb 28 12:00:00 AM",
        "block_id":"8,682",
        "potholes":"6.9",
        "street_name":"Cavalier Dr",
        "from_street":"Hamilton Ave",
        "to_street":"Hillary Cr",
        "weight_in_kg":"171.29",
        "weight_in_tonnes":"0.17",
        "electoral_ward":"River Heights - Fort Garry",
        "neighbourhood":"Pembina Strip",
        "location":"LINESTRING (-97.300484251164 49.891202741272, -97.300912640968 49.892591236442)"
      },
       "status":"OK"
    }
```

	

	
	

	

	

	

	

	

	

	

	
