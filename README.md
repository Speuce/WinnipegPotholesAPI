# WinnipegPotholesAPI
Winnipeg Potholes API


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