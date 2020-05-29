# Solution

* Go to the VIP area, typical 'access denied', gotta break something
* Check cookies, `data` cookie is suspicious, looking like base64.
* On decoding gives
```javascript
{"1":false,"2":false,"3":false,"4":false,"5":false,"6":false,"7":false,"8":false,"9":false,"10":false}
```
* Converting all to true, encoding to base64 and setting cookie, reloading the page gives us the flag

```
tjctf{wkDd2Pi4rxiRaM5lOcLo979rru8MFqVHKdTqPBm4k3iQd8n0sWbBkOfuq9vDTGN9suZgYlH3jq6QTp3tG3EYapzsTHL7ycqRTP5Qf6rQSB33DcQaaqwQhpbuqPBm4k3iQd8n0sWbBkOf}
```
