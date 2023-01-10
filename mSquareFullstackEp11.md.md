## MSquare Programing Fullstack Course
#### Episode-11 Summary
ဒီနေ့သင်တန်းမှာတော့

DOM (**D**ocument **O**bject **M**odel)<br>
  အကြောင်း လေ့လာသွားမှာပါ။
 ## 
 #### Html ထဲကို javascript file ချိတ်မယ်ဆိုရင် `</body>` အပေါ်မှာ<br> `<script src="app.js"></script>`<br>ချိတ်ထည့်ပေးရပါမယ်
 

    <!DOCTYPE  html>
    
    <html  lang="en">
    
      <head>
   
      <title>Document</title>
    
      </head>
    
      <body>
    
       <script  src="app.js"></script>
      </body>
    
     </html>
## 
### Document  method အသုံးပြု၍ html elementများ လှမ်းယူနည်း

    <div class="hello" id="world"></div>
    
    document.getElementsByTagName("div")
    
    document.getElementById("world")
    
    document.getElementsByClassName("hello")
<br>

>Using QuerySelecter
<br>
![alt text](https://cdn.dribbble.com/users/1343196/screenshots/13992184/upload_f.png?compress=1&resize=400x300)

> class name တူသော element များကို တစ်ခါထည်း လှမ်းယူလိုပါက querySelectorAll() ကို အသုံးပြုနိုင်

    //Html
    <div  class="hello div1">div 1</div>
    <div  class="hello div2">div 2</div>
    <div  class="hello div3">div 3</div>
    
    //Javascript
    const  allDiv = document.querySelectorAll(".hello");
      console.log(allDiv)
    //NodeList(3) [div.hello, div.hello, div.hello]

##
###  Document  method အသုံးပြု၍ html elementများ ဖန်တီးခြင်း
>for create `Div` element

    const newDiv = document.createElement("div");
    
 >  for create `image` element

    const newImg = document.createElement("img");
##
### Add style in html element
#### Syntax
`element-name` **.** `style` **.** `css-property` **=** **"**`property-value`**"**;
> example

    //html
    <div class="hello">DIV TAG</div>
    
    //JavaScript
    const newDiv = document.querySelector(".hello");
     newDiv.style.color ="blue";
     newDiv.style.fontSize ="20px";
     newDiv.style.border ="1px solid black";

Styleတွ အများကြီးထည့်ချင်ရင် တော့ <br>`cssText` ကို template literal အသုံးပြုပြီး ရေးနိုင်ပါတယ်။
```html
const newDiv =document.querySelector(".hello");      
newDiv.style.cssText =`color:blue; 
                       font-size:20px; 
                       border: 1px solid black;`
```
> **Template literal**
> string ထဲမှာ code တွေ variable တွေ ထည့်ရေးလိုတဲ့အခါ အသုံးပြုပါတယ်။

> `backtick key` ( **``**  ) နှစ်ခုထဲမှာ ထည့်ရေးပေးရပါမယ်။
   

#### Example

     const num1 = 25;
     
     //normal
     console.log("Room" + " "+ num1 +" " + "is my new room");
     
     //Template literal
     console.log ( ` Room ${num1} is my new room `)


##
### Append()
Create လုပ်ထားတဲ့ html element တွေကို html file ထဲ ထည့်ရန်သုံးပါတယ်။
> Example

    //html
    <div class="container" ></div>
    
    //JS
    const containerTag =document.querySelector(".container");
    const newDiv = document.createElement("div");
     
      containerTag.append(newDiv);
    //containerTagထဲကို newDiv ထည့်ပေးလိုက်ပါ။
    
 

   >Multiple append
   >
   `Image` element တစ်ခုကို `Div` တစ်ခုထဲ ထည့်ပြီး html ဖိုင်ထဲက `container div` ထဲ ထည့်မယ်ဆိုပါစို့။
    
        //html 
        <div class="container" ></div> 
        
        //JS 
        const containerTag =document.querySelector(".container"); 
        const newDiv = document.createElement("div"); 
        const newImg= document.createElement("img");
         newDiv.append(newImg);
         containerTag.append(newDiv); 
        
   ##
   ### innerHtml
   သက်ဆိုင်ရာ element ထဲကို html codeတွေ ရေးထည့်ပေးတာပါ။<br>
   Element တွေ အများကြီး create လုပ်ဖို့ လိုအပ်လာပါက innerHtml ကို အသုံးပြုနိုင်ပါတယ်။
   >example
  
  အထက်ပါအတိုင်း `Image element` တစ်ခုကို `Div` တစ်ခုထဲ ထည့်ပြီး html ဖိုင်ထဲက `container div` ထဲ ထည့်မယ်ဆိုပါစို့။
 

       //html 
           <div class="container" ></div> 
           
           //JS
            const containerTag =document.querySelector(".container"`);
            containerTag.innerHtml =`
                                  <div>
                                  <img src="" />
                                  </div>
                                  `

  ##
  ### classList
   သက်ဆိုင်ရာ html element ကို class ထည့်/ဖယ်/စစ် ပေးရန် သုံးသည်။
   >add class
   
    //html (before class Added)
        <div class="container" ></div> 
        
        //JS 
        const containerTag =document.querySelector(".container"); 
        containerTag.classList.add("main");
         
         // html (after class Added)
        <div class="container main" ></div>
> remove calss
        
    // html (before class remove)
            <div class="container main" ></div>
            
            //JS 
            const containerTag =document.querySelector(".container"); 
            containerTag.classList.remove("main");
            
            //html(after class remove)
            <div class="container" ></div> 
            
  > contains ( class ရှိ မရှိ စစ်)
  
    //html
    <div class="container main" ></div>
    
    //JS
     const containerTag =document.querySelector(".container"); 
     let chkClass = containerTag.classList.contains("main"); //True
       let chkClass = containerTag.classList.contains("superman");//False


