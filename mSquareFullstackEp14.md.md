﻿## MSquare Programing Fullstack Course
### Episode-*7* Summary

ဒီနေ့သင်တန်းမှာတော့ 
 - ‌git branch
 - git reset
 - git merge<br>
 စတာတွေ အကြောင်း လေ့လာသွားပါမယ်။
 ##
 ### Git branch
 branch ဆိုတာက အကိုင်းအခက်ကို ပြောတာပါ။<br>
 git မှာ အကိုင်းတစ်ခု ကို git branch လို့ ခေါ်ပါတယ်။
 ကိုယ်က ဘယ် branch ထဲ ရောက်နေလဲ သိချင်ရင် git branch command  ကို သုံးရပါတယ်။
 > Example

 ep14  ဆိုတဲ့ folder  ထဲမှာ git init လုပ်ထားပြီး index.html fileတစ်ခု လုပ်ကာ code တစ်ချို့ ရေးထားပါတယ်။<br>
 အ့တာတွေကို git add/ git commit လုပ်ပြီး commit တစ်ခု မှတ်တမ်းတင်ထားပါတယ်။<br>
 git branch လို့ ရိုက်ထည့်လိုက်တဲ့အခါမှာတော့ လက်ရှိရောက်နေတဲ့ branch အမည်ကို အစိမ်းရောင်( * )အမှတ်အသားနဲ့ ပြပေးနေပါတယ်။
<br>
git log ထုတ်ကြည့်လိုက်ရင်လဲ HEAD -> masterဆိုပြီး ပြပေးပါတယ်။ ပုံအရ ကြည့်လိုက်ရင် ခု လက်ရှိ master branch ထဲ ရောက်နေတာပါ။<br>
<br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-1.jpg?raw=true)

##
### git switch
git branch တစ်ခု ကနေ နောက်တစ်ခြား branch တစ်ခုကို သွားချင်ရင် `git switch branch-name` ကို သုံးပါတယ်။<br>
ခု ကျနော်တို့မှာက branch တစ်ခုပဲရှိတဲ့ အတွက် နောက်ထပ် branch တစ်ခု ပြုလုပ်ပြီးမှ လက်ရှိ branch ကနေ သွားလို့ရမှာပါ။<br>
ဒါကြောင့်မလို့ ကျနော်တို့က `git switch -c new-branch-name` ကို သုံးရပါမယ်။ဒီ command က **ပေးလိုက်တဲ့ နာမည်နဲ့ branch အသစ်တစ်ခု လုပ်**ပေးပြီး ၊ ထို **အသစ်လုပ်တဲ့ branch ထဲ တစ်ခါထဲ ၀င်ရောက်ပေးသွားမှာ** ဖြစ်ပါတယ်။<br>
ဒါ့အပြင် **လက်ရှိ branch က commit history တွေကို အကုန်ကူးယူပြီး အသစ်လုပ်တဲ့ branch ထဲ သွားထည့်ပေး**သွားမှာပါ။<br><br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-2.jpg?raw=true)
<br>
- (1) git switch -c feat/tab <br>
feat/tab ဆိုတဲ့ branch အသစ်လုပ်လိုက်ပြီး ထို branch ထဲ ၀င်လိုက်တာပါ။
- (2) Switched to a new branch 'feat/tab' <br>
main branch ကနေ feat/tab ဆိုတဲ့ branch အသစ်ကို ရောက်သွားပြီးလို့ ပြပေးနေတာပါ။
- (3) git branch ကို ခေါ်ကြည့်လိုက်တဲ့အခါ လက်ရှိရောက်နေတဲ့ branch က feat/tab ဖြစ်ကြောင်းကို အစိမ်းရောင် * အမှတ်အသား နဲ့  ပြပေးပါတယ်။
- (4) git log လုပ်ကြည့်တဲ့အခါမှာ feat/tab ဆိုတဲ့ branch ထဲမှာ master branch ထဲက commit လုပ်ထားတာတွေ တစ်ခါတည်းပါလာတာ တွေ့ရမှာပါ။<br>
**HEAD -> feat/tab, master** လို့ပြထားတာက လက်ရှိ feat/tab branch ထဲ ရောက်နေပြီး **`bf30faa` ID နဲ့ commit က feat/tab မှာရော master branch မှာပါ ရှိနေတဲ့ commit** တစ်ခုဖြစ်တဲ့ အကြောင်းပါ။
> feat/tab branch က သီးသန့် branch တစ်ခု ဖြစ်သွားတဲ့ အတွက် ဒီ branch မှာ လုပ်သမျှ changes တွေ commit တွေက master branch နဲ့ သက်ဆိုင်ခြင်းမရှိပဲ 
> master branch မှာ switch စလုပ်ထားတဲ့ အခြေအနေအတိုင်းပဲ ရှိနေမှာပါ။
##
### git commit များကို ထိန်းချုပ်ခြင်း
track လုပ်ထားပြီးသော commitများကို git add လုပ်စရာမလိုပဲ တစ်ခါထည်း commit လုပ်လိုက်လို့ရပါတယ်
> example

ကျနော်တို့ index.html ဖိုင်ထဲမှာ h1 tag နဲ့ welcome to yangon လို့ ရေးထည့်ပြီး save  ကာ commit အသစ်တစ်ခုသိမ်းမယ်ဆိုရင် git add bla bla...လုပ်စရာ မလိုတော့ပဲ  `git commit -am "added welcome h1 tag"` ဆိုပြီး တန်းသိမ်း(commit)လိုက်လို့ရပါတယ်။git log ခေါ်ကြည့်တဲ့ အခါ commit 2 ခု ကို တွေ့ရမှာပါ။<br>
<br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-3.jpg?raw=true)
- ခု လက်ရှိ `feat/tab` branch ထဲမှာ commit လုပ်လိုက်တာမို့လို့ `master` branch မှာ သက်ရောက်မှု မရှိပဲ git switch စလုပ်ကာစ အနေအထားတိုင်းပဲ commit တစ်ခုပဲ ရှိတာ သတိပြုပါ။<br><br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-4.jpg?raw=true)

### git reset
git commit တွေကို ဖျက်ချင်/ ပြင်ချင် ရင် သုံးပါတယ်။
### git reset --hard commit-ID
ဒါကတော့ ထည့်ပေးလိုက်တဲ့ commit-ID နောက်က commit  မှတ်တမ်းတွေကို ဖျက်ထုတ်လိုက်တာပါ။<br><br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-5.jpg?raw=true)

 1. p tag တစ်ခု လုပ်ပြီး commit လုပ်လိုက်ပါတယ်
 2. လက်ရှိ commit 3 ခု ဖြစ်သွားပါပြီး။
 3. `git reset --hard 7c3874f` လို့ လုပ်လိုက်ချိန်မှာတော့ ID 7c3874f ရှိတဲ့ commit **နောက်က မှတ်တမ်းတွေအားလုံးကို ဖျက်လိုက်ပြီး** အသစ်ထည့်လိုက်တဲ့ p tag ကိုပါ ဖျက်ပေးလိုက်တာကို တွေ့ရမှာပါ။ ထပ်ရှင်းပြရရင် **ID 7c3874f  ရှိတဲ့ commit** ကို **git commit လုပ်တုန်းက အနေအထားအတိုင်း** file တွေကို ပြန်ထားပေးလိုက်တာပါ။
### git reset --soft commit-ID
 ထည့်ပေးလိုက်တဲ့ commit ကို staging area(သိမ်းရန် အသင့်ဖြစ်သောအဆင့်)သို့ ပြန်ပို့ထားပေးတာပါ။
 ### git reset --mixed commit-ID
  ထည့်ပေးလိုက်တဲ့ commit ကို working tree (အလုပ်လုပ်နေသောနေရာ working dir)သို့ ပြန်ပို့ထားပေးတာပါ။
  ### git reset commit-ID
  git reset --mixed commit-ID ကဲ့သို့ပဲ   ထည့်ပေးလိုက်တဲ့ commit ကို working tree  (အလုပ်လုပ်နေသောနေရာ working dir)သို့ ပြန်ပို့ထားပေးတာပါ။
  ### git checkout commit-ID
  သိမ်းထားတဲ့ commit တွေကို ဘာမှ သက်ရောက်မှု မရှိစေပဲ ကြည့်ချင်တဲ့ commit ကို သွားကြည့်ဖို့အတွက် သုံးပါတယ်။ git checkout ကို အသုံးပြုပုံ ရှုပ်ထွေးတဲ့အတွက် လက်တွေ့မှာတော့ သိပ်အသုံးပြုလေ့မရှိကြပါဘူး။
  ##
  ### git merge
  branch တွေကို ပေါင်းဖို့အတွက် သုံးပါတယ်။
  #### `git merge branch-name` လို့ ရေးပေးရပါတယ်။<br>
  ![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-6.jpg?raw=true)
  
 1. **`git switch master`**
 `master branch` မှာ `feat/tab branch` ကို သွားပေါင်းထည့်ဖို့အတွက် **လက်ရှိ  `feat/tab branch` ကနေ `master branch` ကို သွား**လိုက်တာပါ။<br>
2. **`git log --oneline`**
 `master branc`h မှာ ရှိတဲ့ commit တွေကို ကြည့်တာပါ။
လက်ရှိမှာတော့ master branch မှာ **commit တစ်ခုသာ** ရှိတာကို မြင်ရမှာပါ။
3. **`git merge feat/tab`**
`master branch` မှာ `feat/tab branch` ကို **ပေါင်းထည့်လိုက်တာပါ**
4. **`git log --oneline`**
 `master branch` မှာ ရှိတဲ့ commit တွေကို ထပ်ကြည့်တာပါ။
လက်ရှိမှာတော့  `master branch`မှာ **commit နှစ်ခုမြင်ရမှာပါ။**
ဘာလို့လဲဆိုတော့ **`master branch` မှာ `feat/tab branch` ကို လာပေါင်းထည့်လိုက်တဲ့အတွက် `feat/tab branch` က commit မှတ်တမ်းတွေပါ ပေါင်းထည့်ပေးလိုက်လို့ ဖြစ်ပါတယ်**။
## 
### merge conflict
branch  နှစ်ခု ပေါင်းတဲ့(merge) အခါ တစ်ခုက commit history ဟာ နောက် merge လုပ်မယ့် branch က commit history နဲ့ ကိုက်ညီမှု ရှိရပါမယ်။ <br>
merge လုပ်မယ့် branch က commit history ဟာ
နောက်merge လုပ်မယ့် branch က commit historyထဲ ပါရမယ့်သဘောပါ။ <br>
အထက်ပါအတိုင်း ကိုက်ညီမှု မရှိခဲ့ရင် conflict ရှုပ်ထွေးမှု ပြဿနာ ဖြစ်ပေါ်လာတက်ပါတယ်။ အောက်က exampleကို လေ့လာကြည့်ရအောင်
>Example

![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-7.jpg?raw=true)
<br><br>
ပုံပါ အတိုင်း branch နှစ်ခုမှာ မတူညီတဲ့ commit တစ်ခုစီ မှတ်တမ်းတင်ထားပါတယ်။
git merge လုပ်လိုက်တဲ့ အခါမှာတော့ အောက်ကပုံအတိုင်း conflict ပြဿနာ  ဖြစ်လာပါပြီး။<br><br>
![enter image description here](https://github.com/Aungtat/MSquareFullstackCourseSummary/blob/main/git2-9.jpg?raw=true)
<br><br>
merge conflict ဖြစ်လာပြီးဆိုရင်တော့ မြားပြထားတဲ့နေရာမှာ
လိုချင်တဲ့အတိုင်း ရွေးချယ်ကာ branch တွေကို merge  လုပ်ပေးရမှာ ဖြစ်ပါတယ်။
##
>Important Note!

 - branch အသစ်လုပ်တဲ့အခါ branch name ကို (feature) feat/nameဆိုပြီး ပေးလေ့ရှိကြပါတယ်။
 - branch name ကို **rename** ပြန်လုပ်ချင်ပါက `git branch -m new-name` ကို အသုံးပြုနိုင်ပါတယ်
 - git init လုပ်တဲ့အခါ မိမိအသုံးပြုတဲ့ project folderထဲ မှာ တစ်ကြိမ်သာ ပြုလုပ်သင့်တယ်။တခြားနေရာ(Desktop..etc..)မှာ git init လုပ်လိုက်မိရင် မလိုလားအပ်တဲ့ ပြဿနာတွေကြုံတွေ့ရနိုင်ပါတယ်။
 - ဒီ အကျဥ်းချုပ်ကို ဖတ်ပြီးလို့ git ကို သေချာနားမလည်ဖြစ်နေပါက  [git အသေးစိတ် ကြည့်ရန်](https://www.youtube.com/watch?v=CYY7bAQEmmc&list=PLmQKoPepuLJ9TtiSLQTbQ2MWqU3J-QO1G)
မှာ ဆရာကိုယ်တိုင် အသေးစိတ်ရှင်းပြထားတာကို လေ့လာနိုင်ပါတယ်။
 <br>

