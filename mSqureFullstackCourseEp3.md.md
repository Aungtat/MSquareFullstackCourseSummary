
## Msqure Programing Fullstack Course
### Episode 3 Summary
Episode 3 မှာတော့ 
CSS Layout နဲ့ ပတ်သတ်တဲ့ အရာတွေ လေ့လာသွားကြပါမယ်။

 - Media Query
 - CSS Box-model
 - CSS flex-box 
 စတာတွေလေ့လာသွားကြမှာပါ။
### Media Query
ယနေ့ခေတ်မှာ website တွေကို ကွန်ပြူတာကနေပဲ ၀င်ရောက် အသုံးပြုကြတာ မဟုတ်ပဲ mobile Phone/Tablet/TV စတဲ့ Devie မျိုးစုံကနေ  ၀င်ရောက် အသုံးပြုကြလေ့ရှိပါတယ်။
web ကို အသုံးပြုသူများရဲ့ 50%ကျော်ဟာ Smart Phone ကနေ ၀င်ရောက်ကြတာပါ။
   Devie မျိုးစုံအတွက် ကြည့်ရှုရ အဆင်ပြေစေရန်
   Media Query ကို အသုံးပြုရတာပါ။

![enter image description here](https://www.freecodecamp.org/news/content/images/2021/05/image-56.png)
သတ်မှတ်ထားတဲ့ screen size ရောက်တဲ့အခါ အထဲမှာ ရေးထားတဲ့ CSS code တွေ အလုပ်လုပ်ပါလို့ ကြေငြာထားတာပါ။
 ဥပမာ။ ။

   **Example**

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Media query</title>
            <style>
                p{
                    color : blue;
                }
    
               @media  screen and (min-width: 600px) {
                p {
                    color : red;
                }
               }
            </style>
    </head>
    <body>
        <p>Hello</p>
    </body>
    </html>

အထက်က  ကုဒ် ကို လေ့လာကြည့်ရအောင်။
p tag တစ်ခုမှာ Hello ရေးပေးထားတယ်။ အဲ့ဒါကိုCSS နဲ့ color နှစ်မျိုး ပေးထားပါတယ်။<br>
`@media  screen and (min-width: 600px)`  က **screen size 600px ထက် ကြီးတယ် ဆိုရင် သူ့အထဲ က ကုဒ်တွေ run ပေးပါလို့**  ကြေငြာထားတာပါ။<br>
တစ်နည်း အားဖြင့် screen size 600px ထက် **ငယ်တယ် ဆိုရင် သူ့အပြင် က ကုဒ်တွေ run** ပေးပါလို့  လဲပြောလို့ရပါတယ်။<br>
အထက်က html ကို **screen size 600px ထက် ငယ်တဲ့ ဖုန်းနဲ့ ဖွင့်ကြည့်ရင်** Hello ဆိုတဲ့ စာဟာ **အပြာရောင်** ဖြစ်နေပြီး 
 **screen size 600px ထက် ကြီးတဲ့ ကွန်ပြူတာ**နဲ့ဆို **အနီရောင်** အဖြစ် မြင်ရမှာပါ။
 <br>
နမူနာပြထားသလိုပဲ 
screen size ဘယ် အရွယ် ရောက် ရင် ဒါကိုပဲပြပေးပါ ဟိုဒါကိုတော့ဖွက်ထားပေးပါ။
ဒါကိုတော့ ဒီလိုပြောင်းလိုက်ပါ စသည်ဖြင့် **Responsive ဖြစ်အောင် Media query နဲ့ ဖန်တီးလို့ရပါတယ်။**

### CSS Box-model

![enter image description here](https://lh6.googleusercontent.com/n3LEsgGJx6nsOtm3MaoI2Ro8FqznwaJ2TDzWZL_KzucTXVDNEyqBtH4XrbMNMtfOv_d9q2HA3G0kU7fDM8tOLYuS2NfBA9CmERRqIGkbQ8P1VYvLj7xI9vJirpCJWJF1r5AMKaKy)
    
**Margin** ဆိုတာက element နဲ့ စာမျက်နှာအစွန်း ရဲ့ အကွာအ၀ေးပါ
 margin : 20px ; ဆိုရင်  element ကို စာမျက်နှာအစွန်းကနေ 20px ခွါပေးပါလို့ ပြောလိုက်တာပါ။
 ![enter image description here](https://4.bp.blogspot.com/-N3SbVSNaxac/UtA5nfYVlTI/AAAAAAAAAAc/X6xjzVfaH6g/s1600/css+margin+layout.png)
 လိုချင်တဲ့ နေရာလောက်ပဲ margin ပေးချင်ရင်
 ပုံထဲကအတိုင်း အပေါ်ဘက်ဆိုရင် 
 ```margig-top : 20px;``` 
 ရေးပေးရပါမယ်။
 အလားတူပဲ
  ```margig-left : 10px;``` 
   ```margig-bottom : 5px;``` 
    ```margig-right : 0px;``` 
    ကြိုက်သလို သတ်မှတ်နိုင်ပါတယ်

**short-hand** 

    margin : X Y;

X = margin-top + margin-bottom
Y = margin-right + margin-left

    margin : 10px 0px;
အပေါ် နဲ့ အောက်ကို margin 10px စီ ထားပြီး ဘေးဘယ်/ညာ ကို 0 ပဲထားပါလို့ ပြောလိုက်တာပါ။

    margin : top right bottom left:
    margin : 20px 0px 5px 10px;
အပေါ် 20px  ညာ 0px အောက်5px  ဘယ်10px
##
**Border** ဆိုတာက element ရဲ့ ဘောင် ဖြစ်ပါတယ်။
element ရဲ့ ဘောင် သတ်မှတ်ချင်ရင် 
အရွယ်အစား `border-width : 1px ;`
ပုံစံ `border-style : solid ;`
အရောင်  `border-color : black ;`
စတာတွေနဲ့ သတ်မှတ်ပေးရပါတယ်။

Short-Hand
**border : width *style* color;**

    border : 1px solid black ;


**Padding** ကတော့ Content နဲ့ border ကြား အကွားအ၀ေး ပါ။

![enter image description here](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQm6mrQioTK-r8tMtNwgVa62-mvdcJHRgoI2A&usqp=CAU)

    padding : 5px
  
Content နဲ့ border ကြား အကွားအ၀ေးကို ပတ်ပတ်လည် 5px စီ ခြားလိုက်ပါလို့ ပြောပြလိုက်တာ။ Margin ကဲ့သို့ ရေးသားပြီး အသုံးပြုနိုင်ပါတယ်။

##
### CSS Flex-Box
Html element တွေကို Layoutချတဲ့ အခါ အသုံးပြုပါတယ်။
Real world web app တွေ ရေးတဲ့အခါ တကယ်ကို အသုံများတဲ့ CSS နည်းပညာပါ။
Flex-box ကို မလေ့လာခင် Html Element တွေ ရဲ့ nesting သဘောသဘာ၀ကို အရင်သိထားရပါမယ်။
``` html
<div class="container"> parent element
     <div>child element
     Div 1
     </div>
     <div>child element
      Div2
     </div>
</div> 
```
Div နှစ်ခု ကို Div တစ်ခုထဲမှာ ထည့်ထားပါတယ်။
Div နှစ်ခုကို ထိန်းထားတဲ့ container ဆိုတဲ့ Div ဟာ သူ့အထဲက Div နှစ်ခုရဲ့ မိဘ parent ဖြစ်ပါတယ်။
အထဲက Div နှစ်ခုဟာ container Div ရဲ့ ကလေး child ဖြစ်ကြပါတယ်။

parent Div ကို display : flex; လို့ CSS property ပေးလိုက်တာနဲ့  သူ့ရဲ့ child Div တွေကို နေရာချ စီမံလို့ ရပါပြီး။

``` html
<div class="container"> parent element
     <div>child element
     Div 1
     </div>
     <div>child element
      Div2
     </div>
</div> 

CSS
   .container {
     display: flex ; 
    }
```
အသုံးများသော Flex -box property များ

    flex-direction : ### ;
    justify-content : ### ;
    align-items : ### ;
    flex-warp : ### ;
![enter image description here](https://byteiota.com/wp-content/uploads/2020/11/flex-direction.png)
![enter image description here](https://miro.medium.com/max/434/1*iigDGiNFBOUVJQ_07C1B2g.png)
![enter image description here](data:image/png;base64,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)
![enter image description here](https://samanthaming.gumlet.io/flexbox30/10-flex-wrap.jpg.gz)
##
    justify-content : center;
    align-items : conter

![enter image description here](http://2.bp.blogspot.com/-wSizB5Yw-EU/UCzPr_RVTzI/AAAAAAAAElg/a2BecXgMjSI/s1600/flexbox_layout.png)

### Important Note

 - margin /padding စတဲ့ CSS properties တွေဟာ Element တစ်ခုကို နေရာချ တဲ့ အခါ အသုံးပြုပြီး Layout များ လုပ်တဲ့အခါမှာတော့ flex-box ကို အသုံးပြုဖို့ ပိုပြီးသင့်တော်ပါတယ်။
 - display inline ဖြစ်တဲ့ element တွေကို width and height ပေးချင်ရင်  display : inline-block ဒါမှမဟုတ် display: block; အရင်ပြောင်းပေးရပါမယ်။
 - -child  DIv တွေကို စီမံချင်ရင် သူတို့တွေကို ထိန်းထားတဲ့ parent Div မှာ display : flex ;  ပေးပြီး flex-box properties တွေကို parent Div ရဲ့ CSS အထဲမှာပဲ စီမံရပါမယ်။
 - ပုံ နဲ့ စာ ကို center ကျကျ ထားချင်ရင် `vertical-align : middle ;` ကို သုံးနိုင်ပါတယ်။
##
## Q&A
   
Q. Media query မှာ min/max width ပုံသေသတ်မှတ်ချက် ရှိပါသလား?<br>
A. မရှိပါ။ W3School က သတ်မှတ်ပေးထားတဲ့ အတိုင်းဆို အဆင်ပြေပါတယ်

    /* Extra small devices (phones, 600px and down) */  
    @media only screen and (max-width: 600px) {...}  
      
    /* Small devices (portrait tablets and large phones, 600px and up) */  
    @media only screen and (min-width: 600px) {...}  
      
    /* Medium devices (landscape tablets, 768px and up) */  
    @media only screen and (min-width: 768px) {...}  
      
    /* Large devices (laptops/desktops, 992px and up) */  
    @media only screen and (min-width: 992px) {...}  
      
    /* Extra large devices (large laptops and desktops, 1200px and up) */  
    @media only screen and (min-width: 1200px) {...}
     
Q. What is SVG format Picture?SVG ပုံဆိုတာ ဘာလဲ?<br>
A . Code တွေနဲ့ ဖန်တီးထားတဲ့ပုံ ပါ။ SVGပုံကို browser နဲ့ ဖွင့်ကြည့်ရင် သာမာန်ပုံတစ်ပုံလို မြင်ရပေမဲ့ VS code နဲ့ ဖွင့်ကြည့်ပါ code တွေနဲ့ ဖွဲ့ စည်းထာတာ မြင်ရမှာပါ.
ပြင်ချင်တဲ့အရာကို photo editor တွေ မလိုပဲ vs code ထဲမှာတင် ပြုပြင်လို့ ရပါတယ်။
SVG ရဲ့ အားသာချက်က ပုံ ဘယ်လောက် ကြီးကြီး resolution မကျသွားစေပဲ ပုံ ကွာလတီ အတိုင်း မြင်ရအောင် စွမ်းဆောင်ပေးပါတယ်။ 
