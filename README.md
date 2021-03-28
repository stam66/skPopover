# skPopover
A popover control for LiveCode, implemented as a group. Multiple aspects of the popover can be configured graphically or via API. 
When in edit mode, a red 'gear icon' will appear - hovering over this will open the configuration panel.
**Important:** The configuration panale stack should live in your Plugins folder to launch automatically; otherwise this needs to be opened manually.

### Putting a Popover on your card:
You can copy a prototype Popover simulation to the topstack to edit as needed by clicking the Copy to topstack button.
You may edit the prototype before copying across, or edit the popover after copying, by hovering over the corresponding Edit Settings icon
 
### The Edit Settings icon (the red gears icon)
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
