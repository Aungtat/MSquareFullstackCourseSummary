## MSquare Programing Fullstack Course
### Episode-*17* Summary

ဒီနေ့သင်တန်းမှာတော့ <br>
### Node js
### file system module ( fs )
### web server 
အကြောင်း လေ့လာသွားပါမယ်။
##

### NodeJS
#### Node js ဆိုတာ backend (server) မှာ JavaScript ကို အသုံးပြုနိုင်အောင် ပြုလုပ်ပေးတဲ့ အရာ တစ်ခု ဖြစ်ပါတယ်။
ပုံမှန် ဆိုရင် javascript ကို browserပေါ်မှာသာ runနိုင်ပြီး 
backend ( server ) ပိုင်းမှာ ကျေတာ့ အခြား programing language တစ်ခုကို အသုံးပြုရပါတယ်။ node js ကို အသုံးပြုခြင်းအားဖြင့် JavaScript နဲ့ပဲ server မှာ ထိန်းချုပ်နိုင်ပြီး ဖြစ်ပါတယ်။

##
### fs ( file system )
### fs ဆိုတာ node js မှာပါတဲ့ module( object/function) တွေထဲက တစ်ခု ဖြစ်ပါတယ်။ 
fs ကို အသုံးပြုပြီး  file အသစ်လုပ်/ဖတ်/ရေး/ပြင်/ဖျက် စတာတွေအပြင် folder တွေကို လဲ စီမံထိန်းချုပ်လို့ ရပါတယ်။

###  အရင်ဆုံး မိမိ computer ထဲ nodeJS ကို install လုပ်ထားပါ။
 မိမိစက်ထဲ NodeJS ရှိ မရှိ သိလိုပါက `node -v` command ကို terminal ထဲ ထည့်ပေးကြည့်ပါ။
### `v18....` လို့ ပြပေးပါက node တပ်ဆင်ထားပြီး ဖြစ်ပါသည်။
 ![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/node1.jpg?raw=true)
 ##
### fs ကို အသုံးပြုပြီး ဖိုင်တစ်ခု ဖတ်ကြည့်ရအောင်
#### အရင်ဆုံး index.html ဖိုင်တစ်ခု ဆောက်ပါ။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver1.jpg?raw=true)
#### server.js  ဖိုင် တစ်ခုဆောက်ပြီး အောက်ပါကုဒ်တွေ ရေးထည့်ပေးပါ
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodefs.jpg?raw=true)
> ရှင်းလင်းချက်
### `const fs = require(“fs”);`

```
file system module ကို require function သုံးပြီး node ကနေ လှမ်းယူလိုက်ပြီး 
fs ဆိုတဲ့ variable ထဲ သိမ်းလိုက်တာပါ။
```
---
     fs.readFile("index.html", (error, data) => {
       console.log(data);
    });
    
    fs module ထဲက readfile method ကို သုံးပြီး index.html ဖိုင်ကို ဖတ်ခိုင်းလိုက်တာပါ။
    --
    readFile method ကို fs.readFile("file-name", callback-function) လို့ ရေးပေးရပါတယ်
    --
    callback-function မှာ (error , data ) parameter နှစ်ခု လက်ခံပါတယ်။
    --
    error parameter က fs ကို ဖတ်ခိုင်းလိုက်တဲ့ ဖိုင် မရှိရင်/တစ်ခုခုမှားနေရင် error အဖြစ်သိမ်းထားတယ်
    --
    data parameter က fs ကို ဖတ်ခိုင်းလိုက်တဲ့ ဖိုင် ထဲက အချက်အလက်တွေကို သိမ်းထားတယ်
    ----
    ကုဒ်တစ်လုံးကို အကျဥ်းချုပ်ရှင်းပြရရင် fs.readFile methodက ရလာတဲ့dataကို logထုတ်ကြည့်တာပါပဲ။
##
#### terminal ကို ဆက်ကြည့်လိုက်တဲ့အခါ

    Node မှာ run ဖို့  node  file-name.file-type  လို့ terminal မှာ ရေးပေးရပါမယ်။ 
    ပုံထဲမှာတော့
    ခုနက ကျနော်တို့ ရေးထားတဲ့ server.js ဖိုင်ကို node မှာ run ချင်တာမလို့ 
    node server.js  လို့ ရေးပါမယ်။
    အောက်မှာ ကျနော်တို့ log ထုတ်ထားတဲ့ dataကို terminal ထဲမှာပဲ buffer အနေနဲ့ ပြပေးနေတာ 
    တွေ့ရမှာပါ။

##
##
### http and server
### http ဆိုတာ *server( backend)*  နဲ့  *browser(frontend)* ကို ချိတ်ဆက်ပေးတဲ့ နည်းပညာ ဖြစ်ပါတယ်။ node js မှာ http ကို အသုံးပြုပြီး web server တစ်ခုကို ကိုယ်တိုင် တည်ဆောက်လို့ရပါတယ်။

### server ဆိုတာက browser(frontend) မှာ ပြပေးမယ့် (ပြုလုပ်ချင်တဲ့)အချက်အလက်တွေကို စီမံခန့်ခွဲပေးတဲ့ နေရာ လို့ အလွယ်သတ်မှတ်နိုင်ပါတယ်။ 
ဆာဗာ ကို ၀င်ရောက် အသုံးပြုနိုင်ဖို့အတွက် 
- **လိပ်စာ( `IP address`)**
- **၀င်ပေါက် ( `port`)** လိုအပ်ပါတယ်။
>  **http `IP-address` `:` `port` http://127.0.0.1:3000**   
### serverကို ထို လိပ်စာနဲ့ ၀င်ပေါက်မှာ အသင့်စောင့်(`listen`) နေပြီး ၀င်လာသမျှ အချက်အလက် ( `request`) တွေကို လက်ခံကာ သက်ဆိုင်ရာ အချက်အလက်များကို ပြန်လည်( `response`) ထုတ်ပေးပါတယ်။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/server.jpg?raw=true)
 ##
 ### Testing JavaScript on `node Server`
 

 ### 1 - server.js ဖိုင်တစ်ခု ဆောက်ပါ။
  ### 2 - server.js ထဲမှာ log တစ်ခု ထုတ်ကြည့်ပါမယ်။
   ### 3 - Node မှာ run ဖို့ node file-name.file-type လို့ terminal မှာ ရေးပေးရပါမယ်။ ပုံထဲမှာတော့ 
  #### ခုနက ကျနော်တို့ ရေးထားတဲ့ server,js ဖိုင်ကို node မှာ run ချင်တာမလို့ `node server.js` လို့ ရေးပါမယ်။
#### အောက်မှာ ကျနော်တို့ log ထုတ်ထားတဲ့ hello node ကို terminal ထဲမှာပဲ ပြပေးနေတာ တွေ့ရမှာပါ။
   
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/node2.jpg?raw=true)
### ထပ်ပြီး setTimeout function  တစ်ခု ထည့်စမ်းကြည့်ပါမယ်
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/node3.jpg?raw=true)

> nodeJs သည် **sever ( back-end) မှာ သုံးတာမလို့** JS file ထဲ log ထုတ်တာကို **browser/GUI (front-end)မှာ သွားကြည့်စရာမလိုပဲ** TUIဖြစ်တဲ့ **terminal ထဲမှာပဲ log ထုတ်ပေးခြင်း**ကို သတိပြုပါ။
##
### NodeJSကို အသုံးပြု၍ simple web server တစ်ခု ကိုယ်တိုင် တည်ဆောက်ခြင်း
### အရင်ဆုံး web server  မဆောက်ခင် ကျနော်တို့ လိုအပ်တဲ့ moduleတွေကို  node ဆီကနေ လှမ်းယူ ထည့်ပေးရပါမယ်။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodehttp1.jpg?raw=true)
> ရှင်းလင်းချက်

### const fs = require("fs");

    file system module ကို require function သုံးပြီး node ကနေ လှမ်းယူလိုက်ပြီး 
    fs ဆိုတဲ့ variable ထဲ သိမ်းလိုက်တာပါ။

### const http = require("http");
   

    http module ကို require function သုံးပြီး node ကနေ လှမ်းယူလိုက်ပြီး 
     http ဆိုတဲ့ variable ထဲ သိမ်းလိုက်တာပါ။
##
### လိုအပ်တဲ့ module တွေ ထည့်ပြီးပြီ ဆိုရင် web server တစ်ခု စ လုပ်ပါမယ်။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodehttp2.jpg?raw=true)
>ရှင်းလင်းချက်

### const  server = http.createServer((req, res) => { });

    http module ထဲက createServer ဆိုတဲ့ method ကို သုံးပြီး 
    server တစ်ခု create လုပ်လိုက်တာကို serverဆိုတဲ့ variableထဲ သိမ်းလိုက်တာပါ။
    ---
    createServer method မှာ call-back function တစ်ခု လက်ခံပါတယ်
    ---
    ထို call-back function မှာ (request , response ) ဆိုပြီး parameter နှစ်ခု လက်ခံပါတယ်။
    ---
    request ဆိုတဲ့ parameter က ဆာဗာကို request လုပ်တာကို လက်ခံပေးပြီး
    response ဆိုတဲ့ parameter က ဆာဗာကနေ response လုပ်တာကို လက်ခံပေးပါတယ်။
    ---
    အတိုကောက်အနေနဲ့ http.createServer((req, res) => { }) ဆိုပြီး ရေးလေ့ရှိပါတယ်။

### server.listen(3000, () => { });

    အထက်မှာ တည်ဆောက်ထားတဲ့ sever အတွက်  ၀င်ပေါက် (port)ကို 3000 အဖြစ်သတ်မှတ်လိုက်ပြီး
    server ကို စောင့်ကြည့်နားထောင်စေလိုက်တာပါ။
    ---
    ထို (port)၀င်ပေါက်ကနေ  ၀င်လာသမျှ request တွေကို  ဆာဗာက စောင့်ကြည့်နားထောင်နေပြီး 
    request တစ်ခု ၀င်လာတိုင်း response တစ်ခု ပြန်ထုတ်ပေးပါမယ်။

##
### server  ကနေ html code တစ်ခု response လုပ်ပြီး browser ပေါ်မှာ ပြသခြင်း
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodehttp3.jpg?raw=true)
>ရှင်းလင်းချက်

>### callback function ( in create server method )
#### `res.writeHead(200, { "Content-Type":  "text/html" }`);

    server ကနေ response ပြန်လာတဲ့ အခါ browser ကနေ သိအောင် ခေါင်းစီး အဖြစ်ထည့်ပေးလိုက်တာပါ။
    --
    ရေးနည်းကတော့ res.writeHead(status-code,content type); ဖြစ်ပါတယ်။
    --
    res.writeHead(200, { "Content-Type":  "text/html" }); မှာ
    --(200) က status code ဖြစ်ပြီး ဆက်သွယ်မှု အောင်မြင်ကြောင်း အသိပေးလိုက်တာပါ။
    --{ "Content-Type":  "text/html" } က serverက response ပြန်တာ 
       html ဖိုင် အမျိုးအစားဖြစ်ပါတယ်လို့ ပြောပြထားတာပါ။
###  **`res.write("<h1>hello world<h1>");`**

    broswer မှာ ပြချင်တဲ့ html ကို response ပြန်တဲ့ အထဲ ရေးထည့်လိုက်တာပါ။
    browser မှာ hello world ဆိုတဲ စာကြောင်းကို header tag အနေနဲ့ ပြပေးပါလို့ ရေးလိုက်တာပါ
### `return  res.end();`

     ဒါကတော့ ရှင်းပါတယ်။ server က response  ပြန်တာပြီးပြီလို့ အသိပေးလိုက်တာပါ။
----
>### callback function ( in server.listen method )
### `console.log("Server started: Listening on port 3000");`
ဆာဗာကို စတင်လိုက်တဲ့ အချိန်မှာ ဆာဗာကို port 3000 မှာ စတင်ကာ စောင့်ကြည့်နားထောင်နေပြီး ဟု
terminal မှာ log တစ်ခုထုတ်လိုက်တာပဲ။ ဆာဗာ on /off သိနိုင်ဖို့အတွက် အသုံးပြုကြပါတယ်။


>### start server in terminal 
### `node server`

    ဒါကတော့ node မှာ server.js ကို ဖွင့်လိုက်တာပါ။ နောက်က .js မထည့်ပဲလဲ ရေးလို့ရပါတယ်။
    အောက်မှာ ဆာဗာစတင်နေပြီး ဖြစ်ကြောင်းကို server.start method မှာ log ထုတ်ထားတဲ့ အတိုင်း
    ပြပေးနေတာဖြစ်ပါတယ်။
#### ခု ကျနော်တို့ server ကို browserမှာ သွားဖွင့်ကြည့်ရအောင်
browser address bar မှာ localhost:3000 လို့ ရိုက်ပြီး enter  ခေါက်ကြည့်လိုက်တဲ့ အခါ
server.js မှာ createServer လုပ်ပြီး response လုပ်ထားတဲ့ hello world ကို header tag တစ်ခုအနေနဲ့
မြင်ရမှာ ဖြစ်ပါတယ်။ **(ဘေးပုံ)**

>server ကို ပိတ်ချင်ရင် terminal မှာ shortcut key **`ctrl`**  `+` **`c`** ကို နှိပ်ပေးရပါမယ်
##
### Server တွင် file တစ်ခုကို ဖတ်ခိုင်းပြီး browser မှာ ပြသခြင်း
### index.html ဖိုင် ကို fs module အသုံးပြု၍ serverကို ဖတ်ခိုင်းကာ ရလာတဲ့ responseကို browser မှာ ပြခိုင်းကြည့်ပါမယ်။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver2.jpg?raw=true)
#### server က response ပြန်တဲ့ res.write မှာ fs က ရလာတဲ့ data ကို ထည့်ပေးလိုက်ရုံပါပဲ။
#### node server.js ကို run လိုက်တဲ့အခါ index.html မှာ ရေးထားတဲ့အတိုင်း မြင်ရမှာ ဖြစ်ပါတယ်။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver3.jpg?raw=true)
##
##
## Try it yourself
### server မှ တစ်ဆင့် route ကို အသုံးပြုပြီး အခြားဖိုင်များနှင့် ချိတ်ဆက်ခြင်း
#### ![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver4.jpg?raw=true)

![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver5.jpg?raw=true)

### တကယ်လို့ request လုပ်တဲ့ url က root ( " / " )ဖြစ်ခဲ့ရင် index.html ဖိုင်ကို response လုပ်ခိုင်းတာပါ။ 
>user က address bar မှာ IP နဲ့ port ပဲ ရိုက်ထည့်ပေးလိုက်ပေမယ့် browser က root ကို auto  ထည့်ပေးလိုက်တာပါ
>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver6.jpg?raw=true)
##
### တကယ်လို့ request လုပ်တဲ့ url က root ( " /about.html " )ဖြစ်ခဲ့ရင် about.html ဖိုင်ကို response လုပ်ခိုင်းတာပါ။ 
> index.html မှာ link ချိတ်ထားတဲ့ Go to About Page ကနေ clickလုပ်လိုက်တာပဲ ဖြစ်ဖြစ်
> address bar မှာ localhost:3000/about.html လို့ ရိုက်ပေးလိုက်တာပဲဖြစ်ဖြစ် about.html ဖိုင်ထဲက
> dataတွေ ပြပေးခိုင်းတာပါ။
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver7.jpg?raw=true)

##
### ဒါကတော့ မရှိတဲ့ ဖိုင်/route ကို address bar မှာ ထည့်မိတဲ့အခါ ပြပေးတာဖြစ်ပါတယ်

![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/nodeserver8.jpg?raw=true)
