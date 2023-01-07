## MSquare Programing Fullstack Course
### Episode-10 *Summary*

ဒီနေ့သင်တန်းမှာတော့ 

 - **setTimeout** 
 - **Promise**
 - **fetch**
 <br>စတာတွေအကြောင်း လေ့လာသွားမှာပါ။
 ##
 ### setTimeout()
 လုပ်ဆောင်ချက်တစ်ခုကို အချိန်တစ်ခု သတ်မှတ်ထားပေးပြီး သတ်မှတ်ထားတဲ့ အချိန်ရောက်မှ အလုပ်လုပ်ခိုင်းတာပါ။
 #### Syntax

`setTimeout`(`callback-function`, `delay-time`)
#### Usage

    setTimeout(() => console.log("Delayed for 1 second."), 1000);
    //အချိန် 1000ms(တစ်စက္ကန့်)ကြာပြီးမှ console.log ကို run ပေးပါ။
  > 1000 = 1000 milli second = 1 second   
  ##
  ### Promise
  callback function  တွေကဲ့သို့ အရင်လုပ်နေတဲ့ လုပ်ဆောင်ချက်တွေ မပြီးမချင်း စောင့်ပြီးမှ အလုပ်လုပ်စေချင်တဲ့အခါ အသုံးပြုလေ့ရှိပါတယ်။<br>
  `Network Request` , `Data respond`  တွေ စောင့်ပြီးမှ ဆက်လက်လုပ်ဆောင်ရမယ့်အခါ **promise**ကို သုံးရပါတယ်။
  <br>
  ### Syntax
  `promise-Name` `=` `new Promise` ((`fulfill`,`reject`) `=>{`Do somethings..`};`
  
  
 ![enter image description here](https://cdn.programiz.com/sites/tutorial2program/files/javascript-promise.png)
 <br>
 ပုံကို လေ့လာကြည့်ရင် promise တစ်ခု
 - ပြီးမြောက်(fulfill/ **resolve**) သွားပါက **.then()** **method** ကို ဆက် run မှာ ဖြစ်ပြီး
 - မပြီးမြောက်(**reject**/error )ပါက **.catch() method** ကို သွား run ပေးမှာပါ။


 
 #### example-1   resolve(**result**) > .then(**result**) 
 
```
const countValue = new Promise((resolve, reject)=> {
  resolve("Promise resolved");
});


countValue
.then((result)=> {
    console.log("the result from resolve is" ,result);
  })
.catch((error)=> {
        console.log(error);
    });
    //output: the data from resolve is Promise resolved
    
```

 #### example-2  reject(**error**) > .catch(**error**) 
 
```
const countValue = new Promise((resolve, reject)=> {
  reject("promise rejected");
});


countValue
.then((data)=> {
    console.log("the result from resolve is" ,result);
  })
.catch((error)=> {
        console.log("error from reject is" ,error);
  });
    //output: error from reject is promise rejected
    
```
## 
### promise chaining 
####  when resolve

    const testPromise = new Promise ((resolve,reject) => resolve("Hello"));
    
    testPromise
      .then((result1)=> result1 + " " +"world")
      //return "Hello world" as result2
      .then((result2)=> console.log(result2 + " " +"Myanmar"))
      //output: Hello world Myanmar
      .catch((error)=> console.log(error));

####  when reject

    const testPromise = new Promise ((resolve,reject) => reject("rejected"));
    
    testPromise
      .then((result1)=> result1 + " " +"world")
      //return "Hello world" as result2
      .then((result2)=> console.log(result2 + " " +"Myanmar"))
      .catch((error)=> console.log("Your promise is" ,error));
      //output: Your promise is rejected


## 
### fetch
Url တစ်ခု (api)က data တွေကို လှမ်းယူတဲ့အခါ အသုံးပြုကြပါတယ်။ <br>
**fetch() method** က **promise တစ်ခုကို return** ပြန်ပေးပါတယ်။<br>
**promise တစ်ခုကို return** ပြန်ပေးတဲ့အခါ **resolve (or) reject ကို auto သတ်မှတ်**ပေးပါတယ်။

#### Syntax
`fetch`(`url`);

#### Usage
```
const url ='https://fakestoreapi.com/products?limit=5'
fetch(url)
//promise တစ်ခု return ပြန်ပေးတာမလို့ .then() .catch() method တွေ သုံးလို့ရပါပြီး
  .then((response) => response.json())
  //ရလာတဲ့ promise ကို json ပြောင်းလိုက်တာပါ။
  .then((data) => console.log(data));
  //ရလာတဲ့ json ကို data အနေနဲ့ သိမ်းလိုက်ပြီး၊ log ထုတ်ကြည့်တာပါ။
```
### Example 
> return ပြန်လာတဲ့ data မှ total price ကို ရှာကြည့်ရအောင်။
```
const url ='https://fakestoreapi.com/products?limit=5'
fetch(url)
  .then((response) => response.json())
  .then((data) => {
    let totalPrice = 0;
    data.forEach(data =>{
    let productPrice = parseInt(data.price);
     totalPrice += productPrice;
    })
    console.log(totalPrice);
  });
  //output: 896
```

   
  



                                                
                                                


                                                           
  
  
    
    


 

