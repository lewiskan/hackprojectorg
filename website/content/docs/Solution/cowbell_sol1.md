---
title: Modern Cowbell - Solution (rural Nepal)
---
**Proposed by** Pravin Raj Joshi

### Solution
### Material used
radBeacon -- http://www.amazon.com/Radius-Networks-RadBeacon-Dot-Technology/dp/B00JJ4P864/ref=sr_1_5?ie=UTF8&qid=1459677045&sr=8-5&keywords=ibeacon
piBeacon -- http://store.radiusnetworks.com/products/pibeacon

**Deviation** does not use mobile device

**Value of solution** faster to production. Cheaper and more easily usable that mobile.

### Steps
-- make sure the radBeacon is "ON" by clicking on the small button. It will blink green when it goes on. The battery will last for a year.
-- put radBeacon around the cow's neck as necklace using strong rope.
-- Let the cows wonder off to graze.
-- While tracking the cows, start the raspberry pi by providing it power.
-- You will see a green light glow when raspberry pi goes on.
-- Move around with the pi to known locations to find cow.
-- The raspberry pi will give beeping sound when a cow comes near its field.

### Implementation of the raspberry pi

### Algorithm
- Scan bluetooth IO for beacon every 250ms
- When beacon found check against cow beacon id
- When known beacon found, trigger alarm
- When unknown beacon found, continue search


Github link to project code : [http://github.com/hackproject/]

My notes at Google Notes and Keep :
Discuss on Slack #cowBell Channel : hackproject
Read complete project on Medium : 
Post comment on Twitter #hakcproject:cowBell
Schedule Mentoring session on skype : public google calendar or claralabs
Pre-req for mentoring : 
	- should know basic howto of raspberry pi
	- should know basic of ibeacon
	- should know simple python