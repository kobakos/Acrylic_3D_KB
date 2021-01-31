# Acrylic_3D_KB
This is a 44 key 3D keyboard made by laser cut acrylic, designed by @kobakos32(twitter), u/kobakos32(reddit)

I assume that most people who read this has basic knowledge on building keyboards,like key matrix and firmwares,so i will just write about something specific on this keyboard.

In this guide, I will call the red colored part 'plate section', and the gray part 'bottom section'.
![case structure](/readme_images/irowake.png)

You will need solvent ,to adhere the acrylics together, and other basic things you'll need when you build a keyboard.

# About the laser cut path data
This data was made to fit into an A4 size sheet. please follow the format of where you order your acrylics to.
If you want this to be in a different format, you can modify this using graphic softwares such as inkscape.
Please use an 3mm thick sheet for this keyboard.

# rough procedure

## temporaly assemble the case
I strongly recommend you to temporary assemble the case before adhering the acrylics together. Even a minor error can add up to a major error, which will make the plate section unable to fit the bottom section. 
First assemble the bottom section, using these images as a reference.(If you want to takei a closer look at these images,please look at the original images in the images folder in this repository.)
Don't place the switches at this point.
![case structure](/readme_images/bottom_bunnkai.png)
![case structure](/readme_images/bottom_bunnkai_2.png)
Then, assemble the plate section, using these images as a reference and insert it to the bottom section.
![case structure](/readme_images/top_bunnkai_maue.png)
![case structure](/readme_images/top_bunnkai_naname.png)
![case structure](/readme_images/top_bunnkai_sita.png)
The plate part and the bottom part will intersect like this.
![case structure](/readme_images/top_bottom_intersect.png)
![case structure](/readme_images/top_bottom_intersect-2.png)
![case structure](/readme_images/top_bottom_interset_3.png)

## adhere the plate section
After assmebling the whole case, adhere only the plate section, since you wil have to solder the switches, and it will be hard to insert the plate section to the bottom section with the switches on, when you also adhere the bottom section(Because of my bad design...). Put organic solvent such as dichloromethane in a syringe or brush, and pour the solvent onto the acrylic bonding surface. Apply pressure(not too strong) to the bonding surface, and wait for tens of seconds to adhere the acrylics. You'll need to wait for a day for the acrylic to stik completely, but you can move on to the next step.
When handling dichloromethane, use the following safety precautions:
- Wear protective clothing. Footwear should cover the entire foot.
- Always wear PPE such as chemical splash goggles and safety gloves.
- Work in a well-ventilated area (preferably in an environment with a fume extraction system).
source:[MSDSonline](https://www.msdsonline.com/2015/02/20/dichloromethane-methylene-chloride-hazards-safety-information/)

## wiring and setting up firmwares
Before wiring, think about where and how to place the pro micro, or any other microcontrollers. In this keyboard, pro micro is meant to be mounted to the bottom plate using [ProMicroSocket(ProMicroのおうち)](https://booth.pm/ja/items/1073313) and m2 standoffs. If you are not using this, you will need to somehow mount the pro micro, and solder the cables to for the left side and the right side to communicate, which was originally done by trs cable. Reset button can be substituted by shorting the pins on pro micro, so it won't be a big problem.
The rest are the same as other keyboards. Please refer to [hand wiring guide](https://beta.docs.qmk.fm/using-qmk/guides/keyboard-building/hand_wire) and [split keyboard guide](https://beta.docs.qmk.fm/using-qmk/hardware-features/feature_split_keyboard) from qmk.
Don't wire any rows or cols to the D0 port(PD0) if you are going to use the default settings of QMK's split keyboard.

## operation verification
Check if the keyboard works properly since you won't be able to access some of the part of this keyboard once you adhere the whole case.
Check if...
- each key is responsive.
- there is any soldering defect.
- the communication between the left side and the right side is working properly.

## Adhering the whole case
If it seems like there are no errors, insert the plate section to the bottom section and adhere the whole case. Then mount the pro micro to the board and you're done!
