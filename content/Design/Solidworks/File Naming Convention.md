---
tags:
  - Solidworks
  - CAD
---
# Rules

- When you create a part or assembly, immediately save it, following the naming convention and putting it in the correct folder to avoid complications and issues later on
- Convention: ”<span style="color:red">###</span>-<span style="color:orange">__</span>-<span style="color:yellow">###</span>-<span style="color:lime">##</span> <span style="color:cyan">[Insert Descriptive Name]</span>”
- The <span style="color:red">first 3 digits</span> indicate the assembly (top-level, sub-assembly, sub-sub-assembly)
- The <span style="color:orange">next character</span> indicates the file type (P for Part, A for Assembly, L for Layout, D for Drawing)
- The <span style="color:yellow">next 3 digits</span> indicate a unique part number (so the first part made for that assembly is 001)
- The <span style="color:lime">last 2 digits</span> indicate the configuration of a part, since it is the same file but a different physical part (if there is no configuration, it is left as 00)
- The <span style="color:cyan">Descriptive Name</span> should concisely indicate the purpose of the part. Keep it professional, we send some parts out to sponsors!
# Example: Lexan arm on the Charlie’s cargo intake

Theoretical breakdown:
- “<span style="color:red">000</span>-A-000-00 Charlie” is the full robot
- “<span style="color:red">200</span>-A-000-00 Elevator” is the top assembly
	- Assuming "<span style="color:red">100</span>-A-000-00" is already taken
- “<span style="color:red">230</span>-A-000-00 Cargo Intake” is the sub-assembly
	- Assuming "<span style="color:red">210</span>-A-000-00" and "<span style="color:red">220</span>-A-000-00" are already taken
	- The cargo intake is not in a further sub assembly, so the third digit is 0
- "230-<span style="color:orange">L</span>-<span style="color:yellow">000</span>-00 Cargo Intake Layout Sketch" is the layout sketch for the assembly
- “230-<span style="color:orange">P</span>-<span style="color:yellow">001</span>-00 Cargo Intake Arm” is the first part, with no configurations
- "230-<span style="color:orange">D</span>-<span style="color:yellow">001</span>-00 Cargo Intake Arm" is the drawing of the same part
- "230-P-001-<span style="color:lime">01</span> Cargo Intake Arm" is the first configuration of the same part
	- This is not the name of the file - you would have configurations numbered accordingly in your part, then you can refer to the configuration number when you're communicating with someone

![](https://lh6.googleusercontent.com/N9IwBsTdyLTFGuZ5FYNGl9DMnsqTMtU8Q73mQxQfIv4xWtO8Bbs24kfesgESeqiXkzxVDa2RPNo_tixIudjvaIOdxfnwp1HmPba_8La_spKooOUOX-RDyC8ihd19OeNYJz4GuoVd4opjSWCtl1cFjQ)
