## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=name,url,formatted_address,formatted_phone_number,website,type,photo&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
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
                "photo_reference": "ATtYBwKnVZUhJXaXQ2eqgT0Dv4MZkFwQiBnzJMmjIoDpk3oMyUrHMLtwpGYC7RLoduHEvefHxxRyh6tmjt36oGTXcEahSoO4WepZcMHg7FTO8xS9W7sg9MISngsfjYBOd-mgkNVZDI1V-syONrr-p6X2_OyfQ0CaT9LkUHfXaUDlo4XvTR4a",
                "width": 4032
            },
            {
                "height": 800,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/106748439247716180853\">Karl 1974</a>"
                ],
                "photo_reference": "ATtYBwJglI9HkQw53HGwxda5yzjo1N8rUKlzpQjtUQBjFx81OfaakooZEzIkhtyv4h52gbEYF6uHYSXfUwDqUUw8ikXTKGFXLZttiMfhQ2x9Zrc49Q7_gCuvg1hmpooXVOM_SuU1rDo4zIy3BI6PhwHjN9QG2wpQUqSEyz4Sy2URRdtjyGuu",
                "width": 800
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/105280404763450371863\">Sabrina Nazario</a>"
                ],
                "photo_reference": "ATtYBwKIwgzkztJWLNhb8E4RWUvGpXRjBgMGZOoyP4d2Vi818mlMSATMWC-RU3SYlrJX0PM_3OqQf-WeO6bWQr5Nn0IUUK2IrFlXtJeNBFlCkH402ZmlfLjsPoOUG39jbJHwhBluNW67a5Qm7qqnjs6uJz2sdKDirzTaQfeQUvBDBJAqkVZO",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114414941791922473064\">YehHsiang Chen</a>"
                ],
                "photo_reference": "ATtYBwK3t2il9z0_Fwk_8AORHcEIb-g8Ye1rZN8UTQC_B3EIbN3FnmKJlOR28DhgkkQTXG24OQ1k7Ed-uADytHDOTic4VbvihMQMX8cstSYkzWdJ6uYFSll2kBlIng2PDDDayGXSts8cfPi_eBuEQqFfJwPYAKQjEeb3nkDsk72lXLLuqaJQ",
                "width": 4032
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/114217576882578419305\">Eva Mikulcic</a>"
                ],
                "photo_reference": "ATtYBwJ2TT_N0saEfe5cWW-Abo1dFjnCRxgpiOCB-ug9dRymFA_wB0lwvDlI9STmsfZuMQHcCpDlFghUQg4iI3tLr5Il7giUu1XD_3nyckN5PjC8ti-NszjWM8ibjq50FsGOrPw06cc89qaYBM1zoNjTQQMZ932i3QAMdrvFEQxNxqJuRq38",
                "width": 4032
            },
            {
                "height": 5304,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/115568864800951782024\">Kenneth Hines, Jr.</a>"
                ],
                "photo_reference": "ATtYBwL_X2kjfFhLK8ZIqFs5Mg5TLIGBOsQyNG6G-incoewH0H-BjewOKwcWUUjivDwKfM2pLKR0qOSgbaqGbQEL2nznYOQqlie3hYZWTOZgMbdLED9Nwfzpbn_PXQ5nWsZWYow4TVNUYXxmGvzMGOsNO_EXreVS5Tar56qy5T4B1UlOoMIN",
                "width": 7952
            },
            {
                "height": 3456,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108035579848062480030\">Jefferson Nyilas</a>"
                ],
                "photo_reference": "ATtYBwI3ujZAYXcrxFsjhAtdmmqCmHyGVzRnKtNcAOwdqcN_ldWEuBZk1a_kqjPpQwiIJlU1UkDLwLv4g6biiPxYo5RYAakniU17ZJr0XoxWEsz0c6Xiwz91r7LrUgsQdhCpH_hFGU34PivFMFMTlaVmT1NTegLE3Ot_eMSiezfk579quqdy",
                "width": 4608
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/107487783334312254168\">Giada Baldi</a>"
                ],
                "photo_reference": "ATtYBwL-ShgWerFpGDe1pr91JQBrnmxm3VgAxHj0mM7EY_DhQT7u_oHrbi2TMBd_hPSPqRFJUFrgmXIXXHNBKV5DaRK3R8JQ-fQ5-2edfcKYtE-I2gYrEbJAJOjmXjBgdWqqSj94b_Y42mSNdQU9G8668VKvy0UR2dGBbUDodjdY1qe4NvSM",
                "width": 4032
            },
            {
                "height": 2484,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/108919448933946114771\">Carlos Aviles</a>"
                ],
                "photo_reference": "ATtYBwJuFS8CM2vzUSo7mQHwsQzqcwP5Om2_P-CbEb12lskrkbuitBP9c-QiEnqMXKFCQYBWFv3ffFZxVKQbd5ANlahW6kdFLoFXUwyYJ9M1MKX-Hn6MGCxoaSS8dO9CDNEEC7o_HZ44cnhQi91PUioUGJovvbcfvv8n1inibFyWtfbbYdws",
                "width": 2739
            },
            {
                "height": 3024,
                "html_attributions": [
                    "<a href=\"https://maps.google.com/maps/contrib/109850608939875361213\">jamil blackmon</a>"
                ],
                "photo_reference": "ATtYBwJWUqQD5Z3VkR-Z5VNdoyzNFe573gJX-kTLZv2MANGP6uUvd5xyuwfKTA2ZZw_YgTk2tTIPi1ptVCZNr1iY8UQhoE4BpqKdMBjYdHUTKu3J5dZwCYQXu3ojAZWWjqkG7pE6la5zJJ2PLwI9rRyPm8SwEBZqX6k8Fvnld8tq02jt_WtZ",
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
https://maps.googleapis.com/maps/api/place/findplacefromtext/json?input=Museum%20of%20Modern%20Art&inputtype=textquery&fields=opening_hours&key=AIzaSyDQUCJ6lAXU2Ec7POR9hQAOYaxAIbD_rHY
```
```
# paste the response data here
```
<br>

- Can you get just the address for the CUNY Graduate Center?
```
# paste the request verb and URL here
```
```
# paste the response data here
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
