Front height has been a minor topic in keyboard interest checks for a long time, but recently enthusiasts have been putting more of an emphasis on it - not just designers, but consumers as well. This is a good thing, as too high a keyboard can worsen typing comfort and ergonomics, but at the time of writing there is no standardized way to measure keyboard height, which can lead to confusion when a front height is quoted without context given. It also makes it a relatively difficult concept to discuss in designer communities, where "what's a good front height?" is one of the most common questions from newcomers to case design.

For that reason, we propose this standardized method to determine and compare keyboard height, the Effective Keyboard Height (EKH).

## Definition
The Effective Keyboard Height (EKH) is the distance from the bottom of the case (without bumpons) to the center of the spacebar stem (or some other bottom row key in the 60% cluster), when the switch is unpressed.

## Measuring
To measure this dimension on an assembled board, we recommend pulling the keycap, aligning an open caliper against the bottom of the keyboard, and gently closing the caliper until it just contacts the switch stem.

To measure this dimension in CAD, we recommend measuring based off of the provided dummy switch which has been designed to make such measurement as simple as possible, as many publicly available switch models do not adhere to manufacturer specifications. The circular portion at the bottom is designed to fit just into the model of the PCB, and the square section in the middle should fit into a typical plate cutout. Proper orientation is noted on the measuring dummy, and the measurement should be done from the bottom of the case to the ridge at the top which represents the center of the top of a switch stem.

## Goals
The objectives of this measurement system are as follows:
1. Ensure the dimension is independent of aspects irrelevant to typing such as bezel height or width
1. Allow for easy measurement both in CAD and on physical, assembled boards
1. Make the measurement process as straightforward as possible, to minimize error (as well as effort)
1. Maintain compatibility with as many layouts as is reasonable

## Previous Work
Similar definitions already exist to define what a proper keyboard height should be, with specifications for modern “low profile” keyboards (fun fact: Cherry MX was developed as a low profile switch) existing at least as early as 1984 and continuing to be updated to this day. However, there are a few reasons why we feel this standard is a better fit for this community.
* Existing standards assume that a keyboard will only be used with the keycaps with which they come
* Measurements based on the home row can be gamed by using a particularly low keyboard angle
* The intent of this standard is not to set a maximum keyboard height, but to create a better shared vocabulary
* This is free

## Limitations
Many ergo keyboards will present a challenge for this measurement system. Keyboards with some keys angled off the horizontal axis (such as the TGR Alice or LZ Ergo), or ones with tenting or columnar stagger may introduce some error, as keys on the same row as one another will have different distances from the bottom of the keyboard. The EKH can still be used on such boards, but should not be a primary method of evaluating such a keyboard’s ergonomics.

Keyboards with more standard layouts but with thumb clusters or angled spacebars can still have a measured EKH, but the point to measure should be any of the non-angled/detached keys in the bottom row of the 60% block.

It may seem like keyboards with separated arrow keys pose a challenge for the EKH, but this is why we recommend measuring from a key on the bottom row of the 60% block, so if not a spacebar then perhaps the alt or control key. This may be a bit more difficult to design a board with separated arrow keys to the same height standards as one without, but since they don’t play into the typing experience, it’s best to ignore them for our purposes.

Also, when measuring physical keyboards, avoid using switches with silenced stems, as the thickness of the dampening material can introduce some (admittedly tiny) error.

## Best Practices for ICs
When discussing your keyboard’s EKH in your IC, you’re free to simply list the number on its own. However, we recommend providing the following information if relevant:
* Keyboard angle
* Additional height from bump-ons, specifying whether compressed or uncompressed. This should be the total thickness of the bump-on minus the depth of the recess they’re placed in.

## Context
