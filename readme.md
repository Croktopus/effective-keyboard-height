Front height has been a minor topic in keyboard interest checks for a long time, but recently enthusiasts have been putting more of an emphasis on it - not just designers, but consumers as well. This is a good thing, as too tall a keyboard can worsen typing comfort and ergonomics, but at the time of writing there is no standardized way to measure keyboard height, which can lead to confusion when a front height is quoted without context given. It also makes it a relatively difficult concept to discuss in designer communities, where "what's a good front height?" is one of the most common questions from newcomers to case design.

For that reason, we propose this standardized method to determine and compare keyboard height, the Effective Keyboard Height (EKH).

## Definition
The Effective Keyboard Height (EKH) is the distance from the bottom of the case (without bumpons) to the center of the spacebar stem (or some other bottom row key in the 60% cluster), when the switch is unpressed.

## Measuring
To measure this dimension on an assembled board, we recommend pulling the keycap, aligning an open caliper against the bottom of the keyboard, and gently closing the caliper until it just contacts the switch stem. Avoid measuring based on switches with silenced stems, as the thickness of the dampening material can introduce some (admittedly tiny) error.

To measure this dimension in CAD, measure off the appropriate dummy switch from the measuring-tools folder. Most publically available switch models aren't quite dimensionally accurate, so these models were made to be easy to use and to match the datasheets for each switch type. For the MX model, the circular portion at the bottom is designed to fit just into the model of the PCB, and the square section in the middle should fit into a typical plate cutout. Proper orientation is noted on the measuring dummy, and the measurement should be done from the bottom of the case to the ridge at the top which represents the center of the top of a switch stem.

You will also find Alps and Choc stand-ins in the measuring-tools folder, which can be used in similar ways (lining up the rectangle with the plate cutout and measuring from the ridge representing the center of the stem). Measurements using Alps will generally be slightly higher than ones using MX due to the switch being slightly taller, adding somewhere between 0.5mm and 1mm depending on the design, but the two are mostly comparable.

When listing an EKH in an IC or GB, if your keyboard supports multiple switch types, we recommend listing an EKH for each type of switch it supports. If you would like another dummy switch to be added, please open an issue and include a link to a reliable switch datasheet. We also recommend noting how much height you expect bump-ons to add, either in their compressed on uncompressed states (so, total thickness of bumpon minus the depth of the groove that you set them in).

## Goals
The objectives of this measurement system are as follows:
1. Ensure the dimension is independent of aspects irrelevant to the typing experience, such as bezel height or width
1. Allow for easy measurement both in CAD and on physical, assembled boards
1. Make the measurement process as straightforward as possible, to minimize error (as well as effort)
1. Maintain compatibility with as many layouts as is reasonable

## Previous Work
Similar definitions already exist to define what a proper keyboard height should be, with specifications for modern “low profile” keyboards (fun fact: Cherry MX was developed as a low profile switch) existing at least as early as 1984 and continuing to be updated to this day. However, there are a few reasons why we feel this standard is a better fit for this community.
* Existing standards tend to measure from the top of the keycap, which ignores the potential for different profile keycaps to be installed on the same keyboard design
* Measurements based on the home row can be gamed by using a particularly low keyboard angle
* The intent of this standard is not to set a maximum keyboard height, but to create a better shared vocabulary
* This is free

## Limitations
Many ergo keyboards will present a challenge for this measurement system. Keyboards with some keys angled off the horizontal axis (such as the TGR Alice or LZ Ergo), or ones with tenting or columnar stagger may introduce some error, as keys on the same row as one another will have different distances from the bottom of the keyboard. The EKH can still be used on such boards, but should not be a primary method of evaluating such a keyboard’s ergonomics.

Keyboards with more standard layouts but with thumb clusters or angled spacebars can still have a measured EKH, but the point to measure should be any of the non-angled/detached keys in the bottom row of the 60% block.

It may seem like keyboards with separated arrow keys pose a challenge for the EKH, but this is why we recommend measuring from a key on the bottom row of the 60% block, so if not a spacebar then perhaps the alt or control key. This may be a bit more difficult to design a board with separated arrow keys to the same height standards as one without, but since they don’t play into the typing experience, it’s best to ignore them for our purposes.

Keyboards that use a feet to provide angle can also be troublesome, but you can create a dummy desk top in CAD and measure from the top of that surface, as is shown in the Dire Wolf example below.

## Example Measurements

Here are a few reference images, that illustrate the positioning of the measurement tools, as well as the points from which to measure.

![Cypher, by Cablecar Designs](https://i.imgur.com/YRlJnds.png)
*Cypher, by Cablecar Designs*
# 

![Bushwacker, by Metamechs](https://i.imgur.com/BbJp7pk.png)
*Bushwacker, by Metamechs*
# 

![Dire Wolf, by Metamechs](https://i.imgur.com/WNKLEOg.png)
*Dire Wolf, by Metamechs*
#
# EKH Database
Designer | Keyboard | EKH
------------ | ------------ | -------------
Cable Car Designs | Cypher | 20.9
Duck | Orion v2.5 | 25.4
MetaMechs | Bushwacker | 21.8
MetaMechs | Dire Wolf | 26.3
MetaMechs | Timber Wolf | 23.8
pngu | idb60 | 23.7
Quantrik | Kyuu | 21.6
Cable Car Designs | Phoenix | 23.2
mkh studio | bully | 22.4

If you would like your keyboard to be added to this list, you can open an issue in this repo. Please include the designer or brand name, the keyboard name, and its EKH, as well as a screenshot or picture of the measurement.

# Credits
The EKH standard is a collaboration between DarthWTF and Crokto, with input from various other members of the Keyboard Atelier discord server.
