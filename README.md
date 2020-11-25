## Summary
You will be using Google Maps API. Please copy and paste any URLS you send requests to and response data you get back into the code blocks below each question. Once you are done with this exercise, please push your code and open a PR with the following name: `<YOUR_NAME>_exercise_2.2`.

## Instructions
You will be using the [Google Maps API](https://developers.google.com/maps/documentation). To get access to this API, you will need to register for the Cloud Console and obtain an API key. You can get instructions on this process [here](https://developers.google.com/maps/gmp-get-started).


**Places API**

- Can you get data about the Metropolitan Museum of Art?
```
# paste the request verb and URL here
```
GET https://maps.googleapis.com/maps/api/place/details/json?place_id=ChIJb8Jg9pZYwokR-qHGtvSkLzs&fields=place_id,name,adr_address,photo&key=AIzaSyBY_p65zSyoiIcnrd6e-LnPTfDUNGUUjxU
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
