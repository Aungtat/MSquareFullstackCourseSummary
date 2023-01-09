## MSquare Programing Fullstack Course
#### Episode-9 Summary
ဒီနေ့သင်တန်းမှာတော့

 - try catch
 - while loop
 - for in loop
 - Object/Array destructuring 
 - ternary operator <br>
 စတာတွေ အကြောင်း လေ့လာသွားမှာပါ။
 ## 
 ### Try Catch
 Javascript မှာ  ပေါ် လာတဲ့ error  တွေကို ဖမ်းယူချင်တဲ့အခါ သုံးရပါတယ်။
 #### Syntax
 

    try{
       code here
    } catch (error){
       console.log(error)
    }
#### Example
   

    try{
      const num1 = 10 ;
      num1 += 20;
     } catch (error){
       console.log(error)
     }
     /*output: TypeError: Assignment to constant variable.
               at <anonymous>:3:13 */
##
### While loop
loop လုပ်ချင်တဲ့အခါ သုံးရပါတယ်။<br>
`While loop`ကို သုံးဖို့ အရေးကြီးတဲ့ အချက်က ဘယ်အချိန်မှာ ရပ်ပါ ဆိုတဲ့ `exit condition` ကို **မဖြစ်မနေ** ထည့် ရေးပေးရပါမယ်။<br>
 **`exit condition` မပါခဲ့ရင်** loop ဆက်တိုက် လုပ်နေကာ **ကွန်ပြူတာ ဘာမှလုပ်မရတော့ပဲ ရပ်သွားသည်အထိ ပြဿနာ ဖြစ်နိုင်ပါတယ်။**
#### Syntax

    while(condition){
       //Run this code
        //exit-condition    
    }

#### Usage

    let num1= 0;
    while(num1 < 10){
     console.log(num1);
     num1++ ;
    }
    //output :
    //0
    //1
    //2
    //3
    //4
    //5
    //6
    //7
    //8
    //9
    

(**condition**) တကယ်လို့ `num1` က **10 ထပ် ငယ်နေသရွေ့**  <br>
(**Run this code)** `num1`ကို log ထုတ်ပေးပါ။<br>
(**exit-condition**) ပြီးရင် **`num1` ကို 1 တိုးပေးပါ။**<br>

>တစ်နည်း

**num1 တန်ဖိုးက 10 မဖြစ်မချင်း**<br> `num1`ကို **log ထုတ်ပေးထားပါ။** <br>တစ်ခါ loop လုပ်တိုင်း `num1` ကို 1 တိုးပေးပါ။<br>

>တစ်နည်း

 `while loop` ကို  ၁၀ ကြိမ် run ပေးပါ။

## 

### Array destructuring 
arrayထဲရှိ item တွေကို ခွဲ/ထုတ် လိုတဲ့အခါ သုံးပါတယ်။
#### Syntax
`array-name` = `[ item, item, item, item, ]`;
`[variable-name]` = `array-name` ;

#### Usage
> example-1

    const numberArray = [ 1, 4, 7, 9, 18];
    const [a,b] = numberArray;
    console.log (a); //1
    console.log (b); // 4

> example-2

    const numberArray = [ 1, 4, 7, 9, 18];
    const [a,b,c] = numberArray;
    console.log (a); // 1
    console.log (b);// 4
    console.log (c);// 7
> example-3

    const numberArray = [ 1, 4, 7, 9, 18];
    const [a,b,...rest] = numberArray;
    console.log (a); // 1
    console.log (b); // 4
    console.log (rest); // [7,9,18]
## 
### Object destructuring 
Object ထဲရှိ item တွေကို ခွဲ/ထုတ် လိုတဲ့အခါ သုံးပါတယ်။

>Example-1


    const product = {
				     id: 1 , 
				     price: 100 , 
				     name: "T shirt" , 
				     color: "blue"
				     };
    
    const {id,price} = product;
     
     console.log(id); // 1
     console.log(price); // 100
>Example-2


    const product = {
				     id: 1 , 
				     price: 100 , 
				     name: "T shirt" , 
				     color: "blue"
				     };
    
    const discountPrice = ({price}) => console.log(price * 0.9);
     discountPrice(product) 
     // 90
     
   ##
   ### for in loop 
   #### Syntax
   **`for`** ( **`variable`** **in** **`Object-name`**){
   console.log ( { **[** **`variable`** **]** `:` **`Object-name`** **[** **`variable`** **]**} );
   };

    const testObj ={
				    name : "MSqure programing",
				    type : "Web Dev",
				    course : "fullstack"
				    };
	for( let superman in testObj){
	    console.log({ [superman]: testObj[superman]});
	    };
	    //{name: 'MSqure programing'}
	    //{type: 'Web Dev'}
	    //{course: 'fullstack'}
##
### ternary Operator

Conditional (if , else) ကို အတိုကောက်ရေးနည်းဖြစ်သည်။
#### Syntax
**condition** `?` *true* `:` *false* ;
> Example (True)
> 
const `num1` = `20`;
`num1 === 20` **`? console.log("All right")`**  `: console.log("Nottt!!")`  ;
//output : All right
> Example (False)
> 
const `num1` = `56`;
`num1 === 20` `? console.log("All right")`  ***`: console.log("Nottt!!")`***  ;
//output :Nottt!!
