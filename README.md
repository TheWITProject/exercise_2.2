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
```
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
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=name,geometry/location,place_id,photos&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
```
```
{
    "html_attributions": [],
    "result": {
        "geometry": {
            "location": {
                "lat": 40.7486485,
                "lng": -73.98400699999999
            }
        },
        "name": "CUNY Graduate Center",
        "photos": [
            {
                "height": 3258,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102171454142994281799\">Sebastian Förste</a>"
                ],
                "photo_reference": "ATtYBwKFtmXRCXlMIQy_A0DlcEP0EvY9nAHNjfh-H38DdcTCDWNfwqtN1iWmu5NkwzIunXwlFA36q8xnXcFTsHw67QfBSCqAEZtBU2b7_fhkok5uxUnnhj_Kx49juii_xxSDSgb5085W7HlnL4v4swLx9RbMYW8c6WgCcPbFFgd28abL88lu",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwKBMMqGSdfaja_U1OKLYxUCIW04Mt6ZaHM3QZZdyqF4IJxU8wed5ZuZWy4tz3xUbpGLbWeB7Mm3Oi4qU-gzc8Di-wZUDCCBO0L4BUuuS1LSi3preePdb7H4--9zdyTpHoIwcDh59WpH41nbdIcV7XgW5ppjFlOF-Bouoc3DzpizkOLh",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwLQWsG-TBPlgeGUmSQRwE0SIJnJhK4b5Vv74aeRRm4942CVEjAZJ4b5hyoi0hhHo9KIz2ImzasbgOttMheHP6mbjFf4Uq2iuBJJ-UitVdp3PzU1ysJeDR-C300U1I3p3uUa7xX0tIxiHbByeE59tdY9eExf1fOtPVvIUOJzskP1NYMB",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwJiCmTi9JY_GRgCLnmzkk0h82Nw-abkC_HW075mj87TlIZ-Q58i7OvETO-WbtTK_x3ngkOGDfm1uh3J_FE72HHU6DDfFcfkagUxNYJvkWPW3_WxzhbTxQBJLYTm-662RIkYyrvkFuDxcUM31w6gb2yVcVULTbQtrxw_5qFJY9fCzZXb",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwIbzbVBdj5TVZZIZO4HO78XNK7yLujH1Gn1pUKsYlXCQU2bWt05DTVQM2EtNkHXSkTsYt_uf5wKT1qt0T77ZqJ_T5B3j6xV1iWXZpZtTbRKU9RGSoGAvXiszPt0ivRj54Am6Wi3Sg_hg1N9BobTh-pI3JCu0ijdOfuMWeyGzJQqyfNG",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwJw5fSc4jSr1AtxR8Ly6tGxB9ye9mp4HUxxqa5UdFhhY7tLbEV2MR8IlqCddfU7-6I67MOktxScQjiZVmKAuBcWrRajV2Ojs2Nia6Bk6E1LGhaVwQCxkLPdQ4IX60Gz_RrIpGcblNwpHbpA5XH4J3wefXCoFKKThKoRHsPNINRpkIXf",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwLjjbOEdw5n8XqJDerKhKlt175z_EuKb9bY4O4rpH6PwtKO5jO_KoaL7UAVv825_7447odC1YISYZGHMEgI0PvrHGXBYJdZnWlpFB-N58d4WiGTO5IbzM0ZbERpk6gIXCwIJ_fRxTWM-fHKTcn7XeW0tOguQlwkAPmKY8dVF0K_PX_R",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwLgD4vlSd0FTVJaorjPHCgUumjhkUwD7VnYZRoJUIp8RNtBbZRPRpDwumPl2h_J7dGg2ElmZhrMeoU9cZm6tHBA2e-8UQSHml7rDDvNatEwE_j1uVVm1E0zbjaUszbhiIP1qnB7dxLlgjtkLyocSHjbe8SN8KzEgdJ3WfP7sjDSvyXH",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwIouARdZl5vyKezuIMvsv5ZjtOyHO9G0Bctib6QLD3zj2XreKgulm_wZqllFw98XPoqD_QOlGvvFE6_pjEWZKnzqvbqy36fgQQiWEH1qNP_CVTGQoBhHrr5-WW2RrUfdf_MquKSQJTJrVdkB0_lpuvXdpq4qQICWgL_ql11Ai-PAg6H",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwKqIoQ3w0FvWYhWp3NZKinqcvkYlDnSTlCg49sp09gArEBrEcz4aqAkMcxeVKOLG0i4A5c6oR-ISbnXW6LAoKYoAx_m2Ne6ppSjtpYK9wPsK5qUXz7ZQK4CBmyDW5Hz2QuZSnLwi7WqjMxWHMm0SBeahNTXLf0uFh0I_od6ErRCWWkE",
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
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
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
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destination=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
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
                    "lat": 41.7892787,
                    "lng": -73.94416129999999
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
                        "text": "2,901 mi",
                        "value": 4669127
                    },
                    "duration": {
                        "text": "1 day 19 hours",
                        "value": 154039
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
                                "text": "60.0 mi",
                                "value": 96575
                            },
                            "duration": {
                                "text": "54 mins",
                                "value": 3224
                            },
                            "end_location": {
                                "lat": 38.5144105,
                                "lng": -121.7757764
                            },
                            "html_instructions": "Keep <b>left</b> to continue on <b>I-80 E</b><div style=\"font-size:0.9em\">Toll road</div>",
                            "maneuver": "keep-left",
                            "polyline": {
                                "points": "in~eFzgmiVsBVmIjAkBXA?]Fa@FoDh@cBVSBA?_IjAcEl@qB\\g@F]HkGhAyGlAgKlBeAPsh@pJw@PODyI`By@PUDKBOBcARkGnAmFhAkCj@wA\\_L|BiJnBw@NcB`@aB^}Bf@{Bd@wBd@mARC@sAToHbAqAPo@HsDb@yDh@w@Ji@LUDa@FuEl@iBVcAL}BTqAJG@c@BQ@gA?}@AYA_@CEA_@C[CA?{@OwA[sAa@a@OuGkCo@Su@Ug@Me@Ik@G[Ek@C{@A_@?u@Bs@Dc@DUDUBMBMDyA^gBj@iA\\{Ab@sA`@wAb@mA\\_Bf@{Bp@w@T{@Xk@Pi@Po@TQHa@Nm@Vs@Zo@Zk@Zg@VC@[N?@g@XA?aAn@QJiAp@s@b@MHoBjAo@`@gDtBaAl@k@XoAv@w@d@_@TaDnBoBlAID_@VoBjAu@`@_Al@_B~@qBjAk@^m@\\
```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ
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

- Can you get the travel time from Oakland, CA to Brooklyn, NY?
```
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destination=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyCPT7YPRbTq5sEJo2zEu1pfmT3A1qWZhPQ

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
                        "text": "4,669 km",
                        "value": 4669124
                    },
                    "duration": {
                        "text": "1 day 19 hours",
                        "value": 154041
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
