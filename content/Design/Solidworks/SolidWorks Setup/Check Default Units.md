---
tags:
  - Solidworks
  - CAD
---
To check your default units, create a new part and check the lower right hand corner. If it says IPS, your default units are Inches, Pounds and Seconds which is perfect for our purposes (we generally design in imperial units). If it says MMGS, it's best to change the default so you don't finish designing the coolest part anyone's ever seen just to realize your part is 25.4 times too small. 

To change your part's default units:
1. Create a new part and leave it blank
2. Set the units to IPS by clicking "MMGS" in the lower right corner, then selecting IPS
3. Click File -> Save As
4. Change the name to "Part", and the Save As Type to "Part Templates (\*.prtdot)"
6. Make sure you're saving in a folder named templates, then save the part template to overwrite the old one
7. Close the part

![](https://i.imgur.com/l8q91Pt.png)

Now, when you create a new part, it should go straight to IPS units. Repeat the above steps for assemblies by creating a new blank assembly, changing your units, and saving it as "Assembly.asmdot" in the same templates folder.