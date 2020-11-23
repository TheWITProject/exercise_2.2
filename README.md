## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,formatted_address,formatted_phone_number,website,type,photo&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
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
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJRRI8walZwokRCPoUQ0TSCoQ&fields=name,formatted_address&key=AIzaSyDYT-3TgER3wxAOkrQYRpQORWATz9c5Li0 
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
```
```
# paste the response data here
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
