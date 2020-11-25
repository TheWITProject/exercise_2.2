## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=place_id,name,geometry/location&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
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
```
{
    "html_attributions": [],
    "result": {
        "formatted_address": "365 5th Ave, New York, NY 10016, USA",
        "name": "CUNY Graduate Center",
        "place_id": "ChIJRRI8walZwokRCPoUQ0TSCoQ"
    },
    "status": "OK"
}
```
- Can you get some photos of the CUNY Graduate Center?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=place_id,name,photos&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "html_attributions": [],
    "result": {
        "name": "CUNY Graduate Center",
        "photos": [
            {
                "height": 3258,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102171454142994281799\">Sebastian Förste</a>"
                ],
                "photo_reference": "ATtYBwLcQ71fNkgPAJ21U0CTBApX8K1zanmlLK4_L3GSRpT9lAXTLhOudhrQ6dbYg7FScg1RjMo6BJeFa-UMq4HK5p8O3_oTIELLaCF2xi6B1cOy5ZwqnyBGOeqHjZ34IbrnmGBG9tdZ4-L4NO6j-cfNhnOuqsV0_fs2-9bLudhnawbbkYw7",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwKe_PatkqaJ3tD75mVWILYqISHO8dcGuFZaq--yzpMBVfcWPE0oqJ1N6tfBXyCfto-hJGrNoG_bP-Iz7wadiF8A0pmYnKfw7sMtYHo2WUxgF4hgl8ZI7Qc4i3OLho4irCtPtbGWN-BC-JyO_qS5wv155yD3VfuB91qhUcVGGuNi36xt",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwJPxwMNq3SD1OtBnTobllpfHwKIwiYpCIEVcRyLGy5Mw_pI-Br-UusjsbeD3yznKP_hvccMZ78WZzxVquNZ5o4fAY95lWd8zSATtYdMbcck840KNky2u0sSVjxb8b0e_vg4j46oxNT-U5h7itI28p1HonLBAC1pQc3WY0OIxzuYPhAv",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwLyulA2yejly2umptePWgtZc1ZXT9HqMXbyEJv9MfivxKfAwg2g9HPPjheakU1RpnCSTWiROan-hZWFKTxCwMzyaF0ZzNEbzaO-MCMvKVgfzpNObmPiJAK7HE2nBjo-VQLKEd7ZJQOs-ZOj5F3Ql-fLgvpvxiwJrGtp2_wXypFJTOJk",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwILhtzonctOpy1S00937LB4VEahTPuZ9wM9PPsd7_BBtv-Yy8X30QSwZOgAMrKB1bmSTHnCGFQiRwBJiQZtg9E3qksv21LPrixen98PlImJiNCbRD2wTtBeFG5jAtvHMBWc8g3LK2FfqkZ1ymleI6mNV8CzRY-Q1-SdBDa6J6pOcOYF",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwIsjrc_kkBu9ZhebnlcNmMOrtdDfiGhD7Hzq41aTC-YCJcBSxCAYmIrzdnEX6Lonc4XC1N0j6PiGEk4AfUOnkv3jKtH_REg_j0EjNVW1mVqSe036azS94lWP6NN5BIzhAjpLkR9S00TZcGQQ2874cLvJE4D2J4w55LmLD3MvyEhUqOM",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwLpNc2Q6psYad-bCTXb14LupYWIxxsnXuAhhY-osdqkvwTUVusnAIXVByvgE-hZb3SfF3gd7r5Hc_alZ6sRCamCIhKXvfj4jZppvPa3kWf-roYJFgqMxYOXuiPj2Y3gFgLfbC71l-v8KXp6-Z5E1HPCX-Er-UqEOj6wpB-iuNA2zkJ_",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwI8rXgmr8mOW3nnXUJHfyMlrntovYoH2Y0BJuug8gWmjELUzzyMCsxjWhLG0Axy--hlk2MtRTTLDXbzOtXwCupKt1dc-dd8iVaNm8_u1fTxDoSQsnM-a5Gvn6hp4aNGthp2QhqW0rs73B9It5r7B4JrVUn73q2U23xJHMdeY7gURmeY",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwLLKI20JJ0Zab4QwrOMDjfYMQLKZoO-Co8sFq7s_Ds-Y_YVoaCRa2vyCW1dOsSg80AS617fHoQKT-SRkqOMbbdBE8qefwQNHWn-f3XaL3YBVwFX1rlmtISCg7hH2iWH1Bc6n0MxCr3gYvvIeKO921KTHa-SfFyszEHRYMxBzWQPT2XA",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwISwmYnD8RPCwtBjdlgs7xBM38BPPjANQiNKiyTeLL1d6crPSAaRw8yT7yY7_DeDDC4S2AAokYY42Tmi8kByXfAozDbLU02BYy0tnDhL7vzH_aOt8VNKGtsnFYqNKlqUtzatmih-P1elW49hTpwfHMWxeKTXD3F-88R7PHS1opLlPqV",
                "width": 3872
            }
        ],
        "place_id": "ChIJRRI8walZwokRCPoUQ0TSCoQ"
    },
    "status": "OK"
}
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
                    "photo_reference": "ATtYBwJRqgPgMZSx9RbZ7Y7WIaOpDH89JGHgp2COdhyUsXl7Ip1wyMyC-dfKi_31o6CaR_at-G4U24pFfIf_fozXe05Cf7rzrHrOI9w18San3NnE91lbBleJ0raARFLx5jpOki5qqc6oudEa-6fnXe25fkmUFz7zQQpwkLzRzwj1zBBhV9MA",
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
                    "photo_reference": "ATtYBwKlQ32z1M5Spz19grzwIRijrv_3deRxUifKhYAwMF55YaGMZUkN43OYcEkaTtpgMwFtZ17XISI02WjRbFKmGvyKdjDat757p4hD6byqtb3vRMACZXq5hJc0ZTgufsRcjg5aDuHHWM50_nb71422zFiJm_biUUtd4NREiJpgtMWXNbfC",
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
                    "photo_reference": "ATtYBwICEQmam2BrOQ2dsSuhiQ-LGwF78Faih7LdCXAGLGDnQIm46bYuOfpuCDd6Ox5AL80Xyn3PMtEJU31JTNU577ygcqpRMCvT9xUO5n2tnMF8b9Fo24k0enAqJiV5gL-58n6nBFPIhWrmOhuVt44IzJfHYwBs2uzMF7XuffqSNgYpLfvu",
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
```
```
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
