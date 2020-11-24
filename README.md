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
# paste the response data 
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
```
```
# paste the response data here
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
