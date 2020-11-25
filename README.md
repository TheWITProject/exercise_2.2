## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,formatted_address,formatted_phone_number,opening_hours,type,rating&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8&query=Metropolitan Museum of Art
```
```
{
    "html_attributions": [],
    "result": {
        "formatted_address": "1000 5th Ave, New York, NY 10028, USA",
        "formatted_phone_number": "(212) 535-7710",
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
        "rating": 4.8,
        "types": [
            "art_gallery",
            "tourist_attraction",
            "museum",
            "point_of_interest",
            "establishment"
        ]
    },
    "status": "OK"
}
```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=opening_hours&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8&query=Metropolitan Museum of Art
```
```
{
    "html_attributions": [],
    "result": {
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
        }
    },
    "status": "OK"
}
```
<br>

- Can you get just the address for the CUNY Graduate Center?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=formatted_address&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8&query=CUNY Graduate Center
```
```
{
    "html_attributions": [],
    "result": {
        "formatted_address": "365 5th Ave, New York, NY 10016, USA"
    },
    "status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=photos&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8&query=CUNY Graduate Center
```
```
{
    "html_attributions": [],
    "result": {
        "photos": [
            {
                "height": 3258,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102171454142994281799\">Sebastian Förste</a>"
                ],
                "photo_reference": "ATtYBwJ2Z0GmM9Yie8tnMTEkEOFTM2EUDh9xVgQJOGHkhzXW9zY1JTS2HqZIudKtc9ALGZKIdojWKbMLZfZPzsyb1mwAyTr0jPI19bJiZOidrWTdwE_LVYeQTa9bV4YVqsE3uh36mWf-Y5BI5L8FL7e-jKgICu1Q36lF8YC0fA50AMSBe99j",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwL4_meyN70itTWZqbgMx2oZSKV340mr4v2lWUq-cPdhcRgmJ08wlH7vcS10hakWKkrUUV-6bWab3XjHLyrfWNjGbSHWTiBLkEr8zhs4Ai1HMc2QvTifkYGInS7YYbVho6UKk9m0YUiENW0ldNSg26DiX9o_hVyMG8nWv8cjt1kcgfI2",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwJfXQLwVrX3ZlLBRRjTa8D1s5-mMYJozfEmJUCHig1BRG2EeLlLVCBrVG9100-ulFEfEZ56NRIB4B7LkGrjGlTflugc9aj78AJ1NzpwWpNUODLawBp-H8tr5kw4b2CN9-W-EvcwM8rNQywSNHMJKhEC6O4KM6wVGfLgO32DmNC8Q0t1",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwLaHolI-Nw1eh_JOV6_sKGlcECiepIQrLzPBIalbiyxJ9mgUftqoEbX_oPK0cE9Kzz84VLStaGhXf03HuVECkntgzGkj4AtyMENHFMnzdIk0rgXNeFK2HTyQWXxHzcZCuFzRFKIa_A8RkihEuc4TtF5GUqVBLw0LQkezRADIjqVc_KJ",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwKurnMHND1FgTxNoiFrnKcc6d2afgEAIDSXsGmnmAmY5GDXxG_IuIs1wFJbPfijN0bRI_kDtg0kTov_Xyw4srse17ICksYICpbBrG8JJfc2AYctyGifDppxmAPk1X0PbSmPkhGmISk6RzeSrIbFo8SgeuZN7Nsns45uInxeezsxWHJY",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwIrT951iyxBaczDiB_wiewFwPZz1k07D7sAtKb_-psO9Bt6Mt2ThI4r6ga-xL-DQ_hijzL5DcwAJcP6v2yNmGZFrVm6A_JmNgnN7fZBKXxslNqQYUDGhyt5GISiJ79SYLOS5KUtngG8IqyTRgf9q_5rfwIq8hhAVB4nkKCDR2TTNbU5",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwL8y4hPdQ6PihCImZQFIL3qf-ZPdQf_H2Nd7ncFWCYZFrAMAT90QCIWPPoMwBHXriw63XUvsdphQqTs5DnYxLcHLosdQtyBkj938kFVmu1nbh_M6rMOaUwsTQ-jmSfjWftWwiCATcLS7Bh2bBYX_Kzj84Ph07A-9x74f2IwQuRAwOVz",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwIW8vusGye_kUku4k2SM-HmMTTDIdEghuguXoL089YThIc87FxAizAtBOErw4ZEdq6svpTZoRVdyuNHf9uEWkxdhDU7xLFINMWQ4rMSc0wA6YjOIqLFVmJUDSnuVAuFHhhfeWtdR3iGmJdnEqzm_F_FEWbQJry9C5Iknl-YUsUMWV94",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwLLEhN3j1SnjiD0gKACtVRRvyBr5QltbjLz_oOeli5eNPDFtMCvvsuANGgG5DoPzuFcWycgdl-WEI2vTYY4_ZLSJWTZOEBDQyv6KwqZwgjmCijrqgOdNDrysy2mfmQCgMfV6gDQy7gLyKmWmTebnN1PMxGL5AF8UwYGJm7Ap5LQNr5E",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwITIqtTNpO7kIaOMe9FPToTmQs7ZNRIdlctNd0bB492mDBqPznpZq4kB8rKGAD5RKhm4ekyqW2Cv0UOVpRdjGGpvdDjHN8ekTALBewIs0L7OzUz1-r_8qm_phwzVgZL7OO0zqCn3-7MLc4ZWLF4v9RffmDU9BVOF48sQudcZxWMoo73",
                "width": 3872
            }
        ]
    },
    "status": "OK"
}
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
https://maps.googleapis.com/maps/api/directions/json?origin=CUNY Graduate Center&destination=Metropolitan Museum of Art&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8
```
```
{
    "geocoded_waypoints": [
        {
            "geocoder_status": "OK",
            "place_id": "ChIJRRI8walZwokRCPoUQ0TSCoQ",
            "types": [
                "establishment",
                "food",
                "point_of_interest",
                "university"
            ]
        },
        {
            "geocoder_status": "OK",
            "place_id": "ChIJb8Jg9pZYwokR-qHGtvSkLzs",
            "types": [
                "art_gallery",
                "establishment",
                "museum",
                "point_of_interest",
                "tourist_attraction"
            ]
        }
    ],
    "routes": [
        {
            "bounds": {
                "northeast": {
                    "lat": 40.7795899,
                    "lng": -73.9602326
                },
                "southwest": {
                    "lat": 40.7452406,
                    "lng": -73.98641069999999
                }
            },
            "copyrights": "Map data ©2020 Google",
            "legs": [
                {
                    "distance": {
                        "text": "3.1 mi",
                        "value": 5022
                    },
                    "duration": {
                        "text": "16 mins",
                        "value": 969
                    },
                    "end_address": "1000 5th Ave, New York, NY 10028, USA",
                    "end_location": {
                        "lat": 40.7790691,
                        "lng": -73.9622212
                    },
                    "start_address": "365 5th Ave, New York, NY 10016, USA",
                    "start_location": {
                        "lat": 40.7488025,
                        "lng": -73.9843068
                    },
                    "steps": [
                        {
                            "distance": {
                                "text": "0.2 mi",
                                "value": 367
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 70
                            },
                            "end_location": {
                                "lat": 40.7459153,
                                "lng": -73.98641069999999
                            },
                            "html_instructions": "Head <b>southwest</b> on <b>5th Ave</b> toward <b>E 34th St</b><div style=\"font-size:0.9em\">Pass by Reinlieb Laurence (on the right)</div>",
                            "polyline": {
                                "points": "_wuwF|`qbMDB^V\\VhCbBxBtA\\V|AdALFn@b@|@j@"
                            },
                            "start_location": {
                                "lat": 40.7488025,
                                "lng": -73.9843068
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.1 mi",
                                "value": 156
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 51
                            },
                            "end_location": {
                                "lat": 40.7452406,
                                "lng": -73.9847924
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>E 30th St</b>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "_euwF`nqbMJ[FYRm@~@sC^kA"
                            },
                            "start_location": {
                                "lat": 40.7459153,
                                "lng": -73.98641069999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "2.7 mi",
                                "value": 4276
                            },
                            "duration": {
                                "text": "13 mins",
                                "value": 765
                            },
                            "end_location": {
                                "lat": 40.7788867,
                                "lng": -73.9602326
                            },
                            "html_instructions": "Turn <b>left</b> at the 1st cross street onto <b>Madison Ave</b><div style=\"font-size:0.9em\">Pass by Chase Bank (on the right in 2.4&nbsp;mi)</div>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "w`uwF|cqbMQKiBmA{B{AyBuAiCcB]UeBiAOIi@]a@Y_@Ui@]QM}@k@]Uk@]q@e@UQa@WcAq@_Ao@{@k@s@e@gAs@_@Ug@]]W]W[U]Wm@_@_@U_@U]UA?]W[SWMi@[}@m@_Ak@_Am@aAq@w@k@}@o@_@U]W_Ak@{@o@}@i@a@W_@UcAq@w@m@_@U_Ak@]ScAq@w@m@}ByAc@WGEg@Uk@a@_@U?A{AaAYQo@e@{@o@[Sa@YgAq@}B}AeAs@u@c@OMkBoA_C}AyByA}ByA}B{A}@m@}@m@}B{AGEiBkAIE}B{AIIs@c@}@m@}B{AIEmBoAQKiCcB}ByA_Am@_Ao@}@m@_Am@_C{AqBsAKI}AeAc@YKI_@SwAaAGEIGuBwA_C{AEI_BeASM"
                            },
                            "start_location": {
                                "lat": 40.7452406,
                                "lng": -73.9847924
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.1 mi",
                                "value": 157
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 57
                            },
                            "end_location": {
                                "lat": 40.7795899,
                                "lng": -73.9618385
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>E 83rd St</b>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "as{wFljlbMKP}@pCa@pA_@jA"
                            },
                            "start_location": {
                                "lat": 40.7788867,
                                "lng": -73.9602326
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "217 ft",
                                "value": 66
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 26
                            },
                            "end_location": {
                                "lat": 40.7790691,
                                "lng": -73.9622212
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>5th Ave</b>/<wbr/><b>Museum Mile</b><div style=\"font-size:0.9em\">Destination will be on the right</div>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "mw{wFntlbMFD~AdA"
                            },
                            "start_location": {
                                "lat": 40.7795899,
                                "lng": -73.9618385
                            },
                            "travel_mode": "DRIVING"
                        }
                    ],
                    "traffic_speed_entry": [],
                    "via_waypoint": []
                }
            ],
            "overview_polyline": {
                "points": "_wuwF|`qbMlEvCbGzDlBnARu@rAaE^kAQKeFiDcGyD}DgCwHaFsKgH_CcBkCcByAaAaAi@}ByAwF{D}@m@{B{AcEiCwAcA}A_A{B_BaDqBo@[kAw@eD{BwAcAiBkAiGcEcNaJqRgMyFwDsGeEyRmMmKeHeCeBsBsAKP}@pCaA|CfBjA"
            },
            "summary": "Madison Ave",
            "warnings": [],
            "waypoint_order": []
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get directions from Oakland, CA to Brooklyn, NY?
```
https://maps.googleapis.com/maps/api/directions/json?origin=Oakland, CA&destination=Brooklyn, NY&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8
```
```
{
    "geocoded_waypoints": [
        {
            "geocoder_status": "OK",
            "place_id": "ChIJA-2qKIt9hYARZ5N1NdUVtHE",
            "types": [
                "locality",
                "political"
            ]
        },
        {
            "geocoder_status": "OK",
            "place_id": "ChIJCSF8lBZEwokRhngABHRcdoI",
            "types": [
                "political",
                "sublocality",
                "sublocality_level_1"
            ]
        }
    ],
    "routes": [
        {
            "bounds": {
                "northeast": {
                    "lat": 41.7893352,
                    "lng": -73.9021048
                },
                "southwest": {
                    "lat": 37.8043479,
                    "lng": -122.3171428
                }
            },
            "copyrights": "Map data ©2020 Google, INEGI",
            "legs": [
                {
                    "distance": {
                        "text": "2,916 mi",
                        "value": 4692913
                    },
                    "duration": {
                        "text": "1 day 19 hours",
                        "value": 154240
                    },
                    "end_address": "Brooklyn, NY, USA",
                    "end_location": {
                        "lat": 40.678183,
                        "lng": -73.94416129999999
                    },
                    "start_address": "Oakland, CA, USA",
                    "start_location": {
                        "lat": 37.8043479,
                        "lng": -122.2711543
                    },
                    "steps": [
                        {
                            "distance": {
                                "text": "0.1 mi",
                                "value": 174
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 43
                            },
                            "end_location": {
                                "lat": 37.80295,
                                "lng": -122.2720566
                            },
                            "html_instructions": "Head <b>southwest</b> on <b>Broadway</b> toward <b>14th St</b>",
                            "polyline": {
                                "points": "etveFtahiVDB`Aj@hAn@PHp@`@`Ah@"
                            },
                            "start_location": {
                                "lat": 37.8043479,
                                "lng": -122.2711543
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.4 mi",
                                "value": 584
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 102
                            },
                            "end_location": {
                                "lat": 37.8052878,
                                "lng": -122.2780113
                            },
                            "html_instructions": "Turn <b>right</b> onto <b>12th St</b>",
                            "maneuver": "turn-right",
                            "polyline": {
                                "points": "mkveFjghiVcAhDCLaAbDAFq@zBK^_@pAo@xB}AhFw@rCc@zA"
                            },
                            "start_location": {
                                "lat": 37.80295,
                                "lng": -122.2720566
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.9 mi",
                                "value": 1510
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 68
                            },
                            "end_location": {
                                "lat": 37.8170212,
                                "lng": -122.270106
                            },
                            "html_instructions": "Turn <b>right</b> to merge onto <b>I-980 E</b> toward <b>CA-24 E</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "azveFpliiVGGA@C@A?C?C?IAGAEAGAE?C?C?A?C?E?E@O@E?E@E?Q?SCWGUKMIc@QWMYOA??Ae@SaAg@GCaBw@]QAAm@[sBiA_B}@oAu@i@[[E[Wa@WA?UQECe@]e@_@WSUUm@m@[[Y]e@i@OQQSIIIKCCKMo@u@EGWYACQSAAeAoAOQY]UWw@cAa@e@a@c@[Yc@_@k@a@IGKG]SOIIGECUKIEc@Q]MAAWGMEm@MAAEA]GkB[CAg@Ii@I"
                            },
                            "start_location": {
                                "lat": 37.8052878,
                                "lng": -122.2780113
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "1.6 mi",
                                "value": 2501
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 99
                            },
                            "end_location": {
                                "lat": 37.8267206,
                                "lng": -122.2869164
                            },
                            "html_instructions": "Take the exit onto <b>I-580 W</b> toward <b>San Francisco</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "kcyeFd{giVIMIIKCWEc@GoCm@y@Q{Bg@u@Ua@IiB]kASw@Qy@QW@}@Q_@EMCUEEA]GEA[Ia@I_@ESCg@Cg@Co@F]Dc@HMDKBEBC@UHA@OHC@A?A@MJA?A?MHSPGDMJEDCBIHCBGHA@KNS\\ABGJQ`@Oh@GVAHg@lD?BADEVM|@K|@MlA?@H`@QlAABKv@WdBCP[dCk@jDCNObAe@|Cu@lFCT_@~BIh@_@dCsAzIKh@Gt@EXC\\CZAVATC`@?^AR?J?f@?`@@Z@`@@N@P@X@PBTBXDb@?DDZJl@L~@\\bCHj@F^T`Bj@jC"
                            },
                            "start_location": {
                                "lat": 37.8170212,
                                "lng": -122.270106
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "1.5 mi",
                                "value": 2419
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 93
                            },
                            "end_location": {
                                "lat": 37.8443679,
                                "lng": -122.2977394
                            },
                            "html_instructions": "Take the exit onto <b>I-580 W</b>/<wbr/><b>I-80 E</b> toward <b>Berkeley</b>/<wbr/><b>Sacramento</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "_`{eFfdkiVGXA@?BD^DnAApACv@Eb@Gn@Gh@EVGb@Ij@A@?BG\\?@ABIf@WjAi@|BADABMd@CHCJCJK\\ADELKZ?@Up@GTUf@MTMPMPEDMNGFYZSPKFIFWNUJWJA?WHYFSDE@YBA?W@K@I?S@E?OAYAA?WCC?c@Ca@CQB{@Cg@AY?u@@c@Bq@FE@o@JUDE@]Jo@R]LeCfAu@^a@Rw@^eCrAwGdDA@QXo@Rs@X_@Lg@Nc@JKB_@HSDWB[Dg@DuANwBTsBRM@}BVmBT_@De@D_JnAmCb@_AJ"
                            },
                            "start_location": {
                                "lat": 37.8267206,
                                "lng": -122.2869164
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "25.8 mi",
                                "value": 41575
                            },
                            "duration": {
                                "text": "24 mins",
                                "value": 1433
                            },
                            "end_location": {
                                "lat": 38.1673182,
                                "lng": -122.2028576
                            },
                            "html_instructions": "Keep <b>left</b> to continue on <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "in~eFzgmiVsBVmIjAkBXA?]Fa@FoDh@cBVSBA?_IjAcEl@qB\\g@F]HkGhAyGlAgKlBeAPsh@pJw@PODyI`By@PUDKBOBcARkGnAmFhAkCj@wA\\_L|BiJnBw@NcB`@aB^}Bf@{Bd@wBd@mARC@sAToHbAqAPo@HsDb@yDh@w@Ji@LUDa@FuEl@iBVcAL}BTqAJG@c@BQ@gA?}@AYA_@CEA_@C[CA?{@OwA[sAa@a@OuGkCo@Su@Ug@Me@Ik@G[Ek@C{@A_@?u@Bs@Dc@DUDUBMBMDyA^gBj@iA\\{Ab@sA`@wAb@mA\\_Bf@{Bp@w@T{@Xk@Pi@Po@TQHa@Nm@Vs@Zo@Zk@Zg@VC@[N?@g@XA?aAn@QJiAp@s@b@MHoBjAo@`@gDtBaAl@k@XoAv@w@d@_@TaDnBoBlAID_@VoBjAu@`@_Al@_B~@qBjAk@^m@\\k@Zo@ZIBe@Rm@To@Re@LQB[HA?g@H}@Hq@Bi@Bi@?wC?e@?}B?_BAyDB}B?_H?e@?cA?oBA_DBy@BeAHeBTcARo@Nk@NiAb@m@XeAh@iAp@o@\\_CtA_B|@qAt@kC|AiAl@eAp@]RA@uErCsBrA_Al@oCjBaAp@aBfAkAx@uDdCeBfAm@b@e@^WLA?o@b@MJ[To@^uAz@IFGDgCxASHKDWH]LA?SFMBc@Ha@FG@c@Be@B}@@Y?OASAUC]EaAQg@M]Kg@QcAa@}Ao@A?AAiAe@}Ao@wCoAkHyCa@QgCaA_Ba@o@Km@I[AWAYAs@A]@G?o@BQ@YB_@Dq@JaAToDlAiI|CsI~CYLsNpF_A\\cDnAaCz@k@VsFlC}BhAkCpAgB|@c@Ro@Vo@Rk@N[Hq@Ly@Jk@Fm@B[By@?C?q@Aw@E}@IMAc@GkASQE[Iq@Wm@Wm@YcAm@m@c@{@q@g@g@s@y@WYc@o@q@gAMSc@y@[s@cB}DeAeCIQ}@uBi@mA]w@q@_B[u@i@iAMSKS_@q@s@cAq@w@]]_Aw@g@[u@e@_Ae@s@W]Kc@M]IeB_@eBc@OEeEcAiHcBEC_Ci@}G_BsD}@uCq@aBa@_Dq@EAkCi@OEiCq@C?aBa@m@QEA}Cs@GAkCo@kEcAmDy@uD}@iD{@sAa@wAg@m@WWKo@[eAk@{@g@aAi@y@g@uA{@w@k@i@c@k@e@c@a@EEUUQQg@i@g@i@e@k@e@k@a@k@e@o@a@m@c@q@AC_@m@aAeB_@s@_@u@Q]KWYs@g@gAYw@Yw@Wy@Y}@Uw@U}@Oi@i@gCY{AO}@M{@S_BUqBOmAKwAUwD]gEEm@IoAWgDC_@AKASMcBQeCCOa@wFIcAa@qGYoDGy@[qEEm@WqDOcBW_COaAOcAc@wB_@{A]mA?Cq@kBEIm@{A}@iBc@u@c@s@c@q@c@i@e@k@SWi@m@g@i@_@a@aB{Ac@a@][eGoFwCmCuBsBsCcCc@a@oAiA_A}@s@m@aCyBqCgCmAgAsEcEeEuDmF}EqCeCaDyCi@e@iAeAcCuBa@a@iAcA]YsBiBgFyE]Yy@u@[[oAiAkHuGeF{EaA}@_B{AiBaB}@w@_@]s@o@cFoEyDmD{BsBwAqA][_@]gAaAKK]YwAqAMMiIqHw@s@WUeD{C_ByA]Yy@u@cFqEcD{CeB{AmF}EoAkA][cC}BYU{AsAQQaEuDg@a@g@_@_N_MwAoA}@y@m@i@c@c@CCe@e@Y[c@g@w@eA[c@_@q@_@s@wHyLoFsIoDwFwBiDWa@qBaDEGWa@Wa@QY]i@U_@AAc@s@k@}@g@w@U_@kCgE}BqDWa@Ua@{DiGgAeB_BeCqHsLyA}Bo@cA[e@g@w@mByC{@wAWc@IM_A_B_A_BAAWg@Yg@KOa@m@Ya@KMo@o@SOUSg@YCC[OAAMGQGSIa@Mk@MYEOCc@Ae@AmCFa@@c@@c@BwLd@_EPsBFqAD_DLwEPa@BA?gADgADgADkBHgALWBK@c@Da@DA?c@DG?YBA?cAFO@E@a@De@HG@C@q@L_@JE@g@Li@P]LKDSHQHo@TSHwAj@IDWJa@P_@Nc@PoAj@c@PWNQJYPQLKFWNa@VEBk@d@eBrAC@cClBgBtAcBhAq@d@}@n@yAbAgBnAg@\\m@\\WPe@Xe@Vq@ZIBcA^eA^{@ZQFGBWFq@R_@LC?_@HA@g@JsB`@UFaALC@]DM@a@FWBWBK@a@De@B]BC?_AFW@S?U@M@U?g@@I?{A?g@?i@Ac@AE?O?o@EkAGg@Cc@E}@Is@Iu@Kk@IWGiAUCA}Cq@E?QGQGICEAe@Mk@Oi@S{@Y}@[C?q@SeBm@KCeBm@ME{@YYIoBo@oAa@g@Mg@Oy@Q_ASg@KkASa@Gm@Ik@GMA]ACAkAIgAIo@EkAIm@COAo@Cs@Eo@AmACE?]?i@AcA?g@?mBAq@Ao@?qA?mBAw@?c@?C?qCAeA?wAAM?{@AaGCkA?mAAyAAgFAk@?Y?U?wBAA?k@?gEAoDAoBA_@?g@?c@Aa@?m@?mA?o@?_@?[@e@@Q?G?[@I?Y@Y@I?k@B[@g@By@BcADW@{ADm@BG@mHVU?qADi@@u@DS@O?wAD{AFc@@c@BaBDaEP}AD{@Dw@Be@@[@O?i@?_@Aa@Ay@Ae@Ca@AEAc@CWAu@IkAMq@KgASq@OWG_@K_@MUGc@Mc@O_@Oi@U_@Oo@Yc@U_Ae@aAo@GC_Ag@u@a@aCmAUKaCsAGC{DyB{DyB_@SSMeDkBcCsAcB_Aq@_@{DwBmAq@mDmBeCsA_@SoCwAq@]kBeAc@WSK_@Qe@_@eCuAe@YyBoAc@Uc@UoBiA{Aw@eAm@cAi@_@SoAw@q@_@[Qk@YgAi@UOq@Y[O{Ak@EAcA[kA[eB]kAS}AQSCy@IWEKCk@A{ACmA?gBDeCHcBFkBBaAAQ?gCMg@C]CGAyAOu@M]GQEQE_@IiBg@QGsAe@ICu@[q@[q@]QKq@_@y@i@u@e@g@[{BwAk@]oD}Bq@c@iEmC_@UaAo@[S{ByA_@U}BwAoAy@m@_@{A_AAAgCaBoBoAeAw@g@c@i@e@[[MMSUQQYYkBaCACc@o@S[_@k@a@s@S_@eAiBUc@eAiBUa@eAiBUc@mAsByBuDKO"
                            },
                            "start_location": {
                                "lat": 37.8443679,
                                "lng": -122.2977394
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "34.2 mi",
                                "value": 55000
                            },
                            "duration": {
                                "text": "30 mins",
                                "value": 1790
                            },
                            "end_location": {
                                "lat": 38.5144105,
                                "lng": -121.7757764
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "wp}gFzvzhVm@iAmCiE}AeC_BmCWa@qAuBgBwCgAgBiAiBo@eA[e@u@oAcAgBCGsAwBs@iAeAcBmAeB_BiBg@i@qAoAAAeG}ECE]WIG_Au@wAiA_Aw@i@g@WUg@g@}@_Ae@i@y@eAW[MQgAaBcAcBo@mAo@oAm@oAoAeC_@s@AAS_@KS_@m@c@s@e@q@AAYa@EGU[QUg@m@SU{@_AqAuAmAqAWWCEa@c@SWSWEEY_@Y]u@eAU]KSIMYc@a@s@k@mA[s@uAmDc@yAQm@CGa@cBe@qB}AkJCOIk@Ow@Ie@G[Q{@Kc@Sy@GU[gAe@{Aq@iBISgAeC_AoBw@uAe@u@QYc@o@w@eAQU{@eA_AaA[[GGwAqAs@k@]Y[Wi@c@USYU]YeA{@cA{@cBuAyBgBaCqBaAu@}BwBcBkBwAeBIKQQwEyFoDkEwAcByDsEkDcE]a@[]Y_@Y]_@c@q@w@m@s@aCyC_AgAY]q@w@}@cAeAqAoCcDkDeEqCeDmBaCkAuAY]GIsBcCo@w@g@o@o@{@[c@KOe@s@?Ae@u@GKWa@Wc@SYmAsBaA_BYc@{E}H}CaF{JeP}DsGWa@yBqDk@}@Wa@yC_FwA}Bg@y@yC}EyA_COU]o@mAoBcHiLaCuDwCuEYe@aBqCo@mAWe@]s@gB_DEMWg@m@kAOWk@mAsAoCmB_Ea@y@wB_Fm@sAq@eBsEiLSi@k@wA_AuCIWwAoEg@yAy@cCiAmDyBwGuBmGGOQo@uCuIyAkEoB}FcEkMqAaEkAuDQk@}@oCYy@mAqDm@gBeBcFu@eCcEyLo@mBu@sBaCiHKWqFkPEKuAeE[{@uBoGa@oAy@aCqA}DqEaNeBgFSm@uBeGu@_CUq@_@iAe@yA}@mC{@iCg@wA]gAGUe@yA[cAWy@g@oBe@wBYwAc@aCKo@Ko@O_AY}AOy@UcAWw@c@sAo@}AGMg@aA[m@oAoBg@m@W]sAyAIIcA_AIGk@e@UQWSs@m@aAw@_@[iCuBmB}Ay@s@SO_Au@YWsAgAi@c@UScDkCaEaDaHuF_EcD_@[_@YcLcJuC{BaBsAeIsG[W[WmGeF[W{JaI_DgCoAcAiDoC]YmFiEmGcF{@q@]Y]WsDwCuC_C]W]YyAkA]WSQqAgAeIqG]Y]Y]Y{@q@]YwBcB]YmGeFqDwCeG}EuBeBiCuBuBcB]YyAkA]Y]WOMMKiByAaEcD{CcCsAgAwAiA_@[uBeBECaCkBOK]UA?k@_@WOm@]o@[YMe@Qa@MWIYIYIWGYIYGs@KYEWC[CGASAOAa@CYAI?O?SAI?aBAE?_CCyCA[A{MIo@?gIC{HIyC?_CAw@?c@?c@?mHCw@?}BCa@Aq@AE?o@Cc@A{@Ei@CaAGqAK]COC]CoAMaBOeBQQCqAKcAKwGm@y@Gu@Kk@KSE]Gq@Mw@Sm@OWIWIYKo@Uc@QMGSIk@Us@a@WMWOSMYQSMUOUQi@c@uAiAACaBuAaA{@_Ay@yHyGwDeDk@e@[YmC_Ca@]qAeAkA{@k@]w@g@yA_AsBkAk@[q@_@YOSMcAk@EAqAu@yBkAkBeA}A{@CAwBmAe@W_B{@k@]sBkA[Q{DuBsKcGkDmBkJgF{Ay@_Ag@k@[i@Yo@]m@_@WOWOUOWQUOUOUSk@a@WSc@_@YUk@i@QQUWg@g@[]a@e@SWm@u@m@}@QUc@q@a@o@Q[OYWe@GM_@w@MYO[]u@M]CGe@mAWu@]eA_@qA_@yAS}@Q{@[_Bm@yCc@_CY{AGa@a@uBa@wBEOUiA[uAACMg@CMK_@Qq@Me@Uy@_@sAOg@_BsFYcA{@yCqCwJ{@yCU{@K]iA}DuAwEkBmG{@{C{@_DkA_EcAkDYgAe@eBSo@[iA]mAgA{Dy@qCkAeEYcA[cAOg@Uw@i@kB}@}CQk@eAsDe@_BIUY{@Qe@GS[w@Ug@GM]u@a@u@[k@We@a@k@c@o@OSW]OSs@{@AAeBmB[[{DgEUW}AaBe@i@WWACqAwAu@w@iBuBQSe@i@c@o@cA{Aq@gA{@_BmA}ByBiEw@yAUg@e@w@yBgEsCuF?Ak@eA{AsCkAeCa@q@i@cAmAyBiAmBo@cAg@u@aDsEeCoD_AuAY_@AAwDoFcCoDs@_A_CgDIIqAgB{AuBw@gAQUoAcB}AmBkAyAy@cAkA{Aw@gAGIeA_ByB{C{@mA}@oAeBaCcAyAOWkA_BgA_BoBmCg@s@MS{AwBoBoCy@kAa@i@mBoCqAiBs@aAOUsCcEgA_BiA_BkBoCw@iAW_@gBgCeA_BA?W_@Wa@Y_@u@gAyAwB{AwBs@aA_B{B{AuBU[eAyAw@gAmAaBOSIKqAiBiA}Aw@kAgBeC{HuK_B{BoBoCqJwMoCuD{BgD_AmAoBiCi@s@yQeWcDsEmHcKSUiAaBiGoIeD_FGIgCoDgBiCyAwBgPsUYa@gEeG}BeDq@aAuB{CkBkCW_@uCeEYa@W_@wHqKu@kAaMuQ_LaPmBmCyAoB}Ty[Ya@oKmOiLoPmJaNqL}PcWw^cRaXcAwA{AwBaE}FaCgDqG_JY_@EG}CeEa@m@_MaQoCyDACe@q@a@k@KO}AwBeDqEs@cAaE{FwEqGiEaGyAuBoCuDaDoEiDyEcFcH{CiEyDkFa@i@{AyBwIuLeCqDmAcBcAuAkEkGY_@{FeIyC_EW_@qDaFuBuCKOIOoDcFeBcCwAqB_RmWW_@Ya@{EuGa@k@uFaIkBgCY_@mAeB}AuByByCiAyAgFiH}AuByDmFiA{AACeBaC_GaIY_@qHcKYa@}FaIeFcHkEaGgFaHs@cA_BwB_ByB{@kAMSu@cAmAcBW]q@}@aAwAe@o@wBqCKMk@o@{@cA{@_A_AeAoQ{R[][[[]Y][][[u@{@[[iCsCu@y@qAyAIIcBkBaBgBuAaBgEwEeBiBY]aEkEkEyEaCoCqC{Cw@{@a@c@_DmDSUgDsD_AcAoFcGmJiKkFyFo@q@W[sD_EmAsAmE{EcHwH"
                            },
                            "start_location": {
                                "lat": 38.1673182,
                                "lng": -122.2028576
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "12.1 mi",
                                "value": 19439
                            },
                            "duration": {
                                "text": "11 mins",
                                "value": 639
                            },
                            "end_location": {
                                "lat": 38.5749407,
                                "lng": -121.5723105
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to stay on <b>I-80 E</b>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "ajajFrigfVSMmKiL[]gCsCMMcAkAeAiAqA{A}@aA_EkE[]oCyCUU[]Y[e@g@mF_GiEsEeCuCqAcBEG{AyBkAgBeAgBCEkAuB_AmBu@}Ai@mASe@]w@o@aBM_@CGQg@k@_Bq@wBYcAe@oBWaAw@sD_@_BY_B]sBMw@o@wES_BYaC]{CMiAQoAg@kDOeA]mBa@iBg@iBu@mCOe@qAsDqA_DaAuBWo@uAaCmAuB]i@cCkDMOY]gEkF{@eAuCmD{AiBqBgCq@{@a@e@wBqCuDyEuBoC}EeGiEoF{ByCU]qAwBaAgBkAyBCGg@kAg@oAs@kBm@gBcAiD{@oD_@kB_@mBa@kCOgA{BkPE_@oBgNmGyc@uAyJqDqWqDwWgAmIu@kFe@kDQ{AOeAYkCAEQqBOmCUmDK_B]uDKeAIu@OcAMu@a@sBWmAa@iB]yAq@yCw@eD[aBI]]oB_@kCIm@_Hag@yFqa@[cCkAyI{CkU[cD]gECa@cBwTOsBcBgUs@oJm@mIiAuO_@gESwBOqAGk@m@iGOsAAEiA}Ka@{D]gDKiAuBkTW_CYmCYgCWgC[oCYqCU{Bm@gGCMAMEc@mCyW{BkT}Dg`@QcBaBcPUsBGm@Gk@Gk@aAqJ]gDAQEYAQm@{FkAeLmHus@Gk@oDy]WgCGk@_@sD_Es`@WeC_AgJGk@wCsY_AcJQgBmAsMGk@AGEe@c@oFQwBEk@EaAI_AEc@CQSeCAOe@uFOsB{@uK"
                            },
                            "start_location": {
                                "lat": 38.5144105,
                                "lng": -121.7757764
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.7 mi",
                                "value": 1174
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 41
                            },
                            "end_location": {
                                "lat": 38.5787205,
                                "lng": -121.5609626
                            },
                            "html_instructions": "Take the <b>I-80</b> exit toward <b>Reno</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "kdmjF|q_eVD]BYEw@GsAG_AIqAEsAAo@?E?U?e@FsC@U@m@HgC?o@@aAAsA?WEo@IqAGq@AIMy@QiAMk@Kc@]qAIUGSAA[w@Wi@]s@m@_AUa@g@o@UWGI]_@k@e@c@_@_@WkDsBg@]EAMIIEAAGE"
                            },
                            "start_location": {
                                "lat": 38.5749407,
                                "lng": -121.5723105
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "11.8 mi",
                                "value": 18977
                            },
                            "duration": {
                                "text": "11 mins",
                                "value": 636
                            },
                            "end_location": {
                                "lat": 38.6447049,
                                "lng": -121.3845307
                            },
                            "html_instructions": "Continue onto <b>I-80 E</b>",
                            "polyline": {
                                "points": "_|mjF~j}dVwOqJcCuAm@]kEiC_@U}@i@YQy@e@aAm@cAm@g@YGEKGsBmA]SaNcIw@g@cAm@_Ak@]U_B_A_B_A_@UcBcAeDoBKGYQe@YeAk@w@g@y@g@o@_@cDoBsBmA_FwC_@U_EaCGEIESM_@UYOeDqBUOSKm@]sBkAUMe@YEEi@]sGwDsAw@gAm@mAu@OIQK]QAA_@SQKw@c@sAw@s@c@wBoA_Ai@CC[Q]SgAq@WQqAu@iC}AAA_Ai@kAs@c@W{@c@]Us@a@eBcAqAw@yA{@uAw@qCcBeBcA{@e@eC{Aa@Y_As@_Aw@}@y@?A][_@a@}@_AQUg@m@aAqAm@_AYa@MWMSUa@Ua@We@Ui@Ue@EISe@]y@{AoDeBeEIQMY_@{@k@sAAEKUO]m@uAkAmCw@iBQc@k@qAe@gAGQsB{Ek@oAUi@Se@M]EGmAuC_@}@]w@e@cAKWKSaAwBm@wAoEkKWm@AEQ_@Se@KWc@aAyAkDk@qAAA?AYq@_@{@Wm@Qc@Yo@?AO]AAQe@AAMYCGACUg@{AmDkAuCi@kAGMMWk@qAe@eAEMYm@]y@Qa@q@cB_EkJeFuLSe@oFgMgCaGeFqLSe@oFiMeAcCoAyCoAwCiBgEsB{EkBkECIuB_FKW[s@AC]}@[u@Oc@GQK]o@qBYaAUy@_@}AI_@Ka@Kk@GSQcAMs@QcAM}@My@MaAEc@OqAQqBC][gFGaAWcEk@qJmAgSEm@UuDMiBQwCG{@UcDMwB]oFEu@Eu@UuDCm@AEKgBMgBCe@OiC?GKqCCe@Am@E_C?QAiC?E@cA@aCDiD?UBuB@k@?UB{A@{A?Q@EHaI@y@JuF?W@kA@_@@w@@{@?E@m@@s@BoA@mA@aA@s@@aARmR@m@@{ADmCH}GAuD?yA?iAAw@CcAAe@C{@AW?U?GAMAM?MAG?GASAK?Q?IAC?EASEq@IkAG}@C[CW_@cEIu@CQGUo@mHYsCYoCEc@?AAISgCm@mGOyAEa@Ek@AKOcBSuBOaBGu@Cc@CYI}AEqACs@AYA{@As@@{BAwB@c@@q@B}A@m@@U@WDy@Be@Du@HmA@OHs@Fy@J_ARyANmARmAHc@ZkBTmALg@`@gBPs@`@sAb@sAN]|@gCbBoEpCgHhBqETk@Pg@x@uBv@sBHSX{@Rm@\\kANg@Lk@HWDQLo@He@Jk@DUHc@Fc@Hc@@EBY\\}CL_BJqBF{ABwB?W?_@?oA?aA?eA?}@?aA?Y?KAc@?I?_A?aA?G?m@?K?U?M?a@?eAAaA?aA?eA?}@?C?i@?W?_A?O?AAq@@mC?aC?K?uB?K?a@?KCyAAo@Cs@C]Ig@Io@K{@Ko@Kq@Mg@Oi@i@iBcA_Cw@wAi@w@aAyAaAwAaCwDCEAA?AAAiByCkBuCm@cAYc@{@{AS_@kAiCo@}A_@aAu@eCIWg@oBk@kCKk@YcB]mCWqCi@kIKwAU_DcAsN"
                            },
                            "start_location": {
                                "lat": 38.5787205,
                                "lng": -121.5609626
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "621 mi",
                                "value": 999579
                            },
                            "duration": {
                                "text": "8 hours 51 mins",
                                "value": 31859
                            },
                            "end_location": {
                                "lat": 40.7204651,
                                "lng": -112.2304589
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Passing through Nevada</div><div style=\"font-size:0.9em\">Entering Utah</div>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "kxzjFh|zcVa@aFE_@C]?EKcAQyBGq@WoCEk@[sDQ{AE[AOIk@U{AUqAScAq@yCOk@Oc@Oc@Wo@O]KWQ_@M[g@eAWg@QWUc@GKU]?A}A{BsA}AY]IIwDcEKKmD_E{CiDcAiA}DkEqBwBaEsEWYiCuCIKk@o@[]{CkDgF_G{DgEkToVeCmCeO{OmFeGuCcDcH_I_EqEu@y@[]kBwB}OmQ{AcBoF}F_@c@UWmBwB[]Y[GGwHuImD}Du@{@[]Y]w@{@Y]aDoDsDeEKKeAmA[]wHuIwA{A{CiDcDqD[]]_@iB{BoAwA[[qAyAgHcIaBiBa@c@aCoC_JyJgDwDoC_DSSqEgFcDsDk@o@_BgBiRiT{BgCgCwCq@s@sDcEoAuA{BeCaGwG}EqFcDsDs@w@mByB[]yFoGY]w@{@aBkBsD_EiD}DaCmCY]}JcL[]sA{As@y@eDqDcJcKeAkAmD{DmEcF_@a@u@}@aBmBcAiAyBkCwCmDoAyAyE{F[]Y_@s@y@mB{B}AgBeAiAWYAC}CkD_BgBuFeGeBoBgGaHgBkB?AkBuBmHiIgCuC[]aPuQ_HyHsDcEq@w@gCqCgH_IcAcAkAeACAYU][iA{@i@a@cAq@{A{@wGuD[Q_Ae@AAQKkAq@gKaGWO_@SqC_BmAs@uNeImGmDECc@U{CiBoGmD}HqEm@[WOeAm@{IaFsBiAaDkBsDyBoDqBqBmAkC{AsBkAcAm@w@i@_Au@_@a@o@o@o@w@{@mAu@mAe@}@a@w@y@{AoA_CMWgAsBuAkCuEwIiC{EkDmGoAaCs@uAcAkBk@gAaDcGsBwDmEgIy@_BaDaGQ[aAkBwGaM}AqCo@kA]o@q@mAoA_Cg@_AqCgFUc@GK{AcC_B}BEGaBwBgFqGmOoRcAsAuAiBc@k@mB_C}@iAsBiC}CyDuBkC_AmAe@k@e@k@eC_D}C{DaCyCQUeAoAaAkAsE}FUWEE{AoByCuDyEaGkA{AqHkJsBiC_EeFeAqAaAmAyAiBwD{EaC{CsBiC_DaEaBqBaCyC_EaFsCoDuBmCkFwGcEiF_EaFy@cAcFoGk@u@wCsDsE}F_BoBqP}SeDcEa@k@wAkBeEeFW]QSyBqCyEcGYa@iB{BAA}BwCuIuKiGyHsLiO{EeGwKeNyGoIoA}AW]iB}BqBgCaAmAY]iAwAq@{@sA_BmDmE}C}Dq@{@oA}Am@u@oA_BuAeBMQaAmAgAuA{@eAg@o@yAqBsBkCGIoAaBOQmA_BuBmCaAoAiA{A]c@_AkAg@s@CEs@{@iCgDi@q@cAsA}@iAm@y@o@w@}AqBsBkCqCqDk@u@{@iAgB}BaC_D_AmAuGmIY]}@mAa@e@yEiGgB}BiGcIcBwBW[cEoFcH_JwCyDiGcIqDwEkDqEcCyCsAuA[Ys@k@aAu@}A_AeAk@_Bq@cBk@eBc@kASgBUmAKgBQmAMkAKgBQmAK}CWyCYqAMcDYyJ}@q@GsAOs@GkASkA[YKo@Ym@[YOwAcAi@e@i@k@g@k@c@o@c@q@a@u@O[]{@Yy@Wy@U}@S}@O_AM}@IaAGq@AYAYG}BGsCY{N?YA[McEGeCIiDGeBKaBGaAIaAEa@KaAG]Ec@OaAW}AY_Bm@{CoBwJ?AKi@?AmCyMiBiJiA{Fu@{CcAuDo@oBg@sAQe@Yu@]w@m@qAo@sAmAcCmB{Dm@kAq@sAOYkBwDoB_EqAiCy@kB]w@[{@Yy@e@yAk@wB_@yAS_Ak@_DOiAq@uEc@oCUqA]yAW_AWy@[{@k@sAm@qAMWe@u@OWQYw@gAmAyAcBqBc@k@e@o@a@m@w@qA[o@Sa@a@cAmAuCa@eAc@cAO_@]u@a@s@_@m@i@o@e@i@MKs@q@g@e@yAoAw@y@g@m@]g@c@{@c@_AgA_CSk@s@{A{@qBSc@Yg@Q[_@g@W][_@a@c@mAuAeAkAkAuAqBeCsB_CQUQUuA_B[]KMOSm@s@aAeAg@k@q@i@y@k@c@W]O[Qm@Y]OeAYm@MIA]GWEWCe@EkACcA@o@DwDDu@?}@Eg@Gi@I_@IUIUGeAc@cAq@sAeAs@{@oBqC_@k@g@u@e@s@CGu@gA]c@[_@q@o@o@i@yBaBSMgAy@{AgAa@WaA{@c@c@{BaCuBeCiEcFY]QQq@w@qA}AoCeDy@{@m@m@k@e@m@c@aAq@o@_@q@_@qE}ByHyDyAu@gAi@IE{Am@eAa@cBk@GAgBe@WIsB_@{Cg@yAQUCiC]mC_@{Fu@qBWkGw@}AQo@IwAQy@Ky@K}@KqAOo@Is@M]ICAy@U_@Mw@[}@e@m@_@wBuAsAy@cDuBWMeAm@k@[c@UmAk@_@Qo@WmBy@oBy@{@]qAo@w@_@q@a@s@i@QKmAmAmA{AcAsAuEkGACoA}Ay@cAUWqAyAKKcBiBAAsAqAsAuA_D}CkBkBCCc@c@qAqAUSo@o@u@q@KIe@c@k@e@EE[YWSq@k@OM_@Yo@i@g@a@]YWSkAcASO}@w@YSq@i@}@u@GEy@o@i@e@SQsAiAu@u@i@k@u@{@e@m@W][a@i@u@e@u@_AuAGKWe@O[[i@KSa@u@IMKS[m@g@_A?Au@wAc@w@EIOWO]o@iAo@oAs@qAi@eAa@s@]o@Sa@kBqDWe@eAmBg@{@Sc@y@_BYe@Yi@o@oAa@w@{@aBk@eAo@mAi@_A_@u@GIi@cAg@_Ag@}@e@{@i@eAc@{@Yi@o@kAUa@OWQYQWSYc@g@]]e@e@YWy@q@y@i@{CgBCAy@c@s@a@WOUMa@YcDiCWUg@e@iAiAwAsAwAqAqAoAc@c@kAgAAAi@e@YYMIw@m@u@k@{@m@m@_@iCeBIEgAu@]U{CqB}@m@aBgAwCoBWQeBgA{AeAECqJkGe@[u@i@s@e@i@_@w@g@a@Ye@]{@i@o@c@{CoBoAy@k@a@GEeDaCy@s@][uAgA_CsBwBqBiAiA{@w@{@w@}@}@w@s@q@m@s@s@m@k@_@a@II_@_@y@w@m@k@c@a@KKk@i@e@a@]]c@a@]]a@_@GGc@_@[W_@UOM[SMGUMg@YcAg@s@_@iAk@WMq@[u@_@}@c@s@]i@Ww@_@o@Yg@W]QOG_@Qu@]o@[i@Wu@[m@U[KsC}@y@UaA[aA[sAa@w@Uo@SUI_@MA?kA]eA[oAa@y@WWISIm@U}@_@WKw@]o@[gAk@k@]o@_@cAq@cAs@i@_@_C_BuAaA}AcAwAaAq@e@{AaAe@[aAq@kBuAsA}@k@a@MIc@Yu@c@e@UWMWKg@QSIKCs@S[Io@KOCw@I]Ae@CA?a@Aw@BsCFqCJk@F_@?m@EkAGs@Ig@GOCc@IWGc@MME[KAA]OOIUKYQu@e@a@Yo@k@a@c@Y[W[MQU][g@MS_@s@]w@MYKWGQAGQg@Uq@gCmHk@}Aa@kAa@kAUq@Yu@O][w@O]OWMWEEMUS][e@Ya@SUMOEG[]GGkAiAmB{AWSm@e@WSOMqB_BYUSMCCAAe@[s@a@a@S]O_@Ma@Oi@Qc@Ma@Ge@KUEWEWGq@Om@K[Ia@Gk@KYGGASEOEi@KeAS[GSE_@Io@M[GSEu@MYGOC_@I_@Gm@M_@GSE_@GUCu@Ku@I]ESCWEs@Iy@IYE_@EaBOk@Iq@IiBSo@I{@I_AOe@IqAYWGUIo@UYMQK]OYQSMq@c@k@]AAQKs@e@UMWQGCa@WYQQKOIOIm@YWMg@Si@QUIYKo@QCA]Ik@Mi@Gg@Kk@Ek@Gk@AQ?gAAW?[@G?s@DY@[BUB[Dc@Hy@Pg@Ji@J]H{@Pa@Hu@PSDu@PQDYFa@Fi@Fu@D_@@e@?Y?WAq@Cy@G_@Gk@KSCk@Mw@Uy@Y_@Og@Q_Bk@s@WOGa@OeA_@_@Mq@Wq@UyAk@s@UYM[Kk@U]McAa@UI[Ks@U_@MOGu@YeA_@o@WMEe@Qw@YiA]gA[cAYKCo@OYIu@QgAWaAQm@MUEm@Kw@OkASSCkASk@IGA}@Oc@GYGy@MSEs@Oq@MmASq@Kw@MkASeAQUEe@IcAQA?u@Mo@K[GiAQCAgASw@QIEg@Ms@WUIWK[MUKw@a@e@WKGoAy@y@o@CAo@i@y@s@u@q@KIk@i@k@e@UQYUOK]We@Yi@[A?]OIEYMc@O_@M[ISEg@Ka@IMAc@E?Ag@Co@EUAe@AiDM}@Cs@CiAEYCQAc@EcAOiAWy@YWIm@WoB}@kB{@_Ac@}@a@WKm@Y}@a@ECq@[UMs@[g@Ww@[ICGA[OmD_BoCmA{@]m@]cBw@kBy@oAi@sCqAqL_F]O_Bq@UI{BaAcCcAeBs@eAe@gAc@SKuD}AQKYOo@]o@a@ECe@]SOi@a@WUc@a@m@k@e@g@o@q@?A{A}A_AcAs@u@MO{@_As@u@GGg@g@a@a@o@k@UQWUm@c@UQs@a@k@]_Ae@w@]m@U_A[iA[w@Ou@Mm@Ku@IwAKqAK[CaAEiAGyBOkAGOAmAI]Es@E]AaAIy@ECA_@CgAGYCkAKm@EEAw@IcAIgBSGAUCa@Eo@GSCE?UCWCo@I_@EOA[E]EsAMgAMu@GeAMUCSAIAeASEAKC]GSGo@Q]Kk@Sq@YEASIMGSIMGkAe@aAc@u@YUKgAa@a@Og@Qu@Us@Sc@M{Aa@o@SQEyK}CkAY]KQEu@S]KA?qCw@}@WKCkA]kA[GAQGq@SWGu@Ss@UUIWKWKWMYOWMKGIGk@a@UOWQYSMIECWQ_@WKKQKYSWOYQSKCAm@Y[MWIWIYIYG[GUEYEQEG?GASEA?YEEAg@I_@GsAUa@GGA_AQOCe@IOEUEWEGCSE_@K[IUIYKg@WWMYO_@QYQuAs@qAq@s@]u@_@gAk@uAs@s@]k@[o@]cAg@_Ag@]Qm@Yq@YYMSG[Me@OKCEAOE[Mo@SYIm@O_Cg@mAYs@Ok@MWEUG[GYGYGWGa@IYIWISGWK[QWOUOUSg@g@QSQWc@q@]u@M[M_@CKEIQw@Ke@Ow@Kk@K_@Ia@Os@EUCKI]EK[_AWk@Yg@a@m@Y]SSk@e@WQWOc@Yo@c@o@a@a@Yk@_@o@_@k@_@a@Sm@_@m@a@eAo@i@a@SMOMYYQUQUQYQ[MYMYMWIWIYEMCOCMESG[AICKAIASCOC]Ce@?OAQ?[?a@@_@By@FiAFaAJiBBe@LwBLwBDk@JiBJcBFy@@W@Y?CB_@?G?K@Q?W?S?Y?U?UA_@C_@A_@CYE]CYE_@CKCSCMCQEOIa@G]IWI]K]Ma@M[Qg@IQM]OWQ]QYOWQYSYMUS[c@q@EGIMQYS[OWs@eAc@q@c@q@e@q@a@q@a@m@c@q@SYSYSUSUKMIGSQAAUSUQUQUOWOm@]g@Sc@OYIk@Q[IYIq@S[Im@S[KSIQK[QWQWQSQSSQQCCOSKKIKS[OUUa@?AWk@Se@IUK]GWEKCMCOEMCMCKCOCOEYAMCQCUAK?EE]?IAK?GAO?UA[?_@?S@s@@aA@_A@g@?o@@i@@[?i@Ae@A_@A[ASAMC_@Ea@CQCUEYGe@GUKi@S{@CMEMCKEMM]Oc@O_@K[KW[y@e@qA[y@Yw@]_AUm@q@iBAEe@qASm@e@sASm@iA}CYu@m@cB[w@a@iAe@mA[y@AC]{@Oc@u@mBCGo@iBi@uAM_@gAuC[}@cByE{AiEs@uBYy@Y{@IY[{@Yy@m@eB_@eA_@eA]aAM]Yy@AEWu@Yu@CKIS[}@Ww@a@eASk@[}@Sm@EKY{@Sq@g@cBUy@AEUy@_@{AEQOk@Sy@IWMg@S{@a@}AU}@_@}AK]U{@U}@_@}AK]K]Y{@O[M[IQCGOYQYc@q@g@m@QSi@i@USo@c@cAm@o@[WI[KWGYIKCe@G[EYCq@C_@?W?kAF]BYBmAJq@Hs@Fs@F[DY@WDu@Hq@Fu@Bs@@Y?a@Aw@EO?YEYC[GUEs@OWGu@Uo@UUKo@[WOWQi@a@WQWSSSUSUUg@i@c@i@OUU_@Wa@OSYm@Q][s@Se@Sm@Ma@Ma@Mi@Ka@EQEQCQOw@O}@Iq@Gc@EQY{BKo@G_@OmAG_@Ii@Ec@EYEWIm@SyAIg@Io@Mu@K}@U_BSuAESU_B]iC}@sGM{@Km@OaAQ{@Mc@Uw@Qg@Qg@Qg@_AsBIMa@u@e@q@c@m@i@o@c@k@SWuBkC]e@oA}AkBcCkEsFUWw@cAoA_BAAY_@W]oA}Ae@o@MO[_@w@eAg@m@e@m@e@m@_@g@m@u@{@eAe@m@g@o@g@o@e@m@SWmBmBa@_@CAg@a@WQi@_@WOaAo@m@_@q@a@m@a@ECMKUSUQUSUSSSUUg@k@SWe@m@SWCE]k@_@m@CEOYO[MUCEKWM[]{@e@kACIi@wA[w@g@sA[}@[w@[w@[}@Qg@Um@Ma@GWGQCOIY?CS}@G_@G]?CG]Ea@E]Ec@E]ASAKCa@Aa@EaACeAEaACw@?MC}@EeA?UEg@AaAAWGyACqA?K?a@Aa@?c@@_@@_@@_@Bc@F_AHk@Hs@D_@Ha@^eBPu@R}@R{@VoADOFa@F_@Da@Hu@@OB[D_B@kA?G?YC_@A]?IG_AIcAQcCEm@CSQgCGaAIaAC]AGC[MaBM}A?GEa@?CAECUAKCWM{@Ic@ESCMG]CKGQK_@M_@K[M[Yo@CGq@kAMWACEG[i@_@s@A?GMYg@_@s@Yg@GIa@u@a@u@a@s@CEo@iA]q@QYQYMWU_@OQGIKMUUSUQQCCECMMWQUQWQWOYMs@Us@Sg@KsAUa@Im@MiAWq@Qs@Sa@Oi@Ui@Yg@Yy@i@y@k@eAw@CCUQWQaAs@m@c@cAu@cAq@WOo@]q@]ICo@YwBaAMGo@WYMm@]UOUQWSUQSQUWe@m@_@k@AAWa@Q_@Q_@ISWu@KY?CK_@I[I_@G[ACGc@EWEa@OaBMwAK}AIw@W_Ds@aJI_AKeBEaAAy@Ag@?k@?q@@]?a@@_@B_@@a@Ba@Ba@B_@Be@Fy@B]Di@FcADm@HkAFcADq@Ds@Ba@@a@?_@@a@Ag@?M?KAM?MCe@?OCQ?CC]C_@E_@G_@G_@EWI]Mi@I[CKEKAGK[ACKWM[MWKUSa@c@s@_ByBKMMMuAqB_@e@a@o@S[a@q@OWKSOYO[Q_@O[M[M[M[O_@Um@K[M]M[M_@O_@Ws@i@uA]_AWs@e@mAO_@M]a@eA[y@qAcDEKc@aAWi@]u@oAiCwA{C}CuGg@iAm@kAWk@OWCI]q@k@mAEKk@kAi@gAIOg@gAgByDWg@u@_By@eBs@wAk@kAWk@c@_Ag@aA_@o@KOGIKQ_@g@KMSUMOSUUSe@c@USUQYS[SKGw@e@u@a@CCaB_AUMg@Y]Si@]k@a@A?k@c@WUUSWSe@c@UUSUSSY[SW[]Y[QUQWQWq@aAU]QUa@m@W]QUc@o@QWSWS[a@k@c@o@g@u@_@g@W_@}@qAYc@MMQUWYUU[Y[W_@We@[YOYOOKYOm@][Si@Yi@Ys@c@_@WA?KKSQUSSSSSSWSWCGKOQWOYOYQ_@KWWs@[_AK]Us@]_AYy@Y}@Wk@Sc@GKS_@QYi@u@QUA?SSSSSSYUKIg@]IEYO[OUKWM_By@w@a@}@c@g@YECSOUSUUSSACQQSW]e@IOMQMYYk@Qe@eAkCWq@_@aAWi@GOO_@Q_@S]OYKUYc@MSS[SYOUk@u@u@y@a@e@k@s@mAyAU[a@c@GG[[USYYi@e@SOUQYQSOYOQK[OUMUKCA]Oi@Qk@SSGMEOCYIUEWGWEe@GQCUCSCYC_AEcBGoBEG?O?_@AYAKAKAQAA?YG[EYGWIWKWISKMIkAq@KKSOOMKIIIGGEEGGEGKMUWIKEGIKIOIMMWGKIMYo@_@{@Sg@Q]]{@Q_@O_@g@iAUi@a@gAKYQe@[_A]iA[_AY_A]gAMa@IUKWM[KWGOKQISOWKQS[W]OSa@e@_@_@QQ_A_AcAaA{@{@k@k@i@g@a@a@]]c@a@g@e@o@o@i@i@k@k@k@k@o@m@y@u@o@q@s@o@KM]]i@g@k@k@g@e@_@]YYm@k@e@e@k@k@i@i@UUSSg@g@e@e@WYMOKMa@m@CEOWS_@Q]O]GMGMEMCKM[K_@K_@Me@U{@k@wBMe@Uw@GUM]O_@[y@Yo@S_@MWMQQ[Ya@OUMOW]i@m@SUUSWU]Y]UOMYOOKSKSMWM]O_Aa@cBs@e@QgAc@}@a@cAc@_Bq@q@YsCkA{@_@cAc@iAe@aAa@_Aa@}@_@gBs@qAk@g@SoAi@sAk@]MkAg@aAa@_@QUKMIWOGGQKQMOMQOc@a@MMa@e@]e@W_@OWS_@Sa@MWKWIYOa@Qm@K[YmAq@yCu@}Cs@uCUcASy@cBoHiCwKCKMi@AGMc@Oi@Qi@Qe@Yk@Q[MSWe@g@q@a@a@a@a@_@[e@][Qg@W]QWKaAWUG_@Gm@ISCC?_@AY?Y?i@@}HXgADi@?y@Ak@E[Ak@Ia@Io@Mq@S[MSIa@QOI]Qs@c@i@]SQWUq@o@_@c@o@w@c@o@Yg@MUGOm@uAYs@Yy@gCgHiFuN_AeCkBiFs@sBWq@a@gAIWuA{DmAeDm@aBq@kBoFiOiEsLgGyP{BmGmBoFACcD_J?CcAoCWu@EMEKKa@I[Om@Ic@AIIg@M}@Ek@Em@Ce@Aa@AaAGcDCiBGeCE}@?SCUAYC[C]CYGm@Gc@Gc@Ik@CIAMGY?CI]G_@I[GWSw@Ma@IUUu@Qg@IUISSe@O[OYIOS]OW[k@Wa@gAeBUa@k@_Ag@y@Yg@Yc@GKIMOUW]OSIIKKOOGIQOQM]YEC]U]SyAs@aBw@y@a@]QCA_@WMIQMOMKMUUWWOQIMOSMQMSGMUc@Wi@Se@M]Qk@I]Qw@Qu@UaAESOs@cAsEu@gDe@}BYyAKm@Ii@Ik@Im@E[WgB[sBSyASqAcD{SIg@SoAc@mC_@}Bm@mD}@iFm@{DAGe@oCoA{Hi@eEc@_EOsASoBUqBMkAk@wEUyA_@gBS{@e@iBY}@?AGQUo@u@mB_BcE?ASe@aD}H_C{FqEgLWu@U{@S_AOu@Ic@G_@Ea@Ga@Gq@G}@E{@GoDIiFGyDCg@Ac@Ek@Gi@Gi@Io@Ii@Ia@YoAI[GUAEKYIUQg@Wk@]s@g@}@a@q@gCaEwCaFiDyF_AeB]u@Yq@g@yAQo@q@yCSeAQwAUuBK{AE}@EmCAoACqCGoDMcCU{B_@eDO}@SkAG]I_@Kc@W_AUy@[_AY{@]y@?A[u@iAmCQc@k@sAo@_BeAgC[u@]{@ISq@yAi@yA[{@Q_@]{@_AyBSg@k@sAkAwCCGwGcPMYOYS[OUW]SWSWEGOOSQSQAASOWQOKECq@_@i@Uy@a@UK[Oo@]WQWQUSWUEGMKUWe@m@U[KQCGc@w@Se@Sc@IWUu@Sy@Ga@G]Ia@E_@Ea@Ca@AOAUCu@A}@Am@A{@A}B?}BKqDMcBIm@QeAU}@W}@Ww@O]CGISa@u@Wa@KQQWm@w@a@i@}@gA{@gAu@_AWYc@k@g@o@c@m@SYQ][o@Sa@Qe@m@sBYyAGe@Gi@Gs@Cc@C[?MCo@?o@Am@B_ADgAPeBh@cD\\oBX_Bl@oDd@kCt@iExDyTb@iCz@eFdAgGb@yBPy@r@{BHWPg@FSVo@Ra@Rg@R_@R]NYNU\\g@Zg@hAyAbEoElAsABCnBsBVYlCwCPQbAiAh@g@^a@X]h@m@v@aA^g@PWf@u@p@mAf@eAVg@HOL]Vq@Re@?AVw@ZcA\\kAz@_DZkAv@}CVy@\\aAZq@BGXo@^s@FILST_@z@sAXa@jDkFd@_A`@y@b@iA^kA`@uAXmAh@sCn@aD`@mBp@aC|@yCd@qAhAoCh@gA`EgJpAuCf@iAvG}N`AqBP_@vAmC~BaEZi@r@iAn@gAh@_A~CuFhB_Dn@iAZk@N_@Re@Zy@Xy@Pk@Ps@FYLk@Lq@vAyIr@wELs@Fc@L_ABYBWDu@B{@?q@?o@Ac@Aa@Ee@IeAOaAU}AUqAUqAWcBIc@E]Is@Ee@Ei@GyACc@A_@?{@?e@@_A@wA?{A?a@BcD?u@Ck@Ae@Gw@Gw@QqA_@_BMi@Qg@Ma@Qc@Wg@We@Ye@[c@SUIIUWQS[WWSo@c@_@S]O]OYKm@O_AW_AWiBi@s@QiA]g@QOEe@Qc@Ug@W[S]UYUg@a@_@a@c@e@UWUYYc@S]S]Yg@Ym@Se@O_@K]IUMa@EMGWMe@Mo@EQE[My@Io@AAG}@G_AEy@Am@?CAo@@q@@o@@o@Du@Dq@Fq@Fi@Hm@N_A`@gC^sBTsANgARmAXcB\\yBF]R_BHu@Hu@Dc@HgADs@Dw@By@@MBeCBsE?_B?[@cCBqG@aC@_EBuE?uAByIBmF?ABwK@mCA_AAeAA}@Cy@Es@GaAIgAKgASeCOcB[uDIy@SgC[cD[uD?AW}C_@mEa@kEYiDU{BMmAMwAWwCOmBG_ACc@Cu@?ICk@?w@A_A@eABeABgBDcCFcDBkB?EFuCDiEBuA@}@A_AAw@Ce@IoAKmAUoBEWMs@UgAAEYkAOs@EOg@yBe@uBEMG]I[WoAOaA?CKq@Ky@CWGu@Gw@Cu@GiBAkA@}@?_AB}@Bw@F{@FiA@MJqAJkAHeAJmAHmALcBL}ABa@JuAT_D\\mEVmDH{@JyA?ADk@RcC?ETsCLwBD{@DsA@i@?aAC}BA_@Cw@MqBKeAGg@CWGi@WmBMgAK_AKaAS{AGg@E]Ky@Gm@Go@OgAOqAUoBg@aECOOoAS}AQuAQ_B[eCWwBYaCScBSgBC]SeBU}AO{@SkAUiA[sAYiAa@yA_@qAa@wAa@uAOg@aAiDe@aBm@wBYeACGK_@c@}Am@sBk@uBq@_Cq@_Cu@mCc@yAm@wB}AqFe@aBi@kBa@uAc@}Ak@oBYgAQg@?Ew@mCGQa@yAo@}Bw@oCs@cCg@gBMg@Mi@Kg@Ge@Ik@Gi@Eu@Ei@Ci@?CAq@?m@@k@@u@Dk@Di@Dk@@CFg@Hg@Fa@Jg@Lk@ZkAb@mB`@cBb@gB^}AT_AHc@Nu@BSJk@L}@BY?AD[Fm@Fq@Do@Dq@BgABcA?u@?u@A{@CcAEcAGcAI_AK_AMaAG_@SyAWaBWgBk@_E_@mCMy@QkAE]WgBCMUcBWaBM_AeAkHSuAQsAMw@SmAS_A_@uAMc@CEIUCKCEUm@_@{@o@wAa@eAk@uAc@cAA?CIk@sAq@{Ae@eAi@qA]}@Oc@Kc@K_@Mk@I_@Gc@E[Gi@Cc@C]Em@Ak@Am@?m@Bq@@e@Dm@Di@Dk@Fa@F]DYF_@VwAl@mDJe@L}@Jq@Lu@?CL{@NmAHw@Fw@HgADu@@ID{@D}@DaA@s@@O@[?_@@gA@uAAm@?]?MAu@CmACsAE_AEeAIsAI_AKkAMoAOoAQqASuAWwAUgAQ_AOo@CIWaAa@wA]iACIQi@K[a@iAk@_BSg@Wo@g@oAk@{AYw@Wq@gAuCkAyC_B_EaAgC_BcEg@sAKYy@yBc@iAw@sBUi@Qg@e@mA}AaEyAwDw@sBo@aBCIM[Wo@]u@e@eAa@w@_@w@c@s@k@_Ak@y@s@cAs@cAeAwAqBqCm@{@i@w@Ye@[e@[i@Yi@[q@_@{@_@aAWy@Us@Qm@AECKGWOq@AAOu@ScAg@gC_@mBk@yC?Aa@yB]aBKc@k@yCuAgHwAkHeBeJ_A_F_AuEY{A_@cCOgAIu@IaAAKIaAGeACc@A[GwA?MAW?_@AkA?_B@cADmCBgBHaED}CLuG@w@BeABmBFcCBeAB]Du@Fo@LcALw@ReAR{@n@yBn@}BVy@\\oAH]P{@Ji@@MJw@Ba@BYDm@Bi@?W@u@?a@Ac@C_AGgAI}@Ge@UwAO_AQeAO}@O}@QaAIy@IgAE_A?_@Ac@?Y@i@@c@B]Ba@F{@Fi@Jq@TiAH]J_@Na@J]L[\\u@\\q@b@o@`@m@b@m@d@o@d@m@z@oAhA_B^e@b@o@lAeBjAaBb@k@d@i@PUj@i@RQTQXSf@YXQTKVMVKp@Sx@U`AW|Bm@jA[p@Qp@Qr@Ur@Yn@YVKl@[n@[dAo@~@k@dAq@dAq@zA_A`Ao@VQdAo@dAq@l@_@l@a@ZYTQ`@c@h@k@V]^g@T_@Zk@^w@h@wAZaA\\uAXaBRcBJcB@WBi@@cAAiAC{@Cc@A_@E_@C_@CQK_AOu@CSGWGYEOK_@K_@Y}@M[Ys@S_@AAMYOY_@k@W]c@k@e@k@aAiAq@y@W[SWa@g@S[OWQYMWOYM[O_@K[M]U_AMk@EYG_@EWK_AEi@Cc@Cw@?g@?aA@i@@W@a@Da@Dc@B]L}@Hi@R}@z@iDR_AZqAP{@FSt@cDf@qB\\yA|@{D^}ALg@h@}BZsAj@aCd@sBT}@TeAT}@R{@Lk@Pq@X}APcABYD_@Da@Da@B]Dg@DaABcA@{@?O@YA_@AaACcAEy@Ea@Ei@Ek@Ik@M}@CUCIIe@I_@I]WeAa@wA{@wCcAmDW}@Kc@O{@QiAEYIm@Gs@A_@GaACo@?YAIA]?OCq@CcACw@Cc@A_@Ea@Ei@Kw@AOMq@Qu@Ka@W{@u@uBq@iBQi@mAkDg@qA[cASs@S}@Q}@QaAE]K_AGg@Ca@G{@Cc@CaA?c@?a@?c@?c@B}@BcADkAL{DFcBPsFRoGBkADw@TmHJgDDeAFcA@YHgAJaAJcAR_B\\cC\\aCTaBN_AF[H_@Je@^wAJ[Z}@Vq@Tg@HSP]NYPYvH}Kf@u@PYR[R]DGHOJON]N[LYNYL_@L]L]DMDMJ_@J]DQBKH_@DUH_@He@D]N}@VeB?EN}@b@wCV_BNcALcAL_AB[PgBDa@@O@QDe@@U@Gn@kKF}@N_CPeCRwDHuA@E@O\\wFFaAl@qJ?CXmERgDR_DRgDXiETeEB_@DcA@a@@c@By@@oD?ABcF?cC@aA?o@BwI?c@?oB@eC@qF@}A?oC@wA?{ADyN@{B?W@qBAo@EmBAe@Es@K_BIy@CWAEC]AGCSOeAEUAIa@qCCK[yBIe@]aCG]cAwGE]G_@Ia@G_@Ia@G]I_@K_@AEGU?CK]I[Oi@ACQi@KYUq@m@}AGIi@iAk@eAm@cA[c@q@aAe@m@[_@IIGGKMSSSSMOGEUUg@i@CCe@e@EEiAiASU}@aAg@k@yAgBGImBiCqBwCq@iAAAs@kA]q@QYMWEGISGIGOQ[MYGKIQYq@Q]GKEMGIGQOWUg@EK]s@IQUc@MYq@wAs@{Aa@w@yA_DgFyK]u@MYMYO[KYM]M]K[M]K[I[Ka@K]K]I_@I_@G]GWAGG]Ga@G]G_@Ks@AMs@aGE_@QsAa@cDe@_Eq@sFEW?GG_@O_AGa@QaAK_@Os@Ke@M_@Ka@GQOg@K]IU]aA[u@Q_@k@oAEIIQa@s@a@q@QYm@_Am@w@QUw@cA}@mAsAiBqBoCOSyFqHu@eAaC_DcGcIMOq@_AKMSY{AoBw@gAmAaB{AoBw@gAkA{A{AsBc@m@w@cAkA_Bw@cAy@iAeAwAy@cAu@eAw@eAu@cAgA{A_AkAcAsAy@gAc@m@[c@q@_Ag@o@[c@sD}E{DkFSWQU}B}Cs@_AY_@u@aAa@m@U[OSo@cAw@qAm@kAg@cAWm@KW[s@AAIUGQIUWo@CIIUGQOe@[cA_@wA_@_BS_Au@cEwBsLY}A[cB{C_QwA}Hs@aEkAuGCI_@{Bg@oC{@yEG[g@qCG]Ms@OgAOgAC[OoAQuBAS?IIuAGgBC_ACgAAc@CgAAsAEoACc@A[CYCMAIC[G_@Ga@Mq@_@yASo@Sk@i@iA_@q@c@m@a@g@_@c@g@e@AAaAs@mAo@MEo@S}@WaAU{Cq@w@SKCmCu@u@UA?}@WgAWAAcBk@A?{Au@mAu@oAcAAAkAiAg@i@q@}@eAaB_@o@]s@GMWo@]_Ac@qAmAuEOk@m@}BQk@kAoEg@}Ae@qAi@qA_@w@Wg@}@aBuAwBy@mAcA{Ai@y@aA{AyA}Bo@iA{AmCQ]y@aB}BoEoCqFyDuHk@gA_AiBQ_@Yk@iAyBIQO][}@Uw@S_ASqAAGOwAOiD_@kIOeDIsBUwEQwDSuEEgAAQA[Cs@A[?QAK?q@?aA?eBDiBFwABo@De@Di@Hm@LcAZwBn@yC@Ib@cB\\kAHUZ{@\\}@Zu@Rc@Ra@HSDG@C@??AxBmELSFOnAcCDKjBsDP[`@y@dAoBHQf@o@LOp@u@h@c@`@[x@e@vBeARId@Wh@WRIj@[\\UPMHGROZWj@o@VYT[`@k@HOPW^w@Rc@Na@JWX_Ad@aBFSH[ZeAV}@J[DOb@{AV{@DQd@cBRo@`@wAV}@Ty@V{@V}@Ty@`@_BP_ALy@Fk@LaAJeBFaAHgBFaAHcB@WLqCHsALoCFkALgCHcBLeCJgBLiCHcBB_@HsANwATyANs@Lc@f@_Bj@sATg@Vo@vB_Fx@oBRm@Rs@Le@Nw@Fe@Jy@DYDc@Bg@BaA@k@?YAcACk@Eu@MkBKuAIqAGaAEc@QeCOaCQ_CEm@S{CGg@IaAWcBQ_A]}Ac@}Am@wBc@}Am@wBc@{AU{@Ok@a@sAk@uBW{@Ke@i@eBCMUq@Sc@[o@U_@QWQWq@w@a@][SOMa@W]SMEMGu@Yo@YcAg@o@e@{@w@k@s@c@s@Yk@ISSg@Oe@U{@[wAg@_C_@aBQy@Mi@e@yBAG[sAQ{@G[U_AWiAc@aB[y@M[a@u@]i@W]e@g@YYi@c@o@a@q@[QG_@Oq@Os@Ms@Gm@Aa@?o@D]Dm@J_@Fs@RiA`@iAh@gAp@wA~@WP}AdAOJiAr@UJOH]N[HYHq@NWFa@D]DY@_@@I?u@C_@Aq@Iu@Is@KeAKa@G]Ci@EE?[?m@?y@Di@HK@kAV}@TuBf@a@JQDs@P_B^WDUFa@F[BO@U@g@@S?Q?]AOAUA_@EWEYE[I_@Kc@Mk@Ye@We@[{@g@c@a@YYcAeAy@y@eAgAY[_@a@}@}@y@o@o@c@{@c@MEs@Ua@Mk@Mq@Gu@Co@@i@@s@HmCb@g@F}AXWF_@J_@La@Rc@Z]Rk@d@g@f@k@x@Y^o@bA{@`Bm@hA]z@i@dAIJMTa@d@[\\QP_@Z]Vc@Vo@\\WJy@Ta@FWDS@YBc@BqABeBDoBDcABm@@gEJQ@y@JE?g@J_AXm@VsAh@cCdAiA`@w@Ro@Jq@Hm@D}EZmAN_@H]HQDk@PYJm@V{@b@s@f@e@`@w@l@uKzIwAjAiBzAoAbASNe@b@QPYZY\\_@`@yAhBMNaAlACBk@r@a@^a@Zc@ZCBo@Zk@Vk@PWF_@F[Bc@Do@Be@Aa@Ec@EWCi@MqEqA}Ae@{Bm@cF{AmA[{Bq@c@MsA_@YK[K]QQIm@_@k@_@USm@q@_@a@Ya@a@o@q@sAyAeDmAiCaAwBo@uAaAmB_@q@g@{@kAsByDyGkBcDs@oAeAiBwKkRoDkG_AaBwBuDa@u@k@qAY{@_@sAACg@}BS_AUaAy@uD]_BUaAU{@Sm@Ws@Wm@u@_Bc@s@W_@S[]c@W[y@}@k@i@k@c@k@a@m@a@gAg@_@Oo@Uw@U}@Q_KqBmAUeB[]GWGm@Io@GWCg@Ci@Aq@Ac@@a@?Q?gIH{@@}A@cB@iCBe@?q@@yBBoAB_B?oACgBO{AUw@My@QqA]u@Y{By@wBs@}B{@cAa@sAq@o@[_B{@{CcBwAw@_B}@}BqAeBaA]UaAk@s@_@yAy@q@a@m@[cAm@wAy@w@e@g@]y@k@wBaB{CaCy@q@s@g@uAiAcBsAq@o@]_@c@i@}@yAs@}AMY]w@a@w@k@eA]c@a@g@_@[a@]c@Yc@Wc@Sc@Qs@QkBe@UGeB_@qD}@w@SuBi@_Be@}Bi@SG_Ci@qAYmBc@wEeAuAYmAUqAQy@KkBOgAIkAA{AEo@?Q?Q?eABuADWBi@DaAFk@FaBTs@LuAVs@PIBk@NcAZw@TqCv@qA`@aFtA{Cx@kGdBMDuDbAm@P_Dz@IBYHa@Jm@PuA\\E@iARaANA@A?wBXaD^wC\\g@Fi@FUDa@BK@qD\\cCVcBN{APkD`@oBPqAJc@Bi@BqA@WAU?UAgBOiB][Gi@O_A]e@OUMmBaAo@e@eA}@i@e@CAY]EGyBoCaAyAi@{@Qc@I[Qe@CICGWw@aAgCc@eAu@mBc@kAKYWq@s@mBYy@cBkE_@gAUq@YaA]oAe@iBOs@g@yBAIUoAQcAM}@Kw@Ks@Go@AKIo@Gm@Ec@G_AIcA?CIaBIeBCoA?ACy@CqB?eB@w@?_@@u@@a@@m@@m@@GBy@Bg@Bm@@UF}@HmAFu@@GFm@H}@Ho@Ju@\\eCj@yDf@kDNeAXiBHi@Jq@v@qFvA{JRsAjDuUt@_Fr@}EDY?AViBJ{@ZiCB]Fk@@c@DQ@UBiABs@Au@Ao@Ac@A_@Ck@Ck@AYMsAIaA_@kDWmCe@kEE_@Iy@[{CWgC]gDIy@QyA?EGg@Gk@C[SoBIaAGm@SkCKsBAs@?QAm@?s@@q@Bu@Be@Di@?EB]Fc@Da@Fi@Hg@D[Lm@Jg@Lq@XgAXcARs@f@eBFSXcAl@{B^uA\\uA^gBPgAR_BHm@@SDg@LwAHwAFcB@q@Bm@AaA?aA?k@QwEIyAKaAOuAM_AKw@sAaGw@sC_AuCc@mA[_AcBcFmAoDyAgEQe@u@oBSk@_A{BaAuBsBsEQ_@[o@EISe@k@qAs@cBUi@s@eCMi@Qy@O}@EYC[Gg@Gu@Ce@Em@EsA@[?k@BgA@k@@YD_AJoANgATcBL{@b@cCHc@^yBX{AxAoILs@F[Js@p@wDV}ATsALq@Fc@PeAJu@D]Fa@LiAHu@Hy@ZmDDe@JgBHoBFgBFwB?U@cEAiDASAoAC{@EkAE{AEm@MuBIsAQkBQeBGy@?A?AIw@sAoOa@mEI}@q@aHg@gGK_AK{@KcAi@cG]yD[qDSwBOeBEm@UiCAQCWAi@UyBCWO{ASoBOwAGm@mAeMIw@o@aHu@mICYOaBI{@E]KmAAGGi@Iu@CQa@sC[sBe@iCMg@_@cBk@gCaAuDk@wBk@mBY{@Oa@oCgHaA{BuDkIuCqGoCkG{CyGo@yAo@wAqA}Cc@aAe@mAq@uBQm@Oc@K_@Oi@Om@Mm@UaACKSeAQeAO}@Gi@EU]iDKcAEa@IyAQmEC_B?m@AUEgJCqHC_EQuLMeI{@ij@AqA?MC}AGiDAi@Co@Aa@O{BCWUoBGc@EUESGc@I]G[CQEOMk@Ma@Ka@Ss@_@cAWs@Yo@M[CGSc@a@w@e@_AWg@KQAAAA?AACQ[AA?AKSS]yAiCk@cAQ_@MWOYKWK[M]KWGSIYIYU_AAECMESMo@UmAg@wCoA_HGYUkAWoASw@CMW_AY_AY{@q@oBu@{BeAwCk@gB_@iAKc@IYGYKe@G]CMCSEQAOY_CSgBE_@MsAYoCaAaIE]OeAMs@Ki@Mo@}@{Dc@oBYmAc@uB]_BKk@Mq@EYEYG_@E[E[EYCYC[C[Gm@Ca@ASA]AGEsAA[AY?]?A?QAY?]@w@@iD@gA?K@sA?sA@u@@{@?O?O?O?K@q@DeE?qADcFBqE?wA@qA?A?Y@aA@sC@eCC_BSqGSeFEu@_@{J]yGG_BG}ACm@Ey@Ca@IuBSsFAUCiA?eA?sBBuADaAFu@HcARkBJ}@Fa@V{ALw@XkAXgAZkAVq@Na@L]L_@FMtAsDVo@@CDKJYFQPc@x@wBd@eBVeA`@gCHm@Fi@ZcETiCF{@B[P}C@QBkAB}@DcB@}A?OAgF@yF?aF?G@kI?}C?iBBwQ@mC?g@?{B?sA?uG?eEAoB@cB@aD?cFAoAAu@CcACu@IwASoB[cDMiA?GKoAIaBEeAAiA?cA?_ABuS?e@?sB?aE@}@@w@@a@?UDm@Bw@HeANwAPoANu@Nq@R}@XaA^mAj@cBj@cBp@sBb@qA^iAd@wAbAaDt@{Br@yBbCsHr@wBZsAVeA|@eE\\kBZsBTuBPcBHcARgCDo@t@qOh@cLDcAHyA?Md@}I~A}[bBm]LgCLgCDaABg@LmBFiBHsBLgCH{AJqBNoBRgCPsB`@_E`@gDn@oEXiBx@{E`AiF^eBNo@r@mCdAgEtAqFxBqIHUz@cDPi@^qAj@_Bl@{Ab@iAXk@d@eAf@eA\\m@hAqBFIz@uAdA}A|BgDvAoBT]@A`AkANOx@u@x@y@XWxAoAr@q@FEZ[?At@w@@Cb@i@RWbAyApA_Cf@eAb@aARg@bCsGfAsCh@yARg@hA{CRi@Zy@L_@HYb@yARu@Jg@ZaB\\cCPkAHk@NaAVmBXmBNgA?EHg@f@oD^gCF[XgB?Ax@sEdAqFj@}CTmAXmBViBPqBPaCBo@HaBBmABkA@_C?g@A{ACgAIkBGuAMoBMoA?CGm@Ii@MkACUK}@W_C?GsA}LQeBEm@AIEa@e@yGa@cIMkC[uFIoAGy@Iq@Kk@Q}@[sA]iAs@uBm@aBg@yAWaAMq@Os@Ku@Iq@Iw@Gw@Ey@CeA?{@?yA@aD?U?A?k@?A?EAgBA[?AGuAGu@Gy@UkB]gB[qAg@cBc@gAm@qAm@kAmAiB_CsDeAcBc@s@[g@Yc@eEwGeDkFo@cAu@kAy@qAqBaDkAiBaBiCgBqC}CaFkAkBOS]i@OWU_@kBwC{A_CuCuEiHeL}E{H_AuAa@s@]k@e@q@y@qAYg@S]CE_@y@_@{@M_@Yu@Qk@Mc@Oi@Sy@G]GYO_Ao@qD]uBWyAMs@SoA}@qFWqAOo@Qm@[iAKYCKM]Yq@i@oA]q@Ue@e@s@a@q@m@w@ECa@g@Y]mEkE[[[[gEgE[YACwHuH][o@q@aA_Aw@y@][y@y@oBoB]]mCkCiEiEYYg@g@eBcB]]WWe@e@k@m@g@k@m@s@]c@SWa@k@]c@W_@c@q@Ua@_@m@]m@g@cAe@aAi@mAa@aAYs@_@eAc@oAQo@c@yAUw@m@gCW_AOs@a@yAe@mBaByGU{@Oo@S_AO}@Ik@Ga@Io@I}@KcAO}AOcBKkAIw@a@mEM{AKeAMeAGi@AOKs@QwAUaBg@oDUuAa@_CAGQaAUkAWkAOo@]eBS{@WcA?CSu@U}@Qu@I[AEc@yAQk@Qq@IUK[M_@_@eAQk@_@eAk@_Bk@_Be@qA[{@Qg@Uk@M_@k@_Bw@wBYy@w@yBSk@CIM_@]cAe@qA_@eAWq@gA{Ce@qAu@uBiBgFk@{Ay@}BYy@s@kBm@cBi@{AOc@M_@}CqIoBoFQe@}@eCk@}AYy@s@qBaAkCc@oAq@kBe@mAGSo@eBAGs@kBSi@g@yAe@{Ay@kC]oAWcA_@aBk@eCUkAEOScAQkAKi@[uBSwAIg@Ea@S{A_@uC[gCKy@Ms@Ku@GYMk@]}AMe@G[Y_Aa@mAKW_@eASc@Se@Ue@Uc@AA_@q@We@s@oAYg@U_@_@q@]m@c@w@oAyBu@wAg@eASg@Se@Sk@KWOe@Sm@]oAU_AWmAQ}@Mq@Ky@My@Iy@OeBGw@Ew@Ew@EuA?MAa@?I?C?_@?U?q@@qA?IDkHFaM@kA?CF_LDoH@{A?o@BqEBqCDaI?[?O@o@DuJHaNBmE?KBoEBiEByC@yD@uA@k@@qA@y@BgADeA@Y@SD}@D{@^sHTcEPcDLqCDk@?EBg@h@mKp@mMPeDFsABc@JgBDmAFiAFeAB_ABg@HwCBgA@g@@eABgB@}A@cC?wAAqA?]AqBCkA?e@CmACcAC}@EkACw@A_@MiCEeAEi@Ce@KaBK{Ac@{F[_EEg@Q{BQ}BOwBMwAGm@Mw@Mu@Kg@Kc@Ia@Ss@Uq@K]Qc@O_@]u@Q]OYQ[U]Yc@e@o@e@k@[[[[YUWU]We@[WOSM_@SYMSIYMc@O]KWG_@IWGUEg@Ga@G_@CYCe@A]Ae@?Y?Q@_ABm@@qAD_@@cABe@@q@@S?g@?o@?WAWAc@ESAWCi@Ge@I[Eq@Me@K{@Wi@OcA_@s@Ua@Oe@Ou@Wu@WwAg@_Cw@eC{@sBq@SIOEu@WaA]cA]gA_@g@QWKKEc@Qk@[_@Se@[a@YUQUS_@]a@a@_@c@[a@GIS[Wa@[g@U]a@{@Wm@Wq@Oc@q@qBg@}Ag@yASo@IQWs@Qa@MWQ]Q[i@cAGIgAmBkBcDcAkBa@{@Wm@Um@Sg@Og@Uq@Qo@Oo@Qu@Mm@Ks@Mw@Ig@Eg@EYEe@Ei@C_@Cg@Eo@Ak@CoAA[?[?u@@]@_@?]Bo@@a@Du@NoCNmCTcE?Eb@sHf@qJDm@DaAt@_NRoDHiBBs@DwADyA@mABy@?c@@qA?}@?K?s@?y@AiAAkBAkAMoSGyKCsCCgE?c@E}FIgM?k@G}IA_@CkCAkAGkBQiDQeCKoAKaAMeAQyAGe@EUGi@o@aFM_Ai@mESsAEa@YsBIw@i@cEGk@OkAGu@CUC[Ei@Eo@?ECa@Ck@GyACc@Aw@Ak@Ak@AyA@qA@uAByAJgDDeADiADsABy@@SF{BHmC@YB_@@[JmBJuAFw@Hu@BYBU@GD[B[Ju@Fa@F[BSf@}CL{@p@eE@G^_Cj@uDTyALw@PqAHk@H_ALuALsANkCJkC@e@@m@@{@BiCEgEEcACy@GuAC_@IuAMsAGy@OuAc@gDGe@ACGi@kCuRQoAe@gDIk@w@{FKw@KsAEw@Cw@Ai@?q@@w@?]?C@_@@UBY@[BYBY?EBQ@GB[DYD[DYLu@FY`AeER{@H_@FWVoAF[DYBIBQHu@D_@HgAFuA@w@?C?m@@GAy@EsAC]MoBKu@Ku@UsAe@cCEOQ_AiBwJ]iB_@iBOi@Qk@K]Uk@K[KSSc@Qa@Wc@S]MSOUe@m@Y]QSy@y@w@u@KGgA_Am@g@QO_Aw@w@o@w@o@oAiAQOa@c@OQQU_@e@[e@c@w@MUWm@MWWo@Uo@IYQq@Qs@YoA{@wDm@iCkAmFSaAIc@Ks@OaBEe@C]Aa@Cq@A}@?E@uABw@FcBL{C?OF_BBuABu@?_@@yC?k@Am@?KEoCEuAGuAIsACm@AECe@AGIiAQcBCYE[OmAYqBE[_@uBe@cCS}@Mi@q@_D_@iBMc@sE_T_@cB{DqQwAsG{BkKkAkFyEiT]{Ay@qD_BsFw@yBy@yBo@_B}@oB[o@e@cAc@w@Uc@KQIQ}@yAy@sAgAkBgAgB{@uAq@iAS]EIYe@eG_KWc@gFqIsDiGgAgBk@_AS[s@qAk@eAu@_Bq@}Aq@_BK]m@aBu@}B]kA[mAk@aCQ_AEQWoAa@eC]gCYiCQoBKsAM_CIwBiDgbAAQAe@Cy@U{F?SG{AGsBEgAAKEsACw@GsAEsACy@Cw@Cy@CsACsAAy@AsAAc@A}D?gEHyFHiDJsC@m@B]VaF?C@QDm@VwDJ{ADm@RmCVsDHgA\\}EB[Dm@\\iEHgAZqE`@yFHsAXwDDm@^eFd@sGT}CHcABe@?CNkBj@wH^mFHsARwCV}EP}E@[?QJgE@uA@g@@wC@}FCkIAeIC_OAiICeF?eBAiG?gDBsEDqCDsBHeDPiEViELsBTcDHcA?EHiAhBmWJqArA{RDg@LgBJoAn@eJRqCPkDHsCDiD?sCE_EE{AKqBQyCMqAC[Ca@E[Eg@McAKy@QqAO_AI]EYQaAKe@_@wBm@aCmAaEMa@c@oAM]Y{@]}@mAgCk@iAm@kAg@}@[g@Ye@Wc@{BeDgGaJu@gAuCkE_CkD_@i@qByC}@sAuGwJgCuD[e@KMs@gAiCyD_@k@oAiBeBkCeA}AcCoD_IkLgA_BQYaAyAg@u@g@w@iAcB}@uAeHgKEEe@u@AAo@aAMQkBoC}@sAeFwHOUkC{DiAcBaP}UsB{CcAuAW_@AAW]Y_@mA_BqBeCqCmD{FkHoDqEOOQWY]eAuAw@_Aa@g@{BuCY]cFoGIKY_@}@gA{BqC}AoBuAeB_@e@oA_BmA}A}CyD_I_KgH_JqAaBoA_B{@gA{@gAoCkD}GsI_AmAIMq@_AyA}BiAkBeBuCsBiDqF_JuBmDoCqE_DmFoQaZcCcEoJyOcBsCeBsCuA_CsCwE_@m@Wc@CCy@sAgAmBcBqCsBiDgBuC_C_E}@wAWc@gAiBk@cAgAgBAAuBmDMQeDsFmDaGiJoOkIiN}GaLmD}F_BmCWa@OY{BuDqCuEgDsFuDmG}AgCsAsByA{Bo@}@aB}BkBaCsBeCa@a@cAmAo@q@MMy@}@s@q@gBgBa@a@kBcBg@a@eA_AqC{BwD}CYWsAgAmAaA]Ye@a@{E{DiEkD_Au@}CeCy@s@mB}AcH}FaHwF{AmAaDmCWSc@]e@]kAeAw@q@sBoB{B{BgCsCu@{@kAsAyDiE{AaBy@_AsB_CeBmBwDgEkDyDkSgUsAyAwL_N[]aEqEyXe[yLaNkRcTqN_PgF{F[]qN{O_BgBkDkDMMoCgCyAoA_LaJyBgBiJsH}GqFmFmEyAkAm@g@c@_@sAgA{AkAqEsDeBuAeEiDyD}CYUwBeBc@_@oCyBAAoB}AEEkCwB_CmB{AmA_@Y]YkCuB_DiCCAqC}BSQOKqCyBiByAOKsA_AmD_CiD}BgAs@eBkAu@g@}DiC}@m@c@Y_C}AyByAoBqAcDwBu@g@cBiAwE}CcC_BeEoCQOcEmCWQ}B{A}@m@GCmCiBeAs@m@a@o@a@qCkBi@]wCoB_DsBQMoBqAeBkAq@c@_@WuBuAe@[sBsAgBmAQKwBwAq@c@eBiAuA_As@e@i@_@eC_BWQwBwAcAq@yAaA}AeA]U_Am@aAo@wCqBk@_@qJmG{@i@o@c@iAu@{@k@UO}@m@wA_AcCaB_@USMII_Ak@?Ai@]SOk@_@a@YmA{@WQECwAcAc@]iAy@mByAGEUQ]Yy@q@_@[sAgAa@_@_Ay@qDcDwRmQoCcCuAmA][yAsAqBiB{@u@[[w@s@oF_FsCkCiZgXoCcCQQyBoBoBgBOMk@g@{@w@e@a@QSy@u@KIgC}BCCu@q@kAgAeAaAa@_@sAkAWWoBgBiBiBqAsAs@u@_AgAcCuCQSkCgDeAwAACo@}@o@cAw@uAm@gAyAcCi@cACEi@aAg@_Am@mAc@}@]y@aBuDYo@KYGMa@cACIsAmDkA}CcDuI]{@_DgIsFsNkA_D}@aCs@kBSg@y@wB{DaKmBaFgD}IuBqFmAaDSg@kA_DQe@Sg@eAsCgAqCe@qA{CaIoBeFoAeDoBgFIUmCeHy@yB_BcEe@oA[w@]}@k@}A_@aAoAcDoBeF?ASg@kA}CSg@kDcJSg@w@qBwAwD]_A_AeCeAoCUk@c@iAy@uBkA_DSm@kAwCmCcHiAyC[y@Wo@cEyK{C_IiB{EmAcDiC{Go@cBsBmFkFkNGOSg@kA}CgBwEwE_M}@_Cy@wBM]}IqUaAiC_AgCgC{G_HqQy@uBQg@_@_AyCyHsG}PQg@sAkD}BgGaBeEoBoFUi@Qc@u@sBUm@Qe@{@wBsBmFQg@aBaEe@qAaBoEO]e@oAe@mAa@iAUm@e@oASg@c@kAg@sA{B{FkBaF_AgC_BeEy@uBe@oAkA_De@mAu@oBi@uAw@wBgCsGSi@Qg@Wk@gAwCe@oAaBiEsAgDu@eB]{@w@eB}@eBGOMUc@{@GMgCwEWc@Sc@iCuEACUc@_MyTc@w@We@mRi]}AoC{AoCiCuEUc@Uc@qEcIgAmBk@eAkGcL]o@AAqBqDUc@Wc@eAmBiCuEoJ}PIMMUqGqLgUsa@kGcLaEoHaEmHyB_E}BcEmBiDmQy[cJiPu@qAaAgBcB{Cm@iAoBmDyAiCsAeCwAiCwAgCiAmBiAsBaAiBQYwCmF_EoHiFiJ{@_Bs@qA[k@_CiEcCgEa@w@A?a@u@i@cAw@}AOW[m@w@}Ae@cAYo@e@eAg@gAM[Yo@c@gAg@mAa@iAc@mAo@gBi@_Bu@cCi@mBgAuDsAqEgAwDq@}Bk@mBeBcGc@wAy@sC_AaD}AmFgBeG}AmFsAqE{BuH{AmFgBgGEMcB{F{AkF{BuHqB_H_BsFa@wAo@yBsAqEqAoEqAsEqAmEiBiG}AoFgBgGgBcGoAmEaDqKcBaGgCwIsAqE}AoFgBaGe@_B_@sACIK_@yBoHgBgGw@kCmBwGyCcKyAcFi@gByDyMuKc_@k@uBy@qC{GkUSs@EOYaA_@sAaAeDa@qA_@sAi@iBgAsDmAiEa@uAyDsMsEwO}CmK}HkXkHuVeAqDyAgF}@{CeAoDmBuGoAiEeAsD}@{Cg@cB{@yCoAiEcB{FoEqOgCsIaCgImAcEs@}BUq@?A[y@a@gAw@iBw@eBe@}@sAgCcA}AkAeB_AmAk@s@gBqBwAuAi@g@e@a@kCsBsB}AiKyHcDcC}BcBeE}CiAy@_BmAmA{@yAiAiAy@w@m@mA}@}AiAoB{AaEwCk@a@i@a@{[aVqA_AkCmBcAw@qB{AqB{AkA{@qA_AaNaKmGwE}AiAeD_C}AgAwA}@iCqA{Aq@uAi@gBk@mBg@kBa@c@IqCe@iDi@}Do@uCe@sCe@eC_@_Eo@a@GYGeFw@kEq@c@GOC{AWgEs@k@IcC_@oAS_Dg@wAUqDk@wI{AoBYc@I}ScDiDk@aC]y@O[G_@GkBYuCc@yb@aHi@IsDk@a@IsGcAyAW{A[sBe@uA]oA]wBm@qBo@cBm@s@[EAsAi@m@Wg@U}@_@mCqAWMoCqA_Bw@iCmA{CyA{CyAi@Wu@_@cBy@cBy@k@Yw@_@KEyAs@_CiAaAe@OIu@a@oAk@{BiAaBy@yCuAq@]_@SiD}AaBy@[OwBeAc@ScD}Ak@WKGeB{@m@Yw@a@KGQKOGa@SMGa@QoBaAWM}C{A{BcAkCmAaBy@m@WsB_AqAo@i@W{@a@_D{AGEk@WsDgBeAi@}@c@eB{@cAg@UKgEsB{As@_CiAQKaAe@m@[g@Yu@a@_Ag@g@YmAs@y@g@]SWQ_Ak@_EkCi@a@sAaA_@USOSQsB}A}AqAuBgBCCCCWUYWyBoBIIk@i@UUAAQSqCiC}AcBa@c@iCuCu@{@eAoAgCaDkA}AuAmB{AwBgAaB_AwAu@mAcC{D{@uAgAgBy@sA{@uAuA_C]i@A?Ua@c@s@eAeBeCeEoIgNi@_AgAgBEKaBmCw@sAc@u@uAcCiAwBoAiCe@}@kA_Cm@qAaAsBmBkEwAgDgAoCy@wBeAoCAAUo@mAgD_AqCkAmDmAoDSq@aB_F_@kAcA}CaB}EkB{FyByGiDcKiBuFWw@a@oAi@aBk@cBaE_Mi@eBmBuFeBoFeA}CsBmGk@aBGSoBaGoGsRsBkGYw@sD{K]iAIWaAsCWw@iDgKmE{MkBwFuBsG_@kAeCqH_FeOsCwIm@iBmB}FMa@o@oB_DqJ_FaOW{@mGmRAAa@qAuEiNcLi]Uq@cBgFK]eA_DmCcI]gAgAcDCGyCqImAyCKWiC{FMWyG{M[q@uEgJsHgOUe@sGkMmCuFaAoBiG}LwHsOiEqIcAqBeDyGk@iAyCcGmN_YsHiOu@{A_DkGmBwDSc@Uc@c@}@oDaHoJsPMSKS[i@yD_H_@q@mPuY_IkN{@yAcBwCgBuCeDaFo@_As@_AoAcBiAuAeAoAqA{AyAaByEuE{BuBqBaBwC_CsB}AgCcByCoBaBgAmCgBa@Y_@U_Am@iAw@qBqA}@m@_@Uw@k@qHaFcDuBsEyCkCgBA?y@k@aBeAOKy@i@s@c@eBeAi@[sBeA_Ae@cEsBa@OAA_@OkEyBYOECkCqAuCwAAA_@QcEsByAq@iL}F_@SEA_Ai@i@Yc@Wk@a@e@_@_@Ya@_@i@e@_@]]]IIQSKK]_@a@g@]a@Ya@a@i@Yc@q@aAi@aAa@u@KS]o@Yo@M[MWOa@Oc@O]So@]aAyAgE]{@Qi@Qa@_@eA]y@g@iA[q@]q@]o@Ye@]k@CGIIi@{@s@}@a@i@SWOQsAyAu@s@g@e@o@g@s@k@g@]sA_As@c@{DiC}B{Aq@e@}AcAk@_@_BcA}AeAq@c@?As@c@uMyIwHcFyB{AqBqA{EaDyByACA_@UGEq@g@_BsA{@y@i@k@k@o@w@_A]g@o@}@c@o@QYKO?AAAYg@AA]q@cAqBSc@Uk@Uk@c@iAIUK[Ss@Qi@Qq@K_@Mi@S_AS{@u@wDaAaFQw@?AMm@QaAA?Ie@k@uCsFyXmAgG{AsH{BeLwAeHo@eDg@gCw@{D_@kBUkAWuAOs@UmAq@_Dc@mBI]]uA_@wA{@_D]gAKa@Qk@[y@q@uBc@mAk@aByAuDm@{Ak@oAa@}@i@kAYm@Sa@Ue@i@eAsAiCeB{C}C_F{AyBgA}AmA}ACCY_@k@q@g@o@k@o@e@k@a@c@}@cA}@{@_AaAgAeAgBcBcA_AgAcAeE_EuIgIaFwE{JmJ][eBaBoWoVwCoCu@u@oWoV][KIoHgHiOuN}HqHm@i@kI_IkVoUu@s@oEgE}BwBiH}GaE}DyCqC{FqFe@c@iI{HuGmGEEWUEEcAaAAA]]aA_AIGSQ_EyDyLiL_A{@{@{@c@a@OO]YiRmQcHyG[Yu@s@{AwA_A{@w@u@eAaAu@q@gAaAy@q@gA{@mE_D_CuA_@UsBoAmCyA_@SuFwCoCyAQK{EeC}I{E_IiEA?]SwN{HwOoIqAs@eIkEGEaFmCaO}HaDcBgJaF{DsBGC_B}@_@UiAm@w@c@_@SaCoA{Ay@eAk@aB{@_@UeJ_F{HcE}@e@eB_AiAm@cDeBcDgBaDgBqAw@_@U_Ak@}ByAqE{CWQi@a@{@k@cN}Jw^cX_GgE_D_CgCkB_CcBGEIGMIOMkA{@UQkCkBi@a@[U[U}FiEkAy@kDgCga@cZsByAuDkCcE{CmCoByDuC]WoCqB}BaBcEwCkBuAkA{@kOyKkCoByCyB_@WqHsFuF_Ea@[oA}@KIUOg@a@]UaBmAQMcCgBsAcAmLqI_@[_@W]UuP}LuCuBq@e@m@c@e@_@q@g@aAs@WQoEaDsA{@uCiBwDqBqDgB}DcB}EcBkDeAaAWkBe@aAUsAY}AYiB[eBW}B]iEm@kC_@{AS}Cc@qHgAiC_@qr@wJ_HaAc@GKAUEgBWkBW_BUwCc@gAOkDg@cEk@sB[eDc@sFw@wG_AsEq@cG}@eJoA_OuBmC_@sEo@sDi@kb@aGcQeCgAOyASkEi@{HiA_AMkAOcBWcNsBGAoDg@gDg@wASwB[oFw@{ImAeP}BuT_DiC_@_Dc@s@IsG_AyK}AuWuDUC?AcZeEa]{EeG}@_QcCgAOeAOgBWGA}IoAkCa@k@GuG_AyB]aIiA}K}A{AU}PaCsEq@kBWgBW_AMoAQaOwB_Fq@cC]{AUuDg@_AMaAKiBQqAKm@E_@CUAKAUAkAGeBG_Qu@uDQiKe@c@CyFUe@Ca@CiDOsAGMAeAEcJa@C?mKe@cCMkCKoBGc@CYAI?{@E}FYaCIsCMaCMiBIaCK_AEiBIkBImAGKAwESs@Ca@CcH[sESqFU{FWsCMiLg@yEUwOq@_@AkI_@eNm@cPs@{FWaI]uES_BGyCOwEUsPq@c@CkBIoCMK?_BIa@AkBKeS}@c`@cBc@CcI]}GYy@Esh@}B_Oq@kKc@uEUcI]aCKyUeA}TaAqMk@_GW}BKqG[iDMkESqFW_CKsBOmBQwAOg@G}ASuCe@e@IcASeCg@a@KeAWcAY{@UkBm@eBi@uAg@eBq@yAo@{Ao@uBeA}BkA{BkAeCqAsFuCwBiAgW_NeIgEq^oRiPuI_@SsAq@a[gP_LaGcEwBgHyDqBeA_G{C}F}C_@SsDmBKGYOSKcAi@mBaAYOiFoCaB{@_Ag@iBaAsBiAaAg@SKsAs@qAu@qBmA_Ak@aAq@mBmAiAy@qAcAu@o@{@s@s@m@g@a@s@o@u@s@c@c@cAcAs@w@{A_B_@a@m@u@QUuBiC_AoAkAcBqDgFsCaEqC_E}A{B]g@w@gAgA_B{@oAo@aAe@o@k@y@yAwBmBoCoAgBmAgB{AwB_E{FuDsFe@o@oAkBeBaC{AyBqAmBIIkAgB_AqA}@qAe@q@{@qAi@u@m@}@o@_Aq@_Ak@y@{@mAm@}@k@{@}A}Bq@}@qAkBw@kA}@sA_B{BcCoDiBmCkAaBCEgA}AkAeB{@mA}@mAoBuCiBmC{BcDm@}@gBiCc@o@eBgCg@q@w@gA{BeD}@qAeC_E{@wAYi@gAqBm@kA?AUc@u@{AYk@cA{B{@mB{@yB{@uBsAyDo@kBkD_KGUISc@qAc@qAi@}AeA}CMa@oCaIw@_CQi@qF{Oq@uBc@mAeA{CmAoDiBmF_@gAqB_GcAwCeA}CGQQi@y@aCoDmKoAqDcCkHYy@k@_BaCeHY{@Qg@gAcDCIM_@q@mBCKQi@m@mBSq@oAiEk@{BWcAS{@]}Ae@uBc@wBu@{DUoA_@qBCMYaBy@mEYaBAEg@cCm@kD}@_FY}Ag@kCi@{CiBqJo@mDKk@uAwHCGIc@iAiGKi@?CuAqH[eBqCiOaDcQSiAQw@uDkSIc@_AeFIc@Ke@O{@UoAMq@Kg@cAsFcAsFAC?AyBwLg@mCiCkN_D{PuE}VsEsVKk@iHk`@}CsPmEgVsAkHYwAeAyFu@}DaAqFyBsLu@{Ds@}D}@}Es@}DcAqFkAqGe@gCm@cDqBsKqCiO_B{Is@yDe@gCe@iCs@{D_@mBkAoGaCsMkDgR?Ae@eCiAkG_@qBcAoF{@}EcAoFi@yCKg@q@uDY{Ac@aCo@mDQ_A[uA]}A]oAu@wC?As@cCOa@Oe@K]EOQi@sAsDCEYy@mAuCkAiC[o@}A}Cw@uA[k@kBwCw@mAo@}@wAkBoBcC_AeAs@w@q@s@q@q@iBaBeCwBw@m@e@]{AeAUQkBkA_Ai@[QqAs@gCoAUMa@S_@Qa@SeFeCkJmE_@SA?{J{E}Ay@sAo@a@Q_@OkQsI_Ae@{CwAyPgIeD_B{L}FiJqEiI}Da@SuU_LeFeCa@QyAu@GCwFmCeAg@sZ}Na@QwYmNa@SoAm@yHuDyDiBie@aUkAk@oJsEyHwDgGwC}QyIyBgA_Bw@gHiDoFiC{BgAgI_EwBeAmG_DcGwCwDiBeBw@eBu@}@_@eB{@mCqAgd@mTiEuBqHoDqAo@mDeBqCsAyCyAuL{FqKeFeK_FwKmFae@_UeTgKiAi@mDcB{BeAeB{@eD}A_Bu@KEsAq@gHkDsHsDeAg@yYmN]OgDaBa@S{DkBeXsM}^mQiI}DcGuC]QgB{@kReJiMiGsE}BeCkAiCmAeBy@wDiB}WoMmEuBiNwGaGuCsDkBsBiAaBcAaBeA_BgAoByA}CeCiCsBgBwAYWWQgByAuEsDeT}PgCoB_XcTuf@q`@_@Y]YqFkEmH_G]YgUyQ}AqAuYqU]YUSwC_Ce@_@]WqBaBGEyCaC[WqW{S_@YwCaC{AmAaDgCiB{AcB{Ao@m@{@y@_@_@WWmAoAwA_BoB}B[]o@{@kA{Ac@k@W_@KOg@s@a@o@{@oA[e@w@oAg@{@uAcCkBkDkAaC[q@wA}Cm@yA_@_Aq@aBs@mB_AkCi@aBu@{BmBsFQi@K[Qi@g@wAe@uAK_@AACGQi@}B}G_C}Gc@qAQi@GSqDmKaCkH}AsEsDuKgGqQu@{BaAoCY}@eA_D_CcHeBiFiAcDEKaAyC{CyIKWeAkDgA}CCEq@qBq@oBqAwDc@sAmAkDm@iBuBoGc@qAq@qBu@wBqBcGgAaDgAgDk@cBm@eBe@wAWq@{@iCeDuJ}AuEY}@oAoDi@}AoAwDu@{B_AmCgAeDuAeEiAeDu@yBs@sBkAkDuAcE_AoCgBoFw@}BgBiFg@yAYy@kBoFeFoOsDyK_CaH_ByEgEaMsBmGiA_EeAyDcAqEmCwLcE}QcBqHmHk\\gFsUcBsHeAyEMk@Mk@Mk@qK{e@wBuJcD{NsJec@_CkKuDwPWeAAIS{@a@mBy@oDkAqFi@aCiCeLiAgFmAiF]}AWkAWcAoBoH{@sCyBsGc@kA[{@k@wA?AYm@Sg@aIuR[{@k@uAWm@cB_EgAqC{ImTyAqDcAgCsAcDiCqGyCkH}AyDeAkCgBkEuBiFgBoEmBuEiCsGeBmE}AkEy@wC_@qAi@wBm@uCo@aDuA_Js@{Eu@_Fa@eC_@iCy@mFq@oE}@_GMw@o@iEi@cDW{A]}Ag@}Bs@mCk@uBa@oA_@gAc@iAa@eAAGQe@MWa@cAa@_Ae@cAq@wAw@yAMU]o@MSs@mAe@q@GKe@u@cAuAaAmAc@k@y@}@s@y@y@{@_A}@o@m@eB{A{@m@e@]u@k@s@a@mA{@_Ag@_Ac@WMc@U]Qg@Ue@S]QC?c@QECsAi@qBu@oBs@eE{AeC}@yCgAsCeAeC_Ay@WMEgCaAkE}AyEeB{EiB}EgB}EgBaGwBwBw@}@]mAi@y@c@w@c@w@e@w@k@g@]u@m@k@e@}@y@cAeAc@e@a@e@eAuAu@eAy@oAOY[i@?AcCkES]wAeCWc@QYEICEuBsDi@_A{AoC{AoC{@}AWc@eAkBMUk@cAOYeAyBGKACQ_@i@gAAESg@CC_@}@e@kAGOACc@kAKYUq@AEQi@Sm@ACSq@g@gBy@cDEOQw@WmAKe@Km@Ko@_@qBWmBAA]kCe@cEOmAu@sGUwBc@}DOkAa@qDGm@UmBq@aG_BeNsBwQyAkMcA}Im@wFgAgJe@aE{AyMK_AK_A[kCsB{Qi@oE_@iDGi@Y_CIw@Q}A[kCa@kDIw@qDm[c@mDGa@]iC]_CAM[oBUmAUqASgAa@oBYsAWmAMk@EOOo@I]Mg@y@aDa@yAQm@_@mAeBeGoAiEs@aCIYq@{BiA{DaBuFSo@}@}CgAqDgAsDeAqD}@{CIY_@mAo@sBCK{@wCs@aCg@cB{AeFMa@cByFgAuDg@eBoBuGmAeEMa@gAsD_@oAOk@u@gCgBaGoAgESq@}@{Cg@aBi@iBq@}Bc@yAaAgDa@uAo@uBqAmE{AeFo@wBMc@qAmESs@eB_Gq@{Bi@kBq@}B[cAkHoVa@wAuDiMoB{GuBeH_IaXw@oCcEgNoEmOkFmQqAgE{@wC}@{C}@wC{AiFq@_Cq@}BgBcG}@yCg@eBoD{L{GeUeCoIe@}A_IcXM_@}DaNIU]oA_@oAuAuEOg@s@aCo@_C{@yCS{@Ok@Qw@I]U}AQqAE]Go@E_@GgAGiBCs@?u@Aq@?c@@[@_@?U@WBs@Bs@Do@De@?GFs@DYBUBW@IL_ALw@F[FYF]Nq@Rs@H[\\kA`@kAd@iAf@iAVg@b@u@d@u@HKR[NS^e@p@w@dAgApBsBFIh@i@DEVWtBwBxGyG~A_B@Ah@g@fBiBhHgH~C_DvAwAJKTU~CaDfBeBvAuAfBgBdAeAr@u@\\]f@g@`@c@hBeBdAgAfBiB`EaEvByBbAcA`@a@RQb@e@dAeA`@_@b@c@d@e@NO`AcAzAyAxBwBd@e@`BeBlCkCnCqCbBcBzByBz@{@x@{@d@e@jDkDdGcGNQ^_@FGrAwAdAgAr@s@`BaBVWxByBv@w@dBgBvDuDpKqKXYvAwAtAuAtAuAzB{BzByBbAeArAsAfAgAd@e@FGXYt@u@`@a@r@s@b@c@`@a@b@c@b@a@`@c@PQNOb@c@r@s@`@c@b@c@`@c@b@c@X[FG^c@`@c@PS`@c@^e@`@e@^e@^e@PSNSNQ^g@^g@^g@^g@j@}@l@}@zA{Bl@}@lGwJxJeO~BqDh@y@bBgC~AcChBqChBqC`A{AHKLUdEoGhEuGVa@tCmE~@wArEaHjDoFf@s@fC{DxUq^rB}CXa@v@kAvCwElAkBvBgDLSXa@lBuCjBsCbFwHxJgOrDwF`@m@dBkCjCaExA{BxAyBn@aAj@}@l@_AjAgBvCoExCsE|RoZzCwE|@sAnE}GvBiDh@{@NYZm@Ta@Ra@~@qBFOP]Xs@Vo@Tq@Vo@Pg@BI`@kAHYPm@\\oARu@Pu@XoAFSXoAXqAXsAXoANo@d@{B`AgEVoAj@gC`@eBh@gCXqAr@_D`@kBXoAXqAb@mBLk@lAsF|@cELk@fDmO~AkHnB{ItAkGz@{DlAsF^aBR}@z@{Dr@aDrDoPXoA^cB`@oBdAuEl@oCLk@r@aDv@oD\\}AXoALk@j@mChCgLh@gCj@eCv@kDlDePlAmFv@oDJc@@GLk@|@}DF]Lk@v@oDn@uCrCmM?ALk@r@}CtBoJ`BqH^eBr@_DJa@@ILk@xAyGdAwE`@iBNu@Nu@DWNy@D[Ju@NoAB[H}@@W@CDu@Bc@@YDoA@a@@Y@_@?s@?a@AmBCyACe@AQGyAKuAOwACYMaACQKu@EQKk@COG][wAMi@a@kBi@eCGUYqAOq@c@kBa@kBa@gBWiACIOs@GYG]My@Ga@Gm@Iy@Gw@A[C]Cy@Ao@?Q?Q?s@@y@@c@@]@[@YB[B]Di@Fe@J_AFa@Jo@FWF[FYJe@@ELc@FWJ[Ro@JYJWFOPa@BCTk@h@eAXk@`AgBBG^s@n@oAl@gAFOx@_BLUh@eA`@w@Ve@bAmBtAmCXk@Tc@f@_A`BcDh@eATc@dAoBjBqDjCeFt@wAf@_A\\s@b@eA`@iA\\eATw@HYPs@?A@?Lu@ToAJk@@IDc@?ALcAHaAFq@@a@@M?AD_ADyA?q@?q@?o@As@?YAa@AYC[E}@KuAI_AGo@Em@AKUkCQ_CAKEc@Em@SwBOqBKqA]eEGw@CWUwCGs@AEOkBQ{BYgDCQG}@OqBGw@Gw@IwAE{ACy@Aw@A{@?uA@sA?e@?SDyADuADw@FkAFaAFw@H_AHq@?A@GFm@Jy@L{@Lu@?AFWLs@Lu@H_@FUTeAPo@No@J_@ZaAFWVu@\\iAr@yBjAuDHSDQPi@jCkIPi@HWb@sAVy@Ni@tImXRq@Rs@ZmAXmAVoANu@BQHg@@EJo@DWD[XwBLkAJiAHqALoCFcBByA@wBAkBAuAEyAMkCEy@MsBQoCSiDMiB?A?EKwAQkCCo@ACg@cIWmEEw@C{@E}@AgAC}AAw@@qA@y@?g@Bu@Bw@?GF}ANaCJoAH{@ZiCJs@L}@TqAToAViAT_Ad@aBh@kBXcALc@Pi@`AgD`@sA`@sAtAqENi@Pi@`EcNPi@pCiJbCkIjBiG~@_Dl@oBf@cBp@}Bj@iBnAkEp@yBzAcFTw@HW^oAfB_GXaARo@n@wBz@wCTs@^mAb@qAt@_Ch@uAVu@hAqC`@cAj@{ARg@t@mBVq@Rg@lA{C@ARg@lB_FhBuEd@mAfAoCFOpBcF~A_EdAqChAoCTq@`BcEb@gA|@_Cz@uBdDmIxAwDRg@x@wBh@sAN_@Xq@b@kAd@kAfAmCzAyDdEmK`BcErBiFzF{NvEqLx@uBb@gAn@}An@cBv@qBp@eB|@{Bn@_BfAqChAuCvBoFjB{ExBsFzC{HxBsFhO}_@zH{RfHsQ`CeGpZmv@xIwTjL}YtAkDhDqIxBuFj@{AxEuLvAoDvIsTzN__@p@eBVo@JWfAsCXo@Rg@N_@vGsPzK{Xn@aBPc@Pg@x@qBrIiTpAeDpCaHbAiCf@qA|@yBz@yBn@_Bn@aBVq@b@eAVq@rAgDn@aBhAoCVo@Xo@LWVm@LULWJWLUJWLWZk@JWLUN[LUJQLWLULULULULULULUNULWLSNULULUNSLUNULSLSV_@V_@LUNSNS\\i@PUl@y@\\i@p@}@jCsD|BaDpFqHfDuE`@k@^g@^g@LSNU^e@\\i@^g@^g@^g@\\g@z@mA^i@b@k@\\i@^e@T]FINUX_@BEBEPUv@gAl@y@^g@PWJOJOPWTYHO\\e@NSNSf@s@DERYh@u@^g@l@{@DGX_@NSBEvAoBzDoF`@k@xCgE`CeDzOsT@ADERY~P_V|@oA|AyBj@u@Xa@X_@zB_DlD}EnBqCNS\\e@HKbKoNfEaG|CiEjD}En@{@pBqCz@kAhCqDzB_DbEyFrLmP|CiElBmCn@{@l@{@nBmClAcBlAcB|AyBl@y@NSHKXa@zB}CjD{EzB_DlAaBRY^i@l@y@l@{@`AqA|@qA~@oAl@}@n@y@z@mAl@{@nBoCJMXa@V_@~@qAh@s@d@o@n@}@lAcBnAeBzBaDn@{@nAeBzAuBl@y@|@oA`@k@x@iAl@y@^g@jAaBpC{DzAuBhBeCzAsBfCmDbCiD|@mArEqGfCkDjAaBn@{@d@o@bAwAr@aAT]|@mA|@qAl@y@bAyARY@A`@m@v@eAr@cABEn@{@DGv@eAr@aAZ_@DG\\g@hA}A\\e@TY`@k@r@_A@Ed@o@\\c@fBcCDIf@q@dAyAdBaC^i@V]V]V_@f@q@^i@~CmElAcBnAcBjAaBpBqCzAsBnBoC~AyB|AwBlAeBn@{@|BaDl@{@nAaB|@qAdB_CfBgC|AwBz@mAp@}@`@i@jD{E@CX_@hA}AvF{HfBeCNSRYJOT[v@gANSNSNSNSLSXa@n[mc@bCgDT[fE_GtJ{Mn@}@RYx@iAlCuD|CiE^g@n@}@bCeDrMuQ|AyBl@{@~@oAlD{EjD}E~@oAx@iA~@qAjA_BXa@lEgGvHmKzI{LlAcB^g@z@mAjEcG~GoJ^g@h@u@DENUl@{@n@{@^g@\\g@`@i@NSLSNSt@aAvGeJz@mAp@}@lAcBV]V]zB}C|AyB`AqA^g@l@}@^g@^g@l@{@n@{@|AwB^g@\\g@n@{@n@{@LS`AsA^g@jBiC^i@^g@\\g@^g@PUl@{@^g@^g@LSLQLQX]tBwCJM`@k@|@oA^i@^g@bB}BhA}ApAgBX_@@AFKJMl@{@n@}@^g@FKv@eAj@y@p@}@n@_Ab@m@JKl@{@^i@^e@\\i@JMpBoC`AsA|@oAzCgE`GgIXa@jJqMpDaFXa@`DmE|@mAnBoCjA_BnBmC~@qAl@y@p@_Aj@y@lAcBn@{@Xa@TYl@{@~@qAnAcB|AyBn@{@l@{@n@{@n@{@n@}@zEwGnAeBjNsRZc@~@oAl@{@z@kAtBuCl@{@jBgClAeB~@qAl@y@~@qAn@{@^i@\\e@p@}@|@qAl@y@^i@^g@l@{@^g@^g@^i@^g@\\g@^i@|@mAp@_AZe@^g@PW\\e@\\e@PUNU\\g@PUNSNSJONSNSNSNU\\e@NSNSNSNSLSNSNUpAeB|AwBzB}ClAeBnCuD|BaD~@qApDaFtJ_NJOb@m@|AwBhA}A@Cz@iAPU^g@R[Xa@n@{@v@gAt@eAfBeCdBaC@Al@y@zAwB^g@n@}@|AwB~DuFd@o@fA{AlCwDZc@NQrAkBfE_GXa@|DqFlv@}eALOf@s@lAcBfA{A`DmEbAwAvF}HxKkO|KoOXa@n@}@PU~@qA^i@lAaBp@aAl@y@r@cAjA}AFIv@gA^g@^g@~@sAbAuAl@y@fFiHnAgBn@}@bCeDt@eA|B_D^i@pAeBn@_AbB}BLSdFeHvAiBf@m@p@y@t@y@b@e@`BeB|AaBdAaAv@q@VSbByAb@_@dBuA~AkA`BkAdBgAnAw@~BuAv@a@f@Wj@Yj@Yj@YpAk@l@Y`@QlCkApGqCtB_ApAk@jHaDnHeD|@_@fAg@tAm@rAm@~BcA~As@nAk@tB_AxFeC|K_Fj@WrCmAfAi@^Qz@c@x@c@d@[v@e@hAw@hA{@t@m@dA_Ar@q@r@s@b@c@z@cAPURU\\c@\\c@`@k@Zc@^i@\\k@f@w@Vc@^o@Zk@j@gAVi@Xk@Zu@BGvC}HX{@Pk@Lk@Ps@HYPi@@GNc@?A`@{An@yBRu@hAaEdAyDdAsDpAyE\\oAjAgE~A}FhBuG~BoIvE{PtAcFnC{Jd@gBh@iBj@sB|BiIT}@Pg@XeA`AsDrBmH`AmDJa@vAcFlAkEnC}JjBuG|@eDvCwKxDeNvAiF\\mAp@eCNi@@Cb@gBv@{Cf@_C`@iB^eB^uB^kBZgB\\sBXoBZsBTeBVkBNuAHu@Ju@NwANuAJsAFg@NmBNkB?CNyBNsBFmAJoBD}@By@JkCFeBD{AByAHcDDiCL}EJmEPiIT_KTuJ\\cOXeNVeLHuD@o@HcEFcCj@oV@_@j@_W^{PhCqhALaHV_LPyHPuHRuJd@uSBo@@a@j@wVFwCBcAHuDJ_FDgCNkGJ}GDuFAsG?AEkFGwCGuCIiCGoBMgCWgEY{E[wDOgBUaCOsA[uCi@eEm@kEm@oDo@sDw@_Em@uCe@wBs@wCk@_Cq@aCg@iB{@wC_AyCeA{CkAcDw@sBg@oAmBsEsBoEgA{BcBcDm@gAaAgBsBkDu@iAk@{@cBiC{AwBsAcBaC{CgE_FsAwAk@m@mAkAs@q@}AyAaDoCsAgASMeEaD}BgByEqDkEeDkCqBYSoCuBcE_DmDoCu@k@i@a@_BkA{AiAs@m@{@o@yAgAg@_@SOy@o@}AkAuFiE}D{CUOCCgBsAwBaBkBwA}BgBmGyE_DcCuAeAaE}CqAcA}@u@oAeAoAgAgAaA}@{@u@s@CCuAuAaBeBkAoAuA_BsA_BaBuBw@_Au@cAcAuAmAgBgA_B_@i@}@uACEGKKOKQQ[aA}AuAcCcB_DKO?AIQKSmA_CcAuBm@sAi@kAm@uA{@sB{@uBm@{Am@aBi@{Ai@}Aq@oBs@}BkA{DwDmMcBwF_AaDcAgD{AgFcEgNsAsEq@uBiHgVYaAAEW{@}@_Da@yAg@eBsBaHs@}Bu@gC{@sCuAyE}ByHkA_EyFmRmAcEu@gCwBkH}@{C{@sC{AgF_AsDk@}B]yAi@kC[}AYuA]sBWuAUwAYoBWmBWkBQ}AW_COaBOeB]kEIoAIuAMyBIkBGuAIkCImDCaBAiAA_CAgB?aB?_B@aF?{E@cA?M?_F@wE?C?i@?w@@mD?iF@mI@aH?qC?wB@eG@gI?oF?_D@}E?oA@}G@mF?wH@iG@cI@yG?uC?o@?eD@{E@{H?uB@qH@aH?{E@yE?I?qF@yD?g@?qE@oF@kE?kB@aH?{E@sB?yB@}F?[?aA@aG?oI@qC?sBCmCAqAC_BGyCIkDKiDIaBEeAI_BAE]uFY_E_@kE]{CUuBUgBa@cDm@_Eq@eEW{A_BwIe@aCuB{K[cBiCeN}D_TwK}k@oAuGoA_H_G}ZuAsHcOww@gBsJsAgHi@sCeBkJoC}NiCgN]iB}AkIGWyBqLMu@qBoKKk@aAiFgDmQoA}GiCeNgMeq@gAaGSgAG[]qBACO{@SqAOcAMw@WmB?AOkAK}@a@eDUmBMmACOQ}Aq@aGeD_Ye@uDC_@o@wF_CcS}@cI{@gHq@eG}@uHkAgKE[E_@IaAEk@CQAKC_@C[Ci@GcACa@A[Cw@EqAAg@Ao@?CAc@Ak@?m@Am@?y@@q@?A?s@@e@@kA@c@@_@DqAD}@@WBa@Dy@NoBZwEl@aJb@wGVwDPaCj@yIb@oGVwD^yFh@yHFaA@]HoAVmDVgDDu@Fw@Dc@Dg@HcAHeANgBRoBNyARgB`@iDPoAN}@v@uFDWBSLw@^{BF[BQ^kB\\kB@ELi@TeATiAVkANo@Ns@d@mBv@_Dt@sCV}@?CVy@j@oB|@wC\\cAX{@f@yAd@qAx@}Bj@yABEl@}Ab@iA~@wBd@gA|@oBpAmCf@eApDeHvCwFJSTc@jA}B`AmBlA}Bp@qAnByDFKbAmBpAgCv@{AzAyCfAsBpDcHjBsDd@{@p@qApAgCtAmC@CvAoC^u@nAcCx@_Bz@_BvDmHxAsCbAqBtBaEhBkDDINYjA{BLWj@iAVe@?ApAcCFMTc@rCsFxAsCp@sAXi@Zm@h@iAP_@HOZs@b@_Ab@eATg@Zy@Tk@Vo@jAwChBwErAkDfBqEdBiE|AcEvBoFvBuFPa@zAyDDKjA{CdAkCFO`DgIl@}ATk@\\{@Xu@Ri@tAmDJUtAqDhAqCtBoFl@_BFO\\{@Ri@Ts@f@yABG\\kA\\iA\\qANi@Ha@h@yBZwAP{@Jc@Ls@F[?CPcAZoBRwANiA@QJ{@LcALoAFy@Dc@Dk@HaAHqAHwAD}@JmCBo@XmF`AqSXoGj@cLLyCh@eLr@gOJ}BNyCBi@@EVkFBm@Bo@ZyGLaCFaBBu@JuBNmCNkDRaEL_CLeCLmBPaCR_C?GPgBLqAZkCPyAFe@ZaC^eCf@_Db@cCh@mCVqA|@}Db@gBjBuHv@}C@CNk@Li@jAwEBGlByHbA}DdAeERy@n@gCt@yClLee@l@_Cj@_Cd@gBpAiFd@kBZoAZmAPs@d@iBZqA~AoGVcAZkAPu@^{AVaAdBaH`AyDRy@l@_Cb@eBb@iB\\qAZoAn@kCVaAXmAr@_Dj@mCTkAVoAH]TmAPu@Ji@VkAReAH_@Nq@VoAZyALk@r@oDLk@pAeGJk@Lk@\\aBPw@TmAXqA^iBXqA\\cBl@wC\\aBPu@^iBNu@Je@d@{BRcAJg@@C\\cBNw@DSLk@Jc@h@kCNu@XqANu@XsA^gBVmAVoA^iB`@oB`@mBb@uBb@sBH]r@oDl@qCXqAVoAZyANw@\\eBZ}AR_ANw@Nu@RsAJw@Ju@Hu@LsAF{@F_AFoAD}@@k@@g@@oA@o@?YAq@?u@Ai@Aq@Cu@A]Ew@A[C]Eg@Ek@KwAOuAKw@Ku@Mw@Ou@Mu@Qu@Ou@[mA]mAUs@Uq@Uq@_@iAm@eB{@gCCIo@iBa@iAWq@ACSk@a@gAUq@KYKYSm@ISWw@m@cBSo@M[CMg@wAa@iA?Aa@iAUq@Qe@Ma@CGs@sBSm@Ws@M]_@gAWq@GQIUa@mA_@iAi@eBSq@[mAc@iBYoAOs@Ou@UqAUoASsAKw@CSEc@CIGm@MqAAIKiAIaAEk@KcBCe@KeBAe@Ck@GwAAIEgAEcACk@IsAG{@AWCUI}@MuAOyAGo@Gg@Ms@QgAMu@Mw@UqAYmAOu@U}@Om@EOYcAY}@Oc@]gASm@c@qAW_Ai@}A]aA]eA]gAEMISAAIU?Cm@cBw@cCOc@Sm@[cAGQM_@GOs@qCQu@Ou@Mw@Mu@Kw@Iu@Iw@Ea@Ca@Ek@Eq@Cg@E{AAg@A_@?_@AiC?uC?]?mCAS?Q?KA}@Ai@C{@CWASGaAEm@AMKcAMeAMcAKu@G[CQCICQCQ[mBEYSiAWuACUQcAQ_AMw@Mu@EWIc@SmAa@eCUqA[kBCIIk@Km@AGIe@Y_BUsAUwAESE]EUOy@?CSmAUoAQaACMG]Ks@Ke@Ii@UmASsAESO_ASoAG]UoAk@kDmAiHIi@COGW_@}BKm@G[Ig@SmASeAGc@UwAEQKo@YaBW{AQiAMq@Mw@UsAUqAUsACQAEGa@Mw@WsAMy@EWOw@Ig@OaAWsAW}AAEEYMq@OaAQ}@EYKk@_@{BQ_ASsA[mBUsAQsAQuAIw@K{@MqAGo@KsAEe@AYE_@IqACy@A[GmBCaAAYAk@?c@CcA?a@?q@AmB?sABmADoC@wA@K?M@a@?A?U@a@@{@?{@@g@?{@?EAm@Aw@?[Cs@GuAGkAImAKmAMmAKy@Io@Mu@WeBQkASmA]{BEQEW}@uF]mBUyAk@gDIk@Ig@QoAgAuGa@}BSkAW}ASqAm@kDSkA[gBUgAOq@Oq@WgA[iAOm@Ma@i@oBi@cBoAgDK[c@gAmAmCe@eAmAkCkAkCgByDmAkCkAkC}CyGuDgImEuJyAeD{@sByBoFeCkGsAgD[y@Sg@iAoCcCiG}FyNwBoFmByE}CyHYs@aCeG[u@qDcJeCkGwBmFmByE_B_EgAoCy@_Cu@aCe@cB[oAe@wBc@}B[mBi@eDqBoMmFg]y@mF_@_Ck@sDMs@Os@Mq@Mm@GYQq@Qs@a@{ASs@Qm@g@}Ac@kAy@yBe@iAWo@a@{@_@w@[k@w@wA{@yA{@qAmAeBaBsBwA}Aq@s@_ByAcA}@m@e@gBqA_BcAcB_AcBy@mCqAiEsBoCoA_D{AkCqAuDeBuBiAgC}AuByAmB{AmBcBgAeAcAiAaAgAuAaBmAcB}@sA}@sAw@uAw@wAi@cAg@eAs@{AcEcJ_CeFmAmCeByD}AgDsDgIgByDmAoCwA_DiB}DcCoFqDcIqEyJcBsDaA{BqDcIu@_BO[Se@uBsEu@aBq@yAKU]u@_AuBk@qA_@}@u@wBOc@Wu@a@yAc@}ASy@YmA_@_BG]SgAUsAc@_DWoBMqAQ{BAIEs@Em@G_ACm@EaA?GA[C}@EyAAgB?K?sB?kB@iA@C@mAPua@@cCDmF?C@w@BgE?W?mA@aA?cAAs@?o@Aw@A_@MsDOgEKqBQoC_@cE]gDK_AWiBSuAU}Am@eDMs@Ou@G[c@mBS_AWiAe@yBWkAi@aCwAoGmAsFi@kC_@{AAIaAgEs@gDs@aDe@kCe@iCUuA_@aC[{BWoBKu@Ec@Ie@KeAEe@CYIy@SsBCa@MwA?AGw@Gy@Gw@Ca@A[?AIuACWI}AA_@AWE{@EyAEwACcAAo@Ac@Au@Cs@?a@Au@?c@AY?]?_@AuB?uA?a@?w@?wCAuB?eA?Q?]?wBAkICyP?wDAwD?kGAkG?wB?iA?{@?_D?}BAmD?yBAkE?]A_AAy@CwBCy@Aw@Cy@C{@G{ACw@Cy@IyAI{AWeEIyAWoDMyBKsAa@iGIuAOwBQqCa@cGYkEQwCSoCQsC]iFc@_H]kFKyAOuBK}AAUOwBEm@Ci@Gs@G_AMuBC[Gy@i@}H{@wMAQEm@MkBO}BEo@Em@c@yGQkCEm@Eo@AUIaAEs@?GIuAGeAAWEsAEgAAm@Aq@?aA?KAgA?W@m@?]?Q?c@@o@BeADuADwAFeAHmAHmAHiAPeBNqAD]BUDYL{@PiARoAReAZ}AlA{F~@qEf@iC~@oE\\cB^mBZsA~@yEb@oBt@oDTkAPy@Nu@|@mEVkARaAXuAb@wBLk@VmANm@Pq@V_AJ[Pe@BE?ANa@h@wAXu@\\y@`@_AtAmDf@mAVm@d@kA`ByDh@oAf@iATe@Tg@Xk@LUJSHOt@cB`@_ATi@b@gAv@iBn@wAz@qBZs@p@_BZu@Ti@n@yAfAeCl@wAVo@Vo@Xu@Pg@h@{AZcADMNi@ZkAXiAZqAVmATmAVsAXmBLy@JaAPyAJeABKHeAFu@J}AT}DXkFXqERuDp@eLf@sIXyE@Q\\kG@GReDD}@JgBTwDDq@D{@@W?[@Y?[?w@A_AAi@ASAQAa@G}@Gs@ACIs@Is@Ms@GYIa@EWMe@K]I[IWKYIWUo@M[KSSc@MWCEWg@]g@{BgDw@iAgA}Aw@iAeA_BqAiBsEyGwCiE}A}BcDwEuAqBs@eAc@u@]m@Wa@M[c@{@Yk@Wk@Ui@i@wAg@wAy@aCkAgDyCsIsBcGAEiAcDa@iAQg@g@{AoAqDUk@Uo@e@oAg@kAk@oAYm@sAcCIOOUYe@u@gAg@s@e@m@k@s@eAkAMKg@i@c@a@oDcDkBcBkAgAKKiAcAc@a@w@s@uAqA_CuBw@s@uDiDyAuAsAmAgA_AUUu@m@u@m@e@[aAq@IGmAs@k@[a@Ui@Y{@a@gGkCcJ}DcL}EqCmAmCiA_DuAyFcCcBu@yB_AeBu@}@a@}@a@{@a@oAo@qAq@KGuAu@mAu@A?u@e@{@k@y@g@SOe@[y@k@uAeA{BeBMKmB_BQQc@]yBuBw@u@eAeAeBkBa@c@c@e@q@w@{@eASWs@{@qAcBmAcBgA_Bc@m@_@k@uAyB_@m@i@_A{@yAS]GKOWMUu@wA[o@[o@mAcC[q@g@gAiAiCq@aB[s@GQ_DyHmAyCkAsCo@_Bo@}AuCcHeEcK{@wB{@qBkKgWeCeGuAgDmCsGYs@_@_Ai@oAo@aBKWg@qA]_AKWUq@k@_BK]_@iA_@iA]iAg@gBa@yAa@{AWgA]uAOq@YsAOm@q@cDG[a@mBUiAs@sDo@aDq@cD{@eEKi@y@aEw@yD]eBUiAKk@[wAs@qDu@uD}@qE[}AUcAu@wDGWe@cCe@yBk@wCw@yDwAgH_@gBWqAm@_D]_Ba@oBYwA[aB[{AYsAa@oBg@iC_@gBa@wBk@oCScAWoAi@mCg@eCQw@q@cDS_AMg@UeAc@iBMi@]sAc@gBSw@[mAc@{As@eCOi@k@gBi@iB_@gAa@oAY{@c@mAc@sAK[Ws@Qi@Uo@Wu@K[Ws@}@mCaAsCACuAaEa@oAa@iAi@aBa@iAk@eBa@gAi@aBmAoDwAeEcAyCkAgDyAoE[_Ae@sA]cAg@wAg@yAgAcDe@wAKYq@mBs@sBY{@a@gAk@_BsAiDoAaD[q@iAoCiBaEwA{CgB}DiAeC}C{GwA_Da@aA}EqKiDoH_CiFkC}FsBqEAAw@gB]u@sDeI_CeFk@oAgA}B_CyEs@qA_A_Bi@_AW_@k@aAq@eAw@kAgA}A}@oAg@s@o@w@_AiAuAaBwAaBc@g@OQSQ]_@g@i@EEa@a@eD}CgA_Ae@_@g@_@a@_@QMUQc@_@i@a@mCsBeDkC_BuAw@u@g@e@cAaAoBqBw@{@w@_AUWe@k@c@k@cAoAmBgCkAeBkAeBw@mAm@cA]i@c@u@}DoHaEwHgBgDoBsDg@aAk@cAa@w@_AeBmBsDc@w@Q[qAeCqAcC{CoFWa@aAaBk@}@o@aAk@y@k@y@W_@g@o@mAcBqBeCwCeDgDmDgAeAiCeC}A{AmBmBiBgB}A}AcAaAeAcAa@e@GIQSEGY_@k@y@GIo@eAc@s@_@u@]s@k@oAe@mAe@wA_@qA]uA[wAYsASuAMgAMiAIk@Gi@E[CWE[c@uDYgCUqBe@wDg@sEq@uFOeASsAe@gCSy@CMYeASu@y@aCc@iAc@aAc@_Ai@aAa@o@}AcCw@gAw@mAo@aAwCkEa@k@AA_@k@s@eAiBoCi@{@}@uA]k@cAkBMUi@eAe@cAe@cA]{@Ws@A??AAAUm@[}@i@aBg@cBYiAK_@[mA_@iBa@mBSoASoASqAQqAg@aDi@oD_@aCeAgHM}@?AO{@g@mD_@cCiAiHYoBq@qDa@oB]cBy@iDYgA[mAMc@Ss@Us@Uu@[_AY_Ae@sA_@eAe@mAm@{Aa@aAWm@{@mB{@gBMYc@{@i@cAy@}AmAuBe@s@?Ae@s@iAaBs@aAi@u@iAuAcAoAa@e@a@e@_BgBi@k@e@i@eAiAgAmAa@a@GGeAkAk@m@iAoAa@e@oD}DaCiCmAsAiCsC}@_AeAiAaBgB}BeCw@{@aCkCwDcEyA_BgAkAg@k@CCc@g@aGqGmPuQMO]]iSwTaAgA_DkDg@i@gDqDwFiG{DiEeAkA{CeDmDyDiBsB[[KKe@g@WWa@a@]]i@e@m@i@kAaAk@_@c@]e@Ye@]]Sg@[g@WSMo@[u@]k@Ws@[uAi@]K_@M_AY_AW}@Sm@MqAU_@GwB_@wF}@cAQaCa@{@QqAWk@O_AUg@Mc@MuAc@s@Ws@W{@[o@Ww@]{@_@[Q]O{@c@y@e@i@[g@Ye@[wBuA_@Ye@]UQSOc@]_@]]WGGSQ_@]w@s@AAeA_Ac@_@s@q@QQe@c@wAqAUSCC[Ye@c@q@o@w@q@?Au@q@eAaAgAcASQgAaAa@a@yAsAgAcAMMkAcAc@c@u@q@qAkAk@i@u@q@cA_AmBgByDmD_@]a@a@]YSQe@e@][y@u@a@a@US?AUQIIcA_AmAiAq@m@y@u@eA}@o@m@_A{@u@q@sAoAaB}A}AuA{@w@}AwAq@m@QQqBkBkDaDyCoCi@g@u@s@kAcAuAqAw@u@cA_AgAcAs@o@}@y@k@i@g@e@q@o@c@c@s@q@]_@i@k@OOo@s@MOe@g@QUq@w@o@w@q@{@MOq@}@s@_Aq@aAeA}A{@qAAAe@u@S[k@_Ak@aA[i@{AgC{AiCaBoCeAgBgAkBg@}@k@aAKO{AiC_C}DeCiEgBwCsA}BoDcGeAiBGGk@aA]m@OYU_@CEiB}CgAoBS]s@iAg@{@gByCk@aAk@aA[i@_@q@i@}@}@yA{@wA{@yA}@}Ai@_AOU_AkBYk@Q]KSWk@k@kAe@eAIQe@iA]w@_@aAo@_BSm@CEAEM[i@{AwAiEK]y@aCmEyMqIkWuAcEkDgK_@kAuBmGQg@cNya@eDaKsAcEa@oAeA{CqDyK}@mCEMmAsDM]Qi@oCiIa@qAQg@Oc@AEMc@Ss@Ma@Oo@Ok@?EQq@Qw@Ou@Os@Mm@?EOu@Mw@OcAMeAK}@AAKcAMqAKgAMgB?EGaAE{@Cy@Cs@Ci@?CAi@A]A_AAs@?q@?iC?w@@uFBkJ@mF@mFDcTBcJ@cJBgF?m@@mF?o@BkJ@mHBgJ?}@@eBD_O?cC@qE@mC?o@BkL@_E?q@?E?C?q@@iDDaS@u@@{FD}UH_]BoNFcY@mIBkK@eFBgK@kD@yD?C?cF?I@gG?S?_F?sB?wG?iE?q@?iAAkA?sO?yN?i@?gA?iL?IA_E?eD@qAAoD?YCq`@?CAmQ?gB?o@?_MAkA?}@?oG?eA?sK?mAAy@?yFA}CAiBA_CEoBAiAEqAIcCG_BAUIcBKuBIyASyC[}Ds@eIIs@IaAUmCCW{@uJM{Am@wGEm@]{DAEk@oGGo@aAaLu@eI[sDiBsSs@eIGm@a@oEIgA]yD{@sJmB{TeCgYmEgg@_Eed@UqCSyBm@qHEa@[iD]}DCO_@qEWuCQoBe@cFYiDWgCAOQ_Bc@kDQqA?EQgAYsB_@aC_@sB]kBCIk@wCQu@a@gBYoASs@m@cCSs@]mA]kA]mA_@iA_@kAUq@_@eA_@iAe@mAIQEM_@aA{@wBa@}@O_@g@gAs@}A}A}Cu@yAg@_A]o@k@aAMUMSk@aA{@sA{@sA_@i@g@w@q@_Ao@{@q@}@_AkA}@gAq@w@w@{@o@s@q@s@w@w@KKgAgAiAeAe@a@c@a@u@o@e@_@u@o@{AkAe@]e@[a@Yw@k@{@k@{@i@g@[kAs@u@c@SM[QeAq@mAs@i@]kAq@cBcAmAu@c@W{@i@_BaAg@Yw@e@i@[}A_AaBaAi@]mAs@w@g@{@g@aBaAw@g@mAs@aB_AsBoAiAs@mAu@oAu@_B_AoAu@_BaA_BaA{@g@KG{BsAiAs@qAu@mAu@}A}@kAu@}CkBkAs@aB_AkAu@cBaAsBoAsBoAuBmAsBqAuBoAsBmAaBaA_EcC_BaAkAs@qAu@e@[sBkAaBcAsBmA_BaAaBaAuBoA_BaAeCaBeAu@e@]mA_AkA}@cA{@kAcAkBcBaAaAiAgAOQEE_AcAsA{AaAiAo@y@_@g@a@e@k@w@c@k@k@w@a@m@mAcBk@{@}@qA_AsAk@w@o@_A{@qA_AqAgAaBq@aAo@}@{@mA}@sAaB}By@mAm@}@k@{@mAeBo@}@}@qA]i@mAeBkAeBo@{@kAeB}A{BkAeBmAeBmBsCgA}Ao@_A_AsAq@aAi@w@o@}@]g@kAcBoBqCIM_B_C[c@o@aAk@w@}@qAm@{@SY}@sAMS}@oA}A{Bk@w@o@aAm@}@_@g@m@}@OU}@qAm@}@k@_Ak@}@]k@k@_Au@sAk@eAMUYi@[m@[m@[o@g@cAYo@Ym@Wo@Ym@Yo@c@eAc@gAWs@Um@GMi@uAUo@Wq@o@aBa@gAo@cBYu@Sk@a@eAc@iACKm@{AcAkCm@cBWo@y@yBWo@Sk@eAoCc@iAWs@KWYu@a@gAa@gAy@{BUm@Wq@Wo@a@eAM_@KWUm@Ws@KUGMg@uAUo@o@aBYw@GQw@qBkBcFo@_Bk@{AQe@EMsAmDm@aB_@cA}@aCm@_BeAqCy@yBm@}AsAoDa@iAc@iAeAoCeAsCeAsCm@{A{@_Cm@_BeAsCcAmCo@cBeAoCyDgK}@_Ck@yAEKu@uBy@uBm@cBo@aBo@cBcAoCo@aBqAkD}AcEqAiDo@cBgB{EeAqCqAkDaCkGqAiDeAqCeAsCa@iAqAkDa@gA{@{Bm@_B}AcEeAsCc@iAm@_Bw@wBo@aBm@cB{@{Bc@iAcAoCo@cBa@eAm@_Bq@gBy@yBWq@y@wBgAsCIWm@cBeAsCoBmFEMaAmCmAiDqAmDcAsC}AgEcAsCoAkDcAsCoAmDoAkDgB}EoAmDeAsCoAmDmAkDyEqMgBaFeB{E{AgEeAsCyAaEgBaFkDuJc@oAAAc@mAQi@y@wBACyF_PgFiNq@mBe@uA{ImVSk@k@}Au@oBKYgJeWACgBeFSi@Sk@{IoVQc@yBeGQe@oD_K_@cAgB_FmJsWOe@Qe@Oc@AAaDyIIWe@qAqAqDw@wBqAqDcC_HUk@wAgEy@mCYcAQu@Mk@Mk@IWMu@Ow@Os@UsAKs@G_@SwAUmBSsBOmBGaAAYEk@Ci@GwAC{@CaACoA?o@AU?Y?U?aB@uB?QFyWBoMB_M?o@FcZ@mG?gA@oA?qB?}@@cBAs@BeGBeL@iF@kF?m@@o@@qF?qA?C@iD@_I?MBqH@eE?o@B}J@}G?m@DyM?oGFySBsR?w@@o@?o@?cABgJ@aFDgQ?o@@kF@}G@oBB{N@mI@}A@}D?U?iA@aBBoM?cC?]@}A?uA@_A?[?yAAoCCgBMuEMiEEcAK{BCg@Ew@Gu@MoBAYI}@Eq@u@oIeAyKa@qEE_@a@iEm@uGqAiNcA_LqAeNkBmS_AsJkEoe@[eD_AgKeG{o@kBmSaDi]Gm@{AoPO}A]yDGm@o@wGk@sGy@uIQqBgBoRk@}F_@aEAGs@yHiAkMa@gEEk@Gm@CYe@eFo@qG[iDO{AMsAa@uEIaAg@iFGm@m@wGCYk@aGS_C[aDi@{F]{ESqCUaEEo@U{EMuBIyAIkACc@Gw@MsBGkAi@cJWeFYkEUeESgDScDCi@SgDQsCOsCOiCOuBMoBKcAEs@QkBUwBMgAMcAOmA]qC]}Bc@yCe@gDeAkHuAiJsAsJMy@_AoGeAoHcBoLiB{Ly@wFWgB[uBCSIm@s@{E_@qCW{Ao@qEo@kEq@yEa@mCCWs@}Em@_EsAmJmBwM[wBo@iEuAyJg@cDk@eE]iCYqCQaBW{Ck@{HS}DIcBGsBKoEEgBEeFAkE?aCBuBDyB?MBkBF}BJcDJ{BFsAPmC@OLsBHaAJsALmAF}@N}A@QFw@XiDJeAxBkWd@wFXcDR{BPyBLqAV{CTkCFs@ZwDVmCLaBp@_Il@}Gj@kHReDNyCDoAJsCNaEFaBTcHHgCJsCBg@L{DB{@PkFLsDBs@By@LmDTcHPaFB{@JwCBy@D}@DgAHsC@_@Be@Bu@DcAPwFBs@Bo@Bk@DcANwEDwABg@NgEHkCz@cWTcGHsCBo@Bu@Bk@Bo@@a@HoBFiBDoABo@DqAP_GH_B@c@@SHqB?U@Q?EFaB@]@U@MJgCBw@@m@?EBs@Bs@Bs@?EBm@FkAH_BHwANgB@UH}@Dm@Fm@Dc@@IJcALeA?ABQDYHm@Hm@@GPsA?AHi@@EHg@b@iCZcBJg@f@cCZ}ABKTeAdA{EBK`AoEt@gDt@kDJe@Jc@n@uCReA\\{A\\{AR_Af@_C\\aBNo@Je@BIj@oCNo@\\aBJe@@?Ny@@Ax@wDNw@h@eCVwAZsBV{BTqBDo@RaCB_@BS?CJwBDeA@q@Bq@BeA?Q@k@DuADsDJiG@k@DkBBqBLgGJ{HBeA?WDoCDcC@I@{@BcC?m@?aAA]?]AcAAk@?SEqAAg@Co@MiC_@eF?GEm@G{@_@{Ee@qGEm@Em@_@cFg@qGK{AM{AAOOwBEm@SiCEm@KyAYsDM}AEm@Em@SiCEm@Ek@?E_@_FCe@Gu@SgCEm@K{AYuDCYASGm@QgCM{AO{BE_@C_@AUGw@OmBGu@]}EU_DOsBGu@_@iFMaBGw@AOQ{BCc@OkBEq@KsAWmDEk@WkDEk@Ek@Ei@}@{LQ}B[gEQsBiAsOIqAw@kKe@qGM}A?GYsDIcAAYGm@S}CKmASkCK}AgAcOEo@Eg@eBsU[mEQaCi@cHWkDAOOyB[aEAKu@oK{@oL[gE?AEm@G{@u@yJ_@{Ee@yGaAsMQ_CcAmNy@aLs@oJgAkO[}DEm@mAsPEk@ACg@wGmAkPMeBe@yGKaBaAqMw@sKcAiNWuD_@gFEe@Ee@[sECYUiECw@Es@KyDCm@GqBCgAAmAAeAAsAEcJAwDAsE?cDCqICgIAo@?wACgEAmC?_BA_B?}A?o@A_BAuC?gCAo@C}MAmCEyJ?cBA_BA}D?_BAmBAqFAeCAw@AoD?sB?i@Ao@?mD?OAo@AoC?G?_AAaEAoDA_EA}A?_BCsGA_CAoCAmFA_BAmCA_BAmF?o@Ao@?w@?eCA_B?cCAyCA_BAoC?o@Am@AoC?_B?YAsHAmF?W@aADsD@OD_BBo@@c@By@Bc@FqA@WFaAFkA@MP}BDg@VcDD]N}AP{ADWBUHm@BOd@gD?El@mDDSDWTkAP_A^gBjC_LdAmEBKj@cCf@wBRu@vDaPDQLk@|AwGjB_I|@yD@EZoAb@kBp@yCJa@BIhBwHdAsEXmArAyFdCmKDMlAgFxHk\\hBwHNi@j@aCpBwIdCmK`B{G~AcH?AJa@Ni@dBqHLi@@?h@cCDOd@qBf@uBZsAj@aCbCgKNi@p@uCr@{CLk@XiApAqFd@wBvAcGl@cCnIi^nDiO`AaEZqAx@mDf@uBPw@\\uAZwANk@j@aCZuANk@fA{ERw@FWZmAZuANk@ZuAj@aCj@aCh@_C\\wALi@pAqFx@eDpDsOvJ_b@j@aCNi@Lk@R{@p@mCnFiUzGoYnO}o@`AeE`B{GtA}F~AwGpAuFj@cC~@{Dv@aDh@{BJc@t@aDb@kBJ_@FUx@mDz@{Dv@{Dr@aEh@aD`@kCf@cE`@iDRoBVoCr@uH\\mEj@yFj@}GX}CNyANuATqC?AZwD?ADa@Fw@XkDH}@?AJyAHgAPsCJuBVwGBwADkCBy@?e@@o@@aB@qA?gBAs@?c@?I?y@Ac@A_CCeC?WEmC?_@Ao@GmC?OG}CGiCCwAAwA?CEmCAw@EgCC_BAq@Ak@K_FCmBEuBGaDIcE?CAi@I_EAi@EwCAk@AEAi@IqFA{@Cy@?s@?aA@q@?M@mA@A?YBc@Du@FeA?IDg@B[Hu@@KD]@MFa@Hg@BSLs@Fc@DS\\{ATgARy@X}@@ADQHU\\_A\\{@l@wAzBkF`@_AXs@P]`@_An@eBVu@l@gB@Ad@mA?Az@sB@C`@}@DKRa@dBgEtAcD\\cAT{@J_@Li@L}@D]@AHo@Hs@Bi@JoB@}@@w@?AAwACuAGoAOuAOsAYaBMs@Qq@Mg@Ok@M]K[Yu@_@}@[q@_@q@QYYc@CEo@{@c@i@_@_@m@g@oFuESQmDuCo@i@s@m@aBsAm@g@MMc@c@k@s@w@iAi@{@_@y@OY?Ag@oAQg@CKK]Qo@YmASiAQwAMsAGy@Ai@C_AGcCAe@E_AIgAMgAIk@EYIk@Om@Ms@_@mAEQCEEQOa@CEa@cA]q@Qc@Wi@Ue@?AUc@GIM[m@qASk@a@kAMe@K_@CIMg@?CSy@O}@My@E[CQGm@i@iECYMgAe@iDk@uEGs@Gm@_@wDGg@[oEA[KoBG_CCmACcBA_C?aD@kA@o@BoABgAF_B@e@Du@DiADs@Hw@Ba@F_ALyA@AJqARcBHq@\\eCT{AJk@f@kCXqAPw@h@uB^sA\\oAb@}Aj@cBXw@Pi@jAcDpA}DL]`@gARm@H_@Ty@j@sBLe@Rw@dAcFVsARoAXgBTcBb@}DTeCV_DN_CF_ADw@XkEPsCHsAd@yGJcAHy@Jq@LaAHk@RoAVuA~@_Ep@eCt@}Bv@qBVo@l@qAHQh@gAr@oAd@u@`@o@p@aA`@i@n@w@r@_AZ_@^c@dBqBnA}AjAwA`BeCv@sAnAcCtAcD^cAdAaDX_A^yA^cB^oBb@qCVgBFi@\\{BT{AVmBXgBRwAJm@@IPmA^eCLk@Jk@Jk@ZuAXkA@INi@DMH[Le@@ANi@Pi@L_@f@wA?ADKJYTk@b@mAFQTe@r@}Av@_B`BuCZg@Xc@V_@vAqBbAoAt@{@FIbAeAbAcANO@A^_@rBmBv@s@@CXWBCpBiBBCVW`@_@\\[t@s@\\YZ[FETUb@a@Z[t@o@`@a@VUDEpCiCVU|AyATSFGZYnBiB~@{@VU`@a@\\[VUZ[b@_@\\[Z[vAsArCiCTUDEVSDEjCeC\\Y`@a@nBiBZYz@w@x@w@\\[x@u@x@w@b@a@r@o@z@w@pEgEVUvCoCVUb@a@nAkAz@u@Z[POl@i@tAsA\\[jAeAJKtAqAzDoDl@k@z@w@v@s@z@y@n@o@`BaBHGPS`@c@VWJKlByB\\_@lA{APUHIr@_AX_@BCT]X_@x@gA~@uAFIVa@v@sAh@y@Va@Va@Vc@DEh@_AfAkBfAiB^o@R]Xc@Vc@p@gAVc@~AkCVc@DIPYTc@Vc@v@uANUVa@xAcCZi@@?Zk@t@qAd@y@v@oAVc@Va@BCj@aAv@wAJQxBuDfDwF`A_BrDmGhPsXpCsEhD}Fbl@}aAnBaDnCsEvHoMr@kAhJyO|CiFVa@rAyBzOcXt@oAh@}@fAkBVa@~D}G~D{GvBoDVc@vBqDnCsEfAkBnBaD^q@h@}@`BqC~AkCvHmMVc@l@eAfDyFVc@T_@Xg@xE}Hn@eATa@`BoC?AvA_Cv@sAj@aAr@kA`AaBn@eAbAeBt@oAlCsE~D{GlB}CHQhDyFnCuETc@n@eAVc@Vc@n@eAVa@?AVc@n@eAn@gAn@eAhDwFVc@~AmCBCbDsF|GiLvA_Cx@sAd@w@`@q@~AmCfAiBVc@~AmCn@gAfAiBfAiBTc@Vc@~AmCfAiBt@oA|CgFhDwF~AmC\\m@`AaBn@eAvE_IdEeHrBkD|BuDFMBCJQtBqDn@eAVc@Vc@DGP[@CdDsFnCuEfDwFnCsE~EkIXc@lCsE@ChEgHz@yAZg@R]Vc@xFoJdAgBrAyBjFaJ~@}AtFiJjVoa@d@w@pBiDnEsH~DwGx@uA|AmCb@s@t@oAp@iAlD_G~B}DrAwBdAgBLUfBwCfAmB^m@nAcCr@sA`AqBp@wA^{@Ti@tH_QR_@dAgCpDkIxFqMh@mApCoGf@mATe@nEcK|BiFRe@hCaGVk@dAeCdBwDN_@jBgEh@mAfB_ElGyNbKuUdA_CRe@|BiFvDuI|DcJ~@sBzBiFfEuJd@cA`@{@\\s@Zo@JS^s@Xg@j@aAh@}@^i@Zg@vAkBh@q@RUdAkAf@i@HIl@k@hAcAr@m@dAy@v@i@`@Y|B{AzCsB~@o@zCsBv@g@tCoBb@[b@Y`C_BvA_A`BkAbAy@n@i@d@c@v@u@bAiAbAmAh@s@T]~@uALS`@s@Tc@^m@N[b@{@p@{A@AVq@`@cAd@mARg@f@oAjCwGTm@~@_Cj@yAFO|B{FPg@FOJWx@sBb@eAh@wAlA}Cf@oAlA}Cx@wBx@qBx@sBp@gB~@}Bp@aBfCwGL[zAuDl@_BjCuGd@mAf@oAz@wBRg@r@mBXq@v@yBb@qA\\iAPo@Nq@VoAReAD[Lu@Hq@D_@LiABSFy@HoA@[FqA@a@@k@@{@?wAAkAEmBOiFI}CCcACcAA}@Ai@?e@?E?u@@c@?K@_@@e@@c@@]@YBi@@S@UDe@Ba@?CD_@Fm@Hu@Hu@Hg@Hc@Ls@Ls@\\gBdBiIPu@Ha@Lk@Jk@Lm@l@qCp@cDZwADSFWLk@f@}BR}@H]Nk@\\sAn@aC\\qAPm@XeAv@kCp@}BPi@Rs@bA{CL]l@eBVs@L]JY\\cAL[d@oABENa@Rg@f@oAf@mARe@FOJWTe@Rg@Re@Re@@A~@qBL[Zo@Vi@Ra@`AoBhBoDnA}Bb@w@JOdAkBHKd@w@Xc@n@eAVa@Xc@Va@JQf@s@z@qA~@uA\\c@n@_A`@k@h@u@PSz@kANOZc@`@e@j@q@h@q@Z_@r@{@p@u@`@e@x@{@p@s@`@e@\\[vAyAt@u@x@y@rBoBZ]\\[v@w@^_@r@s@dCcCt@w@v@u@Z[tAuAVWvAwAt@u@`@c@\\[v@y@d@e@p@q@x@w@tAsArAuA\\]x@u@nCoCdIcIn@o@|C}CdAgA\\[\\[v@y@tAsAx@y@hAiAvDwDbBaBfAiA\\[Z[xFwFlCmC\\]h@k@~B}B^_@dHeHtGsGxIuI`G_Gn@o@tDuDdCcCbAcAt@w@|C}CdAaAdGeG`@a@VWzIyIfMeMrGqGtDsDv@w@xEyEfAgAzD{DjAgAlJkJ|A}AlMiMt@u@HIj@k@jAiAhAiAbBcBfPcPNOPQz@y@lCoCb@c@^]bAcAZ[HGLMTUvBwBhCiCrDqDPS|B{BPQHI@APOBC~@aAz@y@t@u@xAyAPOZ]JKLMLMf@e@r@s@t@u@t@s@^a@x@w@bDcDfCeCtEuEbDaDfMeMtAuAvBwBXYxHwHxCwCr@u@rFqF|D{D\\]jDiDx@y@Z[RSxAyAzByBr@s@vFsFnDoDdAgAt@s@vAuAb@c@n@o@@AZ[pBqBTSVYzCyCrCqClBmBPQhBiBlAkAZ[\\]@AnBoBxBuBfBiBb@_@lCmC`F_FnDoDrBqBZ[xGyGrCoCtGsGr@s@j@k@nAoAt@u@d@c@Z]lAkAb@c@^_@t@s@xFyFt@s@nBmBJMhBgBt@u@TSb@c@`BaBfBeBTUpDqDpFoFzEyEv@w@x@w@|@}@t@s@`@c@r@q@hEgEdBeB~B}BxCyCnCkCzB{BzByBlCmC@A|D{DJKhEgEZ[|@{@lBmBx@y@nCmCxEyEr@q@PQZ[\\[n@q@dBeBfAgANSp@s@b@i@NO^e@r@}@`AiA`@g@\\g@r@_AtC_EBEfA}ADGp@}@f@u@x@kAfA{ArAkBlAcB~BeDpC}Dr@aAX_@xAsBh@s@b@o@lCuDd@q@fCmDPYX_@r@aAJQLO~BeD@AV_@rAkBRWrAoBlAaBr@aAn@_A|BaD^g@Va@t@cA|AwBFIXa@X_@Va@f@o@JQr@aAXa@Xa@p@aAXa@X_@Xa@X_@jAcBDGRYX_@Xa@^g@j@{@pAiBrBsCd@q@nAeBJOpAgBn@{@r@cAV_@@?dBcCr@aAXa@lEgG~@qADEz@mAPWbAyAhA}AlEoG`@i@r@cA@?rB_Dz@wA?AdAmB`@s@z@cBv@aBXk@jAwC`AcCzAsElAcEj@_Cp@mCXuADQ?ALk@Je@l@yDF[XwBT{Ab@uDLuAHcABWBWB[LoBLyBFwAFgA?IDyADyA?SDkB?M@m@?I?sA?}A?A?o@?]AoB?KCaCA_BCyCAqACoC?m@Aa@?MAuBAgAC}A?QAmA?m@AcAAkAAaBA]CcC?o@Ao@C_EAk@?o@A_BEoFCeCCwCCaBAeC?C?uB@W@}A@o@@o@?ODkA@{@Bc@FyA@KFqADm@@MFm@Dm@Dg@?GFm@B]ReBJeAD[D[^mCLw@Lm@V{AVwAXoAn@yCJc@Lm@t@mDd@{BvA{GTcAj@mCt@kDReAZyAVmABKLm@ZyAFUx@wDXwALk@hAkF\\cBH[?CTcAbA_F@ETgA\\iBb@mCXoB@ENmAJ}@V_CNmA?GFs@NcBL}AB_@Do@@MBm@@MFkA?C@SDkABkADoC@cA?_B@eBAsA?KAcBAY?EAm@Ao@?c@CaAE}AGeBEoAGgAC]Gw@GaACQG}@KkA]_DGe@Is@Im@E]UaBQkAUqAOw@i@iC}AeHW_AUaAGU_DwLES_@uA]sAWaAGS]sAOm@Ka@Qs@Oi@m@_CMc@a@}A]sAOk@i@wBa@}AwAsF_@uAOi@gAkEm@wBQo@U_Ag@qBOq@WmAi@gCWqAg@kCi@wCMu@SiAGc@YmB]}BOgAGe@W{BUwB]aD]eEUuCAGIoAI_BIyAKmBIqB?CMaEOoGCqAAu@CcF?uA?iE@w@BwBBkB@y@FwBBoAFyBFqAFuADw@PiDRaDNyBPqBLqAPmBXuCTwBTsBXqCl@yF`AmJj@oFHm@Fm@h@eFViCl@}FnA_Mt@iHZgDv@cJb@sFP{BTwC^eFb@aGLqBlAmSHyALqC@EVsFl@cNj@eNJeDDoA@i@Ba@Bm@JaDNoFDuANgFTqITeKFgCF{C?CPmIRsLRaOJaIF{HDqFFmHJcOHaO^ks@BmFFmMBmEHqJ@gDDqFBcFDeIF}JD{IFqIZim@`@ct@LiURm`@LcUN{VFkNFyJBcCDcI?{@LsSLcWHiM?o@DyFFgL@o@Ng[LuRDkG?_B@UDkKJqQBwFHePBcBdAmiBBcFj@g`APuZ?ONiYPuW^gp@BoGHoL@aBBuEBiEDmJ@sAJoPFgJFsKF_MBcFLmS@mBHcOHoL@aAHyKXkf@Xci@f@uw@^sp@Vag@l@ebAf@cw@D}ID}GNsXd@iq@@o@HoM?o@l@gaAP_ZPkYHyMDyGb@kr@Rm\\h@g{@\\wg@JaPV_d@@e@LgTt@skAhAkcB`CarD`@ok@Rg[Xec@Tu\\?QDiF@uBHsLLkPJ{QXw_@N{THsLFyKBqDNgRJiQL_QHsMHyJFsJ?_ALgQJiN?[F}IJoNNwTHuLDeFDeGF{IHqLHyKBcDH}LLaSHwKDaHHiNN_SBkDb@}n@@sC@w@?_AF}G^{f@@sAhAyaBVu\\PqVPkYj@kw@BkERqY@{@Xkb@HuKFeGD_HDcGJwLDcG@_ALyQB{DBaDBoG?u@D}GDiM?w@@qCBeG@oC@wBFuSBmL?uE?c@FqSH_a@@_A?qD@sC@uB@mD@_FD}H?sC@oA@kGDqL@aHDoNDaQDeQ@iFBcG?sA@yA?e@@mHBcJDoM@aHDmN@aIB}H?oC@iFBeFBaI@wJBcH@kE@mC?a@FuK@u@@eG@mDBqF?SBcH@iE@mDBcI@}IBiE@kE@oBBsCDeFHaHFiEFkEDmDFaETgRDgGFmN@gF@{@@cG@_G?}@DgF@kD@kEB{J@_D@wE@gF?cB@aED}HBuJ@_E?qCDkL?s@@oB@aHBkD?Q?iA@_@?oA@kG@kCB}G?w@JwW?iC@}R@yBHsLByKDkMBwIBeIB}G@uA@mE@}D@yD?wABaHBaHB{JDoMB}IBaH@iE@yD@aD@mE@qD?SBmEB{JDeQByJPe`@B{GH_\\@uDFgSBkI?[FwO?s@BeMBqHByHDsN@uE@gHBaE?sABeG@mE@{ED}K@cFFkTB{E@qE@oA?}@Tej@HeRJ}V?yW@iDAaEAoDEsC]aMGkBUsEWmE]wD]gEa@yDY_CS}AmAuIUyAa@yB}@_FWwAcDmQ_FmXa@_C{DeTeDyQa@_Cu@eEqFiZ[kBi@sCiGy\\aF_Ys@_E[gBqAiHiFmYMk@WyAKk@q@qDSmAiGu]_AiF}Fu[yDcTwAcIMk@a@_CeIyc@w@qEMk@oM_t@m@mDq@wD]gBKk@Kk@c@eCiAiG{@wEkAoGgAgGKm@Ow@G_@EQw@kEKm@Kk@mBkKMm@o@qDc@eCMk@Kk@{@}Ec@eCYwA{@}EKk@Kk@Km@aBaJKk@Km@WwAKk@}@}EWwAo@qDKk@e@eCY_Ba@}BSeAaAoFc@eCq@oDEUEUc@aCo@uD[aBSoA[aBg@iCYcBWqAc@eCW}AYyAiCwNwA_IEWESW{AY{Aq@uDW{AMk@Km@Km@kAqG_AmFwAeIKk@c@{BaEeUkGu]WwAmBqK_BcJMm@G[yAgIi@qCu@yDa@cB}@uDs@mC[mAq@}BSm@c@yAIUIUI[sAcEEKM_@CEkAgDEKKWCGe@mAeAeCiAkCQa@mB_Ey@aBEIUc@IO_DyFuDeGwCeEuEqGOUgBeCe@o@c@k@GIgFiHKKW_@m@{@mCqD_@i@m@y@kAcBmDyE_B{Bk@w@a@k@gE{Fg@s@kDyEq@_AuKaOaGiIU[aF}GgA}Ai@q@y@iAyB}CCCUYW_@eDqE{CaEGKeE_GmEgGu@aAmHeKsCyDY_@mAaBq@aAYa@eB_CACY_@gBcCoCwDkCqDYa@}DqFgRkWuLqPiBcCiA_B]e@iA_BkBeCeBcCeFcHsBwC}@sAuAwBqAwBAEgAiBeAmBoBwD_BgDoAoCuAiDiAmCc@oAe@oAyAmEoAwDGUeFyOQi@gAeDqD}KOi@c@qAQi@Qg@mAuD}CqJuBuGwBsGa@oAOg@GOQi@i@cBQg@q@uBeBmF_@iAg@yACImAyDSk@]gAkAsD[eAw@sCQo@ACGY{@_Eo@yDWsBe@wEO{BOeCG}BCsDAq@D{DBwA@q@?]Bi@Bi@JeBLgBFu@Fo@BWD_@DYDe@He@Hq@Fc@Hq@d@iC@AH]He@Lk@R}@Nk@Li@Le@Pk@J]Lc@Rm@Ro@J]Na@Rg@Xu@N]j@sAp@yA`@aA\\u@f@gAVo@`@w@Zu@n@uAf@kAd@eAd@eAhAeCxBcFP_@DIf@kAx@iB~@sB~@sBRe@rCmGh@kALWpAwCt@_BdAaC`@{@Re@Tg@jAgC\\w@Re@|AoDHQnBoE`@}@Tg@Re@`@}@fA}BTi@~@uBRc@Tg@Re@dJmSrAyCTg@Re@j@mApCkG|D{I|@sBh@kADIxB}ERe@Te@rBsEHSjFkLP_@Rg@fHyO|BgFTe@|@sBz@iBjFoLpEaK~@sBRe@fDsHTe@Tg@zFmM|BeFTe@dH{OTe@Rg@hB_ErCmG|@qBpEaKjBaE|FgMhBcEh@mAtFcMlFqLrAwCp@_B|HeQ|AkDhBaE`AuBlKwUrAyCn@yAjIyQrAyCrHsP\\s@rAyC`CqFx@iBfG_N|C_H`BsDdFcL`EaJdA}BhC}FfGaNdDmHXo@N[JUzDwIfDsHTe@xByEHOnCiGdDqHtBuEhAsCx@yBf@sARk@dAeDdAsDnAeF\\_BZ}A\\gBTqAZkBT}APoATiB`@oDLqAHaALsAFeAR}CTwET}E|@uRBo@pAiX|Diz@ToFtBgd@dDyr@f@iKBm@bAaT~@cSp@eNpBub@Bo@Bm@hCui@hFqhADm@d@yJBm@dAaUn@uMlCek@tKo}BDgAFsA`@yIDq@f@wKX_GBe@Dw@?ALoCViFZyGLuC@i@\\yJRsGNeFHeCl@gRb@eNDsAJuAJqALsAPqARmAVuA`@oBZmAJe@@Et@wC~FaVLi@DQhBmHbBaHbBiHJa@lA}FJe@Jk@`B{HDQpBoKnAyGtAiHnG}[dAmFrBoKpCsNnBaKFYr@qDnAmGvDyR|AaIH_@jCgNpF_YbLel@fMyo@`BkI^oBLm@jAgGhF}WxLin@dD_Qn@wCZuALg@ZqAXgAVaAj@qBDOV}@@GNe@?CPg@tAiEfAkDPg@|BiHtC}I\\eAh@aBvE_O`CoHhAmDlAsDhAmDdGcRbCyHFQvAmEFS|@qCjB{FpA}DvAoEd@yAFU@?BIr@yBn@oBz@qCPs@`@sA|@aDv@cD\\uALk@H_@ZuAZyAx@iEt@mERwAXgBJu@@EPoARaBLeAPqARwBLiA`@{Dh@iFv@oIFq@tBkTtHgw@Fo@rBeTtBeTb@wEf@qEX}BRyAPyANaAL{@VaBN{@PcAf@sCh@oCVmAb@qBbAoEd@gBn@_CdAuDdC}ItCeKj@oBDONi@Ni@dBeGbEaOJ[Ni@~@cD`AmDxAoFbFkQvAeFhA_Ef@gBpBgHbHyV@?Li@`B}FNi@Pi@pC}JdDqLZkANi@b@{ApAwEHa@~@wDf@wBbA}Ej@uCf@sC`@iCLu@Hk@Lu@ZaCTgBTqBJ}@BUp@}FJ{@Fm@`@wDJ{@LqANsANmANmA?ANqA?Ej@aFFm@vAiMFo@ZkCFo@PwAFk@VaCRcBDa@r@sGzA_NBWVwBl@wFx@mHn@yFd@iEdCaUvAsMP}A`@iDPoAL}@^iCZmB@EHk@TsAN{@XwA|@qEr@uDJi@d@_Cl@_D^kBZ{AJk@f@eCBKF_@fAqFDU@Af@kCv@wDfB_JfAyFJg@fDaQ@CdCkMNw@lAiGtAgHdBwINq@rAaHj@wC^gBLm@|C_PdEySb@uBF]lAiGrBoKZ{Ap@kDLo@Pw@zBkLvAkHpAmHfAsGv@eFbA_HxA}Kv@uGd@}Dv@eIXwC^mER{Bf@qGXeEV_EJ}AXeFPuDJeCLsCPsDLgDDyAFaCNmJHgEDcEB_D@oD@cC?}G?m@AqAAiEA_B?q@CsDCeBAmBEcC?i@Am@CsAMeGOqFImCMwDMsDGyACm@CWQyDQcDCi@_@mGWqDe@wGu@aJe@{Ea@_EOwAa@yDw@}G[cCQwA?Au@wFQgAg@oDQmAo@eEAG{@gFq@_EEOuB_L_BcI_AmEu@eDu@cDe@iBw@gDs@oCe@eBQo@{@aDGUGSOi@Oi@YcAo@{BoBkGsAgEsA_EoAsDSm@}AiEGQKUQg@Uo@u@qBQa@sAkDaB_Eg@qAuDuIm@sAKSWm@aBoDiDgHuAoCKUk@eAqBsDMU_AeBCEiAoBIQe@y@{@{AmAqBQ[aAaBcDgF_AyA{BeDkFsHyAsBoBgCcB{BsAaBcBwBcBqBqA}AeDuDiDwDgAmAiBiB[]iDkDMK?AcC_CgD{CkD_DiEsDqCwBIIkA}@gA{@eCkBQMc@_@u@g@e@_@g@]y@k@aAq@aAq@cAo@OKqGeEcAo@A?c@YmGoDkCyAQIoDqBgCwAoAs@oAo@w@e@e@Yi@]a@Yk@a@_@[QMe@c@_@_@c@g@o@u@a@i@a@g@U_@S[MSS]S]Q[MWMWg@aAg@gAu@{ACCq@yAu@wAaAsB[k@Ue@]u@cAsBoAeCmAgCqAkCsAkCQ]kAcCgBqDcAqBcAsBaAoBoAiCcAqB[m@MYe@}@e@cAe@aAiA}B[m@q@uAq@uAs@wAy@aBSc@_CaFuEiJmEcJgBmDkBsD"
                            },
                            "start_location": {
                                "lat": 38.6447049,
                                "lng": -121.3845307
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.4 mi",
                                "value": 672
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 39
                            },
                            "end_location": {
                                "lat": 40.7221441,
                                "lng": -112.2232966
                            },
                            "html_instructions": "Take exit <b>102</b> for <b>UT-201</b> toward <b>2100 South</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "}epwFj__lTASAEEKO_@KWEIQe@[u@_@_AOa@Wm@Um@w@oBYs@k@wAYs@KUGWGSGWG[G_@CMASCYAOASAO?MAK?O?Y?U@S?A@[BWBYBYn@cFFc@"
                            },
                            "start_location": {
                                "lat": 40.7204651,
                                "lng": -112.2304589
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "16.4 mi",
                                "value": 26360
                            },
                            "duration": {
                                "text": "17 mins",
                                "value": 1004
                            },
                            "end_location": {
                                "lat": 40.7241921,
                                "lng": -111.9189609
                            },
                            "html_instructions": "Continue onto <b>UT-201 E</b>",
                            "polyline": {
                                "points": "kppwFrr}kTLgAD[BW@QDe@BS@c@@_@@[?c@Ae@?}@Aa@C]Ce@Ee@Gi@Im@UuASuAQiAQmAk@wDUcB{@gGKw@g@oDiAcICUuAsJe@uD]aCQuAOmAUoBMy@QqAWiBGc@}@oGGa@AEE]KaAQoAM_Ac@cDU{BSoBI{@QyBWyCIoAGq@[cF_@wFe@mHQiDKqCImCIgEASEmCAo@GiCOiJGyDGaDGOIiE?a@IyEA}AOyJQkKKgHCcBAw@McJCm@EgCEqCEqDAuA?uA?[@oABaCB_AFaBFkBJuCL}D@MB_ABk@@W@UF{@B[Fm@Dc@@IFg@PoAFa@BOLs@Ns@Rw@b@cBf@{AHYN]tA}DN]@CN]N_@Ti@l@sAVi@JUP[\\o@BELUVc@BCh@y@BEB?D?DADENU\\e@Xa@|@gA^c@p@u@Z]b@e@dAmAx@eA@CJQDGJQJQHOXo@Rg@N_@FSBIL_@?CPq@DUH]DY@CFi@Fe@Fq@@ADo@B_@JkBFuABc@L{BDq@F{@J{@De@DUBWF]FWFa@FWNq@Rs@@CPi@J[^iAd@wAZ_AZ_A^eAJYPk@ZeALe@P{@DWDQFe@Hs@Hw@D}@Bq@?m@?w@?MAu@Ce@Ey@KmBGiACwAA_A?q@@{@Be@BY@WBUDa@Jy@Lw@Ha@b@eBV}@X_A`@sAd@{A`@yAJa@R{@TeAF[Ha@V_B@En@eEf@wCN_AL_AJy@BKJoAHu@Bg@LeBNoBJwAB]Fm@Hg@j@eFBKZuCLmAHeABe@Bk@Bk@Bq@@iAAk@?w@CsAI{AIsACSSoCCYSsBCUOuAOoASsAEWE]q@cEYcBUmASsAc@mCCQG[E[Gc@Ks@MsAOyAOwAKgAMiBE{@C[AQCo@A[GaB?OCm@A[CwBAi@?o@AW?yC?iB@mC?gD?_B?aB?e@?yH@iD?wF?_P?e@?kI?K@}A?mA@{@Bw@BaADqANeEHiCH}ARqCv@_JJoADy@Do@?SBaABiB@oB?}A@aFAiAEsAGuAIcAKcBGo@Gq@OkBQoBw@_KMeBGu@M_BEm@?MCcACwA?sA?]?iJAkLAsD?}HAiO?iCAwB@uB?q@?kC?wC?e@AuF?iD?gFAmE?mA?u@A{C?gCA_J?m@AkA?WCsBE_BCs@?EEs@A[AYCg@E{@Gw@GgAI{@Ek@C]U{BMaAIq@QsAQaAIk@WwA?EUiAQy@]aBWaAYiASy@Uw@Sq@Qk@Uq@Qi@s@qBaCiGaBgEQg@o@aBIUaDkIkAaD{@gCg@cBeAuDWkAS{@_@kBOs@G]UqAGe@WgBKs@Y}BKcAI}@QwBS_DGuAC}@Aq@E}@CaACaBA{AEyC@iFAuB?aBAqA@oF?eF?oCCwF?u@Ag@?eCA{DA_LAk[?aGAyI?_G?cG?g@?o@A}G?iIAe@?oL?qJ@mS?yD?mF?Q?aD?{C?_F?M?_Q@sB?}T?cBAkH@ua@?o@IqHAcAGeCE_BK_CCq@GqAIqBKwB?IEo@Cw@IcBIiBGyAIcBEeAGoAKuBKsBCw@Cg@Cq@Aa@?GCk@Aw@Ay@Ae@?i@?uA?u@@_ABuA@q@By@B_ABi@Bg@@a@Be@B_@@[B_@?ADc@HoAH}@Da@De@JiANwAb@aEFw@DY?GBUB]B[B[@Y@[@[Ba@@Y?]B{@?sA?]?i@A{F@oHDeEBeA@UHoBDy@JqBF_AXoDNuALwA@KDm@n@{HFq@^wFLoBXcEBUNmBPeCPsBTeDBYPaDFiD@_ABqC?s@CqFAm@?k@?o@?E?e@?G?{A?o@AoBAwCAo@AuCGeF?YAS?o@A}AAo@?{@CqA?o@A}@AiA?u@EsGC}GAo@CmEAmDEwJAcB?MAI?A?_A?e@C_CA}E@wAL{G?EFeE"
                            },
                            "start_location": {
                                "lat": 40.7221441,
                                "lng": -112.2232966
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "1.2 mi",
                                "value": 1998
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 76
                            },
                            "end_location": {
                                "lat": 40.7178255,
                                "lng": -111.9011861
                            },
                            "html_instructions": "Take the <b>I-15 S</b>/<wbr/><b>I-80 E</b> exit on the <b>left</b> toward <b>Las Vegas S</b>",
                            "maneuver": "ramp-left",
                            "polyline": {
                                "points": "e}pwFndbjTAm@@m@Bo@?AFkC@i@?C@]@aABuB@W?m@?o@@o@?u@CgCA]IeDOsD?ACm@Co@Co@Cm@?ECi@Am@EcAIwBE_AEk@?ACm@?GAg@?s@Dq@Be@F]Fa@N{@La@J]@CVq@P_@BELYV]j@m@RQ\\WBCZQJGRK`@ORGREf@KzACXAXId@E`@Eb@CjAKb@EdBG^E^Gz@WRI?ATKx@g@LK\\]`@g@V[P[Tc@LYN_@@CDKLc@Jc@@EBMDS@IDWBU?EDY@S@Q@O@S@k@?a@Ag@IsB?C?CAA?CAEKS"
                            },
                            "start_location": {
                                "lat": 40.7241921,
                                "lng": -111.9189609
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "4.3 mi",
                                "value": 6978
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 241
                            },
                            "end_location": {
                                "lat": 40.7124754,
                                "lng": -111.8202668
                            },
                            "html_instructions": "Continue onto <b>I-80 E</b>",
                            "polyline": {
                                "points": "muowFlu~iTGgBKwCAi@EkAOsEAo@O_FAM?E?u@?KAeH?s@?Q?a@?cB?yA?oA?O?}F?{B?I?C@mBAmC?gD?M?K?gB?C?a@?kA@wH?U?wB?mC?kI?gB?E?w@?iH?mC?kL?o@?mC?_@?A?OAo@Am@?OEgEAU?]G}BA[A[GwAMaC?AO{BIgAGo@?AGo@AOEm@I_Ao@cHO}AM{AEs@Eu@GuAGkACcAE{AE}BAs@?A?A?s@AIEsD?m@EoCCmCAm@IkIIyIAa@CqDC{AAmB?}@AwBCkL?G?A@GA[?A?A@{A?C?sB?eA?}D?sE?_CFsI?CDuABy@@q@DcBHwAHsAF}@LiANsAVqBXgBJq@d@oDLy@j@iEb@aDTaBHe@nByNXuBP_AXsAR{@Tw@Pg@Z{@l@{A@CBInA_D^_AZcAHWHUPq@Rs@@GJa@FYTsADQVuA`@_Cl@cDX_BJi@TwAt@eEzBaM~AkJDSDYBI?CLo@d@uCNmAH{@F}A"
                            },
                            "start_location": {
                                "lat": 40.7178255,
                                "lng": -111.9011861
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "428 mi",
                                "value": 689085
                            },
                            "duration": {
                                "text": "6 hours 11 mins",
                                "value": 22257
                            },
                            "end_location": {
                                "lat": 41.11333570000001,
                                "lng": -104.8571346
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Entering Wyoming</div>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "_tnwFt{niT@o@?s@Ay@Eo@C]AMIm@Mq@YiAOg@MWYm@a@w@w@qAmA{BUc@KUM[Qc@Uy@Qy@M{@Io@Ew@Co@?m@@iADaBDmCDiCNmIB_A?_@@WBgADsAHsBHkAD[BWFe@V{A?A?ABODQ@ED[F[Je@Ns@Le@ZkATw@zAoEHUx@_Cb@}A?AVcADMfAcFNq@z@{Dv@iDH[@CVoAHi@BO@IFe@Bc@@Q@S?K@Y?_@?C?SA[?CCe@?CASAEEi@Ig@Ig@Ia@CQGYCQAGGWk@eDIc@Im@G_@Ga@I_AEi@Aa@Ck@AU?UAY?]?eC?U?Y?S?GAq@AOCg@Eq@CWCW?CGc@AICO?CO_AWkAQk@Qm@Wq@[o@O[yBgEkA}Bk@gAGKeAiBg@q@Y_@SUWSe@c@_@Wm@]IEMG[M_@Mi@Q_AUmAU_AUUIQGUIMGMEKGs@c@WOEEMK[WWWQUm@w@Yg@Yi@Qc@Se@CIKWEQI]CKI[Os@UkAM{@WuAQ}@S}@Mg@Me@IWOi@Uo@c@kAeAaC{@yA?Ay@oAa@m@aAuAQWYa@y@mAs@eA_E{Fk@y@oAiBa@q@KQMUGOKSUg@Oc@U{@Qo@Ki@I_@COQgAUiAG_@GSQw@Us@ACYy@Yk@We@]k@Ya@UYk@m@QQ_@a@aA_As@u@QWk@w@Sa@Uc@Qc@Oa@Qk@Qo@UgAKe@Ga@O_AM_ASkAQ}@_@gB_@sAWy@M]Wq@Sg@Ui@e@_Aq@mAuB}C]g@a@q@OYWg@Se@Se@KWEOEKIYK]Os@I_@Ig@Ik@Gi@?AIy@Ey@Cw@EgAEo@Es@E]ASEYE]Ik@Kk@SeA[sAOq@EWKi@Ks@Ee@CMEm@Ey@GuBIkBGuAGg@CWO_AMq@Qy@Sm@Sm@[s@Uc@y@uAk@q@MOy@u@e@_@e@]AACCcA{@MMMM_@c@OSKQU]U]S]M[[k@oA}BMS]i@_@g@]a@_@]a@[s@k@e@Uc@Ua@Oc@KmA[kBg@i@Qw@[_@Ua@[c@_@]]_@a@S[SWQ[Yk@Ug@M]ESUu@Me@Mo@Ii@M_AEe@Em@Eo@AY]kHEs@C}@Cq@G_BGyAIcCASCc@YoDKq@Q{@Mm@Mc@K]]cASa@GOMYWg@Yg@w@mAq@eAWe@Yg@Q[[q@[w@e@mAe@oAcAqCmAiDwBcG{@eC}AgEk@aBQg@Si@IYq@wBk@{AQg@O]O[_@o@Wc@_@g@e@m@i@k@i@k@m@o@g@m@s@w@USa@e@a@g@k@u@SYMSKSMYQ_@Ui@Sq@Qi@Q{@Mo@KaAK}@Eu@Am@?i@@k@?_@Bg@Be@BYDa@Hm@Hk@F_@?ABGTcAPg@Na@L[LUTe@R_@t@mAfA_Bt@eAr@iAJSP[^u@Pa@\\gAd@aBZgAf@wCTmCD{A@aB?kACeAE}@k@yGCg@K}AEmB?QAwADgABm@Ba@FaA@SNmAJw@DUTmANm@Lg@FOJc@Vs@Pe@b@}@x@_Bv@mAl@aAn@{@p@iAVc@LWh@gAXo@Zs@Na@BIJWNg@La@DOLi@Rq@b@cBx@}CJ]j@gBxA}Dt@oBhB_Fb@_B~@kE^oCVqCLwBJuE@mBG_DWqESeEEsA?qCDkBJqAXwBr@wD`AqCx@gB`AcBj@u@pBmC\\k@n@_AXg@NU\\s@BITg@L]Lc@`@yALk@VmA?AHg@Dg@Jy@HgA@WB]By@@u@?]?EAeAAe@E}@Cg@SmBQwA[yA_@aBMYy@yBq@iBgC_Hk@}A{AiE}@eCWs@gAyCo@mBY_Am@sBU}@WgAWiAOy@WsAUqAM_AO_AK{@MqAKeAAKI}@Eo@G{@Ew@Ew@IaBIaBGmAG{@Eo@Gw@MsAEe@Gi@AEGm@AAK{@Km@E[CGCQG]I_@SaAq@gCmAuEc@cBe@oBOk@Oo@_@mBUqAQkAKi@Ky@Kw@UiBSuBUgCCSa@}ESaCOaB[kDKiAG{@MkAWmCs@gEq@aD{@{CKY]eAWw@Yo@w@gBu@{Aw@aBy@aBk@qA_AsBe@iAm@{A[{@i@yAq@qB[}@I[Qg@[cAI_@Ma@Ka@Mc@GUGSWmAYsAI_@Ia@ScAMm@w@sEAAKu@SkAYgBKy@K}@KaA?EGw@Ek@Cc@?AAQE{@CgAA{@Aw@?{@?C@{@@u@BkABa@@e@@QBa@FaA?EDg@B]Da@@QH{@BMHo@Fc@F[Ls@P}@Jk@F]BI?CH]@G@EFUPs@Tu@ZaABGVs@bAsCN_@x@{BXy@Vw@\\_ABI\\cAVw@Ng@La@Nk@\\oAVeAH]Ha@Nw@TkALy@L}@Ly@Hy@Hm@Dq@Bc@Fy@HkALoBD}@BkA@u@?a@?AEeFIuCO{CGy@OoASoBEY]{BOw@YaBUcAMm@Oi@Ki@Ws@CKSq@YaAwAsEGSeCeIw@eCeAgDwB{Gu@eCk@gBOi@EKOi@AEy@eC]mAMa@EMOm@Om@WeAGYI]G[EQGYCIIe@W{AEWE_@Ik@E]Im@UuB?EIw@KsAAM?ACm@AGCg@Cm@?ACo@C{@CeBAqA?s@?aA?G@k@@o@@cBDgABi@HyADg@TuC^oDp@eEn@aDH[F[^yAJ]FYJ[L_@?C@CHUDOHYN]Ne@To@Pg@Pa@Ti@Tg@Tc@LUf@aA@CRa@Vg@Zg@NYNUPYTYZe@NSLQX_@\\a@`@i@HIPQ^c@TUf@g@`@a@|@{@JIRSZY`DwC~EsEtBmBBA|ByBv@u@~ByBhAeA@?x@y@LK`C{BZ[|AwA@A`@_@j@i@~AyAz@w@x@y@bA}@BCpAmAzBsB\\]^]xBsBxDoDbB}At@q@\\[~FoF`@a@TQv@w@`BaBXYhCeC|A{ADEfD_DhHyGjAcAvCoCTU\\[RQZYj@k@lBkBFIHKh@k@HKLORWPWZc@PYLQHOP[b@u@Xk@Xm@FMRe@Rg@^aAt@sBBEvCaIh@{A`@eABIh@wA`AqCdAsCNa@L[La@L_@@EPi@FSb@yAPq@Pu@RaAP}@@CH_@@KJk@DQL{@RsAl@}Dh@cDPkAXgBj@iDPgAnAkIlBaMF]x@mF|@cGr@qERuA?ARoANcANeAJ}@Hs@Dk@BWBa@@MDk@D{@@k@B{@@]?a@?e@?u@?}@Au@Ck@Ak@G}@A]C]AQGg@Em@MiAE_@E]Ii@Kg@COGYKi@Q{@Qu@W{@Uy@Qk@CE_@gAm@iBc@kAq@iBiAaDe@oAi@yA[{@i@uAg@yAUo@y@{Bq@mBiGuPQi@i@uAu@qBeAyC}DiLy@{B}FcPSg@y@aCQe@KU]cAaBsEAA}@cCUo@ACISCI?As@mBISSk@eAuCeAyCeAqC_AkCUk@AG{@}BCKa@gAiAaDUm@m@eBk@_Bm@aB_BkE_FiN{BgGIWyBcGK[aBuEO_@Oa@AEOa@e@sAqBwFc@iAa@gAu@mBq@eBO[Yq@Ug@O_@}@qBEGIQe@cASc@Q]_@s@y@_Bq@sAu@qAa@s@IMiEaHgAyA]]{@s@e@_@w@c@iAi@uAa@k@M{@ImAIiA@sBLUBuCVa@@q@@A?_@AYAe@E_@CKAWEk@GmCs@iBc@{Bo@_Ba@}A_@gAIaACmANy@Vy@\\gBnAy@r@m@f@_Ar@}@j@c@Pk@Pu@Pg@F}@@c@AMCWEUEoAYaA]kAa@]IWEo@Ki@EoCImAC{ACuAGuACmBGoBGk@?CAK?_@GSC[IUGu@WeAk@q@i@q@o@i@i@[]eBaBy@m@[Ue@QICMEGA]IWEUCq@Eq@Ai@Bc@Hg@Ls@X_@RKFA?QJMHCBqAv@{@d@o@Zc@L_@JQBUDw@D]?g@Ca@Es@MYIy@W}@_@CC}@][MiAc@{Aa@i@I_@IEAeBQoBQCAYC}@KYEc@KYIa@QSMUMOK[WQOm@s@S]QW]s@Yq@Us@Qu@c@{BQiACKOu@_@wBCM]oBAGKe@[}Ae@wASg@[u@MYe@y@CGIMk@aAaAuAm@w@mBmBiBuAkAo@a@Sa@Qg@SaA_@UKGC{@]gAk@c@[g@g@KMUWCGKOu@sAUe@Sa@o@oAo@uAKQO[u@}AIOm@iAYg@a@k@WY]_@MK]YSSQIYSSKA?s@[w@Yk@K}@O_AI]Ao@Gu@Ei@GYG{@QUKUIy@c@e@_@SS[_@[c@[i@KQQ]O]{AaD]i@W[m@s@w@o@MGOKYOSIWI_@KsB]g@GaAMEAaBg@k@WmAy@gAu@a@WKKwAaAiAw@eBsAYSCCkDcD]]{@_A_IwJeAsAkGwH[a@cAqAa@g@CEcBsBmA}Ac@m@OWOY[{@KYWeAa@cBGWYuAg@{BOu@c@oBESEQGYEQWiAa@mBYqAMk@ESkAsFk@aDMs@W}A]aCQiAUiBYuBQaBGi@MwAQeBOcBQiC]mEG{@q@uJY_EImAIeAMgBU_DYkEkAqPCYMoBE}@EgAAcA?qA?w@@o@@_@By@Dm@JuBLmBPkDBu@BaA@]@aA?y@?k@Ak@EmAKsBCYKeAAGOmAYeBMq@Ka@]mAk@gB}@wBu@wAy@{AMSu@cAmAsA_A{@oBwAcFoDq@g@CCm@c@aAm@w@i@UQyF}DyCqBiCgBi@]{AgA_@WeMwIMI{B}AOKuBsA_DoBUKoDqBu@_@UKiCkAsAm@c@QiGcCeFaBwCy@yA]yCq@AAa@IaASkBc@KCIAkDu@yCm@}D}@WGa@KsBc@_Cg@k@MgDs@{A]uA[uAY_ASwA[uAYuA[_AS_ASi@MwA[uAYaAUi@K_ASm@Ki@Ik@Ik@GcAGk@CwACwA@M?s@Dm@Dk@FU@MBgANuAVUF_ATc@NE@[Lw@XqAh@}@`@aAb@_A`@w@\\sAd@G@w@Rk@NC?a@H[Dm@Fi@DaAD{AAwAIa@Ea@ESCuAYc@M]I}@[IEa@OQI}@a@qAm@qAi@sAk@g@QUISGaAYsA[m@MUESEk@I_AKs@I]C[CaAEm@CoBAyABk@BeCNk@FsAPeALQBaCZmBXwAPaALwARwARgANgBTwC^yCb@mBTcC\\mDd@{Ep@u@Ha@FA?aBTwFv@iBVc@FaJlA]FqAPUDG@{APmC^c@FyG|@c@Fo@H}ARc@Fm@H{IfAuFv@yEn@cC\\eEh@mDf@{ARc@FqBVcC\\eEh@{G|@mBV}C^kD^cCXyCZcCXcCXqD`@aCXwANm@Fm@F_AJiAPK@k@HqBV{El@}@LaAPqAT[FsAVaATuA\\_ATi@N_AXaAXi@N}@X_AZk@R}@\\}@\\k@TiAb@EB[Jc@P}@^}@^_A^oAf@sAj@}@^eBx@qAl@uAp@_@RSJgB|@u@`@i@Xe@Xu@b@cDnB}AbA{@j@y@h@c@XSL{@j@kAz@e@\\mEjDoHrG}@x@gC~Bk@h@m@j@GFmDlDc@b@c@^gAbAc@\\e@^SNe@\\q@d@c@Xe@\\g@Zg@XkAl@qAj@}@^sAb@IBw@R}@Tk@Li@Hk@HaALuAJm@DaABi@@W@aA?aAAaAEaAIk@Eg@GYE_ASOCeASc@I{A[_Cc@kB_@cDo@EAaGiAuAWgAUc@IsAWk@MICiASm@M_AS[GOCi@Kk@GkAKI?cAAm@@U@UBI@_@Dk@Ji@Lk@Lk@RSHQJk@Xe@Xe@\\c@^u@p@g@`@YTGFe@`@c@^c@`@e@^QNe@\\YT}AbAa@Vi@ZQHULIDa@R_@RA@i@Te@Rs@V_@LsAb@UFOFQDqA\\iAZcCr@MD_AZ_A`@k@Ze@Xg@^w@p@e@b@SV_@`@_@h@_@j@a@n@e@bA]p@e@dAkB~Dw@bBk@lA]p@i@~@wAbCg@r@}@nA_@b@c@f@CBm@p@QPSRMLu@p@SPa@Zw@j@y@j@e@ZSLy@d@g@Vg@TEBQHe@RqAf@]LiA`@_Bl@]LgBp@a@N{Aj@oBr@a@PeBr@_@P[Pg@Zy@h@w@p@c@b@s@v@q@x@_@f@]j@]l@Yl@[l@MTg@dAi@bA{@fBwAtCg@bAqAjCu@zAy@zAKP[l@]j@_@l@k@|@]h@_@j@k@z@}@tA]j@MVMRi@dACFe@|@mBrDMXWd@CDw@|AKRi@dA]j@[h@_@d@MRc@d@KJUVw@n@UNk@^WLUJs@XaAZYFw@NkALY?g@@WAWAUAUASCUC_@GSEKCICSGSGUISIUKIEYQQMSMQOQQOOOOQQOSOSMSIKEIEIOWSa@Yk@_AoBk@mAUe@CEMa@_AoB]s@]u@U]y@cBg@eAiAaCQ_@s@yAc@eAUc@ACCEQa@qAoCkB}DaAqBu@}Au@_BSe@CEQ_@a@{@A?eCsFo@sAqFiLkA_CyBsEiAcCy@gBiBuDy@eBs@aBmAoCa@aA[w@c@oASg@o@cBi@}AY}@u@{BmAyDqAqEw@kCmA{Da@oAcAwC}@gC}A_Es@cBq@}Ao@wA{@kBc@{@Ye@m@mAYq@OYo@kAa@w@Ua@i@}@_BkCgAeBu@iAa@m@c@o@qAkBiCcDiAyA_AgAwAaB_@c@i@m@}@aAmAsAe@i@e@g@MMc@g@u@w@_AcAKMi@k@i@o@SWq@y@_@e@eAsAm@{@II{@mAm@}@k@y@CE}@sAk@_AMQ]k@i@}@i@_AEGoAyBk@eAw@wA}BaEaAiBEEgAoBu@qAw@uA{@{A{@wAYc@o@cAKO}@sAkBoCiBeCoAgB{@kAmAcB_AqAm@y@mAcBmAcBY_@eAyAgCmDoBmCgAyAGI{@oA[i@]k@MYKQKSKYMYISIUKYI[K[G[I[GYCIIe@EWMy@WiB]oCe@yDKy@Ge@Km@Ku@Ms@G[GWQu@I[GYKYIWIWKYKU?AKWKUMWMUMWKSOYQYYa@OUOSUWSWWYa@_@UQSQUS]WYQ_@UUMQIWMOGUIYKUK]Io@Qi@MqA[w@Si@Oc@Mg@Qg@Sg@Ui@We@Wa@Wc@Yc@]e@_@c@a@CCWWSU[[UYY[W]U[W_@Wa@Ua@Q[Uc@Wg@MUMYUi@Um@[u@Wo@Uq@Uo@Uq@qC}IiAqDs@yBUs@Ma@eAeD_@mAi@cB_@oAGOg@gBeAyDaAkDg@gBo@aCe@_Be@iBGU]mA]qA]iAq@eCkAeEg@iBc@_BAEk@sByBaIaAoD{@}Cm@{By@wCi@oBe@aBw@uCy@{CmAkE_@qAc@aBW{@W_AUu@Sq@Us@a@iAWo@Wo@Yk@Yo@Yk@]m@[i@]i@[g@_@i@_@c@]e@c@g@_@_@a@c@c@c@c@_@c@_@mA}@u@e@y@g@i@Y}@c@w@c@}@c@a@W]S]UUQ[U[U[Y[[e@e@a@g@c@e@a@i@_@e@]e@Y_@AAY_@iAaBk@}@m@cAy@sA_AaBi@cA]o@[o@Wg@[s@Wi@c@aAYq@}@{Be@kAi@yAo@kBg@}ASo@Ss@]kAc@eBQq@Qu@e@qBa@cBa@iBa@gBk@aCa@iB{@yDcAoECGSeAWsAUiAOaAQgAOiAWsBUqBIy@CYOsAOuAYwC[sC[{CQ}AS}AKs@Kq@WsAWkAI_@_@cBAA]oASs@Oa@CMc@kAa@gAYo@Wm@a@}@Uc@Uc@cAmBy@yAqA_CAAaAgBYc@Yg@g@u@_@k@W_@QW[c@_@g@Y]?Ao@w@o@u@i@k@GISSSUs@q@s@s@s@s@{A{A}A}A}A{AyAyAGGUSsAsAsBqBoBoBsBqBiAiAq@s@UUQO_@c@_@a@CCY]_@c@UY_@e@]e@q@_Ai@w@]k@]i@]g@IQGKs@oAKO{@{AaBuCEIu@oAc@u@c@w@i@_A_@q@k@_AYi@]m@oA{Bk@aAWe@IKoBkDS_@s@mAkAuBKSWe@Wg@a@}@g@iAe@kASk@Uq@Sq@Ss@Ma@EOQw@Oo@Qu@a@gBQy@Ow@Mk@My@UwAOgAOkAKaAK}@MkAGy@o@uGm@wGUsBOuAKw@Km@G_@Ic@Ia@Ke@I[IYGYIWIWKYKYKWIW[s@IQYo@e@cAy@_Bi@aAs@uAaAkBkAyBoAaCo@oAWc@Yk@aAoBi@eAg@gAm@mAy@iBs@yAq@_Bi@iAuAaD_AyBkAsCMY_BwDoBuEEMIQSg@s@_BsAeD_BwDa@aAs@cBu@eBkAuCuAcDSc@Qc@o@aBq@aBaBeEk@uAcAcCgAmCe@eAe@cAw@}AcAqB[k@m@gAi@}@o@eAYc@S[gAeBgAaB{A}B}AcCYe@OUm@aAg@_Ae@{@Ug@Wk@Ys@Uq@Uu@YcAU_AQw@WqAO{@G_@G_@Kw@Ie@EYq@mEUwAIc@SiAOu@Oo@Qy@So@Oi@Oc@Qe@Sk@Wm@[q@g@gAg@_AmBsDwAoCkA{BsAgCy@{Ac@y@k@gAeAoBq@mAo@gAs@gACEu@iA{@oA_AoAAAcAsA_@c@o@w@m@s@SU]_@YWeBmBY[oE{EQS}DiEo@s@iBwBo@w@m@s@s@}@g@o@w@gAu@eAMQq@cAi@y@iAkByAaCiAgBYe@e@s@a@k@a@o@u@aAw@cAi@o@_@c@m@s@k@m@k@k@gAaAeAaA_@[c@]]Y_@[SOu@o@wAoAm@k@_A{@iBeB{@}@c@c@UWu@w@gAmA}@cAy@cAaAmAU[W[s@_Aw@gAWa@EE]g@m@}@u@iAu@iAiAkBgAiBcAeBmB}Ce@u@e@q@?As@aAgA_B_@c@c@m@_@e@_@e@_@c@[a@cAiAaAiAiAqAaAgA{@aAgAoAeAkAaAiAcAkA[]UWEE{@eAo@w@IMaAoACCWa@Y_@_@i@]g@MSGKU_@SYS_@m@_Am@eA]o@?AWc@Ue@Ua@s@yAa@y@m@qAACc@eAUk@O]]}@i@wA[_AQc@c@uAGOIYWw@Uw@Ss@a@wA]sA]yAAAAEYmAUeAOs@Q_AKe@AMI_@G]Mq@Mw@M}@Ko@U_BS_BUiBSmBCSI{@CSIkAACImAMeBGwAG{@GuAEgAEkACiA?GC_B?KCgBCwA?CAs@A{@CuAC{@AUA]?CAOEq@Eq@IcACQ?AGg@McAKq@Ig@G]Mk@Qw@U{@?ACI?CY_AUu@Uo@a@kA]_AKW]{@i@uAg@uAe@kAYu@KWgAsCeAqCs@kBSi@gAsCc@iAy@yB{@{Ba@eAYo@e@eA_@{@e@aAe@}@e@y@e@u@s@eAu@eA_@e@SWW[[_@u@{@s@s@OOa@_@sAiAqAcA}AeAy@g@y@a@{@e@}@e@i@[kAm@a@UyFuCyC_B_@SeAi@}CaBsAs@yBiAwBiAcCqA}BmAeB}@a@UyBkAgAk@wAu@qAq@qAq@cB}@EC{Au@iCuAoAo@{@e@oDkBg@WaCqAmBcAoCuAaB{@i@Ye@Ue@WgImDWKSIg@QSIKEOGUIOEICgBm@EAyBq@kCw@mA]SGk@SqAa@_Bk@cAc@a@Oa@Q[MgBy@gAm@m@_@aBeAgAw@kKeI]W}CaC}BgBeC_BoAo@y@_@gBq@e@Ok@S{@UcAUi@KWE{B[o@GcE_@]EyBSeE_@oC[qDg@i@IcCc@uAY_Cg@gBc@_EiAuBq@eEqA_A[wBq@yDoAoBm@kKgD_A[gBk@yBq@YKsC}@oAe@g@Ug@U{@e@y@i@e@[u@o@o@m@YWY]a@c@OU_@e@Ya@S[y@wAi@aAc@eAm@}A_@kA}@uCi@cBs@{BMa@Og@_AwC}@uCi@eBs@}BSm@a@gAWo@e@eAYk@Q[c@y@]i@OWm@y@o@y@s@w@q@q@o@s@s@s@wAuAsAuAo@q@[[IIeAeA_@a@c@c@mAoAUUyA{AwCyCsAwAsB{B{@cAuA}AOSc@i@cC}CoDmEsBmCiBwBwAkBaAoA_@e@{CsDq@_Ak@q@OSqGgImEsF_D_Ec@i@aD_EeKkMuCiD[]iAqAiAcAsAkA_Aq@c@YuBmAgB}@}@]q@YaC_AqMaFa@OaDmAiAe@aFqBICwDyAmCaAsCgAGAYMaE_BmCiA_@QWK{@c@wBiAmAu@{@m@sCuBeCuBoFeFuAqA][_A{@oDgDqH_HqEiEwCoCy@u@CCqBkB}@{@sAmAYYiBcBiAcAgBcBwFkFaGwFsCmCCAgBeBkAcAUU[WeHyGyDqD{BuBaDyC}CwCwAsAsA{Am@u@CC}AsBAA}@sAuAyBW_@IOc@{@w@}AKWe@eASg@[w@c@kAk@_Bi@cBg@iBQq@[oAa@iBm@_DM_A[qBSaBUsBEg@CSQgCOiCCa@EoAE_BAmAAsB?}CDeBFeCB{@ZkFB[Dm@@GLuAZgCXsBDUHi@BOTwALo@TeAR_ANq@Ru@ZmAn@}B^sA\\sANi@v@wCPw@Pu@TiALg@Hi@DSDUHi@F_@F_@Fe@BOBMDa@Dc@Fe@B]LmADq@Dy@HsABy@D}@@_ABiA?aA?I@{@AmAAeE?o@A{B?aDAI?gDA}AAgFAsHEaN?QAqF?oA?y@A{A?_DAk@?s@?}BCaDAwAAkBCmAAiAC{@Ay@C}@?IC{@GaBIwAGqAIoAGcAOuBQ}BWiCQ}AY_CWoBGa@UeB]sBSoAUkAAIg@eCe@yBUcA_@}Aa@cBAEMc@CK_@sAgAwDqA}D{AeE[w@aAkCAE_BiEOc@AEuBuFw@wBu@uBUi@Qg@gAwCmAeDoAiDIUw@uBeAuCu@uBQe@kA_DeB{EUm@Qe@Qe@[y@e@qAIUq@iB_@eAm@}AIUo@cBa@kAy@uBUs@u@qB]}@Sk@gAyC_AgC}@aCiBeFcAkCq@iBOa@KU[y@s@sBM]Uo@Um@Sm@Oe@Ma@Ma@Mg@Om@Os@G_@Ko@CYAACWGg@C[AMEe@Cg@?EEw@Ai@Ag@?A?g@AaABm@DgALaBPaBB_@He@Lu@FWPs@XgAh@_BHQVo@d@aAVg@|BgEJSf@}@DKj@iA`@_AXq@@CPi@@ARm@JYBGDO@CPm@Po@BMLg@@CTeAF[Ns@Jq@N_ANgALoAFq@H_ADo@Bg@FgB?O@o@@i@AiB?AAgBGcBSqEIcBGyAKeBCm@Co@I}ACe@MiCAMCq@Iy@QuBC_@MeAg@sC]cBYiAYaAEOGQM_@c@kAUq@c@eAA?mAcCKQUc@S]w@gACGUYW_@]c@a@e@_@a@_@a@[WIIiAaAmA{@[S_@U_@UmAu@iBmAi@_@q@e@UQ_@Yc@a@QOs@}@]e@c@o@a@u@o@mA_@aAUo@Uq@WcAWoAKq@]}BIqAOuBOcDEaAG}@AS?GM{BIsAAOGiAGaBI}AMgDIwCGsCGgDAwAA}A?s@AO?M?qD@oDDuC@aA@o@B_ABmAB}@^qKFaAJqA@YBm@NuCJqB\\eHf@{JTcEDy@TaE@YFy@XaEZaEPsBF{@PqBFs@LsAVkCd@oEr@kGf@yEXeCz@mITqBjCkVnAaLx@}Ht@wG\\}CFo@fAgL\\eEPqCXaFFwAPwEBo@H_EFcEBmD?kB?g@?sECyDEaCKcEAm@WgHYwF[qEY{Dc@sEKcASaBi@}Di@yE[qBG]QaAs@cEAGKk@AEgAoFy@sDS{@EM]{AoA{Ew@oCyA_Fq@qBSi@e@uAgDsIeBaE_AyBiAgCwC{GoCmGcDsH_@{@c@gAmAwD[kAu@kDWcBOoAU{BE_@Ck@Ei@Ew@Ae@E{AAkB@cBB{AFmBFiAJmAPkB^oCJg@F[VoA\\uAjAoEd@_B~@iD|DiNrAuE|DwNl@kCR}@VyAb@cDFi@TuBF}@JcBDcAFaBBy@BqB@kBG{DIoBSeDMiBi@mEIs@g@iCa@qBu@sCe@_Bm@gBw@yBmAmDu@sBeBaFoAoDoB{FiA_Ds@cCa@{Ag@_COy@SeAOgAQiASkBIo@Em@Gw@IuAEw@E{@EaBAmA?qB?[@uA@{@DgBBw@HaBFkAT}EBm@FuADy@LiD@yA@Q?u@@gAAeACkBE}@KoBKqAEe@CWUkBKu@SkACOQ_AGSSaAYcA?C]cA[y@u@wBc@aAgAaCq@gA}DyFGIU]OUGIGGS[sHuKiD}EaCoDeBeCiA_BeBeCiBgCs@eAYa@wFwHy@oA{AyB_HuJsCcEAAYa@yDsFkCwDeEgGyCaEoAgBqCaEuCcEcGqIuAuBOWqAyBSa@u@uAy@eBi@oAs@aBmD}IkAsCe@mAyAsD{DyJgFsMoD_JwBqFoB_FSg@qAgDo@cBm@oBe@{Ae@gBcAiEc@uB_AeFk@yCAIMq@c@wBKk@AEoAsGoBmKc@}BAGIc@AImAqGG]Mk@Ou@c@}BCSmAoGwDgSG[kBuJaAiFi@sCI_@_BwI_@uBIk@EUKy@Iw@QcCCo@Eq@Cw@Ay@?a@?e@@i@@o@ByADy@Fy@F{@PaBVeBz@qE^gBBOXwApDuPt@uDRy@N{@JYn@{CXoANu@\\_Bf@cCLk@v@qDjCyLjFwVJg@@C|AqH@Cv@oDXsAZ}ALk@Lk@Jg@rAmGFYnA_GdCiL^cBVkAt@oDt@kD~AuH~@qE^_B@GJc@VoA\\uAT_APs@d@yAVu@Na@Xs@f@iApAwCtAaDt@aB^}@~@yBXo@\\{@\\aA`@oARo@DOHWJi@Jk@N{@Ls@Jw@Fo@Hu@Dm@Bg@Bi@Be@@q@@g@@u@?s@?CA}@Au@CgAMuBGm@CMCWGi@Ku@EYIc@Kk@Os@Mc@Oi@CKa@qAM_@Oe@ACSe@e@iAWk@o@wAoCcGa@y@s@_B_@q@e@iAg@qAOg@Me@GQU{@Su@?AMi@CMS_AYyAUyAOaBIq@IgAGeACk@Cg@Ae@CaAAiB?eA@sB@kB@sA?{@@g@?o@@o@?o@?o@@wAByC@yD@yB@yGDwH?o@BoE@oA@kB?}ABcC@mD?_@BgF@_EFmL@g@?q@?E@gC@gB?o@@gC@{@@yD@o@BwGFoN@cDBiG?_B@aBBoEBgF@uA?o@@w@?]?_@?mADgEDqK@wC?GB}GB_H?g@@o@BuE@eB?e@?e@BeFByF?w@@o@?mABqE?o@BaD?o@@o@@oCFmN@wB@_CDyJBgHBkGB{CHgQLs\\BgGD}HFwM?eABsFDqIBeF@o@@iCJuT?mADcGLyW?KFeOFyM?o@BoC?o@?{@@sAFmLFuOBaEHeQF{NFoMPm]@s@BqHBaCF_O?C@mE?}A?kA?y@Ac@?I?a@Cu@Ao@Cu@?GE{@EkAEm@?OGaAGeAI{@G{@Iu@?CGm@AMK{@K}@QqAKs@AGIo@Mw@QcASkAQ_ASeAUcAyBcJaAeEsAsFeB{HG]AEKc@Qu@eBqH{ByJ_AaEsB}IwAgG[wAMk@Mi@AAw@iDaCiKaCkKMk@iAyE}@{DI_@kHk[CKoBqI[wAk@gCQu@aDiNqAyFeGuWYkAEOQ{@Su@i@eCYsAyAoGk@cCIa@g@yB_@_BIe@CEOs@y@oDwAgGuAeG{@yDiB}HQy@I]_@cBS{@AAMk@_@_B_A_E}@}Di@}B}@{DiAcFyAoGmAiFwCqMWcAMk@uAgGMk@qAwFkP}s@qAwFaAiE{C{MiEcRy@sDUgAYmASeASaAOy@WwASeAUyASkASsAYoBQmAIy@Im@EYCOK{@CWEYa@_EMoAMwAM_BMaBEo@y@uLEm@?ECYg@uH]cFGeAOsB]uFa@oFW_EScDOaCKqAAYAEGcAKwA_@wFGw@YqEiBgXw@gLUkDk@{Ia@}FMsBUiDAQEo@]uEg@cHg@}GWsCQsBAGI{@Eo@e@oEUsB[kC{@gHi@yDQkAM_AO_AGc@M_A[uBSkAaAkGw@qEg@qCa@}Bg@iCq@aDc@wBUeAQu@UgAMg@[uAw@}CI[yAcGQu@u@qC]sAEQOk@K_@Su@Qk@o@_Ca@oAq@}BAAQi@a@mAkByFSm@Qi@u@yBeA{CWq@iAcDw@yBK[qBsFuEmMsMy^o@gBkAiDOc@[{@{BiG_@eA_@eAgBcFqC}Hs@qB{@_CgA}C{@cCs@qBuAyDuAwDgA}Co@eBi@{AkBiF]_AgBcFGQcBwE]_A_AoC]cAOg@Oc@W{@Sw@W_AQs@[qAI_@I_@S_AMs@Ki@WwASsASsAUeBIo@Ei@Gg@Ea@Ce@Gu@IaA?AGiAKqBAKCw@AUC_@Aa@Cg@Ag@?AAa@Ao@Ao@A_AAy@Ac@?k@As@?qA?wBAcEAwC?mEAiB?qAC}I?{D?o@?U?yB?kC?sFA_FAoDAoFAsDAsB?gAA_AAq@Ag@GcCAo@Cq@Cw@IwBC_@GcAASK}AgAcMM_AQsA[sBc@qCQ}@Y_BS}@UmAAAUeAq@_DuAwGwAqG}AgHmAqFkAwFI[GWy@oD_@iBa@cBI_@]_BMg@SaAYmAUgAAC_@eB_@gBi@cCiAgFcAmEo@yCYqAe@}B[_BCKG_@Km@Mo@UwAQcAa@iC_BoLw@iGi@eECOE][aC{CyTE]M}@}@aH_AoHEU}@wGe@kDcAcI_ByLMcAOeAGk@g@uD]eCi@{DGm@QwAYsCQiBa@qEOmBEe@YcFI}AUwDC]g@}IiAmSOwCEm@OmCk@yKs@{LU}D_@yGI_BoAgUEo@i@yJEo@e@kI]mGq@wLEo@m@kKUeDMiBMmBk@wGC[O_BGk@a@wEKaAEm@gAqLiAgMSuBeA}Ks@uHGo@UgCUqBc@yDYqB[_C]cCYkBIi@Q}@_@uBIe@[_BIe@y@uDa@iBWiAu@wCu@oC_@sAg@cB]iAq@wBe@wAc@oASk@Uo@K[CEy@yBe@oAUe@u@kBaAaCmBoEw@iBw@iBcB_E]w@{BiFm@uA{@wBy@wBm@}Ay@aC]aA}@mC{@uCg@eBc@}Ao@eCWeAq@oC]aBYoA[yAg@gC]gBG_@SiAYiBUyAEYYqBw@mGG]sAqLIm@mAeKCYw@uGIo@e@wDaAcI_@}C_BiNIo@Q}A[gCE]CQUoBa@cDk@uEg@oEkA_KsAaLY_C]uCo@kF[wCw@iFGa@SoAUuAUmAAIKm@GW]gBUkAm@{Ci@eCYiACIg@wB}@cDSq@cAoD]kAAAQi@I[i@aBm@eBIU_@eAq@iBc@iAgBmEKUIWm@{AoBwEi@qAQ_@_A}BQc@cB_E_CuFa@cAmAuCWo@cBeEmAsCuDeJoAyCiBiECG}GoP{EmLkAuCuAeD}AsD{@wBqAoDe@wAa@wAe@cB]sAa@eBYoAG[k@wC]sBOeAWqBoAyKO{AS}Ae@_EqByP_@aDQqAK}@O_A[mBa@cCi@gCS_AmAoECIW_A_AsCw@{B_@_AaBwDYk@]q@mA}B}@{AQU{AaCmBeCmA{AyAaBkAkAyAsAw@o@w@o@oDcCw@e@oC_B}@a@qAm@u@[oAm@cCgAiEoB_F_Cy@e@{@g@o@a@_Ao@w@k@{BiBsAiAu@s@o@q@aBgB_AkAW]q@{@s@aAyAyBmAuBaAkBo@oAk@oAk@qA_AeCwA{DQk@Qk@AAa@wAqAiF{@mDiAyEkCsKaDwMeDeNa@_BCI]uAgD_NwCaMMg@k@}BUy@s@qCYiAMa@m@{Bi@iB{@oCoA{DsAsDq@iBs@gBSe@}AqDIQoBkEe@_AmAmCsEwJwFwLm@qAyBsEyGwNmDqHyPu^aCeFmHyOyByEuAwC}Sed@uAyCwE_KwBuEuEyJmC}FsCiGkCwFwBuEoC}F[q@Sc@o@uAqIsQkB_EoC}FyEcK{A_Du@}As@}AcDcH[q@yAwCUc@cB_DcBuCqCoEiBoC}AwBQWm@u@gDgEmByB]_@qByB_DmDoE}EWWsGgHoHcIwB_CqAyAcDkD}DmEsImJw@{@oCyCSU}CeDsC_D{AcBYYAC[][]mCuCe@g@y@}@cAgAwBaCmDkEmA_B_BsBsEcGgDkEkF_Hw@cAkCmDiAwAiBaCY_@AAeDiEQUq@{@kCwDqCgE{@wAi@}@eAkBoCgFkA_Cy@eBg@gA{BoFoAaDs@iBmA_Dq@gB]{@Sg@iCsGACy@wBoA_DoA_D{ByFuBgF_AyBiBsEM]sBiFw@oBuAoDi@oA}G_Qk@wAAEi@qAeCkGkCyG_BcEmA_Dq@eBsDiJCIQa@_FcM}AyDwGqPgBsESg@sCkHuc@whAyFuNgHsQ_FcMsBiFcBgEkCwGiEyKmD_Ju@kBqPmb@yB{FiDwI{@uB_CaGsDmJoA{CmA{CqAeDiAsCeAkCeAiCs@iByAwDoC_HyAwD}@_CYw@]gA{@mCm@yBsAsFYqAAEs@wDe@sCe@mDS_B]kDOcBIiAUcDOmECmAEmAAiACqA?k@As@?qB@aCBaBDoCFwADuARsDFw@HoAz@wIDg@~@kIr@wGv@gHd@yDRoBr@yGH_ALoAH_AJkANmBJyAR}CJ{BD_AFqADeAFeBFoBDqA@cABmAB{BBoA@qB?eC?_BAmD?GCoBCsDAkACcDC}AAcACkD?SKaLKkLMmLI_KKoLGwHC_BAaACwBAeBAOA_CCcBEeE?i@EgECoDEoD?WAo@AgBE}DCyBEyBC_DAoAAo@?aAEsDCqD?GAo@Aw@AyACyCAoAIgKIqIA{@IqHC_EEsDE{CCeDE}DIiIEoECwBCuCCoDAqD?S?mB@eB?eA?mE?oE@}G?yG@gE?cE?_E?kD@{G?}C?qF@gC@qD?eD?qI@_S@uL?aE@oO?cF?kH@oI@cU?qI@uM?{E?gC@iC?iA?{A?yA@mG?uB?{D@cB?}A?aH?uI@{K?}@?_C?mD@sD?eK?oB?_B@wD?S?qB?{G@{E@wD?kE?s@?qC@uC?iF?uC?eC@cF?qA?_A?eC@uC?uC?yD?aA@mD?oC?eB?mH@qD@mF?}C?iD?eE@gB?{@?mE?gE@eD?uB?gD?oD@}H?_F@iF?{D?iD?_E?_@@iB?kC?oC?i@BmS?yF@wL?yC@}C?oA?o@?gF?oC@cH?A@}L?gD@mE?{I@_C?aF?gC?yF@}F?S@{E?g@?gE?]@eE?K?wF?iE@uF?gA?yA@}E?yB?aA@qC?oE?mC@eG?mE?qD?yA@iB?uC?yE@sF@qG?oG@}F?iD?sJ@_G?eEBe]@oF?{J?_F?wDGaECoBCgBEqCAi@?EMoFAo@WuMMiHuB_fAOoIQqJE}BG}B]mRWeMCkAYmOOwHSoKSsJMkGCuAAo@Ak@CwAGsCAw@CcAIiDAq@EmCKmF]sPKmFGoDGaDCaBAm@AQK}EM{GEcCM}GAo@I_EQiIG}DImDCoAG{CAWEkBCw@Em@C{@IkASqCEi@ScCWwBQsAOiAi@cDa@sBOy@_@cBSy@Qw@W_AYcAW{@Qi@Uu@Y{@_@eAg@qAWq@GO_@}@k@mAISWm@e@_AQ_@a@}@w@aBgA}Bo@uAUe@mAgCmB_EqAqCwBmEk@qAUg@kAcCyA_DgA_C_AuBk@wAm@eBIUK[Oa@Qk@Y_ASq@Qo@Qq@W_AESMk@Ka@Qs@YyAIe@Mq@I]W_BSwAEUGe@QwAOuAMeAOoBQkBEu@M}A_@sEg@oGIgACWCWc@gFg@wGScC]oEQyBEe@C[MeBQkBEk@Q}BSaCQiBK_BQ}BO_BKcAWaCS_BWkBIq@]uBAEUuAQ{@Mu@GUOq@WeAo@gCKa@i@oBs@cCwBqHoBwGuBkHg@gBq@_CeBaGi@kB[oA]uAa@mBO{@SkACWUwAScBKoAKaAKwAIsAGy@C}@CqACcAAeB?}A?{@?e@@e@B_AFuADmA@SB_@Be@D{@J_BJmAXeCp@kEh@uClA{EpB}GjAeEZoAZoA\\aB^iBVqAN{@XsBNeAL}@NoAJaAD_@d@{FXuEB]R_Dr@_Mt@wMd@wHNmCF}@Hu@BYBWH{@@IHm@NmARmARmATmAXuAXsADMTy@^oA\\iAb@sA?Av@wB|AmEDK`AoClAiDt@_CBKHU@GNe@Pk@TcA^{AP_A@EN{@TsAPqAHg@BWNkAJiAFu@Do@?EFkAHqAHmB@QBo@JyBLwCDmAHaBFmAFyAV_GZcHBa@NmD@QT}EXwGTeFP_EHkAHuAJkAL{AJcALeAP_BRsARsAPcAN_AXwAZ{A`@iBTy@R{@Tw@HWJ_@BIPk@Ts@Vu@Vu@`@eAh@yAl@uAr@}AJUr@sAp@uAHOzAwCTc@l@kAbAmBTc@d@_A|AyC~A_Dd@{@d@_ApAeC~A}C~@eBl@aABEp@aAd@o@p@}@f@o@JKp@q@h@e@`@YVSfAk@~BmAJIHC`CkAv@a@n@]|@k@NIh@c@`@[POr@q@XYZa@NSJMR[Xe@h@aAVk@Vm@`@iA\\eAfAsDd@wAJa@La@L]\\iA~AaF`CoHRq@Vo@b@eALYRg@LYr@_Bf@gAHQJQVe@`@s@bA_BpCkGn@mAdBkDz@qBV}@rAoCnAcDl@aBj@iBpByFTo@Pg@fAeDXu@Rg@j@wAf@gA@Cb@{@DKTc@Ve@Te@DG~@eBJSnA{BjBcDxByDpBsDrAyBFKv@uAd@y@xCkFhCsEd@aA^u@HSJS^{@n@mB\\kALk@XmA\\{AL{@He@R_BJaAFy@Di@Da@@UB_@@k@Bi@@s@@o@?E@}A?}@Ao@EaBCk@Co@Eu@Gy@Iu@K_AKw@Kw@E[I_@Ig@ESG]GWI_@Ka@Qo@]iAIWi@kB_@qAm@mBM_@wC}JkBqGWaAe@gB_@aB_@iBIY[oBYmB[kCWmCQiCK{BA[M_G?A?{GBs@F_CZsGH}ABo@F{@^qH@Od@uIh@mKXiFDu@@g@@Y@YBu@DqBBwB@sB?YAcCAoAE{BKsCAQEiAEcAImAAQCe@SuB[}D_@{EEe@k@aH?Ag@_GKgAa@mFOiBGs@E[Ei@Ku@K{@M}@My@UiAWoAGYQu@]wAQm@K[Oi@Wu@[aACCc@gAaA}BSe@}AcD{@iBu@aBk@kAi@mAg@oA[cAa@sA]oAAES{@O{@WyA?GSsASiBEi@Ei@I}@Ci@CaAAm@A[?OAs@Ao@?w@?s@@O@i@F_BBs@Bc@NaCToDXkE^uF`@sGHcBB[DsB?Q@cB?gBAc@Ao@GuAGqACUC_@SkBWoBUaBGSUkAc@mBqB_HOk@Sm@wDmMg@aByHoWkEcOsAsEwC}JIUkBsG{AiFGUyEwOe@aB{B}HGWuBgHoAgEkCyIe@_Be@}A{AgFg@iBaAqDe@mBKe@eAoEo@uCaD}No@yCgDaPeB_IS_AYiAu@_D[kAMg@Og@mAeEuAgEmDoKo@mB{@iCmBwFoB_GaCkHa@kAmAuD{@eCY}@q@mBsEeNWu@g@yAaCiH}D{LiKyZ}GoSiBqFo@sBqGmRkJ}XQi@_HoSaCkHq@gBi@iBy@qCgA}DoSgv@mC_KgJo]aBaGuDsNwAgF_@uAiAcEeBwG_AiDmAuE{AqF_CqIs@{BaAgCs@gBu@aBm@mAAEu@yA}@}Aq@iAm@cAq@_AOSkAaBQUsAcBmAsAMMoAmAm@g@_@[][mC{B_Aq@}AcAwCcBaAi@aDgBuL{G_@QqBiAsGqDoBiAoDsBq@_@cH{DgBaAmC{A_Ai@aAi@_CsAw@e@iDmBaAi@_@U_@SaE_C_CsA}G{DYSu@a@iBcAOKMI]SuAw@{@e@c@]i@g@GE_@]_@_@{@iAu@cA_@o@Ua@Uc@GMOUISWm@[y@Oe@CGi@cBuAuEq@kCQi@Uw@YeAo@}Bw@mC}AkFQq@s@cCUu@e@}AMc@aD}Ko@gCk@{BIe@UqAYkBGe@CMGu@Gw@KeAGwAAQEo@?UEqA?sAAm@@_A@yA@O?QBw@FiAHuA@KHcAH_AHk@@E@GD_@@KFa@Jm@TqAP}@Ja@Ja@Ru@@ELc@Nk@DKRo@Rm@HQFSXs@Xm@L[DKTg@hCeGp@}A@Ad@kAdDaIDKhCgGTe@zBmFRe@Rg@x@oBBETe@h@mA@AR_@@Ch@aABEZg@Xc@V_@`@g@b@i@\\c@LOX[n@k@z@s@jBmA`@UfAq@|@i@z@c@FAXMFC|Ai@bA]xAg@ZMB?VKPIb@SFENENGlAc@vBw@h@Uj@W`@UTMHG^SRMJI^WJKl@a@`@]@A^[|@y@jAsAbAsAx@mAd@w@b@{@t@}AN]N]n@iBNa@^kAp@eCVgATkAf@uCRuAJy@F{@@?FgAFoABs@?GDoB@kA?{@?y@?GA_ACsA?UCk@GkAKuAKsAMcAMcAKo@EY?COw@EOG[WqA[iAEOI[Qo@Ww@IUIYGOk@eBkAoDkAgD_@eAIUQi@ACmAmDg@yAW_AQm@Mi@S{@WkAWgBUkBQmBIuAKmBEoBCmDi@ap@E_ECoCEkBGuBOcCUgCWaC[sB[iBWsA_@cB]qAAE[aAW{@Y}@]}@M]o@}A_AsBaAgBcBoCq@}@sAaBY]{@gAyAgBg@m@MMmA{AgAqAKM}AkBw@cAw@_A{AqBKOkAeBiAiBu@oAsAkCm@oAkBoE]_Ae@uAo@iBa@uAeAyDs@kCaAqDgBqGaAqD_IuYm@}Bm@{BaCwIa@yAkEgPkAiEe@cB_@uAIYOk@Qk@_AqDw@sCk@wB_@qAo@{B_AqDaAkD?AeA}Dm@{BiCyJkA}DkCwJsEwPmDqMoAwEoAuEqCcKwAoFw@sCaGoTOk@_AkDoCaKOk@cL}a@_BaGoAwE_BaGqAwEcAuDyAyFOm@s@oDSaA{@kFo@yFo@gHs@oHo@_HeAeLmBsSmAsM{AePuBoUe@gF_AyJI_AgAmLIeAgIg|@c@oEQoAGi@OcAo@aEEUScAWqAWiA_@yAc@aBW}@iAqDkAsD_AwCaAwCeAeDqBgGwAmEk@gBiCeIaBeFcBeFmGyRwE}NeD_Kg@_Bg@_BkAkDoD}KkCgIwAkEyBaHQi@CG{AwEK[Qi@oA{DaBaFaD{JqCyIM]iByFoHeUQi@oHgUaBkFuBsGY{@{@oCM_@}@qCu@_Cu@_Ck@eBaA{Cs@{BWu@g@}Aa@oAOc@Ma@CEOi@Y{@_@mAi@aBGOy@iC_@kAkAsD]aAMa@CGqAcEk@eBOc@qAaE{@mCM_@k@iBaAwCi@eB]cAa@qAk@gBa@kAi@eBwCaJu@_CaAwCSo@Uu@u@}Bi@gBg@gBYiA]sAOs@I]e@gC[gBG]Mu@UcBIg@UuBSqBOqBKiA?G[cEMkBWcDIqAASI}@IoAMmBE_@MgBMkBIoAUeDQgCOoBImACWQiCC[ImAC]QeCG_AEo@Ew@IoAA[MgCGmBAQAo@Cg@C{@EgBEsBA_ACiA?u@?QAcAAaDCwF?aB?q@?QAcDAuGAeCAoA?c@AkBA_E?qB?mAAgDAiA?g@EgH?a@EgBGsBGmBCo@G{@Ew@Eo@QkCKqAO}AUyBIs@UkBYiBYiBKq@[eBOu@Ms@WkAGY_@}AGUg@oBYgA]iASo@]gAIY]gA_@eAa@eAGOe@kAa@aA_@u@EMg@_AYi@i@}@y@gAo@u@QQIIu@s@{@o@o@e@w@e@]QAASIq@[w@Y]Mk@QSEi@OcBe@i@Og@MGA_HkB[IkD_Am@Sa@Oc@Qi@Sy@]e@Ua@UYOq@_@c@U}AcAi@a@KIc@[_@[i@c@EEcB_BIKw@y@c@g@k@q@CCY_@ACOSGIi@s@SY}@wAo@eA}@aBq@sAc@aAe@gAIUCG[w@KWACa@iA?C[_ASq@c@{AAE[gAyCeKyByHq@_CQq@K[Oi@K[}AqFw@oC_@oAc@_B]oAEMS{@U{@S}@UmAMq@Ku@a@kCWsBIq@Ea@OmBOmBC]Ck@?CImBGuB?IAg@AwD?Q?sAB}@FmC@]@QF_BP{Cr@}K@OF}@LkBBYBY@[B[HqAJqADu@@IDm@x@kMHsAFu@@SH_B@k@By@BqA?s@?C?[?y@AkAEy@Cw@Ew@CYEs@CUC_@MqAKs@Iu@Ko@QwAO}@COOkAQkAYoB]aCKs@Ik@Ea@SsAQmA[}BEYSuA]aCWgBQqAG_@g@qDQkAQsAUkBMmA?AKiAOoBGqAImBAAAs@EmBAu@Aw@?OAiA@U?s@@mABsADkADkADgADq@Dy@LaBLgA?GLeA@OPqANmA^gCDY@CHm@Hi@Fa@PmAPqAFe@Lu@Fe@Hm@@Gf@oD@G?CJq@j@wD`@sCNeAHi@t@mFHm@D[d@{CFe@TcBHe@@GHm@^iCFe@`@qCBSF[^oCD_@Lu@NiARsANkAzAkK@EHm@DYrAmJL_ALs@Js@d@qDLkA@GDe@Da@L}A@MDo@@OJgBFw@D}@FeBBy@@q@@_@BmA@wA?s@?oBCeDAoACmACaAEaDEeDAw@Ao@Aa@EaDCsAC}AEsEGaEI{ECeBAs@?o@EeBEcD[oTAw@EaDAwAC}B?aA@{@@o@?[@]Ds@@MDu@Dg@?EFm@Hy@Hm@TuAHc@Je@Rw@^wAHUH[Rk@Ts@t@qBj@_BTq@HU^cA`@eARk@JYj@}Aj@aBTk@To@^cATo@Rk@L]dC}GPi@JWFOVq@Pg@vA_EjAiDLc@jAyETcAb@}BTuALy@Hk@TiBTkBr@{F@EPuAVwBVoBHm@Fo@BKj@wErAwKJ{@R{An@eFlAuJJ{@hA_JHs@d@mDp@yFHo@^_D`@cDz@yGJy@Fm@Hm@bAcIFo@Hg@?EHm@`@cDZmC`AqHRcBVuBD]PoAB]Hy@NcBHu@BUFo@D]\\cEV{DP}CLuCJeCDcA@m@LuDNeFF_BHgCLgE?AZ}JDuA@k@H}BDeBLoDDwA?GNyEB}@@]NgFBs@DeAPqFv@kWFaBHuCXeJTaH@i@FyAPoE@OBSN{BBe@JeABYHs@JeAFk@@ANqANaAL}@DULu@F]N}@b@wBDQXsATeAf@mBh@kB\\kARm@J[Xu@Na@n@cBTk@~@wBFOZo@Xk@`@y@|@_BVc@Vc@jBiDbCcE~AsCt@qA`BqCxDwG@AdD}Ff@{@^q@lDcGvEgINWVc@Vc@fAoBbCeEbAgBJS~B}D@CVc@n@gAz@wAz@{AVc@Vc@HOLSVe@d@y@fB}CVc@NWFK~CqFzD{G`@s@Vc@lCwET_@@CVc@nAuB~@aBh@aAh@aArAgC~AcDBCfAcCv@cB~@yB|AuD`AeCfA{CbAwCf@cBh@eBx@yCTy@J[Li@@C|@oDFYBKNk@BKH_@ZwALk@^gBNq@DWn@cDJi@BQ^wBBOLw@DWl@_E?CR{AFe@\\sCHu@Fe@N}AJu@De@ZqDDe@HaADo@P{B@QRoDD}@R}D@[JwC@y@D_BDmA@o@?QB}A@g@?C@{A@aB@_@@cDB}B@uBD_E?I@e@B_B@qA?M@o@@_B@o@@o@B_E@_@@qABgC@q@?EDeG?[BkD@eBD}F@w@@m@DcF?o@DoFRoR@YL_Q@o@LqORaW@i@B_CD_F@gD?wA?uA?_@AoAAuA?u@A[Ay@Ay@CoBCy@CqAA[Cu@AWCo@A]?MKkCCe@AQKkCOkDIkBMqCIoBIoBIoBSaFIoBA]MkCKmCMmCIoBGkAKsCIaBEeAMmCKkCA]GqAIoBGsAEw@QeEMmCKkCKsBAUCo@G_BImBOiDQeEYwGKmCEw@Cs@MoCAWKoCIeBCg@KmC?AG_BEcAKmCGkBC{@EsA?]A[?GCgAAa@CqBA[?e@Am@?C?mBAkC?uA@w@?U?G?sA@A@oB@u@B{@@w@?EBmA@g@Bm@@[By@DqADuABa@@SHeB@KFsABSD_ALqBDg@FeAZcEHuABY@UF_AB]LmBPiC@OJ_BBSBe@Bc@HkA@SBSFgANuB@UFs@Bo@@I@IHkAPiCLmBBa@HkALqBLsBBWHsAHqAFw@HuALmBVaEHkADo@Di@PkCPkCDw@XcE@QJyAPuCPeCDs@@SBc@PmCLiBB_@JyAB]?GBWPwCb@sGZuEPkCRuDLgBJ}AFcAZyEH_C@QFcBDwADyA@Y@q@@c@?A@C?IDcB@s@Bq@@q@Bs@@q@Bq@@q@DkBZgNBuBDiBBc@DkBDkBHoCLuEJaE?U@c@Bc@NkGLuF@i@Bo@@o@RoINoFJsE@Y@W?U@UVkKFqC@k@D{AFqBBaADoB@m@FoB@u@@c@@SJmEFgCHsDJsDP{HBk@@m@HsDBm@ByABk@DqB@UHaD?QFgCZaM@W?U@UT_KFyCf@wQRoID_BLoFBo@B_BBm@^oONaGFsCBg@JiFHeCB_BBo@f@uSHaD@o@DmB@GDyBVyJZmM@o@D_BRoID_BLoFFoCd@oRNuGDiBBo@D_BJkEZeMH}C@o@DcAJyEBo@@o@F{B@SHqDB}@LwF^gORoIBy@@u@@W@_@BcADaABaABcBHcDFsBD}Bp@oXFsCB}@HoBRgIB}@B{A?CNoGHoD?ILeFFaCTeILoF@o@Bo@@i@?EHoC@o@LoFV_KJoE@]@e@b@_Q@o@HoCLoF@o@J_Ed@mR?ABm@N_HBq@@m@Bo@@o@Bo@@o@r@cYb@yQ@o@DaBXmLJaEXmLJ_EDaBn@{VZwMRwHZgNp@{W?EPmHLoF@o@FmBJ_GBiA@o@V{MP_JHqE?g@B{@BuAFiEJ}FJoFFqCF}AHmCb@eNp@}RRqGFmBb@cMHiDToI`Aoa@NoFBgA@oAf@uRV{JHiC?EDsA@o@TsJNoFX}M^cNHoCLoFXmLj@oUHoCLoFj@qTHsEHiD@eA@o@BoCB_BB_BJkIFgG@uADiCBeC@o@?]JoI@o@@a@LaLFiF@o@h@af@RoOBoCFqF@o@@o@P_OVqT@o@HoIH_HHqFd@oa@@uBFcDJsG?e@DyCBeC@wA@Y@aAPiODsB?o@NeLBqB@o@D}CPaO@m@?AL}KHqF@}A@o@H_H@o@HaIHqG@_C?uCCmBCiACw@IgCCq@E{@GsAmBaUk@{GM}As@iIeBsSy@wJGo@k@yGEo@Gm@Go@o@_IOuAYqD{AwQ{B}WKaAASCWIy@AMq@kIASg@eGc@aF}@oKkAoNAMq@iIM_Bi@yGMaBe@gFa@yEoAqOAEM}AqAeOe@kFg@cGCY]_FYoEUeFA[ASg@qJSiEOyCm@sM]{G{Aw[_@}Ha@wI_@{H]aH?GMoCUmE[cHc@iJCm@McCk@sLW}E_@mIaCgg@o@}MCo@WmFI_BCg@gA}TqAiXS}DI_BUyEu@_PMiCEs@_@mICo@e@sJcAkTa@gIcBe^SmE[mGQyDOsCCo@WeF]eHGuAe@}HWcDQuBCWa@yDAIa@}DkDkXgA{IaAmHiBoNQ{AsC_UqA}J{CaVEU]oCGa@UkBe@gDm@}EScBg@}Dq@eFOkA?AOkAmBqOeAiIAEAKkAgJE]a@}CKy@u@oGu@}HMuASeCg@eHyBa[u@gKsAkRAO}@oMAIO{Bk@aIcAyNg@{GkD_g@_D_d@sHafAGq@eC_^oAkQQcC]kFa@aGaAgN_BgU]}EmC{_@qFwv@K}AIwAi@eH{@mMk@iIEq@M}Ag@sHGy@Gs@yBc[w@}Kq@kJ?KAUe@oGCa@_@kFcAqNCi@SkCCc@_D}c@qAgRSoCy@iLe@}G_AyMc@iGW{DEo@aEek@WcDM}AYcCAGIm@Io@_@gCc@gCy@qDMk@[sASw@[mAEKEOGS}EqNIUEKK[}BoGc@oAc@qAqBuFAAuCiIe@sAq@gBc@sASg@_BsEOe@o@gBY}@s@mBe@uAg@uAkAcDmBkF{@cCQi@Yw@q@kBQi@aJkWgA}C}@cCw@{BcAuCg@uAk@_Bo@gB}@iCa@gAu@yBEIi@{Am@gBoAiDe@uAeEsLcAoCiAcDaAsCeAuC]aAUu@[_AK]Mc@Mc@[eAQu@WcAKe@WiAQu@c@}BOw@GYMk@Km@[yAMk@ScA]aB{BaLkCuMsAwGg@oCMk@c@yBCKcAiF_@eB_@kBUoAe@_Ci@cCQy@UmAMk@e@aC_@mB[cBg@eCYsAMk@?Ao@}Cu@yD[aBm@yCw@wDoAkG}@kEAGe@_CEWm@yCMm@e@cCeBuI_@kBMk@SeAc@sBc@_CMk@y@eEa@sBw@wDs@mDc@wBc@uBG]Mk@a@oBScAMk@WsAUiAeEuSUkAYyAg@eCMk@a@uB{@kEIa@}@{ESkAMw@Km@Kk@a@mCIk@WgBOgA_@qCE_@Iq@Gc@Gc@Iq@Gk@Go@QaBEg@QgBCUAKMqAC]KmA[cEC[C_@MmBEq@MyBGkAGsAACAe@Cc@Cw@Ey@GkBE_AAm@GqB?CEwBEiCAi@A{@EgDCiBOwM?o@AcAGaFCaCEyDG_GEoCCyCA{@IuHAo@AyAIoGKiKEgCAcAAsAEmF@oB?[?i@@kA@a@BiB@o@@e@@w@DwAHqBB_AFaADy@Dw@Ba@@QHoA@MFu@Dm@Fo@Bc@NyAjAgLFo@D_@@G`@{D`AgJZ_Dr@{Gr@_HFm@XoCb@}DFo@Fo@^{DFq@Hy@F_ADo@JwABq@D}@DoADuABaA@o@@sA@{@?cB?W?k@AuACuAA}@CmAIqBEu@GwAIgAG_AKmAG{@MiAIq@AOE][cCMu@WmBu@sFOaAIm@OgAGe@[yBIm@OaA{AoKmA{Iw@qFc@}Cc@cDUwAUcBg@gD{@kGo@oE_@mC}@kGiAeIKm@?CaBiL[yBa@sCo@{EIm@SqAk@aEIm@Km@AGcAeHWoBKm@Im@McAOeACQG[Im@EYc@}Cc@aD[qB]iCIi@Kq@_@iCQoAKy@c@{CQiAIm@U}A]eCKo@S}AIm@Ku@SsAc@{Ci@{Dq@wEm@oEw@qFu@oFU}AQkAGc@a@qCYwBi@mDE_@a@yCEQ_@oCe@eDMaAIi@a@qCg@mDG_@CKWgBIm@EWAO]aC[wBGg@Ii@AMKs@Ku@Ic@OgACSSsAKw@Ky@Ga@CIKu@o@sE}@sGOcA]{B_@iC[cCa@qCIm@ACIm@_@iC}@mGi@yDAICSwA}JwAeKE[CO?AG[u@oFqAgJCSAAOeAeAsH{@kGa@oCIm@?ACOIm@[}Bk@}Dg@mDa@wCg@kDCQE[u@mFu@qFw@oFM}@i@sDIq@_@gCIo@YqBk@yDWqBw@sFSyAU}AU_BQqAM{@q@wEwAcKo@mEIo@Ko@_@kCmBgNACq@_Fg@iD_@mCw@sFeAyHYuBc@eDKm@Im@s@}E[yBIk@Kq@i@{Ds@}Eq@}EIm@_AuGS{Ae@_D}@qGy@aGcEyYM_Aq@wEMaA_@iC[_CAA?EIg@AEGg@AES{AMw@QqAS{As@cF]{B_A_HWiBy@yFCSi@sDu@sFc@}C_A{GIk@Ik@My@e@cD_@mC_AwGIm@aBuLOaAEYs@gFQiACQu@gFSyAS{ACOe@iDU{ACO[yBa@}Cs@}EeAsHa@oCIm@Im@COy@{FKw@k@_E_AyG_AuGeAuHCUa@cDG]AOMeAK{@Go@Gs@Gg@Ca@MeAEo@AIKoAIy@IuAEo@Gw@IyACq@Cm@AMEs@EmAGuACy@Co@KoCAo@EiAEeAEwAEgBKoCIkCEcBG_BAo@KqCAo@M_ECo@Ao@G_BCo@E_BCo@Ao@U_HKiDCeACo@OqFCo@S_HCo@?OMoDAo@M_E_@oL]}LEsACo@Co@G_BKmDS_HQoFWoIAo@e@mOCo@OoFCo@S}GQoFK_ECo@qAuc@S{GS}Gg@wPAUA[Co@OcFE_Ba@_NCo@IoCM_EAo@Co@EwA]qLMeE_@wLKwD]mLE_BCo@E_Ba@uMIyCCo@Co@K_EAUAYM_EIoCWaIAm@G{AMgECkACk@a@gNGyAMkEAm@IiCEuAGaBEoA?KGwAA[ASEeAKqBCk@AYKoBI{AKyACk@CUAWEk@Cc@Ek@AKEk@CYASGk@Es@OeBCYMuA?CGk@MuAWkCMuAYeCE]YaCUiBIk@E[[cCWgBe@qDEWM_Ay@gGs@eFOoAIk@Ik@e@oDIk@Gc@o@eF_@oCsBmOg@sDIk@oAqJ[_CKw@wCqT}@{Gu@oFo@}Es@gF{@mGQqAGg@Ig@Y{BYyByCuTgAcIIq@c@_DWqBwAwKyE}]OgAM{@cBsM?A}@uG]kCIk@wAkK]kCwCuTU{A?AcBmMIk@eBmMGi@_Iql@wDaYmDoW_Gub@m@mEsBkOoGud@wGgf@}Jet@kAuIqByNSwASwAsAwJq@}EkAwI{@qGG_@q@{E]aCCQwAmKUeBUcBWaB_@yCi@kDUaBy@eGIk@i@aEOcAy@}F[_Cu@qFOiAs@eFs@kFMy@Io@QoA{@aGOaAq@cF{C_UeDgVWaBuBqOc@cDoByNyAgK[cC_A}Gm@oEOcAo@kEIq@[}BSuAQkAe@iDAGIi@UoBWgBWwBMaAM}@QyAMoAa@qDe@kF[sDCYCYCUEk@MaBK_BOmBCa@Em@Ee@Co@C_@Cg@Em@?EEo@GiAE}@EaAGqAEq@a@mHCo@_@}Gw@_OYwE[{FYuFy@eOQ{CCo@MsBUwEW}EO}CEq@O}DGuBEoB?MEmBCuCA}C?yB@{B?[?eA@G?{A@gBD}BD_CFuBHyBFmBLuBBa@TmD\\aFPaC^aEXoC@KLgANoADWHm@Hm@Jm@Hm@Fi@DYJm@F]VgBToA^uBRmAxA{HJk@lAmGdJof@Jk@lAmGJm@d@gCr@sDnFkYbGw[tAkH~BcMh@oCZiBh@uCf@iCX}AHe@b@eCj@qDb@cDb@cDb@wDXiC@MFm@L_B@GDe@Fo@NkBN_CFo@Bg@@EPaDP_ENsDJiDHmDBkB@u@@w@@mA@wA?sB?gB?y@CiCAqBCmCIcEKcDGqBa@eMG{AK}C[_KYoI[{ICw@?ECq@O_EM}DCo@g@mOOiESqGEiA[gJYsIIaCCo@E{ACs@UoGWoHk@eQ[yJ_@oLCo@QoFCo@KwCGwAKkCKyBGgAMwBM}AI_AGm@QmBy@kHKq@_AcI]iCWcCqAeLuAyMuAcN}@{I_@eDGq@KaAi@mFEu@Gk@Cm@EaAEgBEaC@}@?o@?KB_ABuADaAHkANsBRsBZ}BDYBQDOLs@`@eBR_APq@T_A`@_BZkAZkAl@{B~@qD^uAt@wCVcAh@aCXuAX}Al@iDR{AReBReBPkBLyAHqA@[@SF}@HgBF}ADmCByBHoGDsFLmKXgZJoJJaK@sADmF?A?s@@wA?u@?A@W?Y?m@CiA?SAe@CwAC}AKoB?C?GCg@?GGkAMuBGq@IkAK}@Ee@AICWQaBWcBAKAEIg@QoAQkASeAY}Ac@oBa@cBU_A_@sAg@eBk@cBk@aBuAsDQe@cE}JcI}RqA_DyBoFuBgF{EoLa@cA_@aAoA_DaBaE[w@]y@Qc@Sa@y@qBq@eBSe@Uo@Qi@Uo@K_@Ka@IWGY[_BKm@Mw@MgAIm@Ec@Ek@Cg@Es@Ai@A_AAo@?q@@{ADmADs@Bk@@ODe@Fq@Jq@v@iGzAmLf@cEHo@VsBPmAh@oEt@qFv@_GR_Bh@gEdAeIbAqIb@gDTgBbAyHbAkIn@yF\\cDb@iFZ}EX{E^wJJgEj@cQp@{SD_BL_El@oRVmILaE@o@PiFBu@D_BBo@`@aN`@mMXaJHoCTaHNmEH_CNkFFkBJ{CHwBLsD@o@Z_KHsCPoFPoFPoFNwEHcB@_@Dg@B_@Dc@D_@Hu@?EDWF_@PaAN{@Li@Pu@Pm@^kATq@Xq@b@aA^s@^q@p@iAVc@jDuFf@y@Va@bE{GtCwE@CVa@p@iAVa@LUx@sAfAkBj@kAj@kANc@f@yANa@@ENk@H]No@Nu@@?F]BMJm@DUJ{@@I?AJ_AH_AFw@@]Bw@DmBByB?U@q@BqIBqKDqT?gADaGJcIHgDHsB?OJeCHeBXuERaDp@kIv@{Id@wFf@oFZmDJsATmCViDJuBBi@Bm@BuC?s@?uAAqBEyAIoBQkCG{@OcBOiAKs@Im@Im@Io@eAcIg@cEa@gD[aD?IO}BGsAKuBGsBAc@EeBCuF@qBFkDJqCFuAJoBJ{ANoBZyCZiDTgCbAeJ~@iJ\\oDp@mHfAgK`AgKhAoLT{BrAaNLqAjDy]Fm@hAiL~@sJx@iIFm@f@mFViCbA}KzDaa@h@{ERqBXoC~@oJd@cFb@eEj@_G\\kDj@{Ff@gFz@qIn@_Hb@eEn@wGj@}F|@qJl@aGNuAhBqRf@iF|@wIpCeYl@kGhAcLlAeMr@eHPgBd@uEt@uHpBkSRsBdAqK^mDRkBl@gGj@_Gb@iEh@wFXsCXmC`@cENaBh@wFRoBt@kHj@{Fr@iHh@uFlAkLp@mHbA_KPmBRmBt@}Gb@iDXmBZwBPcALy@RoAbAqFbBeKVqAh@aDpAuHv@sEh@aD`@{Bp@{Dv@uEn@sDd@kCn@uDV{AX}Ad@mCl@iDvAgIJm@Hg@r@aEx@{EJk@n@uDl@iDf@wC\\sBBOt@cEzB{M\\wBb@oCn@}ETiBRoBZwCFu@JsALuAViDN{BLkBLmCJmCNaFFuBFkDFkELyJJsIHoH?QDaDn@sg@v@eo@VaTJaH^q[ZaWFqDt@sl@BmAJkH?AHaH@{A@o@HaH?C@k@RaQ?C@k@HoF?s@@o@B}ABsCDoCBoCBoB@_@@o@BsDJmHFyFJgIXaT?o@DwBByB@o@L_KFqF@o@F_E@o@@_BTkQ@w@Bw@LqL@o@RgQDuDNyKPwL@u@@}A@o@?C@m@?AB_B@}AB}ANaLFsEByC?M@a@?Y?U?_@AyACcCMcLC_BMaKG_ECuDI_HC_BAo@KqICgAAgACoCAo@EmD?SAo@K_KEqCIuICoBEqBKqIAo@SqOEaDC}BAo@G_EEaEM_KAo@K{IIkGKkKIkHCoC[qUUaQA_BC_BK}GCuC]qXAy@A{@KoI?K?qB?o@?i@@a@?]Bu@@m@@W@Q@YB[B]Fu@Bc@D]D[BYJq@PuAD_@F_@Lu@Lo@`BwIpBuK`A_FXwAd@gCxA{HJk@@?DUz@}E`@uBxC{OXyAd@eClAmGXyA`AcFb@cCvBcLTgABQp@uDDQD[TmA@KNeADUR{ABSJy@BODe@Ho@Di@F{@`@cFXeEn@{JRmCV}DJ_B^kF?IPeCJ}ADo@Dm@JyAn@{Ij@aIDo@Dm@b@}GJ}ARoCJ}AJ_BPmCJ}AVyD?CL_BJ}ADo@^mFDm@@SB[J_BX{DJ_BDo@b@{GdAiO\\mFX}DJ}A\\aFRyCPmCDo@Do@j@kIBW`@cGd@}GDm@PkCDq@@IBe@@QB]DaAFmA@O@_@Bw@Bu@BqABkB@{A?oC?o@AaCK_M?o@E_EA{@?e@Ao@CoCA_B?o@Ao@Ao@GqIC_FEoFAq@CoFAo@?AA}AAo@AaBC_EA_BAo@A_B?q@Ao@AoCCoCA_BAaBA_BA_BC_BA_BAaB?o@AoA?OGqIA_BAo@EoFAo@?q@CoCCoCEoFC}BAcDAo@AoCEaHI_KAm@?m@KcNA_BAo@C_EEaHEgFGkDA]Ai@C{@GeBE}@CSCq@K{A?AKqA?KKsAGm@Gk@UgBS_Bc@aDQcAKm@WyAcAgGMw@Kk@}@cFKm@G[}@sFKm@qA}HeAqGkAkHc@mCgAkGc@gCkByK_@{Bs@aE}AkJKk@Km@c@gCW{Ac@gCKm@WyAKm@Km@Km@w@yEOu@y@wEGc@Ic@e@oDQsACU?AC[CQEk@OkBEe@Em@AKCe@Cc@E}@Ck@AUAYAYCu@Au@Co@?IAo@?E?i@Ak@?]AU?E?oA?I@o@?K?e@?M@u@DaBDqABw@Bi@@i@Bk@@IBi@JcBJgAHaAPmBLgA@IFc@VqBBYfHwg@Z}BHm@f@wDHo@PmA@MR{ADYBSBQFe@LoAHs@Dk@Fq@B_@@OBg@Dw@Dq@Dq@Bm@FyABy@BiABaB@cB?cA?{@?}AAo@?k@CoAG_B?AG}AAMGuAGaACW?KCYGy@Eg@?EQqBC[Go@Gm@AM]mDGo@wAcOO}AWmCGm@QoBE]Gm@UmCWmCO}AO{As@iH]kD_AoJOeBm@yGGo@_@_EOyAo@yGg@kF_BsP_AwJGm@Go@[{CKmAGo@O{A?AGm@Go@CMMiAKq@Im@ACIi@_@aCAGIm@Km@Kq@k@qDKm@O{@G]m@}DeAyG]{BKm@m@uDIm@W{AU{Aw@cF{BwNiCcPUyAIm@c@iCk@wDKm@o@aEkAuHeB{KcAqGKm@y@mFSqAcAqGKk@EUEYKw@Ku@QwAKaAAOO}AEg@]cEYmDa@cFuBcXUmCKqAOwAQsAMgAU{AU{AEWWqAo@aDc@mB[mAU{@_@sAe@wASo@m@eBYu@a@iAc@gAy@uBa@kAIUc@kAeAoCCESo@Wu@So@Qq@[oACKMi@Mu@Oy@Iw@OoAG{@ASAGE{@Ew@AgAAk@?]@{@?WB{@@g@BY?QFy@Fy@Hy@Hk@@MLs@ZgBBKVeAPu@^kAVy@FOJYVo@x@kBfAiCzCcHLYLYRg@Zq@`@_AtB{En@yAp@{AbB{DjDcIvDuIdCyFp@{Af@eA\\m@\\o@f@y@r@gAd@s@PUr@_AV]p@w@p@u@|@}@d@e@VW`@_@b@_@fA{@`BiAh@]BCpAq@d@W`@Ud@UdEsBbD{A?A`@U`Ai@zA}@n@]b@[d@_@x@q@b@a@BAJIPQRQr@s@f@g@@A@AZ_@Z[NO|@kA@A@AX]Z_@n@}@h@{@j@{@h@aARa@Tc@Rc@h@gATg@BEd@iAJYDIPe@Vq@Vq@Ro@Ts@BGZeA\\oAX_ABIRu@f@iB\\mAV_AZiAn@cC^oAjB_Hh@oBjAeE@GpAuEBKlAkEvCoKlDkM\\sArBoHv@sClFuRXaAtEwPjHsWxBeIPi@Nk@pAwENk@rBoHr@gCfBeG@C~AeFTo@Tu@Z_Av@{Bl@iBb@oAd@oAbAoCf@sAdAkC`@eAn@_B|@yBr@cBv@gBjBkEhB{DHOnAkCh@iAJSdBkDlBqDdCuEbBwCNW`CaEVc@vBsDvBqDpBgDhGmKb@w@t@wAPa@p@wAN_@Pe@b@iAv@yB^iAf@iBb@eBXoA`@gBVqA\\oBVkBVmBNyAJmAJsAL}BHeBFwB@o@DgCBmBR}NJ{HXoRJmIByBDqBDgB?GFqBBu@F_ABWHsALoA?GLoAL_APqARqALu@D]VoAVqAHa@No@Ty@FWNk@lAwEZmA\\sAn@eC`@_BDKd@iB\\qAb@iBn@eC\\oAd@mBn@aCV_ALg@f@oBb@iB\\qA\\oABMLg@x@{Ch@gBl@aBn@cBd@iAd@eAh@gA\\o@Zk@Xi@R]p@cAh@y@Xa@`@i@BE\\a@n@w@r@y@`@c@POb@e@r@o@BCXUZYf@_@t@m@d@[nAy@nAs@x@c@xE}BbAg@`Ac@bBy@hCoAvBcARKpAm@|@c@f@WnAm@|@c@z@c@hB_Ab@UdB}@b@W|@e@vDwBfAq@nAu@z@i@f@[v@g@jAw@|@k@v@i@z@k@jD}Bd@[zB{AbAi@dB_AhCmA`Bm@`@Ol@Uv@Ut@UdAWbAUfAW@?l@KpASXEREv@M^GBAhAQx@M|@Qb@Gl@M`@I~@SdAYx@YjAa@n@UdAa@n@[h@Yn@[x@e@b@Yj@]^WxAiAHGb@]n@k@JKVUDETWXY^_@v@{@DEpA_BRYZa@p@aAVa@Xc@lAqBTe@n@mALYDIh@iAf@oAN[To@Pc@f@sAXq@Tq@vAsDxEgMzFeOx@wB?AhCyGPg@JWZy@x@uB@A`BiENa@|@}BPi@Pc@bBmEPg@tBsF~IuURi@rBqFx@yBjB{Eh@uAFO^cApAiDN_@Vq@x@uBv@sB?A`BiEhC}GlDeJXs@`CoGnAcD~AeE`BiERi@\\_A|B_G@A~AgErAqD|A{DDKTm@x@sBJYFMFSBEtAoDDMrAmDbAsClB}EBGx@}Bv@sB|@eC`@gANa@d@wA?CZeAZaAJa@Nk@Pq@Jc@d@sBb@_CRkATuABIR{AVoBTmBLeAXwCHy@B]Fu@PgBL_B@MT}BD]XwCPcB^uDFs@RuBBWZoDPiBD[HaA@CDi@D]H_ATyBBQ?AFm@N}AFm@Fo@D[HaAJkABQRyBBQ?CDk@LmA@OFm@N}ABWJeALiARqBH_ARsB@GN}Af@iFN}AJiABSb@qDJu@Fc@Lw@BOLs@P_ALo@Ja@Pu@@Ep@mCj@mBBIL_@Pi@BKL[l@_BLYx@iBp@yATc@b@y@`@u@v@qAvAiCvAmCxAkCl@gAvAkCl@gAlBoDb@u@b@w@zB}DtBuDrByDfCqEj@cAf@cAl@gAjA_CDKh@iAb@cA^aAh@uA|@gCX}@`@sA\\oAH[HYRw@XoABKLi@?CVmA^oBNy@Ny@PqARuATkBv@_HjBeP@IHm@l@gF@Sj@aFb@uDZoCHm@?IFe@~BkSt@uGHq@t@sGFm@R}ApAaLP}AD_@\\yCFm@ZkC@IpAeLRcBf@kDRoAf@kCXsA`@iBZkA\\oA`@oARo@`@oAn@eBJWL[DKTe@FSf@gAXm@Zm@DGTg@j@aAj@cAj@_Al@_Aj@w@n@{@rAaB`AkAl@m@FGRSbAaAfB{A`BqA\\WBCvAgA^YFErAcAHIRO\\Wl@e@l@e@^WHIdBqArB_B|AkAjBwA`CkBbAw@r@i@h@a@pCwBx@m@~AmAzBgBXS|GiFzDyCpB{AxC}BtEoD^YrGaF\\W|AmAt@m@b@_@ZYFGt@s@b@g@NQX_@FG^g@d@s@FIh@{@PY\\m@Zo@f@gAb@gA@APg@BGj@eBRs@Pq@Nk@BMXoA\\wBRuAJ_AHq@HkAFeADu@D_A@s@@_A@yA?sC?_B?qL?_B@sE?qAAoA?m@@aH?o@AqC?o@?qFAaH?mA@{A?q@Bs@@i@F}AJaBN}ADWLkAZoBVwA\\sA?ANi@^sAHUFShAeDb@iA@Gd@oAhEiLjVuq@|AmEXu@jBiFjCuGj@qAvA_DN_@zDaItImQxDaIpZon@xRaa@jB{DdCcFxDaInEaJTe@BIZm@`CaF|CmGbTic@`FcKnAmCl@wA@ARg@d@iAp@oBp@kBd@}An@wBl@aCl@wCf@gC\\oB`@kC\\sCTgCd@kF^kFXeEn@}I`AwMn@aJt@sK|AsTPyBz@_Mz@wLL{AVoDTeDN_BNcBN{AX{BXsB\\sBRkA\\gBl@eCXkAVaAZgAb@{Ar@{Bb@kAb@iAzAuD`AuBdAcC|BiFTg@Re@@CjJiThC{FfC_GrA{CfB_ETi@j@oAx@kBVi@Te@Zq@`@w@pA_CbAaBt@iAn@}@l@y@v@cAv@_AZ]rAyA^a@|A}Al@m@pBsBtG_HRST[`B}AXYfJsJ\\]FIhBiBdAiALMDEnAqARQHKZ[tAwApBsBhEkEZ]lBkBx@{@xE_FdIaI~AaBn@m@~A_BRQHIPS`B}AZ[x@y@BANOZ]HGvAuA`@c@h@i@HGRSFGxAwAtAwArBmBnBmBpCmC`@a@ZYX[r@u@`A_AfAkA`@c@\\e@\\a@b@o@LQZe@n@cAr@oAp@qAl@oA`@_A`@eA`@mAVs@Ts@V_ARu@^wAv@}Cb@cBr@kCZgA^kATo@Vs@N]f@kA@ERc@Te@h@_At@kAVa@Za@p@{@x@}@^]JKz@u@l@e@d@]h@_@l@]rAq@nAg@d@Q~@WrA]~AYpB_@xAU`@GrEu@fAQ`@IlCc@rF}@zDs@PChDi@fBY~HoAtF_A@?`@GjDm@h@I^GlAUhAW|@Sz@Sd@Op@SbA]VK~@_@jBw@|Au@hGqC~@c@|DkBlAk@|BeAn@]zAw@|@k@vByA`CiB`Ay@r@q@j@i@x@{@|@aADG\\_@p@y@|@kAfA{A?AbAyAx@uAl@gATa@Vg@j@iALUn@oAj@iADI^s@nAiCpCuFt@{ATe@@CjByDHSfA}Bn@sA|BiFtA}CPc@nCmG`AyBRe@@AhAkCp@}A|@sBhBcEx@qBpEmKn@yALYtDwIz@qB@Ax@mB`DqH^{@xFqMv@kBx@kBfBgEf@gARg@zBiFrAyCbHePzBkFlCmGZo@`A_CrBwE`LqWrA{CVm@lDiIpAyCv@gBpAyChBiExD{IhAmCpEgKdBaEzBiF|@uBlG}Nh@mATg@zBiFRg@nCiGXq@h@kAxAeDbAqBj@cAp@gA`A{ArAeBz@gAhAmAvAuAjFiFpAqA~A}AfBeBjAiAtAqAfAgA~A}AhBiBv@u@lBkB`A_Ax@y@z@w@jDkDjEgEfAeA`AaApCmC`A_A~A_BtAuA|@{@l@k@j@m@nAmA|@}@~@_AfAmAv@_AnAcB`AwAp@iAfAwBf@eAVq@d@kAVm@`@iA\\iATw@Rw@\\wAh@gCVsAPmAT}APoAZ_Ch@aEl@oEZ}B`@{Cb@eDT}At@yFNmAPwARoB`@wETiCj@mHh@eH|@gLn@iIHy@?GFs@p@iIpAsP`@aFj@eHjAiOV_DF{@TkCDo@b@iFzAyRl@sHh@uGT}CRkCh@{G~AaSdFoo@bC}Zh@iH\\mE^uEZ_E`BqS`@iFXkDVeDH{@Da@Hu@Hq@Hi@NgAXoBRkAFa@N{@Lk@PaAPu@Je@Le@Ps@J_@ZmAh@eBPk@h@gBtAoE|@wCjAuDTu@r@aCfAoDj@gBRo@tB}GpC_JrBwGBKrByGdAgDv@iCt@aCxBeH|@yCbDmKr@}B|E{OfHmUrBwGp@yBbAaDdDuKjBaG~AgFzAaF~DsMfDsK`BoFxBcHVy@bAcDfAoDr@aCbA_D~@aDv@eC@Cf@_Bx@kCh@aBlA}Df@{AL_@Xw@Nc@Tk@DKHSVq@Ti@Zs@?Af@gAXi@Zo@\\q@Xe@HOz@yAlAmBj@y@LQV_@Za@X_@d@k@\\c@bAkA`@c@dAeAf@e@p@m@b@a@lAaANMbAy@l@e@t@m@xAmApAcAr@k@tBcBrEqD|D_DxC_CjCuBf@a@`CmBhByARQvDyCDC^[pDuCdAy@\\WPOh@c@VS`@]\\WZU@Ax@q@TQf@a@\\Y\\W?APMdCqBpC{BDCdBuAxCcCtDyCn@e@nB}ArEsDfBwAjDqCf@a@xBcBlCwBvFqEbAw@dA{@hAaA~@{@nAqA`AgAbBoB^g@n@}@`@k@|@sAd@w@j@_ADIfAoBd@aAx@eBDIRg@FOVm@`@_AhCsGhCoGb@eA|BwFt@mBfBqEnA}CtAkD|A{Dr@eBdDmIhEqKnA}CRg@hGuOz@sBpBaFnF{Mz@wBzBuFN_@dBkEn@aBZy@tCiH`CaGb@eAHWLWHWHSXq@z@uBVo@JWPe@|@yBXs@b@gAd@kAl@_Bp@mBZcAJ[h@oB^oAPs@Ns@j@eC\\gBRgAN{@ZgBZiBTqALu@TsATmAD[Ls@ZcBTwAzAwIxDuTV{A\\mBd@kCb@eCx@}ELs@TsAr@}Dr@_ELw@`@_Cz@_FXcBRiAz@}EbByJJi@N_AZgBBKJm@DUVyA\\oBHc@Lw@DSDWBKXcBh@_Dr@gEVyALo@L{@Ly@NiAD]RaBFi@B]TcCNkBNmBFy@@ODe@RkCNiBVkDNoBFw@Fw@HiATsCJsAJsAXcETkCh@sHXiDDs@XgDn@mIf@uGh@iH@GBe@R}BX_Ev@gKZaEVgDNiBDm@@MXmD@UPwBDm@RmCFo@nAsPb@{FP{BL}A?E`@eF?ADm@J}APcCNgBL}Ar@cJHiAPaCP}CB_@@Y@QBeA@[?[?[?u@?Y?I?UAa@Aw@?YC_@EeACg@Gw@Ei@CWKgAOkASuAEYE][oBq@kEUwASmAKu@Ks@I{@CYE]Gu@Cg@Ek@Ai@Ci@?CCmAAy@Au@?y@?eA?oB?o@AoC?_B?cB?mJ?gC?cA?Y?oBAwA@mB?MAiBAuf@?o@AuJ?wC?o@?_Q?o@AmI?yJAoE?oJAoA?oA?cE?yD?qD?s@?cE?wC?y@?{AAuHAwP?mP?q@?yL?{EAiA?yL?_K?iCBaDHaDF}AHkAJeBFe@JiA\\gCJo@Jo@Lm@RiAXoA^uAh@mBh@cBn@gBh@}ApFsOX}@BIZw@@GL]Xy@Z_AJ[v@yBv@yBb@mAlAiDbB}EPe@nC{HNe@r@oBzAmEVs@|C{Ib@oAl@aB`@iAl@gB\\_Ad@sA@EPe@l@_Bh@oAb@aAb@y@j@cAr@cALMTWZa@`@c@r@q@r@k@tA_A~@e@`@SbA_@v@Un@Ol@Mp@KHAXC`@En@EtBKz@CzAI~FUvBIp@E~AGvRu@t@CpCM^A~CMd@Cf@C`BG~@ClAGhAGv@Cx@ETA^AXAl@C`@C`@Ah@Cf@Az@Ej@Cf@CnAEbBGb@Ar@EfDOpEQtFW~@EbACt@CvEQdHYTAnBE|@Ef@Ez@E|@EF?fDOtESH?xGW`AGH?nAE|DQF?lCI|BIv@ExBY~Aa@p@Wn@W\\Ol@_@h@[z@o@VS\\[`@a@`@e@X]Za@LUj@}@`@y@N]Zq@\\eANe@ZoAPw@Jg@F]l@cDLu@@KN_A^uBFa@p@sDr@cEHa@xAoId@mCHa@N{@TmAP_A@Ar@eE?Et@kE|@_Fz@aFbBqJ^}B@E@E^qB~@uFd@eCh@{CVyAb@iCVwAdAaGd@oC`BmJbCgNj@aDfBeKf@uCb@gCj@aDp@{Dt@uEV_Bd@sDZgCTsBRmBNsANmB@ADm@Ba@PsBHsAHuAJuAHiBFaADoADs@?EBc@BsAFqABuADsB@g@@k@@{@BmB@oB@mD?yD?yC?K?eB?oB?yD@mSAgL@}X?eF?gF?aC?q@?yJ?o@?qH?aG@eF?mK?wF?{A?o@?}D?o@?_B?}M?mK@]?]?wABuA@q@@c@Dq@Bc@Fu@NuAJs@TmANs@Rs@Rq@Ro@Vo@Xm@Xm@Zk@Zi@\\g@Xa@V[`@c@h@k@XWn@q@d@a@tJaJdB{Ar@q@`ByA`@_@nAmAzB}BzEoEbKoJbB_BvCoC`@_@`@_@`@a@dAaA^_@RQHIf@i@NOZ]FGRUZ_@r@y@\\a@NSl@y@l@{@NSJSXc@T[R[`AcBd@{@v@}Ar@yAr@}An@_Bb@iAJUz@aCRk@Xs@Vo@Zy@Rk@Tm@Na@Rm@Tm@Ne@Pi@Tw@\\mAPu@Ry@R_AP_AN_AL}@L{@NmAJaAH_AH}@HkADcAFyA@w@BgA@q@N{M@o@FoFFyFH}IDsFAiCE_BCo@AQCo@A]GkAIeAYsD?Ac@_GKiAGiAGeBAu@?a@@oA@m@Fu@FaAHu@N_ALu@Lk@T_Ad@wAVq@`@}@t@oAd@q@f@s@hByBl@u@nA_B`AkAz@gAnAyAhAwAp@{@tAeBZa@^g@RWFIXe@LUFINYP[h@oATo@Tu@XeANq@Hc@@GHk@Jo@JcAFw@Bo@@OBg@?G@m@FcDFaED}BFmBNuBNsAF_@Hc@Ha@BKJc@Jc@@ANe@@EJ]DIL_@BGHUP_@Vi@`@y@x@}ArByDFMVc@FOLUFKPc@Tg@Nc@Vq@HYHSNm@Ry@Nu@Ls@TkAX}AV}A\\eBFYHa@Hc@H]Ja@Le@@CFWFQ?EPm@H[L_@DOHUNe@Tm@L]L]Vo@Ra@DKPa@`@w@j@iAr@wAjAyBn@mAdAoBjBsDz@}AZm@v@yAlA{BpB{Dp@oANYJQTe@JQf@cADGf@_Ah@aA\\i@Zi@T[RYX]^g@DGV[BC\\a@XYLO`@_@^]DEPOLI`@]b@[h@]h@[j@]TO^SRKJIpAs@NGjAo@~A{@vAw@^S^Q@A^SzAy@fCuADCXOfBaA`EwB|DuBlAq@|DuBhDkBdAi@vAy@~A{@rAs@xAu@fAg@l@Wb@Sf@Sn@U\\Mr@Wl@QFCv@S~@Ul@M`@I@?fASj@Ir@It@Gd@G\\Ct@Kl@GjBYtAQLAp@KdAKh@Gr@GxCIj@A^@\\Bl@BfALf@Jj@Jp@Pp@Ph@RjAh@j@XjBz@|CnA\\LZLRFZJf@NLB^HNDPBNBTD\\DXDTBd@DD@`@BB?b@B\\?n@?n@CZATAJAx@IlAOvB[bBWxAS\\EhAMdAKn@E^AVA^?`A?`@@n@@Z@XBd@Dr@Hd@Fd@FZDXFf@Jh@Lr@P`ATzItBr@RjAVtD|@hFjA|A\\pEfAhBb@l@N\\J`@Hj@J~@N^F`@Fl@Fn@Bj@@f@?h@Ad@AF?j@El@If@Id@Kb@Kd@OTIZMLEZMf@SPIRIPKNGn@]rAs@dBaAp@_@t@a@b@Wv@e@j@]p@e@\\UFG^W`@]XS^]n@m@~AyAtGaGdGqFbB}AdC{BLK\\[rCiCHIPOpCiChBcB~BuBtCkCJIdB_BzAuAFE`B{AfAaA@A`A{@d@c@~A{AzAsAtAoAt@o@t@o@JMDCTUxAsAnCcC~AuAlBsAl@_@ZSd@WLITMl@[f@U|@_@XM`@Of@S\\KPGd@M`AWvA]~@QlBYvC_@XEfBWrBY~@MtASxBa@dBa@nA]d@Mp@UtAe@ZKd@SnAk@`@QLG`@Sj@[`Ai@|A_Ax@i@lFkDbHsE|DgCtCmBPKrCkB|@k@l@a@p@c@^U|CqB`BgAhFiDNI`EkCzFuD`EkCjD{BpFmDnA{@|AeAf@]`@[h@a@bAw@bBsAZWZYTS\\[l@i@`A_AvAuAv@w@f@i@t@w@v@{@vAaBfBwBjAyAbAmA~@oAx@kAPYXa@Va@Xa@b@q@jAkBx@sAz@{Ab@u@dAoBz@_B|@iBz@gBf@eA|@sBl@sAHU`ByDxAmDjEgKN_@BGRg@pA}CRe@JYvAgDj@qARe@L]DI|@uBz@uBTk@`A{B`@cA\\y@fAoCf@oAXy@Z_AL_@Pm@Ne@Ts@Li@X_Ad@qBh@{B?A`@qB`@wBf@kC\\cBn@gDd@cCbJoe@xAyH`E}StCeOrBqKzA{HpBmKDUn@{C^iB^_Bb@gB@Eb@{AV{@Ts@b@sABGL_@j@{Aj@yAnAsCXk@Xo@DIh@aA`GwKfG_LrBuDVc@tFeKrAeCbByCfAqBtD_H@C~C{Fr@sAl@iAj@mAn@yAb@gAXs@^eA|@iCt@cCV_AV_APw@BMH]Le@TcADYLi@?A`@{BLw@Lu@^qCR}ARmBHeAL}AN_C@IBe@Bm@Bg@?GJoC@m@B_A@oA?w@BkEFgM?o@DaJDiJ?o@@o@BoH@{B@o@@oCDmLBqG@{@@}D?ABsE@sB@cCB}@BaABmABm@Bk@LoCV_EDo@Dm@Do@NmCHqA@EHwAVyDP_DDm@PmC`AmO?CToDHuAF{@HcAHy@B[D_@Fq@H{@J_ALaARcBRyAXiBZiBRgAX{A^iB`@iB\\wAVcAZqA`@sAj@oB`@mARm@X{@b@oAl@}ABIRe@Tm@z@uBdAeCdAkCf@kAf@oATg@Re@lOc_@vBiFXq@`@cAhAkCZw@pA_DjBqE|@yBn@cBd@sA\\aAb@wA\\iARw@V}@VcAXmATiAVmAlAiGLi@lAmGzCqOLo@t@qDXwA@KpAsG|@uETkALm@`@wBlAiGj@sCLk@^oB`A}E`AcFx@gEx@sE@E`AqFpA{HLu@Jk@BQZwB\\sBXsBPuAZoCP}ATeCJuANuBLmBFoAHsABg@@c@@KBaAFcBBuA@_@BiA@aBBmB?{A?_B@w@?aE?uG?aKAyC@}D?kC?w@?Q?iA?sA@uA?W@u@?m@BmABaAB{@DgADaAH_BHiA\\{DH}@ReBVsBXmB^sBToATiAViAR_AXeA^uAXeAZcABGPi@p@oBDMPg@v@{BHUZ{@t@yBd@qAb@qApFsOVu@\\aA@APi@J[Vu@HQp@mB`@kAd@oA?Ab@oARi@FQn@cB@ARg@Vo@|AwDt@iBr@iBRi@N_@Ri@Pe@Xy@Ts@Ty@\\sAXkATeAToAVuANkAL}@?CJ_AN{AJ}ABYD_AHoBBw@@aA@{@?wAAqACwACqAGgBKeBIkAIkAM}AMeBOyBSeCM}AOeCOaCGeAE_AImBEsAEiAA]EsAC{AGsC?[EyBEgCC{BEiCCcBAm@AOEeEE_CIaGASAo@EgDIyDG}BGkBAi@IyCKeCw@}SUgGGuA?EGaBO_EAWEcAE_AAe@GgA?UQoECg@Aq@SkEYuGEu@UyDU_DUaCWeCQsAy@{GyAkM]wC]yCQgBQcBOoBAYKyAIaBAQEwACoAAs@Am@CqA?sB@yA@kA@oABcADuAHsBJyBHsANsCNaCNiCRqDLgCNcCNwCP}CLgCDy@PgDJ{BJsCFaCDyBDmB@yA@I?e@@{@?iC?qB?iAAiBCkCCgDEqF?w@OyOAeDCmE?sC?cC@aB@iA?eA@aBB{ABeBHiE@k@FuBD}AFqBDqAD_AF}AH}ANeDDq@Bq@JeBHeADs@F{@JqAFy@FaAH{@Dq@BYBO?Mf@iGFm@JyAV}CRyDP{G@_GOsI_@cGc@yEo@{EcAgG_@gC_@aCOeAUaBYcCMaAGm@MsAM}AMeBI}AG}AEuAGiBGoBCoAC}@EoAAe@?IMcFUaJSwIMwECo@C{@Aa@IoEE}CCsDAeG@aDB_H?]?_B@aC@kG@oD@y@@aG@}D@oE@}G?A@mC?o@?o@?A@iGAwAAaBCeAA[C{@EeAGiAIsAKwAw@gKGo@?CGu@kAuNu@aJu@iJW_D[uD_@aEiBgUYgDGw@KiAMgBKcAEa@c@qFOwBKkBGsAAUCq@Ca@?K?CC_ACgAAiAA_CKgM?KCaDCyFC_B?_AAaA?m@?_A?kA@cA@}@BaABeABu@FqABi@Bo@@I@QN_CJqA\\wD`@kEJkAN{A|A{PjAeMFo@Di@VoCL}AVkCDm@HaALqBLkCBy@FiBDqD@cB?gCCeBAk@CgAAWEqBMmCQiCKuAOgBYiCOkAQqA_@eCq@sDs@yDq@uD_A_Fs@yDc@_CsB{KiAaGKk@Q_AuDcScAoFmBeKsAwHGa@SkAUiBg@qE_@cFOyBCk@w@sMmAwRIqAg@iIWiEy@_N_AqOAM]kFSgDSaD]{FYyEUyEQ}EEqACkA_@qNe@wPCcASiIe@uPC{@AQC}@KmEKkCE_AEeASmEu@mOYoFCm@c@kIc@}I{@{PUsEOaDGkA[iGQ}CMmCCc@g@mJk@aLk@uL]eHY_G]qGSiEq@{MC_@KkBQmCQ}BAKmAcN{@eJyA_P{@cJc@qEiAwLQyBKgBEy@ImBAQCuACuAAOA}AAcE?iCAwFA_P?}AAoG?cH@kBCmLAgSAm@A_Q?gC?iAAy@?w@A}J?mFEgg@?{DAkBAwN?_B?uGAkF?sA?wC?kB?e@@w@B_BFuA?KFy@Do@PkBNoAPoALw@Jk@Nq@Je@T_ADQ\\kAlDkLPk@?C@AH[@AZcAX_AVy@z@eC`@wAb@cBBMd@}B"
                            },
                            "start_location": {
                                "lat": 40.7124754,
                                "lng": -111.8202668
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "483 mi",
                                "value": 776656
                            },
                            "duration": {
                                "text": "6 hours 46 mins",
                                "value": 24352
                            },
                            "end_location": {
                                "lat": 41.1575451,
                                "lng": -96.1455139
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Entering Nebraska</div>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "k}|yF`|~~R?M?GDQ@EL_ABWDe@FgAF{@B_A?_A?qAAa@Ai@?AEm@Ey@Gw@E[C[M_AIk@?A]gCKm@Y}BKu@UiBsAmJE_@[}BkAcIKy@}A{KYsBQoA[cCg@mFEg@Y_EQwDE}AC_BAyAAmC?sA@yk@?i@?q@?iE?wL?aBAgAAo@?o@EwBMiDGqAI{AMaB_AuLuC}^oA_P]sEKeAK}AM}AmAmOSmCg@wGk@kHKuAMqAIeASsC]eE?EC][yDIkAo@gIM}A}@iLOoBM{Ag@yGGm@}D_h@[{DGm@u@mJc@uFc@qF{@eLe@_Ga@aFCa@CWMaBCOImAWyDKiBMmCG{ACa@Ak@AICu@KcEK}GEwGA[?G?AMiYCqFAsBCiFAoB?mAE{HEcLC{EAqDAi@EuLEsHAkC?G?SAmACoE?cBAeCAo@?EAeB?w@C}B?q@CsBAiC?iAAo@?iAA}@AaBAm@Ag@EgBCuAEy@EiBCg@A[ASA[ASGkAG{AGgBMiBWuDGs@KkAQoB?AGk@Gm@Ea@YwCS{AIq@Iq@K{@Km@Kw@U}Ao@_ECKGa@k@_DQ_AMk@CQi@eCUeA[wAEQcB{Gy@eDgBcHS}@wHoZmDgN[mAsAmFOk@a@aBm@aCAEUy@_@}AmAwEe@cBEMOi@{@yCi@eBqBwFuBgFs@gBwCaHs@cBYu@e@gAoA}CQa@IQiEgKyBkFoByEYq@Qc@kAsCYs@g@mA}@uBe@kAgAmCSa@?AOa@u@gBs@aB_@}@qB}EgAgCw@kBcE_KQc@kBoEQc@Sg@q@cBQa@gAkCQc@gAiCm@{AaB{DgAgC_GuN{FeNmFiM}DgKqB}F{CuJq@{BaDuLeCiKm@mCiAuFCI[aBo@iD_@uBs@mEaAiGEk@k@{Dg@{DQuAGo@YgCc@kEo@_HImAOiBUwCKgBCg@KaBEw@C[MeCMoCMoCGeBI}BGsBIcEAc@Aw@E}BEkD?k@CeDA}C?q@?qDBsJ?W?o@@{C@qJ?I?sA@oADkW@cF@eD@_J@gKBuE@wKBoS?}HB{H@gHAsA@mI@uG@wL@cY@eJ?o@?_B?o@@cD?wG@eIBy\\BcKAiLDgj@@mO?o@@yD?aN@oG?mB?o@AkP@eN?I?}J?o@AwD@_AAuG?}G?_A?I?iA?oF?m@?mB?mN?Q?o@?o@?}D?o@?o@?iT?oI?qJ?m@?o@?oB?m[?{B?q@@yZAmH@sN?eM?o@?o@?mCAeADaM@cB?cBFaI@yA?SBmBDmJDoEFuMB{C@aA?eAZ}g@BwIDsE?o@?UBkD@k@?A?QRm\\?m@@k@@oC@}A?A@}AP{Y?A@m@?A@mAb@ou@LsP?m@BmDBqE?o@?o@@sA?]D{EPkU@sCD{G?m@BqC?m@?A@mC?G@e@FsI?k@DmF@kDBmDD}G?o@HmL@o@@_B?m@@_B@}@DoG?o@HmKLcR@aB@uA?_B@k@DmHBaE?_BDmD?E?i@?s@@}A?A?uA?u@?]?O?aBAcAAgBCsDCoBE_Ca@aVEcBAm@Ao@]kRMmHUmMAo@OmIImFe@kXAo@GmCAo@MaII_GGmGCsF?yE@eI?_F@{I?o@?o@@mI?uA?wA?}J@}G?_B?}A?_B@oA?_A?mFB{V?_B?}J@}J?_B@oC@kU@mL?o@?o@?mC@mL@uI?uJ@_E@g^@yQ@kA?iE@gR?o@Dgj@AmEAaH?q@?iBEeZ?wAAqA?M@{AAsHE}FEkDIiDIwCK_DCi@Ey@OsCSqD[iEWeDw@iL?COmCO}CM{DOgGCoBC{B?GAaH?k@?o@@{F?oEA{O@y@?oC?c@?yS?o@@}D?sC?mI?}G?G@eR?E?wG?E?}G?}P@_R?uI?C?o@Bsy@?oJ?o@?k@?aB@uz@?o@@}J?o@?o@@kX?qI?_B?}G?_H@mF?aN?}C?oC?o@@mO?Y?mB?_H@}G?}D?_E?_B?o@?C?iI?o@?mC@_E?kJ?iI?gC@}G?mG?mI?[?Q?]?qB@mJ?_G@}J?{B?Q?]?{C?u@?SBgABsBDqCBkA@_@DcBDy@D}AHaBHaBNkCL{BPaCHgALqALsALuAD[J{@XuCHq@LcAPmAFe@Fe@@GHk@BSHi@Jo@L{@RkAD[DO?A@GBQBQRiABOn@uDzB}Mx@aFtCqQjC{O^_CpA{HpA{Hn@{DJm@Jm@`@eC@Cz@mFt@}En@aEZyBr@cFp@}EZyBZiC`@gDdA_Jh@gFZ_D`AwJ`@qE\\{D?A`@iFf@yGZiEb@gHn@mKL}B\\mH\\gI\\sJNyEHmDHoDF{CD}AJ_GDmD@e@?I@o@D{CFwG@cD@sC@oF?yB?C?K?kECcF?_CAK?a@?A?o@?SCeE?SAo@Am@?AAo@?SCyCAOC}A?AAo@?IE}BEmCGyBCkAAo@Ak@Cq@?A?_@GmBAo@E}AAm@?ACo@?O[_MeAac@Cm@I{DEcBCo@GsCQoHOqFy@i]AAAm@?AAm@?AsAcj@Co@?MKkEGsBAk@IuCEcBEaAGaAEi@Eq@?AEo@AIM_BUqCOmAGi@Gi@YmBOcAWaBg@iCi@gCS{@Oo@U}@YaASw@ACOi@?ACG]iAAAe@uA]aAUm@Wo@c@aAYs@Ym@a@_Ac@{@gBuDcBoD_EmIaDyGsEuJAASc@AASc@]s@oFcLoC{FmDoHyBuE}AeDUe@cEwI{IaR]s@g@cAi@gAi@gAISa@w@ACSa@GKa@s@]m@U_@EIS[KQYc@e@u@w@eAa@k@U]MQ]a@W]CAm@q@_@a@MMg@i@a@a@CEQO[[w@s@II][CAq@m@c@]SSwAmA_CsB{@u@][]YyAqA[YMKcCuBiDuCWSSS[[UWUWWY[c@U[c@m@_AcBS_@AEMUk@wAQa@GSKYIUOa@Sy@Sy@I]?CG[O}@?AM_AOqAKqA?AE_@?GC[AYCu@Ai@AQ?[?QAcA@mA@k@Bm@Bs@FoABk@Dm@Dm@|@cQNuCLkCLcCRcDDu@HeBDuAF{A@iA?e@A[?cAA]A_@Ay@?CEo@?AEs@I}@Is@CQE_@CMIm@AIMk@Mq@WgAAASw@Sm@Sm@Mc@Sc@[s@Wk@Yk@c@w@_@k@W]s@cA{@mAmBaCu@cAeAqAc@k@Ya@W_@W_@U]_@k@Yc@m@eAYg@Wg@Uc@Sa@_@y@Sg@a@cASk@Oc@[}@Uq@Ma@Oi@Uy@YeAEQGY[uAYqAOs@O{@AEOy@Mw@Ee@Im@MaAK}@cC{TOyAYkCOwACQEYqCgXe@iEAEoAeLkBgQIs@K{@_A}Iq@mG}@mIqAaMGo@K}@g@_FYeCMyAMqAe@eFm@}F_@aE_@yDSiBMuASuBy@iIw@cIa@aEKcAMkAWgCS_Cu@kH]qD[aD[{CM{AeBeQgBqQeAqKSuBKkAAKEa@AMGm@KyAOeBWuDMmBQsCOaDOmCM{CI{B?GGcBEkBE_BE}AEqB?CEaCCqC?ICuAA}@?_AAaA?w@?K?eB?yC@wDBgHH}U@cFBiETiv@Tgs@B}GDyKHqVH{d@DuP@mIByJH{h@?s@@s@BaODqXBuNJwk@@cG?{@?iHAmA?uA?kDAyA?sB?sB?y@A{@?M?wFEoWCmU?}@Ee\\A_HAmE?wBAwA?qCAaH?y@?g@AgB?w@?wB?y@@iE@w@@{A?y@FiEDuBB{ABy@?[@[FsB@_@Bw@XcJBy@HuBHmCJqCHkC@a@HoBB{@Bs@B}@Bs@@[@YJwCFuBDy@DuAJmDLkDFqBHmCHyBDmAB_ADuA@y@@y@Bw@BwADoC@yA@wA@y@?y@?[@aE?y@?Q?oEEkEAc@CoCGiEKiEKmDIoCOkDKoCMoCY_GEwAMgCOoDA_@GoAE{@GwAEy@GqA[cHIsBQgFEuAImCCwAGoCCwAAuACsBAwAAqBAuB?oC?oC@wA?sBDyS@gF@}H@gF?oC@qC?y@?c@?{@@i@Fw]@kG?kE@oCDa[@mDBkN@mD?mD@yI@qC@mD?mD@gE@mC?sD@oB?sA@oD@cG?oC@mDAkD?_@EqLEyIAoDAoCAqCAsAGgPCaHAoC?wAEuKE}HAiEAsBAmDEoCCsBEsBEsBIiD?QOkEEgACm@U}FKsBImASiDS{C_@yEAKEc@[yDIcAWcCm@uFs@cGUkB_@gCMcAKm@AEGe@Km@OkAe@mCi@aDyIgg@Km@c@uBk@iD]mBe@gCUqAUqAc@gCUqA]mBUqAUoA]mBi@cDm@cDi@aDm@cDi@cDm@cDk@cDc@gCk@cDk@cDk@aDc@iCe@eCa@cCWuAk@eDc@iCe@eC]mBw@wEe@gCe@kCi@}COy@G[k@cDq@}D]mBcCiNk@cD_@wBg@qCc@iCWwAUqA]iBc@eCUuAc@eC]mBi@{Ce@kCuMuu@e@iCc@iCO{@}A{IaAwFUoAUqAG[e@iCMy@]gBc@iCoAiHwAgIc@eCc@gCa@gCa@iCg@eDc@iDWoBm@_FYoCg@cF[gDUqCSiCe@qGGmACc@c@gIg@gJYaGUgEUiEUiEUmEKuBSmDQiDi@_K{Cwl@IkAAU?KAEGqAUoEs@sM[gGq@sMQkDc@kIOyCQ}CaCee@_@gHWgFSwDCWKsBOqCOmCMuCQkDIyAUgEIuAIyAKsBE{@MgCSoDMeCAOMoCCc@Gw@GuAOoCCq@]yGg@mJMeCKoBKoBIwAKcBS}Dm@uLUkEE{@MqCCk@Ci@E{AGuAEyAGwBEoBEuBEqCEsCAyBA]?uAAuA?mE?uD?_F?sB?sC@oC?sB?wB?iE?oC?oC@yAAqC?{@@kB?kF?}G?E@eG?S?o@?kC?aB?m@?A@wJ?y@?sB@sB?qF@wF?oE?kD@cH?qE?mD?O@cI@}C?{K@oJ?oB@oI?mA@oK@_B?oF?wA?w@@oC?{F@wF?yA?mA?aB@_K@eE?gCBob@?kE@}G?_B?gEBqQ?aG?sA@cI@{Q@sB?K?O?O?u@?i@@oI?cC@oG?yB?eF?I@oF?wD?GB}M?wB@kI@yF@yC@uD?mC?eF@gH?iB@eE@gF?s@?wJBeI?eF@cA?o@?iA?uB?m@?A@oC?o@?gB?uA?o@@o@?_B?_B@m@?S@kG?o@?K?uG@{G@mF?k@@sC?o@@eF@yH@{J@oA?yF?c@?o@@}G@{E?}B?iB@mC?O?oA@qF?mC?[?sB?_E?m@CmECoDCcFEiFCuCG{GCsDEaFCgCC}DGoF?WE}BCwBAg@EqCG{C?OIuDKeEEoCEaCQ_IKqFAWKkEGqDCwAIoEOqGIeEKuDIkEIaEG{CC}AE{BCmBCqBAwCAaD?iC?}B?eB@o@?sD?_C?cF@eC?o@?o@?}F@eE?mD?uC@sD?gE?cD@aE?}D?gE?qE@kD?kC?iK?aD@{K?sM@gB?kA?cG@gD?mM@qK@gN?yC?mF?Q@aJ?{@@mF?aB?}D?kA@qJ?oA?o@?iB?mF?e@?o@@yC?eJ@}F?aQ?yABu[@gE?aE?qA?sG?sD@kC@wC?Q@eCBaCBoBFgDDcB@EHiD?EHmBLuCLaCJqBPaDP{BN}B@GBYL{AReCD[TcCTyBX_CXaC?CFi@R}AXkBXoBXkBl@wDZmBVqAP}@b@yBd@yB@Ex@yDR}@l@aCz@kDv@uC~@eD~@gD`AeDtAwE@EfAuD`BwFrAqEb@eBn@}BDOFYf@qBx@cD|@sDdBgIP_AP{@`AiFf@yC`AkGLq@RwA`AkHx@iGf@yDjAiJxAoLtB{ONqAx@sGHm@R{A|BqQlAuJT{Ax@{Gp@aFv@cGb@gD@Ev@}G^kDp@cHReC^iEDq@Z{EVmEXuGToFLaEDaABaAVkIBo@JkCPsCPcCJyAj@aFbAmH`AsGfCaQDYBMBMBQBK?G@GNcAL}@p@sEf@kDXuBReBJeAXuCPuBFm@JmAJuAFcAHeADo@PiDHaBDgAHyC@UBk@B_BD{A?m@Bi@BiC@aBDsRDuNBiJ@_B?_@?O@iD@uD@}BB_E@aBBeABcBD_CB}AByBJwDHgEDkCFaDDuBV_NLyG@o@DqABmB@m@D_BH}DPuJFwCNqIHyDNmEBoANgDZ{GJiCPwDDeARqEXyFTwEFqAHaBRmERgEPcETkFRgEHsCHkCH_DHaEJ}I@iBJkXHmR@o@?_BBgDDsK?o@BsDDsKD{HFkMBcIBsF@sD@gBB}ADiLDsHFuEBmAPyGNmEPoEPwDDm@NoC\\{G\\yGn@cMJaBDaAHgBb@aIHcBd@qJTeEV_FXsFz@yPVaFDy@Dm@HcBPmD\\gG\\}GRwD^sHbAeSl@_LZgGTgE\\oGFmAV_Fv@uJ`@oEPyBRaBLyA~@oI`@{CZaC`AgHr@gE\\sBJi@@AJi@?CH_@^oBdAgF|A}GNs@r@aDz@mDd@cBR{@v@oCvBoHrD_LtAcExAqEBGfHcTvEmNd@sAfCyHpBcGrA{DbDwJRm@|@kCdGwQhJaYVs@Vu@d@uAb@sAdAaDpAwDJYDOxAmE`AuC`B}EtBoGj@cBxDiLVs@Rg@DQbC{GTm@rFcNtDeIrBaEv@}AnGqLj@oAp@oAfBgDz@{ArD{G|C{FlBsD`@s@fEaInGqLLSpCkFdBaDdIoObAiBpCkFtAiCnCcFrCoF@ATc@Te@pAgCtC_GtBoEtA{CtAyCvBwE~@sBfCqF^{@lC}FvByEXm@fCsFh@kAN]N[hAgCzAeDrFsLbEaJlFgLr@}ATe@tBuEFQ`CeFRe@hA_Cv@eB|BeFTg@Te@HQbCkF|@mBjFiLr@{A`AwBf@gATe@L[FKRe@tAwCTg@Rc@@ARe@v@aBFOhF}KBERg@zAgDLYrCkGrA{Cj@kAh@kAvCiHlByEpCaH@AbBgEJUn@_Bb@cArAiDlAyCx@kBr@eBJYXq@@CdBiEvAsD`@iA`@iA`@iANc@f@yAb@qAdAmD\\kAd@gB\\mAl@aCt@}Cr@_DJc@Li@VoALu@^mBTqA\\kBTyAn@wD`@cC@Ch@cD`@iCpA}Hj@qDPaARaAZmAh@iBRq@Tq@l@aB`@eALWJWXm@LYXk@Xi@LUPYf@}@\\i@x@qA`@m@z@oAt@kAj@}@\\i@^g@bBiC\\g@dDeFdBmCp@eAvBeDBELUf@{@Xi@Xg@Vi@FMJQr@}AXm@Vo@Vo@h@sAh@wA^kARo@^mAPm@J_@Rs@Ps@H[XmALi@R_ATqAVoAHg@Hk@Ju@`@uCFe@Hw@P}AJqADa@HeA@KJqBLaCDqA@g@@s@BgA@sBBmC?C@gC?_B@uA?{@@oCBeGBgFB}I@iC?UB}G@iB@cFHqTByN@oCFiNFkV@kF?_@DiG@_GDuORwr@Jk^@sALy`@?eC@eCDkK?o@HuRA{HHeWBeF@eG?sBAaH?yIAgH?kDAwO?sDAsB?[CuBCsBE_DE_CCuAGsBGqBASKyCKmCQqDu@cPaBi]u@aP?As@cOi@qKs@eOe@qKQmEKiDEgBEgBEwACaBAcBCyAAw@AeA?yAA}A?eA?uAAuA@qB?_A@aA@}@?gA@U?{@BaA?_AB}@@a@@m@BgABmABeA@SBy@BeABy@Bu@DqA?KBs@DsAHsCBo@BaADuAH}BNaGDkADyADoAB{@BiADwABi@FoB@_@By@DwABcABo@BeABg@H}CDwALuEHuBJqDFsBFuBHkCFuBH{CDmAJkDHkCLuDFmCLaEHwCLeELuDHaDJkDb@{NH{CLwDNyGJwGDkF@mF?gE?}E?aC@gE?wC?gD@}G?kE?wC@iEAeE@uC?aC?wD?iD?yB?gDDuY?mK?uE@yD?uH@eH?gB@iHAoD?{HAiE?gG?iF?aI?gFA{SA_E?o@?qJ?wU?o@?aAA{H?}JAiTA_R?}G?_D?uEAka@?aIA_I?oJAkr@?c@?qAA}K?c@?kB?wP?qR?MAyM?oKAeAB}IAwGAaQA{H?wR?gDA_NC_L?wF?eBA}Q?E?o@?o@AsLAeI?o@?}G?o@?kG?Q?o@?_JEwT?_E?m@CyT?mOAuD?gEAgJ?eD?o@?}AAmRAiM?cJEy_@?_BAmI?mFA_K?oC?wHAoPAqJ?_BAeC?uNCyXAsEA}M?oC?mFA_B?{DAoMCuNE_[G}W?o@Muq@EiOAyHCoKAsIC}RAmGIoc@?oAAiA?w@?sCAeB?eBAq@?s@AgHCwIAqF?S?c@AkA?M?eC?u@AiD?s@?kCAsEAiA?o@?Y?UAcD?{B?QAi@?qD?S?YAaE?Q?]AeB@}IDmFDoDJuNDsDHmI@gADqFHmK@CDiGB}AB_D@o@@mC@WP{TDaEJkL@c@H_LBkB?c@?K@a@?ADeFJiKHsJFgIDoEFgD@o@DuB@{ADy@FkCJcCLmDH{BLaCNiCT_EPiCLaBVeDJsARsB?EJmARiBZ{Ch@uEJy@Fa@XgC@An@}EVaB@CHi@Hk@Fc@BIp@cE`@}B~@gFd@}BdAgFPy@b@iBb@mBBKXkARu@T}@nA_FTw@BGdAwDf@aBr@_CXaAf@}APi@Ne@Rm@Pg@N_@f@{ARi@`@gAlAkDrAyDbBuElBsFhAaDnAmDRi@v@yB~BuGTm@Pg@Ri@b@qAPg@d@qAd@oAPi@Pg@?AvBcGJWd@qA^gA\\_ARe@\\eAHUvBgGxAaEz@cCx@}Bt@uBr@oBp@iBtA{D`C}G^cA`BwEt@uB|@gC`@gA`AmCp@oBhA_DlAmDv@}BBIx@_Cx@mCdAiDb@}ArAyEv@yC^wA\\{Af@uB@CJg@\\wAl@qCb@uBLk@Jm@Hc@@Gd@_C`@}BX{Ah@gD`@yBNeAL}@XsBl@eEf@sDD]|@kHHm@Hm@j@eEz@yG`AqHrAoK~AeMhA}IVuB^sCbA}Hd@yDHi@ZaCZ_Ch@iEv@eGj@cE`@sCTwAZsBf@_Dt@}DTmAXuAVqA@G\\aBv@kD\\aBFYJa@H]\\yA`@eBTy@FW\\uAXcAl@yBf@iB`@uA^qA^kAp@uBx@gCJ]l@gBx@_Ch@wAp@gBXu@p@eBZ{@^{@b@eA`@cAx@kBn@wAtA}C`BmDtBcE~BoELUtAgCpD{Gr@sAP[DG~IoPrCkFjAwBn@iAv@yAzFoK|GeM|C}Fr@qAnEiIl@eAbB_D`AkBtAqClAgClAiC~AuDlAuCzA_E`AkC\\}@FSPg@jAoD|@sCh@cBxAcFr@kCl@cCp@uC~@_Eh@gCXwABMPy@n@gD~@qFhAqHfAaI`AmJt@cIViDDo@n@kJ@IlAgQVoD@IDk@?CT_DPsCL}AVwDDs@x@eLDg@HcAP}BDo@\\iFFo@\\iFDo@RkCjAeQh@_Hh@eIdDye@r@iJ\\{F|AiT^mFDi@X{Df@yGBg@NiCXuF@[L{B?GXwGLcEPaGFqDHeE\\wOLmF@o@@o@pAsk@B}ABo@LkF`Aub@PmILsGH{DDaBRkIFqCPiIN}GFmCLcFZsOV}Lf@yT@m@FmCD_Bh@yVNyGBs@JwENwGfAeg@J}DVkLp@g[RiIJ_F?MDwBFkCF{DVcKNuIRqFRiJLiGD_B@m@BcAByA@[DcB@_@d@wSRsIDoCFyCPcGBwB@STeJ?GPuHD{BBeAJaF@g@DcA@g@^aQHyD@_@d@yRf@iUh@gUD{BDmBPmIRuIXoIZyGFgA@QHwA`@sG`@eFfEkf@NqAl@eH|@iKxCg\\p@yHtEmh@l@wGl@qGFs@NeBTcCxAmPFo@`@oEn@gH~@qKj@cGTiCN}A\\eEd@}Ex@kJPqBXsCTkCt@uIrBaUb@iFN}An@uGVoCFi@TkCtAcPlDm`@jAoM|@sJFm@Dm@Fm@BQF{@fBkSb@wEf@iFh@iGf@yFJiALoA@KJoAZiDRcCZaDFm@LkAvAaPh@gGrCk[XcDjAkMFu@t@cI@UbAyK\\oDZkDf@wF@OZkDFq@XyCHiARcCP}BF_A?A@EDi@Dm@Bs@HiBBy@?s@@aA?a@A]?YAWCi@Ac@Gq@Ca@Gq@Kq@Ii@Ms@EWI[GWGUI_@IYIUIWUo@Wo@[s@]q@OWMUMSOUW]UYUYUWSS_@_@a@]o@g@k@]yAcAaC_BwA}@oBuAs@q@QOUY[]KKk@{@c@q@MQIQGKe@aAkAeCO[Yq@Qc@k@sAy@yBGQEKMSgAkD[cAa@{A_@wAg@mBe@sBq@wCi@kCi@{Cs@wEe@kD]}CU_Ci@{G[wDi@cHIcAIcA_@sF{@iKiAcOwIaiAYoDuAsQi@qGcFsp@_AqLgAkL}@cI}@yGq@uEc@wCk@cDgAkGsA{GwAeHYyAMk@cFmVw@yDGSScA_@eB_AsEeAgFsCeNy@cE}@kEEOMk@uA}Gm@yC_B{Ho@{C}@qE[sAaA{EuCkNo@_DoAiGmBoJk@mCkBcJaCkLqCaN}B_LA?Kk@?A[uAYwA]_B}DuR}B_LaE}Ro@aDKe@ESQ{@WsAQcA]kBi@cD[qBs@yE[wBc@cD_@_DQsAYsCq@}GWsCY{CUkDOmBUyDWyEE}@KiCO_DS}GKmEIyEEeEAyDAuG?{C?aJ?o@?mP?iL?sI?_D@}L?eDEsO?gAC_BEgDGwDK{DK{CWgHQ}DMuBI}AAUS_DSsCAEa@aF[{D_@{Do@{F[gCCYM_Ac@cDg@wDCM_@qCm@kE_@oCoAcJAAgAaIIk@i@{DyB_PIk@gBkM{AyKM_Ac@eDgA_IE[eA{Hm@kEw@}FOaAiBqM[aCoAcJa@qCq@cFgBkM]gCmAyICS_AaHmBmNgAwHgAaIOmA}@gGeBoMcAkHuA}JyB}OqAgJe@uD_@uC}@{HYoCO{Ai@kGSaCM_BAYMqBMsBYaFKuBKgBCy@E_AGcBI_CG}BGkCCmACsBQyMOwL]a[YaUSmQKuKI{EE_DCiBCyBIiFCcAC_@Ew@OwEKoBU_FIkACo@i@oIm@sHu@cI{@}HyAmLqAuIgAaHy@kFG_@mAaIwBcNuBkNwAiJeAaHy@iF}DsWaAkGeA_HwBqNcByKgDiTs@_FwDqVsByMkFm]{@uF_BeK_BoKy@qFeAeH]kC]sCu@gGu@sHUiCScCm@gI_@iGg@_L{@kRs@}PUwEs@aQeAiTi@cJSqCu@cJsBiUc@aFc@sEaAyKw@oI[iDi@iGc@yEa@eEc@aFe@_Fi@_Gg@aF[oCSiBYyBY}Ba@oC_@gCQiAU{A[kBk@eDu@cEc@_Ci@eCg@eC{@wDk@_C]wAsAqFm@yBmAoEg@kBy@uC_AkDq@cC_AmDm@uBe@gBo@}B}@cDcAuDkCyJwAiFCIOg@a@{AU}@]kAaAqDqA{E_AkD]kAOm@kCwJmC{JqAcFi@wBQw@YkAYqAc@mBa@oBWkAKk@Oy@UkAQy@Kq@WoAKu@Ow@QaAa@kCIi@WyAM_Ai@}D_@oCWqBI{@Ik@SsBYcCKkAQwAUmCE_@S}BQoCIw@C]AOIsAEo@Y{EMeCSyEOmDGgBEqBGmB?CEiBC_BGiDCwCAg@?mACiH@}@CwC@u@DkLDuQ?aD@iG@cA@eG@{C@wG@{FBmAAiEGaHG{CI{CG_BQgDQkCKuAYgDQqBUkBKaAQuAOgAU_BYkBMw@UqAYaBUeASaA]iBQu@Os@_@iBa@kB_@gBWmAa@qBw@wDi@mCe@cCk@aD]wBs@{Eq@}EAKEc@Ky@MeAKeAQmBKoAQcBKwAOqBIsAS_DG{AGkAEqAEy@C{@Ey@Aw@C{@CmACwACmAAcBAoAAiA?uAA{B?sB@eCA{E@gG?wCA{D?yD?wD?sE?sD?oD?wD?iF?aB?cD?kE?}C?iC?{C?gC?gE?mD?}E?sF?gF?_B?kF?oA?cA?[?_G?sF?aE?uA?sD?gH?yE?_FA_F@c@?yB?yB?yB?O?iCAcE?{B?cJ@gE?oJ?_E?A?}B?cF?}D?aD?sC?yC?gD?oE?qC@qB@wBBaCHeFHoDJgELkDjAyX\\eHTsF\\mHPgEh@qLXoGLqCPwDvAc\\TeGFgCLsFB{AF_EBeD@iC@kD?cA@_HBqHHa^@oC@_BD_R?g@ByG@{ODgHDaVBeG@yC?gBByG?o@DeN@mJ@eB@wCH__@DeQDmHDuED_DNoGJcEZmHRuE^eGb@sGP{Bp@sHj@yFv@{G|@gHz@oG~@aHz@uG|@sGv@{Fv@_GjA}In@yEVmBp@eFzCcUpC}ShFe`@jCyRj@mEz@kGd@sDdBgMzGog@nByNb@mD|@sGt@wFv@_G^oCJw@F_@Jy@Jy@J{@LiANsAJ}@Da@Da@B]Fs@H_AHaAHgAZ{DNkCDm@@_@FaADs@Bo@HwBBm@Bc@?KBs@Bq@Bg@?[@S@Q?]BaABqA@uABeB@k@?i@?E@aC?{B?kA?aBCuCEoCAi@Ao@CaAEcBC}AGoAAg@E_ACq@E}@E}@AOC]GwAImAKcBIgAOiBC[M_BMyAI_AIq@SqBSeBQ}AGg@Im@M}@OiAE]YgBsA}Iq@sE_@wBgCwPm@_Ee@aDK}@]eCa@cDAIMeA[iCKkASkBOuAQmBKsAE_@KkAG{@Em@Ec@IkAU{CGaAGaACm@Ek@IiBQiDGqAG{AGqBOiFKyDGwDGmGCuE?yF?cB@iB@iCFgEFmEDwC@k@@m@J_GLyHD_CDwBJwFFcEBeBP}JPiKHgEJwH\\aSXgPP}K@I@o@V_OLcIJgGV{O?[Bo@LkIDgBDgCHeGBmAF}H?mGCcGEsDMsIIeESeHMaDUeEm@kLc@iI_@{Go@uK[yFe@sIo@eLw@mNc@yHe@mIUoEUeEG}@WuEC[e@eJQyCGeAe@yHWeF?Ac@yHa@yHMoBw@iOGy@SuCg@kJQkDOsCSgDo@}K?Ak@eKq@sLUgEKqBKsBMqBMsBMkCMuCKmCGuAEuAMaEEoBGsCKwEGuCEoCIeDI{DGyCGkCGsDKgFQ_IKeFS{IM}GOcHKaFIqDIkDIiEQaIK}FImDKmEKsEOoHQqIM_HEaBIiDCeBEsAI{DGaDQ{IIuDAUEkBEoBEeCE}BIyDQsIEaBQaIKyFE_BIuEEuAK_FGeDKyEEcBIaEMuFKwFEgBE}ACkACmACmACiAIuDIyDCsAC{AGeCKsFM{FOeFIuBSgEQgDQmCOuBWkD_@_EWoC]eD[mC[cCe@iDU}ASoA[uBQeAMs@g@uCYaB[aB[}ACI[_B_@eBOm@CIu@eDs@uCc@cBU}@c@}Am@yByA{E]eAY{@a@sAk@_Ba@eAwA}DsAgDgAoCeBeEgBiEgCiGkAqCsAeDcBaEiAkC{BsFcB_EcAgCqC{GQc@kAqCw@oBk@qAy@qBkAuCWq@iByEmAiDi@{AaAqCIYMc@aA}CeB{FyAmFmAwEu@{Ce@oBg@_Co@yCc@sBe@aCUgAY}Ag@sCk@kDQcASqAUyAQoA[wBc@gDQsAY{BWcC]aDMgAMuAIy@M{AQsBOgBSmCGy@IoAGcAMoBIwAK{BKwBMgDI}BEgAMwEI{DCeBCmBCoBAqBCgD?oB?M?{A?}B@}G?oH?gC?oC?aE@kC?sB?eL@mD?oB?oH@_G?mE?kF?cE@}D?{A?kA@eH?iB@}CBoEBkI@{D@_C?YBuIHsX@gG@}B@s@ByJ?cBDsM@sCBuIDmLDmK@wE?K?a@?o@@o@@}FBwF@eG?g@HyK@{A@mA?aA@gA?i@@u@?W?cCA{A?u@AuAAaCAw@?k@A}@AqBEaCI_GIqEIsFAi@SaNAi@IaGAe@?AAWKsHAYA}@OeKEaCK}GQgLIyEGoEGkDAq@QkLAo@ImF?AAm@?AAo@EkCAm@Am@Aq@Ao@C{A?A?CCyAGcEGkE_@w[EsE?QAo@I}G?c@AK?o@EmC?i@EgBAm@GuDGuCAo@Ak@KuECmACwAW{LOwHGuCCkBEuBE}BGmEAiBAeBAu@AaC?{A@mC?aA@yA@oA@{A@aBHkG^uVL}GTeP`C{}AHmFLmIJaGRwN@o@B}AVmO\\kULmIFsD@o@HwF@o@^yVNmITmOR{MDoCF}DBoA?OB}AF_ENmIJ}GR{M@o@LmIB_BPkLZaRHyFBuBFiDh@k]F}DBmBFuCZgTN_JJyGFqDxAw`ANkKB{AL}H^qTP{KNoJNcKJqGD{B@o@DiCPeMNgIHeGHuHJuDNsJL_JLsGBqBF}DRwKTaIRmERkETyDZqEZaE?A\\iEh@yFb@eEn@mFd@oDp@}Ep@wEx@yFp@}E`@sCbAcHt@oFr@cFjAiI`BeLx@yFtA}JrAmJ`BcL~AgLtCiSlBaNvAcKd@}Cb@{Ct@kFRuAxAkKhA}Hz@eG`@sC`BeLv@uF`EkYhAkI`@uCJ_ABOn@qFb@kEZaDR}BTsCXaEXeENaCDs@\\gGd@oIl@cK@QPaDh@kJd@eIVsERkDZeFj@wJLcCj@aK^mG`@kHn@yK`@yGNqCpCcf@ZsF~@kPtAiVxAiW\\}FPaCZ}Dd@gGXoDb@sFn@aIf@gGt@oJH}@bAeM|A{RDm@R{BfAiNb@uGFoAVyEHaBJeCTmGDuA@g@HmDD{BFkD@}ABcC@sC@oGAmL?eYA}H?iC?wD?cE?u@AcI?uF?_I?k@A_BCmIMoKCmBAGCmBAkAAo@Ag@CcBG{DAsACkBQ{LU}OGyEAcAAu@?i@?uC@mC?WBgCFuCDwAFsBDmAFkAHmBLiBPkCVwC`@_F\\}DXmDl@cH`@}ENaBRgCP{BFo@`@qEv@gJ`@aFpAmOB[^iE\\}DHcAHeAH{@ZyDX_D@OB]@GDg@XkDR}BL}AFu@nAwNb@sF@I@MNcBXeDJqAz@cKh@cGv@kJz@mJJkAZaDl@wGXsCh@aG\\eDPkBJqAxCo[f@gFxByUB_@ZkDNmAD]JeABOLyAVcCFw@^iERwBBUBWd@gFf@iFd@aFTgCfAaL@UlAiMj@iGTgCHw@@CFu@LkAlA{MbBiQtB}TrCqZ|BeVx@yI@UPeBLuANuAz@iJH{@j@}Ff@oF\\sD\\sDNaBRsBRsBDa@Da@^yDLqAz@mJ@SVcCNcBfAkL~AsP\\mDVeCh@sE`@cDb@gDx@uFXkBdAiG^qBx@mER_Ar@kDF[`@kBXqANo@b@eBXmAb@eBb@eBd@gBd@eBZiAFQ`@uAp@{Bp@{BpAgE~@wCzBgHnBqGv@cCV{@|C}JPi@v@eCXcA`@yAXeAh@}B^iBNu@VsAN{@PiAR{ATaBNqAN{AJiAF}@HmAJyADmAFeABeADsBBy@D}FBoCBqCFcIDyCDgG@eAB{B@aA?k@?C?c@DwDDcE@sADqCFuBJcCBm@@CH_BLaB@OTeCTsBZcCPgAPgA`@{BNw@f@aCr@uC^uAr@{Bf@}A`@kATo@Tm@n@{AXo@b@aAt@yA\\q@Vg@h@_A\\i@h@}@h@aAl@cA@AT_@NUdAiBrBkDhAsBv@wAdC{E~@iBXm@`AqB`AwBf@gAlBmErAeDHUb@eA^_AJWjCgHr@uBX{@bA_D|@mCRs@p@{Bv@oCx@wCRu@`@_BZmA~@wDfAkEnEoQ\\wAH[v@_D|CeMn@kC\\sAJa@nB}HdAgEn@kCx@eDbA_Ev@aDRy@^{An@eCdAiEdAiE^yANk@bB_HxEmRhGwVlCwKh@sBBMnBiHvA}E`BsF|D{MxDqMhEcOrA_FXcAhAuEx@iDz@}DR}@VmAZ{Al@aDfAgG`AeG~@mGt@sFj@}Et@cHb@iE\\aERmCNqBJyAToDV{DBU^cGz@{Mn@mJn@_Kj@aJvAwTBe@|@qMPgCHeA|@}JbAwJDWh@iE\\gCb@{CZsBb@uCr@cEr@}Dv@gErAqGd@sB|@{DrAsFx@aDpB_H~AiFhBwFbAsCjFgOr@sBp@iB?AtA}DlD_K|CyIlCuHbB{EdEsLdB_F^iAh@_Bb@sAr@yBfAuDvA_FT}@j@uBpAkFj@cC\\yAx@uD`M_m@zEkUReAbKqf@vGy[VoAbMam@f@cC`W}mALk@nAgGzF}XZ{AViAd@uBXoAP{@p@oCT}@XoAVcAJa@\\mAf@iBj@uBj@oBp@cC|@cD~BkIfNcg@lXmaAr^crAz@}ClAkEpBgHlDkMfAwDj@sBxDiNxByHzC{K`BeGPi@rA}Ev@sCjBwGRw@HWLk@Pq@RaA`@oBVkAJo@F_@Lu@Js@Lw@D]Ju@TmBVmCJuAFy@@QJ}At@wKPkC^iFjBmX~AmUbBqVv@sLfAuOx@_MFy@LeBHy@Dq@Dc@JsANyANgBN}ATsBHs@XmCjAcKlAoK~@gIfAmJxAmMvA}LPwAnBcQvBaRPyAHw@PqARsAFa@Jq@F]Fa@Jg@Ny@Nq@VmANs@Ps@H]Ru@Pq@Rm@Ru@J[Tq@HWPk@L]Vs@Vm@`@iAd@eAVm@Zq@r@wAXm@l@cATc@LUR[^k@Zg@R]Xa@|@sAV_@Xa@^c@\\c@PSr@w@PSNO`@a@p@q@x@u@r@m@|CgCrEsDbBsANM|CeCp@k@t@k@vBeBn@g@pAcAbBwAdA}@vDiDv@s@nBmBFGh@i@tAuAl@o@vA}Av@{@r@u@n@s@~BsCtAaBZa@h@s@`AoAj@s@xB{ClBoCz@oAdA_B~BsDtBoD~AqCvAiCrAeClBuD`@{@`BmD|@oB`AyBdBaEn@}A~@cC`AiCx@uBdB_FrAcEzBmHhA{DlBiHj@uBvAkFr@iCBGj@wBXeAh@qBrA_FzAuFb@aBf@mBlBcHhAiEb@_B`@yA^qArAaFj@wBbBgG|@eDTy@xBkIzAqFbBiGf@eB|@}CZcA`AyC`@qAt@}B`A}Cz@qCrAgE`A}Cp@wBp@uBLe@hB{FtByGtAiEfB}FhB{FvAqEFS~AaF~AgF|BiHrBwGt@_CfByFt@aChAoDtAkEdBsFJ]ZcAp@uB`@qAr@{Bp@wBt@_Ch@eBt@}Bt@aC~AeF~AgFz@mCvAqEDOvAmEhB_Gt@aC|A}EbBqFxB_HjAyDrAeEjAsDd@wAfDqKl@oBdC}HpFcQhDuKjCmIn@qBBGhAqDzA{E@EfBwFh@}ALa@tAyDrAcD~@uB`@_A^u@n@qAd@}@h@gAhAqBhAmBt@kAlAiBt@cAf@s@FIdAwAdAyAx@kA|@mAh@u@RWXa@Xa@|@mAv@gA~@qA~@sA~@qAp@aAf@w@r@iAf@y@Xg@`BqCdAqBr@yAtA{C|@uBx@sBn@aB~@oCRo@n@qBf@_BXaAV}@pF_SZiAlEaPfCgJHYZgAbF{QpGsUzN_i@`DkLt@mCzAeF~@yCrAoEPi@t~@yzCvSuq@dHmUNi@fByFNi@Tq@z@wCNe@\\eAf@cBh@cBf@eBl@}Bt@wC`@eBf@_Cd@cCj@_DXeBXmB\\kCVuBrB}QNqAXeCXeCZyC`AoIRiBPqAViBXmBTqAXiB\\gBXuALk@P{@ViARw@XiAZoAl@_CxNaj@bXocA~Vi`Ah@uBlAwElBgHzCgL~B}IzBmIbA{DNk@T{@jEiP|FsTbAwDb@}A^qAX_AZgAl@oB`AwC`A_DrAwDRo@jAkDbB{EtCoIhBmFvAcEvBoGxL}]lBwFv@{BvCuIz@eC|B{GvBiGxBqGpEwMdBaFhAaDfAyCjA}ChBuE|AaE`BkEpAeDr@oB`BgEz@{BvBuF`@eARg@v@uBp@eBlC_H`BmE~DmK|@}B|@{BlA_DfFaNzC_IpBkFdAmCf@wAXu@`AeCz@{B^aAnAeDxA_Ep@mBvAgEtAiEPk@nAcE~@eDr@kCTy@b@gB|@oDnAeFxA}FhAqENk@ZoA|@qDjBmHPq@dAkE@CZkAb@eBb@eBxByIPu@BIH_@BKJa@`@}AZoAbBwGf@qBbGaVVeA`BwGvAwFhCcK@EvA}Fh@uBRu@xA_G\\wARs@h@wB@EZmAb@eBj@_Cb@eBDOf@qBb@gB\\qAhBmHV_AV_AjAgEd@cBx@wCbAoDlAkEz@yCx@wCx@wCjAeE\\oAx@wCx@uCbAoDn@}BZkA^sAPi@d@gBf@cBrBmH~A_Gf@aBv@wCbAoD\\iAlAgEh@iBd@_BPk@t@qCjAwDxIoZlAaEdCuIv@iC?Cj@kBrAuElAgEvA_FzAcF`AcDd@{ATo@Tq@^mA`@iAp@mB\\_AVq@Tq@Vq@b@iAVo@Vo@Vq@Vm@d@iAp@_B|@wBbB}Dp@_B|AsDb@aAHSp@_BjAoC|@wB|@yBjCiGp@}AxAkDJUtAgDb@cAN]|@wBvAgDr@aBr@{Ar@}Af@eAXo@~AeDVg@LWf@aAjB{DjBuDrC{FhEwItC}FLU~@mBTe@`C{E@CvBiErAmC~@mBXm@h@cAr@{AbAqB\\s@p@uA|A_Dt@{ApDkHf@cAbAqBVi@h@iApAiCnAiCh@eAd@cATg@P]r@}Ar@_Bd@gA~@uBlAkCp@_Br@}Ad@eA~@uBd@gAjAkC|BgFrF_MpCmGRe@rJmT^{@jAkCjBcEbFeLp@wAVm@~BkFbA{BtB{ElBiElD_Il@sAnFwL~BoFpAuC~@sBt@cB`@cAj@sAr@cB?CfAoC~@eCz@{BTo@La@l@cBTq@Tq@^kA^kA^iAjGiSNg@Ni@xBeH`BqFpC_JlH}UzBoHfB{FPk@jBeGtHsVpE{NbHgUbGuRnC_JrByG\\gAh@gBpBqGzDiMtD{LdAaDnDkLlEyNfB{Fp@_CpAoE`AqDj@}B\\sAj@eCz@uDh@gCVoAv@{Dt@{Dp@}DRqAh@cDPoA^gC^kCv@oFZwB\\iCd@cDXkB^kCj@aE`@kCz@oGHi@fAwH@EpAcJj@_Ej@yDxBqOp@{E~@qGv@uFx@{Fv@uF^iCT}AD[T{AVkBf@mD~@qGxAcKVeBbAsHp@uE^oCZ{BjAaIr@aFb@wCvA_KLy@v@wF\\wBHi@v@wEN{@PaA^sBNw@b@}Bb@sBXsAP{@TeAPw@XkAR{@Li@n@mCZkAn@cCb@aB^oAdAuDNi@d@wAp@yBv@cCt@{BbAsCx@{B`@gAl@_B~@_Cn@{Al@{Ah@iAb@eAVm@hB{Dr@{At@{AbAqBjBsD@CVc@`BcD|A{CnBwDpAgCr@uAfAwB|A{C\\q@d@_Af@cAhAyBhBoDXi@t@yA|AyCfAyBdAsBVe@v@_Bh@_A~A_DJSt@yApAiCpAeCbAqBXi@fAwB`H}M`@u@dAqBdAsBnAcC|BmEbAoBjBsDjFaKh@gAfBmDf@gAzAcDbBwDhBmEZw@j@yAt@oB`@gATm@`@iAl@cBNc@f@wAt@_Cp@qBV{@Ro@h@iBz@{Cn@}BXcAp@iCZoAPq@ZuAj@aC^eB`@eB\\eBZ{Af@iCVqANy@Ls@He@RkAf@{CLs@TwAViBFa@RwAVcB\\kCZiCn@_GXiCPqAb@cEx@uH~@mI~@oIb@wDdAuJNsAj@aF|@iIp@cGj@cFf@oEn@cGz@qHn@_GpAmLVuBHs@Z{CD]x@sHxDm]VuBb@cEHq@RoBRkBVsCLsALuAJsAFq@FaALcBRyCNmCFeALcCLoC@[D{@NcETaHZsJ\\qKH_CRwFRcGLyDXmIDoAJeD@UJyCDwAPcFNmDD_AFgALsCRkDLqBZcETuCJmAPsBZcD\\gD`@mDNuAb@gDf@}Dt@eGLcAb@iDx@wGdBeND]Z_Cl@wEZoCjAeJlAwJnBoOTiBv@mGb@gD|@iHn@cFX_CR{AVsBLaAX}B^eDh@cFH}@`@{ELyANmBDm@Fm@PeCRgDFaATwERmEDwANqEHaDDqBFkDDsCBeD@_A?eE@wBAkCCkEEeFI{EGeCEmBIgCCk@GsBKuCsAaa@AIGeBaAiZWoIQuEi@aP?CAC?EEgAM{DCo@IkCw@gVs@_TAa@a@sLW}HaAeZCo@MoDC_ACw@EiAE}BGqCEmCAcAC}AAoCAsCA{C@mFBeI?qARsz@Pkw@B{NFkR@iD@aOEgGCqBQeI_@yNWaJKwDiB_p@MkEAo@I_CC_AQqG]eMQkGG{BIkCEmACqAEgAAm@C{@CyACqAAm@EgDAaAC}BAkBAuA?{@?_A?mB?sA@_EFaGD{B@aABcABgADuABcAB_AFeBBu@Dw@JoCHaBFiAReEtA_ZZgGj@aMBi@FqADk@F}ALyB~@eSz@yQJoBHeBZ}GNmCFqAJwBFmAD{@HuAHsA^gGvC}g@PkCL_CN}BJgBP{CP}CFiABi@DcAFqAFwADkABe@B{@Bs@B_ADuA@Q?]By@FwCZsQBkABcBJqFF}DFgDDyDDoD?y@DsD?o@F}FDmFBaE?cD?eB?}DC{DCuCEkDUaRIkGOiLAs@QcN?ACgCE}CKwICwBCmACkBCyBAUGgGCiAAmACuBEwICaDAeA?_AEgEGkKAwCAy@AqC?u@?uA?[@sC?sA@q@@_BByB?w@@I@q@@oABqABcA@q@Bw@By@Bw@B}@By@By@D}@Bs@JeCD_ADy@Dw@NkCD{@FaAXoEPwBRgC\\wDX_DHu@H{@Hu@V{BLeAFa@BWNqAXqBh@_ELw@TaBTwAPcAZqBd@kCX{AdCiNj@aD^sBz@uEl@gDbAwFt@iETwAh@oDT}AVkBVgBVsBVwBd@iEH{@PeBNuAPoBLyAJmALuAJ{ABa@\\yEHqAZiEHqArA}RjA}PJuAHkA`@}FPmCLgB\\gFdD}e@J}Ad@yGFy@NuBTeC\\{DPaBLoANwANqAHy@Jw@Hy@Ju@L}@BWPoAPuAPkA\\_CPiA\\uBPcARsAzAaJRqAPoAPqAPoAVkBTcBNiAFe@@GP_BRmBP_BHw@LiALwAJmAHw@L}AHkAH{@JaBJqADs@HiANaCFoALkCD_ADw@ZsHXoGH}ANsDPeDNoDT}EDgAD_ADcAH_BFwARqEFoAj@}LJoC\\sHLsCTeFLaCP_EF_B@IHkB@WLuCDs@LiCDkALmCLqC\\uHTaFb@cKN}CXsGHeBLyCRgEZsGTeFLqC\\wHF{A@QLmCHyBjAqWjAwWFuAFwABaAJwCDcBDeBDsB@{@BcA@kA@gA@mA@gA@w@@qB?sA?yDE_K?wACkECiFAkAAoCAgEA{AAoBCeF?kBE}GAqC?qAA}@CaGAiECwCKkWOs^AyEE}GEmKE}I?kC?mB?qC@iC@qA@mA@wA@gABoA@w@ByADqA@{@@YDmADyAJgDHqBLiDVwGDeAPwEXoHDaABo@LyCPcFR}EV_Hl@uOTqGNuDLiDPgELiDLkDJyBPaFNaEPmENgD@]N{EB{@DcBDqADeCFkDBcCB_D?mC@mB?oCAeCA_EAaEAcDCwICiIEwQAw@?gC?o@Ao@EeMKwa@?{AAcEAgD?O?kG?sKAoI?qA?_HAoSAsO?iA?eD?kE?iD?mBBoC@wABoCBsBFeDJaEPaHJyDXaKBaA@o@Bw@HkCDwBHmC@]RyHPeHJaEX{KF}CByA@sA@wA@eB?iB?mBAeEAaBA{BC_BCwACqAG}EI_FCuBAeACaCG_DEqDIgFGgEEgDCoCAe@AqA?y@CiB?a@?y@AqD?}C?sD?kC?uA?sD?}E?mNA_C?cA?o@?gDAeZ?gM?{J?kIAmO?}A?sCCir@CkQ?W?iE?sMCsK?mB?mE?m@?oM@m@?E?iC@_K?}@?oNAkAAcACeAEiACk@E}@GeAOmB?AOyAYkCWiBMw@UsAYqA_@_Bg@oBaAcDkBoFeF_OQg@Qi@gHqSoDuKCIiAeDe@_Bg@cBq@gCi@mBm@aC}AkG?Am@gCIe@Mi@Mk@iBwIOs@Km@SeAu@cEGa@Ga@SkASsAW{ACQIm@COYiBc@cDCSIm@]oCOsAMgACSIm@AQE[O{AYwCg@gF_@_FSgCe@gIU}EO_D}@uRgBu_@]sFg@iHk@cHKgAg@aFe@oE}A}Lk@uDi@eDW}AaAyFWuAc@_CWoAa@oBq@}CmGkZuDiQ_B{HqAaGm@uCcA_Fq@aDe@eCa@cCMy@q@wE]oCUoB[eDUkCEw@MkBOqCOgDGwBEoAEuBAsBCeD?yA@oBBsB@wADoBDsAHqCX}Gn@eNR}EFsADwADuADwABoAB{ABqD?kAAsB?wACqBA{@?WAWE_BCu@EuAMeDIuASoDUgDUgDa@_GUiDg@uHk@sIa@{Fk@qIc@yGYeEa@_GWcEk@sI]aFGy@GqAOmCSiEMoCMaEIsCGkCEeAEiBImCA[IkDIgCMkEMeFCcAm@eUCm@Ao@WkJIqCMgEIoBOmDc@mIG}@UiDWkDKmAQsBWmCk@wFOwAw@oG]oC]iCaAsGi@eDy@qEe@iC_AsE_@kByA}G}BsKcCiLYqAgByIi@_C_BqHwBaKaAoEWuAsBmJKk@oEyScA{Ee@yBCI_EeRu@kDKk@Oo@{BoKqBqJkAsFo@{C_D}NiBwI{CwNkAoFy@{DiAoF}@sEgAeGk@iDMy@k@yDSsAo@yE_AsH_AoHw@iGGm@OkAwA_LsBaP}CsVqAoK_@wCoAaKy@uGg@_Em@{EcByM{@aHiB_O{A}LwA}Km@_F{@_HqCaUiA}ICOGm@qEs^w@mGSmBo@uGc@aFUoCc@uG]}FKkBIoAKiBMiDIoBGqBCyAEoBGmCEkDCmCAoCAmC?wB?sA@kC@aGD{N@iEByKBkL?o@@[?[?Q?Q@mB?kB?_@@yF@{J@{C@gC?g@@}A?eC@w@ByJ@oG?eC@sB@_C@{BFoGHeFBwA@]b@sQNiGb@aQBeAH_EBu@DyADkBDsBFyBBs@J{EH}CDuBBsA@uAByABiD@uB@wA?wA?qBAoC?uAAy@CoCEaDIyEEqBAYCcACo@Aa@KqCIgCI{AAUGyAIyAOmCKqBKuAKuAWiDKuAOcBS}B[iDsBiUuAqO{@qJOyAKiA[mDYgDa@mEC[u@gIo@_HIy@QoBWaCUqBUmB[iCWmBWmBYoBe@aDa@iCe@iCYcBO{@}@uEe@eCa@iBa@kBa@iBYqAYiA[oAYmAq@iCYeAkE}OuCkKW}@oCyJ_B_GK]CKgBqGoAoEcFwQgCiJ_DaLmAmEmAoE{AsF{@{C_B}FEMaDkLkB{GqBkHoAwE_BqFEOq@sBi@gBaAuCcAwCqAoDYw@[u@Qe@AAo@cBO[sAgD_AyBy@kBQ_@e@cAiAcCeAyBiA{B_DcGgAoB]k@mCsEqBaDmAiBiAeBaD{EeA_B_@k@}BgDuBeD}@uA}DwGcBwC{BiEs@uA_CwECGq@wAaBqD_CsFsAeD{@}B{@yBa@iAwAcEm@iBi@cB_@iA_BeFcAsD{@{Co@eCo@eCs@yCi@cCk@gC_AsEy@eEk@yCa@oBG]Kk@g@iCsBoKgAwFm@aDa@oBe@eCo@gDeAuFs@uD_@oBo@cDEOu@{DuAoHmB}J{BgLe@eCy@cE}@wEkAgGyBkL{AyHa@wBw@}D}@wEeAsFc@wBi@mCs@cD{@yDkBwH_BgGoAmEIWQi@Mc@s@_CkB{FoAoDwDoKwCkIiDqJ_EeLqBwFIWeB{EyAgEeB_F{AeEyAcEcAsCyAeEoAmDgCiHyAcEUq@yAeE{BmGuBaG_@cASm@yAcEiDsJkE{LyCqIe@sA{@}BaByEgCiHcEmLsEmMu@wBqBwFKYmAkDYu@aAqCkAkDkAsDqAkEeAqDwAkFgAmEeAqEcAuEy@_Eo@aDe@iCy@uEmAkHOw@k@eDgAkGy@yEq@}DaAuFkByKgAoGw@kEqCeP_@{BUqAq@wD}[alBWsAsDeTiCgOkCgOiBuKoAgHiCiOkEyVYeBc@kCiAwGsA}Hg@oCcAmF[{Ak@oCm@sCyEqTiE{Rs@aDuHq]cCcLgCmLgLuh@uGqZkAqFiAcFa@sBMq@W{AQiAKq@McAOuAQaBIiAGu@IaBGmACcAEuA?_@Au@AsA?mB@oADwAD_BLiCNmCLuATsBHo@TcBF]^{BP_ALi@`@iBZoAlAmExAkF@GV{@V}@FWf@eBb@}ATy@j@_CHg@XwAXyARiAVoBJq@LkAH_AHq@HuADm@H{AHmBD}ABeC@oA?k@A}@?qAC}@As@Cw@MgCGkAIcAUiCOgBI}@c@yEGk@OaBWkCUkC}@qJI{@KeAAQMeAGu@c@kEKiASwBAQm@wGU_C[gDEc@CWGq@SiBGo@Gq@]uDMqAi@cG[gDE_@i@{FG{@]oDc@yEUaCe@}EWsC[iDUgCU}BEe@MqAOcBMwAQkBMmAOeBQcBMsAQwB]sDQeBUiCO{Aa@mEQ}BGeAMqBMqCKiCGqBGaCCcBAoBAcA?sA@iCDiE@c@@e@RiHFgAJyBR_DF{@LyARaCD[PeBHq@Hu@XcCHe@R_Bd@gDD_@j@aE@KRsALaAx@eGJy@fA}H@Mp@{E\\mCb@gDP_BPyAJu@N_BNaBZiD\\uDToCZeEZaFRgELsB?URoEFyBF_BNoGFqCFkGB{A?W@eC?kE?sA?o@?q@?q@?o@@kD?mH@eA?eM@yF@i]@uN?}C@kJ?eB@gY@uF?uF?iHAoP?_IAoS?mD@mJ?q@?yA?QA}A?w]Aw_@@iG?mCA}a@?kCA{I?{M?m@?U@eM?mA@mH@yD?aI@mE@kI?aABgP?o@?_B@eM@oI?wKAaECoDAiAOuOMsIEoDAw@KgHM{IQcMMcJ?MQ{JK{HQgMMiJKoGG{HCqFCaHAgDC__@?oGCyTA}NCcVAcO?sDAwGCoW?yECmT?wSAyP?mCC}a@?e@AiE?m@A{L?kM?u@?y@?o@Fe[@uC?cDDk^DmZBmL@eD?u\\?o@@qR?aR?{N@iS?mJ?yA?}@@uJ?sC?uH?eA?iI?gD?iE@qJ?gM?uI?kJ?cC@cC?{G?{G?yA?eC?g@?}A?m@?gC@iD?_B?uQ?o@?}D?gF@kJ?kD?W@uEAcA@eAAcD?yB?aG?oC?o@?_A@iR@iu@?qA@ql@?o@@yJ?cA?kD?uA?I?wC?e@?eB?eI?kA@_D?}C?oD?mC?qA?yA?aF?qC@eO?eI?a@?wF?}E?iH?_C?cI?eG?u@A{H?}A?iC?}F?qC?_A?_A?kD?yD?uD?gFAmD?wB?m@?{C?{@?A?}@?gCCmMAuK?{A?wCA}CAyLAqK?_A?_D?_H?_@?_@Ai@A{A?y@?y@AoL?sBAmC?qAAeH?_A?kBCkM?qB?mDAmKAgF?qBAkD?w@?aHAsB?u@?_HAcA?o@?oCA{D?I?gFAgE@]AuB?_H?}Y?aI@eD?_I?ci@?_H?kG@g[?o@?yS?aT@}HBgE@yA@uABwBDgEBsB?O@o@@s@?IDiBDoCBcA@o@FiC@a@JiEHiDLoDBy@XuHl@cPF}A@Y|@gVJoCNcGFuCBs@FaG@q@B{B@cH?kEC_ECmBAyBEwCCyC]e[Ao@A_BCkCO{LGuECaCE_FA{CAcAAaAAqI?iE?mA?yMBgW@iV?oCB}`@@o^@cI@gM?e@?oA@yZ@_S?eA@kMGwlA?}DC_p@AwV?o@Acd@C{f@?yC?{F?_p@?iM?aG?i]?s@@e]?s@?uH?kh@@{VAsC?sBAmDAkDCkDAsBAy@?]Wuc@c@sr@GyI_@il@a@mp@CcFCoC?sBAoC?kCAaA@}D?aE@{CPmf@BeGJc]JyY?m@@_BTcp@Je\\F{N@yE@kB@iD@{@?oC@oJ?qD?sB?oC?aE?kC@me@@oE?oQ@oG?_E@eM@oL?iA@kCAuBBiO?iF?wC@{CD_b@?uO@wG@aL?gS@{J?iKBiY?o@?mC?gX?iB?{R?sS?gD?{a@?wB?yH?_H?oC?cU?eD?_B?iD?u@?}@?q@?}A?_V@iO?o@?cC?{O?oD?iD?{A?}DBeZ?gJ?eE?a@@wJ?iG?gI@qD?aB?{L?oA?oB?sBAaCA{A?qACaA?i@SiOEmFIqHC}AEcBO_MIaH?CAi@ImHImFGcGOyKEoDGgEAwASqOAwAEkCAqCAiB?wA?yA?{VB_k@?oK?gK?qB@iN?qC?qO?_B?eD@kQ?iD?eE@c]@_BAwA?u@@iD?cL?}F?}@@}M@wK?wI?oC@aL?eA?wQB}k@?m@@u\\@ea@@{G?{C?uL?eC?mU?cF?mH?uG?kP?uG?wZ?yH?g^?yJ?eH?eC?qM@gB?{A?uI?kJAsG?{B@}H?_DAwHB_IAkF?yI?ga@?_L@qK@mB@aCBmDTac@DeGBmFBkC@{BRm]DkIBmE?AByC^}o@B{ER_]DiE?YBaG@yA?y@?mFA}A?A?{A?}ACeGCsLA{JK}j@C_J?{CCoQA{ACcQC}JE_W?iC?wAEqSAqBAmIAkF?o@CoLAgf@?}O?yEAaO?oJ?gIAuI?kH?wB?iE?mM?yB?{GAgG?eF?wP?gB?uA?uD?mC?mFAwXA}D?m@AsD?IAo@IeUCmIOag@K{]Mm]Q_i@?k@?EA_CC_KEoRCkHAaBCsEGyREyPAaDK{\\Ocd@EaLIeXC}GA}D?o@A}DA}A?o@C{G?A?o@Am@AmFAgBEoNC}H?iE?eB?aD?}I?_E@g@?sL?qB?kK?eB?uJ@iN?mI?}B@iGAuEBaZ?mK?i@?{F@mUAsE@wI@gX?wU@yH?}H@oc@?iR?eC@gE@yO@_^?wG@m@?mI?eFBiy@Bwy@@sJB{r@Bwy@@{J?o@?mQBaf@?mF?Y?cD?aG@}R@eI?m@?wB?uB?}GBub@@aL?i@Bw[?sA@a]@mD?mK@uG?uH?}E@mI@aO@}O?cG@_T@sG?{H@eU@sE?Y?o@?wA@sC?mL?yB?sB@}D?o@?m@?mB?oG@}D?gB?iB?sC@_I?uC?s@?}D?a@?uD@_E@mB?cA@yI?{E@mE?{E?uABmC@_D@{@DkCFmD@i@DgBHwG@w@B{@BaC@]@u@@i@@S?c@BmADcC@aA?UByABaBJ{GJkGDgB@o@DoCFwD@g@DsCDoC@iAJqFBmB@WPcLBeA?C@g@?a@FiDB_ADeD?k@@c@@_A@}B?u@@kD?sC?m@?w@?kF?gF?qB?yB?_HAkC@uE?]?gA?sD?i@?wD?oF?gD?kE?qA?mB?uDAkD?_R?}F?sK?o@?aC?eKAkGAg@?}BC}IAkCAaCAyGAsC@{@AaDA_BAqF?i@?uBAgDAg@?qDAuDAiDAyEAaD?UAqCAeA?gD?UA}D?o@Ag@AeF?uDAoE?C?eBAuE?QAm@?oC?CAi@?kC?C?m@AeB?wDAYAsE?}A?eAAwCAoCAgF?uECqI?e@AmF?o@Ao@?oAAeD?sE?KC_FCaJCwGCoE?o@EkI?CCaD?gAAiACoHCyFC{C?gAAg@AqCAkCAu@AeEC_FAsCEcHEqHC}FA{ECeEA{DCoCAm@A_F?oA?eD@wD@gBH_GLkG@u@BeAPiHFmCDoCHcEF_DJ_FFcCBkBHgD@w@JaE@c@VgM?Q?a@B}@HeDJgFL}FJqFJmFB}ABuDBkD@_B?iC@eFDoMBoM@kI@u@B_NJie@DiL@yFBkI?WDmT?}@N}m@@wJBwH@uD@gE@sA@yI?oC?[?CAuA?sAAw@?i@Aq@CqBAsAC}AK_FEsBIuBK_D?KCc@MmCKeCUmEOaCAISoDUcDc@}Gg@uIEu@?CGsAEu@C{@GqACy@IuBOgFIkEK{GCkDAkF?y@?oA?iF@gN?gG?sJ@kF?mL?wC?kB?kB@wH?mI?_H?{A@o@?{G@sM@qA@kCDsCDmCFiDB{@FqBBu@Bo@FaBFsBDeAHmBz@uOJkBDo@T{DJkBRoDLwBd@{I\\qGFy@^yGXiFDa@VgFJmBDa@R_E`@aHJ}ATsDb@aHToEJ_CF{AJkCDqAFwALkCD_AJkBFmAJuBLkBNwB@]B]b@}GDk@`@yGbAqPNuB@QHkAHoA^aGxAcVPwCXwFLoC@WBe@Bo@fBcg@J_DFcB\\}JBeA@QB{B@gAB{CAeCA_DGiCEuBMgDUsEOgCe@wFm@mFWiBQqAYoAOk@CKk@mBg@yAc@aAEIIMISCCIQ]q@_@m@]i@o@y@[c@m@o@?Aa@a@{@w@m@e@e@YiAu@sBkA_@UgBgAwBqA}EuCsHqEuJ}FmCaBcAm@yEwC_FwC{IkFk@]UOMIKGIEMGEEWOsEoCcAo@sBqAiAy@q@e@o@e@u@k@SOm@e@c@]e@_@a@_@][]Yo@k@YW[[u@s@_@]eBeBYWmCoCg@g@a@c@_@_@UU]]QQSQMMwEuEwBuBuAuAwAwAeAeAkCiCqBqBuBwBc@a@qAsAcQeQcAcAYYSSy@y@g@e@gEiE{I}IgWgW][kBkB}G_HGGAAAAGGCCKKUUGGEEMMgAeAg@i@eAgA}@aAu@w@o@s@cAkAg@m@kAyAi@o@m@y@g@s@uB{Cg@s@o@}@_@i@o@gAqAuBaAcBcAmB_@q@EIWg@_AgBAEy@_Bs@_Bg@iAAAuAeDwAaDi@qA{BiFSe@eC_GO]iBiEGOeB{DAESc@?ASe@q@{AEKkAoCmBqE_@{@[w@c@aAM[Yo@m@wA]s@g@aAm@mAo@iAc@u@e@w@]i@a@k@_@i@o@{@W_@i@q@e@k@eAkAm@s@}@aA}AaBuAyAk@m@qAwAkAoAeCmC_@c@u@u@_CiCw@y@wA{AuA{AwB_C}@aAcAgAq@q@{A_B[]QSyBaC[]]_@aEmE{AcBAA}BuCo@}@CEEEWa@u@gAi@}@_@q@}@_BIOKSWe@s@uAe@}@m@iAs@uAkDuGuEqIwCoF}CwFaD_GiAqBiHuMi@_Ai@_AuEoI_BcDi@mAWs@_@gAMc@EKQs@Su@Ou@G]COKe@?GMo@Ky@Kq@MgAAGCe@CSGu@IaBCw@As@C_E?cIAyC?{J?wB?_B?}DAyP?yF?oG?uI?eI?_@?G@eC?}@?w@?W?mC?gC?[?q@?W?oCCiIA{C?aE?kD?IAgI?iIA}B?qGAmL?c@?qD?c@?cA?{B?o@?aC?Q?yA?m@?}D?uC?kC?mF?o@A_B?mB?iHAeO?cJ?qC?m@?eAAwE?mF?mFAcP?oIA}F@a@@mFBgM?eF?{@@gG?I?o@?uBAwB?YEgFAyBEgDQaPIcKWiU?Qk@ek@?e@AS?[?E?MC}ACyDGaHEiD?a@?M?M@_@?]?Y@]@[@[By@@]BY@[Da@@WBY?CHw@Hu@D]F[D]DWF[D[Lo@H_@H]FUPq@H[FYTu@XcAv@uCt@gCt@gCPq@J_@r@uC\\kAV}@Vy@VaATy@DUJ]BMHe@TmAPgALcABOLaALaBHmADwADyA@eA?iA?CA}@AaACs@EeAKmBWiC[{BKo@MoAaD{MmAmFwAeGi@wBSu@S}@}@_EkA_Fa@}AgCuKeAmE{A_HAGOi@aBqHMk@m@eCi@_C[wAESUaAk@aCEQu@gDu@sDi@mCQiAAC}@gFQaACOYsBEUOeAMcAQaACSIi@K{@Mw@K{@Kw@CQQqAOsAIy@Iy@Iu@Kw@Gs@ACSqBSqBC[K}@E]AMCOAWIy@qAsMiA}K]aEACOoAI_AQmBk@sFaBgPa@gEi@qFO}AMgACa@g@qFM_AoAiN?Ck@gFGm@OoA]oDiAwLIw@]oDq@uGcBkPgB{QiA_LASKaAKcASaBAKKy@SwAEWIm@Im@[yAa@yB[yAWmAq@cCq@eCiAaDc@oAw@{Bm@cBoBsF_@aAsBaGoAuD_AeCm@cBsAyD[}@_AiCm@cBqByF}AkEu@uB]eAg@sAmAiDaAqCgAwCQi@Sg@iBoFg@uAg@wAc@qAc@mA]_AeBwEe@mAqBuFkA}C{@}Bu@uBQg@IWm@cBiAaD{@cCcByEGQeBaFeAwCqB}FK[EOgBeFe@uAqGaR{AkE{@eCu@oB]_AOe@_AoCQi@m@cBIUKYEMq@qBGQCIUq@oBgFe@sAy@_CiBkFw@wBaC{Gs@oBo@_B}@uB}@gBGOc@y@i@cAu@sAU[cA}AEGe@q@e@q@IMq@y@iAuAo@y@uAcBoA{AuNcQKK_BmBg@m@SWa@e@gB}BsBgCo@s@MOgJ_Li@o@g@m@QUoFuG]a@EE}FgHqDkEaCwCKMk@s@k@q@}AkBwNiQgEgFkHyIeC{C_E}EuHiJoCcDg@m@{CuDsBmCW_@U[o@_Ak@y@_AuAsCsEi@cAWa@e@y@sJkQyAqCsBsDUc@qAcCQYgFkJmAyBu@wAmA_Ce@{@c@w@}A{C_@s@e@u@qAkCuAiCaB}CaB}C_B}CQ[gC}EqByDkC}E{BiEoBkDu@oAaCyDU]u@gAaEyFo@{@q@aAa@k@mBoCUc@}AyBa@k@eBeCqAkBkDaFiD_FoBsCs@aAU]kCyDOSiD_FsAoBwCgEmAeBYa@qAmB_DqEqCaEi@w@_@k@_@k@_@o@U_@{@aB_@s@Sc@S_@_@y@_@y@Yw@A?]{@Wq@Um@Qi@Si@?AOg@Qi@Y_A_@uA_@yAa@_BOq@?A{@sDeAuEg@wB_@_BKe@Os@[sAMm@Oi@ScAc@kBMk@[oAk@gCgA{Eu@_Dc@qBs@{Cc@mB_CiK_BcH}A{GgA{EaAiEUaAsBcJiA_FYmAMk@Oq@w@gD{@wDKa@Mk@u@cDq@wCmAkFyAsGw@eD_@aBMk@Mi@kBoIEQe@sBm@mCo@mCo@sCSw@_@cBYaAgAgF}C}M]}A_AcEUaAw@_D{@{Dy@mDWcA]sA_@oASs@Sm@y@cCUk@a@cA{@uBAAi@mAq@sAMYi@aAaBuCA?i@}@s@gAoAgBeAqAk@q@i@o@gAgAyAwAqAkA[WQOa@[]YWSc@[GE]Ue@[s@c@k@]YQWMOIQKYOm@[cCoAECYOa@S_@QaCoAa@ScFkC}DqBcDaBIEuBeA{@c@iBaAQKm@]{BmAuBqAgBgAqA{@{AgAa@Yg@_@A?aBoAUQwC_CUSOMA?o@m@{@w@u@q@}@{@IGu@q@qAmAIGKKCAAA?Aa@_@w@u@kCaCe@e@eA_AmDcDmCgCyIeIyAoAc@[cAo@SMkAk@_Ac@y@[{@WUIOC_AU[GSCm@Km@Ik@Ek@EQAY?c@AcAAU@m@@gAFkAJSBWDQBWD[Fa@JSDm@NaDt@aB^WFoDz@uCn@o@NsG|Ai@LaATsAZsAZcB`@eCj@}D~@[HE@gHbBcFhAa@JeAVMBUF_@H[HgAV]HKBq@NSDQBQDc@HUBg@HSBQBSBc@F_AH]DS@Q@g@De@BS@M?S@O?S@a@@Q?Q?Q@s@?]?_@AY?YAU?aAEQAS?g@EWAQASCUCQAe@GQAg@G_@G]E]GSCi@Kk@KWGOCUGOCi@Oe@Kc@M_@MWIe@OUIMESGSIOGQGQGUKUIQISKOG_@QiB_Aw@c@e@WMIYQ[S[Sa@YYSc@[a@]a@YWSu@k@UQw@o@aCiB_BoAkBwAaCkB_CkBk@c@wDuCiA}@mDmCuC}ByBcBw@o@eAw@qCyBaAu@eAy@yAkAoCuBSOyAiAyC_Cc@[kA}@WSoAcAw@m@YUCAe@_@a@[kA}@a@]_@WEEy@m@y@q@{@q@MKQMg@_@eA{@gA{@w@m@YWg@e@}@u@i@e@WUa@a@q@o@q@q@a@a@o@s@e@g@UW_@g@uAcBq@y@i@o@q@_AgAyAm@{@q@eACEWc@iAiBs@iA]i@W_@Uc@Wc@O[Ue@ACS_@Uc@[m@g@_AYk@Qa@KSYm@Yo@e@gACGy@sBeBiE{BuFuAiDyDwJk@yAYs@[u@o@_Ba@cAACmA{CcBgEsAeDKYeBeEw@iBgBuEKYi@qAM]EKeBiESi@GMwCmH_AaCuBoFGO_BcEM[O_@iBuEyBsFg@qAgEsKg@oAo@cBi@uAM[g@sAGM_AaC]y@[w@w@mBIUQa@c@gAk@wAQc@sBiFOa@_A}Bw@oBWo@e@mAGMoBaFqDeJQa@k@yAsAgDy@wBc@gAWm@Ug@[s@c@}@]q@[m@q@oA[g@Wc@iAgBq@eA_@g@KM]e@w@eASWsBsCaJaMaCcDMQKOaCcDGIQUiCmDiDyE}AsBoCyDs@_AY_@oBmCsC{DY_@SYmBiCY_@Y_@gBcCYa@w@eAi@w@e@w@Wc@S_@[o@Yk@Oc@_@_AQc@?A[_ASs@Uw@e@gBe@gBCII]Qm@Og@_@wA]sAOi@Sw@EOUy@]uAo@_Co@cCqB}HcAqDEOu@mCIY?C{AaGCKiBoH?AoByHi@sBm@_Cc@cBqBeH_@uA_FqR}@iDi@yBSq@}@kDYiAc@aBoAwEKe@ACkAkEeA{D{@eDeAaEg@kBMi@oAwEOi@Ok@o@_CMi@o@aCEOw@{C{CmLiB}Gs@mCYgAs@mCOi@a@{AMc@a@qAk@eB?AQe@Oc@c@kAa@aAKWEKUi@O]mAgCk@gA[m@o@gAe@y@_@k@o@eAEEe@q@aAqAcAoAQSa@e@e@i@[[c@e@c@a@OOCEYUWWw@q@u@o@yAmAiA}@qDwCgEiDmDsCsBgBiCuBcByAg@c@wAiAqBgBaCuB_BsAwAoAqAgAUUSSWS{@q@_Aw@q@i@kAaAs@k@iA_AaAy@q@q@gAiAoAoA{@}@MOAAQQW[OQGK]e@a@o@k@y@u@iA[e@uA{BiAiBsBuD{BaEoA}BaB}CYg@}AsCm@gAUe@QYS[c@s@Yg@a@u@"
                            },
                            "start_location": {
                                "lat": 41.11333570000001,
                                "lng": -104.8571346
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "18.4 mi",
                                "value": 29675
                            },
                            "duration": {
                                "text": "17 mins",
                                "value": 1021
                            },
                            "end_location": {
                                "lat": 41.2322891,
                                "lng": -95.84687369999999
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Entering Iowa</div>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "uqezFllyiQcK}QmCcFyDaHqA_C[k@CGAAO[CEsAaC[m@_BsC_@s@w@uA{CqFuByD_@k@mAeBmBiCaByB[e@o@w@uBgCmEkFY]a@g@s@{@gC}CAAkAuAsDmE}CyDwBgCeFcGY]a@e@i@o@EGcCsCEG_EyEkB}BwAeBo@u@oA{As@{@u@}@qBcCY]IKcAqAUWCE_@i@SWMQkAcBe@s@OUm@aAmB{CIKsAwBaDiF{BqDeAiBiAgBGIMUm@cAU_@}CiF{AaCWc@MS{@uAkCgEqBaD_@k@_A_BoBsDcA}AS[?AA?gAeBw@oAwCuES]?A_@m@_@m@QYGIc@u@AC?AoAqBiBwCS[IMKQk@}@Yc@Ua@c@q@EICEACOQOUMQMQ_@e@QSKM?AYYCEQQCCMMOOQOSSQOUS_@YQMKI]Se@[i@Y_@SAAMEcAe@kAc@GCOEQGm@SUG[IWGSEk@KWEOCUEOAa@Eg@GOCa@CQCQAKAmAMsBMk@EMACAc@EkAMKAc@EgD[sBWgEe@qDa@OAEAyBYk@GkAMy@KYCo@IEAoAM[CMAKACAA?uDa@g@Gc@G[Gi@Kc@Ku@Su@Uu@Uo@U_Bq@}Ao@cC_AiEeBaAe@_@QCCEAe@WA?cBs@OEKEUGSGWEUG_@GMCYCi@E[As@Cu@A}F^{@Fi@BQ@I?kBHm@BaBDgBH[Hg@@Q?eBJaA@k@?c@C[Ae@EUCMAq@Ma@KYIWISIc@Se@Ue@Uo@_@c@[][IGGGKOg@i@_@e@m@w@a@o@M[a@w@Uk@Ws@_@kAOk@I]ESEWIe@Im@I}@I_AAIAQCUAS?EAQCqA?CAo@?u@@]@a@Bo@HuAJkAHu@ZqDFu@HcAFw@Fy@\\mEB]`@iFr@eIZ{DFm@P}Bp@}Hh@oHRsD@SHiDB_ABwA@g@?M?k@?sJ?I?eKAuK?eB?k@?U@_IAkI?eG?aD?mI?yI?oE?g@Ai@?a@AYAUA[AQAQAc@CYC[C]CSCWGc@G]E[Kq@I]i@_DKm@qBqLM}@UuA?EGa@Gm@GiAGeAAy@C_BAw@?q@?A@[?iC@kEBmD?sA?u@?c@?Q?o@?W?K?E?I?{IDaH?w@?cE?W?w@A{F@kD@mI?aE@iE@wJ@g@?gA?gA?]?oE@wB?s@?c@BoF?aD?I?{B?E@sBAi@?QAyD?u@?]@mBB}S@yD?Y@O?A?e@?[?qA?G@uD?_E?[?sB@}A?i@?qC@oD?uB@kCAwBBiE?U?U?O?[?i@@w@?K@k@?o@?}ADmCBiAFeBFkBJoBLoBVkDZuFJcBRmCNsBJgBJ{A@GFaAJyBBs@Bs@@G@U@i@@k@BwB@qB?cA@s@AeB?[?A?aC?wG@iM?Y?aCA}@?{@?c@?OC}@Aw@C]Cu@KmAKcAKw@Ky@I]_@gBOu@Os@WsAe@aCm@uCMo@Kc@AG_@oBQcACOIk@My@g@eEAIACEg@?A?CU}BYcDeAmLe@}EaBoQAKMqAGm@]wDEc@AG?AWkCO{Ae@gFYkBGm@WqBOcBQ{BAOKiAQqBACEi@CQAUIw@OyAMkAQwCAuA?uA?M@E?M?GBs@Du@Fo@NsAPiAF[BOFQRkAV_ALk@FW@A@I|AsGDW`@sBA]HuA?CBe@?k@B_A?kBEiD?k@A[AqAAiBAq@?c@?C?YAg@AwAAeBASA}B?[CmA?q@?k@CwBI{BC{@?ACc@Go@Ec@AQCMIm@G]Ga@Mq@Oo@Oo@Oi@o@}BIWg@gBg@mBQm@Og@?ASq@Sw@g@gBAEOi@[cAQi@GYu@_Cw@kCk@sBMe@GQU}@Os@O{@ESAIGa@UqBGy@KyA?ACk@UkGCaAAc@Cg@ASEmAGwAIyAKmAY}DKcBKqAAQ[wEG_BCo@IaC?CIeBOqDAQGmAAYCi@IsBACKaCE}@E}@A]Cu@Ao@IqCi@cRIqB?MEwACiAQkGK_FAUAYOyEEqBKqCC}@AYAa@EsCSyIAg@QaIGg@C_@Q}EAY?I?AIiESyH?UCkAEsAEgFAm@C{EAo@EgG?}@?_C?W@eFAoA@kADqGDuCHmH@yAJ}G@gBD{CBqR@}HBkFAgK?aI@uCAy@@yDByI?w`@?sC@sCAoB@eE?w@B_I?U?]@mC?Q?]?O?_@DoI?eAEaLAyFAgD?uA@uCAgBAgBA}A?_BAkA?kAEiCAcB?_C@kB"
                            },
                            "start_location": {
                                "lat": 41.1575451,
                                "lng": -96.1455139
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "23.6 mi",
                                "value": 37984
                            },
                            "duration": {
                                "text": "21 mins",
                                "value": 1243
                            },
                            "end_location": {
                                "lat": 41.49241019999999,
                                "lng": -95.5854925
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to stay on <b>I-80 E</b>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "ydtzF|a_hQ@mBDcB?ABgAHcD?A@SHyD@_@DkBB{AFeCN}FN}FBqB@Q@y@Bc@R}IByADcCBsAKaFSoCg@uE]_B[iA]gACCU{@Wy@c@cBgBsCyBaDs@{@eAw@}A_AiBq@iC}@k@Qi@OSGSGmCeAcCaAi@WoDaB{@YaDaAcA]c@OUIEA_@Sm@]QKk@a@c@]iAcAm@m@o@{@m@_AS]i@eA]}@Wo@Oe@K_@m@qB}@iDg@kBGQOk@Ok@W_Aa@wAc@uAYy@Wi@Yo@Sa@Wc@QYY_@W_@a@e@U[WYoA{AqA}AkEgFeAoAEEAAs@s@}@{@]]}@u@uDsC}EoDuB}AsCuBw@m@w@k@uAcAiDkC_@W]W_Au@{FiEmEeDMKQMqFcEmCsBiCmB_As@aAs@yBaB_@W{@q@_@WUQGG}EsD{AqAmAkA][IIu@y@s@w@iB{B}@mA}DcGkBwCcA}AcBiCeAcBYa@eA_Bu@kAQW_@m@Ya@aAyAa@o@Wa@IMOUa@m@OSYa@Y_@EGq@{@W[MOc@g@o@s@s@w@o@o@e@c@wAqAq@i@YUECkA}@uA_Aw@g@_@WUOu@_@sC}AwAu@{DyBe@WWMi@Y_Ag@QKqBeAKGqCyAg@WGCYOGCGEi@[wCaBYOgRiKaAg@cDeBcE{BkFuC{Ay@eGgDgFsCgDiB{N}HiGiDKGyC_BiAm@WOaEuBIEmIuE_B_Ay@i@yAcACAOMKGSOMKOMqFmEuLuJsNkL}E}D}MyKyBgBgEkDkEmDsAkAcB_BMKyA}AcAeAwLiMA?AA?AA?GGCEeFoFmAqAwFaGa@c@aNsNkCsCqBuBmCsCmCsCeMyMcBgBwB_CQSKMs@{@m@q@c@i@UYoB_CACkB}B}BqCsEwFe@i@s@}@aToW{@eACCAAAAe@m@WYgNyPiByB]c@MOgA{A{@oAGKw@uAGMg@aAIQ[q@Yo@Wm@Um@KWWs@Uq@K[[eAK_@YmASu@GYG]GYUgAEUAGMu@Ky@Mw@Iy@OsA?EIs@MmAc@eFe@eFg@aGoAaNIu@O}A_@gEIw@c@gFe@gFe@mFWmCIw@Q}AOiAKm@CMMu@UsAOs@CIMi@GWI_@Qm@Ka@Qk@Uu@Qi@Oc@Ws@_@aAYs@Wi@MYIS[m@]q@e@w@]o@_@k@[e@c@m@]e@]c@Y][]m@s@eAeAeAgAcAeAy@y@o@q@cAcAu@y@}@}@m@m@kAmAgCkCo@o@gCkCcCeCk@m@[[w@y@cAeA{@{@oAsA{D_EsCuC_DcD}@_Ai@g@e@g@uAyAyB{B}A_BoBqBgAiA_A_AcAeA}@_Ae@g@g@g@eCiCiCkCs@u@cAcAe@g@[[kAmAg@i@o@q@a@a@a@a@gAgAuC{CwCyC{@}@c@e@}@_AaAaA{A_Bk@k@q@o@EEeCmCuAwAq@q@e@g@c@a@c@e@_@a@o@o@y@{@k@k@ECmAmAk@m@y@{@]_@]]gAgAqAsAsAwAuAuAy@{@s@u@q@s@e@g@aBaBQSQQa@c@g@g@i@k@k@m@YYYYg@i@g@g@g@g@e@a@y@}@[[{A{Ao@o@SOQOSQUQQMSOYUUOe@]u@e@{@e@a@Sc@Se@S_@OaA]q@Ue@Ou@Sm@Mk@MiAQs@Kc@G]CuBQmAIeAIIAsAIiAIgDUm@Ei@Ea@Cc@Ey@Ia@EsAKc@Ca@CCAs@E[AKA[AWAWAw@Ge@Eg@EUCYEUEYEUEYGOCQEc@MMEMCMEQG[M_@MaAa@u@a@_@Se@Y]U]WcAu@YYm@i@}@}@c@e@e@c@kAkAgEiEYYm@o@cAeAcCcCu@u@cAeAc@a@i@k@k@k@u@u@]]a@a@a@a@k@k@k@k@eAcAY[][s@s@Y[WWq@s@s@q@cAeAu@s@cAcAa@c@a@a@[YYYs@u@]]GIKIY[[Yq@q@o@o@_@_@k@i@SUs@q@MOQQu@u@o@o@g@g@a@a@o@q@}@{@{@}@][[]]]aAaAuAuAk@m@g@g@s@s@q@q@a@_@c@e@a@a@aAaAe@e@sBuByBwBa@c@mAmAmAmA_B_Bg@g@s@s@o@q@eAgAaAeAa@c@a@e@s@w@qB}BoB{BoByBY]}@cAaAgAcAkAc@e@a@e@OQ]a@gCsCMO}BiCW[_BiBaBiB{AeBY]q@u@o@u@uB_CuCeDsB_CUWqAyAu@{@k@o@u@{@g@k@{@_AgIkJy@}@aAiAkAqAyBeCyBgC_AcAkAsAqDeEcAkAeAiAcAkAi@o@[_@Y_@c@i@[e@[e@a@o@Wc@]i@Ue@Uc@Yi@Yq@Wi@Uk@[w@Qc@q@kBy@}Bw@yBq@kBs@mBKYsB{Fe@oAOg@GOUk@Y{@{@_CISOc@Qe@iA_Dc@kA[{@Yy@_@cAUo@{AiEu@qBi@yA{@cC}@cCq@kBq@kBUo@M_@Si@Wo@Wm@Ui@[m@w@wAy@kAo@aAEGi@q@_@c@c@e@a@a@IIWUYUIISOOMe@][SWQYQg@Wg@Wc@Sk@We@QQGOG_@O_@Ma@QYKgAc@EA{@[ECw@Ye@Si@Sg@Qe@QSIUI[M]MaA_@y@[oAe@oAg@}@[}@]]McA_@aA_@]Oc@Oy@]a@MUKYKYKYM_@M_@O}@]iAa@GCqBu@y@]}@[e@SaA]cBo@qCeAo@Wq@WoAe@q@WmAc@oAc@s@Wy@[yAk@g@Qg@Sc@Qi@Ui@UqCeAw@YGAs@Ym@WSIYKCCE?sCgAa@M_@OuDwAwAi@{@]e@Qi@S[M_@MyBy@qBw@aBm@a@QGCECOE_A_@eBq@e@OsAi@i@SMEi@S_A_@kAe@yBy@y@Y{@[mCcAeBo@i@SQIKEaBm@MEKE[Mi@SOGUI}@]KEuCgAu@Y_A]_@M_@Me@MWIc@Mi@MSG_ASg@Ki@KUEMCGAE?mC_@qASUCSCC?MCIAKAKAOCe@Gk@GSEUCk@I]Ew@KA?yC_@]GaAMaAK}@Mi@Gi@Ic@G{C_@g@GSEUCUCSCi@IUCSCSEWCoEk@eGw@gBS{AUMAi@KSCMCm@MSEUGQEWG]K]Ki@Qk@SUGq@Uu@U"
                            },
                            "start_location": {
                                "lat": 41.2322891,
                                "lng": -95.84687369999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "95.2 mi",
                                "value": 153282
                            },
                            "duration": {
                                "text": "1 hour 22 mins",
                                "value": 4925
                            },
                            "end_location": {
                                "lat": 41.5920885,
                                "lng": -93.7859502
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b>, follow signs for <b>Des Moines</b>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "q~f|Fh`lfQqBo@uAg@k@Qg@QSGQIUISIQIQKSKSMQMSOOKQOSQQQQQMOSSEGGIOQMSOUMSMUMSMWKU[q@KUs@}AMWMYo@uAc@aAMYYo@Yo@KSWk@Sg@O]IU_AuCc@{AUgAUaBOmAG}@K}@GmB@]?{@?oC?I?_C?sA@{B?oA@]@uA@qA?CDuBBsBB}CFeDBqCDqCBeC@]b@_]?K?O@u@@w@@E@y@BkB?YDgD\\{VDiDFqEFyEBgCFwD?AFqF@k@?g@@[?e@@{@?w@?Q?G?g@AgAAq@CoAAe@Ak@EcA?SCi@GcACm@GqAO_DMaCK}BOqCGgAQoDc@eJQmDk@oLc@_J_@oHQyDIaBQcDAYm@{Lg@gKEgAKcCKgDCiAE}BAkAC{BAuA?CA_B?kA@kC?}@?c@BoCBuBB}@FmDLeGJkFZkOJ_F@MFoDFoCR_K^sRN{GLqF@u@JuEJ}EHmELkGLcGDyB?ADaEFiFByE@cE?o@@aCCcH?q@C{DCkEAmBAaFCsBAgBAwC?UCiGAYA}E?OCgGAc@?wB?cC@_IBaJDcIByF@oC@aDF_N?k@BcHBiF@uC@i@BcHBcHDiJ@oDBoG@kB@cC?KBcFFwL?}A@}ABoF?_B@aB@u@@gC@kB@sAFaJD}F@}BDgC@{BByBB}E@o@@yABsBLoNBcEB{BJuMF{HD_GFwIH}IFcGFeHJgNF_HDoGDsDBsC@oC@k@B_EDgEFgIBmB@yBBuC@gG@gC?uC?qD?iF@aJ?uK?oJ@iE?gH?cG@qC?uC?a@?kO?}@?mB?aI?o@?gA@gD?_H@_N?mB?aI?eE?uH?wJ@oE?gD?cF?oR?}@?sG@oLAuA?qH?qJ?s@?gF?Q@gG?eP?{A?wD?{A?eO?mB?uB?qD?aD?aD@sO?kC?iF@}CAmA@yi@@mE?{E?{C?sA?_AC_CAoFGkGGiIEmGCeDG}ICyBA_DEeFE_HA_@EaFCeF?ECkBEuHMuNEgH?CIaLEwFAiCEgGCcDE}EQqSAcEAcBA{BAUCeEEqDAuBEuFKiNAcBEcGCmDAyACwEEwEC}F?mFDiFFyDB_BD_BB_BFoCLmF@w@JsEHeET{JLaGByAFsCP}HHeEZ}NFoCJ_EBwADyALwFFkDBiAFeG@e@@iC?cB?K@kF@eP@sFAmH@}D?iG?eA@qJBgW@wT@iH?qB@mD?_E@oF@oR@kJ@_M?sA?eH@gC@yA?yG@qJ?iD?_@?c@?M@qC@}N?qB?oB?o@?eF?aB@gD?sC@_G?}B@oE?O?iE@kH@cG?iF?iG?Y?mDAg@?QEoGCeDAYEqFEeFMaLCaDCkDCuBCgBEoFA}@E}EAu@?EIiH?_@IaHEmEAqAQiQMiNGqG?WEwECaE?SCuCAuBAaEAuDAg@?iACkHEaNAcCCoF?_ACqC?]?oBAs@CmGC}ICgFAgC?o@AmACiE?w@AwB?WA_E?QEqJAsBCcJKc[AaBGsLAcD?kA?}CC{DAcE?AE_GAcGA_A?gBG{L?GAkBAuGAqB@{@@cA?s@DwBBuAHuBDy@FsAZaHDs@^wH@ONuC\\cHXcG?EL_CHaBDw@FiAJaCF{@LkCHaB@YNcDHyABs@B]Dk@Bm@D_ADqA@Y@u@DuA@wA?mA@u@?_AA}@CiBAw@CoAIqCCYIyBOmDIsBG_AIgBGwAEsAUeFCo@_@_JASA[I_BCo@IqB[yH?ASiECa@SaFIqBGwACsACsBAqA?}A?{@DwCDgCF_BDuAJmCD{AFsAB_ADgAHsBB{@h@yORkGNmEPgFJuCDkAR_GTaHF{BH_EDkED_LByG@{E@eA@yHB_EDiJ?I@oC?o@?a@DuO@yE@_A@mD?oBDgG@y@?cA?a@?q@?w@?yA?kA?qE?{BAqA?qCCmEAkEAcCC{LCsMAoFAo@AaD?eAAkFG{YKe`@?kAAcDA_EA_E?o@?s@IeZGoOAeF?qBAqBA_E?gDAW?o@Iab@GkT?iBAmE?qA?EAsC?uA?[?wA?}B?eA?{A?w@@yW?gF@uE?}G?cA?oD@yD@gP@q_@@mE@}A@oE@eF?mE@_K@sI?{G?_E?M@eC?Y?aA?aG@kQ?cD?OAoG?uD?y@?Q?uE?gB?{D?sC?iG?eP@qK?_C?oO?mA@qTAaE@{A?sI?G?yH@wC?mB?aC?cC?eW?_E?yE@eF?cCA{A?_B@qE?cB?aF?sD?{@?oB?qD?}G@qC?yD?cE@wh@?{D?{A?_E?cA?{B?kAAsBAwE?WCoO?ACmIAoDEqRG__@AuFA_ECmMAqBAaJE_TC_OA_EC_NGo[CeGAqEAwDCoE@}C?_E@iCByCBaFHeN?_@BuDFuKBiFBoE@oCBoC?GDqIFuMBaEHmMBaG@Y@uE?K?u@?gE?U?_@A{F?oO?qg@?oF?}G?}J@qF?oB?sI?kD?_E?mB?qq@?oB?oD?_E?kABeD@{C?c@FoIJ{LDqFHmL@gB@gCJ_NNmQJmPZc`@D_HXo^BuEBaC?M?o@H_J@mD@qCAoCCuDAy@Ay@EqBAcAAo@Aa@EmBAAC}AEqDAMAo@AsAEqBGgC_@oUEgCWeNUcMG}DAa@EwEAuA?sA?w@?aBDwIDyF?O@Q@yC?SBuB?O?y@D_E?EBaE?g@J_QFiKDmEB}C@gD@a@@qB@mB?SD{FDcIH}L@sB@eC?_CG_QAkG?KA_EAeB?yAAkAC_JAeCAqFAkHAiAAkCA_DAwE?]AsC?]?c@?UAeAAuFAy@?{@?[AuAAuA?_B?oAAcDAgA?y@AcGCiD?{AAcGC{HAsCAyB?m@?k@Aq@?q@?cA?]?w@?]?_@?qG?wA?uA?{F?_G?kA?cD?kD?g@?w@?S@}B?c@AoC?sA@c@?s@?qG?iF?aD?}G?eF?q@?iF?u@?_D@oA?wD?w@?g@?uB?a@?kB@}@@]@{@Bc@Bm@Bc@Dw@D_@B]De@Hs@Ho@Ju@Hi@Nw@Jk@TcAJe@Po@FS^sAHW\\mAHWfCcJxAgFj@qBRm@HYRs@Pq@\\wAH[Jk@Je@N_A@IHe@Jq@B[NuAJkAHqAFwABu@@i@@y@?W?gD?cB?oA?{@?_B?_F?qF?yN?aF?eE?cBAyD?C?{A?k@?{B?w@?M?[?k@?[?]?w@?]?sB?eF?]?kC?mD?}@?_E?CA{A@oC?{@?uA?}A?Q?YAcEAoA@oA?kB?oC?kA?iA?]?uA?G?}@?_D?}A?uH?mD?eE?q@?o@?w@?aU?oB?y@?cC?{CAkF@cB?kL?Y?_@?[?uA?kT?aF?oD?yB?aD?]?uC?gD?u@?iA?_@?eC?}E?sA?sG?oC?uD?eB?oF?K?kD?E?aB?iD?kE?[?}@?uA?{@?kB?eA?yE?cH?{E?iF?y@?y@?iB?cA?[?uB?[?{@@g@?k@AgE?eEAyB?m@Au@EqA?GCi@Ey@IwAEq@ACCa@CUO{AI{@WeCMsA[{Cq@uGe@sEEc@YsCO_BCOIy@SsBCSCWKcAK}@Iu@MuAMqAYqCc@gESoBK}@Gu@SqBOuA]kDE[C]YoCGi@Gg@[gD?ACWE_@E]CWE_@E_@I}@IcAEe@MuBCy@Cq@E}A?e@AmC?s@A}@?qB?a@?oBAsB?sC?uBAeE?qD?mEAiA?_D?_E?o@A_B?_BAqF?aKA{G?}@?kD?sB?yA@uC?[FcMDmJ?CL_XFyL@mDTod@?YBeG@{ANcZ?_BBoC@_EDmHNq\\D_HBoHBkD?qB@aH?oG?uC@uC?eR?eA@}I?mI?_B?]@sC?{A?}B?qB?mO@gA?iA?oC?iD?cB?k@@wF?cI?wJ@gI?uB?gF?G@}E?Q?oF@k@?s@?_B@yI@cJ@gE@iE@mO@gF?{@@_E?w@@wDBaR?Q?mD@aHD}V?yEBqL?oDBiK?sF?kD?q@?qQ?uC@_LAwC?oF?q@@mEAoA@aB?qC?_A?mD?kE?sK?eB?eG?{H?eC?_G?oA@{B?aG?yD?uJ?G?qC?eB?_E?eD?kJ?iA@eG?uE?Y?iI?mOAkH?gH?sAAqD?M?o@?_B?{HAkG?iC?_E?WAsD?gE?cDAmP?gGA_E?S?aEAaCAkT?]?eI?qCA}C?wE?{D?_BAyB?_C?{B?mC?kA?kA?qCAy@?gF?e@?I?gC?E?o@AyB?uB?sC?gH?qCAsC?]?o@?g@?uBAaC?o@?sC?{A?gE?g@AoB?qC?qD?k@?iBAmD?_D?eC?_E?i@AqE?c@?mB?wB?y@?o@?I?{@?y@B{@@{@D{@Ds@D{@Hy@Da@Fq@R{AHq@He@Nu@P{@XoAb@aBRw@ZqAb@iBZmAPs@H_@ZoARs@Pu@Ru@XkARy@Ps@^iBN_ALu@PsAHy@Fu@Fy@F}@Dw@Bw@B}@BcB?m@?{@?{@?aA?[?uA?_@?uA?yA?uA?uA?uC?yA?sC?oA?c@?uB?g@?mB?a@@iF?E?o@?c@?K?iB?sC?y@?wB?uB?wA?{@?W?c@?K?eC?mF?kG@kF?sD?aB?oC?oB?C?sA?uB?wB?qD?qC?qC@qD?wA?wA?gB?iA?uB?o@?oC?O?iF?uA?yB?eA?kB?uB?uB?qC?yA?oB?]?uD?yP@iE?_D?eQ?eF?[?w@@{A?o@?o@?m@?o@?mB?oD?oD?}B?eF?eI?{L?_JA_J?I?mB?aC?_FA_J?C?kF?qCA{L?aJAoE?iG?WAaL?}@?o@?eA?yB?iC?kGAiF?kG?s@?{B?qDAqC?uB?oD?oE?sC?yAAsB?uB?cA?q@?oD?sCAkG?eH?wB?mD?aAAeE?oE?wBAoI?cE?oC?oD?aA?qBAoD?qD?qC?qC?yA?k@?kA?uA?yB?s@?{BAcAAmBCoCCwAAyAAy@CuBGeFEyCAi@EkD[}WC_EA_AKyICsBAoACsBCoBAsAC_ACuBCoCEsCK_JOwNQgPC{BC{AA]GuBA[IwAGw@MsAK{@SuAMw@Os@EYSy@GYQs@Su@_@mAm@cBe@gAYo@k@iAe@{@k@}@a@m@a@i@_AsAwC_ECC?AoEeGqAiBiA}AIKaAsAu@eAEGoBkC{B_D{B}Cq@_AmAcBaAsAYa@QUc@k@Y_@c@m@iA}AcB}BKOKMYa@iA}Ay@gAgA{AsAiBgBcCS[EEqBqCY_@mBiCqLgPSYQYKKw@iAmCqDsEoGgBaCyF}HqFuH_@k@IKGIy@uAc@}@c@}@Uk@GMOa@KYIUEK]cAIYUw@Oq@I[I[G]UmAUwAKw@QyAOkBIuACo@EkAA{@?kB@_E@_E?M?a@?o@AaZ?mN?qA?_B?mB?qA?o@?o@B_N?aJ?]@o@?o@?_B?o@?o@@_K?A?m@@qF?o@?M?a@?o@?_C?_A?c@?KB_Z?o@?o@@aE?_B?_E?o@BoR?o@?oC?o@@oI@qI@oU@_E?iE@aHB}S?_E@aE?{C?c@@_K@_K?wA?kA?uB@mC?wE@gD?oF@wD@_H?eA?gABoZ@}L@}C?gL?Y@k@?qB@iO@cO?{O?aE?E@iX?cF@{O?oI?Q?{BAw@?e@EgBAi@GyAC]AUIwAC[Gu@QsBI}@KmAUmCKeAM_BCUkAsNYcDm@eH_@wEu@uIs@iI_@oE]mEwA{P}@gKUmC_@uEEa@AOEo@AC[aDGc@CUM}@Ms@O{@YmAYgAU}@ACACY_A_AuCWy@Wu@Ww@Qk@Wu@c@sASo@Oc@IWi@eBYw@s@{Bq@wBk@cBUs@w@cC_@iAs@wBUu@So@IWk@eBIUY}@i@_B{AyEk@eB[aAY{@u@{Bm@kBW{@c@sAGU]aAcAaDGQeBoFq@uBqEgNiAoD{AwEk@eBM_@i@aBi@aBIWOg@CEUs@Sq@Sm@Ww@Uq@i@cB[aAa@oAWu@Sq@Uq@Uo@IYSo@s@yB{@kCOc@s@{Be@yAOc@i@cBa@mA_CiHg@aBe@wAY_Aq@uBK[s@uBSo@_@mAaAyCSs@IW[gASy@GWI]Qs@GYG]WmAOu@UoAAKCKMy@QkAQqA[cCIs@Is@Ek@IaAEg@Es@Eu@KcBQ{CMiCQyCOsCGyAG_A]sGAOu@sNe@oIEkAIwACc@CU?IEm@Q}CGoAG_AA]Eq@I{AIuAE{@GsAIwAEw@A]SyDKcBMsBG}AC_@KcBGgAOuCKoBIuAEu@I}AGuACUGsAEu@MwBGkAACMaCGwAGy@Ey@GoAGaAKuBG_AIkBSqDO_CEcASwDCm@GgAOoCGeAEo@Co@MwBQmDEe@Co@MwBGiAAS]qGEo@S}DGuAG}@KsB_@{GaAkRM_CKkBEo@MoCOmCEo@I}AEo@OuCOwCASOkCs@yMS}DU}Di@gKYmFOoCIsAOqBKwAIy@OsASsBe@uDIg@U{Aa@iC[sBeFy[s@oE?A[mBIm@e@uCa@eCUuA{@wFk@oDo@}DQmASkAEYG_@QeASqAG[WiBKy@QqAKy@aA_IOuAIm@?E_CgSaCmS_AwHSkB_AeICKMoA[kCKy@AMUeBiAyJGk@e@aE]sCy@cH{H}p@aHil@m@kF_@wCAYOoAQsAMmAkA{Jq@yFm@gFm@gFeB_Oq@uF}@}HoBsPw@}G}AuM_BcNGc@{@mHOuAY}BOuAi@sEa@eDAMGo@CUMgAIaAIiAOeBsAsPg@iGQyBKuAcF}n@KsAMcB[kDIcAOoBKwAGo@M{AOuA?GGe@QsAKo@O{@O{@YyAUcAOk@g@iBi@eBi@{AWo@Qg@iI}Re@kAYs@Wm@GMYq@eBeEa@_A_AaCeBeEsF}MeBiEsAaDc@gAu@iBSg@Se@}BsFcBeEkAuCqA_Dm@uAkEkKwAmDiAoCSe@{BmFSg@eBeESg@w@kBoBwEi@qAwHeRaB{DCISg@yBmFSg@Sg@qA}CSg@kAsCcAgC{@qBmAwCyDiJi@oASe@qA_D{@uBYq@Yq@uBcFaD{He@mA_@}@aJoTg@wA[_A]iASy@S{@Q{@Ou@Ga@CICQ?AQeAM_AKaAIcAIkAAc@Cm@I_EAiF?A?oI?yKAqT?eQAeEAkO?iA?_@?m@A_H?oC?qA?mACeG"
                            },
                            "start_location": {
                                "lat": 41.49241019999999,
                                "lng": -95.5854925
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "15.0 mi",
                                "value": 24165
                            },
                            "duration": {
                                "text": "14 mins",
                                "value": 822
                            },
                            "end_location": {
                                "lat": 41.650698,
                                "lng": -93.57712409999999
                            },
                            "html_instructions": "Keep <b>right</b> at the fork to stay on <b>I-80 E</b>, follow signs for <b>I-35 N</b>/<wbr/><b>Chicago</b>/<wbr/><b>Minneapolis</b>",
                            "maneuver": "fork-right",
                            "polyline": {
                                "points": "qmz|Fdql{PDCBE@C@E?G?I@}@@q@@y@Bo@D{@De@Fq@F_@F_@N_AJe@BOBMJ[DSPm@To@`@cA`@}@r@oBDKlA{ClA{CHYBKFOLc@He@Hg@Fg@Fg@@IDu@Du@?A?[?_@?A?_@A]A[Ek@Es@Mw@SqA[iA[y@]u@]m@e@q@i@q@g@e@e@]c@Wo@Yk@Q_@I_@G]CW?g@@]?_@B_@FUHWHA?eAb@]P_@Pe@V[Nk@VkAh@]JwBbA_ClAcD|A}Ap@w@\\A@KDaAb@_@Nc@Pg@Ni@Js@Ns@Ji@Hm@Bq@@i@@W@sJ@kB?]?I?E?EBCBEF{CAc@?_BEkA?{CAoC?{FAK?wHCgA?w@?s@?UBM@[AQ?eBAsBAwB@aBBeJGw@?w@?kBBiB?mMAu@?yI?a@?yG@{D@gFF]?A?a@?A?wC@eC?A?cCAuB@sMHwB?iF?sPBo@?c@@G?yA?uF@iA@qC?sMBmE@_L@aB@S?WA_@AY?_@Ck@Gi@GEAe@GUCUEg@KYGCAm@OEA]KQGEAe@Qg@Q_@Qm@Wy@g@w@e@]W[SWSYUm@g@SUGEKMUUOQWYc@k@]e@KOMQU]]k@MWGIOYMUm@sAYq@MYM[Ww@Og@Uo@K]K]Mg@GWGSEWGUGYI_@Ki@Mu@My@Gm@Ii@I{@E_@C[Eq@Ce@Ck@Co@IwF[g^KoLA{@QuP?[AcAAo@EsDAkBQ}RM_NGcGC}ECyDCqAGcGIiIGmFGmF?AEiFAgBAo@CcC?K?O?AI{HAIEqFE}E?o@G}DE_G?{AM}KMoOAq@E_E?o@EeECaCIwJA_CE}BC_CA{BA_@?K?KCmCCmCAyAAk@?gC?G?o@?{A@oCDqCTuNH}E@[D}BBuA@g@?GBuBBeA@o@@{@@}@@[BgBDwCFmCDiCBcB@w@@o@?I@e@BgA@iA@i@@i@@q@BeBBq@?W@e@@k@BwA?W?C@W@e@?EB_AHeF?QF_DDwB@w@?]@c@B}@@{ABu@?O@e@BiA@{@@q@@q@FaC@q@HaFLuGHsF@a@?O?QHsET{NDaCFmEBuA@a@FoDBgBFyCHsEFgDBgCD}B?W@cADiCDuBDeCJsGDcCBo@?K@gA@KB{A?CBgBD}BBiB@i@@S@_AFkDDaC@m@@e@BqABoA@gABoABiA?OBmBBw@@y@?CXkQNkIJwGJmGPqKrAcz@BmAJmGDsD@iA@C@aBDkE@w@?[@aB?m@@q@@cE@gE?sA?_EAqO?_E?oC?{G?iA?iA?mC?uA?uF?mEAeF?kNAwB?uB?mKA_K@eA?cA@oKA{E?_E?_E?oFCaCA_AAiBGeEMkGYwMA{@OgHCaAC_AUoLM_GG{BEyB]gPGoCI_DC}AC}AGoCYqMC}@Cq@G}AGaBO_DQ}CWyD_@}ECaAAc@AC?W?y@?e@?a@@g@@g@B_@B]@ODs@Fu@Da@?ALkA@ONeBB[Dk@HoB"
                            },
                            "start_location": {
                                "lat": 41.5920885,
                                "lng": -93.7859502
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "5.1 mi",
                                "value": 8193
                            },
                            "duration": {
                                "text": "5 mins",
                                "value": 277
                            },
                            "end_location": {
                                "lat": 41.6621959,
                                "lng": -93.4804503
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "{{e}F~wczP@YAgCAy@E_AIoAKeAKy@WaBQu@q@eCUu@iBoEQa@GMM[CIM[M]K]Us@EUe@yBIa@Ga@Ga@Iw@QgBKmAK{AOmBIeAs@{IEm@mAgO_@}EC_@E[?AW_DqAuPGo@M}Ao@iIC[mCc]UmC[}D_@_FmAmO]aEOgB?CCa@cAgMKoAYqDSgCEm@eBmTe@iGg@kGe@iG]gE]uEK_AUgDEc@a@gFe@gGACkAsOOgBa@aFu@yJW_DCWCWUsCYkDUsCUsCEk@QmCS_CEe@c@yFYoDQ}BM_BI}AIyAGqAGcBEqBCy@CiAA_A?{@?iAA_E@cD?_ABoL?qB@oA@aGFoM@eD@s@@eD?eDB_HDcIBiD@iC?yBBaG@iC@aC@gC?kB?oBA{@CsASmFEg@K{AGw@M}AOcAO}A"
                            },
                            "start_location": {
                                "lat": 41.650698,
                                "lng": -93.57712409999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "65.1 mi",
                                "value": 104703
                            },
                            "duration": {
                                "text": "56 mins",
                                "value": 3356
                            },
                            "end_location": {
                                "lat": 41.6956835,
                                "lng": -92.2359129
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "wch}Fx{pyP]eCg@}CaAqE{@sDcAmEcAoEmAiF{@qDsA{F}AaH{A{GwDmPy@yD}B}JyBoJiAmFMs@CIEUGSESEUEUESMm@Ki@Ki@Ik@Ki@O_AAIc@qCe@eDS_BOgAMiAGe@]{Cc@cFKcAaAgL]{DGm@aBkRy@cJc@_FkBcTa@{E[gDMwAMsAMqAOsAOsAMoAOwAKw@Iw@QsAIu@Kw@QsAMaACOKy@QqAKw@Ku@OsAESSyAQqAQsAQsAE]OoASqAUmBWmBYoB[iCo@yE{Ew^?EG]}BaQE[i@cEAGoAoJIm@OiAsAeKeAgIi@aEi@}DQuA]mCYsB[_CUoBKw@SoBO}AGu@O{BGy@E_ACq@GcBC{@Cw@A_AAmA?eA?M?k@?}C?aD?sC@sD?_B?sK@qE?uC?y@@mD?kG@i@?kD?eC?[?cA@yH?uA@eE?wA?gG@_E?oC?u@@oB?W?c@?c@?U?cB?oA?mA?A@g@?G?qD?mB@kB?kB?eC?cD?aB@{B?cB?iD?i@?I?C?_@?_A?eA@}A?{@?aA?c@?w@CaHAgBCgCA_BCqCCgEEmDAsAAqBCqBAoCC_CAs@AwAOiTG_HE{EGeICuBAsBCgEAy@AgAAeAAyAAy@?c@CcDA{@AsACqBAuA?}@AsACqB?KAiAA}@A_A?u@AiAAI?e@?g@EuCAsAAmCAwAAY?c@AsACmDCoCAi@AgAAuAAqBCiBAcA?c@AoA?OAi@AsBCoCEcFEiEAwAAsBGaHEcFEgFE_G?_@A[EaF?o@?KCsDAu@CmCEgF?GC}DImKImKEyFAaAAsAAwAEaFC{DC{CGyF?oACuDCiB?[?SA[AaCGsG?e@EeFAqAAsAAi@Ak@EuACaAC_@?AAYCc@AIEu@G{@CWI}@Cc@Ea@Iq@Gg@CYE]Ik@Gc@AIQgAa@{BYuAg@eC_@eBOu@Mo@Mg@IY_@cBKs@WgAKk@UeAOq@Oy@WwASoAO_AIq@QoAOsASoBMuA?GCYGo@Ew@Eu@C]Ew@Cq@IwBIcCAKMiD?IWkHQ_FKsCGsAMeEIqBAa@E}@EmACs@A_@A]Ew@A]C[AMCi@Ew@C]C[C]CYGy@CMEi@Iw@OsAIs@K{@WoBQsAc@gDi@cEE]Im@e@yDIm@QsA[iCo@_FqAmK]iCOgAmAuJc@gDk@sEAKWoBIu@QuAU_BCUk@sEiA{Ie@qDScBq@mFEa@m@wEcA}HeBkN[aCQuAy@qGSgBuAmKOkAqB{OGm@SyAWuB}A{LaA{HY{BMaAIo@k@kEqAmKwDgZsBmPuBqPmAkJAIs@{Fk@mEkAiJSaBIm@s@wF[eCQeBI}@MmBG{@E{@CYEwAGcCCkB?cB@{A?g@@_ADwADuAJqBLsBH}@LmAJeAFk@Hm@F_@Ju@RqALu@Nw@^kBHY\\wAPo@~A{Fp@cC^qAd@_Bf@gBrBmHv@oCtUyy@Ro@dBiGhLka@zEwPXaAt@mCh@gB`@{Ax@sCXcAl@wB|@_DXgAf@qB`@aBTkAPy@n@qDb@}C\\mCVmCPqBJwAZsEVmDToDViDTmDXgEVkDXgEPkCRoCNmCJwARmERyFLwCJqCDwAVcHVaHXaHnAu]JuCDgALcDF}ABo@FuABy@VaHV}G?IRgFBk@RwFBg@NaETaGRaGDw@JoC?AL{DP_EB_AT_GX_ILiEFmC@cA@SBwCBwALaN@_C?CFuEDcFFuFDuFFuF@_ADgFL}NPkPHiJDcE?_@DcDBmC?C?G@wA?E?_C?e@?qAGyCGeBSaFK}ASgCe@eGYmDk@aHIcAEm@[}DCa@UmCG{@E_@c@sFKqAKqA]gEQcCG{@SiDMyBKaBKmBAIS_EUeESuDOiCYgFMoBG}AIaCC}BAyAAuB?iCA}IAsE?{I@wE?i@?{A?aB?Y?M@qB?W?mJ?g@?{H?U?cE?_E?W?M@eD?{@@eN?uD?o@?G?yD?o@?C?uD?w@?I?e@?IF{I@u@BkA@W?O@WDyCJ_GJeF?GB}ADsCLaHDeCHyEBeA@{@FyDB_ADiDJgF@s@HmDF{EBkB?kB?M?_B?oC@o@?}@@iJ?iB?oR@oL?aI?qE?o@?_A?aF?o@@_G?_@?o@@eI?qE?iC?oC?gD?eC?yB@sA?K?o@@qCRsRFuDBmAD_EHoFJqI@gABuBBq@DkCDmCReODuC?O@YDuEBkAFoFZiSXkT@i@HmF?[FcDBmB@w@@q@FeE@o@DqDBwA@eAHoF@m@DqCFuED{BH_H@o@DoCLgIFyEH}G@a@?CJ}GDaCDmBb@eTNyGFoC@o@L_GHiDN}GFsDHiDX_NJuEDoCh@sV@o@BmAFqCB_A@o@F_DLoGBo@BkB@mA@qC?AAkCAw@EwBG_BGyBK}DO{DMqECqAKmCK_EYkKKsDEyACw@Cm@]_NCo@S_HAo@KoDS_HC_AQcG]gLQsGK_EAm@?ACq@Cm@IwCMmEScHIqCGyBOgFGaCCo@?EAi@AMA]EyBK}CCu@Aa@IcDU}H]wL?CCm@CcAi@gRa@kOU}HCcACg@AQAQCc@Cm@G{@I{@CYIw@QmAEe@EWKs@UwA]kBYqAOs@e@eBm@cCWaAkCaKcGqUi@yBQo@g@oBOm@GSCMSw@IYOq@{BwIcA{Di@uBCKSu@e@kBOk@AGg@iBCOW_AWaAyA{FCIm@_CmBqH{EgRoBsHi@sB]wAIWU}@GWGS{@iDeCqJkAwEK_@GWGWI]CKKe@G]Mu@G_@G[EWCSAIOsAKkAKyAEs@EeAA_@?[A]AoBAaC?qC?s@A}J?qE?oAAoC?U?Y?oCAqF?_E?o@?qCAo@?qLA_E?_EA{D?E?_IAcGAmF?o@?}A?qDAqE?o@?wA?w@AaE?}D?q@?I?y@?qC?[AoE?cIAmECaX?aKCcQA}GAeQ?}D?gB?kAA_B?aB?oH?CAmGCcR?[?yA?}F?gC?uD?m@AeLAyD?{D?iFAoE?I?WAkGAgVAaB?iGCi^?oA?q@?c@?_CAoC?oD?wBA_B?qC?iAAU?a@?sB?sC?sB?_A?aAAoL?mC?}@AoD?kF?{C?gA?wAA{A?sA?a@?sC?K@uC?}@@{C@yB@wA?U?uA?A@wA@c@@cE@yA?Y?c@?{@@q@?{A?A@sA?w@@wA@oC@wA@wA?}@@sB?S@}A@oC@sC@{B@oB?wA@{A?{@@uA@sB@sB?]@{D?U@sB?wA?sA?}@A{@?q@Ac@Aw@?_@Au@Aa@Aw@?]A_@Cs@C}@?K?KA]A]A]A[Aa@?[A]A]C{@AYAYAa@EwBEuAAy@AKAo@Cy@Cs@A_AC{@A]Cy@As@C_ACy@A]C{@EsBGmBEuBC_AGqCC}@O{FEyAC{ACw@C}@AY?ICu@Ai@Ag@EuAC}AASAo@AOC{AEsACy@A{@Au@?_@AyA?s@?g@?O@{@B_CB{@BsAB}@@CBuADmAF{BJkDBcA@q@FaB?UDiABaADgBFgBDmB@]By@By@Bm@@o@@WD}AHmDF{A?YDeA@o@Bo@?KHoCBw@BeABo@Bu@DsA@y@DuAB}@B}@By@By@B}@Bq@BaABu@DyA@y@BwABsB?m@?G@_@?sBA{A?w@A{ACwA?y@AqAA{@?{@A_AAwAAqAAc@?{@Ao@?]CwAA_BAsBCsCAwAAu@A{A?{@Ay@As@?_AAyAAeAAm@AwAA{@?o@?IAy@?{@AY?a@?s@Ac@?uA?{@AwA?]?uA?{@AwA?uA?yAAK?m@?s@?o@?Q?mCAc@?w@?KAgAAaLAoB?sBAwC?sCAoCAsC?mBA}B?mEAsB?uBAiD?{BAqCAoD?mBA}B?mA?g@AoA?qD?e@AsA?qA?y@AcA?wAAqC?yAAmA?{@?y@A{@?I?o@?wAAy@A_EAmA?qBA{BAsB?wAAy@?uAAoB?}@AuA?w@?]A}AAqC?MAuFAi@AaE?w@AuB?Q?e@AoDA{@?aAAoEA}BAaEAkDAsDAyA?wA?oC?wA?}@?y@?{@?yA?{B?gB?W?c@?kBAgA?aI?oC?_A?uJ?}@?_@?]AkF?uA?gD?G?{@?q@?iA?U?y@?uB?{A?w@?kB?}B?sC?sC?sBAsE?{@?s@?yG?I@mE?qC?uB@iD?uC@{A?gA?k@?uB@aJ@}C?mC@yHAyY?gf@AkF?sB?qh@?o@?o@AkK?wP?aG?}B?yB?{PA}H?o@?M?_K?eH?eGAoDAs@AaAEoECuAAa@M}IC{@QyKS{LUkOEeBOaK[mSAs@?CC_B?CA{AC{A?{A?U?g@?}@?o@?k@?G@oB?iC@}ED_N?k@?wA@i@?cC@k@@qC?gB?gB@{A@mD?k@DqP?aJBwE@mB?mB@cB@uB?M@iC@wH?O?G@iD?W?W@gD?WBcGByMBoE@eA?W@IDcDFmCLmFh@uSFyBNgFBuALuDN}FNkG^eNJ}DBo@@q@HmC@o@F_BP_HBo@ToID_B@_@?ODwABw@Bo@BcAF{B\\kMFuCBuABmA@iA@i@?g@@_B?s@@aBAwBAeCEqOAoFCaEA_HOsd@Osg@A_FAOAqDEgR?YAo@GoSA}BCaKKc]GsRAiBEkRA_ECuHEoJAuBCmBEmBCmBGmBGmBC{@M}C_AsYMmDMwDGgB?MAKEmAGyBC{@Aa@Aa@EaBAa@?s@As@AS?o@Au@?{B?oEAiF?SAmA?iE?q@?aDAsGA}N?wHAq\\?M?_@?A?qB?m@?W?wC?uB?uA?cB?qF?M?a@?_@?qB?u@AgC?sA?aC?gC?gC?{A?qA?{C?eD?O?kA?aB?mA?sA?E?i@?MAcA@_S?mE?cC?m@?oC?C?o@?s@?}EAiB@}\\AsJ?iD?a@?aC?yC?Q@}B?eA?k@@Y@}C?y@FiIF}IBwEBsC?k@@mA@_A@_C?]BcD@_BBgEFmIBuB?U?k@?C@o@?aA@]?o@@M?u@@g@?q@@a@?w@?_@@y@@a@?uA@}@@oABgEByCD{GFoJByG?e@@oE?qA?sD@aEBq[?aE@}A?qF?M@qH?kA?C?iA?cC@iD?kO@_IBuG?A@{D?sB@{C?o@?aC?qA@gF?oF?K?I@iN@cB?{A?uA?yB?s@?w@@qBAU?aEAoIAcB?u@?{AAwA?yA?uA?YAe@?yA?kAAkA?uA?}@?yAA}A?wA?aAAo@?kDAeB?i@?}B?QAgBIgj@?EAoLCaHAkKAsCA}JAeCAuMAsHAgCAgMAiGCaNCmIOcc@EaK?YCkEAiDEkK?[AgA?c@?{@M_YCwG?_A?E?gA?mAKaWC_JAeDGiNGiQ?EAmB?cBAqBCsFAkBAqB?_AAa@?cA?uB?sFBmG@wA@{ABmBFcG`@_a@D_E?MDsDf@ci@B}C?[?{@?u@?u@@gCAuF?qC?iCAkA@wC"
                            },
                            "start_location": {
                                "lat": 41.6621959,
                                "lng": -93.4804503
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "81.2 mi",
                                "value": 130707
                            },
                            "duration": {
                                "text": "1 hour 11 mins",
                                "value": 4261
                            },
                            "end_location": {
                                "lat": 41.60363590000001,
                                "lng": -90.6852404
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "_un}Fly}qPA]?u@?s@?]?cGAmFAwBAwXAoJA}DAaH?W?G?o@A_PAcF?oFAqICqUAaE?wDAoF?qCAgE?KAyE?{@CoFAqFA_EOsg@AqC?sBAoCCgD?{AEaQAo@A_HA_BA_E?q@EkL?cBCqG@}E@aFPsq@@eA?wABuJ@eH@cGDuO@kC@yE@cA?cA@sEFaTBwH@aE@wC@_D?}ADyP?w@?w@BwD?uA?u@@aB@sA?uA@wABwBB_B@YD{AHuBJsCVsGHgBHuBHuBFyAHuBFwAJuB@]FuABy@FqABaAHwAB{@FwAHuBLqCB{@HsBJuBRiFJsCFwAFwAHsBJuBBy@HuBFwAFwAFyADy@By@FwAFqA@e@BYFyAHsBFwAB{@@YJyBBw@FwAD{@FyAFwAHuBJsCJuBLqDLqCJsCHoBD}@HwBHsBJsBHsBHuBHsBJqCFuAFwAFwALoCBy@FuAHoBFwAJmCNqDD{@FkBHwBTcFJuCFwANmDBy@B[?MD_AFwA@[FsAJiCHuBRaFLkCFmBFwAHoBHmBFqAFwADuALqCHoBHsBDy@DsAHqBFsAFqAHoBD_ADsALmCDqAFsAFsA@a@HoBDw@FwABw@B]DqAFqAHuBLgDNmDFqANgDJmCJmCJuBNcEXyGNiDF_Br@uQ`@cKNgDHqB@[Bo@DaALqCN}DLsCJmCb@qKD}@PgEPiEH_Ch@eMT}FF_BLmCNgEZeHHuBHoBFqBBcABkABy@@w@@uB@sA?cD@{K?a@?M?_E?o@?{C?mD@_V@yH?cF?}G@{X?eE@iS@eG?eE?wH?iE@kD?aE?kD?O?oF@qJ?_C@aH?q@?oC?kB?sA?o@@yDAgB?qA?qA@gF?}D?Q?kC?iE@i@?wD?yC?gA?sB@uF?oC?aC?{C?uD@oC?kF?uG@{W@wD?_E?{A?gC?wA?O@o@?mA?cA?mA?qC?eE@gE?kD?uA?iD@iE?uB?yB?U?wA?mD@cF?Q?o@?s@?qC?wA@qAA{A?U?o@@i@?{A?y@?q@?c@?qC@iE?iE?uA?gE@sD?kD?kD?_B?W@w@?uB?qB?mD?oD@oC?iE?qC?uA?}@AW?WIoFMcGMcGCw@EuBEuAAc@CoAEwAO_GGqCIeDGwCKgEIqDIoCIsDIiDEiBIyCIiDGmDCeC?g@AGAmA?uB?mCBiF?uBBiD@mE@iEBgF?yABcF?qB@uB@wBB_H@oD@kD@mE@gC@}AB}H@qC@oDBaF?sB@wB@y@?mB?_@@uB@oB?uA@_@@mC?{A@eE@qB@sC@wB@oB?wB@mC@yBBsF@sD@wC@sB@qB?yA?U@o@?k@@sB?wA@wA?uA@oC@wA?u@?M@aB@yB?wA@oA?e@@y@?y@?w@@sA@uA?w@@}A?y@?]@sA?]?wA@sA@uA@eC?_A@uA?uB@uA@qD@sB@mC?cA@oB?}@@yA?w@@yA@wA@uB?qB@yA?e@?U?y@?{@@s@?c@?s@?uC?oE@qCAwA@uB?{@?sA?uA?oA?I?}@?{@?[?_@?q@?_A?uA?uA?cB?oA?y@?_@?oB?a@?]?[?]?s@?y@?c@?oC?sC?{@?oE?y@?uB?mC?{A?qB?wB@qBAyA@yBAuA?mD?_A?qC?wA?K?kA@kB?w@Ak@?uA@wAAwA?_@?w@?sC?wA@{@AqB@yA?sBAqB?wB?wA?uB?sB?W?}A?gG?uA?uB?sC?qD?iQ?S?uE?Y?oF?oD?wA?kF?kG?s@AqC?}A?w@AqDAw@?c@AmDAuAAmDAi@Aq@AwC?o@GoLC_E?gAAiAQw\\?IEaHC_HA}A?_@A_AQi\\AaB?[GwOEaGCeI?gB?sB@wE?uB@gB?wD@aD@eDDqPB}A?gFDyKBmJFaT?}A@qCDcS?_@@cBFwSA_CEqBEuAG{AA]MwBM}AMwACMC_@YkCIo@[}CsAoME_@]gD{BkTsEqc@oC{WIm@Go@YkCWkCIo@CSu@qH]}CQeBs@_HaAeJEe@}@wIq@mGYqCAKW_CGm@WiCIq@Gm@k@wFo@_GAKGm@YmCGm@Ee@MwAAOKcAI{AGmAE}AEwACyAAoBA}AAaBEoFAm@?e@C}CGmH]uh@EoF?o@CqCCoCGaKEoFC}C?a@AoC?a@?wD@sA@iBBoDBkCDaEZa`@FqIL_N@o@?o@FaH@o@?o@F_HBkCNeQByCNwP@qADoE@oB?EByBBoCH_K?aA@}@HsHZ_`@ByBB}BHsJ?o@HwIH_K@_@DsEL{OFkHDwE?ABqCDqF@uADmD?y@@wB?uAAyAAsAA}A?SKaIAa@AmBCmBEyDCoCIaJCyAGoIGsE?GAg@?G?CGyGCaBCiCAo@?w@A]?QAg@E_EAqACoC?_@C{C?CAoCAqC?aA?sC?cB@wN?{G@kIA{F?_K?{J?kCAwG@iF?eB@sB@mA?O@cC?k@@}ADuI@}ABcE@mDBoDDeEDkH?QBsDBgE?o@B_E@o@BaE?g@BwFFaK@aB@q@@{E?Q@u@@u@DqIB_E@{@@sC@i@PuFJoC@UBq@HkAHaABYBUFq@Fu@Hs@Da@Jw@PyA^cCj@gDFa@Hc@TmAl@sD@Al@uDJm@`@aCX_BdAkGfAuGJm@FYBSJk@ZiBRkAJm@F]ZiBf@sCzAaJX_BHe@f@}Cj@aDDWRgAPcAV{ATuATwAd@qCXeBBKBSBMBKRoAJk@Jm@jByKx@{Ej@{D?ANcA`@}CD_@b@}DLkABSBS\\{D^eF@MFeALsBDs@@YHqBHmBH_BD}ABy@@s@@_@@y@DyADkC@sC@eD?kA?qBDcF?oE?iB?M?eA?QBaC?y@?y@?iEB_EAeA@eA?{A?uB@{C@_F@aD?wAC_AAaBI{CGwAM{BO{BWcDo@uIQwBEo@wAaS]yEk@cIEo@WsDIeAKkBE{@A_@AIAe@CWIwEAmAAaB?I@wE?m@@o@@wBJ}OFwG?CBcD?CLeQ@w@B}D?KBoDB{DJuNBsBD{GBmC?o@BmCLgRDkF@eB@wA@o@?G@iABkFF_K@SBgF?U?ODmF?AH}M@s@?WBgD@a@B_D@}ADqFB}D@gA@aBBoB?MBiE@yADcE@q@@g@DsBBc@@e@HgBBg@J{AHkAN}AH}@RkBJu@NmANaAHe@L}@N}@\\cBTkAPw@H[XqAVaAzBoIlBiHn@aCr@mC~AeGh@qBNk@t@sCd@gBp@aCp@eC?CfAwD`@}ANk@VaA^uAf@iBNk@@Iz@_DtAiFxBiINk@`@}ALa@Nk@\\qA@Cb@aBl@_CJa@jAmEx@{Cn@cCjAkEZoARu@d@cBd@iBH[DMLe@ZkAd@gBFWDMhAgE?CLa@?ALe@x@{CBM|CoL|@cDxAqF@Ex@}Cf@kBl@_CPo@p@cCLi@r@mCf@kBvAkFnAyEXiAPk@x@}CtAgF?AjAmEPq@Po@@EJe@f@uBd@cCHe@Lm@TyAHm@NeAFa@@KVqBLgA@KDa@BYJoAF}@Fu@D{@Fw@@]Du@@a@DqAB{@BsA@y@?a@@y@DmDHqK?ELkN@iA@aBNoO?o@DiDRyUDmG@GRmWFsFDqFFoFNyRHwGJqLDqEBoDBuBBcC?c@@K@aBB}B?aA@o@@wB@uAAqA?_@?O?iACqAAaAAw@CsAGqBKqCCq@G_BCo@G_BCo@EaAEmACo@Cm@OcEMsDOgDGuBIuBOqDOkEScF?AMsDMgDCq@AeAC}@AqA?EAw@?u@@uB?_@@{@BsAB}@@s@Ba@@[?AD{@Bu@B_@BWD}@Fs@Ba@B_@RqBLqALeAd@mDzBwPHe@RyAR_B|@sGXyBtAaK^qC~@}GBUj@_Et@}FPqAJeALqARaCH}@FaABg@FeABw@Bm@BaADoAD_C@oB?wB?{@CeIAaDEqRA_ECoFCgJ?gA?o@AoC?UAaB?}A?aAAcFCoF?e@AiECoIA_HAqEAyEAkB?kE?gB@iBBmD@qAF_DDiCD}AZoL@m@@[@SFoCDcB`@yOl@oU@a@HmC@q@Bo@ZmMHoDReH@[B_BBoA@wA@g@B_E?iB?cA?y@AyAEoF?WGgG?AEmFMmNKuJEoFYgZCkC?_@?OE_DIqJCoAAwAGwH?_@EgF?WCuC?{AAgC?k@?qA?}@?o@@iJ@iH@mE?uC?aD@kJ@oI@aE?_B@oC?_B@qNDs_@?e@@iE?qFB}S?q@?_B?c@?qA@{B?U?K?eC@mC?QDsb@?}E@cH?Y?a@@}F?uC@wE@_ADyB@s@Bo@DsA@M@_@Dw@Bi@BS@YHiAHcA?CFk@PaCF{@Fq@f@wGNoBd@cGRcCt@cKLuA^gFBSZ{DJwAr@gJh@eHb@uFt@_KFm@Do@RmCFm@r@mJn@kIVyCDm@TsC^gFH_ABW?EPwBNoBFaAPoBNwBFw@B[B]PqBNuBBUB_@Fy@H}@Fy@BYF{@F{@Hy@JuABYF{@B]Fy@D]JsAF}@Fw@F{@Hy@Fw@Fw@@ODk@B]Fy@Hy@Fy@F{@Fy@B[Fw@LwAJsAJ{AFw@Da@B[@SDc@LwAJ_ABUJy@Jw@Lu@F]F[F[D[F[Pu@F[Pu@ZoARq@J]Ps@Ty@V{@Le@r@eC`@}ALc@Ni@Lc@Tw@Ru@DMLe@p@cCp@cCxAkFJ_@ZiATu@FWh@mBLe@Ni@`AmDNi@d@aBf@iBdAyDLg@Pi@d@gBPs@T{@r@yCH[Je@\\{A`@kBj@kCl@wCZ{APw@FYVoA`@oBXoAXsAh@iCVmAXsABK\\_Bf@eCNu@Py@Ns@XsAVqAPw@p@cD`@kBn@cDZwALo@Lu@@GLu@RmAD_@Lw@@GFm@D]J{@Jy@Fw@Hy@NoBF{@F{@@]Dy@B]FwA@u@DwA@}@@{@ByA@sB@S@g@?w@@_@@y@?E@oA?a@@u@@a@?{@BqB@wA@q@@g@BmCBcDFyF@yB@YBuCFgG@uA@yADqC@qBB{@?sA@e@?I@o@BqC@wA@q@B}DDwCBoD@_A@y@@{A@y@DmBBsABg@@o@DwA@o@?I@GFsBDmB@a@@{@B{@@a@@O?C?c@@[@_@?YB}ABcB?{@?KBgCBmB@}@@uA@]@wA@wA@W@cB@k@@kA@uB?A@}A?o@?C?]?y@?]?uB?_@A]?y@?{@?{@?q@?E?{@?wA?e@?s@@y@?a@?o@?C@wA@u@BoC?o@RqV@yDNePBaE?GBwABmD@aA?sB@cA?q@BqB@kA@o@?U@wB@uABcC@gB@]?[@[?]?_@@{@@{@BgCDqF@sBBuC@{A?o@@_ABsCBkDBiEByCBoC@uCBsB@sB?u@@}@?K@kB@eC?I@qD@eI?uA@{A?mA?aD@s@?wA?{@?sB@yA?oB?sC@oD?{@@{C?U?]?uB@sB?wA?sB?cA@cA?yA?{A@{@?_@Bu@?a@@]@_@@Y@[@W@_@BY@YB[Bw@Du@LmBDu@?A@IDm@Dq@?APcDDu@BYDs@HyADe@@UHqAFs@Fu@Fw@LoAFu@BWBUHw@Hu@Hs@Hu@B[LkAD_@RiBZeDHu@@?Z_DHy@Hs@Hw@?AFq@NoAHu@BWRkBDk@BMBYNoALoAD[LmAFs@Fk@BOHw@?EHs@Hu@LmA?AVmCJu@B[Hq@?EHs@VgCHu@RsBDY^mDlAkLFg@h@iF@In@eFdA}I~@{HbAkIb@eDLcA^uCDk@\\qCb@sDTkBn@_Ff@wD^gCPmAb@}C@EHi@h@yDBMF_@r@gFzAoKPmAp@qETcBRsA?Ar@aFd@aD@KTyAd@_D\\iCN{@TcBnAyIBUXqBLw@Fe@@KJy@J}@Dc@@QD_@PgBB_@@WJ{ADm@D}@JaCBwAB}@B{@@gA@uLAqC?s@?kC?}A?aB?qE@eM?qU?cBA}A?oCAwCAoE?eFAc@?uCAm@?kC?cAA{E?IAyBA{DA{GAkFAkE?uDAgFC_F?sCAmGA{EA_D?_@AaD?]?o@AoB?oAAoD?aJ?M?uI?mD?o@?M?aC?mB?a@?_PAiJ?gB?qF?_E?O?eC?kA?yF?yA?iH?qC?o@?uC?eHAuD?iC?uC?o@?}A@gFAkB?_B?eI?o@?{@?sA?q@?oB?oA?oA?wB?{A?_C?yD?yCAy@?iAAqAAcACqBAKGuFCaCI}HGkEEsCCgDKkH?KG_FCqBSoPIsGI_IIyF?GEwDAk@?CGmE?a@Ao@A_AE_CA{C?qD@wBDgCJ}DPeJ@c@LkFDaBBiBLeGJoEDgCTcKLuGDiBHeDD{BJmE@YFiCj@uXB}A?ALgFF_C@k@DwBLqGDyE@_B@]?Q?eEAeE?C@a@?yOA{F?aG?o@?]@_DAsC?kI?yI?aE?iF?yC?aH?oB?y@?}K?_I?iI?sC?mDAaF?sB?yA?}@?wF?qF?{J?uC?oF?w@?I?mD?oC?qC?eC?}B?mD?sH?yA?w@AcGAo@@kR?qG?uG?cD?sD?qC?iE?oA?}D?yM?gH?A?}H?cJ?}E?Q?cA@wB@_@?A@[Bi@Bk@@]BUB_@H_ADe@Di@Ju@D_@Ly@D[F[Nu@Pw@BOH_@f@sBPq@`Ia]\\wAzBoJlAcFvDePT_ALk@d@mBh@{BtDyOlAkFv@eD|@wDv@cDj@cC|@wDhAyEJg@@Ch@yBtA_G\\yABMNi@Lg@`F}STaALi@jA{ExDePvB_JZsAVeAZqANs@b@mB^uBTiAb@iCf@iDdAuIBYtAgLp@oFTkBjB_PHm@Ho@fAeJd@uDn@iFJ_Al@eFhBiO`@iDp@wFb@oDZcC~AyMLkAVqB|@sHrA{Kf@kETiBpDoZxA_M|@sH\\mC|AkMZmCD]bAmIJ_AHq@VuBRcBFc@@Id@{Dn@qFx@{GXyBBUp@{Fr@{FTmBJ}@pAqK\\qCXwB\\mCf@qD|@{Gx@cGDYPqAr@oFt@oFzE_^bAsHNmAj@gEF_@Hm@Fc@@If@wDFc@Fm@Jy@Fs@De@B[F{@Fu@Dw@Bg@Bo@B{@DsA@Y@y@@}@@m@?c@?y@AuL?_B?oC?o@?qI?gB?aMAgL?a@?_B?_B?A?kN?uLAeL?kf@?sQ?oO?cGAoA@sAAuA?]?k@?S?E?C?_@?oA"
                            },
                            "start_location": {
                                "lat": 41.6956835,
                                "lng": -92.2359129
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.7 mi",
                                "value": 1156
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 42
                            },
                            "end_location": {
                                "lat": 41.5970447,
                                "lng": -90.676689
                            },
                            "html_instructions": "Take exit <b>290</b> for <b>Interstate 280</b>/<wbr/><b>US-6 E</b> toward <b>Rock Island</b>/<wbr/><b>Moline</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "wu||Fv}nhPJ_BB{ADcBF}A?C@O@I?G@SDo@Fw@@E@OB[Hi@D[F_@He@FYH_@No@H_@HUH[HUJYL]Vo@JWTg@NYNWLSJQPYJQb@k@NQ`@e@NOLOTSPORONORMPOFCFERMVOPKRKRITKRIRGRGPGVGREl@MPCREZE|@KTCl@Ih@Ej@Ij@GTCj@Gr@I"
                            },
                            "start_location": {
                                "lat": 41.60363590000001,
                                "lng": -90.6852404
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "26.8 mi",
                                "value": 43087
                            },
                            "duration": {
                                "text": "24 mins",
                                "value": 1416
                            },
                            "end_location": {
                                "lat": 41.4402098,
                                "lng": -90.32875349999999
                            },
                            "html_instructions": "Continue onto <b>I-280 E</b>/<wbr/><b>US-6 E</b><div style=\"font-size:0.9em\">Continue to follow I-280 E</div><div style=\"font-size:0.9em\">Entering Illinois</div>",
                            "polyline": {
                                "points": "ol{|FhhmhPdDc@lAMbAMj@GTCNAXETCTCTC~@Kj@Er@EP?JA`@Az@Cl@?f@?`@?t@?t@?f@?b@?\\?~@?h@?v@?\\?lA?n@?j@?jH?bD?~@@Z?lC?jBD~CJN@j@BT@fAFzAJZBrCXvAL`AJVBh@Fj@Fl@Fj@DrANhBPbBPL@rCXdAJvANXB`@Dr@HdD^@?jCTjSrBf@DjFh@hCTfD^zFh@rCRj@BfAH@?~ADl@?pDCfAAdPg@zIWb@CrGUdGStI[fBEfBGfBEtEKjDE@?b@?bIA~EBX?b@?rDB`FB`A?jBBhJ?nBEjAE\\CbCUVEdG{@lEs@fDg@rWaEbBW`Fy@hFw@~@S\\Eb@IhBYhBYRENCzAUj@Ij@Kn@KRCbAQh@IpASfFu@HAn@IhAIl@EXAbAGZCj@Av@A\\?P?j@?T?z@@vAD~ABpABxFLnCDnCF~GNb@@bA@f@@b@@jBD~DHV@b@@fCFjCF|@An@AVA^Cj@E@?zC_@|EmAl@OpA[vA]vA[`G{AbAW`AWnM{Cz@UdC{@nDgBf@]DAf@_@`@[`@_@\\Yb@e@`@c@Z]X_@^e@^i@v@mA`@o@Zo@Zm@f@cAVs@Xo@Tm@b@eAd@kAb@kAz@wBTi@L[d@kAb@kAn@aB|@yBb@iAdAmCd@kAd@iAhBsE^}@Pa@h@mAd@cAZo@Vi@BEXk@`@y@Tc@v@wAZm@Zm@z@_BrAgCrFmKvBaErGcMlBmDxAqCxBgEpAcCj@eAv@uAp@mAhAiBtCkEd@u@v@mAn@_AXa@x@mAf@u@lAmBl@_Ar@eAhBgCnAeBlAgBlEkGX_@Xa@lIsLXa@X_@lAeBdBeCX_@hBgCV_@jAcBXa@Xa@fBeC~BgDd@s@fDwEr@aA~BgDvDmFnAeBlAeBV]fCoDXa@?Al@y@v@iAr@aA@AhCsDHMl@{@b@o@JO`@k@DEPU@EXa@Za@dBcCjBkCr@aA\\e@RWPWZ]\\_@X]X]b@a@TYl@k@d@a@r@q@LKbA}@POzP}NdB{AhEqDbCeCz@{@r@y@v@{@n@y@|@gA`AoA`DsEt@oAp@oAb@s@d@{@^u@Zo@Xk@Zo@Zq@DIRe@\\y@Vk@v@kBf@sA`@iAj@aBLc@FOTs@hCkI|A_F\\gAh@aBzBgH~F_RdPch@fEwMtAqExB{Gt@aCRq@ZiAZeAT{@`@eBR{@TcAToALo@@EHc@Ls@Hk@Fa@L{@Hg@LcANmAHw@Fs@LyADk@Fq@Bc@Dq@FcAD_AHgBBy@@k@Bs@BwA?{A@wA?c@?kEAcC?sA?m@?oC?oC?sMA{@@UAG?C?[?i@?Q@oBAeC?[?_H?uB?mBAy@AkAAc@A[Ao@Co@E{@E}@Em@I_AIcAKcAUgBKy@EWE]CMMo@O{@G[Mk@?AWgAUaA]iAYaAQg@IUK[GQSk@[y@c@cAa@y@m@oAm@eAUa@MSUa@QWOUGIMQc@s@OSm@{@gHmKk@{@gAaBcBeC]i@_@i@e@u@W]}@qA[e@[g@[i@OUKSYm@We@M[Se@Wm@[w@]aAK[IUUs@M_@k@uBQy@WcAG_@YwAO_AKm@Is@MaAKeAKqAIeAGaAEs@EcACcACw@C{A?eBAiC?qDAqB?o@?K?k@?wMCg]A_L?w@?qBAsCAoAC{AC_ACu@IqBGsAMsBEm@IeAIy@MuAa@aESiBKcAYmCSmB?EMcAW{CSoCOwBMmCI_CAOKsDCsAAw@?w@Ae@?s@?mDAkE?oE?cBAcDA}I?qJA}H?gCAsC?]?O?[?{CAaI?eG?cA@sA@y@@o@FaBBeAD{@@_@B_@@SFaAFu@@YB_@D]NiBD_@D]NqAHw@VkBd@yCH_@Ny@VqAb@qBv@iD^yANi@~CgMf@wBXsAZ}AFa@F[TuAVgBJ}@PyAVqCT{CJ{BDmABy@Bq@@i@@}@@mDCsD?sAC_DAqA?e@AiA?iACqBAiCAeDAcBA_CAy@?}@AsA?{@?}B@iBB}CDqBDyBDuA@y@@]@[Bk@Bk@D}@DsAJsBBa@ZeFF{@Dg@ZiE\\{D~@kLN_CFkADcAD_AD{@BcA@q@@y@@aA@cA?q@?m@?i@AmAA_BGwB?S?IMgFC_AG}Be@iRKmDGqCGwBScIIqCIoCEqBGwBEiBGoBImDCk@?SK{DIoCGqCEoAEcBIqCK{DEcBIqDY{JEwBEsAEyACs@]cNSsFMeDUmEMiCk@yHmA{MOiAg@qEs@oFm@eEKs@o@}Dk@gDg@iCaAwEkAsF[qAYoA[kAg@qBu@qC{@wC{@wCy@iCkAuD}@mCgBsFAEaBeFsAeEu@eCW{@Ss@U_AQw@Ou@Mu@Mo@Mw@M_AOiAMcAEg@CSEm@Gu@Gw@E}@ImBA_@?]AQAs@AiA?w@?{@@y@@s@B{@B}@Bs@Fw@FoAH}@JqAPwAL_AFa@BOJo@F_@Jo@Ha@Nq@Nq@Pu@Rw@Rs@Rs@Ro@Ts@Vo@To@BERi@d@eAn@qA@EP[JSx@yAj@{@FKV]HMb@m@n@{@n@s@t@w@fCkC~ByBJMLMvAuAVYVWzA{AzAyAtCwCLKz@{@pAsA\\[`@a@JIxB{B~@}@jCmCxAwAZ[ZYd@i@p@o@x@y@Z[`@a@bBcBf@e@JKNOxA{ArAqARSh@k@j@i@fBeBr@s@hBgBb@e@j@o@pAwAdAsAb@i@r@aAv@iAl@_Ab@u@DIPYf@{@h@aAr@wAv@aB\\{@lA{Cf@sAPg@^mA^mATw@HW`@yAh@aCTaAz@kEHa@@K`@qCJw@RwAJcABOPoBRgCJuALsCB[DsAB{@BmB@q@B{D@{A?k@FuIH_O?GHyLBqEHcO@{FBkDDmFByD?E?aC@gED}JFuJ@gC?s@@qC"
                            },
                            "start_location": {
                                "lat": 41.5970447,
                                "lng": -90.676689
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "129 mi",
                                "value": 207609
                            },
                            "duration": {
                                "text": "1 hour 56 mins",
                                "value": 6938
                            },
                            "end_location": {
                                "lat": 41.53636789999999,
                                "lng": -87.96879269999999
                            },
                            "html_instructions": "Continue onto <b>I-80 E</b>",
                            "polyline": {
                                "points": "ix|{FtiifPJeUDyI@sBFqN@iA?eA@_A?G?W@_BBaJ?kECmSAyFAmOAoF?o@G}_@AqG?mBCys@?s]AoQ?iD?mG?m_@?mM?kA?_H?_H?_E?iD@aQAwSAwJAyMC_OAoIG{V?iB?iGA}C?o@C_NAgAAwKCqF?ACoF?QAsDCqGGuMM_VG}LGaLEoLO}YAsCAcF?iD?_AA_LAoX?o@AkMCsf@?qG@}S?qEBm\\@_K@_KBw]?w@@iA?y@?kB?{@@uABgABwABm@BgALaCJoBJwAPqBNsALoAHi@@ORuAPoANu@ToAXwAd@aC@G`@cBd@iBd@aBX_ATq@`@kA^eAd@mAVo@d@eAb@_ABGfA_C`O{ZhBuDtEsJzE{JnFaLpAoCLWhDcHzCmGlAgCzNqZ|A}ChCsFXo@LULYZo@Zq@Xk@Zm@JWf@cAx@aBlAkCXi@t@_Bz@gBz@eBhByDHOP_@`AqBf@eAf@cAXk@FKx@gBt@{Ar@{A^w@n@sAf@eAd@_AN[d@eAd@eAb@gAx@yB@CPg@L_@`@oAf@aBRs@\\qAPs@Pu@No@Jc@Lm@P}@Lo@Lw@RqALu@Ly@Ju@Hy@Js@Hy@J_ATkCB]BWDy@HwAHeBDaAB_A@i@@k@@W@cA?aA@SDyHFgJ@yA@uAFuK@]?e@@qA@sB@uB@{A@qBF}I@uB@uADoE@sB@{@?uA@}@@uA@wA@w@?_@BoC@{@D_I@cBBwD@aA@sBBaDByEDeH@OFkJRa]?OFoI?[DcG?aABcD@y@?_@LiQBgDBeGDiFBgFL_RDkFBgE@uB@uAF{IDkGFuI?M@kA@cDDwE?S?c@@O?i@?U@mAB}B?w@?K@yABgB@mC@_A@{ADcGByC@eCDcG@sBDiEBiE@sB@uA?e@BiB@uA@qB@}@BeE@qCBqB@{A?i@@aBDeF@kCBsDDiFDaHFiJ@gBDeFBmEDqC@k@BgA@c@?Y@[@[By@Bw@DwABc@Bq@B{@JqBF{@FuAPoCTwCJmAFw@RqBFw@TqBJ}@Fm@@EHs@J}@Fa@NkAF]Jw@Jw@DQ?EF[XoBF]Jm@T}Af@cDp@aE?CRmArBwM`@gCHi@V}ALy@Ju@F]ZoB\\wBjAwHLu@He@@EPoA`@aCD[NcA\\yB@AHk@?AHg@Ly@He@PeAZqBJq@t@yEJm@PiARkA~@aGd@yCfCiPh@gDD]F]Jq@VoBVsBNoAD_@d@cEB[RqBH{@NqBJuAF{@Fw@RgDFmALoCJ_CFoBDwBFoC@S@o@BeB@sC@}@?u@?}@?oBAwA?y@EoC?_ACqACoCCyAC}BAkACoB_@w[KqIGgFCuAAkAAeAAiACeAEyAGuAEu@GuAKwASmCGu@OwAWmBS_Be@{CQcA[_BY{AWgAa@_B]sAm@qBy@mCw@uBSi@k@wAu@cBq@yAaAiBa@s@y@wAu@mAwCmEq@_Ao@}@u@cAq@{@_AoAmAeByAyBm@eAs@oAg@_Aa@w@_@w@_@y@Yo@KS[w@{@yBa@gAw@eCi@iBYcA]wAEQQs@WmAYqAc@gCUsAM}@Ko@MgAMcAOsAKmAIs@McBKaBEkAGuAGwACoAC_BA}@?{@?eA?eA@sB@iEHuVB}I@_C?OBiA@iAFqBFuAD}@FkAJ{APqBFu@NyARkBXsBRoARqANu@X}ATeAb@kBZmAPs@Ru@^qA\\eATs@Tq@t@}Bv@{BlAqD`AwC^iATs@`@kANe@Z}@`@kAnAyDPg@tD_Lt@{B~@sCrBiGtAaEd@wAfAeDPg@pCmI|AwEzDkL\\cAb@uA`@wAVaAT{@v@kDh@oCX_Bh@oDh@wD~@mGh@}DjAmIpAiJxAiKzAwKxBuO|@qGpByN|A{KnHsh@@I|CwTnBmNpDkWzIyn@pAoJfD}UbAiHhGkc@n@sEd@eDbAmHLy@DYj@aELw@j@aEd@eD|@uG@CHm@d@kDp@}Ej@_ETeBHi@RaBh@_FLqAH}@ViCH}@JqAPwBHmA?E?ANqBL{BLcCJuBR{DLmCJ{BbA_Tv@gPt@uOHkBl@mMd@sJTeFRcERqDFeBHaBDuADwAFyABcABeAFcCBmBDiB@m@?q@BiC@sB@aA?gB?iB?iB?aBAsAAyEAaGAyDAaCC_J?E?mDE}PCwJGqSEkQ?YAyDCkJAaIAoCA{FAeFEkOAwAAgGCcGAgF?uAAwB?mCASAwD?aCAiBCiBCuCAwBAu@CyBEsBAw@Au@?IEaCE_CEoCEsCEsCEoBEmCEuCEqCAy@AWEyBCsBAw@GoDEsCGmCAyACuAEsBCsBCwACoAOaJEsCGoDIeFEqCC_BAq@EsBEqCEiC?KI_FGoDA]EoCCoCCqC?y@AsB?M?eB@qC@g@?kA@y@BqBBwA@e@@y@@UFqBDsAD{ADsAJsBFqABs@Be@HwAJwAHsAB[Fy@B_@Fu@Di@Dk@BYLuABYD_@B[D]Hw@D_@Fs@Jw@Hw@B[PsAFk@b@sDPuA@KFk@NsAJgABM@UH_AB]B[B[@[B[D{@Bk@Be@Bu@@G@U?S@M@_@@U?C@[?]@{@BsA@wA?_@CgD?[A{@C{@A]GqBAc@KkBA]C[Gy@G}@SaC?EC[C]MsAGq@C[QuBKsAI{@Ea@AWMuAGw@Ea@Gu@KsAGy@OqBEy@Ey@IsAKqBCo@EcAEw@A]IqDA[GcC?OAi@Ai@EuDAaC?}EBoZ@oI@wE?g@?o@@oCD_e@@uE?e@@wC?q@?[?W?e@?mA?uA?mBAy@?o@A_@CwAAs@KiCGmAIqAMiBIaAMsAMuAIq@Ea@QqASwAa@iC]iBWsAWoA[oA[oAa@gB[oA[qAYmA[oAYoAOw@WqAOu@SoAOw@Kw@My@Ku@Kw@Iy@Ks@I{@Gy@Gw@QiCYwFQmDIuBKsBKoBIaBAOGyAKqBKmBGyAIuAEy@GsAMsBIuAUiDOqBSoCk@yGSqBMyAMqAMuAKcAGm@MsAMsAQoBMuASoBMsA?AMuAMuAI{@QiBSsBMwAGy@OuBSgCMsBMsBKsBKsBIsBAYC_AImCEoAAc@EkCEwBCqCAeC?o@AoAW{w@AaDAsAEyKAiFCiEAgGAs@AoFCiFCaHCeH?uACiFC{JEsLEsMAuBCeGCcJ?u@EiJI}U?UCiJAkBCcHAmEEoNA}GAa@?eGAiF?_TA}H?gQAcH?uG?cF?_B?qA?_A?eAAcD?gE?}D?a@?_@?m@?_@?U?U@Q?_@@w@@i@@ODwABy@B{@F_A@UDy@Dw@Fy@Hy@JmADi@P{ALgAJy@Fg@Hk@Lw@Lw@TqAHc@Jm@XsAb@iBLg@\\sA\\iAFSFUNg@Rq@To@\\aAd@oAJWNa@N_@FMDM`@aAr@{At@{Ah@cAdAqBv@{Af@cAl@qA\\{@`@cAb@iANa@^cAJWJ[^kARq@Tu@Pq@\\oAXoAPw@Nm@XsA?AF_@Lk@N_ATwATyANkARcB@KPkBNyAFy@Fw@Dy@Ds@Ba@@YBa@@S@]@]@a@Bs@@]@q@?E@aABgC?]@aB?y@@y@?]@oC?u@@]?uBFkP@wA?y@?s@@}A@uB?oC?wA?]AuAAwACsCASE}BAy@A[EwACy@C_A?ACm@?AAACy@GwAEy@IuAEy@IuAOsBKuAGu@MyAQqBSoBSsBUoBWqBEWQwAYmBQkAIc@Mw@G[Mw@Mu@Mu@Ow@Mu@Ou@Qw@Os@WqAGWI[Ow@ACOo@Mg@CMQu@EQKa@Su@Ok@AGMa@EQSu@Sq@]mACMOe@ACOi@AESq@Sm@Uy@Uq@?ASq@IYKYIWIYIYUs@GUiBaGQm@CGSo@k@qBk@gBQo@Wy@EM_@sAEKMc@AESo@Ss@?A[mAg@iBc@eB?Ae@iBc@mB]{ASaAAAS_A]eB]kBEUQ}@EUO{@UqA?ASqAUsAAGQkASsAMcACMWqBQsAQwASmBIu@K{@MuAC[AKQcBKuAIy@OqBCWCa@Ey@KuAAKIgBMqBE}@OiCYwFCg@?EIuAEw@Ey@o@eMM{BE{@QkDG{@Y{Fo@wLQqDMcCOqCMsBQkDGiAG{AIuACk@E_AGcAOkCi@iKc@mIMiCSuD[yFQeDSeEGoAEaAGeAOaCEq@GgASuDMuCEy@IsAI{AGwAE{AGwACuAGkCAg@A}@AE?Y?O?ECeBAyA?i@?s@A[@sB?cC@iBBmBDoBDkCBo@FgB@s@DmAHqBLaCR}CNgCTwCLyAB[PgBPgBNuAZkC\\kC\\mCV}AXkBN{@BMHm@F_@RkAXcBXiBLw@Hc@NeA@?RsAfA{GJk@?AN}@Ju@TmBB[D]LeAFu@H_ANeBDw@B]Dq@Bm@@e@DgADoABo@?SBgA?o@@}@@c@?K?e@?IAy@?oAAu@Au@Aa@As@Ae@Ci@C_AEq@Cy@CYCi@C]IsAKeAEa@AWMiAGk@Q{AOgAOgAKu@SqA]_Co@aE]}BKq@k@qDUcBUuAQiAMaAS{ASaBGk@Ea@Ge@K}@Gm@CMKiAKcAGy@KeAOiBImAK}AG}@G}@IcBEcAE_AE{@E{@Cq@Ac@E{AIwCCsBC}AA_BAsBA}B?wB?cB?eB?mC@kC?iC?gB?eB?iF?mG?Y@iD?iC?oD?aE?gC?cD?{B?Y?O?_D@oC?yA?oC?aC?oD?]?cC?uA?uA@sC?iC?uB?aA?Q?uB?_K@}N?gH?{K@w@?[@_B?kH?uA@qE?oC@qC?wABwC@oDB{BBqA?o@@iAD{BFuDDgCDuCFwCFqDDyCBsABkB?o@?AD}C@wA@e@@cA@iB@uB@{B@aC@oE?{B?qB?mA?{@Ac@?wAAyAAqBAaCAmACcECsA?g@CsAEsC?QAgAE{AAaAAu@G_DKoFEuBCiBCsACiACmBIgHCuCAuAAuDCcFAgG?_AA_H?iGAgF?yD?eA?kAAqB?oEAqA?o@?yG?eBAcAAwOAoLAqA@uC@qBBoC?[FkDL{DFuBDeAHoBR{DVwDBa@Do@LsAVeDXqCb@wDLgAHo@`@wCZ}BTwARiA|@iFr@qD`@kBRkAn@mCd@kBl@aCn@_ChAyD\\kAt@aCpCeJL_@`@sA@Cz@wCl@wBj@iB|CcKj@oBFQ~@_Dt@aCr@cC|@wC`@qATu@h@gBRs@r@aCh@eB~@}C~@}Ch@gB~ByHhAwDrAmErB{GnBgGJWz@eCLa@xEuMbEiLfFoMf@kAhCmGnAwCdA_CzD}IdB{DtFkMpBqEFKd@gA^{@jAiChAiCr@_B~@wBd@eAd@iAh@iAz@sBd@iAj@yAZw@`@gA`@iA`@gAn@mBh@cBp@yBTs@Ty@Po@Lg@d@aBZiAb@gBHY@E`@aBXwAZqARcAJe@Nu@Nw@TkAN}@He@PaAV{APy@`@{Cl@oE@Md@{D^wD|BqU`CwVnAoMrA}MZ_DRuBfBaRh@cFTiCd@aETwCzAiOl@gGf@eFtAyNx@iIr@cHx@sIhCyWx@oIVeCd@iFXeEPgEJqCBu@HiF@qB?[@eBAgI?kH?c@AmR?_EA}D?cFAsL?iF?}C?gB?q@?s@?oI?oFAqZAoEA_FAuJGcFC}GCoFEwH?k@EeGIkQCqGAaAGiNA{BE{JEkHCcFGkMCwD?gAIeQSy`@C{GMgXMaXMm[Qc`@AwBCcF?_@A{@AqBAuB?q@?IAy@A{@K_DGcAE{@Eg@KiAC]Kw@OoAU_BAGGg@AEGa@G[EUUeAGYG[c@eB?AK_@CIMc@K]Qg@]_AUk@Sm@Wq@[s@i@mASc@MWMUU_@MUIMg@}@GIU_@_CoDo@cA]e@[g@s@mA]m@Yk@[o@c@aA[w@CGSk@O][_A_@kA]iAU_A_@yAYsAEQc@gC[wBWaCOyBEm@MyBI_DAcB?G?g@?aADeDFmE?ID_C@qAFwCDkCFuCBsA@i@@o@@Q?C@g@@g@?O@W@e@@]?I@g@?G@eA?M@Y@e@@mABmBFmEHoF@o@PsKFmDDmD@a@@o@BoBHuDJwCBy@Fw@HcAHcAVwBFc@Hq@Hi@Ji@XiBv@qEh@}Cz@aFbB}JTsARoAd@gCh@}CVyAd@wCp@cEJm@DWRwAPyAP{AJoAL_BDgAH{AD}A@mAB_B?{A?oACsHAeG?kAAkFAuC?uA?{F?AAuI?}E?yA?gB?eA?aB?mC?iB?eC?o@AgA?wO?cHAmK?{J?gI?GAgJAw]?m@?cF?K?AAcGByE@mCBkDFeED_B@mAb@kYFcG@}A@mB?cC?gB?eB?E?i@Aq@AmE?kDAqDCoVAcGAkBA}J?wDEw[Isj@Ms~@CiLGog@?a@?k@Gof@O}fAA_E?o@MkeAAgFAgH?o@AgFCuVA{C?mJEqYEwWC{U?sBAoI?o@AwB?gDCwJ?cC?wCAcJEeX?CCyVAoDCqO?kD?o@AgMAgJAwICeL?o@AcHCiR?oFCiJ?eD?o@C}VAyC?uG?o@A{AAuIAkO?o@Ao@?a@AmP?mDAuC?uCAmD?{BAYCsACwBC_AAQCc@A_@GkACc@?KMeBIgAEw@Gm@MuAK{@CYKu@Ge@Ks@M_AIi@?Am@iD[_BQw@Qs@Oo@Sw@Ok@U}@W{@c@uAW{@_@gAe@qAk@yAc@cA[s@a@{@q@yAe@aAeBuDMUmAkCg@iA_A{Bg@yAo@mB_@kAIY]mASu@[kAQw@YqAYsAO}@i@yCWkBWwBQyAIw@OcBKkAKgBKkCIiBEkBEmB?wAEgC?{BCwFAeB?gCA{CEmKAqDAoEA{BA_C?e@C{GAeBAwBCaC?qCAoDAuDAcECgEAcCAcGAaDGkHI}EM_FUmFIaB]{GCm@UgFCu@Eu@G}BGiBAq@EoBE{DCqDCcCAcDGiLGcKAuBAsBC}DEkGCuD?I?o@?A?s@?yA?E?i@?S@u@BoCDoCB}ADkAHmDHoCRoFBmAJmCBqAP}DRsGPuEf@yOBq@@]b@gMVuHZoKF_ANqEH}BPgFRcHB{@TeOBwBBmE?}B?O@iG?kD?Y@qD?oB?oF?iF?_E?kL?kJ@kJ?_G?}J?{E@mCAcB?uC@}K?yF?gD@iGAq@?oD?iB@oQ@oFAcF@o[?K?oI@qX?{@?yM?cB?mH?cC@uF?q@AwB?{@@oC?sT?eK?_B?u@?m@@aF?gN?}G?o@?wE?eJ?}@BiAAeB@qLAkD@mF?kF?mB?}D?iAAuD?yACeOA_HA_HA}JKed@CcIAsKEkL?sCCmG?oBAcHE{NA}IA}JAqDEiOA{IAgCAyCAaIC_JCaIAqDGyUGwUCaJAuB?mDAuDA}EAmDA_EAiHCoF?o@A_CCcIAqHAoACiMEyLCaG?_EAqCAwDAwDA_IE{GCkCAaFE}IGwJAaAIyMEaKI_Q?YEcJIeKCsDAe@G_GCaBAoCGwMIyLEmICyDEuKCyEIwICcHGmI?]EoNEcOEiOAyBE}IAgDAqDA}EA}B?]?q@CeLAwAG_Q?q@Am@?mA?MCeFKo^C}ICuCAuHCuJEaPMe]AeEMwb@Ogd@?iA?OCmIAoCAo@EmO?w@?GMa_@AmEMq_@?sBEgLCmLAk@I_YGkUAmCAyBEiPCwDEuRAkA?o@CkLAoCAm@?w@C_GEiGA_GCqHC}EAo@C_HEuJEy[A}AEcJCmF?CAkL?UAwBAaEGcT?iCE_KCoICuHCoF?A?m@?ACsLA}AG{CEyAE_AAUOuC_@cFWiCKy@EYCYSwAOw@Ii@YeBg@iCYyAu@_DYaAWaA_@mAa@mA}AiEIWmAsCOYQa@yBwEYm@}@sBoAiCMWyCoGo@sAoGgNq@wAkB_EWk@mHyOg@eACGe@cA_AsBO[_BgDiCuF{AaDuDeI_@{@}KyUSe@Ue@w@aBUg@wE}JUe@uAyCoEoJuJ{SeEwIqFqLcCkFuPm^cKqTgMiXIOKUIQ_AqBkB_EaEyIwBuEGMm@mAmDuHaI}PSe@oEkJ_BiDeHgO{@iBkB{D}C{GeDcHcDgHw@gB]s@a@{@}F_MwCoGyEaKiByDyAcDc@cAaE_JmEqJGKuBoEi@iAaAuBUe@kB_Ek@iAiA}B{@cBs@oA_@o@u@oAQWe@w@a@o@s@eAmDaF_@g@i@u@yFcImCyDkFoHs@aAcCkDQWOQkCwDmFsHiEeGsAkB_DqEyFaIgCoDs@cAgDyEqBsC_@k@Y_@iBiC{AuBaAsA}CmEsAmBc@o@oEkGGIwAqBc@m@iA_BMQKOoEmGiD}EoBmC{AyB}AyB}BaDmAeB}@oAoAgBo@{@o@_A{A}By@qA]i@i@cAk@aAq@oAuAqCg@cAe@eAq@cBc@cAKWKWKYIWKWKYKWKYIYKWIYKYIUUs@IYK[IYIWIYIYSq@Su@GYI[Sy@Qs@IYGWGWGYGWGYG[GYI[GYE[GYGYG[G[E[EOAKG_@Mq@E]GYE[E[E[G[E[E[E[E]E[C[E[E[E[C[Iw@E]CYIy@Gy@C[C]C[C[G{@Gw@Es@A_@C[A]C]A[C]A[A]A]A[A[A]Cy@Aw@EsCi@wq@G_HEoFAoCCmCCuC?S?W?A?AQ_TMkQUgXEeGAoA?KA{AIkKAo@?o@CyBGuHIcKOsSA}@GaIKqMEaGC}DG}AAo@?O?OEq@Co@GgAQoBKgAG_@QsAE[G[Ko@Ga@GYG]GYOu@G[IYGYIYGYI[IYIWI[IWIYKYIWKYKWIWKWKWKWMYMYWk@MWYm@MWMUYk@MS?AOUACIM[g@c@s@e@m@SYSYQSa@g@]_@QSOQa@a@WW][UUqAqAiBgBc@c@SQQQi@i@i@i@e@e@OMc@c@QOa@a@SQQQQQOOc@c@QQKMOMEEQQMMCCOSQOQQQOQOQOQQe@e@MMQQa@a@MMCCQQa@a@c@a@QQQQs@q@cAcAwAuAQOKMKIEEOOUUSSOOSSc@a@u@u@a@a@QQQOQQQQOOc@c@_@_@mCiCc@c@QQQQOOQQIIGGQOCCMMa@a@a@a@a@a@SQGIIGQQAAMMMMCCc@a@QQQQQQa@a@QQ[[GEQQOOQQQQQO_@_@wAuASSe@e@m@k@[]m@m@OOc@a@c@a@a@a@a@c@[]GEOQWYY_@IIU]CA[e@OUOS]g@]i@]m@KQOY[m@MUYm@Yo@Se@CIYo@ACQg@AEKWUo@Us@IWI[IWI[GQSy@I[G[EQIa@Ka@GYEYY}AOcAKy@E[E[Iu@?AC]Gq@Ea@C_@Eu@CYA]C_@A]AYA]A[A[A]?]Aw@?}@AuA?w@?{@A]?wA?iAAc@?w@?c@AoDAiF?w@?y@AwA?w@A{@?{@A{AAcF?[AcAAoC?oCA_A?i@?]AwA?wA?[AgA?_CAyA?YA[G}DG_CIoCIgCUeHK}DAw@EoB?}@Ac@?iACyC?q@A_@CaDCaDC{CCsEEkHIiLCoEA_@AcC?gAA_@AeCAmCCyBEeHC_DA_CAuACyA?y@EuAIoCIuAA[G{@Gy@Eu@KqAI{@McAQ_BQwAKy@Kq@My@Mu@O{@Kk@S_ACQGYe@sBWcAYkA]iAI]Og@Oa@Sm@i@_BM]GM?AGQ_A_CKSYu@w@cBu@yAs@wAu@kA]m@i@y@GMOUQWaAqAW]W]CECCCCMQA?EGQUIKYa@mA_B_CyCgAwAY_@q@{@o@y@cC_D]c@GGq@}@}AqB}@iA_@g@A?m@w@KOSWAAEEIMm@u@W]k@s@oAaBiNmQY_@u@_AY_@qAaBgGaIk@s@oBgCqAcBa@i@oAgBi@y@MUm@}@KQQW]k@KSOUMSCCCCCEAC[k@QYe@_A[m@KSCEKWi@eAUg@[s@Ym@_@w@EOYo@e@iAc@eAWq@Uo@M[Uo@Us@Uq@CGSo@Sm@Sq@So@CIQi@G[K[c@_Bm@eCk@eCQs@Os@Ou@Ow@Mo@AEOu@Mu@Mw@Ms@Mw@Im@Gk@Ii@?EAGKw@Io@CSAEGg@OsAGo@KcAGk@Eg@Iy@Gw@Gy@KuAMqBCg@Em@?KEm@?GCo@A[Ce@Cs@EsAA]?E?WCy@CwAA{@CcEE}BC_EAo@IqIE}D?o@C_B?o@CoCEqDCoEEoFAIGgHAwCIqFEqCCgBEwGCiBEsDK_NAqBC}B?o@AaAAo@AmA?]EaD?UMcMAiAEeGA{@Ay@?]A]A]Cw@Cy@QwBGk@E_@Mo@Mq@]_BScAScAKs@G]Ky@E[C[G{@CYA[Cy@A{@?[?[?]@[?_@@]@YB]Bc@@UBYD]D]BS?EF[Ly@\\kBZoB\\oBZgBXgBz@{E@EJm@j@gD@IDWD[D]D[BQ@GB_@@E@Q@Y@G@[B]@W?W@e@@[?W?W?SA[A[Ao@AMAMAM?ICYGs@Gu@Gu@Ec@Em@UiDM}AEm@SmC[uEIoAAI?AIsAC[SmCUgDIqAKqAGcAC[M_BWgDa@kFSmCEu@QaCYwDIuAAOAOIgA?QE}@Ca@C}@A[A[Aa@A[?]Ay@Aa@AyBAo@AmCEeFAuA?a@?MC}CCoC?u@AuAAuA?{@A_@?Y@_@?]?]?]@Y?]@Y@u@Bw@@c@@]BcAH_BFgAFgANsCJcBF}ABs@BqAB}@@aA?K@}@@}A?qACqCGiJ?C?o@KaQE_HGeH?}@AuAEuGKgPAsCMeTE{GCaCEuGCiFAi@?EKqRAo@G_KOsXAo@?uAEiEAiCOuUAoCAo@CoFA}AGyIGmLMiTGoLCoFA_BAiCC_AAq@AWE}@E{@AYKuAC[Iy@Gu@Ea@CWA?Ky@U}AIk@G[QcAKi@I]EWGSI_@Qu@Uy@[eAIYOe@[}@?AKYKUM]Si@MYKWg@eAKWMU[m@MU[m@i@{@OQW]IMgA{AGI_AoAOQa@c@a@c@[[SQg@e@eA{@w@i@s@g@qAy@MGMISKICOIKGYMA?ECe@Qe@QQGkBo@YKQEmAYc@I_@I_@I_Do@qBa@i@KQEC?i@My@Os@Qe@Iy@Mg@Ko@OiAYqBw@e@S_@Q}Aw@m@]c@Wo@c@_Aq@y@o@g@a@cA}@WUKKa@a@oAuAg@k@a@g@iA}Ae@o@CEQ[q@eAWe@o@iAu@yAi@mA{@sBKY]aAGO[_A_@mAIYQi@CK[mAOq@IYIa@EQ[}ASgAMu@Im@U}AUaBwAwJE]s@{Eu@oFQiAYqB]cC_CkPUaB"
                            },
                            "start_location": {
                                "lat": 41.4402098,
                                "lng": -90.32875349999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "11.7 mi",
                                "value": 18809
                            },
                            "duration": {
                                "text": "11 mins",
                                "value": 639
                            },
                            "end_location": {
                                "lat": 41.5622359,
                                "lng": -87.75107589999999
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "iqo|F|k|wOyBwO[uBi@wD{ByOEY[}BU{A}CmTIo@M{@[uB_CmPsBwNo@}EqAaJ_B}KIm@QiAgBkMy@wFa@yCOcAScByCySi@qDm@gEIm@iBmMQsASsAcAgHcCcQWeBSkASkAa@uB]}Au@}CQk@Uw@_@oAk@iBYw@Ws@yD{JyAyD[w@g@sAOc@s@kBo@aBmAaD{@}BoAeEi@}Bi@mC_@cCYqBS_CKuAIgAGkAEy@Cy@?SA_@?OAo@A}@IwRCcHAmCKs]Qme@CiEA{D?uAAg@?C?u@G_KEePIiRAiBG_QEgOGyM?o@E{IAiD?y@KqWA_CIoSCkF?iBAu@Ow`@AsMIgJ?{C?_@GmPEeLCoFAuE?ECoCA_BG{M?o@Ao@?AAgC?_B?o@AiA@gDB_BDmCBm@HwBD_AFu@F}@HiANoB@CNyADe@Fi@PmAD]NgAN_A?ALw@Ha@BSF[Li@Jm@DWXsAReA^mBn@gDP{@RaAHi@Lw@F_@Hi@Jy@Hs@Hu@Di@Dc@JkAD}@Be@Bo@D{@BkABoA?g@?o@?E?wBA}BKs]EqHAo@?gACqE?w@AmAGiPE_HCyDKg\\?o@C_KAuAEyM?o@CiGA{DAiD@eC?e@Ag@?c@E_DGoO?o@C_HGkNCgIC_E?cBIcGC{AA[E{@K}ACc@Co@Ce@OcBOiBIy@Iu@IaAAIKk@Io@Kq@Gi@QcAQiAG_@Ic@YuAWmAQy@Qs@IYEQQs@Ka@Uw@g@_B[eAAA]gAyCsIM_@Qg@GQy@aCaBwEiAgDSm@Si@Qi@q@mBaB{E_AmCIUIUGQ]aAg@{AYu@g@}Aq@kBw@}BeDoJUo@Ww@}ByG_@cAu@{Bk@}Am@gBSk@qA{DqAuD?As@uBy@}B"
                            },
                            "start_location": {
                                "lat": 41.53636789999999,
                                "lng": -87.96879269999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.3 mi",
                                "value": 484
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 17
                            },
                            "end_location": {
                                "lat": 41.5639862,
                                "lng": -87.74575849999999
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "_st|Ff{qvO]iAe@_Bc@{A_@}A[uAUgAYuA_@mBe@eC]kBCMa@aB"
                            },
                            "start_location": {
                                "lat": 41.5622359,
                                "lng": -87.75107589999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "3.5 mi",
                                "value": 5557
                            },
                            "duration": {
                                "text": "3 mins",
                                "value": 191
                            },
                            "end_location": {
                                "lat": 41.5828011,
                                "lng": -87.6860193
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "}}t|F~ypvOUsAMs@O}@Q}@Q{@AGq@}BK[K]M[Ui@IS_@y@KUGKMUEGMUUa@{@qAEGwAuB}@sAuAaCYi@IOMUy@eB[s@CEa@aAWm@IUc@gAu@sBOc@Us@CG[_AUm@o@mBe@uAkCmHM_@K[[{@mBwFQi@uA_EWq@EIIWQe@Sk@Qi@i@_B_@eASm@Oc@Sg@}BcHa@kACEQg@a@gAqBaGQg@cB{EgAaD_@gACI_@iAw@yBe@sAgAcDSi@yAkEeB}Ea@mAWu@GQMc@CESm@e@sAa@mA_@aAEMkAkDc@kAc@qAaCaHQg@_AoC[_Au@{BUq@Ma@c@uAa@}AOk@EK_BeH?A[cB_@}BAGOeAWiBOkAc@}EImACa@KgBGyAGoA?YCo@?AAo@CsAAu@?g@AeBAwC?sE?o@?aK?kC?K?O?wAAo@?eD?}A?eA?Q?qA?cA?i@As@?s@?iA?}@C_B?}A?IAkB@mA?GDeBHuBPkC"
                            },
                            "start_location": {
                                "lat": 41.5639862,
                                "lng": -87.74575849999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "427 ft",
                                "value": 130
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 5
                            },
                            "end_location": {
                                "lat": 41.58255860000001,
                                "lng": -87.6844962
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b>, follow signs for <b>I-294</b>/<wbr/><b>Indiana</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "osx|FrdevOn@oH"
                            },
                            "start_location": {
                                "lat": 41.5828011,
                                "lng": -87.6860193
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "23.6 mi",
                                "value": 38023
                            },
                            "duration": {
                                "text": "22 mins",
                                "value": 1331
                            },
                            "end_location": {
                                "lat": 41.5846019,
                                "lng": -87.23498309999999
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div><div style=\"font-size:0.9em\">Entering Indiana</div>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "_rx|Fb{dvOJ}@L}@F[Fc@Fa@Hc@N{@Je@Jc@@EF_@DKDQF]Lc@Ha@J_@DMDOJ[FUJ_@Pg@La@Pc@HUL]N]N_@FQFKL[?ARc@@CJWN[Ra@NYN[R]LY@AP[BGLUJSFOLSZm@h@mA`@aARg@Rk@To@Tw@Ne@f@oBJa@H_@P_AJo@N}@BQHm@D[NyAFo@Fw@Bm@F_A@o@@O@O@qA@{A?iA?cD?mFCiD?WA_D?yAAkA?GAGCECCKI?Q?kA@uD?u@?qF?WAkC?_B?_B?u@?]?i@?g@?y@?{@@qFAO?o@?o@?O?uB?{FC_H?eEAwDAaH?wICeHAwG?iAAiA?_EAyEA_I?oJAcH?wBAcCAyC?}AAiA?cAAs@A}@A_@Ca@?UCk@Cg@Ai@C[AWGgAAKAOCWEo@KgAEe@I{@Go@KeAy@eIEe@MoAIw@OeBI}@Es@Eg@Aa@Eu@Cq@C}@Aa@Ao@AO?Q?_@Ac@?y@Aa@?qA?eC?iA?oB?_@@_E?o@?GAyGCsGBkH@oU?u@?qF@iE?mQ@cF?A?aA?aB?u@@eA@m@DoDBm@@]@[Ba@@g@Be@Bg@Dk@@[HeAFu@NwBv@wKTqC@MNqBHeAHgAJqATmCH{APkBDs@Ba@Dc@Dg@B]Be@De@B_@HaAFy@?KDi@Ba@DeAB_@FsADyBBgA?W@i@?}@@g@?wA?y@?cBAkB?_E?I?e@?yA?eE?o@?eB?{H?q@A{A?iA?A?E?o@?W?M?aA@OAI@U?g@AoA?uO?iM?c@?cCAyMAoF?cG?uA?W?cLAwK@sF?mC?{ABg@CkG?sECoG?A?A?E?A?G?i@?C?Q?A?A?u@?sF@qL?aGAwKAgH?i@?A?cC?{@?y@?u@DmD?o@?q@AiI?qHAaD?oC?aH?mCAgC?aAAcA?oF?o@?o@?_K?o@?iD?gH?yB?qA?o@@m@FqD@cABeABi@?CJgBJgBFy@FgAJoAHs@Di@Fi@Hu@RcBL}@Hk@\\yBN{@f@uCz@{EP_AP_AfAkG\\gBRiAr@{Dv@mEN{@Fa@F_@Hm@F_@BYZcCNsANcBNaCLiBDq@Bk@@S@[B_@@OBo@DsADmB@m@@uA?u@?eA?cB?S?sAAqBA_C?s@AqB?MAiE?eACiP?OAyEC}ICyHAcE?oAAiFAwCAyA?cBA{BAaF?e@AsE@_G?KC_E?W@e@AsD?gJ?G?sA?uA?uL@sB@sB?aB@cA?aA?g@@e@?U?i@?y@@yI?o@?oC?_B@}D@mK@uF?_EBqR?uF?uB@sB@_D@oL?m@?A?eC?I@aE?}A?mD@oI@wIB_\\@{EBsBDqBB{@JwBHiBJwAJ}APkBPgBReBJ_ARwAXgBF]N}@Jm@Lm@XqAVqAXgA?CLg@DQf@gB`AsDh@kBd@kBPu@ZoAJe@\\eBJk@Ha@F_@Lu@Ny@Fa@Jq@D[BOFi@ToBTsBHu@L_BFs@NcCDw@@MBg@?E@_@BY?QBy@DwABuABaB?y@@oA?{A?oF?E?iF@wK?oF?_E?w@?gC@aK?oF?}E?aH@_I?cD?qJ@yC@cFBeH@oL?o@@o@?gB@iN?oA?[?_V@qB?gJBqM?[?qA?q@B_TBwUBiM?_BDuR?kIDcY?mDB{P@qB?o@?oF@aK?_K@_B?A?wBDmHBwCDwABs@DuADeA?KBc@@[@SBa@Bu@FaAFmABi@LiBXiEToCRuBB[Da@LuAVmC\\gDTiCVgC@S\\yDPoBHgAHoAPqCFgAHcBJeC@WDeADgADyADkBDsB@kAB_B@iD@uF?iCDqa@?o@BuQ@{O@mGB_K@qI@oJBqR@_I@yH?gF?gB?QA{@AuAAkBEgBCiBC}@C}@Cc@A]Cs@O_E?KKoBCe@KqBGy@IcAIaAO{BGg@]}DYoCK{@SkBq@iG_@oDIm@WcCk@qFkAkKEWCUm@iFmAcL_BaOgAaKWaCMcAK}@[qCuAiMm@sF[qCSiBSiBSoBUqBE]E_@Gi@Gi@?AKy@CWE[KeAYqCGq@Io@Iq@C[OwAQwAi@aF[sCCYUoBUyB]kD[qCCSq@_Gy@mHu@aHc@wDYcCg@uDYuBS{Ak@aEq@qEa@iCIm@Ia@YcBc@mCmAwGa@wB]cBq@cDiDwPcHc]c@}B[sA_@mBa@uB{EiUqAwGaAsE_AmEAEGW?AY_Bi@gCYuAs@oD_BuHk@kCa@cB"
                            },
                            "start_location": {
                                "lat": 41.58255860000001,
                                "lng": -87.6844962
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "278 mi",
                                "value": 447806
                            },
                            "duration": {
                                "text": "4 hours 9 mins",
                                "value": 14961
                            },
                            "end_location": {
                                "lat": 41.386756,
                                "lng": -82.1785646
                            },
                            "html_instructions": "Take exit <b>16</b> to merge onto <b>I-80 E</b>/<wbr/><b>I-90 E</b><div style=\"font-size:0.9em\">Toll road</div><div style=\"font-size:0.9em\">Entering Ohio</div>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "w~x|FramsOGeAMk@i@_C[uAOk@Ms@u@aC_@iAOg@Qe@Uq@Sm@[eAEOCOES?Q?U?QBOBOBKDMFK@ABE@ABEFGFEJIHCHCHAJAJ?J@JBJBHDHFFFDFDDFHBFBHBD@HBH@L@H@J?J?J?HAJAJCJCJCHEJEJEHEFKHMJu@j@_An@}AdAaAn@aAh@SJC@WJSHc@PQDa@HgAXm@LuDfAkAXw@RaCp@{@FQ?OAOEMEMKIGOUACOYMUGOUe@Sa@_@u@ISGQEMCKC]AS?S@SHy@RwA@S?g@l@_Df@wBzD{PNo@ZwALk@TaABIR_Ab@kBPu@l@mCNm@No@t@eDjA_FbAmEJe@t@kDd@oB`@iBRcALo@^oBd@wCRkALgAXqBFi@Hq@XoCBQNcBLaBF{@HmAN}BD}@HeBBi@?CBc@F_BDw@PyDDeADmABa@Bo@H{@Dk@B_@D]Fg@@IPuAPiARaAVaAPm@Po@Vu@BGZu@L]Ra@\\q@`@u@d@u@|@yA|@wAz@qA`@m@n@eAf@y@LSHOJQJS@AVe@\\w@HQDIj@{Ah@eBJa@HYRy@b@eCD[NoADc@De@@GBYHcA@YDq@NiCD}@LuBJkBXkFLcCJiBBm@?AHaBLqCJoCFeBN}EHqCNsHFkC?S?U@]?i@?C@u@H}INsYDaI@yD@oD?q@@o@?o@?_B@qCB}F@iF@_A@eB@yB@kA@gAD}AFgBJ_BHkABc@Fi@B[DYBSJ_ARqA@MJm@BOJi@Hc@Lk@@G?AJa@Nm@\\wA@CNk@^oA@E\\aADM?At@mBl@wAb@_ATe@\\o@d@{@p@gAXa@BEz@mAzAqBdAsAdAsA\\e@@CZa@PQzAqBRYV_@l@{@h@y@JSl@gA\\q@@Eb@aABGd@mAp@sB^qADQZwAH[ZaBTaBHo@LeAB_@JiAJcBBu@@c@BcA@gB@kC?]?wA?yF?gA@sA?{L?oF@_B@o^?aB@oL?cBCeCAqAKeCK}AAGGo@Gm@?AAGQuAIi@?EKk@Kk@Ie@Qy@Om@Qu@GSIWYaA]_Ak@yAc@aAe@cAi@aAq@mAmA}BYi@[k@u@sAa@u@q@oAs@oA]m@{@aBACWe@Uc@S_@AAQ_@CEO_@Ym@EKM[ACEKQc@Uk@[cAQi@AAEKI[AAUy@Qo@Oi@Os@Ka@Mm@Ow@Ie@ESEWCUAACUIg@Ge@Gc@AIGe@?EQyAEk@Es@Ek@C[AUA[GgACy@A_@?e@Ao@Ag@?k@?q@AcA?m@?o@?K?qA?{B?gB?cB?_C?qD?}C?iF?gFA}EAoCAkAAsBAqAAa@AsAAQCmBAsA?EEgBCkAAa@CcAIsDImCCs@Cm@AWGgBA_@A]GqAEkACcAEkAGqBCkAGkBCaAAm@?KAc@C_AAiACaACwBAaACiBCuC?a@Ao@?gBAkA?mA?cA?oB?mA?kA?eA@gA?g@?{@?s@@kA?O?o@?G@kB?sC@wB?gB@oA?kA?]?m@?A?_@?_@@g@?iA@_D?kB?U@kB?I?k@BeB@k@@g@@]@e@@c@DgABe@Bc@Be@HiAB[Dm@JgAHy@@C@OFa@Fg@D[D_@He@Fa@Hi@Hc@F]He@FYHa@Lk@H_@Ha@Nk@Rw@Le@V}@v@uCd@aBt@oCf@iBXcAXeATw@h@oBVaAR}@XkA^aB\\aBReARiAP_ARoATyAXuBZcCLkAJcAHy@Fq@PqBVuDZqEPcCXaELmBf@gHNyB?Il@sI^oFH{@VsDDc@@KBa@PmCL_BDm@Do@@Kd@_HRqCJy@FyAVyDJ{AL_CReDPmDFuAHuBHsBNoDN_FBoAL}EDeB?KBsA?[DkCD}C@oA@yBDyGB{G@sC?o@@iCFoK?q@HkS@qB?{B?QHcPBaH@aB@sEBqG@i@?o@B{D@cBHaHDmC?[BcADgCBkADkAD_BB}@LqDFgBDeAHoBBo@Bg@?EX}GJyBFsB@KLcDJyBDqA?A@k@@ID}ALaHDeGAkB?o@?G?cA?w@AI?o@?I?OCoBAoAA{@GwB?CG_CG_BCeACa@G{ACc@Ey@GmAIsAMsBOyBIw@AUCYI{@QmB[}CEa@OoAYiCWoBq@oFIk@E_@COGm@CIi@qEUgBIm@K{@UmBM}@AIk@mEAMIo@Im@a@iDUgBS_BWsBqAiKEYCSe@wDg@sDKs@AIGc@G]AOOeAe@}CIi@ACKm@a@gCCUQeAKm@CMG]SiAKo@a@yBWuAgAwFe@_Cm@sCiAkFk@eCCKo@qCI[EOg@sBm@cCEKI_@EK[oAa@{AACYeAc@_B?AQi@Qq@IWuAsECKeB}FqDsLeAiDkBkGGSaAeDe@aBY_Aa@}AMe@_@yA]wAQq@AIKc@a@gBYsAMm@Ia@WuA]iBSaAOaAQcAQgAEWIm@Km@OaAKs@E]Im@UiBOiAIo@OoAWoCKgAEa@IaAKqAIiAk@kHEg@McBI_A?CImAOqBCg@iAkOu@{J[eEIiAUuCG_AKkASsCGq@IiAWgDSmCKqAUeD[eEi@eHc@_GSmCOmBc@eGSoCGs@I}@UoCOmBCWGq@UmC?AGo@Gk@Gm@WwCGg@Q{Ae@cFGm@i@aGYsCGq@{@aJC]E[a@yEO_Be@eFO}Ac@wEk@yFWaC[iDAO[{CWwCqAiNWgCS{BU_CQoBU{BWqCU}BMwAIy@MsAGm@C[KaAI{@MoAEi@UwBCYGo@Gm@?CQkBO_BCYGo@CSCYO_BO{ACWSwBU{BMwAQoBY{COqAK_AMaAU_BKk@Ic@Gc@Ke@ScAAEMk@AG]sAU_AY_AW}@Yy@Y{@a@gA]{@g@kAe@aAe@_AUc@GMc@s@CGWc@GIU_@OWAAYa@W_@AA_@i@UYUYY]CE[]EEUWUUEGKKUUSUQQ_@]}BuBs@q@s@q@mAgAcB{AUSaA}@iAcAQO}AwA[YYYWUw@u@c@e@y@_Ac@g@[_@SYe@k@e@o@W_@CEOSc@o@Wa@KO[g@U_@Yg@IMa@w@o@mAIMSe@Sa@i@kAi@oA_@_Ai@sAGQ]aAe@yA[cAUu@U_ASs@U}@q@}Cc@qBwA_HUgAMm@u@qDS}@w@yD_AoE_BuHqCyMUgAcA_Fw@qDeAeFeC{Le@sBc@sBiAuF}@cEkAyFs@iDuAwGKe@Mm@oDaQeAaFaAuEm@yC{D_RKk@uB{JiByIuBaKMm@u@qDi@iCYsAESi@iCaCcLmA}FOy@m@sCWiAMk@Ok@YkAUaA[iAQm@]mA]gAe@}A{@aCOe@ACSg@Um@y@qBAGQ_@Sg@IQ_@{@Ue@IQKSy@cBc@w@[o@k@aAq@mAi@y@o@cAYc@}@qAqAkBmA{Ak@s@w@}@KMsAyAuAyAa@c@}@_ACCy@}@{@}@s@w@q@w@EEY]A?i@o@QUwAaBk@q@]c@_AiAcAqAOQOSk@u@]c@OQ_@g@cAuA]e@UYmAcBiAaBW]iAcBy@mAm@_Ac@o@_@m@a@o@m@_AsAwBeDwFiBaDWc@wBwDs@kA{AmCeAgBuBiDcA{AiBkCcAsA_BqBw@cA_AkAeAqA_@a@{@aAoAsA_B_BqGsGeAgAmBmBOQKK}A{AaAcAk@k@w@w@y@y@i@i@Y[c@e@YYg@k@w@{@[_@QSGIMM}@eAy@eAW]w@cAY_@i@s@_@i@SYu@gAWa@W_@c@q@S[u@kAAA]k@e@w@_@o@[g@qAaC?AWc@IOcAoBQ_@a@y@o@sAgA_CuA_DO]Um@[w@Yo@Uo@Wq@g@uAEKK]Qe@i@_Bo@oBa@oAc@{AQi@AIk@oB_@uAq@mCMg@Mk@CKI_@Sw@WiAa@qBk@sCe@iCg@mCo@cDk@cDGYWwAUiA]gBQcAY{A[eB[_BAEIe@{@qEWuASiAIa@Kk@YuASiAQ_AACKg@Kk@CISaA]aBs@gDScAYmAIc@CEMk@u@cD_AyDWeA?AOi@e@qBy@{C{AmFQm@aAgDs@eC_BaF_AyCqA{DEKe@yAq@wB}@kCu@_CuBqGm@gBqC{ICKQi@EOa@uAm@qBMg@[iAs@mCOk@K_@aB{GU_A]{Ai@iCUcAS_A_@mB]cBQcAa@wBc@cCWaBUsAYeBEYIm@G]EYQiAUcBCME_@UgBOkAAEE[MeAMeAK_A]aDW}BMwAC[MoAKmAUmCSkCIiAEs@KaBSaDEs@GkACi@E_AGuAOcD?KEiA?ACw@GuBEgAAe@CsAAWCy@Aa@CiACoBAgAC}A?GAuBCeD?iE?{B@oD@gA@k@?C@e@ByCD_D@a@@o@@a@DiB\\uNPeHPyHDsBDaBHaDRyI@e@Bs@@g@@Q@q@B{ADgBFqBDcC@y@BaB?_A?a@Ae@Ag@Ac@Ak@Cg@Ca@G_AEi@Ea@Ea@E_@Ig@Ge@Ig@G_@I_@Ou@Oq@Ka@]kAY}@KUa@gAISUe@GOQ]S_@Ua@Q[MSQWS[W]OUa@c@]a@o@q@uBoB_Ay@}@s@_@]SQMMYUm@i@WU_@]s@m@QQc@_@OOKKOM[[w@y@_AcAm@s@}@gA{@kA{@mAU]o@aAw@qAs@qAYi@EIGMKSACYi@Wi@Se@[q@Ug@O_@O]Yq@Oa@ACACAGEIEOWw@M_@M[Me@Ma@M_@[eAe@eBw@mCs@gCgFcRoC}Jg@gBAC_@oAy@qCAEg@{Ay@cC{@yBw@qBg@iAQa@Sc@Q_@Wi@a@{@g@cAKOUc@e@}@a@u@QUs@mAs@kAo@aAw@gAs@cAw@eAIK}AmBoA_B_@e@KOSWQUc@k@]a@_AgAgAuA]c@gAsAqA}AqAcBeBwB}AqBm@y@Y_@q@_AeBgCkBuCi@}@sA{Bo@iA]m@MU[k@eAsB_@u@o@qAO[O[u@aBoAsC_@{@{@sBa@}@kAsCcA}B?CoAmCCIw@aB_@u@MYSe@m@kAEGg@}@w@yAMSw@uAS]u@oASYa@q@S[u@kAy@kAy@mAUYGIMSqAeB_AkAsEeGyCyDuBwCQQq@w@q@{@EI]e@u@_A]c@}AsBw@cAGIyBwCu@_AY_@U[oBeCeAwAsAcBEEY]y@cAaBoB{AcBi@o@MMo@w@}@aA]]{@_As@u@qBuBy@y@YYmHqHoAqAEE[[UWk@k@oAoAw@w@[]KKOOoCqC[[]]oAqA_AaAc@e@UYMOOSg@o@OQ_@k@c@m@s@mAc@y@Ye@Wi@q@yA]y@[w@Oc@M[_@gAY_AWaAc@cBUeAI_@I_@[cBUaBQmAEe@Io@Iy@IeAIkAE_AEo@EmAAs@Ai@Ag@C}B?cBAqA?sAEmH?KAsDEqI?}@AsBAiB?C?kBAmBAW?mAAyB?g@?c@AA?c@?sAAkA?_@Ae@?IA_EA_B?c@C}F?_BAo@?o@CoGAkB?EAuCAmBA{@Ae@CkAE}ACaAEw@IgBIwAKiBIaAG}@QoBMkAQ}AOiAUgBIi@SoAEW[eBY_Bc@sB[}Aq@sCsAuE?Cg@{Ae@yAw@{BIWmBwFM_@qB_Gu@cCYaAa@yAYaA]wAo@mCMi@Ie@I_@AAUoAMo@AEYaB[kBO}@Iq@EYUgBWmBKeACOGw@MkAUwCq@_I[}CGi@E]Q}AKw@MaAOaAQkA_@_CY{ASaAMs@Kc@YuAg@qBS{@WeAMa@Kc@CEU{@Ma@o@wBCGe@uASm@k@_BWu@eA{Cw@_Ck@_BY}@s@sBy@_Cm@iBq@kBgAgDa@sAM]sAqE]sA]qA[mA_@}AWeAWiAc@oB{@gEQ{@Y{A]qB[mB?AWaBWgBUcBWqBOmAGg@Gi@Gm@[{CUeCEg@Q}BIaAIgAC_@SiDU{EM_DCoAK_EEkCCcBAw@?SAkDAeAAgF?GAaGAcB?mACoGC_JA_@?O?iAAkAAoAGmC?UIcCKqCA_@KcBGqAGw@Cg@Gy@OeBOiBSqBI{@Ii@E]Gi@UmBMcAQgAQoASqA[gBOw@Mo@_@mBMo@Oo@Qy@Oq@qAeGSy@WmAMi@SaAg@}Bs@aDCK}@cEa@mBOs@I]_@aBg@}Bg@{B_AgEc@sBESaAmEu@gD}@iEw@mDm@qC{@yD[wAgDoOcA{Ew@gD}@eE_AkEs@aDWiAeA}EMm@EQs@eDyA{GoBaJ{BgKg@aCSaAIe@Ic@G[?CQcAM_AIi@Ee@OiAKiAKoAGs@Ek@Cc@C]Ci@Ag@Cc@Ae@CcAC}@Ay@A{@?cA?{@@{@BuADmBFcBFoADo@Bc@Di@Dc@De@B_@BUFi@Hs@Fi@NeAHo@RmALu@Jk@TkANq@R}@\\qARw@Ni@X_ARm@Pk@Ri@Nc@FO?AJS`@eA`@_ATi@JSFOJQf@eAl@iA`AgBj@gAbAoB`@u@h@_AZo@b@{@`@{@Rc@Rc@Pa@b@iAZ{@\\_Aj@gB`@uA@E\\mANq@Ps@Ns@XwARcAV{AHi@Hq@Hm@Fe@D]D_@D_@Dg@DYBc@Fs@F}@Dm@FeADgADmA@u@@M@a@@e@?e@@{@?sA?U?oD?gF?iA?o@?iA?mA?cA@cA?e@?AAg@?kI?yA?u@@cF?}@?o@?o@?oC?o@?q@?s^?wQ@iA?]?Q@cABgABgA@k@@a@@G@Y?M@U@M@S?OBY@]Bc@BY@SFw@Dk@B]Dg@De@D_@@SJ}@@MBUD]PuA@EFm@Jo@N_APcAF_@F_@BMFYDYH]Ji@FWR}@DODULc@DQDOR{@Le@XaAPi@Rq@J]Rm@HSJ_@HSRg@Nc@L[N_@FOPc@N]Re@N[FMZq@@AP_@@CFMLUP]NY^q@Tc@PWJQFMNUBER[NYv@qA`@o@d@w@f@w@\\k@Va@^m@d@u@HMVc@DGPYf@y@HOh@{@d@w@h@{@PW`@q@RYP[P[RYLUR[HMHM|@yAzBqDNWFK\\k@p@gAPWDIJODIXc@BGR[PYT_@PYT]NWNWPYf@y@T]PYPYP[RYNYRYPYR[Xe@|@{Ab@s@T_@Ve@f@_AR[Vg@h@gAVe@Te@v@aB^{@LYN_@Zu@Zu@JWf@qAXu@Ri@L_@Pc@Ts@Vw@j@eBNg@Tw@Ne@v@qCFU^{APs@@INk@DSv@oDDYZ_B\\iBBQVuAJo@b@yCFe@`@}CNmAT_CLuAVaDJsAJ}ALsBJ{B@YDmABm@@k@B_ADuA?U@UBeC@w@?_@@sA?sA@eB?cA?[?oA@iABiJ?kB?g@BeH?a@?M?a@@{A?gA?aA@kA?oA@aG@cA?mA?q@?aB@S?oB?c@@qB?cA@uC?oD@wD?gB?s@@_JCoU?a@A_`@Ay@?cG?sB?a@As@?K?E?sB?eC?o@A{B?mB?{G?gF?{BAgC?kEAuEAcL?aB?{FAa@?M?aB?iA?[?{B?_AA{G?uC?m@?kB?[?yC?aBA{GA}I?wA?oF?kB?wA?wA@mA@gADqBDkAHiBH{AHwANeB?ANcBN{AFk@RyALeAPcA?GZgBZcBTeATgATeAZqAJ]Le@XcATu@ZcAZ_ATo@L]l@_Bf@oA^}@Zq@DKh@eAN[dAsBj@iAVg@j@gAf@aALUd@_AFKVg@NYv@{A\\u@n@qAZq@Vo@\\y@^cA\\_ATs@\\gA`@uAJa@Ja@T_APs@R_Ab@_CXmB^cCLgAJiALkA@QDg@?EHgAFeAFuABy@Be@@y@@S@{A@w@?oB?wBAmECcD?K?kCA_ECyD?gBA}DAwDA{DCyGAmEAaB?WAwE?o@AyB?UAcEAcDAiDAsCAsCA_C?oCCkIAkC?_A?o@?WAwB?o@?UAkBAuDAiJEwF?kCAiC?aCAkC?aDAmA?U?KAuB?{@Ak@?Y?yBAeC?g@?]A_A?kC@{@BoABs@DaADm@Bi@H{@Hq@Ju@He@@CD]Je@Ns@No@Ru@Lc@`@iAb@iAVk@JS`@y@Tc@hAsBR]z@}AjHkMfBaD^o@l@qAPa@Pc@Nc@L_@@A\\eAPm@Li@R_AR_AJs@Jq@Fe@Fk@Fs@BWDa@Bq@@OB_@?CDmAB_A@qA@s@BgBBoCDoC@o@?GBiCDcD@iABaBD_E?o@BiADoDHeH?a@@o@ZsXBkCBcB?C@{ALaK@o@LwMDgDBqBDeD@{B?IBsE?Q?cHA}A?e@Wop@AOA_EAeFC{FCqIAwB?EA_CA_FA}AEiNAwAA_EGqO?u@?YAq@IaTA_E?o@CmGEgICoG?{@?o@AeDAmBCmBKwDMgDIkBOyBKyAEm@UmCKaA[wC]mCS}AMy@g@{CCMo@gDWkA_@iBWeAS{@c@cBOi@YeAYaAe@yAe@{ACG?AOa@s@mB]}@a@iA[s@]w@_@}@a@{@Q_@Ym@ACQ]ACc@y@cBgDgDsGgAyB_AgBWi@]q@q@oAUe@uBcEO[We@Ym@o@kAKSc@}@i@eAcDoGq@qA}CeG]s@qB{DO[MUqB{Dg@cAoCmFIOmAaCWe@e@_A?AKOGOCC?C]s@MYu@gBWm@[{@[{@_@eAYy@y@qCEOEMAEOk@e@kBKa@]_BMk@Ou@G_@Ic@GWE[GYGa@G[G_@Gc@Gc@EYE[Gc@Gc@Ea@Iq@Is@I{@IcAKqAAQEu@GcACq@Cm@C]CeAEoA?]CmAAiA?]A{CAoFAg@?c@AcA?}@AuD?i@?Q?K?k@?a@AmC?GE{OAwG?o@AiCAeB?cAAiD?i@A{C?yAC}G?_A?{@A}E?KAeBA{D?u@AqC?[?o@?u@@oB?{B?M@a@@m@?G@w@?[@s@BmA@U@q@BcADyAF}ADkAFwABm@Bg@B]D{@FoABa@LeBFu@JwA@M@QB]R}BB]D_@JqAN}AJiAVwCDk@LwAt@sI`BiRJmADk@HsAHoABa@Ba@De@?EFqAVmFFgBJiD@m@BuA@}@@_ABoBBgD?yK?}J@iP?M?iH?wR?mC?oB?oE?iA?oD?_@@uK?Y?oC?s@?aC@iD?sF?E?W?gA?eGAsG@aB@wK?u@?Y?O?q@?kA?gB?yC?gD?}B?iA?iA?cC?{B?A?iA@kA?}A?uA?mBAmA?_B?[Ag@?AAm@?]Cu@CiACeAAQ?QC_@Cg@Ey@Eu@IcAImASmBEc@KcAMgAMgAKw@Km@?AIg@OaA[kBWcBO_AWiBIe@ScBKaAEi@Gg@?AEm@Gs@Iy@Ck@AMGy@EgACe@Cq@EaAC}@CaA?WAg@Ac@?e@AeA?mA?a@?eA?e@?_B?g@?sB?oA?c@?cB?oA?gB?uB?iA?c@?]?s@?kB?cB?uA@mA?I?C?Q@gA?o@@w@@q@@{@@aA@}@@m@BuABiADyAF_CBuAHoBDiABo@RgFd@gJDq@Di@DeALuBDeAJqBDsA@UBu@BcAB{@B_ADyA@{@@u@DkF?W?G@yA?]?i@?cAA_A?eA?y@?aAAm@?_A?aA?i@AiA?u@?e@?i@E_LAwC?gBAiBAyC?u@AoB?W?[?eB?uA?wB?u@@Q?]?g@@{A@aA@{B@e@BuB@w@@}@DiDBsAJwE?ILcFXuJPyFDyA?EBo@@o@DsAJaEDcBDaCBeBDcB?UDiCDmD@u@@E@y@BwBBaB?UDsBB{BDwFBsCFcF?KB_B?KFqFDsDJoHFaJ@k@HuF?W@}@?_@@oABiD@yE?c@@aE@{D?[?Q?_FAe@?{B?SAyKAeNAaP?_C?[@yE@_E@}CB_C?k@FiEDcEBuABeB@i@@o@HkFFuC@o@LoIBaB?]D}B?Q@_B@_@@iA@cADwBDcCBsB@{@@k@?I@{@BoA?C@eADgCD}BBaCLcI?a@H_FBoBFyDHgFRqN@o@B}ADgELcHBcB\\wVNsKJaGDqCHkGRwNJqIDkE@eBD}J?_F?eA?{B?eDAuCG_MCwCAo@C_B?a@AMEiDGcEEqBEqBIoDGwCIwCUwHCo@GgBAg@Co@M_ECo@WoIWeHYkJo@}RIyCQcJEaAS{KGyEGgIAyDCsAEaJI}LEmIAcBCoCAqBCmC?OCeGC{EI}MQsXAq@?ICsFKuOCiGIcMGgLCaCCsBEeB?QCw@GiACk@I{AImAIiAO_BOwAGm@Gk@CUKy@M}@a@iCO_AYaBACKm@Km@eAuGKg@{@gFMy@WyAWcBc@iC]uBeAmGk@qDUqA_@_Ca@cCq@_Em@sDaAeGSsAGc@OeAKu@E[CYE_@Gg@Gs@UaCSqCIcBEs@EeACw@CwAA_@Ae@AmBAaA?q@@uA@aAByBHyCJaCN_CPcC\\{DH}@RwBHeA\\{Dn@uH?Ar@iIVcDXaD\\}D@SJiAN_BHmAH{AFcAB{@Dy@@Y@m@DmA@_ABuB?gA?eAAqBAiAEgBGcEUeLMmGGqDG}CG_DO}HOeIUuMKaFCmAAo@IuDA{@AQ?]As@Ag@?C?U?aABmA?E@i@Bo@Do@Bc@Dg@Fm@Fk@Hk@L}@BOJk@R_A\\uA`@qAJ]Ri@JYN]JWBERe@Xk@v@wAv@sAl@gAHM|@aBVa@Tc@v@sAtAeCr@mA@ClAsBvAkCd@}@t@cBPa@Tm@b@kAZgARu@Lc@Pu@Ny@P}@N_A@GL}@LeA?AFk@BWLqAFmADgABw@@_A@i@?wA?i@EyBCk@Es@IyAGs@Ga@Gm@CQMeAOgAiAwGa@wBq@wDg@qC_@{Bk@_DcBmJ}CgQ{AkIqB{KeAkF]cBsAqGkAsF}@_E{@qDw@cDoB_Im@aCuAiFWeAa@wA{BcIY_AkA}DU_AGQIYIYGOGWM_@Ma@Wy@Y_AQg@K]Ma@}@oCu@_CiAgDu@yBY}@[_AAAM_@AEK[EMGQM]K[CGSo@Qi@M]KYIWM_@Ma@K]K]M_@K_@Qk@Uy@CIUu@[kAUw@k@kBGYGQaAwDS{@UcAYiAk@_C]{Au@kDESKk@Mm@S_AEYMk@Km@YyAY{Ai@{Cc@mCUuAQgASuAMaAEYGa@COCME_@CQOcAMcAGg@CUQwAMgAMaACUGg@?GGe@Iy@Gk@?AKy@Em@KcAI}@Gq@Gg@Gs@Ee@Em@Gu@Eg@AICa@Eo@AKEi@Gw@GaAG}@GgAEu@Es@IwAQgDC{@Ey@E}@Cq@CcAE_AEgBEgAAc@GwCCw@C}AAq@Aw@AoAAs@As@?q@Ay@?m@AmA?aAAcA?oAAeA?qB?O?eBAaA?g@?G?SGcYAs@?uE?qDAs@?}AA{FAyEAiD?I?}B?KA_BAwFAc@?kA?}C?qEC{FA_CAiAAuAAq@?G?o@Aq@Ao@Ao@Cm@AkAEsAC{@CiACiAGkBQyEEeAEs@K_CKkBKkBK{A]kFG}@KmAIgAIaAOgBGk@Ee@K}@SsBKcAKcAa@oDMeAMgAOcAUiBSsAK}@Kq@M}@Ms@Io@I_@e@uCKu@G_@]kBUqAIe@Q}@EY]aBgAoF]_BS_AU_Aa@kBa@cBm@cCg@qBiAwEu@wCe@oBa@kB[}AKm@Ke@Ks@QgAQkAS}AOoAKu@MwAGs@Gu@MgBKiBEeAEoAGmBCeBCuB?aA?_@Aq@@{ADeB@{@@e@D_ABs@By@Be@Bg@FeADk@Fq@Bg@Fm@Dc@Dc@Di@BMBWFg@J_ALkAJaAHo@J_AJaAPcBNmAJ_AP{ANyANyA^eDN}APsBNeBJeANiBLmBH_ANuBFmAJ}AH{AH{AJ}BF_AHoBDkA@SDmABcAB{@Bw@BgABcABgABs@?IBoA@u@@}@@e@@s@@uA?w@@yA@qB?sA?m@?C?wB?qB?aAAcAAs@?mAAcACkAAyACwAAc@C}@As@C}@EmBG_CIeDGoBCwACo@GsBGaCGiCGqCG}AAq@ASKyDMcGAa@GkBIqCAs@Cm@CqACk@?AAa@?QAQCkAIeDG}BGkBEmBAIEaBCaAQ}GKqECo@EuBGkBGqCOkFI_DCiAIeDCo@?YIyCEcBEyAKkDCqAEmBGkBGkCC}@GkBO{F?A?A]aOWmJCqAEmBC{A?a@?g@?qB?cABmA@wAFmBDgABw@Bg@Bc@FeAHeADk@Ba@Fm@PkBHu@Hk@D_@Fe@D[Fa@Fc@D]Lw@Ls@Fa@Ha@Lq@XuAFWP}@`@eBzAgHv@oD|AeHf@}BbB_ILk@dBiITiAX}Ad@_Cd@mCJk@h@_DZkBt@qEl@aEJq@@EHm@r@aFTiBXuBXaCh@uERiBDa@VcC^uDl@cHJgA^wELkBNqBLgB@WDm@PoCXmFPwDJyBH}BF{ADgANcEDqBF}B@o@FgCDkBDeDJyIBuD?qC@gD?_@?OAcGCmDCiGEcHCqCCmDCkDE}FCeDCoFAsAEcGCcCA{A?WAsBC{ACsDA}AE_CE{BE_BA_@G{AKoCImBGy@Co@Ce@KyAGgAU{CUsC[eDQeBe@aEGa@[eCy@}FIc@]sBEUi@aDSmAeAiGO}@iAwGEUsImg@m@iDSoAm@kD[gBg@{CCSkAyGUqAKm@c@kCk@aDu@qEYgBIi@Gc@SwAUiBk@uFQuBEg@KeBMeBKaCO}DC_ACmBCoBAaBA}A?wA?m@@_ABgB?EBqBDcCD_CRaNByBBuA@mAH_GBcB@k@?o@@}@ByE@uB?yB?k@?wD?c@?e@AoA?iAAc@?s@CgCEqHA[AuBI_NAc@?MEcGA{BAu@CgF?CEgFAw@A}BCcDAw@CmFC_CAuBCcC?_@AqCCcC?a@Ag@?UIeKUe`@EcFGiJCwDA}@GyJ?[A_BAoAEeGEoFKoOAaBG_K?m@ASAaACkFCkB?c@C}DEcF?[?o@CuD?IAo@AqBC}CAiBA_B?oA?gA@gA@qABeB@e@@g@BsA@[FkBD}@JuBBc@@OLgBHoAPyBLmAPgBTkBR}Ad@iDTwA\\kBpAuGpBmIr@yCh@}BVqAVsA\\iB^wBJu@RmAL}@X}BTqB?AFo@Dc@J}@PsBLeBJaBDm@Bm@N_Dz@qPPgDTuER_ELkCNoCDu@FyALwBFoABe@l@gMZwHTuIRsIHqEDkCDiE@wB?mA@mB@}CAuF?{@CuFEeGK{GIwFIwEIqFM}IAoAEoCAa@CeBU{NIgGAo@GyDCiCA_B?_C?gD@{A@eA@wAJ{FLgET_GLaCF_AJcBDm@HeAFaAH}@LyAZqDJw@b@eEXwBFa@D_@NgARqA@K@O@EBSz@iFDQfCkNpBsKv@iEl@gDTqAToANw@rAmIh@iD`@iCJm@@C@KBIR{ARkALcA@GJq@Z}BFc@@ID]Hm@DWJw@NaANoANkAZaCp@{FTmBNsAV_CXeCLiAH{@Hw@RsBJ{@JkAH_ARqBRwBR_CFw@H}@Di@JqAHaAFy@H}@F_AB]Fw@HmANsBLiBDo@NwBDy@Do@FaALoB@WHsAHgBFgALyBTaFJ{BDeAFiBFmABw@FgBF_BDkAD}A@U@WDcBFcB@i@@e@Bu@?UFuB?ADyBBsAN{I@m@DyDBeD@aA@_A?G@w@?g@@_B?_A@cB?Y?S@gA?iA?k@?y@?e@?e@?]?c@?SAQ?U?UA_@?U?MAQAQAe@A_@CUAWAWCWC]E]C]CUEYE[Gc@Kk@Ga@Ic@Ke@Mi@GUKa@CKGQMc@M]IWQe@O]MYO]Qa@OYS]O[S[S[OUMSMOGIIIGIIMMMKMOQOQQOKKOOSSQO_@]QMa@[w@m@YSsC{BcBqAyDyCcIgGaAs@qB}Am@e@c@[aCkBiA{@iA{@eAy@]YWQSQOMQOUQKKOOo@m@i@k@SSCCIKMOc@k@i@q@Yc@[g@]k@Yg@Wg@Yi@KUWk@Sg@]y@Mc@M][_AUy@Me@WaAQ{@Ke@Ic@Ou@Kq@Ks@Gg@Is@Is@Ee@?IEm@Eq@Ew@Ci@Ci@?[Ag@Ae@Ac@?qAAmB@iC?iBBuj@?_B@cQ?o@Bqb@@kF?wE?_B@{N?gB?{@Ag@AgAAy@CgAC{@Ag@Cy@E{@I_BGaAG}@Gw@KyAI_AGk@MoAMaAIm@Im@OeAWaBWeBcAkGGc@Ku@Kw@Ii@Ec@Ge@CUCQEc@Gk@CUCa@E[Gy@C_@C[Cc@Gq@Ce@Ci@Cg@E_ACc@Aa@Co@Ae@Ag@Ae@Cy@AeAAaA?oA?oA@}A@kCL{P@qAD}F@}ABkD@wB@_B@o@@kBHuJL_R?aAB{B@cA?o@B_DDmFTyZDsHLkQD_FDiI@w@DoF?o@@q@BmDF{LBmG@mD?o@@yC@e@?o@@qF?o@He]@qE@oA?o@@qF@_B?S?kABeH@oE@qCDqRTy|@?o@BsL@uB?cB@uA?cB@{DBcF?}A@qC@qGBqG?}BByF?kC@m@?m@@kCDiO?_A@_C?w@?sCFyP@mHBgJ@iB?oA@sA?yA@{@?}A?uA@g@?m@?i@?g@@_@?q@@]?a@@c@@g@?]@[@W@W@W@[@S@U@U@WBk@B]@_@B[Be@De@Du@PiBHaAFm@Da@Hk@NoALy@^iC\\wB^}BHc@RkAN_APiAF_@XeBTyAHe@`@kCd@uCTwA`@cCBK\\{B@A^aCf@_Dd@yC\\uBLy@TcB\\aCHs@Hk@D_@D[Hs@Fe@Fi@Dc@@CFo@@MLkAHeAFo@De@NiBB[Dg@Dc@F}@RoCB]Do@\\eFL}AJaBb@kGNiB\\}EPkCNoBFy@JuAj@eILoBRkC@WHaAVuDJsAF}@ZsEBYNmBF{@Ba@Ds@BWFy@F_AFy@BUDg@FgAH}@B[@YB[Bg@TkDFgAFaABc@@_@HwABg@Bm@D_AD{@Dy@@Q@_@D}@?ABw@FoAFuBBu@Bm@F}B@o@@SBu@JsEFqB?MFgCJ}D@]@k@Bo@@o@D_BDsAT{I@o@Bq@BkAHoDDeBFmBBaANwG@E@i@?ETaJBmABo@DaCBw@?O@k@@]@a@?g@@m@B_B?i@@gA?cA?E?i@?I?e@?c@?y@?OA_BAm@AeAA{@?o@CeACgAAe@EyAE_BAk@Cc@MyDW_IO}EO{EO{EK{CKcDIiCA]IqCCcAEmBCgACmACaBCwBCiACoDA}@CiD?wAAoB?{@?}@?o@?M?y@?gA?Q?]@cB?u@@{@@kBBmB?q@?E@i@?OD}B@eAFmD?o@@o@@ID_D?G?M@q@DoCBiBDeC@o@BoAD_DByA@gA@m@B_A?Q@w@@e@@m@BaA@a@@c@@QBa@@a@@UBW@OBa@@SBYD_@BW@MJ{@Js@Fc@DSHc@Hc@?CF]Lg@DQDUFU@AH[Ja@Lc@Lc@HWL_@Xw@BCTm@b@cA\\q@b@y@LUXg@~@{AfAgBfAgBlGcKZg@xH_MDGxBqDVa@dC}DrAuB`A_Bj@}@lAqBx@uA`@u@b@{@^y@Tg@x@sBRe@?At@_C^qAPm@h@}BLo@Nu@XaBPiAHq@Jw@NuARmCLoBFkBB_AB{A@mC@oD?m@?u@?M?k@@eA@uD?}A@oFBaM@oC?w@?C?I?o@DyS@uGFu[B}J?E@_F?w@?[?W@_B@}ABiAF}ALkBNyAR{AZeBVcAVeAh@}APe@JW^_Ar@wAx@qAx@mA`AiAn@m@PSlDaDdC}Bp@m@hAcAr@o@TSzAyA@?|BsBt@s@jIuHjF}EtBmBpDcDtBmBdC}BhBcBdB_BfFwETUhAgAn@s@h@o@BAn@y@^e@n@_A^k@bAaBTc@HQx@_BP_@v@kBb@mArA_EJ[J_@La@fByFdAeDr@_Cx@gCRs@l@mBV{@x@iC`AaDfAmDFUX_Ah@cBZcAf@_Bl@sB`@qAn@mBNk@j@eBj@kBPi@dAiDNg@vAqEfB}FDM~AeFNe@d@_BPg@bDiK|@uCz@qCV{@Pi@BGh@eBDOPi@r@}BPi@J]@EtCgJzCwJ~@yCzBgHjBaGpCaJp@uBBIPi@HSTq@X{@t@oBRk@Vq@Xs@Zw@Xo@Xu@~@wBx@gBl@qA`@{@bAqBn@kARc@PYx@}AjBcDj@gAl@cApBqDxCkFrAcCx@yAf@{@FKd@}@l@gAVe@JQHQv@{A`@{@JQt@_B@Ah@mAf@eAPa@BI^{@HQl@yAr@iBXs@Tm@Nc@`@eAL]Ne@Xw@\\eA^kA^kA\\mANg@Pi@^uARs@Pq@\\mAH_@r@mCnAaF^uAt@yCXeA`@aBl@aCd@eB~FqUbAaEZmAn@eCj@{Bd@gBn@}BJ_@Pk@Tw@Vy@V{@Xy@Tu@^iABGTo@@EHSDOVo@Pg@Xu@`@cAb@iAr@cBd@iAn@yAf@gAl@oAl@oARc@Ta@\\q@R_@r@sA^q@R_@jAsBR]`@o@j@_A`A{Ab@o@b@s@`CoDdCuD`@o@LOXc@t@iANUbBgCtAsBDGt@kA~A_CzA{BBGrAoBpB}ClBuCvAyB~@{A`BkC^o@bBwC|@}AlAwBjAwBTa@HQlA}BVg@dBiDz@gBb@_ALWRc@p@wAz@iBdAaCVi@v@gBv@mBRg@x@sBj@uAZw@Ti@zA}Db@mAJWXu@Xu@fBuE|CcIDKxBaGRm@Tk@FQFON]L]b@eA`@_AXu@Ri@~@cCL[|@}Bh@sAb@iARe@HQTm@Zq@Vi@Ra@Ta@BEJQb@s@R[LSFGNUPUNSTYHIFGt@y@NOHINODCJKDEj@e@^[|@k@j@_@\\QBA`@SFEFENGXM^Oh@Sd@On@QZI\\IZGl@K\\GVCz@KdCWb@EpD_@fP_B`@ETClCY`Ea@j@GdAKh@GnBSr@I@?p@K`@Gj@Mb@K`@KVIRGh@SRGPIVMZObAk@@AZS@?j@c@z@u@ZYXYRUZ_@b@k@NQJQ@?LSJOVc@`@s@Ta@Xk@Ra@LW`@y@Vk@NYd@cAx@eBt@_Bt@yAp@wAr@{Ap@uAlAiChAyBfAuBdAmBTc@Vg@f@}@`@s@pA{BXg@Zk@fAiB`C{DJQXc@DIRYd@s@j@}@d@u@t@gAz@qAnBsCnAgBlBgCnAcBfB_CxDcFdLiOhBaCzBwCnAcB~@mAn@_ALQXa@\\k@PYLUR]Zk@HQNYZu@P_@\\{@Ri@Nc@FSHUDQZcAV_AR}@TgA^mBRqAHq@DY?ADYBYDg@Fs@Dg@FeAB]Bc@Bw@@{@@e@@o@?cAAgA?e@Aq@Cw@Co@Co@G}@GcAOkBMcBEo@QuBIaAQ_CQqBIqAOoBQqBWeDImAGq@CWK}AMwAG{@OsBI{@Gu@]oEm@_I[cEAIm@gIKuACU]kEKwAG{@C[Eg@Cg@Ca@Aa@C_@Ck@Ag@C}@A]?]AU?k@?UAg@@q@?{@@{@@w@@{@B{@@{@@]@{@B{@@w@@y@B{AD{AFgEBo@TiN@e@JoF@q@DgCDmBFkDHmE?CHiE@oABgA@[@a@BeALyILgGHkFBmAF}CHmFBaA?M@K@s@?M@Q?S?M@g@@KB{Al@e]TgNH_D@y@BiA@QBcCViNTuMFiD@o@@o@@EFeEBsA@g@FqCDwB?]D_CJeF?YBo@@o@B_BHyE@UByAFuC?YFwC@_AJuEDyB@o@DkCB}BP_I@e@@o@DoCB_BBs@@k@@o@@_AJ_FHoE@_@DoC@o@@GFwD@W?WD{BLcHNqH?_@NoHJqFFqDHkE@m@@o@FcCDcBDiBJmDDoAHqBNaDL_CFqARcDBe@T_DP{BB]TqCBWDm@PiBJmANuANaB@Eb@_EbAeIRuAZaCTyAf@}C`@kCp@yDt@kE\\mBVuAp@}D`@{BTqAbBuJpAqHJk@@KjAuG|AeJtA_IjBqKx@uEnAmHl@gDRoA\\oB\\mBf@cD^kC\\kC`@iD^iDPkBH_APsBJsAFw@F{@LsBHuAHwAFsAD{@FsBHuB@c@@o@Ba@DmCDwBFqEFiC@[LcIHgFN_IHeGLgHL_HXgQXuPPkKVoOBuAPwJFuDJeGTgNLgIFqDDqDBoC@sB?_A@W?kEA{@?o@?I?wAAkBEuDKcHM_JCiAKmIMkHEiDKcGCwACwAC_AEuAGmBAc@Co@?ECi@EiA{@wTwAe^c@uKGoAMoDUcGMyDGyCGqD?c@CkC?mB?kA?kA@{BDaFJgFHkCBo@@[LsDTeGj@uOHaC\\{IViHJqCZ{HLsD\\uJH{BF_B?EBi@LiDFyA`@wKNiENiEBm@L}C`A}WBq@F_BN_ELoDRiFL_ETeF^yJNaEPuEFcBBo@B{@LsCLsDHgBDkAPyENgENeEFcBD{ANqDJkCDoABu@@MDq@VwHB]NqEb@aLBm@By@J_CP}ER{F@K\\gIHyADu@Bw@D_@HyAZoEb@kFXcE\\gEP{BHaAHqANgBJwAF}@j@aHZaEP{BJ}AFo@Do@Fm@xAeRJ}AFo@L}Ah@}Gl@{Hn@wIZ}D~@yLdAaNFw@XkDj@iHl@iIv@_KXwDl@yH^sEF}@N{BDk@LuBPmDN{DBaADqAFiDHeE@kAPmNDoD@mADwCHeGFqFJeJBsABeCl@ai@BkABiBBsCF{DViTFcGNmMRuPBiBTqRJ}GV{SHaITuP?]HgIFcE@e@?INoLJ_K@o@t@qm@B_BDmE`@c\\PoN?o@J_HHoIJaHFkGH}FV_TToR@kA@C@gABaC@q@@o@@o@NcMFkG@o@F_EHwGHkGNmNL_KZ_WBiBH_HBuC@g@@y@DgB@yBFqDDkDBqBDwBBq@?]@]FuBHmCDcA?SHyAJsCJqBHgBBe@HwAJaBHuAFw@NqBVkDNoBRqBPoBNwARqBBQTwBZmCL}@Fo@XoBXwBVkBv@cFr@qEt@eETiAN}@f@cC^kBb@wBj@cCh@cCFU\\uAj@cCf@gBl@aCp@cCf@eBl@qBj@iBPm@~@wCj@eBhCiIlCmIhByFhDqKbCwHjAsDr@}BtAiE`@kAr@{BfAiDhDsKd@wArAgEh@aBd@wABK`@oA`@sAj@eBt@}Bh@cBh@eB`@kAn@qBPi@Vy@h@eBf@gBZmAFYNu@VqAPgAJy@NqALuAFs@D{@FsABgB@]?}AAmBEuAG{AGy@Eq@I}@Q{AKy@iA_Ia@qCg@gDg@gDm@eEe@eDG_@WeBaA}GgCaQq@uEWmBa@aDUoBSwBOiBS{BUkCS}CM_CQaDMaDIyCMeFEkDC}E?oD?gCBgC@WRqLH_Dh@cUNgGHiDDgBFoCLmEBqAHuCNiHRqIRiILaFJsEPeHD{BDkC@kABuB@{A?y@@_C?iA?mC?}B?_HCoR?o@CsXA{J?o@C_`@AgE?yDAaGEkv@?wACgU?qKCmX?cBCs_@AmH?w@Ca\\AiVCa`@?eAAyBAaZAgGCmj@?[A_E?gJ?kGAe@?cD?uD?gD?UAyB?CAaSCk[Ae`@?o@?_BEaf@?yG?k@A_M?oE?sCAoD?yC?mDAoD?qD?_CAwACiEGiEC}AAw@Cu@A_AEuAC}@U_HIuBEaACi@AOCo@a@{Ha@aHa@cH[aGMuBOyCCc@KkBIqAAKYaF{@wOAI?KCW_@}GMuBAWEo@Ck@?CQ}CIyAIsAEo@AWAUm@uKAYEg@GmAM}BAUKwAIkBCa@CgAA_@Au@Cy@?s@?]?wA@k@@k@Bw@@u@DeA@OxAe[HiBd@uJPmDXeG`A_TLcCHaBXiGn@kNViFXcGVoFvAoZDu@LiCf@qK@a@D{@JuB`@yJJiE?_@B_A@YBqB@uB@wD?cEWid@CmCA_BCwHCgCAq@AkD?QAo@AyBCeDCqDAsDCoDCkFAkB?GCwCCqDC{DE_JCaE?_@IaOI{MEwHAuDAw@AwBAq@?o@C_FGsIEcJEgIAg@CuGEyGEcHAu@AgBAiECaECyGCoC?o@CiECqBEsH?mA?EAcACwEGeJA}AEcGIqPA}ACkEAqC?a@KuREqHEqIE}FCeF?{@A{@AkACuFA_BC_EAoBAaCA{@?{@EcD?[?QA]A]Cy@E}@Ci@AOA]IuAGu@Ee@KuAI{@Kw@Iw@K{@Ga@Ig@OaAUuA_@qBKi@UcAe@kBOi@?AOi@IYq@_CsAqEi@gBs@aCo@wBu@cCk@oBUu@Ok@AAk@oBiAwDi@kBUs@ACc@}AeB}Fw@iCW}@WcAWgAGYI]Oy@Ic@QiAE[K}@QiBGaAI{AEuACaA?oA@{B@m@?A?MBsAD{CJuF@kADiBFeD@cAFsDFaDHeF@o@@o@H_FFiDHeFBoBNkI@uA@SBcBByADoBDyBBsBD_D@qA?oB@_B?Y?uB?o@?i@?C?A?cCA{BCwBAyBEwBCqBKeFAk@?CIaECqA?AY}MAg@C}AC_BGcCMuG?G_@wRc@gT?Ac@qUs@y^EeCAo@WiMs@e_@GgCEiBEuCSiJMqGIkHCqDAwBAmD?sD?g@?iCAuC?iB?wJAoLAsZAcS?uFEmcA?q@A_EAa`@Ao[?q@AuA?iB?i@?sC?uBAyB@}AAkB?yCAcC?eC?C?kJAoL?oFA{JAws@AcC?_C?aJ?S?wIAoG?qDA_D?}NCgf@?eB?I?}D?{CAeE?}B?qN?uL?kCAqI?wG?oFAwG?cBAsCEkECkB?IGmDMkFKkDQoGCo@?EAYW}IMwDg@wPGwBG_B?OKoDQmF?SQoFQ{FQ}FE_BE_BKmCOsFUoICm@?ACm@QkGC_A?ACm@OoF_@mLyAmg@M_EQcGEuAC{B?s@@k@?GBeABw@@[Bc@?AB[@S@QD[B[Hm@NmABUF_@FYJm@BSz@kEVkAz@oEVqAj@wCx@aE?ABO@CF_@|@wEpBcK`@{BdAoFTeAf@mCv@cEbAgF|CkP~AcJZsBDUT{A\\yBl@kEZwBl@qE@QZaCHm@?CZkC^kDJ_A^sDJcA^gEPqB`@aFRoCZmEXoELsBHcBh@}JTiEBo@^{GR_EB[b@{HFsA^aH`@aIh@yJNwCRmDHiB^eHlAgUh@{JbBk[dA}RP{CTaEPmDJgB@]BYBe@By@B]B[@[Bi@Bo@Bm@@c@@W@]?]@e@?Q?]?I@m@?]Aa@?]?a@A]As@Cs@A]AYA[EcAEu@E{@E{@o@iMWyEi@_KCk@K{BG}@I_B?C?GKoBGwAGuAEuAEgACm@A[CsAGkB?EE}AC_BCeBCqBCsBA}AAwBAeC?mD?yC?G?aA?aA?Y?kC?cFAgN@aG?{DC}`A?wI?o@?_E?uE?iD?qL?}W?_@?W?w@?W?eA?uD?e@?gE?U?}B?CAmA?mB?wE?cF@mBA}A?s@?{G?E?oF?e@?A?cR@kF?cGAiI?eFA{D?g@?E?G?eAA_C?w@?kB@mE?kFHgHBqA?S?W?A@E?C?K?A@M?A?AB_AHgCFwABw@Dy@?ALgCHgAFcANgCHuALwB@MTaENoBH}AFyAF_BBg@@i@DoB@s@@a@?UDeEF_HB_E@eBDiFH_KJ_N?ABmC@o@BoC@o@@o@@YLyDJmBLkBLgB?ELuAZsC\\cCF_@ZoBBSTuAfAuGDYJk@r@qEDQVsA?GJk@T{A@IHc@Ha@VuAN{@NiATmAHc@Fa@L{@b@_Cz@mFJm@He@Jm@Jm@d@sChB{KRkA`@iCJk@DUToARqAJm@|AkJv@_F\\oBFa@p@eEHg@DWDQRiAh@eDF[xBwMFc@n@wDb@eC\\kB\\}AVaAf@gBLa@HUHQJYn@}A?Af@eAf@cAZk@JUXg@pD}Gn@kAnByDh@gAzAwC^u@bAoB~@qBt@gBTq@Xy@b@wANi@\\qAj@qB`@}A`B_GLi@Ro@d@cBdA}Dd@_B`@{Al@{Bt@mCBKJ_@v@qC|@wCNi@DKn@qBp@oB\\eA`EgMpD_LpDeLlBcGDMJ[fAmD^kA|BgHPe@bAwCfBwFlCoI`CgHb@sAjA{C@Cd@gAHOvE_KxBuEr@{ATg@\\u@`@{@fA_CxByEbEyITg@h@iAdBsDrAsCHQTe@xByEFK~BcF@ATe@jAgCzAeDtBkEh@mAj@mAd@aARe@FK@EJSFKh@kAJSZq@b@_A^y@lB_Ep@wAv@gBb@aAFKd@iAr@gBf@oA~@eCTq@l@aBHYv@{BBIJ_@r@{BbAkDz@_Dd@eBfA}Dv@uC`CqIbAwDzBeI|@aD|A{FfA}DzAqFfBuGvBaI~BoIbAsD`AqDjAcEvBaI|AyF|@_Db@eBhDyLVaALc@l@cC`AkEZ{Ab@}BLq@d@oCF_@TaB\\}BHs@P{AZiCTiCPqBNsBFy@LyBVqELkB@OJ{ABe@Bc@RaDFkADs@F}@Do@Ds@@WHkALyBJ}Ah@cJ^oG@]F}@h@_Jf@wINyCB[Be@Do@Fo@?GH{@b@mFVkCt@oGd@qDj@}Dr@cEPcAToARiAPw@Lm@BMJk@DOF[Je@TcATcA`@cBTaA`@}Ad@eBVaABGNk@@EVw@ZeATu@HWPi@@ERk@Ts@Tq@Tq@HUVq@Xy@j@}Af@uAt@sBd@mAlAiDb@mAZw@l@cBp@kBf@uAl@eB\\cAX{@X}@DOX{@d@_BTu@@Gb@_BZeAT{@ZkAb@yAZmAvJa^Ni@^uAbEcOZiAd@cBjDgMXcApCaKrBsH@AfBuGfCeJfG{Tb@{AT{@BKlAkENk@^uANi@j@uBBIvG_VpDwM\\kAjAmEp@aCNi@b@cBj@qBNk@p@_Cn@_C`BaGd@aBh@oB\\mA~@iD~CgLPq@Ni@VeAZsAZoAF]n@sCl@{Cn@gD@On@qD?CT{ARkAVkBLaA^aDf@sELiAFm@TcC@K?CDg@Fm@RsBVkDVeDLmALkADc@BWTsBN{AHq@n@}GRmBNcBHo@Hq@P{ABQBSDYF[Hk@N_AJm@Jg@X}A@GJe@Nq@`@aB`@aBd@aBZgAPi@DO\\aAv@{B`KqYvCgIzJiYVs@DKRm@lEaMp@mBRm@nGuQNc@`M_^lHsSZ_AzCsIn@iB\\aATm@fCmHp@kB^gAhDwJLYZ_A?Az@cC^aAbB}EpDiKdCeH|@eC~@iCfCkH|AoEvCgIfAcDhAcDDM^eARg@HWDOL]Nc@Z{@Z{@Pe@n@kBRk@DK`@iABGh@}AZ}@lAkDd@qAbByE`C}G`@kAdAwCt@uBhAcD`@mA`@iAx@}BpAsDrB}Fv@yBPi@d@qA`BuEnAqDbDgJ~C}ITm@Pi@f@uAv@}B~@iCh@{At@yBdAsC`AqCbAuCt@{BZ{@\\_AdAuC`AuCh@aBTo@r@_CNi@`@uARu@ZkALe@TcAJa@v@kDZ_B\\eBX}AVeBp@gE\\uBtF}^lCgQJm@pFg^Jk@|DuWN}@N{@b@sCXkBRuA^cCTyARmATwA^gCVaBT{AL{@RqA`@iCRsARoAJm@Fc@ZkBVwALs@ViAP{@Ns@Ru@`@}AT}@\\kATu@Tq@Tq@l@aB`@cA@CPc@|@{B~AwD~FoNlA}CtC_HrC_H|BuF@CFMBGlAwCBE~@{BnD}InEgKn@mBlB{EnAkDv@wBFS\\cAt@}BTq@X{@j@mBZcABMJ[j@kBr@eCPs@Lg@Lc@ZmAV}@n@}B~@gD~@mDNi@Nk@XiABK`AkDNi@h@qB~AcGtAcFNi@Nk@Ni@h@oBT{@zAsFd@gBPq@Pu@b@_BXcAXaApBoH~BwI^uAPk@Ni@n@aC~GeWH[BEDSHYHYH[H[HYFYH[HYF[HWFYH[Pu@H[F[H]FYHYH]H]H]FYF[H[FYF[FYH]FYfB{I~EuVlFcXrEgU?ALk@bHu]dE{StGg\\Lm@pCiNf@eCbC}LzCkOj@qChCoMhCuMvBqKfLqk@Lm@zMeq@bDcP^gBF]F[F[DS@GFWDYF[FYF]F[F]FYF[D[F[F]DYFYD]FYF[D[F[D[F]D[FYD[D[F[D]F[D[BOBUF[Ho@F_@Hm@Da@L}@Ho@Hs@Ly@@QFc@f@cEHu@t@_G`@iDFa@D]D]D[D]D[BYD]DYD]DYD]?CDWD[D]D[D[D_@DYD[D]D]BYF]D[D]D[DYJw@Hc@Fe@F_@Jw@Lw@PkATuAHc@Ls@Fe@Lq@Nw@Ly@RcAn@gDF]H[F[F[F[FWFYF]H]F[FYH[F[H_@Ja@Ha@Jc@Nm@Lm@Ry@Ja@No@Ru@Ps@Ru@@IFQH[HYH[H[HWDSHYV{@Pm@Rs@Po@Tw@Ts@Rs@Vw@\\iA`@mA~@uCx@}Bf@uAPi@LYp@mBp@cBn@eBTm@Vm@Z{@Vm@Vq@Xs@Tq@Vo@d@kANa@Rg@Vq@L]JUTm@Vq@d@mAXs@d@mAj@yAj@yAFONa@Vo@Vq@Vq@Vq@Vo@@ARg@BKVo@Vq@Vq@Xq@Vs@Vs@`@iAVs@Ne@Vs@Nc@Rm@Pg@BIJ[@CPm@Ts@Rm@Tu@X{@Lc@FSZcAXcAXaAXgAPm@@GLc@DQHWJ_@Ru@?ALi@BKXgA@Cj@aCFSDWJc@BGLo@Ru@XqAPy@Lk@DUXsAVsAXuANy@P{@zHua@ZcBZaBfBiJJm@XyALk@d@eCJm@~B_MLk@Jk@Jm@lCkNh@yCxCyOzFoZDOBOr@sDr@uDr@sDnBeKNy@Jk@Lm@d@eCJk@Lm@XyAVwAr@sDJk@H_@bAkFZcBDQ^uBd@_CDUJm@Lk@F[BQX{AJi@Lk@DWRaAHe@TqARiAX_BRiARqAJs@N}@TaBDUHe@@GHm@?ENgAL{@DYBSFi@NkAPsAJ{@RkBD_@BOTwBBQFo@Fo@VeCXoCzA_OtBmShBkQH{@f@_FRoB\\}CbAwJx@iIVeCD_@t@oHb@iEd@oEVgCb@iE\\}Cx@mIXoC`@uDPcB@QJcAReBPgBP_BDe@J}@RmBT}Bv@sHxAsNVkCFo@jAcLH{@LgAXkCJgALgANqAD_@Jw@TkBVuBJo@Fa@^sCBKDa@\\cC^gCPmA?ERsA~@}GTyAHm@Hm@|A}KHm@He@@Gr@cF`AgHL{@`@qCp@{Ed@kDf@mDR{AJu@VgBn@mER_Bl@aEX_CT_BNgARaBFm@LcANqAJeAJgAJy@LuALuADg@@OHy@Fy@PuBF_AFs@Dw@Fy@Du@Fw@Bi@Fy@HoAF}@F}@RaD?KDc@H}AB]@QF{@HuAB_@Dk@JyAFaA@SBYDo@Do@?ALqBD{@Fw@?CDu@HmADm@JeBN{BJ_BTmDFmA@QHkADo@Bc@F}@HiADk@FcAFeABWBa@Dw@H{@Fy@Fy@Fw@Fy@Hu@@QDi@Hw@Hy@Hy@LkADi@J{@Hu@PaBRcBPwAPqAJw@VmBXuBRuANcAHc@TyAFa@\\uB\\yBRmA@I\\qBl@yDb@oCh@iDNcA^}BlAsHLw@l@}Dd@qCf@cDXiB~@}F@Cx@oFj@oDh@cDXkBZoBZmBHe@@Gj@qD`BiKp@iErAoI\\uBJm@TyAb@qCVaBJo@L}@He@h@cDn@_ET{Ab@eCv@cFr@wEd@sC`@eCPgA\\wBNq@Jq@Fa@TwAJk@NcA\\_Cd@{C`BcKJm@@A`@eCHm@Jo@@CnBaMHm@pBgMRsARqA^wBRiA~@eFb@wBx@kDd@oBv@}C`@aBn@eCd@kBj@{BNi@Nk@FW\\yA\\wAP{@l@qCn@cD@Kl@mDn@qD?C^gCNaATiBZmCDY^oDNyAN}AJiAFw@LeBPaCNkCBe@p@kLB_@NqC\\eGJ_Bz@wOT}D@Kl@sKd@_IPkDB_@LwBLwBTaEJoBPyC`AmPJcBLiCZcFNoCDo@^{GPaDf@sIB_@^{GPyCRqDXeFDw@RoDXwENaCBc@D{@XiEJ{ABa@Di@Hy@RmCR_CNcBLqAP_BBWRkB\\wCNmAP{ARyAv@cGTmBJs@ZeC@EZ_C\\oC^uCD_@t@yFd@oDDWf@_EBO`@{Ch@gETcBNqANgA`@gDLcAJeA?A`@oDH_AZ_DXcD@IL_BHcAFs@N{BJoALsBHaB@OB[L_CHyAVyFBSXcG@AJoBNiD@G^qHN}CRgD@YHaB?INoCV_FN{CBa@XmFRyDR}Dn@yL\\{GZkG`@}HDgAT}DPqDn@gMLwBd@sJHkAx@kPBi@h@iKJcBXwF\\cHDi@d@kJFsAZeGRuDBc@TsEFcABa@HiBJuBH{AH_BBo@Ba@Bi@DqBJmE?CJkFXaOJiFZaPBcBf@}WDiBf@cX?GP}INaI@m@JsELiGL}D?OB_@HeCPgENcDVcEJoBLcBN_CVuCHiARqB@QVmCNwAT{B^cDJ{@?IHm@PyAVyBNsAD[VsBNkARkBPsALoAL{@J}@@Gb@oDZqCFg@NqA@CrB}P\\wCD_@Hk@h@oEXeCp@wFp@{FNiAb@wDFc@XaCZmCNuAZeC?Ab@kEH{@Dc@@Of@uF`@mFj@sIFcALqBhAaRTyD\\uFrAcTPeD@MHiAB]Do@FaAJgBPwCNeCN}BBi@Do@@MXsEDq@VcEReDLmBF}@?EFw@TaEDk@RoDLsBXiETqDRqDPqCTuDHkAl@_K\\sFZgFV{DVsEXmE?ATyDBUNyCD}@H}A?EBi@Dq@F{A@a@HmB?MB}@FcB?MFuBBkAFyC?a@B_A@}ABiCBkEBuB@cA?y@RqYDoI@oC@_B@M?a@@m@@aC@qC@{@BwD@gBB}DD_GB_F?W@gA@OB_F?o@@wBHeM@o@?o@@_@F_K?gA@eA@c@@gC?]DoF?o@J}P@wA@_AFmI@cC@o@B_E@uCFkHBiDFcDHwDBmAN}EH_CFwAPyDJyBL_CJ_BPgCXcEJoAFu@TeCVmCViCRgBPcBToBBUJy@`@_DJw@X_CNgAh@cEJ_Ax@oGl@wE@IHm@`@gDn@aF^uCReBn@cF\\oCRyAHm@xCaVHm@Hs@T_BFk@Js@R}At@eGNiAh@iEJw@PwAPuAHm@BOD]Hs@Z{B^}CX_CFo@LaAT{Bf@}EJoA\\kEFs@P}BJwAPaCTyC`@gFp@cJFq@BSNoB^eEb@cEHu@Fm@DULgA^cDh@cELu@Hm@`@uCx@_GLaALaAZ}BLw@f@wDHm@Jm@f@yDn@mEf@uDBUHm@@Af@uDHm@`@wCD_@Hm@LcAL_ALwAJy@@IBY@IL}AVqCFiADe@F}@LcCFcABm@D}@L}CF{BD{B@w@@k@BqC@gAAmF?c@A}@AwBGmDOcF?IEkAMoCGqA_@aGKwAa@kEa@yDSwBq@yGSsBMwAGs@G}@AOCi@I{AC_AEsACc@?WCw@?_@As@?YAg@?i@?mA?w@@}A?IBmA@o@FaBB_AHuAD{@JyBDs@HuANwCHqAJiBJgBVsEVgFReDR}DDk@Bi@H{APoDBq@NyDHqCD_BFoCDwCBkE?Y?gBA_DA{BEyBAwAEyBImCGsBOqEMeEEaBIyBMgE[mKCcAAg@OgFGyACc@AMe@_PEkAC_@QsGUsHI}BWoIeBmk@EqAOcFAo@QgFO{ESoGQwHEcCEwBGwGCqDAsHCoI?OC}ICiNA{B?eDC{EAcF?qAAcCAwE?kBC_G?kACcBGoEKqGOwFOoEQcEI_BOuCi@oI[gEk@iHASEYe@{FKuAc@gFM{ASgCAK_@_Fe@}FGu@o@cI[cEGuAG}@E}@GsAEq@UoFUgGOyFM{GAo@C_BE_EC}J?w@?C?s@?iFAkF?kO?eD@iJAcE?wDAyBAcCE{BEmCG_CCy@Co@Cm@CmAMqEEgA?C?QCo@?GY}J_@mNSwIO_FGuA]aKSyHGgBGuByA_k@k@eS{Awk@EsAGaDi@kRUmIAo@g@_R_Bgm@mAgd@Ao@KyDuAah@C{@GwCe@{PAo@aAi_@MoEOmFAo@MmEQoGMsFCi@MaFUeIQqGUsJYsK_Am]Aw@EiACeA?AAcAA}@Au@Ai@?o@Aq@?G?{@@gA?{@@o@@o@@y@@q@@{@@O@k@Bw@By@B{@B{@Dy@B{@BoAD{@By@@m@DiABs@DwAF}AFmBFuBFiBDyAFuBFwAFoBBcA@u@@WB}@@w@?{@?w@?{AC}@AaAEkAA]Es@Ey@Gw@Ee@IcAOuAIu@Gc@AIO_AM}@YyAa@mB]yAYeAK[mA_EeD_LCIM_@aHmU_@uA[_AY}@[iAe@{As@kCg@mBQu@c@iB[sAe@uB[wAa@gBc@uBe@uBWoAKc@a@kBYoAYmAUaASeAMo@YsAc@oBEYYqAa@mBI]Mk@I_@_@eBWkAUkASeAYwA?ESeAIg@[kBKo@Mw@SyAQgAOoAMcAAGQyAQ}AOwA?AKaAMmAI}@CWC[IaAGo@IwAM_BG_AK_BGiAGeBEo@EoAKcCEgAIwBEgAEcAOeEMkDQaEMaCO_DMuBQgCWkDYoDS_COcBMqAYsCSkBAKe@wD[mCq@{Ek@cEWyAe@yC]uBe@kCOw@Kk@?A}@sEgAeF]eBsAyFm@}BWeAi@oB_CoI}HeXsAsEgAwDwBkHOi@wCgKa@qA{@yCo@wBOi@m@uB}@yC}@yCc@yAa@yAo@yBCEm@yBCIM_@e@cBSq@g@gBSq@]mA]kAY_ACKqB{GSu@oBwGg@eB}@{CyBsHgAqD]mAo@uB]kAkCcJw@oCmAuD_@aA_@aAUk@c@cAYm@Ym@e@cAi@cAc@y@Q[OWk@aAm@}@iAcBs@cAEEs@{@eAoAeBmB_A_AiBkBsAsAoBoBoBoBiGgGwAwAkDkDiAiAuAuAeAeAgAkAwA}AeB_C{@sAm@eAy@_Bo@sAw@mBq@kBu@_Ce@iBk@gC]kBUwAWiBI{@K{@IaAGw@AUC_@?EEw@GqAAa@Cw@CsBG_FCkDEuDAcACgBEiCGgGAUCyBAkACaAAkBMeJA}@UmRAo@OsLAuBEsCA_AAU?YCeBCiBEmEAQAaBA[?OAo@AeACiAAo@?IC}ACqBAqBGgDMiEC_ACy@K}BMsCCWMkCQoCKoAK{AUiCGs@Gm@Go@e@iFU_CgDk_@Gi@IaAQuBEa@g@oFi@_GC_@SyBI_AO}AIeA]}D_@aEGm@UiCWkCScCWyCcAaLGm@Go@mAiNO{AM}AI{@KgAEi@KaAIaAk@iGi@iGU}B[oDk@oGm@}GWkCk@yGWoC]wDGm@M}AE_@I}@CUIgAGm@Im@Ec@Ei@K{@y@}GOgAUyAM{@Ki@U}AUmA?CIc@Ig@CMIc@Ki@QcAWmAOy@_@kBwB}K]iB"
                            },
                            "start_location": {
                                "lat": 41.5846019,
                                "lng": -87.23498309999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "76.2 mi",
                                "value": 122605
                            },
                            "duration": {
                                "text": "1 hour 7 mins",
                                "value": 4036
                            },
                            "end_location": {
                                "lat": 41.1196534,
                                "lng": -80.8457164
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to continue on <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "gjr{F~nqtN{@sEcAgFAG_AgFMs@G]COOeAU_BK}@Ig@KaAE[OuAMwAIu@MiBMaBKqBEm@Ew@Co@Ci@E{ASwGE}ASkHK}Cc@_OMwEs@aVUmIS}GCo@GoCo@qToA}b@OeGo@yTOaFQyFO}E?S[}JImCAo@]gLC{@C{@WmICo@EgAA]OuFE{ACy@A{@Am@AsA?eA@}@B{@Bs@D{@FcAJcALoAF_@Fc@Ha@F]Nu@Ry@?CVaAd@{Af@cBfB{FNi@Nc@J]v@gC\\iAVy@d@_Bl@qBn@qBDOx@oC|@}CfAoDfAqD|@yCr@{BX{@Rq@lD{Kn@{Bb@aBf@uBVmAf@sCf@oDRqAf@eEZiDJaBJ{AJ}BBu@Bu@BkA@o@DyB?yA?a@?kBAoBEsAAq@Ac@EyAEk@Ac@Ew@CWEm@GgAKoAI_ASmBO}Aw@wGGm@MiA_BaN_BmNK}@WwB?Eg@gEK}@Ky@Iw@AIEc@AIGg@AEIaAIaAGgAEu@CiACe@AmB?a@?s@@q@BqABw@F_A@WBa@J_AJ_ATeBPeAHi@^iBT}@XaATu@X{@JYf@oAj@mAnA{Bp@gAl@}@l@u@Za@pCkDtEcG\\e@Zc@R]T]DIt@mAnA{Bj@kADIn@uAr@cBTk@BKZ{@`@mAZgAb@wAZoALe@T}@XuA\\cBDULu@b@mCXyBV_CR{BNqBJwBD{AH_CBkB?w@?sAAgBE_CO_GKqCc@oNYwJC_A[}JCo@ScHi@uPMcEGaCM}DGgBKgD[mJYsIY}IGwBI_CG_CGmBGgBI}BE{AEaBCaAC{@CcAGcDCeACwAAoBCqBAuAA}B?cB?{B?}B?eB@kBBiBBiB@}@@g@@S?UDoBDiBNuGd@{SLyFBi@JuE@o@JeDBsBJuF@k@BwDB}D?]BoF?oC@oF?wD?gB?}FAqG?o@?o@?o@?A?}A?mE@iA?A?_A@O?U?}B@_A?k@FgCFoBFsBBm@Fy@HiA@QLuAF}@RmBL_AX}BL}@?AVyABOHi@Nw@?A`@oBPw@DUFSTeAl@}BT}@FUr@yB@Eh@wAl@yAVm@BE?A^}@FOz@sBN]l@oAb@{@d@y@z@yA|@wAhAgBn@eAXc@Va@|EyHVc@p@eAVa@hAiBV_@?AFIBELSBCp@iAh@}@n@iABEh@aATe@Ra@~@uBr@gBb@iAb@mARk@h@mBXaA^{AZqAPu@DSTkAX_BNgA@G@GNcAHo@ToB\\}DDi@Fy@FoA@O@_@@I?KJmD@g@BaC?_BA}ACaBIsCIqBIuAEs@Cc@?CCg@UeEWqEUwEQ}CK{AE}@KgBAMMcCMyBKmBMsBKsBKmBI_BIsAIyAKqBAIGoAGcBG{BCeBCmC?mC@uA@mA?k@@a@?_@DwABaADoAFsAH}AFkAJ{AJwAH{@LoAJiAFm@D]^qDDY\\gDd@cEHu@Fm@J{@ZwCRkBTyBXmCJcALgAXkCTqBN{AXsBRsAJs@FWDSVqAZyARw@Ps@h@gBj@aBb@iAr@cB`AuBPa@|@mBVk@hB{DpAsCr@{AxAaD|AeDbCkF`AsBPa@^u@bA}B|AgDr@yAPa@Te@?Aj@kARg@Tc@Re@p@}Ax@}Bj@cB^oA^sAVgAVgA@IHa@Lo@VsARmABOBQD[Ju@Jw@Dc@Hu@Hy@HcA@QB[B_@FcABi@B}@D_A@o@BeB@qBBiC?C?k@@qB@wBDsF?O?_@BuF@_BBkC@}C@]?o@@qA@}@?o@?u@BkC@iB@qB@eA?{A?G@g@@wA@uC@u@@eA@kA@wA@wA@_B@iA@c@@oABgB@e@B}@BqADkABu@DsABs@@I?GFkAFuAJiBHsAHgAF}@LyANkBB_@JeAXyCDc@Fc@LgAH_APuAJq@Fg@Hm@NaAL}@PkAJs@Lu@\\kBTsAP{@BMJg@BSPw@Lo@Jk@FUHc@Lg@RaAPu@Pq@ZsANk@XeARy@La@Ru@f@eBf@eBVy@p@sB`@oA~@uCb@qA\\cAjAqDZ}@n@oBj@gBX_Ah@aB@CNc@^iAx@eCx@gCfAgDl@iBvCcJfAmDbAgDh@gBf@iBl@_Cj@wB~@{DPm@XkAp@qCj@}Bt@{Cp@uCNk@x@gDr@yC~@sD^{AXmAj@cCf@qBlB}Hh@yBn@sCP}@H[BWF]Ha@PqADm@@C@K@GDg@@S@MDiAFeB?Y@S?a@?O?cAAkAEeBCqBIaDCs@OgIKkE?K?GKmECcAAcA?k@AG?m@?k@?]?_@@[?WBk@@e@?AD{@FcAFeAJ{@JeAPoAJu@Ji@Lq@Pw@XmANi@Nk@l@iBN_@JYDKFMl@uA\\q@Zk@z@uAp@cARYNQFIf@k@d@i@`A}@RQjGqFpHqG\\YdA_AbBeB`AgAxA_Cp@oAJWHOFOHM^aAX{@Ro@Tw@H[Nk@ZmAd@oB|@yDF]J]x@uDb@uB`@mB`D}O\\mB@CNw@bAyFn@}DJo@n@uDFg@`@gCh@uDF[\\cCTaBBQj@mEJs@d@oD^qCJ{@p@_Fz@sGn@aFPqA@EHm@BQFg@Jq@He@Hk@V{ARqATmAR_AVoA@EP}@TaALk@XmA\\sAZmARq@Ru@Pm@J[Tu@Ng@X_Av@yBn@gBd@kANc@d@iA`@aAh@mA\\u@bCqF@Ch@mAXq@d@iAjAwCl@wAN_@v@uBv@uBbAyCTq@h@wAd@uAxAwE`@sAv@mC~@gDdA}Dj@uBn@qCd@oBT_ADQ`@iBb@sBReAP{@f@gCv@gE|@uEj@}Cv@cETqAd@mCh@wCLs@Jk@Nw@`@{B`@wBd@_CRcALk@R}@XmAZqAPu@Po@Ru@Pm@Rs@XcARo@Ne@Tq@\\_AFUBGLa@@EXw@Na@JYz@yBLYr@iBdA}Bj@iAh@iAt@wAd@}@|@_BDK`AgBdAmBBE|@cBlA{B~C}FDGr@sAv@wAv@yAp@oAx@}Aj@_An@kAf@cAf@cAf@gAd@gAZw@Xq@N]L]X{@FKRo@b@oARo@Pk@Ng@d@gBFUH[DM`@iBXsATeANw@TsAXkBLaAPmARgBPiB?ELwABUJgBHqAD{@DqADmADqA@}@B{A?A@mC@gE@mC@qD@mD@uFBmH@iB@{B?eB?E@_B?mA?Q@kA@cD?o@@oB@mB?o@@_CBkG@iHD}H?wA@kABqT@_EBaABmAF}BL_D@OBq@N}CLkBF}@N_BJqAj@_FPqAHo@RuATuA\\qBRmATmA^cBXoAXkAf@wB`@sANk@Nk@x@oCXaA~AqFpAiEt@iCp@yBBM`@sAZcAr@cCh@kBlAkEjAsENk@FSZqAf@uB\\wAb@sBBOt@kD@Cd@cC`AaFJk@FYbAkFv@cEr@qDXyAjAkG~@yEf@oCf@kCzAwHxCwOfBeJpBiKJk@ZcBHe@^mBPw@PaAb@{B`@qBb@qBn@aCHUNi@Nc@@Et@sB\\{@p@{ADITe@t@{A`AaBrAaCj@aAfAmBfAmBfAiB^o@f@_Aj@aAv@uA@?bAgBP]v@qA@E~AoCHM|@aBn@gAZm@Zk@r@yAf@eA@CRg@b@eAVo@d@kAn@gBh@eB|@wC~AkFp@{BNi@Pi@pBwGhAwDFUZcA`@sAhAwDx@kC|@}Cf@_BRo@DO\\kA\\eA@ENi@FUNi@HYXgABINk@DQRy@XoADQNk@Jc@h@}BNo@^_BTcAVcAdAuEZwAFUNu@Jg@H]\\}AfFqVbAaFh@kC`@yBb@gCDUD[RgAJi@Lq@Je@H]DUNk@VeAj@oBNi@La@Pg@Vu@Vs@^aAZw@`@}@Zq@Re@^s@LYR[d@{@BEP[f@{@l@cAt@oA`@q@j@cAZg@T_@Tc@b@q@R]R]R_@Xa@Tc@FKhAkBjAsBdAgB^m@tBmDLUT]P]PYz@wALU`BqCT]P]R]BCTa@NWT_@@CfAiBv@oAnBiDRYx@wA|@{AhAmBt@oAj@cAj@aAh@_A^s@Va@R_@Vi@`@s@n@mAv@}Ax@aBl@mAZq@b@aA`AwBt@aBTg@N_@p@}AtAkDdAoC|@aCj@_Bd@oA^gA`@mAb@oA@ENc@Lc@ZaAv@cCdAsDb@aBNe@Rw@H]\\uA^uA?ALk@H]Ry@H_@XsA^gB@GJe@^oBd@cCZoB^_CN{@ViBViB@OHm@BQLgAXyBHu@JiALkAD_@Dc@NeBJuAJ}A\\mFNmCLwC?CLmDFkB@o@Bs@ByA@u@ByA?IBeC?m@@o@?Y?eA?Q?kA?AAoC?y@CcCA{@IsDAo@?OGeBE{AMwCY_G?CEi@K}ACc@AKKoAMkBAIEe@Em@Gm@AKEc@IeAKeAKaA{@gIOoAQwA[}BUaBIi@?Co@kE_@}Bg@qCQcA?AUmAOu@YwAQ}@i@iCESGYE[I_@_@gBS}@YiAKe@Ke@Km@Kg@Mk@Ok@I]Mk@AEKg@Mk@S{@[wAU}@o@}CCKI_@Kk@ACIg@Ou@WoAMs@Ow@W}AM_AKy@CUKeAC_@Cg@?CCk@ASA[?KAu@?{@?o@@O?W@[@W?S@MBa@@SDo@Be@JqAHu@PgBJaA@G`@{DToBLoAJsAFm@LoBHmAD_AHiBDaBBaBByA?yA?{BCmCAq@Cm@CuAIgEI{CQuICk@CmAOqHO_HCcBEeBGsCEmBGwCA}@KuEEwBE_BGcDAYAo@OwGM{FCyAE}AKoFAo@O}G?AAm@Ao@Ao@Cm@]mQA_@I}DGmCE_CGqCAo@I}CGiDA]Cw@EiBCgAAaAEaBCiACgAAu@EeBCw@AcACu@A}@EqB?KAa@AWCoD?yD?yA?sA?K@iB@gADsCFyCPaGPyDNsCTsDZaE@UV{CL}AFk@Hi@XiDFw@@OJcAh@{GXkDNeBVuCV_DJiAXgDV_Dr@qIDi@JiAZ}DNkBVmDVsDJyANcDNgCLqCP}ELcFBsABcA@o@D_BDmD@kA?s@BuA?Y@aA@wEDgL@yA@sA@sC@w@@eD?o@@q@FoR@gA?w@@_@?OB_E?U?Y@eC?w@@o@@cC@oC@kB?o@?C@sBBsF?QDoI?YD_I@{B@mC@wCBoF@sD@}A?g@BaG@q@@kA?aABsC@s@DkBFmCJqDFwBLeDHkCHaCJ}CB[?SHyBJsCJ}CFcBHeCHsB@]@o@@SJqCJgCRcGLcEV{HVqHFqBHoBFwBHkCHoB?IHuBFiBTcHNcHF}F?yD?wA?cBCiDAOEuCAi@G_DGoBsAi_@OcEEyAAKQ_FW_HIkCCo@GuASwFQcFKmCG_BCo@I{B_@wKi@_OYmIGiBGgB]mJCo@_Bed@Co@_Bed@_@iLKyBKoCCw@Ay@Cy@CeBCwACyB?}B@yA@_BBq@?IDqBJsDBa@Dm@TaEFiAHaANyAD_@b@iE`@sDNsAXgCNmALqAH}@VyBZoCFu@D_@BYHk@RyALqA\\_Db@{Dl@mFRkB\\cDf@sEZsCBQBYJaATsBHiAJiAVcDHeAJqAF{@JwALyBRuDT}EBi@LiDHmBFcB\\eJTyGReFVeHNwDT_GJaD@SB[FcBNoCRuDDo@Bc@Ba@TcD\\}Ef@}F|@iKV}CTqCBW^mEFq@TmCRwBj@}GReCJcA?ADm@^iETuCNkBPkCX}FHgB@_@Bi@D_BD}@DeBFaDDcEB_EBuC@sBFgIDgIFwI@oBBsEBaEB_G@kAFiJF}IBgDDyGFqJBwDFoIBgC@uC@o@BqE@]@}A?o@BcEHeKDsEFyDH_EJgDLqDHyBH}ANaDJiCN{CLmCXuFFuABm@@CPyDHcBB_@ToFD{@Dm@Z}GF}@@_@d@sJRmFLkDHkDFgCFqDD_B@o@@q@FkC@o@LoGJkFJiFHwDLiGTkKDmCDmBPkJHiDj@iY@u@@WFoDBq@DaCZ_O?IBmA?MH{D@u@NmILqGNcHNyHH{DV{MHmD?Q@m@J}EF_D@o@R}JXeNBuAB{@FiCDqC?e@BcCByD?Q@sB@yC?oB@aLHwj@@}D@oIBiVBaKBsQ?qA@uK@mI?G?wA?C?g@BmL@gB?cE@cG@yH@_D?sEBsI?kBB_M?wC@m@?_J@_B?e@?Q@}C?m@?wB@cD?M@uC?_D?q@@q@?qB?uC@iC?{B@}A?_A?kC@uC@qC?sCBkC@yCDcCFyDHcDBy@NwFFqCHgC?c@JmDF{BBo@JsDDoBLiEJuDNkGJaDHiDHkDLaE@e@DkCDeB?k@HoG@}C?o@?K?c@?}A?kEA}@?oAEyDE_EKiFCu@KkGM{FK}EIsEKcFIuD?MAq@M{FMyGKyEI_FSuKKeFKqFK}F?MAo@KaGEcBMkGEwBIyEEuBIiFK{FGaDEyBEgBAo@GqCC{AIsECkACwAKyEQaLE_ECoDA{B?}D?yA@}C?Q@eBByA@sBDyB@{@J}DJeEHoCJmC@WP{EPuENaELyDN_ENwDToGNiEHwBBm@`Cwo@By@NeFH{AHwCJmDBu@@o@DuB@U@a@@u@@g@?O@m@?ABgB?g@@o@@}BDoKFmR?m@B_HFcS@kC@kC@sGFmOJ{_@@o@Tiv@Vyw@?O?_@?m@R{n@@}G@_BDmOFmO@oC?_B@_B@mC?o@DiN@{AD}L@eDB}BF{CHkCL{CPwCNcBNcBHaAV}BRgBT_BJu@N{@RqAVsAZaBXsAd@wB@GLk@@Cb@aBXcAHWt@eCbA}Cj@yAf@uA~AsD^y@`@{@|@gB|@_B|CkFzBsD\\m@`BqC|@yAvAcCj@_AJO`@q@dCgE`HiL~AmCxI{Nf@{@Vc@`@q@`BoCf@{@Xa@t@oAbAcB\\k@LSHOn@eAz@wAx@uApAwBh@}@Ta@fBwCXe@x@uAZg@p@kAXa@FM~B}DnBcDpAyBfCkE|AeCn@eAJSLStDkG`BmC^o@|AiCZk@f@w@v@oABEVc@j@}@t@gAr@}@t@y@LONMXUNK^[j@c@d@YDCl@_@n@]h@Uf@Sr@UlA[ZKf@Ip@ONCREl@KnDs@jIaBxBa@BAlE{@BAnDq@~KyB`ASr@ODAtFgAlE{@NCrBa@LCvBc@jAY`@IVGdBe@n@S`@Mb@M`Cy@pAg@v@[~As@fB{@@?LGnAo@|A{@d@Y^UDCv@e@@AdBiA`As@RO\\W\\Yr@i@p@i@RQ?Aj@e@NM\\YRQnBmBbAaA@CZ]@?RUxAaB`AiAl@q@X]hAsAb@g@dBqBFIzCmDvBgCX[x@aAf@k@TWh@q@n@s@VY~AmB^c@Z_@LOpA{ApA{A`BwBlA}AFGb@k@fA_Bl@{@dBkCR[BGhAeBXc@DE|@wAnAoBPYx@mAJQJOVc@j@{@fBoCb@q@NUT[pAsBdAaBT_@nAmBxBgDdAcBrAqBlAkBZc@LSXa@p@_Ap@aA@CnA_BfC}CPUtBaCbFyFnBwBtCcD|@eAnByB^a@Z]`CmC~@eAxDkEjHeI|BgCd@g@TYX[dBmBf@k@f@k@|BgCpAyAh@m@PS`BiBfAoAjDyD|@cA`EuErC_DlAsAnJoKjFcGv@{@zAaBX]pB{B\\_@d@g@x@_AfAmA\\_@\\a@PSLMb@i@\\_@VYl@s@~@gAj@q@l@s@j@s@RWPSFIv@aAdAuAnAcBl@y@j@y@z@mAb@o@n@aAxAyBnAoBtA}Bv@qAFMVc@Xg@n@gAz@}A\\o@Ta@t@wAt@yADId@}@nByDj@kAbAqBpAcCtAoCRc@Tc@f@_AzA}CP[Vi@Tc@~@iBh@eAt@yAx@aBp@sA~@iBx@_B\\q@BEl@kAdAuBnAcCjA}B|@eB~@mBr@sAl@oALS`@y@d@_Ax@}A@Ez@aB|@eBf@aAl@mAl@kALYxBgEfAyBRa@Xi@Ra@BEh@eAXk@bCyEpAkCxHkOhFgKVc@dKiS|CeG@A~CiGZo@Te@Zm@\\q@^q@Vg@LW@AJUNUP[Ta@P[HMHONUNWNSPYP[PYLOJONUNWT[^g@\\g@^g@d@m@p@}@X]n@u@RWRU`@c@^c@LMRU@?NSb@c@BC\\]b@c@NOPQb@_@d@c@d@c@\\YTSNMb@]\\Y`@Yh@c@jA{@\\Y^WtFeE"
                            },
                            "start_location": {
                                "lat": 41.386756,
                                "lng": -82.1785646
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.9 mi",
                                "value": 1433
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 98
                            },
                            "end_location": {
                                "lat": 41.111962,
                                "lng": -80.835289
                            },
                            "html_instructions": "Take exit <b>218</b> for <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "yd~yFvdmlNL@B?FAFCjBkApAw@VOj@]NINKVMTIRINERGTGVGj@If@ETANAZAB@z@Bh@B`ADT@V?T@T?J?J?VCPCTETGRGHEJEFCHEPMLIFEPQNQPQLSNULUJUHUL]HYF[DWDYD_@B[@O@M?I?O@]?a@?u@?a@AM?o@Ao@?E?i@?q@?s@@]@Y@a@BYB[B]D_@BUF_@DUX{Ar@}Bv@gCR{@J_@n@uCL_@"
                            },
                            "start_location": {
                                "lat": 41.1196534,
                                "lng": -80.8457164
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.2 mi",
                                "value": 358
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 27
                            },
                            "end_location": {
                                "lat": 41.1098277,
                                "lng": -80.8321871
                            },
                            "html_instructions": "Keep <b>left</b> at the fork, follow signs for <b>Mahoning Ave</b>/<wbr/><b>OH-18</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "wt|yFpcklN^wABKDMFUFSJ[DKFMFQJSP_@HOHONY@AJSTYRYDGfBcBdBcB"
                            },
                            "start_location": {
                                "lat": 41.111962,
                                "lng": -80.835289
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "4.5 mi",
                                "value": 7279
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 263
                            },
                            "end_location": {
                                "lat": 41.1245504,
                                "lng": -80.75049249999999
                            },
                            "html_instructions": "Keep <b>left</b>, follow signs for <b>I-80 E</b>/<wbr/><b>Youngstown</b> and merge onto <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "mg|yFdpjlNBGBC@CDCRUHIJKNQBEDGJOFIFK@CBGHODIDKBIDKBKDOFO@KDKBQBQBK@QBO@O@M@O@c@?O?QAW?K?KAQAQCUCUCQEWEMCOAEAEEKIYGMEOGOKSKQe@u@y@gAW[Ya@W]GIGKGKIOMWISISGSEMCKCKCOGYCOAOCMAMASAWC[?CC]Es@E{@AQAI?CAC?AAAACACIQKkCCeA?GACCm@Co@Ag@GkACy@Cw@C}@Au@Ay@CaAA{@A_A?}@Ay@CaBC_AAs@Cc@Cc@C]Ce@Ce@Ea@Gm@Ge@AGG_@?EEWG]EYMk@Ie@Ia@Mi@G[Mc@Ou@}AsG}C_N]uA[wAMk@]wAcBoHoBwIwAcG[mAs@kCSs@So@Sq@m@eBQc@IWGOOc@M]_@aAk@}As@qBIYAAYy@Qk@So@Qm@k@oBSq@{J_]YeACI_@gAyAaFYeAQi@eBeG}@_D_@{A]yAm@wCG[Kk@Q{@W{AOeAc@yCY}BQ}AOyAAISiCIy@KcBEaAGiAGkAAYKaDAq@Aq@C_BC{A@k@A{D@[CmO?cIAcD?}G?eCA{CAkC?qW?_@CiN?qLAiL?yAAoD?O?A?}F?oBCkAAu@Ew@Eu@C[C[Eg@Iu@K_AO{@Ic@SaA_A{D"
                            },
                            "start_location": {
                                "lat": 41.1098277,
                                "lng": -80.8321871
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "4.4 mi",
                                "value": 7027
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 238
                            },
                            "end_location": {
                                "lat": 41.1473731,
                                "lng": -80.6770118
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to stay on <b>I-80 E</b>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "mc_zFpqzkNSs@KWIOGQUs@Uq@Wo@?Ag@gA[o@MUWe@U_@o@_A]g@c@m@[]EGW[kDiDe@c@sAgAg@]OMcAw@e@_@c@_@SSk@i@c@g@a@e@UYW]OSWa@]g@]k@a@u@S]O][o@mAsCyCwHg@qA{B_GyA_EEImAaDi@wAw@oBUo@eAmCg@oAuBsFiB{EaCkGcCmGsAiD]_AmA_Dy@wBm@_Bo@aB]y@u@qBcAcCa@gAyA{D_CgGw@sBAA_AeCsAkDiD{IyDaKc@iAQc@IUIQSg@gAyCoBeFkC{Ga@cAm@{AM_@Qi@IUa@uAg@iBWeA[kAQ}@UeAOu@Ki@YeBKu@OiAMaAUoBUaCIsAAg@Ec@Ey@AQ?SCm@GqBAm@?kAAcA@y@?g@@eB@O@aCBy@@oB?oA@kAB}D@{@BsD@gC@eBDgF@aD@q@FsKBsE@qC@mC?oB@yA?yABsD?YBeCB_B?ABgBJoCFwAFuAHeAHiAPiCLwAF}@Fy@Fy@Fu@@QDi@?CDo@Bw@Bc@?ABw@?u@?a@?u@A[A[?M"
                            },
                            "start_location": {
                                "lat": 41.1245504,
                                "lng": -80.75049249999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "268 mi",
                                "value": 431212
                            },
                            "duration": {
                                "text": "3 hours 58 mins",
                                "value": 14272
                            },
                            "end_location": {
                                "lat": 41.045375,
                                "lng": -76.01305479999999
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Entering Pennsylvania</div>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "arczFhflkNEw@AWA[C]KoAE[Ga@Mu@Ga@Qs@Qq@IWOe@Yy@EMCGK[O[ISACKQGMOWIOKQM[MSOWMOQUIMIMAA]a@Y]CAa@a@MMCCeB{AyAmAyAoASQe@e@WU{@_Ao@u@_AkAi@s@EIy@iA{@_By@yAcBwCU]yAmC_AgB[o@[m@Q[k@aA}@aB]m@a@}@Wi@_A{Bw@mBSg@c@gAKWa@iAc@sA]oAm@{Bm@eCEQCOQeASkAU_BOuAQeBC[AQOqBMyBeAuSGoAGcAa@sHAO?C]wHO{C?OCk@?MAYGoCEoBA_@AwAAy@?YCmC?_@?u@?_@?O?M?u@?]@y@?y@@gABaB?[@{@DeB@m@@WBuA@[Bu@B[?CJkC@c@B[Bq@Du@D}@X}FNoCHoBFqA@CFsAf@kKNwCR_ENmCFyADcAL{BF_BB{@@w@@U@[@aB?k@A_A?CAc@?c@A_@I_CQuDGs@Gy@WyBW_Cs@_E[uAm@cCgAuDuBeHkAaEeB}FyAcFQk@sAqE_A}CSs@aCeIgAsDu@gCw@kCs@_COi@Sm@qD{LgAwDg@aBmAeEGQoBwGcAeDm@uBk@oBs@iCs@uCMe@[uAe@mB{@cE[{AoAiGc@{Bc@wBcBmIAIm@{Cy@cEu@sDMo@a@uBEMScAMs@[cBc@sB_EeSQu@Q}@[yAIa@Ou@[}AWgACMEWEQMk@Km@GY_@kBKq@Q_AMu@CKEUCQKi@Ii@uAmJIo@Ku@EYE[CQAMGa@Gc@Gm@Gc@AKWaCO}AAMEe@CWKmAAIASAQAIE]UoDUoDEw@IsACk@GmAC}@?ICo@Eu@Cw@A_@Ao@AGAg@AS?[AYAy@Cw@AsAAy@AyAC_CAkICiE?uBAmBAwCCoF?o@AmC?o@?o@?o@A_B?o@?o@AuGCwJE}L?EAm@?o@Ao@AoC?o@A_BAo@?M?oA?o@AY?yAAs@?eAAcB?m@?c@?a@?OAwH?a@?y@?}@AqAA{BAqBAeAAe@Cs@Cm@EgAEw@G_AIoAE_@Gq@Iw@Ea@SgBG_@Ku@?EKm@?CKg@?AKk@SiAOw@Ka@CMGYI[[mAMi@AAMc@]iAUu@?ASg@K[Wu@Um@Qa@EKMY?AUg@O]Yk@KSISCGWg@i@cAQa@IMMUYm@[q@s@uAe@_A[o@EGGMMUg@eAi@eA[o@e@_AoAcCu@{A]q@a@}@q@{Ac@gAWq@Ws@]eAQi@CGIYCGOk@]oAQs@Me@CMI]EUWkAEYOw@Mu@SqAKw@Ga@MmAK_AC]E_@Gu@Gu@Es@Ca@?MCe@C_@Cy@?ICo@CsAA}@Ay@?y@?y@BqBBuA@y@Dw@@_@Ds@Ba@@]Fw@@UDa@B]BYFm@?ADe@D]NoAXmBL}@Lq@BQNu@F]H_@DSDOJi@FUfB}G`@{A\\oAZmAd@gBrBwHp@eCv@yCZkAPw@Nu@@ELi@Lu@N}@NcAFe@@GHm@D]@OFm@?ADe@NaBH}ABw@DcAJwE@g@Ac@?U?o@AsAAeC?eC?K?mB?CAeB?wB?m@Ao@?W?qB?E?o@AmE?_@?iAAsEA_E?aBAsCCaR?uA?w@?u@AA?y@A{@CwACw@?UCe@Cw@Ey@KsBIuAKuAI}@C[Iq@MuAGe@EUIq@QqAM}@i@{CMy@[gB[cBAGIe@Km@WwAKm@GYi@yCAIeAcG]uBY_BKk@SoAOw@SqAOw@Ie@Gc@AMCSKu@Ks@Iu@Iw@Iy@Gy@Gs@Gy@Ey@Ci@Cg@Cq@Ci@?IAWAW?]CqAAY?[AsB?]AU?U?iAAu@AqBAgEAmBA{AAoB?uBCsB?g@?Q?C?Y?_@?CAU?S?c@Ay@AkDAoE@mEIkM?u@GkM?KKuS?_EAgCAmBMq[?mBCcJ@{E?eA@m@?m@@m@@m@@k@?o@Bu@DwA@YDsAB}@Bu@D{@Bu@Dy@B]Bm@@IFuAHuAJqA@SDe@?IJiAJuALsAJsAHs@J}@Hy@@MFi@Ju@NsA\\kCTkBDYHs@@ALiA@KPuAPsANoAJy@Hw@Fw@Do@@EFy@D{@Bu@FyABuA@w@?y@?w@?u@Ay@EyAAc@Cq@Cy@E{@GsAIqBIqBGyAEs@IwBIqBCm@Ce@GwAGuAGuAGqAC{@GuAGsAE{@Cy@Cy@Cy@Aw@?AAo@?IAy@AmB?K@oA@uA?Y@{@By@BuADoAB}@BuADwADsAB{@BuA@KBiAHoD@c@Bo@DwADeBBeAFwB@o@Bo@@e@DyA?O@m@@UBsABaB@kABqB@sB?wA?qAAuA?y@?[ASAaA?q@AaACy@?[Cy@CsAASCo@?CCs@Cq@EqAGuAAUE{@IyAGqAQoCYmFK_BaCib@Co@_@{Gi@aJSmDY_FQmDIqAGy@GsAGy@ASGaAGoAIuAE{@EqACy@C{@CsAAsA?yAAu@@yABqB@uABuAB}@@}@PcMH}EFsDDoCBgCDmC@qB?sBCoC?OCo@Aq@EuA?EEmAAQCg@Ew@KwAEs@C]COIeAGw@CMEg@Gw@Iw@Gw@MuAMsAMsAQmBKsAE]OqBUgDIsAKqCCgA?IAe@Aq@A{ACmBAqACsCKoL?mD?y@?Y@U@{ABiD?WFoEFmGL_MDmDDkD@aABo@B{@Dw@Dy@HqALoAH_A\\iCV_BN}@Ns@XuAR_A^uATu@\\iATq@To@Vo@Vm@j@qA`@{@JSNYh@aAh@aAZk@pA}Bl@gA?AZi@LWZm@Rc@Pa@Vo@Pc@DMTo@HSPi@Ng@b@}AXkA?CZyAToALu@PqAJw@?AD]@MFg@JuA@OBe@?GDu@Dy@@]@o@?I@k@@g@?q@?I?y@AiAAI?e@AUCw@Cw@GcAGw@Gy@OuAWiBUwAi@oCi@eCqAsE[iAy@sCo@kCsE{P]sAc@gBUoAMy@M}@IaAIgAEy@Cy@AcAAaAAw@GyKUe\\?o@E_E?m@C_EIkKAyACuBC{AE}@Cw@Cy@GkAQsCUkC?CGi@KgAUqBE[Kw@Ku@Mu@q@{EMy@yAaKOoAKw@MoAKyAGu@Ck@Es@AWAa@Cg@A_AAk@Aw@?A?u@?{A@e@?E?UDqBHeBFgAHgADk@@KFm@JcAJ}@Hk@d@gDNeAHo@L_AZyBJu@P}AJgADi@HoABs@?[@}@?e@Ay@Ai@Ae@G}@Cc@EYI}@E[AMEWG[Mq@G[Ia@IYMe@Qo@Oc@o@oB_AkCwAcEu@uBmC}Hk@}AQs@ISu@{BUo@s@sBe@sAc@oAeA{CeA{C_AmC]aASk@CIaAwCOi@w@cDEUKq@[cBKk@WgCIy@Em@Gm@]{D]yDm@}G]cEu@qIKoAGk@Ca@AKEa@S{BY{CWyCWwCWkCEo@O{AGo@UkCIaACYGe@QmBKyAK{AEy@AOGgAI_BCw@G{BAw@CuBAO?u@?iC@oABoBFuB`@qLXmIRuEFuBJsC@[FwB@WDwBD}D@gC?sBCoEK{GKiIAo@I}GAo@E_EWkRAo@C_BQ{MAwAAYA}@GyEG_FKaGGiCQcEMqBg@cIg@cI]iFi@kI[yESwDK}BCw@EiBEsA?ACiBCkCA{BOcYCcGAo@Sya@AoDAk@AgCAkB?k@CqA?o@OeHs@sI]aDWuBOgAYeBSgAe@gCi@wCo@sDSkAYwBGk@Ea@E[UgCIaAEe@GaAEw@Ca@Cg@IsACu@Cg@Am@EyA?e@Cs@?{AAiA?}A?A@yABwA@{A@oA@yABmCBuBN}NB_CBcC?I@uA?EB_C@_AB}BBwCDcCBiC@u@?g@@}@BiCBmA?YBoA@c@@]HcCBs@Bk@FmAF{@Do@HeAH}@LoAFs@Ho@LcANcANiA?AHk@N_AZ{B\\aC`@uCf@iDBS`@qCd@}Cd@kD`@{CTiBFu@Dk@Da@@[Di@Dw@@UB_@B{@@g@@]@q@?i@?i@?s@?i@AsA?_@?OAaC?iAA{B?{@?oB?Y?gBAwBAoB?Q?[A{B?SA}@?a@?o@AcAAyB?k@?CAoF?OCaICaG?Y?m@AM?a@?w@?gCAa@?}@Ao@?aBCeE?sCAkBEsBAw@C{@GqAAi@Eo@SmCI}@Gu@Ea@EYOoAMw@Ks@QqAWsAI[UmAMk@CGk@}BaA{De@iBQs@c@eBuCaLQq@S{@]oA[mAa@cB_@yAi@yBk@yBq@gC[mASy@Mi@e@iBYeAMg@k@{BQs@K_@CIU_A[oAK]YgACMWaAo@iCWeAOs@Q{@Km@Ke@Ks@UuAKw@EWCUK{@Iu@MsAKsAEw@Eo@GeAIaCE_CCqB@mB@wA@aABm@@i@Bq@Bq@@KDeAF{@Do@Dk@Fi@?ADi@?AD_@D_@Hm@D]?GJo@Jq@?ENgARuATuAJu@PqAPoARuAL{@Js@TaBXoB@MDULqALiAJiAHiA?KB]@WBc@FqA@u@?S@iA@q@@_A?iA?s@?s@@kB?{@@}B?kB@kB?A?eD@sB?A@cD?oD?wA?o@?yC@oB?y@?aB@oB?[?C@_C?iB?e@?I@cD?oB?yB@_D?mC@sC?mC@}C?_B?}@@wA?qA?aA?w@@{F?yA@gB@yB?sB?iB?I@wB?kB?C@yA?wA?iD@oA?}A@sB?wA?oB@aA?U?Y?y@C}AAo@Ay@EeACo@AEI}AEk@Eq@O{AQqAKaAOcAM}@Is@Ks@E]Gc@Gi@Gc@a@wC]mCIk@Im@Gc@MeAIeASgCIuAGmAGwA?QA[Ae@CmAA_B?[?g@?G@aBBmB@]?YFyAHcBLgBDu@Hy@NuAH}@RiB\\cDVsBVeCJcABQPwAH}@J_A?CHmAHsABaADcABwA@o@?g@?sA?}@CwAC{AEw@Eu@GmAGqAGwAGcAAOE}@GmAIyAMcC]uGEm@EoAE}@i@qKUkEg@sJi@qKMoCKiBGqAE_AGoDC{CKyJGgII_HI}JCoDAgAAw@?o@E_EDoDLeEBc@FmAD_@@M@KFu@Hy@BOFg@PsAJy@DWRmAJw@Lw@Ju@RuAPoAF[Fe@P}AFe@BWDY@Y@OB[H_A@UDaAFcBDqBBsCAu@AkEA_ACaE?s@AwBAc@?sA?WCiCAyDCyBA}DAmBIoFAa@?IAYAY?EAi@E}AEyACe@?ECs@GmACs@OqCC_@GaAEy@Eu@ImAGqAG}@EcAMsBIiBQmDImAKyBGiACy@GsBG_CCeCCwB?eB@}B@u@@cADgCFsB@a@Bu@HcBDs@?OHwADg@Bc@LiBNiBN{A?KFm@D_@BW@QBK@ULoAB_@LsAb@eFBYX_DN_B^}EBc@HuADwADsB?qA?y@?y@?s@AKAi@?KCy@A]A]AYAYC]C_@Ew@KqAEa@Iw@E]OkAM}@SoASoAM{@Ms@EYG[G]EUM{@Mw@QaAIg@UwASoA[oBSoA[kB[iBSqAG[M{@UoASoAAGKq@Mu@Ks@G_@EWE[CYAEKu@Iy@MoAC]C[C[E_@AYCYCc@Ew@E}@AWCw@CuAAY?AA{@AsB@oA@y@?Q@i@?EBsADsADw@Ba@Bq@JwAFw@H}@Hu@D[Hu@Jy@Jw@DYPeAd@uCdB{Jt@mEBKn@sD@CtAeI~AkJ~B}MHe@d@mCn@uDd@kCTsAn@wD~@sFj@}CN{@Ly@ZgB^oB\\qBLy@b@cCj@aDZiBNy@ZoB@E^uBZkBHc@\\qB`@cCPeA@GFa@PsANoANsAFk@Fm@NmBJuAFaAHkBFeBBs@DsANkFNwFJwD@QHgD@o@B_A@Y@YDq@HkAB]D_@Hu@De@Fe@Jq@Jm@Lk@D[Li@Ji@Lg@FWRy@Rq@Vy@b@qAf@oAd@eA`@_AxAkCjAyBv@yA\\m@f@aA|AwCfAqB`@u@Vk@@AZq@d@iAb@aAZ{@L[ZcANm@Ty@Ni@R{@Je@No@Nw@FYF_@TsAL}@NeALqAJiAH}@JcBDs@@e@DsA@}@B}@@cA?cBBqKB{M@gC?wB@U?sC?S?o@?Q@}B@mBAoA?UAu@AmAA}@AWCg@Ao@GsAE_AGmAEy@OmBGy@I}@YgCOmAE[EUAICUMw@EYG]Km@Q_A]kBEUG[{@wE]eBCK]kBw@eEAG[_B_AeFi@sCUmAUmASmAWwAMi@g@qCI_@w@aEuAkHw@gEc@_CsAgHs@qD}@_Fo@iDSmACUOeAS}AMkAGm@Q}BGcAEi@A[GsAEoAEaCGsD?MKyGCmCEmCEkCKgHC}BIwFGaE?UCqAAeB?gB?W?K@e@@c@BaADgADo@Du@Dm@LsAFk@Fi@Hi@RsAX_BXwATgAbBgIv@wDvC}N\\_BVoAf@eCt@qDpAmGHa@Lq@Py@Nm@V}@VaA\\eARk@Pe@Vo@Xo@^y@Ta@N[Tc@P[h@{@b@m@d@q@r@gA|BeDvCkEzBcDj@y@^m@Xg@^m@Zm@Vi@LWLYb@eAVq@Vo@Tq@HWFS`@uARy@No@Li@H_@Fa@ToAN{@Hu@Ho@Hy@NuAb@eE`AmJp@yGXkCX{Ch@}Ej@uFHaAb@}Dn@uG@AFk@TaCPeBFe@T}BLiADi@PyALwA@GXeCHq@RsAT{ARkATkAVqAj@eCZuAr@uCb@iBl@gCj@}BJc@|@sDF[t@yC^_Bf@qBb@gBl@_C\\kAn@yBj@oBr@uB^mApA}DDMRo@l@kBh@eB`@oA^kAPq@T{@XeARw@FYVcAVqALo@DQReATuADSRsAj@qDl@}DfBmLlAcIb@yCLs@r@wED[RmAHq@Jo@PiAHk@F_@DYNiALoAHiABa@Bc@Bw@DeB@}@?g@?]?s@CeBEaBEuAUiJKsD?]A[A[A]?WAYA[A]?QA[A]A[?]?w@?o@?]?[@QBqAHoBHyAHaAZuCL{@Lq@BSBMBOXuAzFc[b@_Cd@kCP{@D[FYBOBKTqA@??ADWF[F[DYDU@EDYF[D[DYD[D[B[D[B]B[@[B[@]@[?[@]?[?[?]?[A]A]AYA_@AU?EA[AO?MC[A[AQAU?QA]A[AA?AAY?OAKA[C[A]A]AQ?A?GA]?CAWC[A]A[A]?[AU?C?C?]?[A]?[@Y?C?[@]?[@]@[@[@]B]@[B[B]B[@[D]^gEL_B`CmXLqAJqAfAcMB[D[B[B[B[@]@]@C@W@]@uA?[?]A[?]A[A[C]C[A[C[E[E[C[G[E[GYG[GYG[GYIYIWI[KWIWKYKWKWKUMWMUMUMUMUOSMSOUOQQSOQOQGEIKQOQQQOu@m@A?yBaBk@a@gA{@c@]WQ_BoAyGcF_CcBkBuAoB{AQMQOSOQOOQQOKKEEOSECIMOQAAOQMUQUKSOUMUMUKWMWKUKWKYKWIYIWIYI[GWI[G[GYG[EYeAqGk@qDm@sDyBiN}AwJMs@Mu@SqAoA}HkAwH}DsVE[GYE[GYG[G[GYI]CI]uAQq@Og@_@iA]}@_BgEYw@Ma@Qa@a@iAWu@a@wAYgAIg@Ie@My@Gm@I{@A]C[A]A[?]A]?[?]?[@G?U?[HoDFyDBgA?[@]@w@?E?W@]?[?[A]?[A[?]A[A]A[CYGwAC[C[Ei@Gk@EYE[E[E[E[EYG[E[GYG[E[GYUoAyOg{@WkAGYMi@U_ACICOIYIYIYIWIYIYKYIWIYKYIWKWKWKYAEa@aAKWKWKUKU?AMWMWKUMUMWMUMUMUMWi@_AOUMSOUMSOSMS[c@iA_BoAeBYa@gDwEMSOSOSOSMSOSOSMUOSMUMSOUKS]m@IOCEMUMUQ]Ue@KUMWKWMYWk@KWKWKWKWIWKYKWIYKWIYK[IUIWIYIYGWI[IYIYGYIYGYGYG[GYG[IYEYG[GYE[G[EYE[G[E[EYE]E[CYE[C[E[C[E[C[C]C[C[C[A[C[C]A[A[Ey@A[A[A]A[?[A_@?YAY?_@?[?]?[A]@[?[?]?[@[@]?[@]@[@]@[B[?M@M@]@[B[B[@]B[B[B[B[B[D]B_@DWB[D]DYB[Ju@RuADWF[D[FYLu@FYF[HYF[FYFYHYF[HW\\mAPs@HYJYHWHYJWbAsCd@gA|@qB~A_D`CoEb@y@nFcK`AiBdAuBbAoBVc@bAoBbAmBbAoBbAkBbAmBbGcLLUJWJULWDKDKJUJYHUJYJWHY@CFQHYHWDOBGH[HYFYFYHYFYFYFYD[FYD[F[DYD[D[D[BYD[B]B[BYB[B[B[@[@[B]@[@[@[?]?I@Q?[?A?[?[?[?[?]A[?S?GA[?KAOA]A[C[A]C[A[C[C[C[E[C[?AEYCSAGE[EYE[EYG[E[GYG[GYGYGYGYIYKc@Og@IYIYIWKYIWKWKWKWIWMWKUKWMWIOAEQ_@aAsBgA_Cw@cBeR_a@?AUe@?Ac@_AMWKUUk@ACMWCIEMKYKWIYKWCIEOIYIYSs@AEGSGYI[CMCKGYG[EUACG]AKAAAKG[?CEWE[EYEYE_@?AEYCS?GE[E[C]CYC]E[C[C[?AC[AO?AAIA]KuAA]A[C]A[Cy@A]A[A]A[A]?[A]?O?KAy@Ay@?_@?[?]?[?[@]?[@{@?[@]@[@]?[@[B]@]@[@]@[B]@[B]B[@YB_@B[B[B]Fw@B[D]@I@QD[B[D[B]D[DYD]D[D[D[F[D[D]FY?ADWF[F[DYF[F[FYF[FWF]F[Ps@HYF[HYFYHYHYRu@HWHYHYHYJYHYHWJYDO@CL]JWHYb@gAJYJWJYLUd@gAJUJWLWJULWhGwLVe@bBeDxAsClA}BbAoBpAeCDGrB_ElBsDvBeErB{D`@{@b@_ATm@Xs@To@h@wBj@yBRiAPiAJu@NyAJqAFcABs@@e@@k@B}@?o@?CA]KqCSkFC_@IkBKsBMuBMaCIaBEoAA_@A{@?c@@kA@}@By@Bi@Dm@Ba@BULuAJoAN}AJoAPiBB_@BMLwANcBFm@Fm@@QLkAL}ADa@LsAXaDXcDVuCLsAJiATaCFi@Fo@TgCRyBPqBFg@LyARyB@M@GVqCVuCB]@ADe@@GDe@?GBORcCHmA@SBg@@e@?E@a@?M?O?U?M?q@Aq@Cq@Ac@AA?OCa@COAQCUCWIs@CYG[UqAKg@Mg@]oAQk@M[KYWm@Ym@MUKUEIS]GKU_@AAS]IKOU]e@ACW]SWAAa@g@SWKKa@c@c@c@u@u@e@a@_@]e@a@c@_@e@c@q@k@s@o@SQECaByAOKa@_@{@u@a@]m@k@yBoB}@y@i@c@EEYU{BmB_Aw@w@q@UQ{AsAcDqCgB_Bk@i@CAMQY_@KKk@m@_AoAw@oAAA}@eBkAeCa@aAM]c@uAm@gCi@mCSuAa@aD_BgQSsBEYEOG[?AO{@Q_ASgAOu@UaA[oAM_@I]IWOg@Ws@[y@Wo@g@qAIQWo@i@qA_@}@Yq@M[Wm@M[Wm@Si@Wu@EKe@qAg@qBi@gCOw@G]Ee@KaAE]K_AG_AAOCUAU?AAWEg@Ag@AM?OCeA?u@AY?a@?S@[@y@@y@Bo@?IBe@@SB_@BY?IBYBYBYH{@Hq@?C?AHk@BMJs@Ls@Lw@Pu@ZqA?AZgANi@X}@L[h@uAFORe@Zo@|@kBx@aBHQJSt@{At@_BRi@FKTm@j@iBPq@VmANy@Ju@Jy@H{@D}@Dk@@c@B}@?_@?C?k@A{@Aa@Cw@ASEo@Ek@Iw@Iu@Ks@c@aDEWUcBSqAYsBQoAOiAMiAEa@Eg@Cc@Eg@Ek@Co@Eg@E{A?ACo@Aw@AaB?e@?o@?M@}A@a@@g@?GD}@Bq@D{@HkAJyANeBJmA?GDg@LyAFu@n@iL^gDn@}FDc@j@aHJsANuBDk@De@Bo@@QB[Bo@@GD}ADiABqA@aABqA?q@?yB?k@Ae@AiACoACs@?AAo@?CGwA?AAo@Ae@AIGcCAIAo@EqAC{@EsAIsC?GCm@E_BAe@K_DAg@AYA}@AoAAy@?iA?eA@oB@g@?CBwAB_A@_@FsA@Q?ODq@Dw@LuBHaAFo@Fw@N{Ad@mD\\sCXyBTkBVsBXyBJ_AhAcJt@_G@GFm@TcBNkA@GVgBFa@Jk@BSFYBOD]BGJo@Ha@F[Ny@TgATgAb@iBDOBOHYHWPy@v@{CjAoELi@jAoE@GNk@FW\\uAV}@Nk@FYv@uCj@sBJ_@vCsKDMrAwET{@HU~@_Dl@yB~@gDdA{Dh@wBp@sC`@}ADQBKRs@ViADO`@}Af@qBd@oB^eB@GLs@NcAJu@F[D_@Dc@NyA@K?ADo@@OHmADsABc@@o@@U?S@oA?u@@uC?{E?mAD}K@yD?wC@mC@yD?{B@{D@eC@wE@iF?}B@m@?A?m@?gA@_A@q@@e@HoBFgAB_@B[VsCLw@N_Ab@aCH]`@cBl@qB@AbAqCb@_ATi@\\q@@ALU@CFIJOXc@`@g@JMd@i@r@y@zAcBnD}DvCcDv@_AJMX]NSn@{@T_@T_@Zk@Zk@Zo@Xm@Xo@Tk@Vs@Ts@@ANi@BIJ_@Pm@ZoANu@Nu@Lw@Lw@NsANsABYF}@B]Ds@D_ABuA@]?w@?s@?aAAsAAsC?sB?KAo@?]AqB?]AiA?oBAy@?W?c@AcD?{@AqA?[@}@@y@@u@B_ABy@HsADo@?GF{@PqBJuALsAJwAPqBFw@Dm@De@LwAPsBDu@Hy@LwAHeADi@PsBRkCRqCLuAJsAJoBD{ABs@?a@@u@?]?m@AkAAu@A_@C]Cy@Gy@Gy@Gu@Iu@K}@E[Ga@Km@Oy@Q{@]cBI_@Mm@G]i@gCOw@Qu@g@eCq@cDg@eCm@uCS_AKg@SaAWsAOy@CIQeAQsAKs@K{@Iy@Ei@Ei@Gy@Ey@Ey@Cy@Co@CaAEqCEiDAEGgF?GEeCEuBEsBCwBEsBEqCCsBGoCCsBEsBEmDGoCCuBGkDAq@CaBEkC?EEsBEkCGqDAs@?_@CwB?uA?qA?a@?y@@y@@yABuABuA@aA?UDqC@wABsBDqCDmCBsCFmDDkE?G@o@ByADmD?UDwCBeC@g@DmDDqCBsBDqCBuADaD@sA@m@Bw@Bs@D_A@QBg@B]Fw@JiAJaAJw@Jw@Lu@Ls@Nu@XsAPs@Pq@J[Rq@HUTq@J[Vq@d@iAXm@DKRa@Xm@Zi@NWh@}@FIVc@Zi@|AeCb@s@d@u@Xe@Zi@^k@\\k@LULUNUXk@LWLWTe@HOFOJWXo@`@eAVs@\\cAX{@ZiAZqAPu@H[Lo@F_@Je@DWJm@Jo@F_@LgAHk@B_@D[BYDe@Fq@Dw@Fy@@YB_@Bw@B{@By@@_A?s@?iA@eC?mC@oC?gB@gK?mC?a@?mB?o@@oC?{A?{A?mC?o@@mR?]AqC?M?OA_@CoAA}@A[IcBCk@Cs@KcBGw@Eq@Ee@Iw@Ea@SmBIs@E_@Im@e@uDSwAUgBKu@[eCGc@_AmHWsB_@oCk@mEk@sEOeAS_BSwACUc@iDGc@OkAWkB]oCIg@_@yCi@cESuAEUMy@Mm@Ki@GYOo@Su@Ss@Qo@Wq@K[M[KWSi@MYO[GKWi@GKMWMUOWMUOUKOQY]e@OSQSMSOQQQOSQSOOQQSU[YUUc@a@c@a@a@a@c@_@{AwAq@o@_GmFgAcA[YsBmBw@s@s@q@SSQQa@c@_@e@KMCCQSOS_@g@o@}@KQQW]i@Yg@AC]k@g@cA[q@KSISISO[Uk@Ws@a@iAQg@Qk@Oi@IYUy@Oq@Mi@CKOq@Oy@Ow@_@gCS}AAMOwAQoBKaACUMoAOyAQoBO}Ai@yFYmCk@aGWmCSsBc@qECWQgBU_CKgASmBGq@KgAMgAEi@KgAASAKKoAG}@KwAEu@I{ACu@GyACu@Cy@Cu@A}@Ay@A{@A{@AoA?}@?w@?uA@_A?U@kA@MBwAFqCBc@?ABm@By@Dy@Dy@@OBi@F{@Du@B_@B]JoAH}@J}@@SJcAPaBJs@Da@XoBL{@D_@F_@DQRqARqA`DwRHm@pA}HTyAr@oETqARqAJq@Lq@BO|@wF^_C@Gd@kCh@_Dh@iDbAkGNeAF_AZiFF}C@mBIkEIaCOqBYkCOqA{BcNo@kEkBeLWaBc@qD_@cE[eGGgDFwC?K?{@?_A@_A?ODqB?IDkAFsALuBBUDy@Hu@LqALaAXyBL{@RmAr@wDr@wDh@}CLk@BOx@sEhAmG|@_F|@_FZcB`@}Bt@eEj@_D?Cv@mE`@oCZwB^oCZgCZoCVmCPkBDa@RmC@KR}CB]HqAPmDB[FyAJ{BV{EHwAPkCZgETkC\\gD\\mDZ}CXwCf@{EDa@j@_GPcB~@oJFm@^{DjAkLf@aFFs@b@eEBYFm@BQRqBVmCd@qETwBNyAZmCHm@PaBPuADYBUd@wDFm@DYh@kEFm@J{@X}Bd@wDJu@Fe@VsBNcAXoBf@aDb@gCl@eDx@}DJi@VeA`@iBBIZsALc@Lk@@A|@gDNi@Nk@j@mBVw@?APi@j@iBFSPg@fAaDp@uBjAoDX}@l@iBVy@b@{Aj@yBVcAVgA\\_B\\gBXeBPgALu@PgATmBVwBRmBN}Af@iFFw@FgADu@@QDm@?AH_BHmCF}AByA@kB@}A?{A?C?u@?yAA}AAgFCmFA_D?AAmC?CAsCAuA@_BCqEA}@?E?{@A_F@gADgCDwADi@FcAJkALqAHs@BOLeABYN_ARkALu@^iBRy@VcA^uAVy@X_ATu@ZeAPm@Ty@Tw@Je@Nw@Je@Fa@LkAB]@Q@IBW?K@K@o@BaABwA@W@Y@y@?e@Bw@?e@@G@aA@k@@Y?O@}@AQ?e@?I?i@?E?WAW?MCYCo@Gi@Cc@M{@AIIi@UeAG[c@_BWq@_@_ASa@IOo@mA]o@iAuBYm@Sa@Qa@IYSk@M_@I[IYI[QaAIe@Gc@Is@Iw@Ew@A[AYCcA?u@@q@BcADeAJ_B^_HNcCBm@Do@NoCP}CReDP{CHeBH{ADw@HkAFeAFeADg@HmALsAHgANeBf@cF?C\\}CB[VgCHeAXuCHo@XsC?C`@_ERkBLqAJiARgBRqBBYLcBDi@Dy@FeBBo@?M?[@o@?s@?k@AgAAe@As@GiA?EE_AEi@Ei@Gs@Iw@Kw@Ik@Ku@ACKk@?ASiAg@}BUeA_@cB[wASeAACMw@W_BSyAIs@Iq@G}@Gw@IiAEs@Cq@E}@Ac@Ay@Aw@Aa@?]?w@?e@?S@w@@e@@o@Bo@?WJeD@o@@c@FkB@m@FeCHoCJeE@aA@]?]?Q?[A_ACgBS}EKeAIy@Is@Is@_@mCSqA[{BIm@QoAGk@Gi@Iw@E]CYCe@Co@A]A]AY?]?[?y@@y@@Y@_@Ds@?CDa@?IFg@BYD_@Jw@F[?ALk@@GHc@DQPs@Rs@To@Ri@BIVm@Xm@NWJUBCHMLSNW^k@^e@`@g@NQZ_@DEp@y@p@w@l@s@r@{@`@e@^e@`@e@p@w@^c@p@y@`@e@`@e@^e@`@e@`@e@`@e@^c@^e@`@e@n@u@r@y@^e@`@c@`@c@b@e@`@a@`@c@b@a@b@a@b@_@b@a@b@_@b@_@d@_@b@_@d@]b@]NINMdAs@dAs@~@k@NKf@Yx@c@@A|@e@d@Uf@WTKPIf@Uh@Ub@QVKRI`@O|@[j@Sz@Yz@W|@WvRcF~Cy@tBi@hCs@B?lAa@pAg@lAm@`Ak@x@i@|@o@bA}@dAeA|@aAn@{@TWZg@n@aAx@{A`@u@n@yAb@gAXu@tAiE@GdAgDnA{DfByFlAyDx@mCt@wCt@mD@Gf@{CZ{Bf@gEb@aDFe@Lo@Jo@R{@Li@Nk@DSHYFQTw@`@iAVo@Zu@Rc@Vk@h@aAj@eA|@{Av@uAr@mAn@gAt@qAbBuC|AoClBeDBGLSRa@b@_A^{@Xu@To@Tw@^mAFUDUd@{BD[XoBXkCLeCFqC?oA?}@A{@MyCGq@]iD]wBGYG]WeAWaAOm@Qi@M]{@}BEKq@aBYm@oCmGg@iAkAkCaBuDqIyRGMwEqKsCqGO_@qCmGACIQKWEIKWe@gAmAoCCGSe@Wm@k@yAa@cAm@eBs@}B_@oAQq@e@gBU{@}EwRmAaFa@{AESU}@S_A[mAAE[kAQw@A?Qs@Qs@Qq@YkA[qAe@iBk@}Ba@_B[oAc@iBg@mBm@cCa@cBCE_@}A[qA[mA?AMi@AGOu@Qu@Oy@Mu@Ow@SqA[aCMaAK{@MmAMuAIaAEs@Em@Eo@AOEy@E_ACm@EoAC_AAy@Cw@?k@?k@Aw@?wBFeKFoIH}M?o@@}A?o@@o@BoFB}D@o@BuFDaF@}B@_CDmGBoE@_BD}G@_DBoD?o@@m@@gA?iA@sA@_BLkR?aALuTJqPHmPFeIPc]@wA@sA@_A?A@wC@mB?S?CBoC@mCD_HBmCDwBDgBDaAFsADu@HyAF}@PqD\\sG\\yGbAkRpAoVXkFb@kInAsUZ{FHgBJgBVuE@k@Be@@]@]?u@?q@?g@AS?EAa@Cs@C_@Ca@C_@AEC]Ge@Ku@M_AMm@Qu@Qq@]iAUs@Wq@m@aBcAuCuBuF}AkEy@yBw@wBcIqTeD_JWs@ACQc@gA{Ci@wAQg@kAaDM]m@aBUm@Us@Us@Sq@Sq@[mAOm@Ka@WmAWqAUqAMs@SsAGa@OiAIw@Is@Ca@Iy@?AEm@C_@Ea@A]C[AWCa@AWA]Cq@C}@A[?]Cy@?K?m@AoA@_A?_A@]@e@@i@@]@]Bu@Bu@@_@B[Bg@Dm@Fy@B_@Dc@Fm@Dc@Hs@Hq@Jy@Jy@RoAJi@BOLs@Nq@Nu@Nu@TaADQVgAZoAXoAn@oCBMH[`@iBd@qBVgAn@qCBMt@}CZqAXoArCaM\\yAVeAtAeGb@iBLk@Le@^cBb@iBDQZyAt@{Cd@yB`AcEvAeG\\}AnBoId@wBh@{Bh@{Bx@mDx@oDtAeGpAqFDSDO@GBGjBkIdBqHpAsFBKPw@DSZoABMnBoINq@\\yAVkA?Cb@eCVmBLeAHs@BSJiAHeALuB`@{HH{AJ}ANsCRoDB_@JqBJuB?S@ABo@?MBy@Bw@B{@?]@s@@]?_@?_@?M?A?c@?I?Y?wB?CCiBEuBGgBCm@?AGeCS}G]uKEkAUmHQsGI_CEqAOeFSgGIoCEyACwACy@?u@?m@?M?_@?[@]@s@Ba@@_@@[Ba@@QB_@B]@WH{@Fq@LeADUXmBLq@@G`@iBtG_XtDgO`@cBf@mBXmA`@aBb@gB|@mDLk@\\uAFUd@iBNk@`@uAx@}CBKLe@Rs@HYdBqGBKJ]nAuENk@Ni@n@aCT{@x@wCH]DMt@oC~AcGpAqFLk@BIXmAh@cC~@cEj@aCtFgVf@}B^}Az@qDJg@fAyEx@oDJe@`AwEdAqFt@}Dr@aENw@|@_FDUFWn@oD?Cn@eDPcAbBeJ\\oB|@_F^qBr@uDl@iDl@cDh@{CBEFc@@GBOJi@bBcJBQx@mEj@_Dj@_DdAwFJk@N}@TgAPaALw@b@cCf@iC@ITmABO^mBTsAFYl@gDx@qENy@hB_Kl@cD\\kBP}@XaBJk@BIrAmHJm@He@ToAP}@Hc@BKz@{EHe@X{Ad@iCFY@KJk@Lw@RwADWBOFi@Ju@Hw@Hy@BWD_@B[D[@YBYDa@B[B]Dy@@YB[@[B_@@O?E@]Ba@@Y@_@@}@@C?QBuBBwA?I?C@iA@aA?C?O@y@BoB?CLoMHsKFeFDmEBkDBoCx@}z@F_GBqDByBBuC@q@DiEDoCDeC@u@@o@F}BLwEf@_RHmDLsEJ{DHuCf@mRL_EJ_EFoCL_E\\qMBoA@i@@kA@yBAoAAkACaCCmAG{AEqAOgCMgBQ}CIyAImAG_AE{@QiCKyAKqBImAMyBSeD_@eGUmDMwBMoBm@{JOiCAKOgCg@mIQiCw@kMqAgTMuBQuCMiBEu@Gy@I}@KoAGm@S_CWkCOsAIw@OuAQoBYkCa@cEOwAYkCGy@Gy@AOEs@GgACc@EoAE{AAcB?KAs@?aA?i@?i@@Y?U@W?O@k@@k@Bw@@_@Du@@g@Bm@HuBLmCB{@NiD@a@FsA?IFkAFqB@W?EBw@?G@k@@eA@aA?K?_@?}@?WA{AAw@A{@EoBCeAE_A?IGsAC_@IsAIgAAQMoAI}@CYWqCQmBa@iEa@cEWmC[gDOmBEm@IeBIsBCu@A_@?OAu@AgA?y@?E@qB@wADsBDeAFgAFgAHiADu@Hw@Hw@H{@PqAd@gDXmBDYRsAZoBRsA\\}B@CHk@Hm@ZoBRsAr@{E`AqGhAwHJk@?Ar@}E@C`AqGHm@He@XkBLw@FWNy@VqANs@Pw@XmAT}@Ng@Rs@Rs@Ty@\\eA^eA@ETm@Vu@d@gAb@gAp@yAh@gAf@cAXi@LUl@cAZi@j@_AZe@`@k@^i@|@mARWb@i@X[`@g@bAkA^c@b@i@^a@LOTSLONQ`@i@p@y@rA}AnB}BLOVYb@g@l@s@b@g@rA_BVYl@s@\\_@r@{@zCoDh@o@n@u@dAmAp@w@X]f@k@LO@A`@g@b@e@~AkBlDcEzAgBHKX[@ATWdDyDzLqN`AmA\\_@x@_ATUX]^e@~AiBt@}@p@y@RSd@k@l@s@z@cAVYb@i@Z]dBqB|@gA^c@f@k@zAiB`AmAp@y@`AqAb@k@n@{@FIPUT]X_@h@u@p@cAn@y@R]Xa@v@iAfA_Bz@oA~@oAj@y@TYNWrGkJX_@nDgFhIqLhIsL`DsEp@aAhCsDhCwDd@q@xB}CVa@NS`@k@lAeBzFmI~@qAv@iA|@uA`@o@Xe@x@wAv@yAf@cA^y@Rc@^{@Tg@N]Ri@Xw@^eAL[`AuCb@iATq@JW^iAdAwCj@aBRi@L_@To@`@gA`@mAb@kAVo@Xo@x@kBRe@Rc@Xm@^s@h@cA\\m@Va@^o@`@k@Zi@\\e@Xa@RYh@u@JMX]pA_Bb@i@^c@lA}Af@m@X_@h@o@X_@l@s@RWn@y@d@i@\\e@j@s@TY\\a@NSRU\\c@`@g@^e@Za@d@k@X]v@aA^e@j@s@Z_@bBuBr@}@`AmAb@i@l@u@f@m@^g@Za@X_@T]R]Va@LWLU^w@Re@L]\\cAZkANo@P_ATqANsAHu@D_AFiA@q@?mAAqACcAEcAG_AI{AgAuQEoA?AAM?[A]AqA?e@?W@e@?C?g@@U@]@g@Dw@Dw@Bc@@QBYFu@Fg@Hu@Fe@?CHg@F]ToANu@FYDUH]d@iB~@}DpFkUnAoFjA{EdBmH?APs@XkAr@_Db@gBH[ZsAj@cC`@cBb@kBd@kBvAeGH_@`@cBl@eCl@eCj@cCl@eCb@kB`@cBb@kB~@yDt@_Db@gBb@kB`@eBPq@l@gCb@iBPw@XmABILi@l@eCt@{Cr@{CjAcFd@mBXiALk@`@cB^}ANm@XmAH[XiAPs@Tw@f@cBbA}C`@eA@EZy@d@iAf@kAh@kAP]b@}@x@{AR]r@kAxAcC`BgCnCmEv@oA~AeCBGx@qAd@s@~@{AtAyBFIpAsBx@uAbBkC`DgFxA_CtBgDj@}@p@eAJQn@cAtA{B`BkCVa@p@eAjDsFLSrD}Fz@uAjB{ChE}GVc@lAkBj@aAXc@LUrAsBx@{A`@w@Pc@N_@JUHWHUJ[FWHYPq@FYH]F[DWFa@D[DYD[Fi@@WHgABa@@q@?{DAs@CqAEmBU_JCs@AeAGwBI{CMyEKmDEqBMeEEsBEeBEgBCoAIuCAuAAkA?E@w@@}@?]@]Du@@]@QBg@Di@De@Hw@@YFc@L{@D_@ZoBBKXkBXgB@ATyAh@eDXyAPaAZuBPoA@IT{ARyAj@uD^_C`@aCZsBDQBSLm@Hc@Le@XiA@GJ[Pg@Rk@LYXo@Vk@NWZk@l@{@`@k@p@u@bAiAPSpAwAf@i@\\_@bAgAdAiAp@q@FGZ[r@m@f@e@~BsBjAgAHGRS^_@t@u@p@u@f@o@j@s@\\g@b@m@Xa@lAgB~@qA~AyBn@y@^c@`@c@r@s@bAeAxB{BvAwAfAgAz@}@HIbAcAX[VY^g@FGV_@\\i@NWTa@R_@LWJYJULYJYHSJ]J[Nk@FWPw@Lq@Hg@F]DYBQD[JoABe@Dy@Bg@@i@@eAB}CB_D@uD?g@BqC@mADkGDuG@gB?Q?m@B_E?QB{B?o@B}D?A@oA@}@?o@BqEBaCBqAFsAF}@Bm@DSDu@B_@NiAD]b@kCTiAVgAz@sDLi@Lk@xAmGPu@Ps@x@qDxBiJv@eDBILi@d@cC`AwDPq@H_@J[FURs@HUf@_Bf@uAX{@j@wAdBsEz@yBTo@dAoC|@aCPg@JUj@_B`@mARq@Ne@@CRu@f@kB`@}AXsA^iB\\gBV_BHk@RqANqABSL_ALsALsA?CNmBLoBH}AFoBFiCDwB@qBBmE?qABiEBeFBmE?kA@eBBmD@gB@oBBcHDyH@iB@aCB}GD}GBmFBmF@o@@yA?}BHqQD}GB{GB}GJqS?I?a@@a@?mAB{B?{@@iA@mA@y@Dq@B}@Fw@Fw@Fs@Di@Hm@Da@Hk@Hi@Lq@Ji@Hc@H]Jc@Jc@Ja@Ja@Pi@Tu@\\aAN]Tk@Pa@Re@h@eALWZi@DGFKR[b@m@R[TY^e@l@w@f@k@j@s@f@o@VYnA}Ar@{@t@_A@Av@_AzAkBj@q@`AkA|AkB^e@`@e@dC{Ch@q@fAqAJMf@o@|AmBBC^c@fAuAb@g@hAuADGf@o@vAcBPSvCqDjDcEpCiDHKdAoAbBsBb@k@jB}BZ_@dAsAb@i@Z]b@i@r@}@`AkAl@u@`@e@j@u@n@y@\\g@Xa@BGLS^k@Zk@Zk@JSP]P_@Te@Ti@N_@FOb@gATq@HUJYTq@Ru@Rs@Ps@Ps@P{@Nu@Nq@Lw@Ju@Lu@Ju@Hw@J_AFq@Fu@Fy@FuAD}@Bo@B}@@}A@kB?AA}BE_BA_@Cc@Cg@?CGgAIoBI{AEs@IaBMeCMkCIeBOiCCq@O}CQaDOcDMcCOwCM}B}@wQM}BWiFWiFUcEKqBKuBKoB?MKiBKsBKqBCg@GgAMiCEaAImACk@O_DGqAKaBCk@?CIyAMkCGwACWKqBGwAKsBAWCk@Am@Ck@AaAC_AAy@?e@?S?w@?}@?{@@y@@q@@aA?IBk@@y@By@D_AFgAH}AF{@Fm@@UDg@LqAD_@Da@Hs@Hs@Jw@DWD]RoANaANy@RgA@CF]ViAHa@DSPu@Ja@XeA\\wAb@aBd@gBNk@p@iCb@eB\\uAV_AfBcHBIt@sCZoAhAmEjC}J\\sAl@aCd@eBVeArFaTBMBIx@aDd@gBv@yC?Cd@gBZmAx@}Cd@iBVaANk@DQd@kB\\mAZmAXmAZqANs@VqAVqALw@Lu@BSTyAJy@L}@Dc@Fg@Hw@D]Fq@Ba@Hy@Fy@HsADy@FwABo@@e@Bw@DuABiA@gA?mA?_BAy@?iAMyECi@CgAGsBE_BASEsAGyBIiCIwCEiBEyAUsGG{BO{FEaBMyEASMiFCs@IkCGmCAi@Ci@YeJU_IGeCK_EGiCCaAIqCMmEU{GCqAC{ACe@CyC@{B?O@iB@m@BsA@[@]D{@Bs@?CBk@@MDu@HuAF{@@UH{@Hy@Dg@JeAJy@Ju@Jw@Jw@Lu@RqATqANs@Nu@Nu@Pu@Ps@DMLk@FSd@eBRo@Ni@BK`@kANc@Z_Al@aBVo@l@_BXy@Ri@x@yBdAqCx@yBpAiDpAmDr@oBXu@dAuCZw@ZcANg@BKPq@Nk@DWH[BOFYLs@RkANgA@QD[Da@Fq@De@Do@Du@Dy@Ba@@s@B{@DiCBuBBuADuABgB?I@e@BoADmCBw@?GBo@?ADk@Dm@?ABe@Fs@Hy@LeALw@Js@Jg@Jk@TgARy@Rs@Rs@L_@Rk@Tq@Vo@Vo@Xk@Xm@Zk@\\k@\\i@\\i@\\g@PULO`@e@p@w@`@c@DGZ[?AZ]TUDGl@m@p@w@NQZ]h@k@fCoCdBkBrA{AfCoC^a@v@{@LMLObAgAl@o@VYbAgAjAqAZ]LOdAgAtA{An@s@tA{AbAgAbAgArAyAbAgAxBaC`AeAjDwDLOdAgA^c@bAgAjAoAv@{@nBwBPS@CVWBE\\a@`@g@NULSNSNSLULULSLUNUJWLUJSLYLUJWTi@J[LYHWJYHWJYHWHWH[HWFYHYFYH[FYF]F]DWFYDYD[F[BYJy@Hw@D[JsA@[BY@[B]@[B{@@Y?]@[?]?]?]?[?Y?]A[EsAA_@A[C]A[C[CYC]C[Gs@Ea@EYCYE]EYG[EYG]EYEUIa@GYG[IYI[GWIYGYIYIYKYIWIYKWKUIYKWaB{Di@oASe@Sg@Sg@o@yAq@aBCGSe@ISISWm@a@}@e@kA_@{@]{@a@_Ak@uAc@cAYy@Ys@GQIWKYK]GQI]IYIWCKEOIYGWGUAEGYCKCOGWWmAAMo@mDW_BCO[oBAGu@}EGg@AGIe@Ku@SqAMs@WyAIe@Ms@Ms@EWMq@AGESKq@ESGc@AIKm@ACIg@COE]EWOw@E]EYCKG_@EWEYE[EWGYEa@Ks@EYIw@K{@Iw@Gy@Iw@Gw@Gy@E}@Ey@C]A[A[C]A[A[A[A[Aa@?[AYA]?[A]?]?Y?_@A[?[?[?]@w@?]@[?]?]@[?Y@_@?[@]?[@_@?W?]@{@@w@@y@@}@?w@A{@?YA[?IAS?IAQA[C]C]C[Gu@E]E[Kw@WoAEUIa@IY]gAGSAEKWK[KYWk@M[KUe@eAYm@ISUg@EKe@eAe@eAg@gAe@eAYq@g@eAc@cAe@gAYm@KYYk@MYUk@MWMYKWMUKWMWKWKUMWKWKWMWKWIWKUKWAEIUGSAEIWKYI[GYIYGYG[GYGYG[Ik@Ga@G_@C[EYCYC]C[CYA_@C[A[AYA]AY?_@?[?[AY@g@?S@[@a@@Y@Y?G@W@W?CB]@Y@]@C@U@YD_AJ}BLmCBm@@]LsCRgEB}@DuA@]?[@]?]?]?YA[?_@AK?OA]C_@?WCa@C[C[C]E[E_@C[Ga@E[?AG[EWG_@G]Kc@Oq@IYSu@Us@IYWo@Wo@KWMWg@aAOYMUMUOUMQEGIMOSOQQUOQOQQSQQQQQQQMQQQQQOuAsAeCwBkC}BqBcBgBaBmB_BuBmBiBcBiC{BqCeCy@u@eA}@{AsAw@s@}@y@e@c@_@[m@o@sA}Ae@m@QSMSi@w@aAmBSa@k@kAUm@Sk@Yu@_@oAY}@Qs@]}As@gDkAwFmD}Pe@yBe@eCu@aEMw@c@gCSmAKm@k@kDkB}KgBmKYeBi@mC]gBe@yBc@iBe@uBMe@YgAo@kCi@qBK_@Oo@_BgGqFeTm@{BS{@g@iBy@uD]}AAKg@wC[uBCSEY{AaLM{@QqAyAuKS_By@eG[qBa@yBa@sBI_@I[c@iBe@kBaCwIcJu\\a@yA[gAi@sBK]sAaFOi@cG{T_@sAc@aB[iAW_AYgAs@oC]yAkA{EMi@sDeO?AeAcEs@{COi@y@iDg@oBc@cBIY]iAOg@Og@Sk@M[e@sAQe@Sg@k@uAs@}AWm@]q@m@kAUa@s@qAS]a@m@[g@sAsB]a@iAwAm@q@u@}@gByBMO[_@[_@oA}AGIQUQS_GiHeBwBcAmAm@u@e@k@}AkBY_@u@_AkB}B{AiBW[mAyA[c@aCmDIKU]e@y@QYy@yAw@{AMUe@aAs@aBo@{Ao@eBc@mAe@wACMEMk@mBWcACGI]AEQq@Kc@YuAY{ASeAG[O{@Ky@EY[{B?Ea@{CMmAKkAK{AG{@KeBE{AEy@EuAAw@?CAiBCeC?oA@y@B_CBu@@w@NoEBiA@a@VeJR_HLuFBgAD}A@iB?y@?w@?KAmAEaC?QEuBK{B?CMoBGoAGu@K_BSuCOuBEk@OyBAUMeBImAAGMqBMmBKuAGqAE_AC}@?KEkACwA?M?a@AM?sAAw@?C@o@?a@@aB@q@?G@o@?ID{ADuAHuAFiADw@F}@De@De@JmANuANuA@EFm@DWT_BJq@Ly@P}@Jm@FYBQFYNq@\\}AH_@Ni@?Ad@uBBKf@uB`FmTnEqRhB}HdAmEt@{CXiAH_@nBuH|AcG|@kDRw@x@_DT_Af@kBVaAt@uCPs@x@aDlAuEl@{Bb@}A^oAd@yA|@sC^eA`@iAp@kBj@{AZy@Ti@Rg@Zw@^{@FMTg@d@eAd@cAd@cA~@oBv@{A^s@tAkCTc@Xi@bAmBfAsBt@wAjCeFrAgC`B{C|@eB`AiBJUf@aA~@gBh@aAp@kAf@}@rAwBn@cA^m@x@mAhAcBpAkB|@oA~@uAx@kApAkBjAcBlAeBbAwALQp@cAjAcBhA}AdAuAvAiBrAaBhB_CvAgB~BuCbAqAj@w@p@cAr@iAr@oAp@oABI`@{@n@}Az@_C^gAT{@ZgA^aB`@mB\\mBXmBRaBRiBFm@Hq@Fi@Jy@ReBBWLeANyAdByPV{B^sDT{BFo@PyATyBHaAJ_ALkAJiAJ_AVaCPuANqATeBXwBF_@Hm@BONkAHm@@GZ_CBQ\\aCDc@NcA\\eCT_BTiBVkBl@kEBW`@wCD_@PkAVuBTiBVoBJcANwAP{APmBJgAR{BTaCT_Cd@eFb@oE`@iELuANkALcAJo@Fg@Jm@L}@Jk@PaAJi@Ja@Hc@Nu@Ry@TaA\\qA^sAb@wAl@wBn@wBt@gCr@cCj@qBl@uBj@kBZgAn@wBr@gCz@uCt@iCVy@ZgAj@qBd@aBj@iBp@_CXaADQHW\\kAX_Ad@cBr@_Cr@eCd@_BLc@HYFORo@\\cAXu@`@_AN]Ra@P]JSx@uA`@o@b@m@b@m@`@g@h@k@^a@dAaAd@a@\\WTQFE`@Y|@i@v@c@jAg@nBcAh@Wh@Y~BoAvCwAjCqAt@_@tAw@\\Q^Q|@e@b@UnAk@x@a@|CaB^S`@QJGpAo@fB}@|@c@lAo@v@a@BAjAi@nBcAjBaAjAy@x@u@hAy@`@]h@a@b@_@v@m@b@a@b@_@d@c@`@a@r@s@bAeA`@c@`@e@b@e@n@w@NSFGfB_CpAcBpAaBhByBV]nA_BpAaBpAaB~@mAp@y@^g@NQ^g@`@e@^g@^e@`@i@~@kAl@w@LQb@i@`@g@d@m@V_@Zi@NUPYTa@\\o@Vi@@CVm@l@wAXy@L[BI\\kAPm@Lk@TeAZaBNy@L_ALgAJcAHgAFiAF_BBoABu@@y@?i@JkGFgEDiC@_ABsAByA?EBiBDwBBwA@aA@o@?WDwBBwBDoB@kABmABmA@qA@W@}@BoA?I@e@@kABuADoC@[BwB?UB}A@SB{BDmBBwAB{B@aA@_AF}CD}C@u@@UBmABu@B{@FwAHkAJcBFs@Jy@JaARaBF]Ho@Lu@V{AVmANy@XkARy@ZiAV}@Tu@Xy@b@oAb@iAXs@Pa@Xm@N]JWDGl@mArBuDTa@\\m@R]d@{@vAiC^o@rAaC`AgBb@w@Xg@DMf@{@hCuEx@yAP[lE}Hp@oA`AgBZk@\\m@pA}BFMTe@d@_Ad@kAl@_B?Ah@cBb@eB@GNm@V{AVuAJaADYD]@OJgAH_AFiAF{AB}A@y@AaBCcAA{@EcAEs@G{@IsAWsDWeDk@wHMyBSgCUwCMoBK{AGw@Gw@Gy@Ew@G{@KqAEu@KuAKuAKuAKuAKuAIsASoCKqAMqBOsBIqAKwAKuAGw@Gw@G{@IqAG{@Gy@Gu@E_@Gs@Ky@Iu@Gi@AMKy@QqAG]Mu@Mu@UqAMs@I_@GYWkAGWI_@Su@[kACIMi@_@mASo@Y}@Qi@g@sAEQYs@iQcb@qA}CcAcCg@mAMYcB{Dq@}Ai@qASg@}@wBq@cBwA}DWw@_@eA_@mA_@kAa@qAo@wBg@iBo@aC_@}AeC}JmA_Fw@aDUaA[qAIYuA{Fs@qCs@wCk@aCs@sC{@kDeAgEqAkFYmA]uA]wA_@{A[qAc@cBk@_CI]k@_Co@cC?Au@yC[qAu@_D[mAk@cC[qAi@cCOu@}@wEUoAUqASqAQgAOaA_@kC]gC[oCm@yFGm@uCqXUuBCSQ_BOyACSOqASoBSqBSqBUoBYoCSmBSmBSqBUoBWmBSsAMu@]kBo@_Dc@mB[kAGS?Co@}B_@kASm@Wy@Um@]{@Qe@e@iAUk@Ug@EGe@eAcAqBi@cAw@sAm@_Ay@qAq@}@y@iAoA_BeEgFuCmDw@aAkB}BUYy@eAa@e@mA}AY]W[_AkAsBgCEGkA{ACEY_@k@u@qBqCuCmE_@k@[g@oAmBkAgBoBwCiBsCuBcDeCuDaBeCGKOUYc@w@kAsCkECAk@y@}@kAs@}@_AgAcAgA_@_@g@g@iAeA}AsAeBqAu@g@[UoAw@mAq@qBeAqHoD{EaCQICAMG}HyDQI{@e@_B_AkAu@y@k@{@q@cAw@}@w@o@k@sAsAy@{@k@o@oA}As@}@e@o@?AU[a@k@i@{@gAgBy@wAaBwCy@wAQ]oAwBgAoBuAaCy@yAmCwEkCyE_CcEmCyEEEmBgDw@qAm@aAcBoCQYg@u@_BeCiDcFSYuDgFa@i@{CcEcCaD}@kAmDyEmA_B[a@aHeJY_@Y_@CC_C}CwAmBmCoDEGw@iA{@sA_@q@Wc@KU[o@Yk@Yo@Wo@Yq@Um@_@iA_@iA[iAI[e@gBc@iBOo@sDmO{AeGuGkXI]}AkGKa@a@eB}AkGsGaXgDeNiAuEoCaLwByIUaA?AU}@Om@aAuEa@yBc@eCYkBAGS{AKu@OiAGe@QmBQeBC]Ea@SiCKkBU{DMuBQwCU_Eg@wIY{E_BuX[aFOsCIwAEo@E}@[aFIuA{AsWe@kIYeFy@aNU}DMwBGcAy@sN]aGC]K}AAQ?AMkBk@eKIyACUEy@Ek@G{@K}@Ec@E]E_@Ig@M_AKs@SaASoAGSGWS_Ae@mBe@mBo@cCwCiLiD_NgD}M_Kea@{H}ZUcA_@{AMi@Oq@Ia@Mm@Gc@Ga@Gc@Gg@E[C]Ec@Ek@AMA[Ck@Cu@Ag@Ay@?k@?Q@c@@{@Bs@Ds@F{@Fw@Fk@Fk@T{A\\cC`@kCj@qDnAsIj@uD@KXqBPwANwAHaAF_ABe@D{@@WF{B@cB?uBA]?GCoAKsBSwCI}@K_AMcAOgASiA}B_MMs@u@}Dm@cDUoA[eBSiA[cBc@aCO}@Oy@Ou@SkAWyAG]g@sC[aBcAoFWoACQKc@Oq@Sy@Qo@Uw@So@Us@Oe@Si@Sk@]y@[{@m@aBq@iBo@_Bg@uA}A_Es@gBO[CKs@kBs@iBeAoC{@}Bo@}AgByEiAwC]_AyF}N{@_Ca@cAe@oASe@mBcFoCgHqCmHuDuJk@qAi@mAq@{Aq@sAm@mA_@s@u@sA[i@_A_B_BcCe@s@g@s@{@gAy@cAoA{AGGw@}@wA{AqAqAmCeCgAcAqCeCgC}Bg@c@qAoAKKw@y@k@o@s@y@m@w@}@mAaAwAk@{@q@gAYg@Wc@s@qAs@sAw@eBg@iAg@mAu@mBc@sAi@_BEO_@oAq@eCsAqFe@mB_A{Dk@{BcAaEsBkIuAyFiBmHiBqHm@eCWmAOw@My@Ik@CMKcAOiAGs@AK?KC_@Eo@Ck@Ca@As@C{@C}@?}@Aw@@oA?o@FoADkAF_AF_A@KFk@?AJcANkAPmANy@PcAR}@VcANk@HWX_ARi@j@{AVm@Zq@JULWd@}@\\m@FITa@@An@_A^g@\\c@\\c@b@g@b@e@j@i@h@g@n@e@r@i@~FgE~@q@`As@f@c@l@m@`@_@V_@TYRY^k@Vc@Vg@n@sAb@qA^gARy@TeATuAPyAH{@@ODi@?CDaABw@?a@?s@?o@CeAEwAK}CE}AAUMcEe@uMEaBKeDG{AIqBUyHOiEGmBMmDGyB_AiYMgEAKKeDGoBCwAAkA?w@@_A@i@@aABk@?GDo@HyAFu@Hy@Fk@Fe@Hk@Hi@Jo@ZwAXmAPu@Rm@J_@L]Pi@J[Pe@Pa@JWt@}Az@_BZm@vC{F|CcGtIiPtBcEx@}Av@_BrByDdBcDxE}Iz@_Bx@_BZk@tAmCdBiD\\w@Zo@Xo@Vq@Zw@Pg@f@qAf@}ARq@ZaAZeARw@T}@ZwA\\}A\\aBJo@Lu@Ny@VeB@MHm@L}@NoADg@BWPkBFw@JsAJwA@MV{DDm@\\oF`BgVDo@ZuELsBRmCPkCFy@FsAFeABq@BcA@o@BoA@M@oA@yA?cA?A?i@AsAAaA?a@C}@Ao@A]GeBK}BK{AO{BMiAAQEk@Ky@Iu@Im@S}A]kCaEiZm@kEa@}Ci@_Eg@sDi@sDq@aF_AeH]iCAE_@mC{CeUi@yDOqAS}AMmAIw@Eg@Ei@Gy@E{@Ew@Ce@Cm@Ao@AW?QK{HIyHC}ACkAM}EKwCSiEWwEUyCCe@m@kHeAqLs@iIe@qFk@yGi@gGa@{EO}AMuA_@sDKy@[kCc@qD{@wGE[a@{Co@eFIk@yAkLG_@Ky@SgBMiAEi@M_BIkAEk@?AMwBAUE{@Ca@g@cJCUQgDGcAc@wHEm@Ck@IuAAKG{AKaBIkBo@yKCk@KaBI{AI}A?AEk@IaBEk@Co@Eq@IyA?CAOC[Eq@u@cNY_FCk@KaBKsBCU?CMiCAAMkCK_B_@{Gs@sMCs@IyAOmCEo@?AM_CAI?CCk@ACMiC?AEk@i@}JKwBMoBg@aJKuBM}BKwAMmBAEEm@Gm@?AK_AC[Gm@C_@COIm@Ik@?ESuACUQeAKk@[kBE[Km@Kk@Km@Ig@eAsGUyAAGIe@cAmGw@yEAIc@eCKm@Kk@G_@U{AMeAKeAGy@ASEiAEiA?eA?K?c@@S@[Bq@JmBD[BOB]@G@MNeAJk@DQFYJk@Ro@?ALc@BEFUDK\\}@d@eAh@gAPYXc@b@m@TYVYd@g@~@y@~@q@DCvBkAjB_A^S`@S^Sf@U|DsBn@[n@]l@YrAs@LGbB}@n@_@?A^UXSj@c@XY^_@`@c@l@{@d@o@n@kABE`@{@Zy@HQHURk@VaAXoARcA?CN_AHs@LuADcABcA@]@i@?}@KcFS_KAo@Ao@CcACiAIoCAm@Co@A_ACwAAgA?M?o@?E@cA@m@Ba@B_ABg@LcB@EHeAFk@Hm@PoARmAH_@Hg@Lk@Jc@Li@DSPu@HYR_ALi@DUDKDSLk@BMJe@VgADSXoADOF[BIDUBMDOFYPeAZ_BBON{@VcBP{AJeAPyAJoAJuALcBH_BD}@HmBDaB@m@@y@@{@?kA?gB?]?[?s@?cAAiA?Q?eAAgA?O?_AA_A?K?{AAuAAyA?a@?S?SAS?I?K?O?K?U?[AW?QA_E?SCkIC{CCaHAmD?_C?i@Au@?mAA}B?W?c@Ao@?y@AoB?qB?aA?_@?e@?mA@iA@{AB}ABsCBoB?q@B}A@u@@yABiB@}@?e@?MJ{ID}DB{C?CBwCFeF?C@_A@gBFmF?a@@k@@]@s@B_ADs@Bg@Fy@D[DYB[Hg@D[Hc@F[H]FYH[J]J]Pk@To@Pa@JWLW@CXk@Zi@JSHIVa@h@q@x@}@f@i@VUTQTQ`@Wn@a@rCaBhBcAzA{@\\Sh@[nBiA|@i@~@i@PKLILGTMp@a@hAq@HCdAs@TOLIHINKLK?APMVWZ_@\\_@RY^g@\\i@JOZm@d@_ANa@Rg@\\cANg@Le@Ps@Ny@Ha@F]Hq@Fg@Da@B_@B[F_ABeA@o@@k@?WAa@?[Aa@A]CYAUCe@C_@KcACYG_@Ga@EYE[Oq@Mo@Qu@S{@UaAU_AQw@[qA[qAmB_IWiAOk@Oq@WeAQq@[wAOm@Su@[uAQw@Mg@Ok@Qm@GYI]Su@AKMk@?AS}@ScAMu@Q{@QaAKk@Mw@Kk@G]Km@M_AQeASoAIi@OcA]}B_@eCYgBM}@U}ASuAQiAGc@AI[sB]yB_@cCYkB[oBU{AMy@_@cC]_C?AQgACQk@}Dg@cDo@kEa@eCWaBQoAMu@QiAIe@AGKk@G]QgAUiAWwAWmASaAo@yCWiAQw@UgAUeAOs@WkAc@qB_@aB_@iBc@oB_@eB]{Ae@yBSaAWeAa@mBYqAOs@g@}BScAUeAMi@Oq@[{A_@aBg@aCUcAi@aCe@{Bk@iCYmAS{@U{@GUI]Ma@Ws@So@Yw@Si@Qc@Wo@g@eAk@kAg@_Ag@{@m@}@aAwA_@i@i@w@a@m@iBkC_AsAc@o@k@y@q@aAMOo@_Aw@iAaBaCq@aAqAiBaAwAaAuA}@qAk@w@k@y@_AwA}@oAm@{@g@w@g@q@a@k@[e@[e@W[}A_C]g@]k@[i@MUYk@[o@Qa@Ui@KWM_@GOQi@K[W{@YiAYmA[aBO_AKo@Gc@Iq@Iw@c@wDa@qDGc@Ea@WyBSgBeCsTE_@kAiKEa@E[Ky@OoAWuBM{@a@_DM{@CWMw@Ge@Ie@U}AU}AIg@Ik@OcAk@{DIe@Ge@Ms@Ku@O_AQqASqAYoBO}@CQM}@OaACKIk@Ku@My@OcAq@qEc@sC]_C_@cCYoBUyAKs@g@cD_@kCa@oCMu@_@iCc@wC_@cC{@yFs@{EUaB[oB[wBUwAKw@U{Ak@wDQoAQiAWeBQgAMw@McAKu@K{@Kw@KaAI{@I}@Es@KqAE{@IaBKuCG_CCoBCwBEaCAuACw@Ay@?g@Aa@CsAAgACqACyACqCEgCC}BEyBAkACeACeBCmB?SAe@Am@CeBCcB?C?k@C}AEyCEeCA}@C{AEyCCyAAoBA_A?u@?}@?_C?mA@cB?w@?eG@aF?[@yG?KDyS@_F?cC@aH@}G?Q?M@mE@wF@uD@qEBoCHmF@g@DmBDuB@s@TqMJmFDkCBi@DqCFeCL{HB_AHkFHeE@c@PkKBuB@c@BoB?g@@iA?uE?aBAqDCyH?gCAaA?g@AsCC{DA{DEmKAeD?w@AgDCyCAoIGkQAaAC_BAo@AWAWCeAIkBGqAOwBe@sGmA{QiAmPI_AEo@uBc[g@mHe@{Gc@gGQoDKoCAIAe@EeACwBAe@CiA?mAA{@?sBBqC@qAH}DLqDJsBT}DNoBPkBB[H}@h@{E\\{BZsBRsAp@sDVkAP}@FUf@yBVeAx@_DDOVaALa@\\cA`AwCHSZ{@`@iAFSnAoDfAyCv@wBhAaDFOpAmD|@iCh@{A|@cCr@oBPi@tA{Dx@_Cz@gCr@yBj@_BhBsFnAsDzAqEf@}Ah@}AjAmDFUb@qAx@aCp@qBv@_C?APe@t@{BPi@b@oAt@{BPk@Rg@DOJWd@sAz@yBb@iA\\{@\\w@`@aAf@iAl@oARe@Zo@p@uAt@{AVg@f@_A|@_BVc@P[`AcBHOVc@t@oAr@kAtA_CfCgEnGsKvAcCfByCvBqDLSHMbEeHx@uA`@s@\\k@JU^w@NYRe@Ti@Ti@Vs@Na@Ne@\\cALc@Ru@ZmAVgAVmABOXwAl@uD\\eFNsBNcE@GD{CBmCD{EDwED_B@gC@e@?CBkDRkRB{BByB@wAL}J@eD@sADsBFsH@o@FmF?o@@o@LkO@m@JkLFwEB{C@y@JaHByBD_EB{@Bw@D_AFeAHiADi@Fs@NsAD_@Fi@NgAXcBlAoH^}BbAcGXcBd@mCDW@Ib@mC|AgJJm@dAoGp@_El@qDfAyGbAcGx@_FJk@F_@tAqItAiIf@cDN{@h@{C@InAoHFYp@_ELw@j@iDLq@fAoG^{BNaAPy@TmAT_APm@Po@XeAX{@Vq@Zw@Zw@f@eA\\q@Zk@Zi@\\k@\\i@^g@NS^e@^g@b@e@p@q@b@a@`@_@d@a@d@]b@[d@[j@]j@a@j@_@pAw@LItBsAFCd@[nEqC~IyFjDyB`BcA~AcArBqA@AzCmBn@a@hBkA`EgC`DsBhDwBrD_Cr@c@f@[^W~AaAbAq@x@k@XU`@]TSr@u@JKTYNQn@{@j@}@b@u@NYLUP_@Zs@Zy@b@oAb@uADObAuDf@eBRo@VcATy@JWFURk@J[Ri@Tm@N_@Xk@Tc@R_@Va@DGPW@AVa@@?X_@BE`@g@`@c@RU|@cAd@i@`BkB@AZ[|@cAnH_IzBcC|GqHZ]rAyAZ]`CkCd@e@LOLOFINQPSPU\\c@RYT[BC^o@JQPYDIFKNYTc@Te@P_@Zu@Tm@JWTq@JYJ]HYLc@FYNi@Je@TeA`@mB^eBnA}FbA{EfCsLVkAViAhFsVlAyFNu@bA}EFYBQdA{Er@_D\\wA`@cBXmAj@wBp@oCj@wBFUh@eBn@_C\\qAZgA`@{APq@ZgALg@`@wANk@zAkFp@cCj@qB~AwFz@wCT{@FSNi@FONg@To@`@iAJYL]LY^_AFMLWVi@h@eADI`@s@Zi@@CNUh@w@j@w@V[RY~@eAnAwAhAoAf@i@b@e@d@g@hBqBJKfAqAf@g@xEaFfEsE`@a@z@}@TYbAgA`@e@b@k@t@cALUNU\\i@R_@\\m@n@qAN[P_@Pa@Rk@f@oAJ]Pq@Tq@J_@XmAH[Py@ReAh@gD\\mCp@yFXgC\\iCXoCRqAh@eE~@kFRoA^iB`@mB^_B\\qAbAyD`AoDZeAnAuEb@_BH_@ZmA`@}A`@{Af@cBZcAZiAHYZiA\\mA`@iBZgBRoANwAFu@Fw@FuADmCAmBEqBUmFg@cLmBcd@YcHw@{QSiFC}@I_DCmACoAC}C?YCmHAs@GoM?qCAqBAyBCyBGiBEsACw@GgAImAGgAKgAKuAIw@Go@Ga@E_@Im@Gm@Im@Iw@Y_CGc@SeBMaAMgAGm@Iq@[kCUgBa@eD[kCQoAC_@Q_BMsAI}@IcAIuAIsAIsBGoBE_BAiBA{A?]AmF@oF@kX?{D@yA?gK?aI?oB?sB?sA?uA?e@Ay@?YCiACiAAK?OC]A[C]Ew@Gw@Gw@Gw@Ky@C]Kw@Ku@EYG]SoAIe@Kg@Qy@Ou@G[Ou@Ou@Ms@G[Os@Ou@Ou@Qu@Mw@Ke@COI[GYCQMk@?AKk@Oq@Ou@G[aA}EESGWI]Qy@IYQu@IYSs@IYUw@IYSs@KYOe@EKK[IUKYOa@e@mA_@{@Wo@q@{AsAyCsA}CoAqCmAkCIQ]{@Wm@k@uAk@kAKYGK]y@Wq@[{@_@cA[cAYaAWcAMk@UgAIk@c@mCS{A[kCOcBI_AIoAUiFSiEGuAWcFSkEIqBMqCKsBKwBYaGKyBCo@SkEKsB?IQeDMeDOuCGmBKcCGeCMkECoAAo@A]EoBAIAe@EaBAk@Ao@Co@OcIIaEIqBEqBCgAAc@Co@?UEeBCcACaAA[Ai@?CCo@?UC_A?IImC?WCgACgAAUAQIwDGmCIiEIgDAWCeACuAG_CAE?QEgAEmAKsCAIAWA]OkCIkAGaAEk@I{AIgAIiA_@_F]eEEc@c@}F_@{EKsBIsBEsBAWA_B?sA?y@?u@Bw@@_ADoAB_AHuAPmCTkDVsDt@}KNiCNwBTgDPiC`@cGNgCFqAD_ADqB@mDAsAAc@Ao@?AE{AGqAQiCSwBYcCa@kCQiA]sBsAcIi@eDGa@kAgH[kBYiBu@sEsAaIEQSsA]wBUoAeAeHwAgI_@{Bo@aECK[kBy@aFIk@SmAQcA]sBOcAa@aCe@}CUiBQwAUqBOmBKuAScDAe@KeCEyBC{AAgB?u@?aABgBBgBDaBDoAHiBb@gHR{CDo@V_ENgCDw@VwDDi@FiAHiAZ_FTeEB[@c@BWD}@HiABy@Be@HeCD_B@{A@a@?e@?kA?iA?iAGgDE{AGqBWcECe@M_BOuAGo@Gi@sAcNMgA]cD[iDOsA_@yDGk@oCsXk@yFMqA[_DMsAGe@O{AQeBOsAMoAO_BOkBEo@AUIsAA]Ck@Cm@Ak@CoAA_AAq@?i@?U?w@@a@?W@{AFyEBsBD_D@m@DiD?w@?qCE}DOiCM}ASqBa@eCUqAe@qBKa@Mk@I]I[I_@Ke@K_@AGEQG[I]Ke@K]G[GWMe@G[K[EUGWOs@WeAyAmGcAgEEQ]yAqBuIa@aBQ}@Ke@GWg@sBu@eDaBeHI]CKu@aDy@oDmAmFaAsDg@{Bq@wCa@cBgAyEaAcEsAwEGO{@sCc@kAEMO_@Uo@IU]_Ae@mAeBaFw@yBkDwJm@_BmAmDQi@Yw@cAuCqBuFw@wBa@oAg@cBa@cB[yAUsAU{AKu@Ge@K}@C]AOIy@QqBc@gFMuAC]Ee@oCo[CWCYMyAgCsY[mDWiCIq@_@uDQ{AIq@e@{DYaCsA{KUkBWsBWkBEe@A?uAiLmBsOWaCI}@Iw@Eo@G}@IgBEcBAu@Ai@?k@?C?_BAI@aA@g@@e@By@Bw@Bs@HsAFeALsAHw@^yDLyAn@sGp@}G@KBMFo@Fo@Da@NcBLoAt@uHNyAh@uFl@eG\\oDf@aFNcBr@kHNaBP{ADk@LmAJ_AJoA@AH{@J{A@QDi@DiAB_ABa@@k@?w@@c@?s@Au@?CAi@CkACy@?GEu@GmAGy@I{@Ea@?AIq@CWIe@Kw@Mw@SoAKm@YyA_@wB_@yB[kB]mBUoAG]G[EYMu@Km@Ia@G]Ie@UoAW{AUqAOy@Ms@SkAQ_ASiA?EKg@O_ASeACOG]Ms@Ie@CQWoAIc@ES_@kBMq@EM]_BESKc@e@sBa@}AOo@Su@oAyE{AyF?C_AiDMg@a@yASy@YeAMe@[kASu@_@yAEKw@yCSs@CKw@{COi@q@eCy@gDaAcEGUG[Q{@o@}CGYCMQcAWqASmAO{@{AcJOw@Mu@O_ASgAiBwKcA_GoAkHSmA[iBc@mCu@kE_@uB}AgJo@uDiCmOm@kDc@iC?EKk@EUO_AKi@AGCQEYACGe@Iq@Is@Gi@AOE_@Gu@Ey@Gy@CcACg@Am@Ai@?m@AaA@W?e@@y@ByAFuADu@Dm@@UFo@RmBJ_AHs@^wCX_CHm@l@eFl@eFHm@ZiCtCaVnBaPNcA@GL}@LiANcAHo@@AHk@Jm@P}@Ls@No@`@}AXmAPq@X{@Xu@JYVo@Tk@LYTg@N]BIh@iAjAqCRg@DKd@gAp@{An@{An@yAbG}MvDuIx@mBz@mBr@eBHc@L]d@cA`AwBRe@Re@d@eABGTg@zBgFRg@h@mAJUP_@LQNS\\w@Te@Re@rAuCTm@Tk@xAgDfAaCz@qBb@aA~AwDb@cAd@aAjAkCzAiDFS|BiFf@eAlCiGbAyBx@gBP[jA_CP[`@u@f@}@n@kAj@cAbAeBPYlAuBf@}@x@uAv@uAv@sAfAkBt@uAXe@Zi@`AcBx@uAbAeBfAkBLSd@{@j@}@b@y@`@s@dBwCbAiBf@{@lAuBnBiDVc@jAuB\\q@v@aB^_ANc@^iAPm@V{@TcARy@Lq@TwANy@NsANwA?CB_@BYBe@HqAD}A@w@?_A?a@AuAAq@CaAGsAA_@Gw@Iy@Iy@QsAQoAUuAc@aCMs@_@wBq@{DGYm@eDe@kC[gBk@eDKk@Q_AGYKu@Kk@Gg@MkAO}AGqAASCo@ASEuAAuA?y@BuABuADw@FsAPoBNqARuARoANu@R_ALi@T_A?ATcAj@}Bb@qBT_ADUVaAx@mDJc@Pu@ZwALg@v@gDfAyENq@Nk@\\{At@aDb@kB`@eBR_ARcAN{@Lw@PqAPuAHs@LwAJqADy@Dy@FuA?MBs@@g@@a@?C@mBCgE?AC}DAgAAuBG}IAsCAo@?m@AmAAaAAkA?aAAo@?OA_CCqCAoCGuJEmF?SCmD?k@EsFAkCA{AGwBCs@E{AAOG_BG}@K}AEk@Go@Is@Gg@YiCYkCGm@YiCa@sD[qCSkBW}BUiBCSKgAk@gFW{Bi@wE]_DGm@McAAQIs@Im@K_AIs@CW]_DMeAw@kHWwBOqAg@sEoAkLi@{EIm@Gm@c@wDGm@Q}AIm@s@sGIm@O}Ak@eFQ{AgAqJO{AIo@Gm@i@aF}@gIc@sDSoBAI]}Ce@kEOsAUmBKkAQ_BEk@a@mEWuCoAqOi@yGaCaZWaD[yDi@{Gk@eJO}CQkDQ_EM{CKqCa@eLKuCe@qMCo@QkFIuBEgAAQCy@Cw@?IAo@?I@mA?u@@a@FwA@SDg@?GJiAPuAFWJk@?ER}@Nq@Rw@Rm@Vu@Vo@Xo@`@w@b@w@b@q@\\g@l@s@lAqA^Yb@]p@e@hBaAp@]n@Wj@Sj@QPGtCw@bBe@lA[`@MfCq@r@YVIv@U`@M`Ba@d@Mx@Sz@Ut@SvA[|Aa@lBe@bBe@d@M`@MvAc@b@MLELE|@_@d@UTM^WVQBA\\YHG\\[^c@PSV[V[j@_Aj@eAVk@b@iAZaAT}@VoANw@PqAHw@Fw@FuABy@?q@?a@?K?o@A]EeAEkA_@yIUcF?Gc@iJY}GE}@OiDEaACo@Ey@KcCAKCa@Co@MmCCo@Q{DCo@Co@YoGMuBI}AYcD[iCSuAYiBAA[kBUcAI[COOq@[mA]mACIOi@GUa@kAa@iAa@kAk@qAi@oAgAyBeBkDuAoCu@yAm@kAEIg@cAsAkCQ_@Uc@yAwC{CeGcAoBaGoLmCoFQ][o@Wm@Yq@IQ[u@c@kAWu@{@oCSs@Qs@Ss@Qs@Ou@G[GYSaAUoAKo@Im@M}@McAMgAMmAGw@Eu@Gw@GaAEq@Cg@IyAIoAGgAAMMqBG_AGaACW?IEe@ASEg@Ky@MaA?AUyAAEKm@Ic@CK[yAOi@Qo@[eAQk@Ys@c@cAg@kAi@eAKQKQ_@m@yA_C}BgD}BiDkBoCyD_Go@_AwBaDa@k@]i@[i@Uc@S_@Yi@O[KUWm@EIQc@Wq@Uo@IYKYEOMc@]mAQw@GUYwAMo@SoASsAIw@MqAGy@Gw@?MEi@C{@GqBK_GWeO?EOuIA[CwACyAEsBEsBC}@_@uTKuFAq@EsBCwAEeB?MA]?CAW?YE{@AYG_B?AMeBMuAI}@KcAKw@M}@QiAi@iCOu@GS?CEMI[I[IYQo@K_@GSKYUs@Wu@Wq@O[a@iAg@oAaBgEkC_H_@}@IS_FmMOc@Ui@Uo@Yq@Um@m@aBWq@c@oAi@}AWs@i@cBGWi@eBUs@Uw@[iASu@Qu@[kAQq@I[G[m@eCQu@Ou@G[Qu@Mq@GYG[GY?AOs@UsAWuA}@}E]mBo@{Cm@aDe@iCe@eC_@mBWqAUqAOw@WqAUmAI_@Mu@ESIa@]iBIg@Kg@AC]iBWqAMs@Oy@WsAWqA[eBQy@Mq@WuAUqAOu@{@yEq@uDAKI_@YeB]oBUsAMu@Mu@UqA]mBSqAMu@WqAc@mCI_@SkACMIm@Kk@AC[mB]mBKo@G]CMKk@UqAc@iCUuAMw@EQUsAUsAUoAO{@SqA]oBMu@i@_DUuASqASuAMs@SwAWiBUaBUcBQqAKw@Iw@QqAEa@E[Iu@MaAg@wESmBa@eEMsAUoB]kDKeAw@_IGo@YiCGo@_@wDa@yDc@sEGm@MkAI}@CSEc@Eg@Gg@Ge@"
                            },
                            "start_location": {
                                "lat": 41.1473731,
                                "lng": -80.6770118
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "33.3 mi",
                                "value": 53541
                            },
                            "duration": {
                                "text": "31 mins",
                                "value": 1835
                            },
                            "end_location": {
                                "lat": 41.069386,
                                "lng": -75.4001818
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "stoyFph}nMaAuJOuASaBKo@Ga@SsAUoAMu@Ow@YsAYoAKc@WaAw@sCUy@Qi@i@_BWcAUeAQm@[kA_@iAk@uBK_@IYOk@e@_B]mAGUQi@CO_@qAUu@g@eBi@kB_@qAe@gB]uAOq@WsAOy@Ga@QoAGc@Im@Iu@Ea@C[Iu@Gy@Ey@AGCo@Cg@Cm@Cy@As@Ak@?u@Aq@?a@@gA@gALgE^aLBo@@KLoDNwE@UL}DNkEPmFZoIHoCDyBBaA@{BAq@A_BC}ACoAAMCm@Cq@SgDGy@S_CUgCMcBI_AGm@W{CQ}BEi@WoCEm@c@iFAI[qDEm@m@eHCc@Iw@M}AKkAOkBIq@OyAMoAQqAKu@E]OeA[qBk@cDmAsGa@yBGa@CKMm@{AiIKc@cDcQ}Fa[AEEWy@kEq@qDg@kCKm@{@mEO}@Kk@CMe@}CKw@SuASaBAME_@OmAQkB?AGk@ASOiBG{@?AGw@GuAEm@EgAEq@?SCi@?EEkAIkDSgKSwKYiOE_BAo@Am@Am@Am@Am@AU?W?ECuAGiC?M?KGmDA_BCuEAsBAkD?cD@aFByF?uA@sA@gD@wAVsw@Pwh@HkU@qE?iD?[AsCCyCEkBIgEGqBGsBEuAGoBIuBEuAEuAGsBEsAEsAEuACy@Cy@Cy@EuAEsAC{@EsAGqBGoBG{AGqBKoDEqAKkDMgEKkDEsAIsBEuAQmCMoBSoBIy@WgBSwASqA_@kBa@kBg@cCg@aCs@eDQ_AI]Mw@O_AMy@I{@AWIcAAk@Cs@A_@?w@?_@@s@B}@Dw@Fw@Fo@JcATqANw@Nq@ZkARo@L[JWVo@Rc@\\o@n@iAv@sAhAkBfAkBNWbAcBvCaFnBcDrBoDz@uAx@wATc@PYl@kA^}@f@iAHQXq@b@iAj@eB^kAPk@\\oAZmAd@iB\\uA`@_BZmAZoA\\qA|@oDp@oCVaAPq@Ry@Ha@P{@N_ARyAH{@JoA@KDiA@KDoB?c@?aA?c@AaAEaAI}AOcBO_BO{Ay@}IMwAQcBQgB]uDO_B]oDa@gESwBQaBUaC_@{DU_C]yDU}B[aDOaB_@{E_@uEUcDWeEIsACS[iFK}ASaDKeBKaBKaBWkEOyBE}@QcCQqCa@_HAWo@gKC_@Ey@IqACs@GsBCs@AcAC_A?aAAyA@gA?aA@{@D}ABeAD}AD}@H}ADcAH}ADcAD{@Bg@Dw@HaBD{@F_BF_A?EDu@FaBBi@HyALgCD}@J_CJ_CHcBH_B@_@D_BBw@@_A?G@_A@{@?aA?i@?SAeA?YAeACaA?YCu@AOAc@IkBCu@Ce@G{@G{AIcBM{BE}@EaAIsAGkAEaAEw@IcBGsAIsAEw@E_ACa@Aa@Gy@I_BCu@Cg@GcAGuAEcACi@?[?CAk@AQ?eA?aA?}@B_AB}@@c@Dy@Be@B[FaAH}@Da@J}@L{@L_ATsAF]Hc@nAmHV}APgAr@cEZcBN_ANw@LaAN{@LcAFe@F}@HsABm@?[By@?}@A}@AGCiAEo@Ca@IiAKgACUMyAMcBAGKoAAMGm@?EGg@Eg@OqAAOUaBCUWmCOsAQeBQ{A[iCQiAIe@WgBOy@Q_AScAe@_CQ}@YoAc@gB_@wASu@YaAi@kBq@{BOk@_@qAg@cBQm@Uu@YeAUw@ACQs@[oAS}@GWMm@EUG]E[GYEWKk@Kq@E_@Ik@E]E[C[E]Is@E]Gu@IkAC]GgAGkAC}@C_ACuACeAAg@?U?AAk@?CK}IGqDC}ACsAA_A?gA?}@?q@@sAJuC?KFw@Dw@FeALmAH{@Ju@BYFc@BMDYJq@Hm@RgAr@eEx@wEvAgILs@z@eFlA_H|AiJb@_Cj@kDf@sCn@sDXyAT{AVuAZoBTsA`@eCPsAJqAFs@H{ADs@?a@DsA@wBAwAAy@C{@G}@Cg@Ci@G{@Iy@Iu@[qBIe@WuAWkAWeASw@_@kAWu@g@oAYq@MWa@w@i@cAo@gAyDsGo@eAWc@cAeBaAaBkB_DuA_Ck@_AaCaEeDuFqCyEEG{AkCIKq@mAc@u@[i@Yo@o@yAWq@i@yAO_@Qm@K[]oAKa@Om@U_AOs@WiAWqAg@}Bg@wBk@uCYmAUkA[sAOs@Mm@Q_AMm@O{@Mw@CMMw@G_@Kq@E[Io@S_BOyAu@}GSoBUoBi@gFGm@Go@MiAs@yGUqBS{AWaB]qB]gB[wA]uAYgAm@aC}@uCUq@Yu@m@cBk@wAo@gBs@eBIUm@}A_@_ASk@Se@Yu@_@aAO_@AGSg@c@iA{@{BUi@Sg@Oa@mA_Dm@eBq@oBs@wBs@}Bu@cC{@aDOo@]mAm@gCu@aDa@cB]wAOk@Mi@Mk@Ok@gAyEQq@iD{NuB{IKc@{@oDWkAQ_AAEY}AM{@U{AAKKu@OwAKmAI_AKuAGiAGqAMaCKqBsBic@Co@e@yJCo@Eo@G}AI}AEo@Co@Cm@yAc[Cm@S}De@yJOeDUuEIeBOuDCq@_@yJAm@IgBEuACm@O_ECm@UqG_@oKGaBG}AEwAAg@A_@?QAA?O?_@AY?]@]?W?[@}@Bs@@]Bm@Dq@Dm@De@B]Hs@J_AHi@\\qBToAPw@Rs@^oA`@sATs@?APi@Pi@^kA@GdAeDNi@r@}B`A_Dt@aC~@wCpAeEJ[h@gB?AL_@Pq@Lk@FWJc@@G?AJk@@CFa@Jq@?A@AFk@Da@@K?AFo@BS@WDc@?I?CBi@?ABc@?MBk@?A?A?k@@I?e@?QA_@?SA}@Ak@Ek@Cw@I{@Em@AAEe@Kw@Ky@My@CMAAEYEO?AEQGWMk@CMI_@GUESUaAa@mB?AMi@?Aa@kBGWKi@Kg@AC?CSiAKy@?AGo@AMEm@Ca@Cq@C{@AsA?e@?EDgBBg@Bi@Do@Hm@BYHk@Hi@F[DODYBMH]@CLe@BKPi@Lc@Rk@L]jAuCTm@d@iAhAqCTo@n@eB^iAPo@Tw@Je@Jg@F_@Jk@@EJu@Fa@BUBUDc@De@Dm@BS@[@UB_@B{@@e@Bw@@UBkAF_C@k@HuCLiEFaCFoCDuADwBBkBHmFD}DD{G@kC@wH?{D?a@@gBAeC@mB?aB@iB@}B@oADgCDyDHcFFcCFwCD{ATgJF_CJkEBsABkAFgCHyCJiEDqBBy@@w@BqB@eB@eA?yB?kD?mAAq@?QCgB?e@C_A?OEwCAUAa@?]SqMKeGCuAAiAE}BGkEGiEGsCGiEIiFGkEEmCA_@CoACwBCsA?a@CwAEqCGcDIaCGqBKiCq@kMIuAAOCm@QcDYkFGgAM_C[kFg@}IWmF?MKoBK{CEwAEoAC{ACcA?EAe@?C?EAiAAaAAm@?WAmB?wA?iB@iH?aC?gDByN@_E?mD?kA@cB?}@BoC@iAD{@Bk@D}@F_AHmAFq@NyAD[F_@B[PiALy@XwADULi@?ATeAHYRw@XcAV{@FSt@iCd@}AdAmDLc@n@uBr@_Cp@_Ch@kBr@aCX}@XcAf@aB@CZgA`@qAPo@BGNi@?AJ[BM^mAZgAb@gB^gBH_@Ji@DUNcA?AHk@?AHe@JaANoADm@Fo@HkAFiABe@@YBg@BuA@q@@qA?_A?uACcACwAGaBEqAGsAIkCOwDMiDEkAGcBMsCUgEOmCMiCO_CQgCC[AQIcAOmBOkBq@yJc@wFY{DGcAKoAASC]AOAOC_@IqAEeAAe@Cs@Ck@Ay@C}@AkAAuA?wA?]@{@@yA?GDiBFeB@s@FaAFgAJaBJwAPgCBc@XeEJ_B@OD]Ds@Dm@HgALmBBY@WBW@UHiANqBPiCLmBTmDRsCJwAFw@^wFPgCN{B@OB_@BWHiAPgC@WVuD`@yFN_C`@aGX_EDo@BWJyAT_ELaBHuAFm@Be@Du@JsBFaBFwABw@FcBByA@k@Bc@?a@@u@@s@@_@@kA@]?O?m@@{@?w@?uA?U?E?kBAmDAaECwC?kCIsRAiCA{AEwEAq@EkCGoCC}ACw@GiCE{AAo@AGKqDCa@YwHQgEEiAS_FCcACeACw@?]Ay@AkB?a@@{B?]@_A@u@DmADcADeA?OD{@LoBF_A@OHcALoABWNyAVeCHq@T}BXoCHw@LqATuBZwCRoB@SZaDFs@BMNoBF{@JoALoBBi@Ds@JqBHuAFmBT{FFqBFkBH{BTsG"
                            },
                            "start_location": {
                                "lat": 41.045375,
                                "lng": -76.01305479999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "63.9 mi",
                                "value": 102841
                            },
                            "duration": {
                                "text": "58 mins",
                                "value": 3492
                            },
                            "end_location": {
                                "lat": 40.8590554,
                                "lng": -74.37587409999999
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b><div style=\"font-size:0.9em\">Entering New Jersey</div>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "ujtyFbrekMRuFPoFBg@TcHHwBJqCDkAD_AFuAFaAJmAH}@LcANeARmABODWJk@^cBLo@r@_Dp@wCF[DMLm@Ni@Lk@b@iB^yAz@iD^{A`@aB^yAVaAtAyFfEyPj@aCn@gCJ]b@eBFWj@}B@Ed@oBb@gBt@}CF[P{@PgAFe@Ju@BSH{@F_ADy@D{@BaA?y@?eACqACm@Cs@AIEo@C]Gq@AGIs@EYGa@MiAMoAIs@g@{D_@gDa@oDCS]qCYiCScBM_AQ}ASmBq@wFg@sEUiBOwAS}AIy@Eo@IqAKoBIeCA_A@m@?GAq@@_C@a@Bm@@g@?O@e@Bg@@i@Fu@JyANeBt@}H?CPeBDY^gERmBd@}EDm@Hy@x@iIhAsLFy@v@gIPgBr@uHFc@Fe@ZiDh@yFd@{EBU\\yD@Gb@aEVwBJq@^yBXuA`@kBVeAXiAPo@^mAj@iBb@gAXu@x@oBp@{AtBwEz@kBRe@l@uA|C_HxC{GnAwCzAcDzAkDf@kA`@y@Xg@d@w@P]@AV_@BET]RW^i@VYZa@\\_@XYz@w@@?VUb@]BAv@i@`Ao@zAw@t@]p@Yd@MVGXGjBa@p@Mz@QjAUhAWj@MpFgApFgAnAYjDw@vEcAlAWfBa@ZGjCk@nAWXGdCi@v@Q^IpAWpAW\\I^GfBc@PE`E{@fFiAnAUlBc@dCi@x@Qz@Q`@IjAW\\G`B_@|@S|@Qj@QzBq@h@QTI`@O~@_@`DwArDcBlDaBbAe@?AfEoBZOdAe@dCiAp@]hFaCtFgCzAq@ZMdAi@`@Sz@c@vBcA|DkB~CsAhFcC`Bu@@?hAi@t@[dIuDbAe@dAg@f@Wb@Wv@e@l@a@ZW\\W?Ah@a@l@i@b@c@VU?AZ[@A^c@XYRW^g@^i@RYV_@Va@Ta@Zm@f@cAd@eAd@gAPg@Re@^{@Xu@lB{E|D_KRg@hCuGxBqFPg@bBeEbBgErLiZRg@`GeOzAwDzAyDtBmF~AaEdCkGtAmDj@wAn@_Bn@}Ax@wBbBeEFOfAyCRg@Z}@X_AZeAVaAXcAhAiFbB}H~@iEvAmG~BoKLk@rAgGZuAZyARy@d@sBLk@f@qB^gBf@eCh@_Ch@_ClAyF~@mEd@wBh@_CJe@j@iCLk@Lk@Lk@`@gBTeALk@Lk@Nm@^gBVeALi@pAaGlAsFPw@d@qBb@sBfBcIn@uCf@}Bj@gCt@kDp@wC~AsHLq@Nu@DYNs@L}@Jm@Hc@PqAPoADUNkA@QLcAVcCFq@JiADe@HcAJuAH_BLaCDcADiAJsCLiEDuBF_BB{@FwBFyB@QBm@@u@JoCRqF@YJwCJ{DLeEFeBBg@@QDe@Di@DYD]Lu@Nu@H_@Ni@J[HUBIHUJWJUXo@Zi@NUJQJOhBcC|@mA\\i@R[x@wAZm@`AyBL_@Lg@La@Nk@H]F[Ls@DUF[BSL{@RuAPkA\\mClAmJZcCJo@Jm@pAoJd@qDd@sDViBNoALaAVuBFe@Fg@F]Hq@He@BQD[BS@SBS@Q@O@U@[@Y?C@i@?]?U?_@AYA]?SAQC[C[AQC[E_@E_@GWE[G_@I]K_@ESK]Oc@EKEMKUGQGMO[KQQ]MSQUACk@s@Y[IIEGIISSYWs@s@e@a@e@c@_@]qBgB{AqAe@e@MKSS]_@_@e@_@c@W]KOGIMQ[a@S[c@s@OUU_@IMSa@Q[MSQ_@Q]CEWm@O]Q]Sg@Qc@Qi@O]Oe@GSOa@Qo@]oASq@[qAs@oCa@wA[oA_@sAw@}Cw@}CYaA]wAaAqDa@{AOm@Mm@q@gCcAcE]qAQq@[uAUw@[mASw@Me@Ka@CGOi@Qi@CKGUCGOi@A?Oi@CEa@mAi@}Ay@yBk@wAaBgE{@uBqAeD_@{@m@}Ae@iASg@y@wBcBeE_BaEOa@]{@Qi@Qe@Oa@Mc@Y{@Mg@Oc@Kc@Ok@K]Ka@Qu@Qu@Mi@cAkEk@aCqCsLm@qCoAiFo@qCMe@I_@[qAAKOu@[aBUgBOgAEo@G_AGmACsAAaABkBD{AFsAHyAFcAJcBL{BNwBVoDLsBB]F{@H{@D]F[DWF]FUH_@FWJ[HYJY@CJUJWf@cA\\m@PWLQl@q@VU@APOJIFERMPOd@Wn@Yv@]fJuD|@]~@]f@Ul@U|B_A^OLGv@[dBs@xKiEb@SpAi@tB{@FCXKz@]LEp@[t@Wl@STEn@Ob@GfAQFCHCVIDANCTEh@I@?NCPClC]lAQ^G`AQFA^IB?f@Mx@S\\Id@Oj@O|@Wx@SdAWbAYfBe@bBi@~@Yh@Od@O~@YpA_@hDeAvC{@xAc@VK^Q`@OZK~@[`@MZKPGDAr@Y\\QVMVMjAq@t@g@r@e@r@g@bBkAz@o@RQRQLMX[h@u@Zi@d@oAL]Ru@Nu@PiAH}@Du@By@Ay@CcAE{@G_AOmB[gDC[QkBAGQoBg@kFC[C[MyAKsAC{@?}@@w@F{@Fa@TkAFWTs@JWTm@Zk@\\g@d@i@`@_@|@w@r@a@f@UXKTI`@MJCVGPCRCTAl@ATAL?`@E^ETEJE\\IDAVKf@U`@UrCsA@ANG`@OJEBAz@W|@UFAFAh@Kx@KbAM|@IBA`AGzAIF?ZCb@AjBIRArBGlBGnBIz@Eb@ALAzAInCM@?p@Ep@E`AG`@Cv@G|@KVEXEXEb@Gp@MTGB?^IXG\\ILEj@OVI^Kd@OLEd@Or@YPIJEhAe@VMZMZQd@Uf@YHEx@i@v@g@FGx@i@BC^[l@i@|@w@fA_ApB}Bb@i@hAoAtBwBHKrAkApAkAlAu@p@k@^W`@Wx@c@r@_@VOJGz@e@x@g@|@o@v@a@n@a@b@WTO^SLINIDEd@Yp@e@b@[j@a@VQz@q@z@o@d@_@VUb@_@^Yx@s@LKpCwBRQXWVSPOFEFGRMBAZU\\U^U\\Of@WTKRGRKDAp@SXId@GTGj@I`AM|@ETA\\APAPAn@CPA@?`@APA`@AZCh@CXEh@IVCJCTEHCFAHAJEFA\\MDCLEFCDCBAFCDAFCFCDCFCHAZQJGr@a@|@o@bAaAlAqANWnDgFrBaDx@sAf@s@NWfBiCn@}@NSb@u@^k@^s@f@{@bAaCFMt@oBDMPc@Rm@|@mC`@sAbAuDP{@Lg@BKPy@`@kB\\_BHi@?A@ID]Nw@\\iCLuATkC@E@SFwABi@@I@YBw@DcADkA@cA@qA?KCqACk@GkAK_BAQO_BMiAOkAEWGQKg@IWAEOo@_@wAGQq@gCUw@e@_Bk@sBCEo@{Bc@cBSu@AIOm@Ia@I_@Kk@Kq@Ig@Gk@Gs@GkAEy@C_BAaABkAD_AHwAH{@D]DYF[D[DSJg@Py@Nk@J]HYDMDOHUJUFQLYN]NYTa@Zk@Zk@\\i@NS^c@^e@b@e@r@o@\\Yj@c@jA{@zAeAhAy@x@m@d@]ZUd@]RQRQ@AJKRS`@c@Za@BCT[d@s@JOBG\\k@Rc@Xk@Ti@Xw@X_ARo@Pw@Nq@Lk@BQDYHq@Fe@D]JiAFu@?ABa@HyABw@?ED_BDcC@{A@yC?SA_ACkAC{@IcBEcAEm@Ce@MyAGi@Ec@MqAa@oCGc@Ie@Ga@QeAUmAS_A{AoG]wAmCaLo@kCm@iCa@}Am@iCAGsBuIiBoHUaA}B}IOg@gAwDGS_AwCo@mBYaAM]IYs@}BUs@Oa@a@oAYcAa@wAYuAKc@S_AGa@EWG]W{AQ_AKm@a@eCc@gCy@_EMk@UuAESIYU{@[iASo@Um@Qm@k@qBY_AMe@[eAe@gBm@gCSw@GYMe@i@qCk@{CCOi@}CQmAU}Ae@wDMmAOmA[kCSgBK_AWgCYqCWqCK{AQkCK_BIaCGaBCsBCaBAuA?sA?U?kA@_A@yDBcB?QDgCD_BBsAHkCBy@Be@P}DL{BL{B@EHaA@OXqDLiBT_C^mDT{BVqB^sCXeBFe@^qC@G\\gCd@cDJy@f@mD@GHc@@G^kCZyBJs@LgAB[LgAH}@Do@LyAFs@Dq@Dy@Z_IPoEJeCDc@@QFi@Fq@Hk@D]DUJs@XwANs@BI`@}Av@qC\\eAZaAdAiDNk@BIp@{BJa@HYd@qBHa@F[BQJm@VmBDi@LyAJgBDwA@w@@eA?A@m@@uA@y@@mCBmC?AFwHDeEByAB_A?ABs@FoADw@JeBLyALkAPaBLeA@MZuBL{@TuAF[@EFWBMFYLm@\\sAFQLi@BIL_@Nc@BINc@Pc@@Eb@gAJQLYd@aADI`@y@x@cBf@cALYHMrAmCRg@p@_Bh@uA`@qAPo@Po@ViA@ILo@Jg@Hm@TyAHaADu@B]N_C@e@@e@Bs@DqB?_A@aA?cBAyAE}AGiCEmAAYASCi@I_BACKcBCYOiBQ}AUiCCY]kDAIU}BGw@Gu@AOEo@Es@Cm@Cg@?AAo@A_@AwAAwB?mC@{D?_B?iA?aA?cC?yB?eA?}E@uD@kC@yC@eA@oBDiBFwBn@cOHuBDeB?Q@m@?A@S?Y?qBA{@A_AGwACy@OyBMmAMoAcA}H_@iCg@uDYmB?AMeAKm@_@uCQuAe@kDWkB}@sGs@sEmAiJ}@{GKw@m@gEmFm`@Im@M_As@cFe@iDe@kDk@oEMeAI{@Gy@G{@EcAEwBAy@?s@@I@iABeA@c@@SJiBFy@Fq@VyBJ}@j@gF`@wDJ{@Fw@Hw@@MPoCDoABYBq@FaE@g@@o@BkDF}DD{BBkADaAHoA@[Fu@H_AFo@Dg@@ADg@Ju@XkBF]@?`@wBBK?AH]XeATw@r@yBl@_BNa@|CcHtB{En@wApAyCx@qBx@sBFMHYL]~@{Ch@qBh@wB@Cb@sBP}@Ji@?AF[^cCLy@VwBRuB@IHaARuCHaBLaEJ{DLqCJ_D@Y@o@FyB@SXuIRqGHmCHsBHgC^kLHmCH}BJeD@U?ALyD?A?O@Y\\mJLyBHiA\\aEFm@Fm@@OD]Fc@@IHm@Hm@Hm@@EPqAJo@@GHc@Fc@DYF[T{AJk@RmAv@cFb@qCn@sDHm@Lu@^}BNcAVcBPqA@I?CDa@Fw@Fy@DcB@qBA}@Cq@Cy@AS?AGm@Cg@K{@Ge@Im@E]]sC?EIm@UkB_@}CS}AMwAGqAAq@AY?KAm@@i@?qA?G@c@@k@JoBDk@JcAl@gD`@mBrAuEpA_E|AmFb@_BBIR{@DMLk@?ANw@V{BFo@Fg@B}@DuA?SBuBC}AEsA]gFOoBCw@WwDKyAGqAI{C?}A?WBeA?UFgA@MHgAFu@BQB]R{ARyAJm@v@uFPgAXmB^kCJuAD}@HqBC{@CeBCmAM_BIsA_@qBMs@g@{Bo@iBeA_CqA_CcAsA{CkD{CaDu@w@]_@k@q@QW]c@GK}@yAIKo@kAaAuBWu@So@Oi@e@mBQw@]sBK}@AOGq@QwB]wEa@sFc@wD]iCa@oC]iCg@cDIg@Ga@Ks@WkBCOGg@C]C[C[Es@Ae@Co@?QAa@?O?S?]?YBuA@Y?ADw@B]Bc@D]Fm@Da@Hk@D[Ja@F_@R_AT{@J_@N_@L]Z{@Vm@FOJULWPWJSVa@Va@X]TYZ_@XYXWPQ`@]PO^Wb@WHGXQj@]ZQRK\\UXO\\Q\\SRKPKHEdAm@`Ai@r@e@d@[NKXUXWBCz@y@`@e@LQX_@\\i@^k@\\m@Xk@\\y@Tk@Ro@Ne@FQ\\sAZ}A`@cCJs@Js@LkAFi@Fk@HiAHaAHeBD_ADgBBu@@}A?_E?e@AsGAuC?uB?sAD{ABs@Bo@F}@Dk@Ho@Da@BUN_A?EN}@Jc@RaAVcAPo@HUl@cBb@mAj@oARa@`@aAHQl@wAn@}Az@sBDIHUJUt@_BrAeDj@}ATw@T{@@GJi@Lo@BKFa@DWBSDg@J_ABa@B_@FaB@{@@y@Ai@?QA}@Cs@EyAA[[kJc@qM[uJEwACsAAa@CeDAcB?cC@oB?S@[BuAFyBDyBPmDLoB@QB[J}A?CLyAFi@?CVqCFg@h@gEn@cEX_BRmAf@eCDS^cBl@eCLi@Ru@\\oAf@qBZ_ARq@X}@Pi@`@iA\\_AVs@\\}@x@kB~@sBf@cAj@kADKP[bB}CVc@lAqBfA}AdAyAXc@PWBADG?ANQNSDEDGLQTWLOp@y@JMbAiA^_@fAgAv@u@xAqADGfA_AbCoBHGpA}@^WdAq@XQhBgAvBgA`Ag@bBu@pAk@xFkCpBaAvBgAHCv@_@`Ai@bAo@n@e@p@k@^]jAkAh@o@j@s@LQt@eAv@eAf@{@f@}@t@wAj@uATg@JWVs@\\cANc@\\oAH[Lg@\\uANs@Py@\\sBLiAZmCNqBJ_BJwDB{@L_LBu@B{A?k@HeEHkGDqCPcMDcCDqBBw@?Y@y@B_BDoCReNByAH_G@o@@m@F}D?I@e@F}D@o@HmFDyB@s@@uA@mA?[?m@A{AEcDCs@IgCQ{BCc@K}AGk@Ee@QoBMsAI{@CQCWKw@M{@Ik@My@m@iDs@yDq@uD[cBg@wCUqAO_AGe@EWIs@CYEc@Iy@MkAMcBC[AQEg@KiBIyAKcCEkAEeCAkAASAyA@oA?k@?C?m@@u@BcA?UFqC?C@[TaJBiA@a@@{@JyE@SFaCDyAB{ALoFBgADaCBmA?_@@gA?yA?{@AaAAmACcACu@A{@C{@EaAEy@Es@AQC]Em@KoAM}AKoAMgAIo@Kw@OgAKs@?CIk@Ig@QiAEWS_A_@mBe@}BScAKk@[wA?Ee@_CcBoIm@uC_@kBScAu@uD_A{E_@iBe@eCQ}@}@mEcC{LKk@Qw@k@qCWmACOS_A[{A]cBG]I[AIWeASeAUeAEW{@qEI]g@mCe@cC{@gESy@EYa@qBk@mCKk@WuAMo@]cBACc@sBy@}DKk@YwASgA[aB{@oEa@sBs@mDm@uCa@oBMk@?Ac@uBOy@Mk@?A]gBQw@YsAY{Au@qD]eBc@wBuBoKc@sBOy@?AACScACKe@aCo@aDQaAk@mCs@qDgB_JkBeJKg@Qy@s@kD{@mEUmAm@uC]qBU_B[}BKw@KgAQyBKuAKmBK}BG{CCcDFoDB{BR{FJmBPoCl@_I`@aGRuCPeCPqDFcBBeA@mABmA?gB@y@CcBA{@?KCs@G{A?ECo@Co@AKCa@AUGy@Cc@IaAEe@AMUuBUcC]cDIq@cAwJGo@a@_ESkB_AeJCOI_ACKMsAEc@?CCMEi@ScCYuDC_@MyB?EG_AIsBG{AG_B?EGeCAWCoAEoBGwD?c@CgDCsEC}DAuAQw\\A}AEcH?sAAcDIsKAmCEuG?CCmGEwF?sCEkG?QC{E?QA]CmF?Q?]C}D?Q?[A_BA_BA}A?QMwTCwHEmIEcF?[?Q?E?WAo@A}A?S?e@EsG?AGyM?Q?[A_B?QA]?gBCoC?k@?s@AaAAcAGmICmFAq@AeC?u@?WAyAAoB?s@?y@?aA@sA@gA@e@@k@By@@o@Bc@DeA?KRqDDa@@SB[DYBYJcAFy@ReBPwAPoATuAJq@He@Lq@Lk@Ji@ZwAH_@ZmAb@_Bb@yARm@Lc@J[DM`@mA^eAFQN_@JSJ[l@sANa@Vi@Vi@NWd@aAvAyCb@cAp@qAfA{B~@kBP[Zo@`@u@r@sAdAgBVa@R]jC{D`AwAXa@x@kAhAwAX]t@_Af@q@bAkAzBmCf@k@Z]DERYnB}BhBuBh@k@|@{@h@g@zBeB^Yb@WlAu@VMjB_Ah@WtAo@xCwAjB}@f@Un@a@t@c@r@e@v@m@p@m@RSf@g@v@y@f@m@BE`@g@X_@\\i@`@o@Xe@`@y@d@}@Vk@l@{Ad@qAPk@`@uALg@DOLk@R{@FYpB}Ir@_DJc@?Cz@mDP{@b@iB\\oAPq@HYPm@Rk@Rm@Tk@LYbAuBZm@BE`@q@^q@@AZe@t@_Al@u@`@c@`@c@`@a@v@q@LKTQt@i@b@Yh@[B?RMz@c@d@St@[b@Ol@St@Q~@Sv@ObAOlEm@tASt@MfAQnAWz@QBAhAYZI`@Ml@Qz@Yv@Yz@[`@Oh@Uf@U@?FEfB{@j@Yt@c@v@e@d@Y`@WTOp@e@@Ad@]fAy@b@]XWjAaAXWpAiABCZY`@_@`@a@p@m@t@u@lAoA`AeAp@u@l@s@bAmAXa@BC`@k@^g@^i@\\i@^k@Zk@^o@Zm@Xk@Zo@Xm@Zs@@CBIRc@Vs@L]FO@CFUHQBIL_@DQHWJYRu@HYHYPs@Ry@Ns@Nu@Lo@Ls@F_@BO@EBUDWL{@Ho@Hw@Hm@Fw@Hu@Ds@Fw@Bo@D{@Bk@@I@e@?QBu@@u@@u@LoLB{@@y@@q@@w@@k@@I@u@H}B@SHgB@WDw@@UBe@@IDm@Fw@Fy@F{@VsDX{D^aFVmDDw@Fy@F{@Bs@FaABw@B{@Du@B{@FeBBm@NmENiEFqBNiEJwCJ{CHgCDmAX}IDiAFiBFeBFuABy@^kIHsBLkCHaBb@{I\\cGX_ELiBLcBHqANuBXiD@SJwALwAdAkLH_AHaA`@qETcCPcBt@}GZqCPaBR}AReBR_B?CRyA^}Cx@kGHs@Ju@Ly@Ly@Lu@Ly@Ly@nBwMLw@Jw@Hu@Hu@Hy@Hw@F{@Fw@Dy@Ds@?GDw@By@By@@w@@{@@w@?{@?u@A{@?w@Ay@AWAa@Aw@GqC[yPIsECy@Aw@A}@Aw@?y@?y@?{@?w@B{@@u@Bw@Bw@LeBBq@Dy@Dw@@YB]Du@Fw@Fw@Fw@D{@Hu@Fu@x@sIFi@Fm@Fi@Ba@Dk@Fg@Bc@Di@Hi@Di@Fg@?CFk@Fk@JsA^eF"
                            },
                            "start_location": {
                                "lat": 41.069386,
                                "lng": -75.4001818
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "12.8 mi",
                                "value": 20675
                            },
                            "duration": {
                                "text": "12 mins",
                                "value": 698
                            },
                            "end_location": {
                                "lat": 40.9064994,
                                "lng": -74.1639584
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-80 E</b>, follow signs for <b>Interstate 80 E</b>/<wbr/><b>Paterson</b>/<wbr/><b>New York</b>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "chkxFdp}dMHUTqBXiDD_@BYB]@]B[B[@]BY@_@@[@]@]@]@[?]@]?]?[?]?]?[A]Ae@?wACe@Ce@Eu@Gm@Go@Iu@Iu@Mw@Ms@Ii@Mi@Mo@Qq@Qs@Ss@Ss@Uo@Us@_@eAUq@Uq@Wq@Uq@[}@Wq@Y{@Uo@Uq@Um@GS[_ASo@a@gAKa@Ma@Me@Ic@Qw@Ka@Ki@Ic@[cBE]COUkBSgBCQCYCSEw@SgDEwAEcBA{@?o@?sABcCDiBHgBHwABk@B_@XcGDq@H{Ah@uKLgCFgBBc@JsBTiE?KDi@Dw@Bo@Du@Bk@FaADq@Bw@Dy@Ba@B{@D{@BsABeA?UAiAAuAA]Aw@GqAEq@Gq@Eo@Ec@OsAMcAUqAQcA]_BWcAKc@Uu@]eAQi@m@{AYo@Yo@a@w@a@u@a@q@QWi@y@IKW]W[a@g@QUm@q@aAaAYYw@s@u@m@aAq@}@m@e@WwAw@s@]e@Sy@[m@Us@SaBc@m@OYGGCUEqBc@mGsA{HcBa@I}A]iCi@sAYWGyA]kCi@{FoAqBc@_@KqCu@gA[kBo@cAa@i@Sm@Wa@Sc@Qw@a@GEq@]kAq@q@a@o@c@QMMIe@]m@c@k@e@GGu@o@gAaAg@i@o@o@IK[]IIy@aAq@y@QUoAcBW]QWa@k@cA{Aq@eA]k@Wc@U_@e@y@m@cAy@}Am@gA_@w@y@aBgA}B[w@Ue@O]mAwCaAeCSk@u@sBaAyC}@wCg@eB_@qAAEIYCK]uAOi@g@yBS}@e@uBACKk@WoAy@kEQiAKk@QeAYoBWkBMy@K}@OwA]aDWgCC]I_AM}AOyBG}@GoAAKEw@OuDEgAE_AAg@Ao@Ck@C{ACcACaC?m@A_BAuCAuD?YAgCAwC?qBA{@AsDA{DAcCAwFG_VCwLCqGIg[E{PAuAAuAEmGG{DMoGMwEUwFKwBKwBCm@Ek@KeBS_DC_@Ck@Gq@OuBAUSkCCSEi@KmAG}@E_@a@mE]wCGYCSIeAAC[oCIq@YsBQwAm@qEg@mDESIm@cA_HCKCQIi@AACQE[Km@w@aFMw@QgAMs@SiAi@sDS{AIm@_AoGIm@Ic@?Im@eFc@gF]iDo@kH?AU{CYwE?AQeDAMGsA?OEs@A[A]Co@?KIqCGwCAs@?WAwA?kABsADeA@m@HwADm@Dk@NuAJ_AHk@He@F_@Ny@Je@d@aC~CaNr@_DHYP{@ZqAj@iCVqARoAPqARoARqBDs@F}@?C@]@e@B}@@_A@eAAoCCu@G{ASmFGmAE_AYsGAOMoDUmFYoHSmFGuBAa@AsA@e@FuA@QDo@Hw@DYFi@Lw@Ja@BKT}@z@qCt@gCLa@No@F[Ps@N_AHm@NyAJqBBkA@yAC{ACwAOcBUiB_@uBa@aBm@aBMWe@aAe@{@OYq@cA_@g@UYm@i@[WYWi@_@q@c@o@]UKa@SiAg@{Aq@CA}BcAwAu@_BaAOKy@o@WSSQa@YAAs@m@_A_As@_Ay@kAU]c@y@OYOYEIKUIS?AEI[}@Sm@Uu@_@aBOm@YuAEUKe@a@kBCGKk@c@oBc@eBU_A]iAeA{CGQu@qBc@gAi@iAm@iAe@_AMUoA_Cu@_BYu@EKISQk@ACMk@Qw@Ou@Km@OqA?CGeAGmACsACsCCqD@qHHsDJkDDs@@]HeABa@PeCRgB?A?AHw@?A@GJaA@A?CJ_ARuBf@}EHeA@I@K@K?ABQ?EFk@\\kDLeAD]@GD_@P_B@Q@A?EDWZyCFi@@OJcA?ED]DY?E@AB[JcABOdAoK"
                            },
                            "start_location": {
                                "lat": 40.8590554,
                                "lng": -74.37587409999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "3.8 mi",
                                "value": 6075
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 217
                            },
                            "end_location": {
                                "lat": 40.9031782,
                                "lng": -74.09525630000002
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-80 E</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "sptxFvctcMHs@Do@LqAPyAL{@Lo@J_@@IH_@HWBGDSHWHWNe@LYJUHQJUVa@P[Zc@DGRW`@k@~@gAr@u@bAkANQPQFGFIHKT[l@w@h@s@Vc@d@{@d@aAZu@Vq@Rk@Po@FSNi@DOF[Li@N_AF[Hk@@IHy@Fq@H_ANaBRaCV{Cp@eIRmCLuAL}AJkAF_A?CV{CHiA@OFyB@iBAiB?QE{@GoAEu@QoBOsAScCIo@QiB?A?C?AACCU?AEi@_AeJQiBe@uEC]AEAMGq@O{AMsAIaAG_AIqB?EAq@?]@{@H{FFmAB[H{@PqBLkAD]PaBHaAf@cFTkBHoAF}@Bs@?g@?I?{@?W?A?A?]Ag@Aa@Eu@Iu@Iq@E]AGKq@Kk@GYQw@_B}FaAiDGWAAYiAg@kB_@qAOg@CI_@{Ac@uBAE_@sB]{BMeAGa@?AOkASuBQwBG{@Cc@CWCy@GyAA[EqB?AA{AAY?uB@s@?_@?a@FeCBqAViKFiC@W@Y?O@a@@a@?K@WNiFDsB@k@BcABy@?S?C@c@LuE\\iOH{CFiDJkF?a@@U?ATuI@m@@o@FoC"
                            },
                            "start_location": {
                                "lat": 40.9064994,
                                "lng": -74.1639584
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "5.4 mi",
                                "value": 8642
                            },
                            "duration": {
                                "text": "5 mins",
                                "value": 290
                            },
                            "end_location": {
                                "lat": 40.8653029,
                                "lng": -74.0172371
                            },
                            "html_instructions": "Keep <b>left</b> at the fork to continue on <b>I-80 Express E</b>",
                            "maneuver": "fork-left",
                            "polyline": {
                                "points": "{{sxFjvfcM?uA@a@LuFJiDJwBHwADy@@CViDXqC@I\\{CDWHq@Jm@RwA@ATwA?AN{@TgAVsADQ`@gBj@uBb@iBVs@Pm@To@\\aABITk@p@qAv@kAh@s@T_@VYPS@AJKh@g@JGd@_@n@e@n@[l@[TIFCNGJEb@Mp@Q^KZGz@SpA_@|@Yj@Sj@Wd@Wt@e@RMNKVQJKTQPQ`@_@NQPSZ]l@w@JQ\\k@b@u@f@aAb@_AVk@hAaCDGh@eAn@cAr@_Ad@g@t@{@^c@rB{B|AiBJIZ_@pAyAFG~@cAJMZ]j@q@`AeAv@}@Z]DEnB{Bj@m@\\a@|A_B|@_A`CiCDGBCNQd@g@@A`AaA|@u@f@c@b@[`Ai@bAe@l@U`@Ov@WpBq@fC}@pIsClCcAnCeAbCgAf@STKlCsAj@]x@e@DChBcAv@e@^WHERO^Ud@YXSh@a@RMl@c@jA_Av@k@z@s@hB}ALKVSDEZ[ROf@e@@A|@{@FGl@o@t@u@PSjBqBr@y@BEPS^c@^e@b@k@t@aAf@y@PWh@_ABINWFMJSVk@Xq@@ATm@Ri@L]?AJ]Rq@Ro@Nq@Li@Po@VuAJs@Hk@Js@BWBQB[Fu@De@HgAHmAFcAB_@HcBFqA@IDiABi@?MHoBFuAJcDBuA@[B}@BaA?_@@Y@]?W?W@A?c@@a@@u@?q@@]?c@?o@@g@?g@?Q?a@?c@?I?A?q@?IAq@?k@?E?i@A_B?G?e@?o@A_B?eAAU?A?EEkGAkBC_FAo@AmC?o@Ao@C}D?m@CeD?M?e@?e@AyB?U?e@?A@iA@g@?YBaA@mAFyB?A@CBuAFgAF}A@UJiB@M@UHiANmBhAuNDm@RkCDm@@KDc@Dm@@SBYFo@HiAf@{F`@iFVgDb@kF"
                            },
                            "start_location": {
                                "lat": 40.9031782,
                                "lng": -74.09525630000002
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.6 mi",
                                "value": 964
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 33
                            },
                            "end_location": {
                                "lat": 40.8663097,
                                "lng": -74.00623829999999
                            },
                            "html_instructions": "Take the exit on the <b>left</b> toward <b>I-95 Express N</b>",
                            "maneuver": "ramp-left",
                            "polyline": {
                                "points": "colxFvnwbMfAaOFy@HwADyA?E@i@B}A@i@Cq@?SEoCEmAAMAIKgBKiAOiAWmBSiAKe@Ia@WkAYkAIUSo@_@eAMYi@}AK]"
                            },
                            "start_location": {
                                "lat": 40.8653029,
                                "lng": -74.0172371
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "2.6 mi",
                                "value": 4216
                            },
                            "duration": {
                                "text": "3 mins",
                                "value": 164
                            },
                            "end_location": {
                                "lat": 40.8597641,
                                "lng": -73.9753126
                            },
                            "html_instructions": "Continue onto <b>I-95 Express N</b>",
                            "polyline": {
                                "points": "mulxF~iubM]w@i@cAm@eASYW_@c@q@[_@GIoB}BwE}FqA_BoCkD{AkBa@g@qAgB}AaCyAiCuAiCEK[o@o@wAk@uA_@aAMWWw@}@oCCKkAsDYgAm@aCGUUaAYuAGWKk@G[CQKk@G]O{@G_@AMIm@Ga@Q_BOcBK}AC}@CuA?a@@qABw@FsAHiAFu@NcAZgBTcAH]Li@Nc@L_@DOPe@d@iAVk@@Ad@_AZo@Tc@JSJQv@wAZi@b@s@@Ch@y@\\i@R[d@q@f@u@j@u@NQLQT[l@u@~@iAf@k@f@i@b@e@h@i@f@i@p@m@XYXWhAaA@AxAkA\\YBCx@m@h@_@z@m@rA{@jAq@hAo@l@[FCx@a@h@WzAq@HCv@]JEJCLGXKJCr@Uh@MRELATEd@Gp@E^An@Af@Bv@FZDr@JTDXFVFPJdBTt@Lr@Lz@PbDn@j@J"
                            },
                            "start_location": {
                                "lat": 40.8663097,
                                "lng": -74.00623829999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.8 mi",
                                "value": 1214
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 83
                            },
                            "end_location": {
                                "lat": 40.8538876,
                                "lng": -73.96433399999999
                            },
                            "html_instructions": "Continue onto <b>Interstate 95 Upper Level N</b>/<wbr/><b>NJ Tpke N</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "polyline": {
                                "points": "olkxFthobMV@d@?b@Af@ELCRC^KBAb@OLIZQFE\\U`@_@RWX[RYZe@@CJSPW~CoF`@o@LYVc@Xi@\\u@\\w@p@cBPm@Rk@?AV}@HWFYPs@Pu@No@Nq@Js@Lq@BQD[?C@KD]@KJqAP{BBQXsCPsAHm@Fa@Fg@VkB"
                            },
                            "start_location": {
                                "lat": 40.8597641,
                                "lng": -73.9753126
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "1.1 mi",
                                "value": 1761
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 102
                            },
                            "end_location": {
                                "lat": 40.8499249,
                                "lng": -73.94406529999999
                            },
                            "html_instructions": "Continue onto <b>U.S. 9 N</b>/<wbr/><b>Interstate 95 Upper Level N</b><div style=\"font-size:0.9em\">Toll road</div><div style=\"font-size:0.9em\">Entering New York</div>",
                            "polyline": {
                                "points": "ygjxF`dmbMF]@KJmA@ITkBDYD[^kDh@iEFo@@EFg@?A?CFg@?C@AFk@Fk@Hq@Fk@?AFk@@AB[BO?AD[@O@AB[BO?AD[Hw@ZmC?AHm@LkAHm@@KHm@Da@@I?AFa@@I?ADa@@Kd@eE\\sCB_@BIBIFm@@?Fo@BOD]Fm@Fc@@IDc@@IHm@Fm@Fc@@IDc@@IHm@Hm@Dc@@IHm@Dc@@IFc@@IDc@@IHo@Da@@IFc@@KFm@Fa@@KDa@@KFa@@KDa@@KHm@Fm@Fa@@KDa@@KFa@@KDa@@KFa@@KBYDWBUBYBSD[@QFe@D_@@IBO?A@Q@C@GDa@@G?GD]@K@GBM"
                            },
                            "start_location": {
                                "lat": 40.8538876,
                                "lng": -73.96433399999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.8 mi",
                                "value": 1295
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 90
                            },
                            "end_location": {
                                "lat": 40.8457486,
                                "lng": -73.92980489999999
                            },
                            "html_instructions": "Continue onto <b>Interstate 95 Upper Level N</b>/<wbr/><b>US-1 Upper Level N</b>",
                            "polyline": {
                                "points": "_oixFleibMN{A?CFi@@GBW@I@C?AFi@?AHk@BS@Q@GBSDYFk@Hm@Hm@?CFm@@CFi@Hy@NoA`@qDFk@Fg@Js@Hm@PyA?AHm@PyA?A@AFk@@AJk@Pm@Rq@@GHSJ_@?ABGb@sAd@yAXaAFQr@{BRk@Pi@To@HWX}@X_An@qB`@sAHYRs@@C?A@?BO@A?EBKDU@MBM?A?A@GDS@K?A?A@C@GN{@DWF]BMNo@"
                            },
                            "start_location": {
                                "lat": 40.8499249,
                                "lng": -73.94406529999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.1 mi",
                                "value": 197
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 14
                            },
                            "end_location": {
                                "lat": 40.8452163,
                                "lng": -73.92757089999999
                            },
                            "html_instructions": "Continue onto <b>I-95 N</b>",
                            "polyline": {
                                "points": "}thxFflfbMPiAHi@T{AFc@@GJm@@IFc@FYBQ@EBYDY"
                            },
                            "start_location": {
                                "lat": 40.8457486,
                                "lng": -73.92980489999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "3.4 mi",
                                "value": 5486
                            },
                            "duration": {
                                "text": "5 mins",
                                "value": 281
                            },
                            "end_location": {
                                "lat": 40.8052013,
                                "lng": -73.92058209999999
                            },
                            "html_instructions": "Take exit <b>1C-D</b> to merge onto <b>I-87 S</b> toward <b>Queens</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "sqhxFh~ebMT[FMHOHMDGHKHKFIHKJOHKJKFKJOFMDKFQDQBM@I?K@K?IAMAOEWCMEICGEGEGCEGGEGIEGEGCICCAEAG?EAI@G?G@G@GBEBGBGDEBEFGDEFO^CJCLCN?DAL?J?N?H?JBT@LDNDPDNFNHNDFFDFFFD\\T`Bv@`@R^P`@R^R`Ad@`@Pd@VPHPFPFPHRDXFVFJBL@LBR@N@XBP?XBVBTBF@N?bBf@b@PpBbAn@XbAh@n@Xd@Rh@Tb@PB@`@ND@h@RRFVFHBZJj@Nn@Pl@Nf@Lh@Lh@J`B\\vJfBr@N`APnATLBlB\\`ARnATTDB@PBTBVBF@^Bd@@P?^AV?RC~@Il@KTETGNGXIf@SXOhAi@HEJGRI@?PINGBAPGl@MRCf@GPARCPAP?P?b@AN?P?P@^BL?\\F\\D\\DP@t@DR@V?PATAv@CHAP?PAh@Cn@CP?pAGz@C@?`@Ch@A`AEdAE@?b@Ch@A`AElAEpAErAG\\A\\A|BIp@ElAE`@AP?B?T?T?V?P@TBT@TDTBb@JZFRDTDL@H@PDTBT@T@T@T@TAR?TATATARCl@E`@KVAPCRAR?T?Z@R@P@H@RBRDTDPDhAVTFbAVzA\\RFRDF@LDH@L@PBRBX@R?T?VAVCRCTETERIPGTITMPKZSPMLKNQNQLOPUjAcBpAkBj@w@@CX_@V_@@EV]BCl@_Ah@u@NULSLULULWFIDKLUJWLYJUHWL[La@Pm@Rm@f@eBz@sC?An@}B`@sAV}@x@qCh@cBv@iCBIn@wBJ_@L_@J]"
                            },
                            "start_location": {
                                "lat": 40.8452163,
                                "lng": -73.92757089999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.3 mi",
                                "value": 555
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 33
                            },
                            "end_location": {
                                "lat": 40.801706,
                                "lng": -73.91704969999999
                            },
                            "html_instructions": "Take the <b>I-278 W</b>/<wbr/><b>Triboro Br</b> exit toward <b>Manhattan</b>/<wbr/><b>Queens</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "ow`xFrrdbMLUN[Pe@DKBEBGLULULYHUXq@JYJ[d@oABKRg@J[Vu@FMTo@@EBI@AFKFMFMHMHKHMFGDEHIJILKLILELGPENCRCNAB?P?L@H@H@HBPBB@JDD@HDRJNF\\L"
                            },
                            "start_location": {
                                "lat": 40.8052013,
                                "lng": -73.92058209999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "3.1 mi",
                                "value": 4957
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 244
                            },
                            "end_location": {
                                "lat": 40.7687427,
                                "lng": -73.9081364
                            },
                            "html_instructions": "Merge onto <b>I-278 W</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "merge",
                            "polyline": {
                                "points": "ua`xFp|cbMd@Z^VPJxAbA`GxDr@d@VPVPBBjD|BPJrBhA`At@PLBB@?DD@?NLFBd@\\n@d@h@`@FBpAbALLLJz@t@B@\\XVT?@FDB@LLd@`@f@`@RNRPTNBBTRB@TRFDNNLJHFNL@BJHPN?@B@VTVRVTTRDD@BDLn@j@h@b@BBXXLHDBRN`ElD\\XrAlAZVXVh@b@h@d@`@\\DDDFl@b@@@TTrD|Cj@d@LJ\\ZZV\\XZV^\\|@t@TRFDFFTPPNJFNJNJFDNHHBPHb@P`@L^HD@NBJ@VDV@L@N@P@@?P?^Aj@GXCb@INCHCPEBAVI`@QXMHGLGl@c@d@[rDiChAy@xByAFGBAJGFENMzB}A|B_BzB}AtByATOJG@CXQBCJGt@i@PMROtB{AtAaAJGJIVOpA}@JI^UXQj@a@XSHGHERORMPOPMd@a@RQRQRQPS`@c@d@k@\\c@b@o@Xg@PUHMDGLWlAiBn@eAp@cANWr@oAd@w@LWHMp@eALQ?APWRURYTYLQJOLQ@AJMJQLSBEDIBELSBIFKHSFOFQDQDODQDSBQ@G@IDY@G@QDc@f@aGTgCLuAT}BJoAD]Fy@Jy@@GFg@DSD_@PwANqANiBFaAF}@DwA@wA@k@"
                            },
                            "start_location": {
                                "lat": 40.801706,
                                "lng": -73.91704969999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.4 mi",
                                "value": 642
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 39
                            },
                            "end_location": {
                                "lat": 40.7650428,
                                "lng": -73.90329919999999
                            },
                            "html_instructions": "Take the exit toward <b>I-278 W</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "ssywFzdbbMDMDQBo@Fs@LmAHs@Ho@BKLw@RgAP_A?ABMBIDOJa@J[JYFMBIP[BEDEDEHIJKPONKFE@?DCFCFCHELCNGPGDALC@A`@MPGHCXK^K@AVGPGBAzAg@dBi@"
                            },
                            "start_location": {
                                "lat": 40.7687427,
                                "lng": -73.9081364
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "3.0 mi",
                                "value": 4820
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 229
                            },
                            "end_location": {
                                "lat": 40.7352736,
                                "lng": -73.91921549999999
                            },
                            "html_instructions": "Continue onto <b>I-278 W</b>",
                            "polyline": {
                                "points": "o|xwFrfabMt@WzAe@TEl@QbA[BAjCw@r@U@ALEz@Up@OfB[v@K@?`@GFAx@MhBYnAQZE\\GfAQTCJCd@IbASl@OREDAj@K`@O@Ad@ObBu@d@UVM`@U`@S^U`@Sd@Wb@WZ[rAu@b@Sf@YfAo@ZQ\\Qd@U\\UlAu@@?\\U^Uh@WXMLERELCTEFAXCTEn@EbAID?\\Cd@ERAHCf@Ib@KHCFANGZKNGPM`@QRKr@]NGf@WTMRKf@YLG@A@?@ABA`@S@?@A@?@A@AXM\\Q`CmAj@Y\\QXKLG~@a@t@]bAe@l@ORCTC^CT?N?b@@`@DLBNDF@F@NDPDTHLF`@TXPf@`@FDHHLLPRLLjBbCDJd@l@d@n@dB~BVXh@p@f@l@j@v@X\\f@p@JPFHBBDFHJ@B@?@BNRJNRVfApAZd@JLFL`@j@LVR^Vf@j@lATl@Rn@V~@\\rA^tAZhAZjADRBH@BJb@f@hBHLDN|@fC|@jCNb@DNDJL`@Tx@H\\FRJh@Jn@Hb@F^DZBRDh@L|AB\\@NFz@Dn@\\zEDl@\\xE@NNlCPlCPhCHl@Db@@NDv@\\|EDl@?@@\\F|@@LH~BBx@HhDDf@Bh@Dx@"
                            },
                            "start_location": {
                                "lat": 40.7650428,
                                "lng": -73.90329919999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "2.4 mi",
                                "value": 3908
                            },
                            "duration": {
                                "text": "4 mins",
                                "value": 221
                            },
                            "end_location": {
                                "lat": 40.7134256,
                                "lng": -73.95403519999999
                            },
                            "html_instructions": "Keep <b>left</b> to stay on <b>I-278 W</b>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "mbswFbjdbMB\\D\\?@@NBRDn@BZB^@H@NBTBTDTHl@PfALh@H\\FTJ\\HXFTFTBFLj@L^HXHTLVJVLVJR@BLZLXJR@BHPJP@?v@~@VXt@p@DD\\VXRRLDBZXJHJJb@`@x@f@HDbAn@`@TXP@?zE`CtCvBHFFDVP@BRPPR@BRTNPPPNRNPLPLPNRLPNPHJDFPV@@@@DHPRJNLP@@JNJNBBPV^d@TX^b@?@X`@@?V^B@HNNTFJFLPX@@R^R\\P^@BXl@FPLVJXNf@HTDNDRLb@@F@DBPFRP~@R~@FVH\\@DJb@BNBLVhAJf@Lf@FZXbBDXFZHb@DVj@jDF\\ZvAXpA@BZbAj@vAx@hBd@dA?@d@|@`@|@d@|@bBdCp@hA^j@FJTb@NZVf@Vj@t@zArApCd@|@Rb@b@z@^r@xAnCj@jAzArCHNDHxAxCDFT`@Zl@RZJRLRf@|@Zf@`B|CNVLVDD|@zAXb@^l@l@|@l@|@LPVZBF^d@X^BDTZBBHJf@n@HJNPbAjAn@t@HJDFRTZ^n@z@"
                            },
                            "start_location": {
                                "lat": 40.7352736,
                                "lng": -73.91921549999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.7 mi",
                                "value": 1125
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 64
                            },
                            "end_location": {
                                "lat": 40.7043058,
                                "lng": -73.9596028
                            },
                            "html_instructions": "Keep <b>right</b> to stay on <b>I-278 W</b>",
                            "maneuver": "keep-right",
                            "polyline": {
                                "points": "}ynwFvckbMRRb@f@JJNP^b@j@l@FFLLDD\\ZPLLJp@d@NLr@^NFRHJDPFNDTHhB\\VFVF\\Nb@PVLXNPJjBz@p@ZfBx@PHp@ZLFxCtAl@ZfAf@|At@BBzBdAB@|@b@XLTJTLVL`@R^P"
                            },
                            "start_location": {
                                "lat": 40.7134256,
                                "lng": -73.95403519999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.2 mi",
                                "value": 333
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 63
                            },
                            "end_location": {
                                "lat": 40.7016756,
                                "lng": -73.9614503
                            },
                            "html_instructions": "Take exit <b>31</b> to merge onto <b>Williamsburg St W</b>",
                            "maneuver": "ramp-right",
                            "polyline": {
                                "points": "}`mwFnflbMHNBBFDFBj@Zp@^ZNj@ZHDJFHD~@h@`Af@JFZTDBJHPL\\VHFRT^T"
                            },
                            "start_location": {
                                "lat": 40.7043058,
                                "lng": -73.9596028
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.2 mi",
                                "value": 325
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 105
                            },
                            "end_location": {
                                "lat": 40.6994152,
                                "lng": -73.9590283
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>Wythe Ave</b>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "oplwF`rlbMJKNONO?AJK?AFE@Ch@m@`AgAtB_CHMx@_Aj@q@RWDE@CFCDAD?"
                            },
                            "start_location": {
                                "lat": 40.7016756,
                                "lng": -73.9614503
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "272 ft",
                                "value": 83
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 31
                            },
                            "end_location": {
                                "lat": 40.6986808,
                                "lng": -73.9588789
                            },
                            "html_instructions": "Continue onto <b>Franklin Ave</b>",
                            "polyline": {
                                "points": "kblwF|blbMzBYVC"
                            },
                            "start_location": {
                                "lat": 40.6994152,
                                "lng": -73.9590283
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.3 mi",
                                "value": 472
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 129
                            },
                            "end_location": {
                                "lat": 40.6993957,
                                "lng": -73.95336209999999
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>Flushing Ave</b>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "w}kwF~albME[WyCEUUqCE[OqCCc@?YQyCSqDUyD"
                            },
                            "start_location": {
                                "lat": 40.6986808,
                                "lng": -73.9588789
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "1.4 mi",
                                "value": 2223
                            },
                            "duration": {
                                "text": "7 mins",
                                "value": 410
                            },
                            "end_location": {
                                "lat": 40.679636,
                                "lng": -73.949585
                            },
                            "html_instructions": "Turn <b>right</b> onto <b>Nostrand Ave.</b><div style=\"font-size:0.9em\">Pass by Key Food Supermarkets (on the left in 1.0&nbsp;mi)</div>",
                            "maneuver": "turn-right",
                            "polyline": {
                                "points": "gblwFn_kbMhAMtC]fCYHAdAMpC]F?lC]F?tAQ\\ETA`CYFCJCxBWB?NCHCJAd@EtAQPA|@KRCn@IdAMjAMv@KBAlAOD?rC]lBUb@EjC[F?pC]bC[L?pC]hAOhAM`AKnAOv@KxAQbAMlAMpC]rC]`BQp@IpAQJCFAFAFCPKtCL"
                            },
                            "start_location": {
                                "lat": 40.6993957,
                                "lng": -73.95336209999999
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "0.3 mi",
                                "value": 469
                            },
                            "duration": {
                                "text": "2 mins",
                                "value": 145
                            },
                            "end_location": {
                                "lat": 40.67933600000001,
                                "lng": -73.9440398
                            },
                            "html_instructions": "Turn <b>left</b> onto <b>Herkimer St</b>",
                            "maneuver": "turn-left",
                            "polyline": {
                                "points": "wfhwFzgjbM^gPDeCTeL"
                            },
                            "start_location": {
                                "lat": 40.679636,
                                "lng": -73.949585
                            },
                            "travel_mode": "DRIVING"
                        },
                        {
                            "distance": {
                                "text": "423 ft",
                                "value": 129
                            },
                            "duration": {
                                "text": "1 min",
                                "value": 77
                            },
                            "end_location": {
                                "lat": 40.678183,
                                "lng": -73.94416129999999
                            },
                            "html_instructions": "Turn <b>right</b> onto <b>Brooklyn Ave</b>",
                            "maneuver": "turn-right",
                            "polyline": {
                                "points": "{dhwFfeibMpBHh@BHBX@X@L@"
                            },
                            "start_location": {
                                "lat": 40.67933600000001,
                                "lng": -73.9440398
                            },
                            "travel_mode": "DRIVING"
                        }
                    ],
                    "traffic_speed_entry": [],
                    "via_waypoint": []
                }
            ],
            "overview_polyline": {
                "points": "etveFtahiVswSl~GadOebBaaOqsLa}Zg{Qkm_@gme@st\\{we@}bLsde@m}Nwdh@ipk@ugs@klWq_QqnRafIaxHs}QusZebm@pOq_cAkiHqk`@qsDalGwdO{bE}sHsdc@~oCcbYmiFm`SozFcjd@muCulX}sVguc@{mTkmW}mUwsl@yjWc{QqySir]iua@ol[kbo@ofMwgOypb@st`@krTwyHi~UmuLgw[p{A{qZxkPokp@pmc@eas@hxPyub@u`Kudb@n_@gze@r`DclW_}Ni{j@p{@s_VumLinTwl[kgf@olEwgi@s|LuoNg|LqpnAbeEqgcAhxPmyf@tza@sjo@bkJ}aRda@eoj@rlAsnyBsnLcht@gfCwnLtsJabUbrMkh`AksFaju@}Mmjo@wlDcu{@fvDykN}tJqmJujKs{LqdQ`iC}cIgk@gbHqeMchPau^cbSm_O}oEe~ScoEmpv@{rJkwbAgt`@yplAa`FqdnA`vFgfSsqJ{}c@wvOolx@mc@eeh@hwEo{q@{vJ_goBsmPcojCtoIujiCbrTqfl@fi`@_`v@zgSyz_A`mQyxd@rqLcgDxlKokXrdBwry@k`ImivA{k@a|wA{mFk~eAxH}qsAlaP{}pAfWo}{@vuJ{`b@pwAupo@csJsl_AiwAu`uAob@omeBb`W_`bB~ic@{xtAn}Oujf@fzCego@t|Cq_rAwiRagwAe_Jokl@~Riz_AQolqD|J{_i@}zFkm]umOqix@wl[{w^}uXsn`@g_Aw~n@em^ksa@smSmpVvEsh|ApSazaDimKwz~@a|GiuXkoHgiPuwDafdAhAc`hAg|AylkCpx@gmqChhIstnBj{Duml@`nQsrAncKynUak@kxW|{FkdkAlmDav~@czA{rp@dlE}rcAqu@{v_B}_RomhAy`Oqe{Ae_Fi~fBxrBq{c@efJuyo@ixOm~b@czDaag@niBmx}AgwBcjmBgMiwo@veL{sj@z~Km|l@rnCc`aBrJghuArcOw_x@vn^olrBhhBo{gAqnJqf_AvhTwgzAbfIy_dChiV{}Y{zHwqd@itE_orAfcB}_wAkR{xwBjrG}_`@|`A{|t@njJsgj@h_Mmug@hsEc``@a_Keg^haNaqf@}sQ{tt@mgD_tnAbj@mq]|vHa}T~g@g`p@u[{_n@o|Bolj@{kHguxAdeAokj@j|IyuPdhDm~SnqAyjLfrG}xEoI_we@~dF}ha@jW_sm@bkDc|OycDeeLa}Akje@`}Euz[~`GyrGriKiuDpaKrgJlhCw`B"
            },
            "summary": "I-80 E",
            "warnings": [],
            "waypoint_order": []
        }
    ],
    "status": "OK"
}
```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/distancematrix/json?units=imperial&origins=CUNY Graduate Center&destinations=Metropolitan Museum of Arts&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8
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
https://maps.googleapis.com/maps/api/distancematrix/json?units=imperial&origins=Oakland,CA&destinations=Brooklyn,NY&key=AIzaSyBxMGOjXaBIg42zO1bJAFbDeTeLCix5Vr8
```
```
{
    "destination_addresses": [
        "Brooklyn, NY, USA"
    ],
    "origin_addresses": [
        "Oakland, CA, USA"
    ],
    "rows": [
        {
            "elements": [
                {
                    "distance": {
                        "text": "2,916 mi",
                        "value": 4692910
                    },
                    "duration": {
                        "text": "1 day 19 hours",
                        "value": 154241
                    },
                    "status": "OK"
                }
            ]
        }
    ],
    "status": "OK"
}
```

## Already done?
Play around with some other public APIs. [Here is a great list](https://github.com/public-apis/public-apis).
