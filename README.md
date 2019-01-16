# pyrit-tutorial

الاوامر المستخدمة والشرح:

اولاً نقوم بتحليل الملف بالأمر التالي:
pyrit -r captured.cap analyze

<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/pyrit%20-r%20captured.cap%20analyze.png" height="30%" width="30%">
</p>

ثم نأخذ اسم الشبكة أو الـ SSID 

ثانياً نقوم بفصل ملف captured.cap إلى ملف أخر بالامر التالي:

pyrit -r captured.cap -o new_captured strip

<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/pyrit%20-r%20captured.cap%20-o%20handsake%20strip.png" height="30%" width="30%">
</p>

في هذا الأمر قمنا بفصل المعلومات المفيدة ووضعناها في ملف جديد 

ثالثاً نقوم بوسترات ملف كلمات مرور إلى قاعدة البيانات بالأمر:

pyrit -i /usr/share/wordlists/rockyou.txt import_passwords

<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/pyrit3.png" height="30%" width="30%">
</p>
ثم الأمر 
pyrit eval 
لمشاهدة كم عدد الباسورد

رابعاً اضافة الـ essid إلى قاعدة البيانات كي يتم التعرف عليه بالامر التالي:

pyrit -e Too_cl0se_to_th3_Sun create_essid

<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/pyrit%20create_essid.png" height="30%" width="30%">
</p>
<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/evel2.png" height="30%" width="30%">
</p>
خامساً نقوم بتجميع المعلومات في قاعدة البيانات بمعنى أنه يتم اضافة اسم الشبكة والملف الذي استخرجته من ملف captured.cap وملف الباسورد إلى قاعدة البيانات بالامر التالي:

pyrit batch 

image pyrit batch

سادساً نقوم بالهجوم على الشبكة بالامر التالي:

pyrit -r new_captured attack_db

<p align="center">
  <img src="https://github.com/Hackers-0f-sYr/pyrit-tutorial/blob/master/image/pyrit%20-r%20new_captured%20attack_db.png" height="30%" width="30%">
</p>
