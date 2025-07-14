---
tags:
  - Solidworks
  - CAD
---
# Topics
- New Part Templates
- Part Tracker Spreadsheet

# New Part Templates

If you're not familiar with what part templates are and why they're incredibly useful to us, read through the [Part Templates segment](https://wiki.wafflesrobotics.com/Blog/2023/12-December/10th-December-2023-(Sunday)#part-templates) of the December 10th blog.

![](https://i.imgur.com/JlDuhkf.png)

New are the Box Tubing and Plate templates with integrated part properties that show up in our BOMs.

- **Box Tubing** - Adjust sketch plane, tubing size, wall thickness, length
- **Plate** - Adjust plate thickness, , material, custom geometry

Do note that the sketches for both these part templates are undefined - this is intentional as it allows for students to fully define the sketch according to how the parts will be used, whether that be by defining geometry in the sketch or by referencing a layout sketch. Also note that if you want if you want to change the extrusion direction (vertical tubing, plate facing up, etc) you can do so by changing the sketch plane of the profile sketch.

![](https://i.imgur.com/MaNejwy.png)

EDIT: The plate template breaks every time you delete the 
# Part Tracker Spreadsheet

After briefing Gavin on some of the stuff we've been working on in terms of finding a good CAD workflow (layout sketches, part templates, configurable components), we looked a little into how to use BOMs (Bill of Materials) to our advantage. Specifically, we looked into how to export BOMs to a Google Sheet and into what details should be on a part tracker spreadsheet.

![](https://i.imgur.com/pYm9IMh.png)

The A-F columns above are exported directly from SolidWorks and already has all of the information required. The person making this sheet only has to manually input the "Spare Qty" and "Source" columns (Total Qty is automatically calculated).

Once the parts are in the sheet, students are responsible for keeping the "Next Step" and "Next Step Notes" columns updated as they work trough designing, fabricating and assembling each part.

The next step for this sheet would be to implement a system that can sort/filter parts by their subsystem, probably by the first digit of their part numbers. I'm not sure how to do that though, so I'll leave that to someone who's more familiar with spreadsheets.

\- Brandon