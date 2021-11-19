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
        "date":"07/10/2021",
        "potholes":"6.9",
        "street":"Cavalier Dr",
        "neighbourhood":"Pembina Strip",
        "location":"-97.300484251164 49.891202741272"
      },
       "status":"OK"
    }
```

	

	
	

	

	

	

	

	

	

	

	
