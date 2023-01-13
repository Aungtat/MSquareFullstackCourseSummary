## MSquare Programing Fullstack Course
#### Episode-11 Summary
ဒီနေ့သင်တန်းမှာတော့

**Git** အကြောင်း လေ့လာသွားမှာပါ။

## 
### what is Git ?..
Git ဆိုတာ version control system တစ်ခုပါ။
Project တစ်ခုမှာ ပြောင်းလဲပြင်ဆင်ချက်၊ ထပ်မံဖြည့်စွက်ချက်တွေကို မှတ်တမ်းတင်သိမ်းဆည်းပေးထာပြီး ဘယ်အချိန်မှာ ဘာတွေ ပြုလုပ်ထားသလဲဆိုတာကို ပြန်လည် ကြည့်ရှု ရယူနိုင်တဲ့ စနစ် တစ်မျိုး ဖြစ်ပါတယ်။
##
### Git ကို စတင်အသုံးပြုခြင်း
Git ကို ကွန်ပြူတာထဲ install လုပ်ပေးထားပါ။
VS code မှာ project folder ကို ဖွင့်ပါ။
new terminal ( ctrl + ` )ကို ဖွင့်ပါ။
terminal ထဲ **git init** ကို ရေးပြီး enter ခေါက်ပါ။<br>
![enter image description here](https://static.javatpoint.com/tutorial/git/images/git-init.png)
> project folder ထဲ git ရှိ မရှိ သိချင်ရင် 
- vs code မှာ `ctrl` + `,` ကို နှိပ်ပါ
- search bar မှာ  exclude လို့ ရိုက်ရှာပါ.
- file exclude အောက်က **/.git ဆိုတာကို ဖျက်ပေးလိုက်ပါ။
- project ထဲ git file တွေကို ပြပေးမှာပါ။
- git file  များကို ပြုပြင်ခြင်း၊ ဖျက်ခြင်းများ မပြုလုပ်သင့်ပါ။
- git file  များကို ပြန်ဖွက်ထားချင်ပါက file exclude အောက်မှာ ` ADD patern` > `**/.git`  ဆိုတာလေးပြန်ထည့်ပေးပါ။
##
### git `commit` (လုပ်ဆောင်ချက်များ မှတ်တမ်းတင်သိမ်းဆည်းခြင်း)

Project တစ်ခုမှာ ပြောင်းလဲပြင်ဆင်ချက်၊ ထပ်မံဖြည့်စွက်ချက်တွေကို မှတ်တမ်းတင်သိမ်းဆည်းမယ်ဆိုရင် 
- working Dir (လက်ရှိအလုပ်လုပ်နေသောအဆင့်)
- staging area(သိမ်းရန်အဆင့်သင့်ဖြစ်သောအဆင့်)
- git repository (သိမ်းလိုက်ပြီး ဖြစ်သော အဆင့်)
ဆိုပြီး ရှိပါတယ်။ <br>
လက်ရှိ ဘယ် အဆင့်ရောက်နေလဲ သိချင်ရင် git status ဆိုတဲ့ command ကို သုံးရပါတယ်။
>EXAMPLE

<BR>
Project folder ထဲ FILE တစ်ခု အသစ်လုပ်ကြည့်ပါ။
ပြီးရင် git status လုပ်ကြည့်ပါ။<br><br>
    ## 
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git1.jpg?raw=true)
- Untracked file ဆိုတာက git က မိမိပြောင်းလဲလုပ်ဆောင်ချက်တွေ ကို တွေ့သော်လည်း အလုပ်လုပ်နေဆဲ အဆင့်မှာပဲ ရှိနေသေးပြီး သိမ်းရန် အသင့်မဖြစ်သေးကြောင်း အနီရောင်နဲ့ ပြနေတာပါ။
- သိမ်းရန်အဆင်သင့်ဖြစ်ကြောင်း **`git add` (file-name)** command ကို ရေးပေးရပါတယ်။

    git add index.html 

    git status
    <br>
    <br>![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2.jpg?raw=true)

- Changes to be committed: ဆိုတာက သိမ်းရန်အသင့်ဖြစ်တဲ့ အဆင့်ကို ရောက်နေကြောင်း ပြောတာပါ။
- အောက်မှာလဲ သိမ်းမယ့် ဖိုင်ကို အစိမ်းရောင် နဲ့ ပြပေးထားပါတယ်။
-  မိမိပြောင်းလဲလုပ်ဆောင်ချက်တွေ ကို သိမ်းမယ်ဆိုရင် `git` `commit` `-m` `"message"` ကို ရေးပေးရပါမယ်။ message မှာ ကိုယ်ရေးချင်တာရေးလို့ပါတယ်။ 
- ပြီးရင် `git log` command နဲ့ git မှာ မိမိလုပ်ဆောင်ချက်ကို ပြန်စစ်လို့ရပါတယ်.
- (1)  `git commit -m "Start New commit"`
- (2)  `git log`
- (3) သိမ်းလိုက်တဲ့ commit ကို ပြပေးထားတာပါ<br>
    <br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git3.jpg?raw=true)
- ဒီအချိန်မှာ git status ကို ပြန်ခေါ်ကြည့်မယ်ဆိုရင် **nothing to commit, working tree clean**(သိမ်းဆည်းရန် ပြုပြင်ပြောင်းလဲချက်မရှိပါ) လို့ ပြနေပါမယ်။ဘာလို့လဲဆိုတော့ ကျနော်တို့ ကပြုပြင်ပြောင်းလဲချက်ကို commit လုပ်ထားပြီးသားမလို့ပါ။
##
> Important Note!

- ဖိုင် တစ်ခုထပ်ပိုထည့်ချင်ရင် git add file-name အစား `git` `add` `.` ကို အသုံးပြုခြင်းဖြင့် ဖိုင်အားလုံးကို သိမ်းရန် အဆင်သင့်အဆင့်(staging area)ကို ပို့ပေးပါတယ်။
- staging area မှ working Dir (လက်ရှိအလုပ်လုပ်နေသောအဆင့်) သို့ ပြန်သွားချင်ရင် `git restore --staged file-name` command ကို အသုံးပြုနိုင်ပါတယ်။
- git commit မှတ်တမ်းများကို အတိုကောက်ပြစေချင်ရင် `git log --oneline` ကို သုံးနိုင်ပါတယ်။
- git username နဲ့ email ကို ပြောင်းလဲချင်ရင် <br>
git config --global user.name "new-name"<br>
git config --global user.eamil "new-eamil"<br>
ကို သုံးနိုင်ပါတယ်။

