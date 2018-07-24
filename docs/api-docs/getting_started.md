---
layout: default
title: API Basics
nav: basics
---

### Getting Started

The current version of the API lives at `https://api.mabrian.com/v1/path`.

As usual, you can use GET requests using `curl`


    $ curl -X GET --header 'Accept: application/json' 'https://api.mabrian.com/v1/status/'    
    {"status":"good","last_updated":"2018-07-20T09:55:21Z"}     
    $    

Or even better, using python-requests

```
import requests     
resp = requests.get('https://api.mabrian.com/v1/status/')     
print resp.json()    
#{"status": "good", "last_updated": "2018-07-20T09:55:21Z"}    
```

#### Versions

| Version         | Date         | Changes |
| -------------   | -------------| --- |
| ```version 1``` | 1/2/2018   | Initial deployment |

#### Endpoints

| Endpoint | What it does |
| ------------- | -------------|
| ```/airdata/searches/``` | Returns Searches insights (adv search days, adv stay days, etc) based on query parameters
| ```/airdata/bookings/``` | Returns Bookings insights (booking type, adv purchase days, adv stay days, etc) based on query parameters
| ```/airdata/capacity/``` | Returns a monthly basis array of Capacity insights (pax, connections, flights, etc) based on query parameters
| ```/airdata/flight_prices/``` | Returns a monthly basis array of Flight rates based on query parameters


<body id="basics"></body>
