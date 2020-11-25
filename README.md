## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=place_id,name,adr_address,photo&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "adr_address": "<span class=\"street-address\">1000 5th Ave</span>, <span class=\"locality\">New York</span>, <span class=\"region\">NY</span> <span class=\"postal-code\">10028</span>, <span class=\"country-name\">USA</span>",
        "name": "The Metropolitan Museum of Art",
        "photos": [
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115967679611787063919\">Richard Stark</a>"
                ],
                "photo_reference": "ATtYBwInEDATIVBE-WnHfDRPndVKX24_P255MUElzRMzb0KeKVa6YiU87303krn37wjjZnofGPzG22GKlb7cjbBgcOqC0oFXMZKKkadmD64N3uoESJrsGUWMb6zIZI2eClL00KQ30U9b2nJaAG8ns87y92AsxKFeVxnvEf2a-LrMr37uMApA",
                "width": 4032
            },
            {
                "height": 800,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106748439247716180853\">Karl 1974</a>"
                ],
                "photo_reference": "ATtYBwIHA7o7rD_b4Xm8cv5nEdYofgxL4hM_ovuUYFhA1ALNOKv85celzYzKoCqG45gp0JVa1c5U4Bi5sMQM2csI4AlA4mPl6XGcknUC7VCGznHXNVCaJyB2iVuue6BbeKrlmh3bKTOEK3aiJVM56KytmXLfL3WdhF_jMbSK0612rRR0uvmP",
                "width": 800
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/105280404763450371863\">Sabrina Nazario</a>"
                ],
                "photo_reference": "ATtYBwKpH_cFrGXVddVg2xPVFoVbOOrgeBTYCEOjAUkOqgTM98Bv1oVP_wBiGjlEfaitwMRgwHKmy-MVkRA2RA0YV8wdcSmoaVaDVrCle601TQIIdCB8VPSJ3EmTH52TeSnUXxSsE-uFx1gJFk2mri8w_Vvf0vRKtHhUkvr6IlEJj2_UU6Le",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114414941791922473064\">YehHsiang Chen</a>"
                ],
                "photo_reference": "ATtYBwJJe5ImO1fmecjFSibYnp8t7kyTABWtANDpZ602cGlqUmi2d_h44ivbFP9F2OhRb71GSQwq17Yg-EpF-8XLh9GiV9kQODwBQpnPO5FtBI1N1R7q4vZQhtP8aOEN8jJbHNDL9mph_Umc-Aeogh95GJ0hlali5NEGVs8MLpldOJgropWK",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114217576882578419305\">Eva Mikulcic</a>"
                ],
                "photo_reference": "ATtYBwI09uwGQyv5LyXo2kY0np9SPhT7fTe2zPYCwlhlc29ktkmny4FmxFSfOouvBjNcytDJoMDDdox1bfBb7HTHwxGoPtLzIKh3mRyTnK_H3RcMd4Y7jgwsClYL4ta1GOjiERPj86h0gnS6fRPhejTWyEn6jstn-0EJUaRmMu8-KgRobf2s",
                "width": 4032
            },
            {
                "height": 5304,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115568864800951782024\">Kenneth Hines, Jr.</a>"
                ],
                "photo_reference": "ATtYBwJPKsHwHJaNeU_CRXuAPWxoesGWVAWMx7E3WKiEVWSfCS_OTct8i2OOu_9IKKPA2h0awl5vCLeYChkGjEvIMH_9TPpzdTrs66FLB6HpOD8Tc_0EMupryw6hJoHXKUltKbPJo6b9SSL66zu8OfMudyRxcsPlVj89xSb_JM_ZwFbe58vW",
                "width": 7952
            },
            {
                "height": 3456,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108035579848062480030\">Jefferson Nyilas</a>"
                ],
                "photo_reference": "ATtYBwLA32AZ8FvbV7GG1HqtoWYnPU9oIhWUOkTLYYwM97CJWK_zZ_9GCoKyltnfIksNK4G6AN1HuRdDEAdSsPxwGGekIIWS1O7s1vZjFhox0PYIAVdWrfKlRTnxRiuTosdDl7clEB43NtseM2Zz6Ee4JWpwV1jscDa2w7B6ONbYa40H7lSM",
                "width": 4608
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107487783334312254168\">Giada Baldi</a>"
                ],
                "photo_reference": "ATtYBwJtVXd6pYg3cDt7RF2xkX-21N0qIOQZ5iL9zMPCtbBFKdnIZVeAmO6yVUaXFQdikaZU6AsNNFTuIisAVPD-queJPuVWPbqiPM_vx8TsY46Q1Dk_BzWqsSzqJ8MWZYNh06iKruPjKJfwT_uX1jYyGHiHMQl0ScbHtEyrH0Yql_phs4-r",
                "width": 4032
            },
            {
                "height": 2484,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108919448933946114771\">Carlos Aviles</a>"
                ],
                "photo_reference": "ATtYBwIhXzdQaxFlYZ69ErjaHaHmqFNlbPc0ADcz5yDMl9aEk7774-q7gJ9Dpi81Sa76YoPsOjNZA-0VYNuMtvFLrMGtC1ImKQCknXm5Oxe54B89XHUz5nuPPBrpfkoaVc8Wmc7BOmZUP3NhCxm39_k-z5CqStr0N8S-jsBnq8m2XlNDat1R",
                "width": 2739
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/109850608939875361213\">jamil blackmon</a>"
                ],
                "photo_reference": "ATtYBwKibkVNCtHgvkRzgzexRtVd3QTZb5P7zcAG1dr-8DeBzYn9ktwGbKfl6aqeTWcBsDFow1e-dPoxL85leI2s9Glj9bFrd173TNdV4yBBIiMQmPXaVjKvRDwZtlk8jGlpoAsIsd5WqL8urXVuHHsHxjSsOwqBMgACB1_4B5cnc4ZC-fvp",
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
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=opening_hours&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
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
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=name,adr_address&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "adr_address": "<span class=\"street-address\">365 5th Ave</span>, <span class=\"locality\">New York</span>, <span class=\"region\">NY</span> <span class=\"postal-code\">10016</span>, <span class=\"country-name\">USA</span>",
        "name": "CUNY Graduate Center"
    },
    "status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=name,photo&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
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
                "photo_reference": "ATtYBwIe-36dt5kVWcx8J086-UZTwU634DXn5bz1PBWr3vzh8wcz4wtTFwzcAkMHG9E5eRm0O55wD0T9yhgQibuK3eiVa0E3dMOwclFh1RPAyoEP-WyDxEOb1Oyi6VjSlb6M93DZPVuN7AM-fZmGMpsl2yhs7OscxhJ64nHRFlkmir0s-WHF",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwIltEO2pjwT9RGmNQBTkdZful-n69Y2_7QaGFo6I7StmVMXVwOzuhGhilMs68v4GQ0BfwOShaTHgNCdzhwUf_ccAyvrN3UZfe_oETLnz7Jn6hVa2ztJZJgtHR6yjbLWSAaNzp_30o7oJ2QpGYUpFlZmamtQdRKOL7CaOIra6D1tupqE",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwISVkmChGU2jRLIvFcVWFyoQEbZtpA9mmbI2ibLbOAtqvZr1-H_DR-yJgPBfffGMC0gs8rSHtQ5u6uiosxghBb7QID43XTQ6kyly6aMZ4g3x2llk7tsnQAReeKaqlgU9TWub45GERiOn-iP2OlAX9Dh9jnTGPqdmFUUpUyUDr5BgfaC",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwIvfdAbiQ0E5irFwavFLnZdbLO7DzOKEf3s9FBXSFplYJ-r75WR9xNdy9gsjsanNiOje-v_-Na6NAiyb_nCKfeO_-rCNF2OlaMcpyLoJUh6cUUtAZ8BSbF95A5GMYd2MMs6mSeOWOKuOQQJXcWBjkjiN8p_9CG9dbnJpYtLotdUA_3d",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwLkZHwf_O8JS8HENRgRKmKCoY5mwarScT8etwaxN8-4v3fdF5j39bPgS-DSx0AH9ceR5P26CJ-d5lPy07Oa5pY8WHWXkwWWnldMIUCNxtKQNupEcLoFSeTQDPTFvM5toLOOry4OhJNVDQ4ZATVu2wJN182QLW2GjZXt30gEGqnGPDMZ",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwLvy_hL_v8q5N-KBQuyAb_Jgm4p1DBwd2_CC7yPgFI2LQfl2GpRzZsE1XUrfZCBAbDLg_PJOHF_dPjjoCQq4cOQG7yznL0YF0R_9Dumci3BiZFX_WGtiH9CVLfrf0-GSDbX72UFGli7c_RkfFBZgKiVo_Ft8tayz685J8MEhEI50hwW",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwJD1sueRO7Q9VNZDKllz7IM5GwwqOkQ0xgt6zoM8ZEZ-SfWgnxSdCFXwRhpMt1w1eJAnCEZjLUBIUCyZcXgx0o8lFb5w4I9TI-8v7W566jse3t_Z7N5Q5n8cfpAYSG99w-KlJYIAKcmIizxJ8dvGYuYXRlsjOoFKKlZWJxXC_9D916v",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwJy3x7Vp-nFYv1dTS1jmwDs5vcjClgpgBRAv7wpkVFg5jOb_BD55J9MJ3n45tpaFILaMQxQ0pXNf8MEY78nLpK-aNTWUGbEuU7Wz0Bvu7LI0Gbf7SyWqL2g74idH7fAN9R0kuE2-7zudJZxjY3sEQNKs1Hd-B5CPJmVrUIuxaZWORQU",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwLMt5nw2wY9J3RTAPIYC94yDO57N1Vx3SI_ZQrtNGUoWjBQ032I9FJLkgWjDJyR4yI2WjgSXiYNNIjP0ZFiw5aGoP29m4MC9wJNfqV7nHZSAcEYVfqx88OIS39FTHHApiDvm8y5go1kJDKAQUI-J1a9DxhktA_2e9H2eMqzPyB9Vsg0",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwJdNeqajpRmWX0TNs9meenCmCitZalGOhvkKrAgChwydihvzwlJ3wZ0CDAP6pUJWOJWKIRw4MXONoNCD36d45JJgvz6_04EEYq_741uabXRUI1UVoCZ9OrWp_WqovWCl4PgqeyBzkZfCwML3eaN9POHemAg47t4EbhXqpDAAzonATqx",
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
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=40.7427996,-74.1770884&radius=1500&type=restaurant&keyword=name&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
{
    "html_attributions": [],
    "results": [
        {
            "business_status": "CLOSED_TEMPORARILY",
            "geometry": {
                "location": {
                    "lat": 40.7402077,
                    "lng": -74.1673266
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74130097989272,
                        "lng": -74.16625047010727
                    },
                    "southwest": {
                        "lat": 40.73860132010728,
                        "lng": -74.16895012989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "NICO Kitchen + Bar",
            "permanently_closed": true,
            "photos": [
                {
                    "height": 2640,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/116014581836866297644\">NICO Kitchen + Bar</a>"
                    ],
                    "photo_reference": "ATtYBwLxlzwfoYXUQS5KGbaE3bhhSDdjEvZTfSW5gZydg3VkaR40KXtkjbbANMB2D4qZpVwzIuchNqTxKZPaJHtKA7xtsjJnnZUkq_jpKuvjD1wODTPgVLTF3EMyz_KmqZDz0Fv91y1hiA9zY5YFcadL3WC43bm-JzmLqBCcWX_LNxgBmGia",
                    "width": 3960
                }
            ],
            "place_id": "ChIJDTNm9oBTwokRatnhvZXWRsU",
            "plus_code": {
                "compound_code": "PRRM+33 Newark, New Jersey",
                "global_code": "87G7PRRM+33"
            },
            "price_level": 2,
            "rating": 3.9,
            "reference": "ChIJDTNm9oBTwokRatnhvZXWRsU",
            "scope": "GOOGLE",
            "types": [
                "bar",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 256,
            "vicinity": "1 Center St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.741171,
                    "lng": -74.168412
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74262047989273,
                        "lng": -74.16709317010728
                    },
                    "southwest": {
                        "lat": 40.73992082010729,
                        "lng": -74.16979282989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Chinatown Diner",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1034,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/110961279328040426310\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwLGg2mxLP-blxMlpj3SpFQ2V1HB_dbX-RrAlVv13WGkmA7ZjGDf5s74pv6hDY7rde4UEgHNQwHC1RN6WelQ70-HsHymo3hxfTJbps3AwYIU0uECx79L2R7VVS6VXfwCsORggnzDNb4PQMqrWmTq_kWRF76oUvueMzTAU5qOZQz8HqTX",
                    "width": 1242
                }
            ],
            "place_id": "ChIJmz2OdoBTwokRh8rtEtDe504",
            "plus_code": {
                "compound_code": "PRRJ+FJ Newark, New Jersey",
                "global_code": "87G7PRRJ+FJ"
            },
            "rating": 4.5,
            "reference": "ChIJmz2OdoBTwokRh8rtEtDe504",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 94,
            "vicinity": "Inside The YMCA, 4504, 600 Broad St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7314977,
                    "lng": -74.1623718
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73280042989272,
                        "lng": -74.16110627010727
                    },
                    "southwest": {
                        "lat": 40.73010077010728,
                        "lng": -74.16380592989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "SAGRES BAR AND GRILL",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1784,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/115216186624398651140\">Sagres Bar &amp; Grill</a>"
                    ],
                    "photo_reference": "ATtYBwLt39wj_X9HO57q13JkYF67MXDxMnptsqSpWtPEvp5ESLgbHEzvimcxhq3xhirLJq7Aw3uQ7BMj1dsqFUogBrpF-voeZlSqJ9-afgW1Dvy8pNeosYkvbRGh4p3NtzAydjg4WW7etAyMU5XEEpLtX0ksmWjlIuiFbS2hK8kj_o5vBFNh",
                    "width": 3171
                }
            ],
            "place_id": "ChIJgQ9q2IRTwokRjOZQl4AQx-s",
            "plus_code": {
                "compound_code": "PRJQ+H3 Newark, New Jersey",
                "global_code": "87G7PRJQ+H3"
            },
            "price_level": 2,
            "rating": 4.1,
            "reference": "ChIJgQ9q2IRTwokRjOZQl4AQx-s",
            "scope": "GOOGLE",
            "types": [
                "night_club",
                "bar",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 348,
            "vicinity": "44 - 50 Prospect Street Corner of Ferry and, Prospect St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7315524,
                    "lng": -74.1616777
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73282822989272,
                        "lng": -74.16038562010728
                    },
                    "southwest": {
                        "lat": 40.73012857010728,
                        "lng": -74.16308527989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Iberia",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 2988,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/100782284768869688972\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwLzzvk6aAQKZ3hiazAajHUj-OG6yOeVQPdfhVIl9nr3NRE4u8zFDx5FLR_XKZXatF798Qb5N8n1kqnrKhqmTU5hDJirK-6SNbxCYhgDrHZbr-ytCJ6kHUBjqOK-hLJgnCKA5-IXQZqyrrhKx3RJXWXr-x1uT5tHPxb-WYHMUu_puig",
                    "width": 5312
                }
            ],
            "place_id": "ChIJMf5cL4VTwokRR7eVY2V37ew",
            "plus_code": {
                "compound_code": "PRJQ+J8 Newark, New Jersey",
                "global_code": "87G7PRJQ+J8"
            },
            "price_level": 2,
            "rating": 4.2,
            "reference": "ChIJMf5cL4VTwokRR7eVY2V37ew",
            "scope": "GOOGLE",
            "types": [
                "meal_delivery",
                "meal_takeaway",
                "bar",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 2437,
            "vicinity": "80-84 Ferry St, Newark"
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
