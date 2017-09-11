# ali-msg
阿里云通信 Node.js SDK

## Install

```bash
npm i ali-msg
```

## Usage

```javascript
TopClient = require( './topClient' ).TopClient;
var client = new TopClient({
     'appkey' : 'appkey' ,
     'appsecret' : 'secret' ,
     'REST_URL' : ' http://gw.api.taobao.com/router/rest '
});
 
client.execute( 'alibaba.aliqin.fc.sms.num.send' , {
     'extend' : '' ,
     'sms_type' : 'normal' ,
     'sms_free_sign_name' : '' ,
     'sms_param' : "" ,
     'rec_num' : '13000000000' ,
     'sms_template_code' : ""
}, function(error, response) {
     if (!error) console.log(response);
     else console.log(error);
});
```