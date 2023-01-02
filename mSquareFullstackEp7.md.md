## MSquare Programing Fullstack Course
### Episode-*7* Summary

ဒီနေ့သင်တန်းမှာတော့ 
 - ‌JavaScript Object
 - JavaScript Array
 - loop (for loop)<br>
 စတာတွေ အကြောင်း လေ့လာသွားပါမယ်။
 ## 
 ### Object 
 Object ဆိုတာ data တွေ valueတွေ အများကြီးပါတဲ့ variable တစ်ခုလိုပါပဲ။
 
 #### Declare Syntax

 `const` `object-name` = { 
 `property-key` : `"property-value"` } ;

![enter image description here](https://miro.medium.com/max/856/0*7EptITWWPaI9BoxL.png)
#### Usage syntax
`object-name`.`key` **(Dot** Notation)<br>
`object-name`[`"key"`] (**Bracket** Notation)
#### example

    const user = {
                  name : "Aung Aung",
                  age : 23,
                  address : "Yangon"
                  }
    //dot notation
    const getUserName = user.name;
    console.log(getUserName);
    //"Aung Aung"
    
    // bracket notation
     const getUserAge = user["age"];
     console.log(getUserAge);
     //23
### Important Note

 - object ထဲမှာ property တစ်ခုထပ်ပိုရင် နောက် object မ‌ရေးခင် ကော်မာ **`,`** ထည့် ပေးရပါမယ်။ <br>
 -Example
 

 

       const myObj = {
                       name : "aung aung" ,
                       age : 27
                      }

 - object သိမ်းမယ့် **variable ကြေငြာရင်**  `let` / `var` အစား **`const`** **ကိုသာ အသုံးပြုသင့်**ပါတယ်။

  ##
  ### Array
  object ကဲ့သို့ data တွေ valueတွေ အများကြီးပါတဲ့ variable တစ်ခုလိုပါပဲ<br>
   #### Declare Syntax

 `const` `array-name` = `['A','B','C','D','E','F' `] ;

ခေါ် တဲ့အခါကျရင် object မှာကဲ့သို့ (**Dot** Notation) (**Bracket** Notation) တွေ မသုံးပဲ index နဲ့ အသုံးပြုရမှာပါ။
### Index သတ်မှတ်နည်း
![enter image description here](https://miro.medium.com/max/640/1*hLp5vDQse-YUOpvgI9hfDw.webp)

 #### Usage syntax
 ‌`array-name`[`index`];
 #### example
 

    const myLetter =['A','B','C','D','E','F' ] ;
     const getLetter = myLetter[0];
     console.log(getLetter);
     //'A'
     const getLetter2 = myLetter[4];
     console.log(getLetter2);
     //'E'

### Important Note

- **Array ** မှာ ရှိတဲ့ items တွေ ဘယ်လောက်ပါလဲ သိချင်ရင် **`.length`** ကို သုံးပါတယ်။     
     - **`index` ကို** စရေရင် **0** နဲ့ စပြီး , **`length` ကို 1** နဲ့ စပါတယ်။
     - array တစ်ခုရဲ့ **နောက်ဆုံး`index`** ကို လိုချင်ရင် **‌array.length -1** နဲ့ ရယူနိုင်ပါတယ်။
     
###

    const myLetter =['A','B','C','D','E','F' ] ; 
     //   index       0   1   2   3   4   5
     //   length      1   2   3   4   5   6
    const getLength = myLetter.length; 
    const lastIndex =myLetter.length - 1 ;
    console.log(getLength);
    console.log(lastIndex) 
    //6
    //5 

  
  
##
### Object in Array
#### syntax

    const myUser = [
                    "Bo Bo",
                    { name : "ko ko",
                      age : 35},
                      "27" ];
    
    // to get ko ko and his age
    const userName = myUser[1].name;
    const userAge = myUser[1].age;
    console.log(userName + " is " +userAge + " years old");
    // ko ko is 35 years old
    
    //get Bo Bo and his age
    const userName2 = myUser[0];
    const userAge2 = myUser[2];
    console.log(userName2 + " is " +userAge2 + " years old");
    // Bo Bo is 27 years old
    
                      
   ##
   ### loop 
   သတ်မှတ်ထားတဲ့ အခြေအနေကို မရောက်မချင်း တစ်ပတ်ပြီး တစ်ပတ် အကြိမ်ကြိမ်ပတ်နေ‌စေလိုသောအခါ အသုံးပြုရပါတယ်။
  ### for loop 
   #### syntax
  

     for ( let i = 1 ; i < 5 ; i++){ 
       console.log("Now i is equal to" +" : " + i)
       } ;
     /*
    (အဆင့် တစ် )i ကို 1 ဟု သတ်မှတ်ပါ။(let i = 1 )
    (အဆင့် နှစ် )i က 5 ထပ် ငယ်နေသေးသ၍ အထဲက ကုဒ်ကို run ပေးပါ။( i < 5 )
    (အဆင့် သုံး )တစ်ခါ loop ပြီးတိုင်း i ကို  1 တိုးပေး ပါ။(i++ )
    */
    //Now i is equal to : 1 (ပထမအကြိမ် loop , i တန်ဖိုး 1 ကနေ 2 သို့ တိုးသွား)
    // Now i is equal to : 2 (ဒုတိယအကြိမ် loop , i တန်ဖိုး 2 ကနေ 3 သို့ တိုးသွား)
    // Now i is equal to : 3 (တတိယအကြိမ် loop , i တန်ဖိုး 3 ကနေ 4 သို့ တိုးသွား)
    // Now i is equal to : 4 (စတုတ္ထအကြိမ် loop , i တန်ဖိုး 4 ကနေ 5 သို့ တိုးသွား)
    
    /*
    (အဆင့် နှစ် )i က 5 ထပ် ငယ်နေသေးသ၍ အထဲက ကုဒ်ကို run ပေးပါ။
    ( i < 5 ) လို့ သတ်မှတ်ထားခဲ့အတွက်  i တန်ဖိုး 5 ရောက်တဲ့အခါမှာတော့
     loop ပတ်ခြင်းအလုပ် ပြီးမြောက်သွားပါတယ် 
    */
   ##
   ### Looping Array 
   #### syntax
   `for` ( `let` `index = 0` ; `index` < `array.length` ; `index++`){ Run this code } ;<br>
   index ရဲ့ တန်ဖိုးဟာ 0 ဖြစ်သည်။ index ရဲ့ တန်ဖိုးဟာ array ထဲရှိ items ရှိသလောက်ထပ် နည်းနေသ၍ loop လုပ်ပေးပါ။ <br>loop တစ်ခါလုပ်တိုင်း index တန်ဖိုးကို 1 တိုးပေးပါ။
   #### EXAMPLE

    const arrayForloop = [
                          {
                           name : " Ko Ko",
                           age : 23,
                           email : "koko23@web.de"
                           },
                           {
                           name : " Mg Mg",
                           age : 28,
                           email : "mgmg28@web.de"
                           },
                           {
                           name : " Bo Bo",
                           age : 24,
                           email : "bobo24@web.de"
                           },
                           {
                           name : " Su Su",
                           age : 21,
                           email : "susu21@web.de"
                           }
                          
                         ];
             //loop one (Get user Email)
            for(let index = 0 ; index < arrayForloop.length ; index++){
              const userEmail = arrayForloop[index].email;
              console.log(userEmail);
            };
            //koko23@web.de
            //mgmg28@web.de
            //bobo24@web.de
            //susu21@web.de
            
            //loop two (Get user Name)
            for(let i = 0 ; i < arrayForloop.length ; i++){
              const userName = arrayForloop[i].name;
              console.log(userName);
            };
           //Ko Ko
           //Mg Mg
           //Bo Bo
           //Su Su

