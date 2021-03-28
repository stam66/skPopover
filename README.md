# skPopover
A popover control for LiveCode, implemented as a group. Multiple aspects of the popover can be configured graphically or via API. 
When in edit mode, a red 'gear icon' will appear - hovering over this will open the configuration panel.
**Important:** The configuration panale stack should live in your Plugins folder to launch automatically; otherwise this needs to be opened manually.

### Putting a Popover on your card:
Putting a Popover on your card:
You can copy a prototype Popover simulation to the topstack to edit as needed by clicking the ***Copy to topstack button***. You may edit the prototype before copying across, or edit the popover after copying, by hovering over the corresponding Edit Settings icon (see *The Edit Settings Icon*).

Examples:
![skPopover Examples](https://user-images.githubusercontent.com/5677273/112755583-27013d80-8fd9-11eb-8917-a53eed0720d1.jpg)

#### How to use:
Copy over to the topstack with button. This will sequentially name all popovers on the visible card of the topstack, but rename the group as needed.

Hint: usually clicking on the background dismisses popovers, so consider leaving 'popover' or some other unique identifer in the group name, so when clicking on the card/outside the control, you can add mouseDown handler to dismiss all popovers:
    on mouseDown
       repeat with x = 1 to the number of groups of this card
          if "popover" is in the name of group x then hide group x
       end repeat
    end mouseDown

#### Resizing: 
**IMPORTANT** - ensure Select Grouped is **not** active and that you are not editing the group - reszing the group will then resize/move all elements of the popover appropriately.

#### Customising: 
Once renamed and resized, you can edit the group to add any controls desired -- do not delete any exising element the popup! 
 
### The Edit Settings Icon (the red gears icon)![mechanical-gears-svgrepo-com](https://user-images.githubusercontent.com/5677273/112755206-9ece6880-8fd7-11eb-8849-0a98c12322e4.jpg)

Hovering over the Edit Settings icon activates the palette to edit the corresponding popover.

It is hidden in browse mode/standalone and should appear only in Edit mode. It configures all aspects of the popover shape - you should add content and show/hide settings in the IDE - currently there is no provision for this.

You may also configure the popover programatically if dynamic changes are needed by using the API (all code is in the card script of Popover Settings).

Holding the shift key down while hovering over the Edit Settings button stop it from firing, enabling you to select and edit script if desired.

### The API methods (see card script for more detail)
- **setSide** *pSide*: left/top/right/bottom
- **setLocation** *pPercentageOfLength*: location of arrow along chosen side
- **scaleArrow** *pFactor*: scales arrow size to the length of chosen side
- **setCornerRadius** *pRadius*
- **setFillColor** *pColor*
- **setLineColor** *pColor*
- **setLineSize** *pSize*
