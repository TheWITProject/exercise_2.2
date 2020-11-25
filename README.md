## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
```
```
{
    "candidates": [
        {
            "formatted_address": "1000 5th Ave, New York, NY 10028, United States",
            "name": "The Metropolitan Museum of Art",
            "opening_hours": {
                "open_now": false
            }
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
# paste the request verb and URL here
```
```
{
    "candidates": [
        {
            "opening_hours": {
                "open_now": false
            }
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get just the address for the CUNY Graduate Center?
```
# paste the request verb and URL here
```
```
{
    "candidates": [
        {
            "formatted_address": "365 5th Ave, New York, NY 10016, United States",
            "name": "CUNY Graduate Center"
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
# paste the request verb and URL here
```
```
# paste the response data here
```
<br>

- What are five pizza places near your college?
```
https://maps.googleapis.com/maps/api/place/textsearch/json?query=Pizza+Restaurants+Near+Baruch+College&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8&fields=name,formatted_address,opening_hours,rating
```
```
{
    "html_attributions": [],
    "next_page_token": "ATtYBwKC_qazzgl1btwY_YB3naHVEYTZrTcUZeedoRvXIwV0tSlhV5-fhMnjhZ7FlMgZPPNzbvfXGhSdKB0xBW4918KEiWdTCfNIpienUpkZX1Yz3cWKJ3cQcudEHCVrE5878QJK9SUp2GsOzTYxtxGITNPUcNT3KbHnCDWwS-4DrBZ7AJrwWe-fehsdhPScd5b3E64whd2zff9WKzC-hRJVIYtLCIVXTHFat4dlmw1Yfuo3SKuBfV75pqgQWu1J2ddtXGkzJA989zqRODuOPqdn7RGiIkR2kr4Et9luWvHOYwTAUiKv-YUyrrJxzRuEhjv8GZ1_0YLM32OtCqVMbGN83bamr-VhaV2GxIOAHTrOkPl2DeYcLYonnYNU8sDC6TM3t1P9eQkCxPMk-eb2jMtKETCPGIly_UM1CtDlL_l9l2_Exmo",
    "results": [
        {
            "business_status": "OPERATIONAL",
            "formatted_address": "350 3rd Ave, New York, NY 10010, United States",
            "geometry": {
                "location": {
                    "lat": 40.740668,
                    "lng": -73.982168
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74196022989271,
                        "lng": -73.98067827010728
                    },
                    "southwest": {
                        "lat": 40.73926057010727,
                        "lng": -73.98337792989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "La Vera Pizzeria",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1015,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/101692531050653106899\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwInG3TMZUDbXWvFo7oNm_m6ldyCGySgtmVm83qwIlCGTlauKgH4RboPb3zL4L9ezLqPQwxbJ9TnDRSrhe9jHn_0AOFHfhTl838B2Xfi-4wIVfbhLbkak-i2SdZlyujIYMyqB5kX0Gz3yLT7mdGYIM5CDvUHEfQ30SXk3Ehmg_qoKyaY",
                    "width": 1600
                }
            ],
            "place_id": "ChIJjfdC8AlZwokRi91iOFbM9aM",
            "plus_code": {
                "compound_code": "P2R9+74 New York",
                "global_code": "87G8P2R9+74"
            },
            "price_level": 1,
            "rating": 4.1,
            "reference": "ChIJjfdC8AlZwokRi91iOFbM9aM",
            "types": [
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 193
        },
        {
            "business_status": "OPERATIONAL",
            "formatted_address": "245 3rd Ave, New York, NY 10010, United States",
            "geometry": {
                "location": {
                    "lat": 40.73694,
                    "lng": -73.98416499999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73835007989272,
                        "lng": -73.98295612010727
                    },
                    "southwest": {
                        "lat": 40.73565042010728,
                        "lng": -73.98565577989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Lunetta",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 2988,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/117619621850691033153\">bethliz irizarry</a>"
                    ],
                    "photo_reference": "ATtYBwJI-87j81PlD3ahDZj75m2zXmO5x8Geq7KgUPtEPgcAbfBxtJQh6NX_B2ztGXJxt3L__4fUi8PGtavahfJ2eNVqgO9qzzdB-Atb8ouUwU3SM-0ZSY39A6pG2dcNIAoyU_e9T55CZwCAAKZ55vGnEZU8KCMbHKZ1tNbMkhgybULmnfAv",
                    "width": 5312
                }
            ],
            "place_id": "ChIJ5Q-Ra6BZwokRd1gGerJ74s8",
            "plus_code": {
                "compound_code": "P2P8+Q8 New York",
                "global_code": "87G8P2P8+Q8"
            },
            "price_level": 1,
            "rating": 4.1,
            "reference": "ChIJ5Q-Ra6BZwokRd1gGerJ74s8",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 274
        },
        {
            "business_status": "OPERATIONAL",
            "formatted_address": "415 2nd Ave #4044, New York, NY 10010, United States",
            "geometry": {
                "location": {
                    "lat": 40.7385388,
                    "lng": -73.98068409999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73985342989273,
                        "lng": -73.97924992010728
                    },
                    "southwest": {
                        "lat": 40.73715377010728,
                        "lng": -73.98194957989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Mike's Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 800,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/107333537688036830468\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwLBFsz1kZ0wV62Nw_AOqa8kWgouQ0UyczwScsjNqxLmLtFd9DqBgRmhlC39tG7xuINsHyxnHrAW3MXof2no-vVcIV1rRyg0ZlqHkwhz6VACBZTJM7gqzAz2xGd3sdb05mDwY3gbLjE6qu7P3qwMXlmvONydM_TwA6RE0cYwmCb1F6yL",
                    "width": 1200
                }
            ],
            "place_id": "ChIJJSedSQpZwokRrv_jfarn6WM",
            "plus_code": {
                "compound_code": "P2Q9+CP New York",
                "global_code": "87G8P2Q9+CP"
            },
            "price_level": 1,
            "rating": 4.1,
            "reference": "ChIJJSedSQpZwokRrv_jfarn6WM",
            "types": [
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 295
        },
        {
            "business_status": "OPERATIONAL",
            "formatted_address": "257 Park Ave S, New York, NY 10010, United States",
            "geometry": {
                "location": {
                    "lat": 40.7387204,
                    "lng": -73.9872144
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74009552989272,
                        "lng": -73.98592687010728
                    },
                    "southwest": {
                        "lat": 40.73739587010728,
                        "lng": -73.98862652989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Bravo Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 4472,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/100840418295435941149\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwLS4RGzEbeldCjSrFO9LPZjHLQh-dLDHlRQz5WmGtTGC_IrY0iAVwp-KqmPQl-y8Z6X1hZoan3OkRAQpD2_gxOiVvP0617EzxCGMy8Pgc5s1-R2MI1carxXPN6s0H4OBl6IM9CBUzZA--u-0ZKsEOnX9dG2SvZ5s7MeZ1O1q2rjtd7V",
                    "width": 7952
                }
            ],
            "place_id": "ChIJ2WXqCqFZwokRK4TaGtes0_0",
            "plus_code": {
                "compound_code": "P2Q7+F4 New York",
                "global_code": "87G8P2Q7+F4"
            },
            "price_level": 1,
            "rating": 4.2,
            "reference": "ChIJ2WXqCqFZwokRK4TaGtes0_0",
            "types": [
                "meal_delivery",
                "meal_takeaway",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 338
        },
        {
            "business_status": "OPERATIONAL",
            "formatted_address": "365 3rd Ave, New York, NY 10016, United States",
            "geometry": {
                "location": {
                    "lat": 40.7409157,
                    "lng": -73.98141389999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74226552989272,
                        "lng": -73.98006407010728
                    },
                    "southwest": {
                        "lat": 40.73956587010728,
                        "lng": -73.98276372989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Macchina",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1152,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/111470257242441946693\">Macchina Restaurant</a>"
                    ],
                    "photo_reference": "ATtYBwKdSXaE_l8bZr-tQkupKXchmvvCiwEZ3V4RsCSpdjvBayqD_j93bPXRSflkeyXdB8qDk9AO9diSsuFu_MtpUf6uRgIsCO47I4ZydGge8PPTooVF8qW2-Eloei1LErzOYsklifMJ13FnqR36XpUOJ_vSfEc5mQlQKyk1hFDxpeeJESwp",
                    "width": 2048
                }
            ],
            "place_id": "ChIJ_UYE6CT2wokR70UjCEbKxXM",
            "plus_code": {
                "compound_code": "P2R9+9C New York",
                "global_code": "87G8P2R9+9C"
            },
            "price_level": 2,
            "rating": 4.2,
            "reference": "ChIJ_UYE6CT2wokR70UjCEbKxXM",
            "types": [
                "meal_delivery",
                "meal_takeaway",
                "bar",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 218
        },    
    ],
    "status": "OK"
}
```
<br>

**Directions API**
- Can you get directions from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL here
```
```
# paste the response data here
```
<br>

- Can you get directions from Oakland, CA to Brooklyn, NY?
```
# paste the request verb and URL here
```
```
# paste the response data here
```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL here
```
```
# paste the response data here
```
<br>

- Can you get the travel time from Oakland, CA to Brooklyn, NY?
```
# paste the request verb and URL here
```
```
# paste the response data here
```

## Already done?
Play around with some other public APIs. [Here is a great list](https://github.com/public-apis/public-apis).
