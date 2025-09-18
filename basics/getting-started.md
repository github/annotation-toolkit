# Getting started:  How to use the Annotation Toolkit

The Annotation Toolkit allows you to apply annotation labels (“Stamps”) over design elements. Stamps may also be set to correspond to detailed notes (“Details”) about the content the stamp points out. Details are often placed in the margins, so as to not obscure the design they document.

> [!NOTE]  
> Since the word “annotations” can refer to the individual components in this toolkit as well as the documentation as a whole (a finished, annotated design), we use the word “Stamp” to avoid confusion.

## Step 1: Label design elements with Stamps

Add a Pin, Bracket, or Lasso Stamp over the design from the Figma asset panel. In this example, we want to add **Link** and **Button** annotations to this page.

Use the **Label position** component property to change the orientation of the label. Try to align the Stamp label on the edge of, or outside the frame to keep the underlying design more legible. 

| Step 1 | Step 2 |
| :--- | :--- |
| <img alt="Selecting components from the Annotation Toolkit in Figma's asset library panel, with a GitHub.com homepage design on the canvas." src="https://github.com/user-attachments/assets/d51d9e73-eb88-442d-bcbe-44329483c99f"> | <img alt="With Link stamps on the canvas, the Figma component properties panel shows options for Stamp position, Note number, and whether or not to show that or the stamp pin." src="https://github.com/user-attachments/assets/01b4f6de-de70-4cc8-9e9a-4232742cf13b"> |
| Find the Annotation Toolkit components in the Figma asset panel. | Add Stamps to the canvas, setting their size and Label position. |

> [!TIP]  
> When positioning Stamps on top of a design frame, it can be helpful to **Lock** (<kbd>⇧</kbd>+<kbd>⌘</kbd>+<kbd>L</kbd>) the frame or hold down the <kbd>Space</kbd> key while dragging a component. This helps prevent Stamps being inserted into the design itself which can make them difficult to edit and disrupt the layout of any frames that use auto-layout.

## Step 2: Pair Stamps with Details components in the margins

Pair Stamps with **Details** components in the margins

You’ll notice that all of the Stamps have the same number. Make sure to update each Stamp instance using the **Note number** component property. This will help associate each Details annotation with its corresponding Stamp.

It helps to add these in a linear order so that engineers can read your annotations without getting lost or searching for two matching numbers, especially if many annotations are present.

In this example, some Stamps don’t need a matching Details annotation. Because of this, we can skip numbering these Stamps.

| Step 1 | Step 2 |
| :--- | :--- |
| <img alt="Selecting components from the Annotation Toolkit in Figma's asset library panel, with a GitHub.com homepage design on the canvas." src="https://github.com/user-attachments/assets/79c6b2f7-08ab-4479-9f2f-3b3b1258fd80"> | <img alt="With Link stamps on the canvas, the Figma component properties panel shows options for Stamp position, Note number, and whether or not to show that or the stamp pin." src="https://github.com/user-attachments/assets/dcb01ea9-ed43-4b19-9afb-ee38e160fbdc"> |
| Add Details components in the margins around the design frame. | Use the Note number property to pair Stamps and Details together. |

> [!NOTE]  
> In most cases, the sequence of the **Note number** property should apply to all different types of annotations on a given frame. It’s rarely necessary to have a separate numbering sequence for Buttons, and another for Links, and so forth.

## Step 3: Fill out the Details component properties

The content of these stamps can include interface behavior, code semantics, ARIA attributes, and more. 

Every type of Details annotation is different. Some, like the Note Detail, are open-ended. Others provide specific semantic properties that can help improve an experience for all users. 

Make sure to investigate the component properties of each annotation type you use to understand all the options it contains.

| Step 1 | Step 2 |
| :--- | :--- |
| <img alt="Configuring the top Details annotation for the design's mobile menu button. The Figma component properties panel shows options for Note number, Title, a toggle for submitting a form, Accessible name (optional), description (optional), additional details (optional), code snippet (optional), and links to docs (optional)." src="https://github.com/user-attachments/assets/32f52ed0-1e1b-4438-aea4-7f0033575eed"> | <img alt="All three details annotations are now configured." src="https://github.com/user-attachments/assets/5374959f-b4cd-439a-b775-f7639c679273"> |
| Add design intent to the Details via the properties panel. | All buttons and links on this frame have been annotated! 🎉 |

## How the annotation components work

Each annotation type has its own color, icon, text label, outline, and shadow. These signifiers all help to identify and differentiate annotation types from one another, as well as the designs they are placed over.

### Stamp formats

#### Pin stamps

Pin Stamps highlight one specific element in a design. 

The pin can be toggled off with the “**Show pin**” property, leaving just the label.

<img width="745" alt="A green stamp, with a label that reads, '1. Image' with a representative icon prepending the label. A dotted line that ends in a small dot extends from the right of the stamp. The '1' portion of the label is identified as, 'note number'. The icon and label is identified as, 'icon and label'. The dotted line extending from the right is identified as, 'pin'." src="https://github.com/user-attachments/assets/724a31ae-a33c-449e-a803-e98eeb2c5ab8">

#### Bracket stamps

Bracket Stamps are useful for highlighting sections of a page and elements without clear boundaries. 

<img width="745" alt="A blue stamp, with a label that reads, '2. Link' with a representative icon prepending the label. A solid line that ends in two forked tines extends from the right of the stamp. The '2' portion of the label is identified as, 'note number'. The icon and label is identified as, 'icon and label'. The solid line and tines extending from the right is identified as, 'bracket'." src="https://github.com/user-attachments/assets/f10c3d9c-45e5-44c0-a9f0-d0269556afbf">

#### Lasso stamps

Lasso Stamps are useful for highlighting groups of elements, sections of a page, or elements without clear boundaries. 

There are more “**Label position**” options for Lasso Stamps compared to Pin and Bracket stamps. This is to help reduce overlap.

<img width="745" alt="A pink stamp, with a label that reads, '3. header' with a representative icon prepending the label. A dotted line that ends in a rectangular region extends from the right of the stamp. The '3' portion of the label is identified as, 'note number'. The icon and label is identified as, 'icon and label'. The dotted line and rectangular region extending from the right is identified as, 'lasso'." src="https://github.com/user-attachments/assets/ab512d13-c550-4e5d-8433-bda455eef99d">

### Note numbers may not appear by default

Stamps for `Focus order`, `Arrow stops`, or `Reading order` have an **Order #** property to communicate a linear progression in the stamp label. `Heading` stamps have a **Heading Level** in their stamp label by default. 

These annotations typically do not need additional info. However, you can pair a Details component with these annotations if you need to. This is done by toggling the **Has note** property to reveal the **Note number** field.

<img alt="Three panels demonstrating a process flow. The first panel has a title that reads, ‘Ordering Pin Stamp’. It shows a focus order Stamp. Below it is a switch toggle with a label that reads ‘Has note’, and it is set to an off position. The second panel also has a title that reads, ‘Ordering Pin Stamp’. It shows a focus order Stamp with a note indicator added to it. Below it is a switch toggle with a label that reads ‘Has note’, and it is set to an on position. The third panel is titled,  ‘Ordering details’. it shows a Focus order Details annotation, with a note number that corresponds to the pin stamp in the previous panel. An arrow also extends from the note indicator in the second panel to the note number on the Details stamp in the third panel." src="https://github.com/user-attachments/assets/5e31f1bb-4541-421f-97da-13b37b7c9bad">

### Many Stamps may have label variants

Annotations such as Note, Heading, Landmark, List, Form Element, Table, Media and Primer A11y Preset stamps all have labels that can be changed through the properties panel.

| Add Stamp | Edit properties |
| :--- | :--- |
| <img alt="A landmark stamp set to show the header HTML element should be used. Next to it is Figma’s component property panel, which displays options for the landmark stamp. It has been configured to have the label position be on the left, to show a pin, and to show the number 3 as its note number." src="https://github.com/user-attachments/assets/7a19b267-3cc2-4995-b76b-fde03abe57ff"> | <img alt="A form element stamp (with a label of Input), a primer a11y preset stamp, and a landmark stamp sit to the left of a screenshot of Figma's properties panel. In the panel is an element dropdown that allows the stamp label to be changed. On the right are additional options for what the form element label could be." src="https://github.com/user-attachments/assets/d2edc964-78f5-4c9d-98ea-87407687c683"> |

### Details annotations can be extensively customized

Details are notes in the margins around a design frame. They are meant to be paired with Stamp components via matching **Note number** values.

The content of these Details annotations can include interface behavior, code semantics, ARIA, and much more. You will be prompted to fill out different kinds of content depending on the type of annotation used. 

Some properties can be hidden, while others cannot. Those that can’t are considered required. This is because there may be risk of accessibility issues or diminished UX quality if they aren’t filled out accurately.

Enabling the **Add more info...** property on any Details annotation will reveal more settings for:

- Additional details
- Code snippets
- Links to documentation (up to 5)

Some Details annotations also support indicating what keyboard shortcuts should be honored.

<img width="745" alt="A filled in Form element Details annotation for an Email input, with labels around the annotation to highlight its anatomy and various options. To the right of this is a screenshot of the Figma properties panel, where all of these can be configured." src="https://github.com/user-attachments/assets/302edd46-c198-4098-86f8-93c4dacd0718">
