## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,formatted_address,formatted_phone_number,website,type,photo&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "formatted_address": "1000 5th Ave, New York, NY 10028, USA",
        "formatted_phone_number": "(212) 535-7710",
        "name": "The Metropolitan Museum of Art",
        "photos": [
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115967679611787063919\">Richard Stark</a>"
                ],
                "photo_reference": "ATtYBwJIqtSneOVpH2fNhiZ6GMDWRVZV3OzHVxsXxN9vw5FN44-2yLA2P6F2QB9gSQh4DzejTqTsJ_uy2_0iOrhW8JNhQ2tsc9xGcawWDGuo1N98nH5kzeCjy7xBNJqEYmLVJemHm66zTdvmSZRC5gtXWcFMZVt2JKVPlAxX6au3AP4L5AYC",
                "width": 4032
            },
            {
                "height": 800,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106748439247716180853\">Karl 1974</a>"
                ],
                "photo_reference": "ATtYBwLSej51_Z39UbpGJ4_y4owosP_q4dRa-YxNsCgUrP9Tb7H9HfyBxaNzezhHJeye93Pu6AiB5vtMjGZIZHXoJE0uVNDkWNP1sFgzEZmO9_ZXqJ7eT3OuqvMv4d0BlshfgPgkJsq0lfkmz7b8LxyzNsrDeQx5xdV57A0Kb_izYySWPGTf",
                "width": 800
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/105280404763450371863\">Sabrina Nazario</a>"
                ],
                "photo_reference": "ATtYBwJUaTXENAjArpHZShngpXKk5xlYxNG2s5K6z0fVWqk-5OGpl4hyTk6q2nh9Fo5MRDY3HL6C8NTzMOD891sPmSw0CMkDrgUEaM0PecQaleJba9z4Eyik3UsScoN28WvvhLHZh0ZEk-d5l4rtReinFNhenAGp12ARM_l1rEWs_qCtXM41",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114414941791922473064\">YehHsiang Chen</a>"
                ],
                "photo_reference": "ATtYBwKqN4xg-r1a4Wmu1tPFgTWbheIScvyBHgw1F_rwNzbp2JMMNU20p2Y18N1oAFylcZLHfu93E79QC08lQ0Yh25MLAqGxExOXZiA8V9hmpS8DeDadxEuAeQyc5xkOMqYvIKcqcrF1DtQQaHVz10D31Ao6pOiFbetSspQccQPodfaZFshH",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114217576882578419305\">Eva Mikulcic</a>"
                ],
                "photo_reference": "ATtYBwLhS6aN1IIhzW3JEGMaxwkPLeZjUtkdVAExwnjBd9SdZzf7T9LBU1JNamI9Gw13kYchJNyutb8KSWE4-uG4qTugSqmRj3kxbzhttrY9Z1F_uSYI27Nmjd7pI2ENPodnSHmGutufvmMTH3xhm0iZyrEFFGw6JuyEKK3atviZRUMoXZmB",
                "width": 4032
            },
            {
                "height": 5304,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115568864800951782024\">Kenneth Hines, Jr.</a>"
                ],
                "photo_reference": "ATtYBwJmpUvpaMIaLLx24vdZ0-oMQCLmDe5oZ538ylO62Jz-0DXc9EEcYJa-s9uqEZsm5qngek9IXj9u_3zUQM4s3XXKc4ceoWi1QMZtCTsL4hbZl6Ifyzb3TzgWQbIrqk6IEiTX9T7_9GzHdQGVVYVsrtLRFK_1Tel7PFzaxjEesmdvY6Gv",
                "width": 7952
            },
            {
                "height": 3456,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108035579848062480030\">Jefferson Nyilas</a>"
                ],
                "photo_reference": "ATtYBwL97KD1JUS6lAoMy_TZoCHDBc6Z_jLXYm3H5RoDp1NLv_X9WARKZgx0b-2xt5Px7TlyRVhm8c8Uvcg_gWehUWncwDPM3YlNyjx5UhieTekVChn2PEeBOsG0RUHj2hsc7dF-I4VlFZmg6wqqNl41KvGDbX96vqhDNfh2ti-crFRW15Wl",
                "width": 4608
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107487783334312254168\">Giada Baldi</a>"
                ],
                "photo_reference": "ATtYBwJoByhLKXX66G_pFKs2wR37QR2nLKhdrIgYU_T9jehYg6INHOsmp96RzbR87i5Qxzu7WGG37_qX0vC5FytogQjv3ifP3BARbzX6LTTo2j4TG0Sh6LZo-D-ThrmM2QZqUjFSIqBVmyFG8-rAIJF2dfJHPL8goKy4SiyDGOAzwidb7uRm",
                "width": 4032
            },
            {
                "height": 2484,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108919448933946114771\">Carlos Aviles</a>"
                ],
                "photo_reference": "ATtYBwI7JPmIpob4VOKWXosaWVakuTKDwtsyb6pJ6zN61wfKUt3PtD_6ogmPv45ldRNoop6WGRnE0pTdRIT330jyNr7oxDAHywSQNd90ExR6S33oI3gwyim8XNNC5TGoHJ39KJmubcsHSH4LBvAAlSGLw6_EqO5ItxkAEkdR7syfOkq0z_bz",
                "width": 2739
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/109850608939875361213\">jamil blackmon</a>"
                ],
                "photo_reference": "ATtYBwLksjX3pcgb6RVVXIK1Tzst6rFvVCW5V9QdFKMHK5TjvcxVi7Kkihu49FMl88i1tGIlwIAAWYP2fQUQ_7iM4hjYHnhk6kUS8EfJXCc6nsgMMS4LtUMOyPsT_Rkm9p0QVQjVcWMn5MAooT1ghh2NPKtbSLsUVf-pOkVMCfxAzWA6GstZ",
                "width": 4032
            }
        ],
        "types": [
            "art_gallery",
            "tourist_attraction",
            "museum",
            "point_of_interest",
            "establishment"
        ],
        "website": "https://www.metmuseum.org/"
    },
    "status": "OK"
}
```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,opening_hours&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
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
        }
    },
    "status": "OK"
}
```
<br>

- Can you get just the address for the CUNY Graduate Center?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=name,formatted_address&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "formatted_address": "365 5th Ave, New York, NY 10016, USA",
        "name": "CUNY Graduate Center"
    },
    "status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&mode&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0  
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
                "photo_reference": "ATtYBwKhtUWcSdLl3XHpOpiAWPOHpRQZWFqqWIYurm3NhFvn8Cu17NsKZk-2ygdeW0sZK-5109vzAqRrkklkCuQSLbTKMPVngq4qNFmvaObnCNS5KI_-_d8RkI0FC592Y1R_ZBRsc4L478MeHRKpeDdjXX--uXNK3xdMhGrHDbiNqjVXn4Q8",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwLM0VpRJuJdZQVgcCtQwMQZRNb_Z-8nGaDyJckDy2EFz72ErSLMxfqRT9kYbBujrj7mdDLvQwcZrHfRrya58eXlcQ5vYo37dDGV49nQJc-230Yr7kPSXn6gHQRZ43RVzjVjlPpgTy7MFiO4VK5jRj83V0vTlI_Amp_zPOfwfgsmPjOJ",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwLINKtcucI03J3nJfipag_ArvcLvm-WYBZ26PXTgNpuetPLTtxgO46tE5fKqExed-u5iahqof2X_GPl_XdlmCg1bIYrbj-O0PYxbLT-MGmOGGGmLdCW5afYh5C8z4QoFRvhxFt3j5KqQMww_mN828nvIJ_b8ZH89Ur5gx4R-rNkKe_1",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwLD_z9Yq_jyHDMcooNngEPTTpZ7fgnYUMLlYbN17GcxWvzpSwITmdf1jWk3omGO9H_Jc59w73ph27vVZS32qgDopdm2z-EvgfEp9Qjg4zG2BRFyn778qLPlf3DJjFRba80fbU72eULv65Y4rwhsEsYDijBefrAfX0_QfZlryHkgCySA",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwIWJE6c5w-6LRcVKX3-lUfOhkwO0TbKED-j1E1R_pr3yrnHtsUVucuSwtDSsRqVxJm9gSbpjsQ6rkO_efiWpvQVc7PZT-jXXg3d04JZN5Ss5U0sIrU3KfAY8UmMyKN4zdI80wQ-f6qZs7K3CcOssmDV6yy4MLnwwaXsd7FBt7rZ64d_",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwKfPKx0uRLNHyrmpa54KhWKw5M9g40DdlTuoSHuLKGgGqgIpSp7VOwemp0EifElO6RqaoYCjFSPeJJ8X9DxtEiRgHO4ekpRuNaIOZpLAwhcBukZaPpiYhJWHR9Wo54QF2Ra7xJDoazKKpKJ2ZvnVUanfW9BwksPO5tl2afVCrQ5IqI6",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwK49gxBPaYzozMuom2vpofUTqmq_zxIDsXVXaC0cxiG-MP66pfrsrV-B802-KOhKzrf1zv6jgTcD-92W6joDPVNnJA2S2v_ZxyVI5xb5MKqIDbYZxLX0sNVEDAHNn0hQJsVpIAMjhV9iXMGA9ObQg4k6cw34fBn7KWhZ2_kAF-f7DVk",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwI929W5HecstZAn8yfqYaTUgRU_SfFE20Kl9IOiVOZVpgJo1dWLYeMpNzl0moS6qB94LFJivo4u_dddxmklzuwMWBFhI8vZWQNfS3SF4gc9glf210e_fbXEOdrFbcB6E7YAn3C0svlRdy4at6vvsKtu7J8fJ-9J0kWGlntpzAzy5JMX",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwINIVkwCjG9Y5rWTNblzAhcIvuozxD5rZO6v3SL_5zwAHSGsWoqJJnKrU2ilMQDX8pzI6_cgUBoYzlgzPpPKeq8vpsgaE7WN67yopd5kJC83Z5c-G6cOJKeX0IZ691aVB9lmq9mD0ouJjVW_M6WkyChW6sX-lbrJrjKuQh36vestFDn",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwItmVX7Vyet755UJAnWRvSOJN3I46KgC1Ly96pznu3wWkHBFn243Bg5853Bfnugnvy0IY9AX91Z3G4EY0dbcn6CR60TxR2UM9DxxHabzfCp9U-V7_2JU7Clp9sLGxj4Tw9MsSzklEP9TExGV7dW3zt4DLnUTQiK8LYMOvlPK3TR9y1a",
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
```
```
# paste the response data here
```
<br>

**Directions API**
- Can you get directions from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
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
                        "value": 966
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
                                "value": 50
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
                                "value": 763
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
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destination=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&mode&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL here
GET https://maps.googleapis.com/maps/api/distancematrix/json?origins=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destinations=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
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
                        "text": "5.0 km",
                        "value": 5021
                    },
                    "duration": {
                        "text": "16 mins",
                        "value": 966
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
GET https://maps.googleapis.com/maps/api/distancematrix/json?origins=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destinations=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
```
```
# paste the response data here
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
                        "text": "4,693 km",
                        "value": 4692908
                    },
                    "duration": {
                        "text": "1 day 19 hours",
                        "value": 155137
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
