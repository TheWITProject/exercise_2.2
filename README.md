## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/place/details/json?key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
&place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,url,formatted_address,formatted_phone_number,website,type
```
```
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
https://maps.googleapis.com/maps/api/place/details/json?key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
&place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=opening_hours
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
https://maps.googleapis.com/maps/api/place/details/json?key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
&place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=formatted_address,place_id
```
```
{
"html_attributions": [],
"result": {
"formatted_address": "365 5th Ave, New York, NY 10016, USA",
"place_id": "ChIJRRI8walZwokRCPoUQ0TSCoQ"
},
"status": "OK"
}
```
<br>

- Can you get some photos of the CUNY Graduate Center?
```
https://maps.googleapis.com/maps/api/place/details/json?key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
&place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=photos
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
"photo_reference": "ATtYBwJJQXwULxnPp_XMu5zNUDJwVTP6jXpGhgw9GSwa28UqE7N_QRold-TpaE6UOqunMYA7X-Ub--pXAYUaBUfXQ_ZMVBB2Un-VRjGWzNvkbkvMZ1C87DjFBZAoF64vIVKS7q0VD4OtHvva5slKp0y6CN3p8pIkgBYA8JpNJ5aOJtZnLv3g",
"width": 4128
},
{
"height": 1280,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/102698931484204577483\">wellington fernando</a>"
],
"photo_reference": "ATtYBwJ4RDt5V4N2jEWO9Dq4y_eVomZXOkjkP_ae2SkJWK_4LOQNeNu42ZJmmi7l6Z2UH2Vfbm5YemTxMo0ByrO4g39GxDzHMz6o6sGglQIcifRCcDDdx3xp2_DV05QzVahVKpH7UR3NT9E9vc6LGk_Hwcm1XY37X8smnMBZFCDc195hFduo",
"width": 960
},
{
"height": 3072,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/106058925743212609964\">Kamar Ararat Kalpakciyan</a>"
],
"photo_reference": "ATtYBwL8rJ7L_KVD3n2cI1B9hZolND491I62dHmqFsg8ce5OwbwqiD8d24MaaJBl35otPbKn9oWE1ckLiDh-ZR5JFP5eBl47emEd171fYPd4IyzrJ8noWnfUWZxk_5o5FS9Um8e2msVj6QocU_OW9z7vj-rZJGJZJaw0ANE3ucXrA0RJFjt8",
"width": 4608
},
{
"height": 5312,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/107696651476482795651\">Bunny Ebanks</a>"
],
"photo_reference": "ATtYBwL-pcVYiH99Xjg9iy-rb3wgwBFvbulAYt5zFkbPgdwunQo49Baym1bn69_dWNNwL9z80OAVaaSIJwDYedxiUDIgALlb4i8Zub4Uv1qlzO5xnfe7M29h6lNNP2d77urVjG2QUB5PBR-4uvzI0W7RMofpa8e_bAG4ipBPOEbz2QKyIBiV",
"width": 2988
},
{
"height": 3024,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
],
"photo_reference": "ATtYBwIzkSii7MH24L9DHcbM7WP7tUt66UhONG3kPiJgiUemkSP1Wuk_Imwo9Ek0dobvkOfuCE7By3P4OvneAhWYcuachX2836xEiklUlDLAMsgddqAvUF6i84fmP7It1xFW3C2rNA94DjAsmnZgetVpa_CP2MOFdT0BgM7gc97IumF_5h2J",
"width": 4032
},
{
"height": 3024,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/111966493996460489847\">Yasemin Gurcan</a>"
],
"photo_reference": "ATtYBwL2ndHdZZU8s1Ih5fP9_ztnRdy9Luib6PIY373rjlJRpGuRXncAWgnPi7SWpto7a3tZn7yU0LGBghvMhjtvMYGmcbbm7zW1Amy4C0oh588cdSVsyoJaGOifNBCz9_L_IaUzyD8U7t-AMqqa619p56CD7gt1GHJwZ6IyjUPHT13SgSjj",
"width": 4032
},
{
"height": 714,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/108230965180565314385\">Qahtan AL-Jammali</a>"
],
"photo_reference": "ATtYBwKJgQ9TbYs1qXP-Pl8nsUdMbiinPROxrzlHmqcsSV13egK39-dc_NSZQ-uZ7k4HptvvW2AwadINu-A2hfu631LELfdyPnnaNBsorsGg5ik0exwcWYIytJQ2J3Xj5t3vvPQ5ZQ-QpC8luF9HjatsAqM2ovDQCOEEks1hFLn76CBuE4vh",
"width": 1071
},
{
"height": 809,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/116365843808688390145\">Arthurious</a>"
],
"photo_reference": "ATtYBwIHheREidcCTVDuM7KN7EKYqbPqhAk8SiKCAkw1GEXDByvQcEeRZy7S5eUl4ay8YTTaTHJxHNXGcL6NLZeR-jzPFoFRUbcdbqB6BgDOSNG7B1T0WEBQYBhO1xLLqn0aZR8lE_JtDVp30mUg-zkU-S3aEQ2yviyK02prbLKYXVZBvZjT",
"width": 1080
},
{
"height": 4032,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/108492738181551111937\">Cherishe Cumma</a>"
],
"photo_reference": "ATtYBwJpVXCjxAiATqT9WAOmhqkZJKMeDqxVzupxNaMklDuKgWu4IE5oo8qRMuifYy9zUQ1ZedNnee8O4wj0sz1Vg03cqiaYYJb9CcPmRBR0OgezJTTpiGUNBjUDYUGKOXwaGFKp_biLBvBG53w3umGZOK752BL3l8sfub7AKskqk5EXYk7M",
"width": 3024
},
{
"height": 2592,
"html_attributions": [
"<a href=\"https://maps.google.com/maps/contrib/110672763140227798702\">Glenn Ennekens</a>"
],
"photo_reference": "ATtYBwKEGzgC1wUFK1bYdmmRVgARZH6mI_I1-HItf5P0j6E_uVhT72aBco__HlkAfWHXaaWpWGFnlnbG6rCKC-pPnm-zCN31uPddkjdVpidq6UAAIWJSDvF8dgnHS4ZZEE9gAG9uY6tW5OunR1Ra7G18dWZeChkxZVFNQfAQYRPCGjJANXbg",
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
https://maps.googleapis.com/maps/api/place/nearbysearch/json?location=40.8200471,-73.9492724&radius=50&type=restaurant&keyword=pizza&key=AIzaSyAKUlglJSs2nN2EZyMDSoo6gEhnAZKUPsY

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
"photo_reference": "ATtYBwKV3oFbRsTCPx5O06IEHhjMC4KBThx3Dh6i5O0aBt1khOUvPBNhPB3zGrU9_fZAfT_KlTkZ-o1zm4gwVIg5YaXdzhlsTSZaUm6NSXsTd-77M1258nt8ZasHpx7FlxMyNpaozz2EEzmWgTIn3yxI09o-3ffL0dZfesJxW-cttkq_q1dh",
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
"photo_reference": "ATtYBwJVfzURyczM-fe2WotxWKOn16gGlAZscsMjsjAQ0l4dxhwqgPBp_1Z3vIibUJHnVI4lVD8kcsD1IWQ6FKRbRj29xouPKAA2KuYqTg9BR-5CO3PzBU3T0hJXjsYyOYSRsHA40fsUFB1g2nuAJw5GKztdnYuar6itm_oFgezBRJZWCPxU",
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
"user_ratings_total": 868,
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
"photo_reference": "ATtYBwIh730VM2RzUBOami9fwP7GK3ICxGPALtpYUTo_sZW-LVbvFRUkxGaDKW7kcI7fiDu746HB4kzFONputV0Lpz4MXusbSK-okoLFZOJqox5e7bOfIqhSFvQxD20aAQTAi7eFWUHg0ZnTqYl9MA-hqiv-R3777AmNTU9b7JsaJqp-Ox76",
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

- Can you get directions from Oakland, CA to Brooklyn, NY?
```
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destination=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY

{
"geocodedwaypoints": [
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
"points": "etveFtahiVDBAj@hAn@PHp@@`Ah@"
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
"points": "mkveFjghiVcAhDCLaAbDAFq@zBK^@pAo@xB}AhFw@rCc@zA"
},
"startlocation": {
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
"points": "azveFpliiVGGA@C@A?C?C?IAGAEAGAE?C?C?A?C?E?E@O@E?E@E?Q?SCWGUKMIc@QWMYOA??Ae@SaAg@GCaBw@]QAAm@[sBiA_B}@oAu@i@[[E[Wa@WA?UQECe@]e@@WSUUm@m@[[Y]e@i@OQQSIIIKCCKMo@u@EGWYACQSAAeAoAOQY]UWw@cAa@e@a@c@[Yc@_@k@a@IGKG]SOIIGECUKIEc@Q]MAAWGMEm@MAAEA]GkB[CAg@Ii@I"
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
"points": "kcyeFd{giVIMIIKCWEc@GoCm@y@Q{Bg@u@Ua@IiB]kASw@Qy@QW@}@Q@EMCUEEA]GEA[Ia@I@ESCg@Cg@Co@F]Dc@HMDKBEBC@UHA@OHC@A?A@MJA?A?MHSPGDMJEDCBIHCBGHA@KNS\ABGJQ@Oh@GVAHg@lD?BADEVM|@K|@MlA?@H@QlAABKv@WdBCP[dCk@jDCNObAe@|Cu@lFCT@~BIh@@dCsAzIKh@Gt@EXC\CZAVATC@?^AR?J?f@?@@Z@@@N@P@X@PBTBXDb@?DDZJl@L~@\\bCHj@F^TBj@jC"
},
"startlocation": {
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
"points": "`{eFfdkiVGXA@?BD^DnAApACv@Eb@Gn@Gh@EVGb@Ij@A@?BG\?@ABIf@WjAi@|BADABMd@CHCJCJK\ADELKZ?@Up@GTUf@MTMPMPEDMNGFYZSPKFIFWNUJWJA?WHYFSDE@YBA?W@K@I?S@E?OAYAA?WCC?c@Ca@CQB{@Cg@AY?u@@c@Bq@FE@o@JUDE@]Jo@R]LeCfAu@^a@Rw@^eCrAwGdDA@QXo@Rs@X@Lg@Nc@JKB@HSDWB[Dg@DuANwBTsBRM@}BVmBT_@De@D_JnAmCb@_AJ"
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
*code continues*


```
<br>

**Distance Matrix API**
- Can you get the distance from the CUNY Graduate Center to the Metropolitan Museum of Art?
```
https://maps.googleapis.com/maps/api/directions/json?origin=place_id:ChIJRRI8walZwokRCPoUQ0TSCoQ&destination=place_id:ChIJb8Jg9pZYwokR-qHGtvSkLzs&key=AIzaSyAKUlglJSs2nN2EZyMDSoo6gEhnAZKUPsY
```
```
{
"geocodedwaypoints": [
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
"points": "_wuwF|qbMDB^V\\VhCbBxBtA\\V|AdALFn@b@|@j@" }, "start_location": { "lat": 40.7488025, "lng": -73.9843068 }, "travel_mode": "DRIVING" }, { "distance": { "text": "0.1 mi", "value": 156 }, "duration": { "text": "1 min", "value": 50 }, "end_location": { "lat": 40.7452406, "lng": -73.9847924 }, "html_instructions": "Turn <b>left</b> onto <b>E 30th St</b>", "maneuver": "turn-left", "polyline": { "points": "_euwFnqbMJ[FYRm@~@sC^kA"
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
"html_instructions": "Turn <b>left</b> at the 1st cross street onto <b>Madison Ave</b><div style=\"font-size:0.9em\">Pass by Chase Bank (on the right in 2.4 mi)</div>",
"maneuver": "turn-left",
"polyline": {
"points": "w`uwF|cqbMQKiBmA{B{AyBuAiCcB]UeBiAOIi@]a@Y@Ui@]QM}@k@]Uk@]q@e@UQa@WcAq@Ao@{@k@s@e@gAs@@Ug@]]W]W[U]Wm@@@U@U]UA?]W[SWMi@[}@m@_Ak@_Am@aAq@w@k@}@o@@U]WAk@{@o@}@i@a@W@UcAq@w@m@@U_Ak@]ScAq@w@m@}ByAc@WGEg@Uk@a@@U?A{AaAYQo@e@{@o@[Sa@YgAq@}B}AeAs@u@c@OMkBoAC}AyByA}ByA}B{A}@m@}@m@}B{AGEiBkAIE}B{AIIs@c@}@m@}B{AIEmBoAQKiCcB}ByA_Am@_Ao@}@m@_Am@_C{AqBsAKI}AeAc@YKI@SwAaAGEIGuBwAC{AEI_BeASM"
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
"points": "as{wFljlbMKP}@pCa@pA@jA"
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
https://maps.googleapis.com/maps/api/distancematrix/json?origins=place_id:ChIJA-2qKIt9hYARZ5N1NdUVtHE&destinations=place_id:ChIJCSF8lBZEwokRhngABHRcdoI&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
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
