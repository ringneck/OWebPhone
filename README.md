# makecall.io  WebPhone 서비스 
How to config /phone/scripts/config.js

//  주식회사 얼쑤팩토리의 makecall.io 신청 후 발급받은 정보를 입력합니다. 

```html
var user = {
    //  SIP 사용자ID
    "User" : "sipuser",
    //  SIP 비밀번호
    "Pass" : "yourpassword",
    //  SIP Auth Realm 
    "Realm"   : "realm.olssoo.com",
    // 발신자 표시이름
    "Display" : "olssoo",
    // WebSocket 서버 URL
    "WSServer"  : "wss://wss.olssoo.com:8443"
};
```

# ctxSip

[Project Homepage / Demo](https://collecttix.github.io/ctxSip/)

A Javascript SIP client based on [SIP.js](http://sipjs.com/).

ctxSip is a Javascript based SIP client that uses WebRTC and WebSockets to connect to your SIP server.  The UI is designed to be launched as a popup from within your application.  Works well with [Kazoo](https://github.com/2600hz/kazoo) from [2600hz](http://2600hz.com)

## Features

- Audio only, Hold / Resume, Mute, multiple call support.
- No plugins required, Works with WebSocket / WebRTC enabled browsers. (Firefox & Chrome.)
- Call log is saved to localStorage.
- Intuitive interface makes it easy for users.
- Easy to configure and integrate into your project.
- MIT licensed.

## Screenshots

<img src="img/screenshots/1.png" width="160" height="240">
<img src="img/screenshots/2.png" width="160" height="240">
<img src="img/screenshots/3.png" width="160" height="240">

## Getting Started

You will need a sip account on a server that supports SIP over websockets.  This has been tested with
Kamailio in front of Freeswitch.

- Clone this project.
- Copy `phone/scripts/config-sample.js` to `phone/scripts/config.js`
- Edit `phone/scripts/config.js` to reflect your sip account.
- In your application HMTL, create a document and add the following code:

```html
<a href="phone" id="launchPhone">Launch</a>

<script>
var url      = '/phone',
    features = 'menubar=no,location=no,resizable=no,scrollbars=no,status=no,addressbar=no,width=320,height=480';

    $('#launchPhone').on('click', function(event) {
        event.preventDefault();
        // This is set when the phone is open and removed on close
        if (!localStorage.getItem('ctxPhone')) {
            window.open(url, 'ctxPhone', features);
            return false;
        } else {
            window.alert('Phone already open.');
        }
    });
</script>
```

SSL connections for are required for this to work!


## Dependencies

ctxSip uses:

- [SIP.js](http://sipjs.com/)
- [Bootstrap](http://getbootstrap.com/)
- [FontAwesome](http://fortawesome.github.io/Font-Awesome/)
- [jQuery](http://jquery.com/)
- [Moment.js](http://momentjs.com/)

Tested on:

- [Kazoo](http://2600hz.com)
- [OLSSOO](http://www.olssoo.com)


## For Korean Users

Translate some menus and titles


