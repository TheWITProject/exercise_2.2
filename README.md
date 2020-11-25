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
GET https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=40.7427996,-74.1770884&radius=500&type=restaurant&keyword=pizza&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
```
```
# paste the response data here
{
    "html_attributions": [],
    "results": [
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7384437,
                    "lng": -74.17079079999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73980892989272,
                        "lng": -74.16931777010727
                    },
                    "southwest": {
                        "lat": 40.73710927010728,
                        "lng": -74.17201742989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Blaze Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 3024,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/116185626778960576036\">Kevin Lahey</a>"
                    ],
                    "photo_reference": "ATtYBwKYTkKc4UvSSCv4v_wF7oKVi2z1Gqc-QTdljQilyykEHiIqZThz46o04k4ATug65nbLt75B0GgVOXoDxJcAZ7lnVhgvzW_2o6cRlEdpSj0E2QEVHXBn7n-7M0obg8rG3XnfZrdqZYfw-0_bOUGvJmVx1PHAIucKti1VWTriuLp9Idy9",
                    "width": 4032
                }
            ],
            "place_id": "ChIJkcWX4IFTwokRGzxAyZe8blY",
            "plus_code": {
                "compound_code": "PRQH+9M Newark, New Jersey",
                "global_code": "87G7PRQH+9M"
            },
            "price_level": 1,
            "rating": 4.5,
            "reference": "ChIJkcWX4IFTwokRGzxAyZe8blY",
            "scope": "GOOGLE",
            "types": [
                "meal_takeaway",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 1427,
            "vicinity": "691 Broad St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7382675,
                    "lng": -74.1720945
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73964252989272,
                        "lng": -74.17090037010728
                    },
                    "southwest": {
                        "lat": 40.73694287010728,
                        "lng": -74.17360002989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Queen Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 4032,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/111922827879507684907\">Marzieh Heidari</a>"
                    ],
                    "photo_reference": "ATtYBwJhGocB2uX7rK6Z_fiOzg3fmBqC3wzO6qYzS5dtqbAU3UuTP9Q9BjiabAIoqJuvaOx5Uk7i5eNsQO9fQmrrS-wV1nkbGoH2URLATOyRK6wjFbaeARdnV0csTQ3uEBEFrs67YYnVebHxhuxaCQ3qKrsbqiqqN_TT2vWRHHfkIGI1altR",
                    "width": 1960
                }
            ],
            "place_id": "ChIJx-Rkan9TwokRNPBn0KmirW4",
            "plus_code": {
                "compound_code": "PRQH+85 Newark, New Jersey",
                "global_code": "87G7PRQH+85"
            },
            "price_level": 1,
            "rating": 4.3,
            "reference": "ChIJx-Rkan9TwokRNPBn0KmirW4",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 140,
            "vicinity": "122 Halsey St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7443562,
                    "lng": -74.17806899999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74562792989272,
                        "lng": -74.17676152010728
                    },
                    "southwest": {
                        "lat": 40.74292827010728,
                        "lng": -74.17946117989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Giovanni Pizza Pasta & Grill",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1932,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/102882800576231090707\">Mohamed Ibrahim</a>"
                    ],
                    "photo_reference": "ATtYBwJjxcipA_iewttd-eSpP1UsungSREeGaUykOeF24HV9nUBMq7pUlfNYsEC0KUNLsOOkXtbtw-5mCiIHEDPhYYJATXT2sGJzwlaakxogtOc9Kg7z80FBxx59PuVn-oMKbLNCtk3DzsmlErAMx4vTfL2NVqOu7Yp-m3v94EIbzQUAw-xo",
                    "width": 1932
                }
            ],
            "place_id": "ChIJ-X73FYJUwokRmvL2xtP8sCk",
            "plus_code": {
                "compound_code": "PRVC+PQ Newark, New Jersey",
                "global_code": "87G7PRVC+PQ"
            },
            "price_level": 1,
            "rating": 3.7,
            "reference": "ChIJ-X73FYJUwokRmvL2xtP8sCk",
            "scope": "GOOGLE",
            "types": [
                "meal_takeaway",
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 386,
            "vicinity": "191 Central Ave, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7408096,
                    "lng": -74.17231169999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74209902989273,
                        "lng": -74.17099722010728
                    },
                    "southwest": {
                        "lat": 40.73939937010728,
                        "lng": -74.17369687989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Robert's Pizzeria",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1000,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/117539974832479103571\">Roberts Pizza</a>"
                    ],
                    "photo_reference": "ATtYBwLcM9PwsIeix5v1qYeoE8gL-YrjDPe7r3DU9KzTKGuKGbvrjW5-3P-1J_U-xtkxhspHnlqgJjKYZ5nZY0ZpfRxD4ztlJ9NFio3zBErhTCkXpiq89zGXWVZ1SG28A58gnBV_xmX8YT5q55fKUX9Smhnl0S6W-rjgcd7kDHlXjXCA_9ZD",
                    "width": 1500
                }
            ],
            "place_id": "ChIJMWP_lH9TwokRDiT12LmCAyk",
            "plus_code": {
                "compound_code": "PRRH+83 Newark, New Jersey",
                "global_code": "87G7PRRH+83"
            },
            "price_level": 1,
            "rating": 4.3,
            "reference": "ChIJMWP_lH9TwokRDiT12LmCAyk",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 217,
            "vicinity": "63 New St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7456497,
                    "lng": -74.1788871
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74705392989273,
                        "lng": -74.17770772010728
                    },
                    "southwest": {
                        "lat": 40.74435427010728,
                        "lng": -74.18040737989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Resa Grill",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 4032,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/104763865552199619296\">Resa Grill</a>"
                    ],
                    "photo_reference": "ATtYBwKEQWaB28Yb3LhafbMnf4Gb9sugTIYtNZlfQ5_ALpxpGTeBwFfb1CN0PiYAZ-tBzAM0mJOmGKWKkZK78ByBekl5JfIkalyAfsqrldGITd5HZi1N_ls1RNiSrItDYHwLh4nUT1oETpTuDP7p68amHwXWMMpLlXfTcp_-r1h2OY1pYGRg",
                    "width": 3024
                }
            ],
            "place_id": "ChIJKaVXTYJUwokREwt4GH2aAnU",
            "plus_code": {
                "compound_code": "PRWC+7C Newark, New Jersey",
                "global_code": "87G7PRWC+7C"
            },
            "rating": 4.9,
            "reference": "ChIJKaVXTYJUwokREwt4GH2aAnU",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "meal_takeaway",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 117,
            "vicinity": "12 Lock St #3602, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7371481,
                    "lng": -74.17271319999999
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73854307989271,
                        "lng": -74.17151047010728
                    },
                    "southwest": {
                        "lat": 40.73584342010727,
                        "lng": -74.17421012989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Mama's Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 1500,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/104733001379228625356\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwJNkQk1qKkwI6DyX8o7k2WIwnRfxzj5txr8wPYPHONjjPe3rgQDDQk-Sk0WD6jFLq1jatFCznbBMxw-_BllrgyLrEMy4xeLs2ixrluNvomfb5c8EiosSdisnDDx6aXa_eIfcFLq0zuwg88cVYwLisKtKlvC98ZG1nkbv2BMF1PDIrmF",
                    "width": 2000
                }
            ],
            "place_id": "ChIJ--bhzHhTwokRQox_tkeWPTU",
            "plus_code": {
                "compound_code": "PRPG+VW Newark, New Jersey",
                "global_code": "87G7PRPG+VW"
            },
            "price_level": 2,
            "rating": 3.9,
            "reference": "ChIJ--bhzHhTwokRQox_tkeWPTU",
            "scope": "GOOGLE",
            "types": [
                "meal_delivery",
                "meal_takeaway",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 52,
            "vicinity": "150 Halsey St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.73631719999999,
                    "lng": -74.1692091
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73771302989272,
                        "lng": -74.16782897010727
                    },
                    "southwest": {
                        "lat": 40.73501337010727,
                        "lng": -74.17052862989271
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Queen Pizza II",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 3024,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/117839698269898801808\">Daniel Rosado</a>"
                    ],
                    "photo_reference": "ATtYBwJcVO1ILe_ksLmbcKCmKeJu1b6rTKGdUUt4fTEj-LYj37zBqzC6emn23TQ07Lrm921l7wUvWhEnr0WJTyAOZDcbNh6cyUg0G5lU79JqZIl0VX9PMNaVjQXFyN9BcAbXdjR_h4T2oGg2qX_fyDJqT_VoBBPNFsRAmKipMcRhueFdLtOb",
                    "width": 4032
                }
            ],
            "place_id": "ChIJh8vaPIJTwokRDfh4x6CjZVw",
            "plus_code": {
                "compound_code": "PRPJ+G8 Newark, New Jersey",
                "global_code": "87G7PRPJ+G8"
            },
            "price_level": 1,
            "rating": 4.6,
            "reference": "ChIJh8vaPIJTwokRDfh4x6CjZVw",
            "scope": "GOOGLE",
            "types": [
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 178,
            "vicinity": "48 Commerce St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7400078,
                    "lng": -74.1699916
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.74131357989273,
                        "lng": -74.16850462010729
                    },
                    "southwest": {
                        "lat": 40.73861392010728,
                        "lng": -74.17120427989272
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Newark Pizza",
            "opening_hours": {
                "open_now": true
            },
            "place_id": "ChIJ0QS7NoBTwokR33Vz_Z_C8RE",
            "plus_code": {
                "compound_code": "PRRJ+22 Newark, New Jersey",
                "global_code": "87G7PRRJ+22"
            },
            "price_level": 3,
            "rating": 0,
            "reference": "ChIJ0QS7NoBTwokR33Vz_Z_C8RE",
            "scope": "GOOGLE",
            "types": [
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 0,
            "vicinity": "633 Broad St, Newark"
        },
        {
            "business_status": "OPERATIONAL",
            "geometry": {
                "location": {
                    "lat": 40.7363776,
                    "lng": -74.1707361
                },
                "viewport": {
                    "northeast": {
                        "lat": 40.73769312989271,
                        "lng": -74.16940622010728
                    },
                    "southwest": {
                        "lat": 40.73499347010727,
                        "lng": -74.17210587989273
                    }
                }
            },
            "icon": "https://maps.gstatic.com/mapfiles/place_api/icons/v1/png_71/restaurant-71.png",
            "name": "Two Brothers Pizza",
            "opening_hours": {
                "open_now": true
            },
            "photos": [
                {
                    "height": 3456,
                    "html_attributions": [
                        "<a href=\"https://maps.google.com/maps/contrib/113460236025716758993\">A Google User</a>"
                    ],
                    "photo_reference": "ATtYBwIigYBjdbztHEPWzwIaYtfWzrzC7Edy0pa0Tknr8JhNgenETVYwNmV_FGDmANrI2uJfohSJoS-Kx-2lnbnIfBrQEEO5vbaiSUnbXn4aRC8UV44VpKf5hMJuTPZTPNN8nj0FoIzJkuE2pnC8OL_D1pi5OpkODd1JDTZt52D3NycvGvQb",
                    "width": 5184
                }
            ],
            "place_id": "ChIJtSEud31UwokRetoVgeHU0jQ",
            "plus_code": {
                "compound_code": "PRPH+HP Newark, New Jersey",
                "global_code": "87G7PRPH+HP"
            },
            "price_level": 2,
            "rating": 4.3,
            "reference": "ChIJtSEud31UwokRetoVgeHU0jQ",
            "scope": "GOOGLE",
            "types": [
                "meal_takeaway",
                "meal_delivery",
                "restaurant",
                "food",
                "point_of_interest",
                "establishment"
            ],
            "user_ratings_total": 98,
            "vicinity": "16 Clinton St, Newark"
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
