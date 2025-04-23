<p align="center">
  <img width="600" src="/images/00_5x12ortho.png">
</p>

# Quick Summary

- :heavy_check_mark: 5x12 Ortholinear Keyboard
- :heavy_check_mark: Hotswappable
- :heavy_check_mark: Modular Spacebar 1x4u (57 keys) or 2x2u (58 keys)
- :heavy_check_mark: Wireless Bluetooth /w nice!nano running ZMK firmware

## Why?

I'm a clumsy man and I often hit the corner of my [96% keyboard](https://www.keychron.com/collections/96-layout-keyboards/products/keychron-k4-wireless-mechanical-keyboard-version-2) when I move my mouse.

So instead of doing the sensible thing and getting a TKL or smaller keyboard, I took the nuclear option of going straight into ortholinear keyboards (because I wanted one and to be honest, they look cool). 

There was a problem though. 

Of all the current 5x12 ortholinear keyboards on the market, I couldn't find one that was a) wireless and b) using a 1x4u spacebar or 2x2u spacebar setup. 

Either I wait for someone to make and sell it or I build it myself.

So... here I am, learning how to make it from the ground up over the course of a few months with no knowledge of pcb design and keyboard form factors. 

Here are some of the steps I've taken to make it.

#### PCB Design
- USB port on the left since it couldn't fit on the top
- Added a reset switch into the board for quick firmware flashing
<table>
  <tr>
    <td>Schematic</td>
     <td>Trace Routing</td>
  </tr>
  <tr>
    <td><img src="/images/01_schematic.png" width=450</td>
    <td><img src="/images/02_kicad_pcb.png" width=450</td>
  </tr>
 </table>

<table>
  <tr>
    <td>PCB Front</td>
     <td>PCB Back</td>
  </tr>
  <tr>
    <td><img src="/images/03_pcb_front.png" width=450</td>
    <td><img src="/images/04_pcb_back.png" width=450</td>
  </tr>
 </table>

<sub><sup>Routing traces is literally playing the Tron Light Cycle game with copper lines instead of bikes.</sup></sub>


#### Top Plate
- 3D Printed with PLA filament at 100% infill
- 4x M2 screws for support

<table>
  <tr>
    <td>4U Spacebar Top Plate</td>
     <td>2x2u Spacebar Top Plate</td>
  </tr>
  <tr>
    <td><img src="/images/05_model_grill_4u.png" width=450</td>
    <td><img src="/images/06_model_grill_2x2u.png" width=450</td>
  </tr>
 </table>
 

#### Enclosure
- Inclined at a [7° angle](https://matt3o.com/about-mt3-profile-and-devtty-set/) as suggested by the MT3 Profile Creator
- Bezeled inner case to support the PCB
- 3D Printed at 100% infill for structural integrity as well 
- Print time was roughly ~60 hours

<table>
  <tr>
    <td>Top View</td>
     <td>Left View</td>
      <td>Right View</td>
  </tr>
  <tr>
    <td><img src="/images/07_model_top.png" width=450</td>
    <td><img src="/images/08_model_left.png" width=450</td>
    <td><img src="/images/09_model_right.png" width=450</td>
  </tr>
 </table>

<table>
  <tr>
    <td>Wireframe Right View</td>
     <td>Back View</td>
      <td>Wireframe Back View</td>
       <td>Bottom View w/ hex screwholes & reset port</td>
  </tr>
  <tr>
    <td><img src="/images/10_model_right_xray.png" width=450</td>
    <td><img src="/images/11_model_back.png" width=450</td>
    <td><img src="/images/12_model_back_xray.png" width=450</td>
    <td><img src="/images/13_model_bottom.png" width=450</td>
  </tr>
 </table>


#### 5x12 Ortho Build
- Added an on/off switch to quickly manually reset the battery powered MCU
<table>
  <tr>
    <td>Soldering hotwap switches & diodes</td>
     <td>Note scribbles trying to figure out the row & col pinouts</td>
  </tr>
  <tr>
    <td><img src="/images/15_5x12_build.png" width=450</td>
    <td><img src="/images/16_5x12_build.png" width=450</td>
  </tr>
 </table>
 
 <table>
  <tr>
    <td>Assembled Board</td>
     <td>3.7v 350mAh DS 602035 LiPo Battery + Foam Inserts </td>
  </tr>
  <tr>
    <td><img src="/images/17_5x12_build.png" width=450</td>
    <td><img src="/images/18_5x12_build.png" width=450</td>
  </tr>
 </table>
 

#### 4u Spacebar Setup
- Tactile Browns on Alphas, Space & Enter
- Clicky on Modifiers, Arrows and Numerals
<table>
  <tr>
    <td>Box Kailh Switches</td>
     <td></td>
  </tr>
  <tr>
    <td><img src="/images/19_5x12_build.png" width=450</td>
    <td><img src="/images/20_5x12_build.png" width=450</td>
  </tr>
 </table>


#### 2x2u Spacebar Setup

<table>
  <tr>
    <td>Box Brown, Orange, Royal Navy Switches</td>
     <td></td>
  </tr>
  <tr>
    <td><img src="/images/21_5x12_build.png" width=450</td>
    <td><img src="/images/22_5x12_build.png" width=450</td>
  </tr>
 </table>


## Completed Board \o/
<table>
  <tr>
    <td></td>
     <td></td>
      <td>On/Off Switch for easy access</td>
  </tr>
  <tr>
    <td><img src="/images/23_5x12.png" width=450</td>
    <td><img src="/images/24_5x12.png" width=450</td>
    <td><img src="/images/25_5x12.png" width=450</td>
  </tr>
 </table>

Shoutout to the wiki guides on [/r/MechanicalKeyboards](https://www.reddit.com/r/MechanicalKeyboards/) and the people over @ Nice Keyboards & ZMK for the great tutorials and help.

[current keymapping](/config/boardsource5x12.keymap)


Apr.25.23 Update:
Added gerber file for pcb manufacturing.

Feedback on 1x4u Spacebar setup 
It isn't perfect or great, would need a custom 4u springboard made to increase rebound sensitivity.
Using 2 additional 1u modified switches does not make it a great spacebar experience.
2x2u spacebar setup is still by far superior in feel and feedback responsiveness. 

Aor.23.25 Update:
Added stl model of the kb upon user request.
#whoa, the last update date and this update is just the year and the day swapped. 
What an odd timing and cool coincidence. 

<sup><sub>I'm on [reddit](https://www.reddit.com/user/winterwelon).</sup></sub>


