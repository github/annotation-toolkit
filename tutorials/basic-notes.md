# How to: Basic Notes

Create interface guidelines and diagrams. Add details that don’t fit within any other type of annotation.

## Note Stamps and Details
If an element needs more info that doesn't fit within other annotation types, use a Note. Each Note stamp will need to have a Note Details component associated with it (paired via a matching **Note number** property).

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 1: **Easy**
- Priority Tier: N/A

<img src="Images/note-stamp-annotations.png" alt="A row of four annotations components: The first is a purple pin stamp with a label of Note, and a note number of 1. The second is a purple bracket stamp with a label of Note, and a note number of 2. The third is a purple lasso stamp which has a white and purple dashed outline attached to it, and a label of Note, and a note number of 3. The last annotation is a Details component with a note number set to 4. It is a white rectangular panel with purple accents. " width="1012">

### Variants

#### Question

Keep an always visible (and less ephemeral than Figma comments) question on the Figma canvas.
This can help when presenting design issues to stakeholders, attending an office hours session, etc. 

<img src="Images/question-annotations.png" alt="A Question pin annotation and an empty Details annotation. The note numbers are set to 2, and both contain a question mark icon." width="557">

#### Concern

Flag concerns with any part of a design for stakeholders, including:
- **Title**: Give this concern a name.
- **Date**: Optional. Add the date the concern was first written down. This may be helpful later on.
- **Description**: Required. Make the content of your concern clear. 
- **Possible issues**: Optional. Who is materially affected by this? How might they be impacted? How could those impacts *harm* users or the business?
- **Dependencies**: Optional. Include relevant constraints (technical or otherwise) that may impact those affected or prevent the concern from being resolved. 
- **Recommendations**: Optional. How should this concern be mitigated in order to reduce the impacts?
- **Path forward**: Optional. Add tangible next steps for how to resolve the concern.

<img src="Images/concern-annotations.png" alt="Four annotations components: The first is a purple pin stamp with a label of Concern, and a note number of 3. The second is a purple bracket stamp with a label of Concern, and a note number of 3. The third is a purple lasso stamp with a label of Concern, and a note number of 3. The last annotation is a Details component with a note number set to 3. The details annotation contains multiple fields, including Date, Description, Possible issues, Dependencies, Recommendations and Path forward.  " width="557">

### How to use these annotations
1. ​Add a **❖ Note Stamp** component from the asset panel. Place the stamp over the design frame and resize to extend pin, bracket, or lasso. Configure the component properties as needed:
   - **Label position**: Set based on Stamp’s placement relative to the element being annotated.
   - **Type**: Set to `Question` or `Concern` as needed.
   - **Note number**: Set this number in relative sequence with the other numbered Stamps placed over the same design.

<img src="Images/note-pin-stamp.png" alt="A Note pin annotation and a Figma properties panel. The note number has been set to 1. The label is positioned to the left." width="557">

2. ​Place a **❖ Note Details** component in the margins next to the design and configure the component properties as needed:
   - **Type**: Set to `Question` or `Concern` as needed.
   - **Note number**: Set this to match the corresponding **❖ Note Stamp**. This number should be unique and in relative sequence with other Details annotations on the same design.
   - **Title**: Add a descriptive name for the Details annotation. Make it clear what the paired Stamp is referring to.
   - If **Type** is set to `Concern`, enter as much info as needed through the optional properties for date, dependencies, issues, recommendations, and plans for moving forward.

<img src="Images/note-details-stamp.png" alt="A details annotation and a Figma properties panel. The note numbers have been set to 1. Show recommendations has been toggled on, but the recommendations field is empty. There is an empty description field." width="557">

---

### Interface Guidelines
#### Post-it
Freeform note component for short descriptions of interactions, frames, and user flow info.

<img src="Images/post-it-annotation.png" alt="Six post-it labels of various colours, including yellow, orange, light red, light purple, blue and green. Each post-it contains the text Write here." width="729">

#### UI Redlines
Redlines are annotations that point to specific areas of a design. Helpful when creating interface guidelines and diagram images. Resize to extend line.

<img src="Images/UI-redline.png" alt="Four redline annotations. There are two vertical lines, one contains arrowheads, the other doesn’t. And two horizontal lines, one contains arrowheads, the other doesn’t. Each have a label of 128." width="729">

#### UI Stamp
Basic annotation that points to specific areas of a design. Helpful when creating interface guidelines and diagram images.

<img src="Images/UI-stamp.png" alt="A row of 6 UI stamp annotations. The first three are pin stamps and contain the following labels: first has a label of Text, the second has a number of 1, the third contains a star icon. The next three are bracket stamps and contain the same labels." width="729">

### How to use these annotations

1. ​Place on the canvas and resize to extend the pointer as needed.
2. Select whether the **pointer** ends as a pin, an arrow, or a bracket. If a pointer is not needed at all, deactivate the **Show pointer** property.
3. Set **label position** based on Stamp’s placement relative to the element being annotated.
4. Set the **type** property:
   - `text` - Add a custom text label. Use short strings only.
   - `number` - to show a number. This can be helpful when creating an interface reference diagram, but is not intended to reference a corresponding Details component, nor convey things like focus order.
   - `icon` - functions similar to circle with an icon instead of a number. Helpful when needing to associate specific areas of a design with an icon legend. Icon instance can be swapped for others in GitHub's Octicon library.
5. Update the label with a short string of text, a number, or icon.

<img src="Images/how-to-basic-notes.png" alt="A UI Stamp annotation and a Figma properties panel. The label position is set to left, label type is text, and the pointer property is set to pin. " width="557">
