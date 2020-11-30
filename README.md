## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
GET https://maps.googleapis.com/maps/api/place/findplacefromtext/json?input=Museum of Metropolitan Art&inputtype=textquery&fields=place_id,name,formatted_address&key=AIzaSyB_qbjwcLagyna7J6zK7Y3s0NErk90I360
```
```
{
    "candidates": [
        {
            "formatted_address": "1000 5th Ave, New York, NY 10028, United States",
            "name": "The Metropolitan Museum of Art",
            "place_id": "ChIJb8Jg9pZYwokR-qHGtvSkLzs"
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=opening_hours&key=AIzaSyB_qbjwcLagyna7J6zK7Y3s0NErk90I360
```
```
{
    "html_attributions": [],
    "result": {
        "opening_hours": {
            "open_now": true,
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
GET https://maps.googleapis.com/maps/api/place/findplacefromtext/json?input=CUNY Graduate Center&inputtype=textquery&fields=formatted_address&key=AIzaSyB_qbjwcLagyna7J6zK7Y3s0NErk90I360
```
```
{
    "candidates": [
        {
            "formatted_address": "365 5th Ave, New York, NY 10016, United States"
        }
    ],
    "status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=photo&key=AIzaSyB_qbjwcLagyna7J6zK7Y3s0NErk90I360
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
                "photo_reference": "ATtYBwIZIFFonfffmJC7mPnXa2s0XgSHHOye5Hxi-T5hi73VpjPpjN19vZGc7UVaQo5y9UNsp8R-QsYofU7_fVbTbBKQPKwV10kOhx0k2z2NmtY0v-sHDLgT1MmIuCO-VJZP6aFYjSf_9s8Z7U_bFoOWFjg3BgMn_KreyZoCuMHEVAs5DzUq",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwK2AIROF1jaETN2j0_ZxGbvyjwaKKHYW7rblJy8FXMgZ4l1lzNAsdgFq3gShP3C92LH8tu1IBrqKZZ7VJwibATUAAu6Hgyk8GYY4QFAjYUuvcLWghq-WgGDwNOxAa2G7GoFUtYiR1h5sfb3Nx61hxrYWOKI42fgojH8Z_mTrt8BBvkD",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwLz1yg0cB6G3KvP8bfxH_XIh6xDwTzeja_-w6wQ2yifBSZlP2fmesbG1yywZSffpqveizTHlN3t1o-Xj37-1MorO7DwfCasB0dKzFcxZ67mVEvdlHjGSpWhCuKoHWsJqQjr4mKabN8qqKUMlZJ4ia31Gn46DkFEuEXq9f3fcj29vS8V",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwLu86eLILwXj3RZXzDO2NXtVe2ItzMbMXrLkYwLrQjvj5sDqSZKpYMp0WsoShhZAuGYpF4YZC0gxIDzFFF27jaFP0qElLTWxMNg_xCMEeFAhIMDyn3SL1P6yIUKZJ05saLoF7Ir4wNbtLUQRQ7ceE_pwltKQhIFjPTOLWJwraeXl2ob",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwLLLKIZRj5zaDwIajiBzfRjv1JdFfTPmPSSTu9sbV4D3OBy3qMX537pQH1u2UQwdc4OBSrfb72aHK-NURDpkygGiLeVOKJVmQCLWJZ_A-BRMGxTSWv39FHQ8be4-LRBXJ1BCjNHh2QEnPB4aZBYaRXHXAJw8SPXmG9VjL2K9Vum4XJw",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwLHm7WLfVtz-WO1jhsvOqmuwvp4u00NMYemoECfkdYjzE4FK-1xeA080P2mVXuo_SX2Z7ggGYIwwXPt2-sKrXOgYOVAvcRDVAWNu-jBw9jmDkeAAnByGp93Us-puTB_pYmSFgELOMADwP-0H1fRiyqdrK4_Bkm4GX10h7ZcS0PCQRyY",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwK80UFaw85GZLe97WWU-HvnaG3XPchVX1nujm9jMkjkLeQVWwwcHwEnSSotuY5IbnBrwuB_RQwr83OTuq_a7EvLeUraLoVsTfrCX0FlzLT-jGFjyWmWL2r0gRga-tRO8ZAULZXzrBhBiRu5CZRhBdPxwyutcSmGpvXDNHnQm4--ERAF",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwJotHWGDlyjrcrv4AxCxd20Le_7tcz6RWy8CqSu7aDB43U7jXCpGeGaPIYK6LtktAecsiRSvQB9kqZvVQiAhaKluJVVMXacGeZ35qmMM6WrnLQotjUUS7jXSgF0YS7bg_74T4i6aBBs_EU3w6LXDTY2zY4GTAhY42BFf5NBOjt7vQlU",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwK9Mgmdver177e9gByddkVjAgYBvoxD0BetQbaaeObaPSSIlVllg_ObXGIm1nhml4TueJu5xMT6UI3_NTY-A9aOwSH2T0zo4gq8byymbsujd4CW5CFRhCccnTuzrQK2fjBzseeAmfkbWmKV5hwwOVLiNpds5aK1947vD--T5SG2Qhmx",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwLnl8rksQe5JyAFZ_mMZntY_fr-fom2y-RA0NUNBC8NkwBbTPgKBdM8Z2I-bfAOXaubYBHg0RD-7EUN80eQCpNpy8os62gYuyQM0Wae5uhhnloyAJMOnldvog9bW_m9NAJOLICYezVwgrBEYmf5hFbo7-Lrx7rl5m8GVUoVExZRpK8d",
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
GET https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=40.8200471,-73.9492724&radius=10&type=restaurant&keyword=pizza&key=AIzaSyB_qbjwcLagyna7J6zK7Y3s0NErk90I360
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
                    "photo_reference": "ATtYBwIAi2ocVjR0nZB9mYRWk0qRypl0rez9JaFB4rcfBQCbwFfs4LCO78xzUW1CJpi2m96OvsLiZ9E2mn1l67sGXelHH1-z_i_woB1tFlriitRPrREZhFYMbpi3C8Sw9wB7PMB46ih2X8KgRnhkb_IHybmNv_3zrrVrl9jdpW4BfR--DQPY",
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
                    "photo_reference": "ATtYBwK39NydWeGxWSsWEi84BvyDdJ89XwiTxFYY2EXqjTdB4PRaR9XPJwyQnVKhYirAmnxNtwJty3VecQ8Nz40lILlD7WtIaHgXxcsq60pKQ01M9KduFCd7azw64drDburCXj3cAJpfOyDEn2bkLyRv8CX70h1PrYmEm7wrHuTrWrcXOMDY",
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
            "user_ratings_total": 869,
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
                    "photo_reference": "ATtYBwLZzFNOY9y0km1q_6Td5M-FaLiRmeg4HaXtQSDCoWngZzzpV57rLNBUphrx3HmUKmIGa-z2PCx9f9E8pc8uWak0LVVbIoj-zsmqu8p39O1tRFcrlXoYlahqrdUCq2bBH7f-_VT4tW4CPc-JG3r-JnFIQ5XTJ8PTz_jyf8Y41OmI1fup",
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
