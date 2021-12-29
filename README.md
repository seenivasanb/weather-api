# Weather API

Hi!  The API was created for the **Weather Watch** assignment which is provided by our React JS trainer. As per the assignment requirement, I have updated the mock data and structures. You can fetch the cities and weather reports details by passing the queries.

## Routes

### Get cities by keyword
- we can search and get all the cities by the name which are maching with the keyword 

Query:
```
baseURL/cities?name_like=${keywod}
```
Examples:
* [baseURL/cities?name_like=Che](https://my-json-server.typicode.com/SeenivasanBalakrishnan/weather-api/cities?name_like=Che)
* [baseURL/cities?name_like=Ban](https://my-json-server.typicode.com/SeenivasanBalakrishnan/weather-api/cities?name_like=Ban)

Response:
```json
[
  {
    "id": 1,
    "name": "Chennai"
  },
  {
    "id": 2,
    "name": "Chengalpattu"
  },
  {
    "id": 3,
    "name": "Chethpattu"
  }
]
```


### Get full reports by cityId and unit
- we can get full weather report by the cityId and unit value

Query:
```
baseURL/cities/${cityId}/report?_embed=${unit}
```
Examples:
* [baseURL/cities/3/report?_embed=celsius](https://my-json-server.typicode.com/SeenivasanBalakrishnan/weather-api/cities/3/report?_embed=celsius)
* [baseURL/cities/4/report?_embed=fahrenheit](https://my-json-server.typicode.com/SeenivasanBalakrishnan/weather-api/cities/4/report?_embed=fahrenheit)

Response:
```json
[
  {
    "id": 2,
    "cityId": 2,
    "location": "Chengalpattu",
    "conditions": "Partly Clouds",
    "icon": "/images/weather_icon_partly_cloudy.svg",
    "temp": 32,
    "temp_max": 35,
    "temp_min": 30,
    "feels_like": 33,
    "wind_speed": 2.5,
    "wind_direction": 170,
    "pressure": 842,
    "humidity": 48,
    "celsius": [
      {
        "id": 2,
        "reportId": 2,
        "temp": 32,
        "temp_max": 35,
        "temp_min": 30
      }
    ]
  }
]
```

For more queries refer https://github.com/typicode/json-server/blob/master/README.md
