## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=place_id,name,geometry/location,photos&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "html_attributions": [],
    "result": {
        "geometry": {
            "location": {
                "lat": 40.7794366,
                "lng": -73.963244
            }
        },
        "name": "The Metropolitan Museum of Art",
        "photos": [
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115967679611787063919\">Richard Stark</a>"
                ],
                "photo_reference": "ATtYBwLzoSiyvAJh9zVke2egB5G6j2f1E3Oje6OIXJm5Ffsx-f9VxRzswIPWTEvwyNlDp93FobB3_IIPNT3fEyp8a9qpNCCEBUSMEvbeA6FsTNJuUVeYzwqy8nKAEdT-RzWr6Zl2FityxMLnu4IfEuxC_681XlzB9G0Y4xlReJI6Ib9eTXSd",
                "width": 4032
            },
            {
                "height": 800,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106748439247716180853\">Karl 1974</a>"
                ],
                "photo_reference": "ATtYBwIqhlPMls0HnFld-w6voTt10CCAQNOO77mNyvmCw_vXk5PltZ_2akTyeUNX7gdqvMitDaYCby0XqD2BZ63zTBBrfB3buiwBW9YKZPlKg2q5F_fpZFv4XsauGZiHx1dMv6g1FlXaM0LmMNBt-gPQ5W-fsVuZsBEPa_CYh2lJOOizdx8D",
                "width": 800
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/105280404763450371863\">Sabrina Nazario</a>"
                ],
                "photo_reference": "ATtYBwK4AKmWJwCiiiZ8vXJcVPoaX3DRfJLiPb0QpmHtOIzLIPX_1QlF1A12s5js4lCgu8il1oebaYnyI6_uqg1n867tIIpRlyJ95RNX_VojIIxZ5kkFw4ORvno1_0Oth1lpCIKPCN3GStx89uQ_-sMbaiTyUidbHU94ZroFxLECbgrONsV_",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114414941791922473064\">YehHsiang Chen</a>"
                ],
                "photo_reference": "ATtYBwJYvaXHrpb1YWLTSfsgcLS29ULy_v2YDIxwGmqoMgVWBR1LgSWYJHca_0qkpwCW2HUvNGp065O0vU7qC7XsiPAgMiPMc6u2HqxliNDwmO3Ek3qyU6kNUrK1EgUOAO5gURF-UpWANsr6ccvtNoeulZTPfVQVsOC3wi13FqdsRQsGJyMk",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114217576882578419305\">Eva Mikulcic</a>"
                ],
                "photo_reference": "ATtYBwLmQ63gGeUcTrWQKAe5asjpPXoPu2ROi9tpAYBLvBFirLELE4P2yNmEykCT1KsVrRUP-KeIhmp0vcmfX5PmspNT1upmw-sSvESgGld3dvOwfdvOopTub6wxLpNJ1oJ6T0_awt2pFRQyboWet0fNVj2rfDXKadDl0pjUs4LGCu7JNkku",
                "width": 4032
            },
            {
                "height": 5304,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115568864800951782024\">Kenneth Hines, Jr.</a>"
                ],
                "photo_reference": "ATtYBwKALOiXhrJ0LgqkksGK3CEVvH41xRV1u7E-Sq8sbYQ5U3Z2b6MLfs4GCX3j9w8RqMvQdFg92KZomnId1aZ9moQ8BJeymSO7W0sSJkFV234LD7eigFr6R2FLfF1Ja5uVP7tF_xW-fgSdiOvqi4MInZiLzCkyII-WEwBRsdwylceMStI2",
                "width": 7952
            },
            {
                "height": 3456,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108035579848062480030\">Jefferson Nyilas</a>"
                ],
                "photo_reference": "ATtYBwJBpkYNJH0b2PUY3Z4XanB3TrLc3ZC5hwJNV05-rFazkhWUjMixQbYrz90HckRMXH5IztFd-y41y32Ydn_Ix3qHJL2u3A_kBRStskgGcDrkfStYZJQcMbe3l5YUgtqXkaqWy2W-HymPORJCNc2VHZ7MWGsIYY5m-BdKJrSsJ7DbovLK",
                "width": 4608
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107487783334312254168\">Giada Baldi</a>"
                ],
                "photo_reference": "ATtYBwKFK-UKq7Zn4OJiNG0hAV7R9EJrWl0sQUWFPdRv7dyEE-FEDVOTh6BRakEV8vDNNQpy78gP86NSHPcCqa6NMjS0VG_cJqPsQva8t5e-mX6j6p5eaECM0-BedpRlyV8DmvU446_9JDfOS3I5PNASw2nJs6GNaTVoh8bTpV3Y7TiQ3Fkr",
                "width": 4032
            },
            {
                "height": 2484,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108919448933946114771\">Carlos Aviles</a>"
                ],
                "photo_reference": "ATtYBwKuVn5Pw1D0iCXSoqve5BGKThEmf7TIeA_AOhaC2qRvIK-fpF9QxuadzGLaaA5GMCGltQOnScMCKfVI2BeT75qMPZ5w2bTf3et_anZuLI6DDVENbH80-OM2EWTPEgrURDCb_aBKLLDlagZP40XFXkvbD7Pm_J0VcDySZNGrCKchb8Cj",
                "width": 2739
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/109850608939875361213\">jamil blackmon</a>"
                ],
                "photo_reference": "ATtYBwKB9KsGiE6hSgHKPvQsXYFDwVcgP_D5rM9DfEoxS8g0QTNMqF9AMFqxwt8P4JpEuSFmFTZ3-QbY-UELh2WNQclwc5CswLNIjnfkz4dlaa1nRJzLTAFtUQkJF4TadPCpnaRXfueFclPi2NBE176J3f0EYYLbUyYEyTXpAMVQVxrfvMA0",
                "width": 4032
            }
        ],
        "place_id": "ChIJb8Jg9pZYwokR-qHGtvSkLzs"
    },
    "status": "OK"
}
```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=place_id,name,opening_hours&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "html_attributions": [],
    "result": {
        "name": "The Metropolitan Museum of Art",
        "opening_hours": {
            "open_now": false,
            "periods": [
                {
                    "close": {
                        "day": 0,
                        "time": "1700"
                    },
                    "open": {
                        "day": 0,
                        "time": "1000"
                    }
                },
                {
                    "close": {
                        "day": 1,
                        "time": "1700"
                    },
                    "open": {
                        "day": 1,
                        "time": "1000"
                    }
                },
                {
                    "close": {
                        "day": 4,
                        "time": "1900"
                    },
                    "open": {
                        "day": 4,
                        "time": "1200"
                    }
                },
                {
                    "close": {
                        "day": 5,
                        "time": "1900"
                    },
                    "open": {
                        "day": 5,
                        "time": "1200"
                    }
                },
                {
                    "close": {
                        "day": 6,
                        "time": "1700"
                    },
                    "open": {
                        "day": 6,
                        "time": "1000"
                    }
                }
            ],
            "weekday_text": [
                "Monday: 10:00 AM – 5:00 PM",
                "Tuesday: Closed",
                "Wednesday: Closed",
                "Thursday: 12:00 – 7:00 PM",
                "Friday: 12:00 – 7:00 PM",
                "Saturday: 10:00 AM – 5:00 PM",
                "Sunday: 10:00 AM – 5:00 PM"
            ]
        },
        "place_id": "ChIJb8Jg9pZYwokR-qHGtvSkLzs"
    },
    "status": "OK"
}
```
<br>

- Can you get just the address for the CUNY Graduate Center?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=place_id,name,formatted_address&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```{
    "html_attributions": [],
    "result": {
        "formatted_address": "365 5th Ave, New York, NY 10016, USA",
        "name": "CUNY Graduate Center",
        "place_id": "ChIJRRI8walZwokRCPoUQ0TSCoQ"
    },
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
https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=40.8200471,-73.9492724&radius=50&type=restaurant&keyword=pizza&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "html_attributions": [],
    "results": [
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.8191441,
                    "lng": -73.95228609999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.82046017989272,
                        "lng": -73.95085582010728
                    },
                    "southwest": {
                        "lat": 40.81776052010728,
                        "lng": -73.95355547989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Pepo’s Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 822,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/105259786586434839237\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwKq1BFBa_TJ27l8V4_eIdSwmHAVFXi7xorZeksmmdEOgITbVBCk-XJyD-otes4l-uOskN7sCrPThPUZWUekCRck26_pg8GEwDq4IqECon7UW8W0L1CjSNr7y3Lxb3wZfBiqYMidz2e2TzOw62qgpsk6s-CSDFWxtwQQDBqbxQkPW6j8",
                    "width": 1024
                }
            ],
            "place_id": "ChIJ1y7mQm_2wokRPqoqstcPkq0",
            "plus_code": {
                "compound_code": "R29X+M3 New York",
                "global_code": "87G8R29X+M3"
            },
            "price_level": 1,
            "rating": 4.4,
            "reference": "ChIJ1y7mQm_2wokRPqoqstcPkq0",
            "scope": "GOOGLE",
            "types": [
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 116,
            "vicinity": "1522 Amsterdam Ave, New York"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.8214251,
                    "lng": -73.95063569999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.82274292989272,
                        "lng": -73.94919132010727
                    },
                    "southwest": {
                        "lat": 40.82004327010728,
                        "lng": -73.95189097989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Fumo Harlem",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1440,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/103345303588623381815\">Jaselyn D</a>"
                    ],
                    "photo_reference": "ATtYBwJlVJaOmDNhYUCcXqqyYq3lIrKh0YPgwwp8PiHiOfszFpZVHKhq40gn4hM_jmI6g0SI38xqymsU44_-V8gDLi6os2_bjLznPaWh42eZu8mYg08h820W9P1oxXYS62aS2N5ZHpbKvpuOUiEroZ5ROgakxgSOajKyGMuPJ-p-tke-KnUp",
                    "width": 1440
                }
            ],
            "place_id": "ChIJLe70p2X2wokReDA-X8LGqZE",
            "plus_code": {
                "compound_code": "R2CX+HP New York",
                "global_code": "87G8R2CX+HP"
            },
            "price_level": 2,
            "rating": 4.5,
            "reference": "ChIJLe70p2X2wokReDA-X8LGqZE",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 866,
            "vicinity": "1600 Amsterdam Ave, New York"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.8213656,
                    "lng": -73.9507102
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.82267317989272,
                        "lng": -73.94925712010728
                    },
                    "southwest": {
                        "lat": 40.81997352010728,
                        "lng": -73.95195677989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Uncle Tony's Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 2554,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/102498524092436005137\">Ari Miller</a>"
                    ],
                    "photo_reference": "ATtYBwLrVsqUKHdiqup0gOhP_YeUaWHNB9P12ZsS5RAz1PDtm6Ot5Wd70bR7frOm-8zYbbCrRWol-TxYR_8M-D_D7zwjjPTSWWMtF4-MAzOcMKHkPIEzmOFk_GMmFUp_3FtjJCYa8n3_Kg4sjGiU6k1y5Zty7IpdUC0g2BrZ3hGsDa29c-4-",
                    "width": 3558
                }
            ],
            "place_id": "ChIJBQyPp2X2wokR-aiSMzFop-c",
            "plus_code": {
                "compound_code": "R2CX+GP New York",
                "global_code": "87G8R2CX+GP"
            },
            "price_level": 1,
            "rating": 4.5,
            "reference": "ChIJBQyPp2X2wokR-aiSMzFop-c",
            "scope": "GOOGLE",
            "types": [
                "meal_delivery",
                "meal_takeaway",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 194,
            "vicinity": "1596 Amsterdam Ave, New York"
        }
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
https://maps.googleapis.com/maps/api/distancematrix/json?units=imperial&origins=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destinations=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "destination_addresses": [
        "1000 5th Ave, New York, NY 10028, USA"
    ],
    "origin_addresses": [
        "365 5th Ave, New York, NY 10016, USA"
    ],
    "rows": [
        {
            "elements": [
                {
                    "distance": {
                        "text": "3.1 mi",
                        "value": 5021
                    },
                    "duration": {
                        "text": "16 mins",
                        "value": 969
                    },
                    "status": "OK"
                }
            ]
        }
    ],
    "status": "OK"
}
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
