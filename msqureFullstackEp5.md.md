## Msqure Programing Fullstack Course
### Episode 5 *Summary*

ဒီနေ့မှာတော့ Javascript အခြေခံလေးတွေကို ပြန်နွှေးပေးသွားမှာပါ။
ဒီနေ့သင်တာတွေ နားမလည်သေးဘူးဆိုရင် Msqure Youtube Channel မှာ အသေးစိတ်ရှင်းပြထားတွေကို သေချာလေး ပြန်ကြည့်ကြစေလိုပါတယ်။

JavaScript ရဲ့

 - Data-type
 - Variable
 - Scope
 - Operator
 - conditional statement
 စတာတွေကို လေ့လာသွားကြမှာပါ။


### JavaScript Data Types
<table border="0"><tbody><tr><td>Data Types</td>
				<td>ရှင်းလင်းချက်</td>
				<td>Example</td>
			</tr><tr><td><code>String</code></td>
				<td>စကားလုံး/စကားစု</td>
				<td><code>'hello'</code>, <code>"hello world!"</code> etc</td>
			</tr><tr><td><code>Number</code></td>
				<td>နံပါတ်များ</td>
				<td><code>3</code>, <code>3.234</code>, <code>3e-2</code> etc.</td>
			</tr><tr><td><code>BigInt</code></td>
				<td>an integer with arbitrary precision</td>
				<td><code>900719925124740999n</code> , <code>1n</code> etc.</td>
			</tr><tr><td><code>Boolean</code></td>
				<td>မှန်သည် (သို့) မှားသည် </td>
				<td><code>true</code> and <code>false</code></td>
			</tr><tr><td><code>undefined</code></td>
				<td>မသတ်မှတ်ရသေးသော</td>
				<td><code>let a;</code></td>
			</tr><tr><td><code>null</code></td>
				<td>တန်ဖိုး Null ဖြစ်နေသော</td>
				<td><code>let a = null;</code></td>
			</tr><tr><td><code>Symbol</code></td>
				<td>သင်္ကေတ</td>
				<td><code>let value = Symbol('hello');</code></td>
			</tr><tr><td><code>Object</code></td>
				<td>အချက်အလက်များ စုစည်းထားသော</td>
				<td><code>let student = { };</code></td>
			</tr></tbody></table>



### Note 

 - `string` data-type သည် 
 -**Single quotes**:  `'Hello'`
-**Double quotes**:  `"Hello"`
-- **Backticks**:  `` `Hello` `` စသည် တို့ တစ်ခုခုဖြင့် ရေးသားပေးရသည်။ Single/Double quotes, backticks မပါသော text သည် `string` မဟုတ်ပေ။ ထို့ပြင် `"6"` `"209"` စသည်တို့သည် Double quotes ဖြင့် ရေးထားသောကြောင့်  `Number` data-type မဟုတ်ပဲ `string` data type ဖြစ်သည်။

- အထက်တွင် ဖော်ပြထားသောdata types  ထဲတွင် `object` data-type တစ်ခုမှလွဲပြီး ကျန် အားလုံးသည် **Primitive Data Type** (ထပ်ခွဲ၍ မရနိုင်သော) ဖြစ်ပြီး   `object` data-type မှာ  **Non-Primitive Data Type** (ထပ်ခွဲ၍ ရ) ဖြစ်သည်။

###  Variable
Variable ကြေငြာရန် var , let , const စသည့် keyword များ အသုံးပြုပေးရသည်။
**Syntax**
`keyword`  `Variable's name` = `Value` ;

    var num1 = 4 ; 
    let userName =  "Aung Myanmar" ;
    const age = 30 ;
### note

 - **var နှင့်  let**  သည် တစ်ခါကြေငြာပြီး နောက် **ပြုပြင်ပြောင်းလဲ၍ ရ**ပါသည်။  
 - **const** ကို အသုံးပြုပြီး ကြေငြာထားရင်ေတာ့ **ထပ်မံပြောင်းလဲ၍ မရနိုင်**ပါ။
 
  `keyword`  `Variable's name` = `Value` ; (**console,log result**) 

example : 1 ( **var** )
   
    var userName = "ko ko" ; ( ko ko )
      userName = "Mg Mg" ; ( Mg Mg )

 example : 2  ( **let** )

     var num1 = 5
      const num2= 8;
       let num3 = 2 ; ( 2 )
       num3 = num1 + num2 ; ( 13 )

example : 3 ( **const** )

    var num5 = 7 :
    const num6 = 3 ; ( 3 )
    let num7 = 19 ;
    num6 = num5 + num7 ; ( Error ) 

  
   ### Scope
  

     const userName = " koko" ; ( Global Scope )
       **//မည်သည့် နေရာကမဆို ခေါ်သုံး လို့ရ**  
      
       let creatEmail = ( ) = > {
       
       const userNameTwo = "mgmg"; ( internal Scope)
       **//ဤ checkName function ထဲ၌သာ ခေါ်သုံးခွင့်ရှိ ၊
       အခြားမည်သည့်နေရာတွင်မှ ခေါ်သုံးခွင့်မရနိုင်'**

       const newEmail = userName + "@gmail.com" ;
       console.log (newEmail) ;// koko@gmail.com //

       } ;
       
       creatEmail( );
       
       let creatSayHi = ( ) = > {
      
       const userName3 = " MA MA" ;
       const helloGuest3 = userName3 + "Mingalar Par" ;
       console.log (helloGuest3) ;// MA MA Mingalar Par //

       const helloGuest = userName + "Mingalar Par" ;
       console.log (helloGuest) ;// koko Mingalar Par //
       
       const helloGuestTwo = userNameTwo + "Mingalar Par" ;
       console.log (helloGuestTwo) ; // Error //

       } ;
       creatSayHi( );
### JavaScript Operator(s)
1. #### Arithmetic Operators
  သင်္ချာ ကဲ့သို့ ပေါင်းနှုတ်‌မြောက်စား စတာတွေလုပ်ပေးတာဖြစ်ပါတယ်။
  <table class="table table-bordered">
            <thead>
                <tr>
                    <th>
                        Operator
                    </th>
                    <th>
                        Description
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>
                        +
                    </td>
                    <td>
                       ပေါင်းခြင်း 
                        let num1= 1, num2=2 :
                    </td>
                </tr>
                <tr>
                    <td>
                        -
                    </td>
                    <td>
                        နှုတ်ခြင်း
                    </td>
                </tr>
                <tr>
                    <td>
                        *
                    </td>
                    <td>
                        မြောက်ခြင်း
                    </td>
                </tr>
                <tr>
                    <td>
                        /
                    </td>
                    <td>
                        စားခြင်း
                    </td>
                </tr>
                <tr>
                    <td>
                        %
                    </td>
                    <td>
                      အကြွင်း
                    </td>
                </tr>
                <tr>
                    <td>
                        ++
                    </td>
                    <td>
                       တစ် တိုးပေး
                    </td>
                </tr>
                <tr>
                    <td>
                        --
                    </td>
                    <td>
                        တစ် လျော့ ပေး
                    </td>
                </tr>
            </tbody>
        </table>

### Exanple

    let x = 5, y = 10;

`let z = x + y;` // 15

`z = y - x;` // 5

`z = x * y;` //50

`z = y / x;` //2

`z = x % 2;` // 1

`let postInc = x ++ ;`// 
post-increment, x will be **5 here** and **6 in the next** line.

`let preInc = ++ x ;`// **7** (pre-increment)


`let postDec = y-- ;`// 
post-decrement, y will be **10 here** and **9 in the next** line

`let preDec = --y ;` // **8** (pre-decrement)
## 
###  Assignment Operators
<table border="0"><tbody><tr><th>Operator</th>
				<th>Name</th>
				<th>Example</th>
			</tr><tr><td><code>=</code></td>
				<td>Assignment operator</td>
				<td><code>a = 7; // 7</code></td>
			</tr><tr><td><code>+=</code></td>
				<td>Addition assignment</td>
				<td><code>a += 5; // a = a + 5</code></td>
			</tr><tr><td><code>-=</code></td>
				<td>Subtraction Assignment</td>
				<td><code>a -= 2; // a = a - 2</code></td>
			</tr><tr><td><code>*=</code></td>
				<td>Multiplication Assignment</td>
				<td><code>a *= 3; // a = a * 3</code></td>
			</tr><tr><td><code>/=</code></td>
				<td>Division Assignment</td>
				<td><code>a /= 2; // a = a / 2</code></td>
			</tr><tr><td><code>%=</code></td>
				<td>Remainder Assignment</td>
				<td><code>a %= 2; // a = a % 2</code></td>
			</tr><tr><td><code>**=</code></td>
				<td>Exponentiation Assignment</td>
				<td><code>a **= 2; // a = a**2</code></td>
			</tr></tbody></table>

## 
### Comparison Operators 
နှိုင်းယှဥ်ခြင်း (မှန်ရင် true / မှားရင် false ) return ပြန်ပေးသည်။
<table border="0"><tbody><tr><th>Operator</th>
				<th>Description</th>
				<th>code</th>
			</tr><tr><td><code>==</code></td>
				<td><strong>Equal to</strong>: x နဲ့ y တူသလား</td>
				<td><code>x == y</code></td>
			</tr><tr><td><code>!=</code></td>
				<td><strong>Not equal to</strong>:  x နဲ့ y မတူဘူးလား</td>
				<td><code>x != y</code></td>
			</tr><tr><td><code>===</code></td>
				<td><strong>Strict equal to</strong>:  x နဲ့ y ထပ်တူညီသလား</td>
				<td><code>x === y</code></td>
			</tr><tr><td><code>!==</code></td>
				<td><strong>Strict not equal to</strong>: x နဲ့ y လုံး၀ထပ်တူ မညီဘူး။</td>
				<td><code>x !== y</code></td>
			</tr><tr><td><code>&gt;</code></td>
				<td><strong>Greater than</strong>: x က y ထပ် ကြီးသလား။</td>
				<td><code>x &gt; y</code></td>
			</tr><tr><td><code>&gt;=</code></td>
				<td><strong>Greater than or equal to</strong>: x က y ထပ် ကြီးရင် ကြီး ၊ မကြီးရင် တူတယ်။</td>
				<td><code>x &gt;= y</code></td>
			</tr><tr><td><code>&lt;</code></td>
				<td><strong>Less than</strong>:  x က y ထပ် ငယ်သလား။</td>
				<td><code>x &lt; y</code></td>
			</tr><tr><td><code>&lt;=</code></td>
				<td><strong>Less than or equal to</strong>:x က y ထပ် ငယ်ရင် ငယ် ၊ မ ငယ် ရင် တူတယ်။</td>
				<td><code>x &lt;= y</code></td>
			</tr></tbody></table>

## 
### Logical Operators
<table border="0"><tbody><tr><th>Operator</th>
				<th>Description</th>
				<th>Example</th>
			</tr><tr><td><code>&amp;&amp;</code></td>
				<td><strong>Logical AND</strong>: နှစ်ဖက်လုံးမှန်ရင် true ။<br>တစ်ဖက်ပဲမှန် (သို့) နှစ်ဖက်လုံးမှားရင် false</td>
				<td><code>x &amp;&amp; y</code></td>
			</tr><tr><td><code>||</code></td>
				<td><strong>Logical OR</strong>: နှစ်ဖက်လုံးမှန် (သို့) တစ်ဖက်ပဲမှန် true ။ <br> နှစ်ဖက်လုံးမှား false</td>
				<td><code>x || y</code></td>
			</tr><tr><td><code>!</code></td>
				<td><strong>Logical NOT</strong>:  ပြောင်းပြန်စစ်ပေးတာပါ
				<br> !( 1 === 1 )  flase 
				<br> ! ( 1 === 2 ) true</td>
				<td><code>!( x = y)</code></td>
			</tr></tbody></table>

## 
###  CONDITIONALS 
`if`  တစ်ကယ်လို့ <br>
 `else if` ဒါမှမဟုတ် တကယ်လို့ <br>
  `else` ဒါမှမဟုတ်<br>

    if ( condition true) {
     run this code
    }
    ##example 1
    const num1 = 5 ;
    if ( num1 > 3 ) {
    console.log (" I'm running first")
    }
    // I'm running first
    
    တကယ်လို့ (num1 ရဲ့ တန်ဖိုးက 3 ထပ်ကြီးခဲ့ရင်) {
    (" I'm running first") ကို log လုပ် ပေးပါ။
    }
    // I'm running first
##
### example 2
   
    const num4 = 7 ;
    if (num4 === 8) {
    console.log ("first log")
    } else if (num4 > 9 ) {
    console.log ("second log")
    }else{
    console.log ("third log")
    }
    // third log

##
### `swich` Statement

    swich ( case ) {
    
    case 1 : 
     run this code ;
     break;
    
    case 2 : 
     run this code ;
     break;
    
    default : 
     run this code;
    }

example 2

    swich ( "cat" ) {
        
        case "cat" : 
         console.log ( " I'm a Cat");
         break;
        
        case "dog" : 
          console.log ( " I'm a Dog");
         break;
        
        default : 
         console.log ( " I'm a human");
        }
        // I'm a Cat

example 3

    swich ( "dog" ) {
        
        case "cat" : 
         console.log ( " I'm a Cat");
         break;
        
        case "dog" : 
          console.log ( " I'm a Dog")
         break;
        
        default : 
         console.log ( " I'm a human");
        }
        // I'm a dog
example 4

    swich ("animal") {
        
        case "cat" : 
         console.log ( " I'm a Cat");
         break;
        
        case "dog" : 
          console.log ( " I'm a Dog");
         break;
        
        default : 
         console.log ( " I'm a Human");
        }
        // I'm a Human
##
### Important Note

 - Javascript ကကြိုတင်သတ်မှတ်အသုံးပြုထာသည့် keyword များကို 
   variable name (or) function name အဖြစ် သုံးစွဲခွင့်မရှိပါ။
  - `swich` Statement ကို `if` ,`else if` စတာတွေ အများကြီး သုံးရချိန်တွင် အစားထိုးသုံးလေ့ရှိသည်။ `swich` ကို ရေးသားရာတွင် case တစ်ခု check တိုင်း `break` ကို ထည့်ရေးပေးရန် အရေးကြီးပါသည်။ `swich` တွင် သုံး သော 
**expression** နှင့် **case value** တို့သည် ***case-sensitive*** ဖြစ်သောကြောင့် **အတိအကျ ထပ်တူညီမှသာ** အလုပ်လုပ်နိုင်မည်။
  
