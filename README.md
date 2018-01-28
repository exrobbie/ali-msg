# ali-msg
阿里云通信 Node.js SDK

## Install

```bash
npm i -S ali-msg
```

## Usage

1. 创建 client 实例
```javascript
const TopClient = require( 'ali-msg' );
const client = new TopClient({
     'appkey' : 'appkey' ,
     'appsecret' : 'secret'
});
```
 
2. 选项

- 短信发送
```
client.send({
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

- 发送记录查询
``` 
client.query({
     'biz_id' , '1234^1234' ,
     'rec_num' , '13000000000' ,
     'query_date' , '20151215' ,
     'current_page' , '1' ,
     'page_size' , '10'
}, function(error, response) {
     if (!error) console.log(response);
     else console.log(error);
})
```

- 文本转语音
```
client.call({
     'extend' , '' ,
     'tts_param' , '' ,
     'called_num' , '13700000000' ,
     'called_show_num' , '40012341234' ,
     'tts_code' , 'TTS_1234123'
}, function(error, response) {
     if (!error) console.log(response);
     else console.log(error);
})
```

## TODO

1. callback改为promise实现