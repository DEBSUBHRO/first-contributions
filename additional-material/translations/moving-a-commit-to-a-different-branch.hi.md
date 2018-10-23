# एक कमिट शाखा को एक अलग शाखा में ले जाना
क्या होगा यदि आप कोई बदलाव कमिट करते हैं, और फिर महसूस करें कि आप एक अलग शाखा में आए हैं?
आप इसे कैसे बदल सकते हैं? यह ट्यूटोरियल कवर करता है।
<!-- What to do if you posted a commit but later realize that it is in another branch? This tutorial will help you out.>

## सबसे मौजूदा काम को मौजूदा शाखा में ले जाना 
<!-- The most important work is to take it to the master branch-->

ऐसा करने के लिए, टाइप करें: 
<!-- To do this, type:-->

``` git reset HEAD~ --soft ```- अंतिम कमिट को पूर्ववत करता है, लेकिन उपलब्ध परिवर्तनों को छोड़ दें। 
<!-- ``` git reset HEAD~ --soft ``` The last commit is changed while the others remain unchanged.-->
``` git stash ```- निर्देशिका की स्थिति रिकॉर्ड करता है। 
<!-- ``` git stash ```Records the location of the user-->

``` git checkout name-of-the-correct-branch ``` - दूसरी शाखा में स्विच करता है। 
<!--``` git checkout name-of-the-correct-branch ``` Switches to the other branch-->
``` git stash pop ``` - आखिरी स्टेशेड स्टेटस को हटा देता है। 
<!-- ``` git stash pop ```The last status is updated-->
``` git add ``` - या अलग-अलग फाइलों को एक साथ स्टेज करने का प्रयास करें।
<!-- ``` git add ``` Different files are stacked together-->
``` git commit -m "आपका संदेश यहां" ``` - परिवर्तनों को सुरक्षित कर देता है और कमिट करता है।
<!-- ``` git commit -m ``` Updates the changes and keep it secured-->

अब आपके परिवर्तन सही शाखा पर हैं
<!-- Now your changes are made on the desired branch>

### सबसे पुराना काम एक नई शाखा में ले जाना
<!-- To bring bring an old commit to a new branch>

ऐसा करने के लिए, टाइप करें:
<!-- To do this, type:-->
``` git branch newbranch```- एक नई शाखा बनाता है। सभी कमिट को सुरक्षित कर देता है।
<!-- ``` git branch newbranch``` Creates a new branch and stores the commit-->
``` git reset --hard HEAD~#``` - मास्टर को वापस #कमिट में ले जाएं। याद रखें, यह काम मास्टर से जा चूका होगा
<!-- git reset --hard HEAD~#``` Resets the master  branch-->
``` git checkout newbranch``` - आपके द्वारा बनाई गई शाखा में जाता है। इसमें सभी कमिट होंगे।
<!-- git checkout newbranch``` Enters the new_branch where all your commits are securely stored>

याद रखें: कोई भी बदलाव कमिट नहीं किया गया तो खो जाएगा।
<!-- please remember that not saving changes in a commit will make the commit remain unchanged-->
