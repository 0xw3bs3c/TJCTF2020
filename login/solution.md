# Login

Leads to a login page, viewing source gives us an md5.js and a little script:
```javascript
    var _0xb31c=['value','c2a094f7d35f2299b414b6a1b3bd595a','Sorry.\x20Wrong\x20username\x20or\x20password.','admin','tjctf{','getElementsByName','toString'];
    (function(_0xcd8e51,_0x31ce84){var _0x55c419=function(_0x56392e){while(--_0x56392e){_0xcd8e51['push'](_0xcd8e51['shift']());}};
    _0x55c419(++_0x31ce84);}(_0xb31c,0x1e7));var _0x4a84=function(_0xcd8e51,_0x31ce84){_0xcd8e51=_0xcd8e51-0x0;var _0x55c419=_0xb31c[_0xcd8e51];
    return _0x55c419;};
    checkUsername=function(){username=document[_0x4a84('0x1')]('username')[0x0]['value'];password=document[_0x4a84('0x1')]('password')[0x0][_0x4a84('0x3')];
    temp=md5(password)[_0x4a84('0x2')]();if(username==_0x4a84('0x6')&&temp==_0x4a84('0x4'))alert(_0x4a84('0x0')+password+'890898}');else alert(_0x4a84('0x5'));};
```

Nicifying with jsnice.org,
```javascript
    'use strict';
    /** @type {!Array} */
    var _0xb31c = ["value", "c2a094f7d35f2299b414b6a1b3bd595a", "Sorry. Wrong username or password.", "admin", "tjctf{", "getElementsByName", "toString"];
    .
    .
    .
    .
    checkUsername = function() {
    username = document[_0x4a84("0x1")]("username")[0]["value"];
    password = document[_0x4a84("0x1")]("password")[0][_0x4a84("0x3")];
    temp = md5(password)[_0x4a84("0x2")]();
    if (username == _0x4a84("0x6") && temp == _0x4a84("0x4")) {
        alert(_0x4a84("0x0") + password + "890898}");
    } else {
        alert(_0x4a84("0x5"));
    }
    };
```

* md5 hash stands out `c2a094f7d35f2299b414b6a1b3bd595a`
* cracking with crackstation, we get _inevitable_
* password is tfctf{} wrapped around_inevitable_ + _890898_
* login as _admin_ & _inevitable_
### Flag tjctf{inevitable890898}