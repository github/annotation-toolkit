# Best practices for annotating 🏆

The best annotation kit is only as useful as it is legible for the people consuming the annotations. Here are our recommended techniques for keeping our documentation easy to read and free of overwhelming clutter.

> [!TIP]
> 1. When positioning Stamps on top of a design frame, it can be helpful to Lock (**Shift + Command/Control + L** <kbd>⇧</kbd>+<kbd>⌘/⌃</kbd>+<kbd>L</kbd>) the frame or hold down the **Space** <kbd>__</kbd> key while dragging a component. This helps prevent Stamps being inserted into the design itself which can make them difficult to edit and disrupt the layout of any frames that use auto-layout.
> 2. You don’t need to annotate existing UI that hasn’t been changed in the current work, or is not an immediate part of the new user experience.

---

## Best practice 1: Keep the design frame legible
Try to place stamps outside the frame, with the “pin”, “bracket”, or “lasso” referencing the appropriate design element. 

With closer proximity to associated Detail components in the margins, engineers can quickly scan the annotations and there is less risk of them accidentally overlooking one.

Keeping the design frame legible also makes the distinction between the original design and our annotations more obvious. This reduces the time and cognitive effort required for folks to understand the documentation.

| **Less legible** | **More legible** |
|--|--|
| <img alt="GitHub’s 2025 Universe website homepage. There are 23 annotation stamps overlaid on the design, placed in such a way that it's confusing to figure out what stamp relates to what content, as well as where the annotation stops and the design starts." src="https://github.com/user-attachments/assets/4aa227ec-2fca-4013-b919-b056a3616407" /> | <img alt="The same page with annotation stamps that are not too close to one another, don't overlap, and extend just past the design frame's borders. Annotations are now easily distinguishable, and the underlying design is far less obscured." src="https://github.com/user-attachments/assets/84395858-46e9-477f-be60-2c2a8917c9d2" />  |


---

## Best practice 2: Split annotation types on to duplicate frames
Large features and full pages may contain hundreds of elements to annotate. Putting every type of annotation on only one frame can make it become visually overwhelming and difficult to parse. 

One strategy to help keep things legible is to duplicate the page/frame and place only one or two types of annotation on each. This also helps ensure there is room around the design to place annotations in a legible way, as described in best practice #1.

In this example, we have split one fully annotated design into two, with Focus Order annotations on their own dedicated frame.  

| **Before** | **After** |
|--|--|
| <img alt="GitHub’s 2025 Universe homepage on mobile in portrait orientation. There are annotation stamps for links, buttons, images, focus order, and headings. All combined, it appears a bit like someone sneezed a lot of confetti on top of a design frame." src="https://github.com/user-attachments/assets/2fb7d81a-e41b-43b6-b1ab-8a74a038f05a" /> | <img alt="The same design, duplicated into two frames. The frame on the right has all of the focus order annotation stamps, while the frame on the left has everything else." src="https://github.com/user-attachments/assets/26ab5239-6b41-4812-8755-33d84c315da0" /> |

---

## Best practice 3: Deeplink stamp labels with details
Linking a Details annotation to its corresponding Stamp can be helpful for helping people understand which Stamp is associated with which Details instance. This can be especially useful for complicated annotations, or situations where the Stamp and its corresponding label are visually separated.

To deep-link a Stamp label with its corresponding label:

1. Select the Details annotation instance.
2. Press **Command/Control + L** <kbd>⌘/⌃</kbd>+<kbd>L</kbd> to copy the Details instance’s URL to the clipboard. Figma will display a badge notification to communicate that the URL was successfully copied.
3. Click on the text of the corresponding Stamp label until it is highlighted.
4. Press **Command/Control + K** <kbd>⌘/⌃</kbd>+<kbd>K</kbd>.
5. Figma will open a command palette menu, with the “Create link” option selected. Press **Return** <kbd>⏎</kbd> to activate this option.
6. A tooltip menu will pop up over the selected Stamp label text, with a placeholder that reads, “Type or paste a URL”.
7. Paste the Details annotation instance’s URL into the tooltip by pressing **Command/Control + V** <kbd>⌘/⌃</kbd>+<kbd>V</kbd>. Then press **Return** <kbd>⏎</kbd> to add the link.
8. The Stamp text will become underlined, confirming the link has successfully been added. 


| **First copy the detail instance URL** |
|--|
| <img alt="A process flow with three steps. Step one shows a detail instance in a selected state. Step two shows a Command plus L keyboard shortcut combination. Step three shows a badge that reads, Page link copied to clipboard." src="https://github.com/user-attachments/assets/0ac6f1e6-3aa0-4ef4-a05c-2fbe12f217c2" /> |

| **Then create a link to the detail instance** |
|--|
| <img alt="A process flow with eight steps. Step one shows a button stamp instance. Step two shows the stamp in a selected state, with a cursor clicking on the stamp’s text label. Step three shows the stamp’s text label in a selected state. Step four shows a Command plus K keyboard shortcut. Step five shows a Figma command palette, with the “Create link” option selected. Step six shows a tooltip placed over the stamp’s selected text label, with a placeholder value that reads, Type or paste a URL. Step seven shows a Command plus V keyboard shortcut. Step eight shows the stamp again, with a text underline added to the stamp’s text label." src="https://github.com/user-attachments/assets/53053e46-e72b-4cfd-ac18-a9f78160855a" /> |


---

## Best practice 4: Annotate only what is needed
Designs often have repeated elements, such as a list of social media links. If there’s no variation for each repeated element, you may not need to annotate every single instance. Instead, you can annotate the first one and make a note of this.

This may also be the case with design treatments across multiple viewports. Many annotations might be the same regardless of viewport size or orientation. In this case, you may not need to annotate it more than once.

> [!TIP]
> It’s best to communicate this intentional choice to engineering partners to avoid confusion.

| **Before** | **After** |
|--|--|
| <img alt="The footer section of the GitHub 2025 Universe website, shown at a mobile breakpoint. There are seven linked social media icons in a row. Each icon has a numbered image and link annotation stamp associated with it, which covers part of the design. To the left and right of the footer are Detail annotations for each stamp, each which has only a small amount of difference in content. These take up a lot of room visually." src="https://github.com/user-attachments/assets/f7cfbc9c-0ccb-4571-8371-5b7decd8cc74" /> | <img alt="The same footer design for the GitHub 2025 Universe website. Now the entire row is selected with a lasso stamp. Only one icon inside the selection has an image and link stamps pointing to it. The corresponding three detail annotations instruct the reader to use each social media service’s name as the accessible name for the SVG icon, which is then used as each link’s accessible name. The overall experience is a lot less visually noisy." src="https://github.com/user-attachments/assets/8a587340-cdbd-460b-bd2e-97bd9f00ff90" /> |

---

## Best practice 5: Annotate complex components separately
The complexity of an interface is not always distributed equally. When annotating parts of a design that are more dense, there may be a lot of overlap between Stamps. There may also be more detail to a component than there is surrounding space to annotate it clearly.

This can be addressed in a couple of ways:

1. Annotating complex patterns in their own frames. Here you can break a design down into smaller, more focused parts to keep  things focused and more legible.
2. Using the Area out of scope utility annotation to cover parts of a page that are not relevant. This will provide more space to annotate complex sections, as well as focus attention on the parts that are relevant.


<img alt="A GitHub.com issues page with extensive annotations for images, links, buttons, headings, and form elements. The page's header, navigation, footer, and all but one Issue in the list have been obfuscated by a semi-transparent blue overlay to indicate that these parts of the annotated design are out of scope or redundant." src="https://github.com/user-attachments/assets/058f8720-9ead-4b35-a4eb-cd33de6a86e2" />

---

## Best practice 6: Split up complex components into separate screens

GitHub is full of complex interfaces, including patterns nested inside of other patterns. This can add additional risk, especially in terms of things like accessibility and keyboard navigation.

It’s helpful to break complex patterns down into smaller pieces when documenting designs. This will help convey vital information to engineers.

For example, nested lists that contain multiple interactive items are found in many places on GitHub. There are separate annotations for the header at the top of the container, the component’s container, as well as the list item itself. There are also annotations to convey focus order and keyboard navigation through several flows (not all of these are shown here).

<img alt="A complex set of annotation frames for our list views component, which has been broken up to make annotations clearer. One frame just shows annotations for the component's container itself. Another has the annotations for the row of actions at the top of the component. Another contains annotations for the content structure of the list items. A fourth shows detailed focus order annotations for the whole component." src="https://github.com/user-attachments/assets/1aedef8f-a99b-4a02-9fb0-477d8d950db1" />
