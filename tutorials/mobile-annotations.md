# How to: Mobile annotations

Mobile annotations are designed to support accessible UI design by providing clear, structured notes for interactive elements. Unlike other types of annotation in this library, **these annotations assume foundational knowledge of mobile app accessibility**. They include iOS, Android, and platform-agnostic annotations to guide implementation across different operating systems.

**Types of annotation:**
- [Mobile Stamps and Details](#mobile-stamps-and-details)
- [View context Stamps and Details](#view-context-stamps-and-details) 


## Why?

Native apps require specific accessibility properties that screen readers and assistive technology depend on. Mobile screen readers narrate visual content in a specific format, with a pause in between each part: 

**Label + Value + Role + Hint**
- Accessibility **labels** provide meaningful descriptions of UI elements;
- **Values** and states indicate the current condition of controls like toggles and sliders;
- **Roles** and **traits** communicate how elements behave;
- **Hints** offer additional context without cluttering the interface. 

Though the order of these parts may differ depending on a user’s settings (especially for Android devices), it’s important that each individual part is included properly.

Mobile annotations also pair well with User Interactions to make things like Touch Gestures clear.

---

## Mobile Stamps and Details

Unlike many other components in this Toolkit, these annotations require a fair bit of knowledge about mobile app accessibility.

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 3: **Advanced**
- Priority Tier 1: **Mandatory** (for mobile apps)

<img src="Images/mobile-annotations.png" alt="Skeleton screen of a mobile interface with annotations. The left side highlights a Title and Heading with pin annotations. The right side has a bracket stamp button annotation in the top right corner, a pin annotation for a button, and a lasso stamp with a note number of 1 for a list item. To the right of the mobile interface is a Mobile Details annotation titled Menu Item, which includes many fields, including label, value, and trait." width="1012">

### Platform variants
#### iOS

iOS annotations can be differentiated by their **blue** color as well as the VoiceOver icon for iOS. 
This distinction can be helpful when designing and annotating both mobile platforms on the same canvas.

<img src="Images/ios-annotation.png" alt="Mobile Details annotation with blue accent colors, a label field, and a note number of 1. The platform has been set to iOS." width="557">

#### Android

Android annotations can be differentiated by their **green** color as well as the TalkBack icon for Android. 
This distinction can be helpful when designing and annotating both mobile platforms on the same canvas.


<img src="Images/android-annotation.png" alt="Mobile Details annotation with green accent colors, a label field, and a note number of 1. The platform has been set to Android." width="557">

#### Any platform

This set of annotations defaults to being **platform-agnostic**. 
This may be useful when building a mobile experience for only one platform and there is no need to differentiate between them.

<img src="Images/agnostic-annotations.png" alt="Mobile Details annotation with dark cyan accent colors, a label field, and a note number of 1. The platform has been set to any." width="557">

### Components
#### Mobile Grouping Stamp

The Grouping Stamp is the cornerstone of mobile annotations. It is used to highlight multiple objects to be announced together. Examples include related information, a group of actions with a common purpose, images and accompanying text, paragraphs of text that aren’t divided by headings, and so forth.


<img src="Images/mobile-lasso.png" alt="Three mobile lasso annotations labelled with note number 1. Each lasso has a unique colour and icon, referring to its platform. The first is dark cyan and platform agnostic, the second is blue and iOS, and the third if green and Android. " width="679">

#### Mobile Structure Stamp

Text marked as a **Heading** will help users understand the purpose of a section. Screen readers users can also to navigate quickly between sections of a view based on headings and other elements. 

**Titles** are announced after transitioning to a view and should be placed toward the top. They are similar to `<h1>` headings on web experiences, helping users orient and understand the purpose of the content.

> [!CAUTION]
> Headings and Titles are optional and it’s common for views to not have either one. Only use headings when they truly help illuminate the structure of a screen.

<img src="Images/mobile-stamp-annotations.png" alt="Two annotations: one is a dark cyan mobile pin stamp with a label of Heading. The second is a dark cyan mobile bracket stamp with a label of Title." width="679">

#### Mobile Button Stamp

Mark controls that initiate important actions. Remember, not all tappable controls are buttons, so be strategic about their placement.

<img src="Images/mobile-button-stamp.png" alt="Three mobile stamps with a label of Button. Each has a unique color and icon, referring to its platform. The first is a dark cyan pin stamp and platform agnostic, the second is a blue iOS bracket stamp, and the third is a green Android pin stamp. " width="679">

#### Mobile Details

Open-ended and flexible, this annotation requires knowledge of mobile accessibility in order to create accurate accessibility specs. Pair with Mobile Button, Grouping, or Structure stamps. 

- All interactive elements (and some static) must have a **label**.
- **Value** can be used to inform screen readers about a control’s current state, what text has been entered in an input, or other relevant info.
- All interactive elements (and some static) must have a **role** to programmatically inform screen readers about what they do. iOS and Android do this in different ways.
- Most interactive elements come with a default **hint** set by the operating system which cues users about how to interact with them. You may edit hints but don't include critical information here, as many users have their screen readers set to ignore hints.
- If using a stock mobile component, toggle **Follow stock native pattern** and link any relevant specs via the **Link to Docs** list. This can help save a lot of repetitive writing during the annotation process.

<img src="Images/mobile-details-annotation.png" alt="Dark cyan mobile details annotation with all toggles enabled, which results in multiple fields being displayed, including label, value, trait, role, state, hint, which all currently contain placeholder text. Additionally, there is an accessibility actions section which contains two further fields: default action, with a value of activate, and other actions with placeholder text: additional actions " width="679">

#### Mobile Live Region Announcement

Primarily used when specific states of multiple components require giving an update to users, such as announcing search results.
The `polite` or `assertive` behavior of live region announcements can be simulated on `iOS` and `Android` as long as specific traits and settings are included.
*Note: These components are isolated variants from System Feedback set of* **❖ Live Region** *components*. 

<img src="Images/mobile-annotations-live-region.png" alt="Two details annotations: The first is a blue iOS live region mobile announcement with a note number of 1. The annotation contains multiple fields, including message, trait (updatesFrequently), and documentation links. The second is a green Android live region mobile announcement with a note number of 1. The annotation contains multiple fields, including message, and documentation links. Both details panels have been set to polite. " width="679">

### How to use these annotations

1. ​Add a **❖ Mobile Grouping Stamp** , **❖ Mobile Structure Stamp**, or **❖ Mobile Button Stamp** component from the asset panel. Place the stamp over the design frame and resize to extend pin, bracket, or lasso. Configure the component properties as needed.
   - **Platform**: Optional. Set to `iOS` or `Android` if visual distinction is needed on your design canvas.
   - **Label position**: Set based on Stamp’s placement relative to the element being annotated.
   - **Stamp type**: Switch between Pin and Bracket Stamp formats.
   - **Show number**: Toggle off if there’s no need for a matching Details annotation (in which case, skip to step 2).
   - **Note number**: Set this number in relative sequence with the other numbered Stamps placed over the same design.

<img src="Images/how-to-mobile-grouping.png" alt="A mobile button pin stamp next to a Figma properties panel. The note number has been set to 3, the stamp type is bracket, the label position is on the right, and the platform has been set to: any." width="557">

2. ​Place a **❖ Mobile Details** component in the margins next to the design and configure the component properties as needed:
   - **Platform**: Optional. Set to iOS or Android if visual distinction is needed on your design canvas.
   - **Note number**: Set this to match the corresponding **❖ Mobile Stamp**. This number should be unique and in relative sequence with other Details annotations on the same design.
   - **Show guidance**: Toggle high-level guidance and resources. 
   - Toggle and fill out other properties like **label**, **value**, **trait**, **role**, **state**, **hint**, and **actions**. *Remember: Mobile screen readers narrate visual content in a specific format: Label + Value + Role + Hint*

<img src="Images/how-to-mobile-details.png" alt="A table details annotation with a title of Menu item and a note number set to 3. Next to it is a Figma properties panel. The label has been set to Pull Requests, the value is blank, the trait is .Link, and there are some additional code snippets, links to documentation, and details about custom actions." width="557">

---

## View Context Stamps and Details

Identify areas that may have different accessibility considerations than native UI elements, such as web views, user generated content, long blocks of text content that lacks headings, or other non-native content such as PDF views.

### Why?
This classification helps developers and testers understand what content can be directly annotated versus content that may need special handling during accessibility testing or implementation.

### Variants
#### Web view

Web views show up in many apps, especially in OAuth login flows, in-app documentation, or other embedded content. They create unique accessibility hurdles that are important to keep in mind:
1. The boundary between native elements and web view content can be tricky for screen readers, making it important to implement careful focus management.
2. Not all screen readers interact with them the same way as native content. VoiceOver will behave differently with web content than with native iOS elements, for example.
3. Web content might have different interaction patterns than the surrounding native app, creating inconsistent and confusing user experience. Users might not realize they're in a web view, so maintaining consistency in the experience is key.

<img src="Images/webview-annotations.png" alt="A view context lasso stamp and details annotation with the note number set to 1 and cyan accents. Both annotations have label of: web view." width="557">

#### User generated

Areas containing content that can’t be directly annotated as they are controlled by users. This might be text such as user profiles, chat messages, or media uploads such as pictures and videos. These areas may have unpredictable content structure, missing alt text, low contrast color choices, or inaccessible embedded media.

<img src="Images/user-generated-annotations.png" alt="A view context lasso stamp and details annotation with the note number set to 2 and cyan accents. Both annotations have label of: user generated." width="557">

####  Text content

Highlight large blocks of text content that aren’t broken up by interactive controls, headings, or other interactive elements. Sometimes there are legal requirements to include large blocks of text. This stamp can be used suggest ways to improve readability, such as adding lists, tables of contents, or progressive disclosures.

<img src="Images/text-content-details.png" alt="A view context lasso stamp and details annotation with the note number set to 3 and cyan accents. Both annotations have label of: text content." width="557">

#### Non-native content

Users often come across content that wasn't built with the platform's native UI components. These are things like PDF viewers, document viewers, media players, and interactive maps. These may not fully integrate into a platform or app’s accessibility services.

<img src="Images/non-native-content-details.png" alt="A view context lasso stamp and details annotation with the note number set to 4 and cyan accents. Both annotations have label of: non-native content." width="557">

---

## Design considerations

- Which elements on this screen need to be announced together by screen readers?
- Do all UI elements have clear labels in your design? Have you identified which text labels belong with which controls?
- What's the logical reading order for this screen?
- Are there any decorative elements that should be hidden from screen readers?
- Can you mark which content blocks should be treated as a single unit for screen readers?
- How should off-screen or dynamically appearing content be handled?
- Which elements on this screen perform actions when activated?
- Are there any custom controls that could be replaced with standard ones?
- How will the VoiceOver rotor on iOS will navigate this content?
- How will TalkBack swipe gestures navigate through this content on Android?
- Are touch targets sized appropriately for each platform?
- How can users navigate the experience with a keyboard instead of touch? 

## Resources

- [​Accessibility documentation - Appt](https://appt.org/en/docs)
- [Guidance on Applying WCAG 2.2 to Mobile Applications - W3C](https://www.w3.org/TR/wcag2mobile-22/)
- [Mobile-WCAG Mapping - GitHub Accessibility Audit Guide (Internal Only)](https://github.com/github/accessibility-audit-guide/blob/main/mobile/mobile-wcag-map.md)
- [Getting To The Bottom Of Minimum WCAG-Conformant Interactive Element Size - Smashing Magazine](https://www.smashingmagazine.com/2024/07/getting-bottom-minimum-wcag-conformant-interactive-element-size/)
