# How to: **User Interactions**

People engage with designs in different ways, often influenced by disabilities, be they permanent, temporary, or situational, as well as personal adaptive strategies. Interaction annotations help designers clearly communicate the full range of user interactions, making sure that diversity is considered and integrated during the build stage. 

**Types of user interactions**
- [Keyboard shortcut](#keyboard-shortcut)
- [Touch gesture](#touch-gesture)
- [Mouse action](#mouse-action)
- [Device setting](#device-setting)
- [Platform function](#platform-function)

## Keyboard shortcut

Annotate keyboard shortcuts to a fine detail with the kit. Choose between 1 to 5 key combinations, and specify both the key type (modifier, alphanumeric, or arrow) and the individual key.

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 3: **Nice to have**

### Why?

Keyboard shortcuts can be immensely useful to power users and novices users alike. They can also hurt accessibility usability if there is no way to adjust them or if it overrides a key feature that their assistive technology uses to map out a webpage.

<img src="Images/Keyboard_keys.png" alt="A series of keyboard keys organized into two rows. The top from left to right has Ctrl, Alt, Shift, Cmd, Opt, Esc, Tab, Backspace, Delete, Space, Enter and home. The second row, below, from left to right reads: End, Page Up, Page Down, and left, right, up, down arrow keys." width="1012">

### How to use a keyboard combo shortcut

Add a **❖ Keyboard combo shortcut** component from the asset panel. Place the stamp over the design frame and resize either the label or the flow line. Configure the component properties as needed:
    - Select a key combo length (anywhere between 1 - 5 keys)
    - Determine key types (Modifier, Alphanumeric, or Arrow)
    - Select the specific keys for the shortcut
    - If using a flow line with a keyboard shortcut as the label

<img src="Images/keyboard-keys1.png" alt="Four keyboard combinations arranged into a pyramid that build upon one another. Top row: Ctrl + Alt. Row 2: Ctrl + Alt + A. Row 3: Ctrl + Alt + Shift + A. Row 4: Ctrl + Alt + Shift + Opt + A" width="557">

**Caution**
- Keyboard combinations cannot interfere with common keyboard accessibility key commands (see [WebAIM Keyboard Accessibility](https://webaim.org/techniques/keyboard/)). 
- **Do not** introduce single-character shortcuts to a new feature.

## Touch gesture

A touch gesture is a physical interaction with a screen, such as tap, swipe, or pinch, made on a touchscreen to trigger a digital response or action.

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 3: **Nice to have**

### Why?

When designing touch interactions, it's important to consider whether they may create barriers for users with different disabilities. Because of this, touch gestures are grouped into three categories based on complexity: **Basic**, **Specialized**, and **Advanced**. These categories are included both as a reminder to consider those who depend on them *and* as a caution against using gestures that may be inaccessible. 

<img src="Images/gestures.png" alt="A row of eleven annotation squares on a gray background. The first ten show illustrations of the labeled gesture in light gray, and the last is a yellow square with an alert icon that says “proceed with caution”. From left to right, the squares read and illustrate: simple tap (closed right hand with pointer finger out. Pointer finger has a purple ripple coming from it); double tap (same pointing hand as prior with heavier purple ripple effect at pointer finger); move pan (same hand with pointer finger and purple ripple effect with a 4-way cursor to the left of the pointer finger); vertical scroll (same hand gesture as before with a long vertical arrow the length of the hand to the left of it); horizontal scroll (same pointer hand with a horizontal arrow above the ripple from the pointer finger); pinch in (right hand with open thumb and pointer, with the ripple effect for emphasis. Arrows start from both fingers and point inwards towards one another); swipe right (same pointer finger hand accompanied by a sweeping ripple affect and arrow pointing right); edge swipe from left (same illustration as before with a vertical line in the background of the hand), tap and hold (same illustration as simple tap with a red clock to the left of the pointer finger); double tap and hold (same illustration as double tap with a red clock to the left of the pointer finger)." width="1012">

### Gesture type

#### Basic 

Basic tap gestures are the most widely accessible, require minimal dexterity, and can be completed with the use of one limb.

<img src="Images/basic-gestures.png" alt="Four squares showing gesture types against a green background. Each has an illustration previously described in the hero illustration. From left to right, the annotations are: single tap, double tap, move/pan, and vertical scroll." width="557">

#### Specialized

Specialized gestures are more complex and should be used rarely, as they may be inaccessible to some users. Tap-and-hold or swipe gestures require fine motor control, limiting people with motor disabilities such as tremors, Parkinson's, arthritis, and cerebral palsy. Some people with visual disabilities will be inhibited by these gestures as they require visual feedback.

<img src="Images/specialized-gestures.png" alt="Six squares showing gesture types against a yellow background. Each has an illustration previously described in the hero illustration. From left to right, the annotations are: horizontal scroll, pinch in, swipe right, edge swipe from left, tap and hold, and double-tap and hold." width="557">


#### Advanced

Avoid using these. Multi-point input (using two or more fingers simultaneously) assumes users have both the physical ability and precise motor control to interact with a design. They are inaccessible on their own and should be avoided unless absolutely *essential* to an experience. 
If they *must* be used, you *must* provide [accessible alternatives](https://tetralogical.com/blog/2023/03/17/foundations-pointer-gestures/#examples-of-accessible-alternatives). Attempting to use these will present a warning and requires acknowledgement that accessible alternatives are provided.

<img src="Images/Advanced-gestures.png" alt="Ten squares, arranged in two rows of five, showing annotation types not yet covered against a red background. The first row from left to right is: single tap two fingers (right hand with pointer and middle finger emanating a purple ripple), tap and hold three fingers (right hand with pointer, middle, and ring finger emanating purple ripple with red block to the left of them), double tap four fingers (open right hand with shaking purple ripple around four fingers), double tap and hold two fingers (right hand with pointer and middle finger emanating purple ripple with red clock to the left of the fingers), and move pan two fingers (same hand illustration as before but a 4-way cursor instead of red clock). On the second row, left to right, is: scroll down two fingers (right hand with purple ripple around pointer and middle finger and left arrow to the left of them), swipe right four fingers (open hand with purple ripple over all fingers, pointing to the right, with a curved right arrow above). pinch in three fingers (right hand with activated thumb, pointer finger, and middle finger. Arrows start from the thumb as other fingers and point inwards to one another); rotate right (right hand with thumb and index in an L-shape, pointed to the right, with activated purple ripple and curved arrow over the thumb pointing right), and complex path (a right hand with a purple curve trailing the pointer finger)." width="557">


## Mouse action

Mouse action gestures refer to different actions that can be performed with a mouse. 

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 3: **Nice to have**

## Why?

Some mouse actions may impact accessibility and create barriers or confusion for users. Mouse actions are not accessible to all users, particularly those who are blind or have low vision, as they cannot rely on visual cues to navigate with a pointer. Not everyone can use a mouse, so all functionality must be available through accessible alternatives such as keyboard navigation. These are grouped into three categories based on complexity: **Basic**, **Specialized**, and **Advanced**.

<img src="Images/mouse-action-annotations.png" alt="A row of seven annotation squares on a gray background. The first six show illustrations of the labeled gesture in light gray using a mouse, and the last, “drag and drop”, features a mouse carrying a comet-appearing gesture with a four way cursor above it. From left to right, the squares read and illustrate: right click (mouse with shaded right button with three lines reaching out from it), double click (mouse with shaded left button and two small starbursts coming from it), hover (mouse with a soft halo effect from it), vertical scroll (mouse with an arrow pointing up and down to th left of the mouse), horizontal scroll (mouse with an arrow pointing left to right above it), and click and hold (mouse with left button shaded and a red clock to the left of it)." width="1012">


### Type

#### Basic

Basic mouse actions refer to those that are accessible for people that can navigate with a mouse. 

<img src="Images/basic-mouse.png" alt="Four squares showing mouse gesture types against a green background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: right click, double click, hover, and vertical scroll." width="557">


#### Specialized

Specialized mouse actions should be used sparingly as they can pose accessibility challenges for some users. They typically require additional user awareness, interaction, and customization.

<img src="Images/specialized-mouse.png" alt="One square showing a mouse gesture against a yellow background. The gesture, previously described, is horizontal scroll." width="557">


#### Advanced

Avoid using these. Advanced mouse actions require a level of physical ability and precise motor control that not every person has. They are inaccessible on their own and should be avoided unless absolutely essential to an experience. If they must be used, you must provide accessible alternatives.

<img src="Images/advanced-mouse.png" alt="Two squares showing mouse gesture types against a red background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: click and hold, drag and drop." width="557">


## Device setting

Device settings refer to preferences or configurations that a user sets at the system or device level to customize how content is displayed or how interactions behave. These, like touch gestures and mouse actions, should also be approached with caution. 


### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 3: **Nice to have**

### Why?

While device settings are meant to honor user preferences and create more accessible experiences, forcing them into design without a way to turn off or adjust functionality may end up creating barriers or confusion for users. These are grouped into three categories based on complexity: **Basic**, **Specialized**, and **Advanced**.

<img src="Images/device-settings-annotation.png" alt="A row of seven annotation squares on a gray background. From left to right, the squares read and illustrate: reduced motion (three overlapping consecutive circles that transform from a fuzzy purple outline to a smiley face); viewport zoom (illustration of a browser window with a magnifying class centering a plus sign covering the bottom right corner); viewport size (three overlapping viewports in a zoomed effect with each foreground viewport being darker and smaller than the one behind it);  horizontal orientation (three rectangles rotating 90 degrees clockwise from a vertical to horizontal position); vertical orientation (three rectangles rotating 90 degrees counterclockwise from a horizontal to vertical position); voice input (line art of a human face with consecutive lines of various length emanating from the mouth); and shake device (rectangle representing device in the foreground with parts of a rectangle randomly placed in the background)" width="1012">


### Type
#### Basic

Common and often expected platform functions, including:
- **Reduced motion** can reflect user preferences that are set at various levels (device, browser, platform, etc) to minimize discomfort from animations.
- **Viewport zoom** can enhance readability and accessibility. This can highlight changes to zoom level whether the preference is set via device, browser, or platform. This may not only increase the size of elements on the page, but affect reflow via layout changes as a design adapts to a different zoom level.

<img src="Images/basic-type-resize.png" alt="Two squares showing device setting gesture types against a green background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: reduced motion, and viewport zoom." width="557">


#### Specialized

Specialized device settings should be used sparingly as they can pose accessibility challenges for some users. These features support some user groups (for example, users with visual, motor, or cognitive disabilities). Not all users can or will interact this way, as individual abilities and device capabilities vary widely. 
- **Voice input** enable hands-free interaction through speech.
- **Viewport resize** can be used to show content adapting to various screen sizes. This may affect reflow via layout changes.

<img src="Images/Specialized-type-resize.png" alt="Two squares showing device setting gesture types against a yellow background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: voice input and viewport size." width="557">


#### Advanced

Advanced device settings are inaccessible and should be avoided unless absolutely essential. Provide accessible alternatives if they must be used.
- No assumptions should be made about the **orientation** of a device. Some users may have their device locked in a horizontal orientation (landscape), and therefore, any functionality that is limited to landscape/horizontal setting cannot be assumed accessible to everyone, or vice versa. 
- **Shake device** should be avoided as it may not be possible for a user to shake their device as an input. 


<img src="Images/Advanced-type-resize.png" alt="Three squares showing device setting gesture types against a red background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: horizontal orientation, vertical orientation, and shake device." width="557">


## Platform function

Built-in behaviors and constraints from the platform which define how people may use, navigate, and understand a digital experience.

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 3: **Nice to have**

### Why?

Some platform-level interactions may impact accessibility and create barriers or confusion for users. These are grouped into three categories based on complexity: **Basic**, **Specialized** and **Advanced**. 

<img src="Images/Platform-function-annotation.png" alt="A row of five annotation squares on a gray background. From left to right, the squares read and illustrate: loading (purple spinner loading clockwise); automatic transition (two circling arrows rotating clockwise with a clock face reading 5pm); open a new tab window (purple square with a blue arrow pointing outwards from the top right corner); time limit (clock face reading 5pm); and cognitive puzzle (a purple square puzzle comprised of 5 pieces and a red alert icon in the foreground covering the bottom right corner)." width="1012">


### Type
#### Basic

Basic platform functions do not present barriers as long as they are announced. 
Loading is a reminder to give users receive clear visual and programmatic feedback as they wait for content or actions to complete.

<img src="Images/loading1.png" alt="The loading annotation label against a green background." width="557">


#### Specialized

Specialized platform functions should be used sparingly, as they can cause frustration and pose accessibility challenges.
Automatic transitions involve system-initiated changes in screen, state, or content without direct user interaction. They can create confusion and disorientation.
Opening a link in a new tab or window may disorient screen reader users unless they’re given an audible cue to indicate the change. This removes access to the back button, making navigation more difficult. Screen magnification users may not notice a context switch at all, leading to a disjointed and confusing experience.

<img src="Images/Platform-specialized-resize.png" alt="Two squares showing platform function gesture types against a yellow background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: automatic transition and open a new tab window." width="557">


#### Advanced

Avoid these. Advanced platform functions are inaccessible and should be avoided unless absolutely essential. Provide accessible alternatives if they must be used.
Time limits can cause stress and anxiety for many users. This includes those with cognitive disabilities who may struggle to complete tasks in a set time limit, as well as those with motor control disabilities who may not physically be capable of performing the task in the allotted time. 
Cognitive puzzles (such as CAPTCHA) can be a struggle for people with cognitive disabilities. This may be due to working memory limitations, which contribute to the complexity of a puzzle, or a cognitive puzzle that relies on one sense. For example, blind and low-vision users that cannot see the screen are automatically disadvantaged when it comes to solving an image-based puzzle. Puzzles that require advanced mouse actions or touch gestures may also prove inaccessible for users with motor impairments.

<img src="Images/Platform-advanced-resize.png" alt="Two squares showing platform function gesture types against a red background. Each has an illustration previously described in the main illustration. From left to right, the annotations are: time limit and cognitive puzzle." width="557">


---

## Design considerations

- Can all functionality be accessed using more than one input method (e.g. mouse, touch, keyboard)?
- Are any input types required to complete a task? If so, is there an accessible alternative?
- Are you relying on a gesture or interaction that may not be supported across all input types (e.g., pinch to zoom, hover)?
- Have you considered how users will discover interactive elements using each input method?

## Resources

- ​[Foundations: Keyboard accessibility - TetraLogical](https://tetralogical.com/blog/2025/05/09/foundations-keyboard-accessibility/)
- [Foundations: Pointer gestures - TetraLogical](https://tetralogical.com/blog/2023/03/17/foundations-pointer-gestures/)
- [Knowbility: Exploring WCAG 2.1 - 2.5.1 Pointer Gestures](https://knowbility.org/blog/2018/WCAG21-251PointerGestures)
- [Home Office Design System: Gestures and motion](https://design.homeoffice.gov.uk/accessibility/gestures-and-motion)
- [W3C: Understanding 2.5.1 - Pointer Gestures (Level A)](https://www.w3.org/WAI/WCAG21/Understanding/pointer-gestures.html)
- [W3C: Understanding 2.5.7 - Dragging Movements (Level AA)](https://www.w3.org/WAI/WCAG22/Understanding/dragging-movements)
