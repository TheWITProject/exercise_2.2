## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,url,formatted_address,formatted_phone_number,website,type&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "formatted_address": "1000 5th Ave, New York, NY 10028, USA",
        "formatted_phone_number": "(212) 535-7710",
        "name": "The Metropolitan Museum of Art",
        "types": [
            "art_gallery",
            "tourist_attraction",
            "museum",
            "point_of_interest",
            "establishment"
        ],
        "url": "https://maps.google.com/?cid=4264808743088595450",
        "website": "https://www.metmuseum.org/"
    },
    "status": "OK"
}

```
<br>

- Can you get just the open hours for the Metropolitan Museum of Art?
```
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=opening_hours&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
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
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=formatted_address&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
```
```
# paste the response data here
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
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=photos&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY

```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "photos": [
            {
                "height": 3258,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102171454142994281799\">Sebastian Förste</a>"
                ],
                "photo_reference": "ATtYBwKprLEgL2JdZhi73w6uke03zi822CF82385vZ4N9IFgXr6tKxGCCKgATZeNJ0BhaRx8XOd86DIvcZtbUtT5GdS3C3AI7ypF5HO8XubzTd1pxOGbDmOodOYg5pKbzGoXQmDopt2VbsDieECuKlCq8GyBX0DpMZsKwCqe7u_o_ByKqSHC",
                "width": 4128
            },
            {
                "height": 1280,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
                ],
                "photo_reference": "ATtYBwInP9YlG90Dfa8hqxTxK_7tCPdI5pw2QIxLakhyfALVay3eioDUUxlZCF8jLR2CaOYfdTcq7cubUJnLKPK75RRYWOs97UfJ6m-MaaExuYZ7G7iAOsdmkcTq0ewEEWwgUwravnqlPDrcmLUw1T5iVTSCeGTnhd948t2-0HXeDFLgMJ3A",
                "width": 960
            },
            {
                "height": 3072,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
                ],
                "photo_reference": "ATtYBwJNX8-SGhdUdkf-1hop7CdgrAAuTQTOt1fS37H9Kr9e9n4DJrsP09O-iBvORCjn0WVrDh298uNiWYohfmBISJzkCLW61_MG15WRPecDLppotXsd9lTppV1iOauqcJXT9g6z7St00i4Ve59AjxDB4wWz-BqO3OoUdYVuhe3zzOgcCvpj",
                "width": 4608
            },
            {
                "height": 5312,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
                ],
                "photo_reference": "ATtYBwLe9Mirrjh2hMiA2SwZVUvEU76TRh-7aa73eexBEQRbY4q4G_Wj8syEfYxysQrgwQVtxmZQVfEPVP0A1qTtkLpg62toLTN0pRhBGNdaO5-251zeu5dT4PvFDq1DVpcJw7j8jdLDkzu8lgjoJNbESiP4Y3aZOQSul9qhEKfR2g5Ct6k9",
                "width": 2988
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwKrhLjPbBb60HXss-kALRDGJnK1AmmIEEWxxlYU1maiN7SpYkYm0K6Cneb23x9vsD5_hmXIXOPcoKwKURVXT42CktiKwSQKthWrAia4FcUcMW1n83rvD9xgovWPFHKvfMXA6C8LhKLw4FxSWdHByfYGTMn33ZtNmaCjM_-JtxK1uARS",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
                ],
                "photo_reference": "ATtYBwKrLoQe99YJxGvjxOzCqlsFhLV1CmI09R6tocSkYcJsQS7MehXwRsTdhQP0NJolhG9WzsHGsusiBA8Bp9FWPQbQxePbLzs53bsmDQQ0D2zNyJFsjXf3QA0p8uWk8sE5nN56Z37omKxPvEeTZ8LA8QWdZ6FXL-d9xOTNWVUDl9QQnQRW",
                "width": 4032
            },
            {
                "height": 714,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
                ],
                "photo_reference": "ATtYBwLDZtuHeHWi1_5q4EVUogTQzOdMxab4JW5b-vqMINbZP1seBzG8yEqaf1BNLAh5sFCp8Sg-JpvsVlnkfF4cJm0Bf68uuYgfbUvPSDoBgaZ0jf-K2Puo65TW3SQVlQ8JnWfWleYbnrt6_imtpR4_d3pWX7m_WuaBA7yYU4KtOn2jK1_6",
                "width": 1071
            },
            {
                "height": 809,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
                ],
                "photo_reference": "ATtYBwJN8zClyFsrLagiqLzvZWF0iwvE1VhuOvxYFPiESs1lRj1JUK5XRj5iBJPy_bBQSlnBMW0Y9B4Y6GowSkb9igu4qpflTeysJAQZxmXJgutIGDHuJgXcGpOHbBh4eqDiwgh558UJXQoOskj2Z8yoLEjR5SIwSuQYNYNvmKrsRdOE_Jvj",
                "width": 1080
            },
            {
                "height": 4032,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
                ],
                "photo_reference": "ATtYBwIl5VgRk8SfI5uUG7lCRIb2HdsEE1PFIuFUxUNxdpOE17U17NgcApzuXj9buoPS_I-igUt8OGbZ3qQmpotrOGjQa5qdQwpw4q9fPe6EItj5W5LJL55cyMXJkaeNI87v9iPiW1QlrnhCV3m6zhYCqzUHiRn9vhXzrbEyfuJ2sQb7QtHr",
                "width": 3024
            },
            {
                "height": 2592,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
                ],
                "photo_reference": "ATtYBwLE13__Pd3HL3rBaLqBRXQKrsnuAUbKCbsNRz0LelPHOHdnXgfePKAlCv2KGS1rg7KxVGpSjMKjexOzlaXCsdI4W-9kLPrK0B6l_pz1BN8kWbhuFgmo40DQNk-PRR4mB66F3-DiOgChu0Tn8BnkEIh4NqkMETbsEIMgSnFDs4smKORb",
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
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJ1y7mQm_2wokRPqoqstcPkq0&place_id=ChIJBQyPp2X2wokR-aiSMzFop-c&place_id=ChIJLe70p2X2wokReDA-X8LGqZE&place_id=ChIJe4_bTnr2wokRWPwq8n5DKdk&place_id=ChIJiyAjh3v2wokRK5YBozpXT38&fields=name,formatted_address&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
```
```
# paste the response data here
{
    "html_attributions": [],
    "result": {
        "formatted_address": "1522 Amsterdam Ave, New York, NY 10031, USA",
        "name": "Pepo’s Pizza"
    },
    "status": "OK"
}
```
<br>

**Directions API**
- Can you get directions from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL 
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY 
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
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destination=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
```
```
# paste the response data here
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
                            "polyline": {... (really long code)
```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/distancematrix/json?origins=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destinations=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY 
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
https://maps.googleapis.com/maps/api/distancematrix/json?origins=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destinations=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY 
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
