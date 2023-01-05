## MSquare Programing Fullstack Course
### Episode-8 Summary
##
ဒီနေ့ သင်တန်းမှာတော့ <br>

 - Call back function
 - .map() method
 - .filter() method 
 <br> စတာတွေလေ့လာသွားကြမှာပါ။
 ##
 ### Callback function
 Function တစ်ခုထဲ နောက် function တစ်ခုကို parameter အဖြစ် ထည့်ပေးလိုက်ရင် ထို အထည့်ခံ function ကို callback function လို့ ခေါ် ပါတယ်။<br>
 **ပထမ function အလုပ်လုပ်ပြီးမှ နောက် functionတစ်ခုကို အလုပ်ခိုင်းချင်တဲ့အခါ callback အနေနဲ့ သုံးလေ့ရှိပါတယ်။**
 
 #### Example..1
 

    const functionOne = (parameter) => {
     console.log("I am not callback");
     parameter();
     };
     
     const functionTwo = ()=>{
      console.log("I am callback");
      };
       functionOne(functionTwo);
      //functionOneအရင်လုပ်ပါ(functionOneပြီးမှ functionTwoနောက်ကလုပ်ပါ=callback)
      
      //output 1: I am not callback
      //output 2: I am callback
#### Example..2

    const functionOne = (parameter)=> { 
       console.log("I am not callback");
       parameter(1,2); 
       }; 
     const functionTwo = (a,b)=>{ 
        console.log(a+b); 
       }; 
       functionOne(functionTwo);
       //output 1: "I am not callback"
       //output 2: 3

##

 - **callback function  ခေါ်** တဲ့ အခါ  သိမ်းထားတဲ့ **variable name ကိုသာ ရေး**ပေးရမည်။<br>
 `functionOne(functionTwo)` **YES**<br>
 `functionOne(functionTwo())`**NO**
##
### array.map() method
**မူရင်း array ရှိ item များ အားလုံးကို loopလုပ်**ပေးပြီး **array အသစ်တစ်ခု** ထုတ်ပေးသည်။<br>**မူရင်း array ရှိ item များ အားလုံး ပြောင်းလဲခြင်းမရှိပါ**
#### Syntax
`array`.`map`(`callback-function`) ;<br>

`array`.`map`((`parameter`)`=>` `{`
do something
`}` 
`)` ;<br>
#### short-hand
`array`.`map`((`parameter`)`=> `do something`) `;<br>
#### Example..1

    const itemsArr = [1,2,3,4,5];
    const newArr =itemsArray.map((element) => element + 1);
      console.log(newArr);
      //output : (5) [2, 3, 4, 5, 6]
      //auto return in short-hand syntax
#### Example..2

    const itemsArr = [1,2,3,4,5];
    const newArr = itemsArr.map((element) =>{
     const newItem = element+1;
     return newItem;
     });
     console.log(newArr);
     //(5) [2, 3, 4, 5, 6]
     
     //if no return
     const newArr = itemsArr.map((element) =>{
     const newItem = element+1;
     });
     console.log(newArr)
     //(5) [undefined,undefined,undefined,undefined,undefined]
     
 ##
 ### array.filter() method
 မူရင်းarray ရှိ item များကို loop လုပ်ကာ **သတ်မှတ်ချက်နှင့်အညီ စစ်ဆေးပြီး မှန်ကန်မှုရှိတဲ့( true) item များကိုသာ ‌**ရွေးချယ်ပြီး **array  အသစ်တစ်ခု** ပြန်ထုတ်ပေးသည်။<br>**မူရင်း array ရှိ item များ အားလုံး ပြောင်းလဲခြင်းမရှိပါ**
 #### syntax
 `array`.`filter`(`callback function`);

```
const  arryItem = [
{
 name :  "Aung AUng",
 age :  34
},
{
 name :  "Ko Ko",
 age :  24
},
{
 name :  "Su Su",
 age :  "18"
},
{
 name :  "Bo Bo",
 age :  23
},
{
 name :  "Mg Mg",
 age :  26
}
];

const  youngPeople = arryItem.filter((user)=> {
 return  user.age < 25;
 //အသက် ၂၅ အောက်ကိုသာ ‌စစ်ထုတ်ပေးပါ
 });

console.log(youngPeople);

// (3) [{…}, {…}, {…}]
// 0: {name: 'Ko Ko', age: 24}
// 1: {name: 'Su Su', age: '18'}
// 2: {name: 'Bo Bo', age: 23}
```

အပေါ် က filter method ထဲက လို ၂၅ အောက်တွေကိုပဲ စစ်ထုတ်ပြီး သူတို့ နာမည်ပဲ လိုချင်တယ် ဆိုပါစို့။
```
const  arryItem = [
{
 name :  "Aung AUng",
 age :  34
},
{
 name :  "Ko Ko",
 age :  24
},
{
 name :  "Su Su",
 age :  "18"
},
{
 name :  "Bo Bo",
 age :  23
},
{
 name :  "Mg Mg",
 age :  26
}
];
//filter people under 25
 const  youngPeople = arryItem.filter((user)=>user.age < 25);

//get name of under 25
 const getName = youngPeople.map((people,index) =>people.name);
 console.log(getName);
//(3) ['Ko Ko', 'Su Su', 'Bo Bo']


```

```
 `array.map((element, index) => run this);` <br>
map() method မှာ **callback function** က **parameter နှစ်ခု** လက်ခံရင် <br>**ပထမ parameter** က **element** ကို ခေါ် မှာ ဖြစ်ပြီး <br>**ဒုတိယ parameter**က ထို **element ရဲ့ index** တန်ဖိုး ဖြစ်ပါတယ်။ <br>နမူနာ ပြထားတဲ့ code မှာတော့ <br>`youngPeople.map((people,index) =>people.name);` <br>index ကို parameter အဖြစ်သာ ထည့်ထားပြီး callback function မှာ ဘာလုပ်ဆောင်ချက်မှ မပေးထားပါဘူး။<br>
 ဒီလိုလေး စမ်းကြည့်ပါ
```
const getName = youngPeople.map((people,index) => index + " "+people.name);
 console.log(getName);     
 //output : (3) ['0 Ko Ko', '1 Su Su', '2 Bo Bo']
 ```
    
 **index နေရာမှာ တခြားစာလုံးဖြစ်လဲ index တန်ဖိုးကိုပဲ ထုတ်ပေးမှာပါ** 
```
youngPeople.map((people,spiderMan) => spiderMan+ " " + people.name); 
console.log(getName); 
//output : (3) ['0 Ko Ko', '1 Su Su', '2 Bo Bo']```
 

 
> Written with [StackEdit](https://stackedit.io/).
