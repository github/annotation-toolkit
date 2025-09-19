# How to: **Flow lines**

Flow lines can help organize design canvases. These components have robust labels for various scenarios to help designers clearly communicate the full range of platform functionality, validation states, and user interactions.

## Why?

Annotating design interactions and gestures with flow lines can help:
- Keep Figma canvases organized
- Label various types of interactions, such as:
    - Touch gestures
    - Mouse actions
    - Platform functions
    - Device settings
- Highlight accessibility features in design, allowing more people to interact with the feature
- Give clear guidance to developers on how users will interact with designs

## Flow lines: Straight, L-curve, S-curve and U-curve

<img alt="Four flow lines in a row. Each flow lines contains a label with the text: write here. The first is a straight line pointing up, the second is L-curve: L-shaped, the third is S-curve: S shaped, and the final line is U-curve: a U shaped. Each line originates from a circle and terminates with an arrowhead." src="Images/flow-line-annotations.png" width="1012">

### Label types

#### Post-it note (default)

Post-it notes are best for short, quick annotations. The color of the post-it can be customized as well as the content.

<img alt="Post it note annotation label that contains the text “Write here...”." src="Images/post-it.png" width="557">

#### Manage focus

Indicates that focus is deliberately managed through code to support accessible navigation and user experience.

<img alt="Manage Focus annotation label: a maroon pill that contains the text Focus Managed." src="Images/focus-managed.png" width="557">

#### Error state

Error states refer to a documented visual and behavioral representation for when something goes wrong. The error can be due to an invalid input, system failure, failed user action, and more.

<img alt="A light red pill with a dark red speech bubble icon and a label that says Error." src="Images/error-state.png" width="557">

#### Warning state

Informs about a potential issue or consequence as the result of an action.

<img alt="A light yellow pill with a dark yellow speech bubble icon and a label that says Warning." src="Images/warning-state.png" width="557">

#### Success state

The visual and behavioral feedback shown when a user’s action is completed successfully.

<img alt="A light green pill with a dark green speech bubble icon and a label that says Success." src="Images/success.png" width="557">

#### Info state

Highlights important information that has an influence on the current view or offers an action.

<img alt="A light blue pill with a dark blue speech bubble icon and a label that says Info." src="Images/info.png" width="557">

#### Live region announcement

Live regions are parts of a webpage that are monitored for dynamic content updates. They “listen” for these updates and announce the changes to assistive technologies like screen readers, allowing everyone to stay informed in real time.

<img alt="A light purple pill with the label Live Region Announcement." src="Images/live-region-annotation.png" width="557">

#### Keyboard shortcut

Clearly labels a pre-set or custom combination that a user presses on a keyboard to initiate an action, such as selecting a menu item, copy/paste text, and refreshing the page.

<img alt="Keyboard keys labelled “Ctrl” and “Alt”, shown as adjacent rectangular buttons joined by a plus sign." src="Images/keyboard.png" width="557">

#### Touch gesture

Touch gestures identify what user action is required especially for touch screens.

<img alt="A rectangular label for a single-tap gesture. The icon is a hand with an index pointer finger out, which has a purple ripple coming from it to convey the tap." src="Images/single_tap.png" width="557">

#### Mouse action

The mouse action label highlights an action performed with a mouse, such as clicking, double-clicking, right-clicking, or scrolling. 

<img alt="A rectangular label for a Double-click mouse action. The icon is a mouse with shaded left button and two small starbursts coming from it to convey two clicks." src="Images/dbl-click.png" width="557">

#### Device setting

Device settings refer to preferences or configurations that a user sets at the system or device level to customize how content is displayed or how interactions behave. 

<img alt="A rectangular label for a Viewport zoom setting with illustration of a browser window with a magnifying class centering a plus sign in the corner." src="Images/viewport.png" width="557">

#### Platform function

A built-in capability of an operating system or application that supports an interaction or accessibility features. 

<img alt="A rectangular label for a Loading state with purple spinner loading clockwise." src="Images/loading.png" width="557">

### How to use these annotations

1. Place a **❖ Flow line Stamp** component over the design (Straight, L-curve, S-curve, or U-curve). Resize and position it on the canvas as needed.
- **Direction:** Specify both the origin direction and the direction that the arrow points. For example, left to right, right to bottom, etc.
- **Dashed line:** Toggle the stroke style of the line.
- **Show label:** Enable if a label is needed to convey more context from one frame to another.

<img alt="A Flow line component and Figma properties panel. The L-curve flow line has a post-it note for a label, which contains the text: write here. The Figma properties panel shows settings to change the direction of the flow line, the label type (set to post-it note), post-it position (set to center), and the color (Purple)." src="Images/post-it-label-detail.png" width="557">

2. If you need to convey more specific context than a general note (state, announcement, interaction, or managed focus), select it from the **Label type** options.
- **Show Post-it:** If the label type is not a post it, toggling "Show post it" on will attach a post-it note below the label in order to help add some more context.
    - **Post-it position:** If Show Post-it is enabled, this allows the note to be shifted from a Centered position to the Left or Right. Helpful in the event that labels overlap key visuals.

3. Configure additional label properties as needed. Keyboard shortcuts, touch gestures, mouse actions, device settings, platform functions all have complex configurations.

<img alt="The same Flow line component and Figma properties panel showing a change in setting for the Label type of the L-curve flow line. The selected label type is Success state, and instead of a purple post-it note for a label, the flow line has a green pill label that says Success. Other properties are obscured by the Label type drop-down options." src="Images/success-state-details.png" width="557">