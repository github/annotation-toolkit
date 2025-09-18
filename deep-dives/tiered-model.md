
# The Tiered Models of annotating

It's not always clear what parts of a design absolutely need to be annotated before shipping. **Time constraints** may make it hard to thoroughly annotate _everything_. We can mitigate that by prioritizing what we annotate based on the highest severity of a potential issue as well as annotations that are quicker to fill out. 

_See the Tiered Model for [Priority](#the-tiered-model-priority)_

There is also a learning curve to documenting accessibility. **Accessibility knowledge gaps** may make some annotations harder to complete than others. We can mitigate that by prioritizing what we annotate based on the complexity of the components and the depth of accessibility knowledge required. 

_See the Tiered Model for [Difficulty](#the-tiered-model-difficulty)_

> [!NOTE]
> Depending on your product’s needs and its interface, some annotations might be unnecessary, or may be better categorized under a different tier. There is no one-size-fits-all ranking of these—this list is just meant as a starting place.


## The Tiered Model: **Priority**

<img width="800" alt="A slide listing 3 tiers of annotations. Tier 1 (Mandatory) includes Headings, Page structure, Buttons, Links, Images, and Form elements. Tier 2 (Ideal) includes Focus order, Landmarks, Language, Lists, Page title, audio, video and Primer A11y Presets. Tier 3 (Nice to have) includes Complex ordering such as arrow stops and reading order, Keyboard shortcuts, System feedback, Live regions, Tables, and user interactions." src="https://github.com/user-attachments/assets/121b76a9-4550-4f60-9488-39565f1c0644" />

### ⚠️ Tier 1: Mandatory
These types of annotations should be a vital part of every ship. The Accessibility team would consider mandatory as we've seen the most issues and risk from these types of elements. 
- Button
- Form element
- Heading
- Image
- Link
- Page Structure

### ☑️ Tier 2: Ideal
These annotations, combined with Tier 1, are the **ideal** level of annotation to aim for.
- Focus order
- Landmark
- Language
- List
- Page Title
- Primer A11y Presets
- Video & Audio

### ✨ Tier 3: Nice to have
These annotations are (combined with Tier 1 & 2) are nice to have and can help us prevent the most issues and make the best quality experiences we can. This is the level of support the Accessibility team gives when we embed with other teams or support new Primer component work, as those have such a high downstream impact. 
- Complex ordering (arrow stops and custom reading order)
- Keyboard shortcuts
- System feedback states
- Live regions
- Table
- User interactions (touch gestures, mouse actions, etc)

---

## The Tiered Model: **Difficulty**

<img width="800" alt="A slide listing 3 tiers of annotations. Tier 1 (Easy) includes Headings, Page structure, Buttons, Links, Images, Page Title, Audio and Video. Tier 2 (Moderate) includes Focus order, Form element, Landmarks, Language, Lists, System feedback, and Primer A11y Presets. Tier 3 (Advanced) includes Complex ordering such as arrow stops and reading order, Keyboard shortcuts, Mobile annotations, Live regions, Tables, and user interactions." src="https://github.com/user-attachments/assets/7c9034df-6366-4937-8824-71df003bcbfb" />


### 🟢 Tier 1: Easy
These types of annotations are the easiest to pick up for anyone new to annotating and accessibility.
- Button
- Heading
- Image
- Link
- Page title
- Video & Audio
- Page Structure

### 🟡 Tier 2: Moderate
These annotations require a bit more knowledge of accessibility to fully grasp.
- Focus order
- Form element
- Landmark
- Language
- List
- Primer A11y Presets
- System feedback

### 🔴 Tier 3: Advanced
These annotations require deeper knowledge of accessibility to use without potentially creating new issues that might not have existed in a design.
- Mobile annotation
- Complex ordering (arrow stops and custom reading order)
- Keyboard shortcuts
- Live regions
- Table
- User interactions (touch gestures, mouse actions, etc)


## Additional considerations
Ensuring that we take care of those Tier 1 annotations will really help create consistency and shared understanding between the product you work on and the company as a whole. Having conversations about these things early on fosters healthy feedback loops.

For example, when we're mindful of **headings** and **page structure**, we're considering where our features or pages are within our vertical as well as within the larger context of GitHub. It helps us create global navigation and breadcrumbs more efficiently, with fewer design-preventable issues.

