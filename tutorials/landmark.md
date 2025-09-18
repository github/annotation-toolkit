# How to: Landmark
Mark important sections of a page and name them to so users can understand their specific purpose in navigating a page. 

## Why?
In every day life, we give context via landmarks. “Do you know where the hospital is on ______ street?” Web pages work the same way. Landmarks help screen reader users quickly scan and move to various sections of a webpage. For example, a `<footer>` landmark makes it easier to find the navigation links at the bottom of a page without moving through the whole website to search for it.

> [!TIP]
> If you are designing a new experience within GitHub.com, you may not need to annotate landmarks for areas of a design that aren’t changing (such as the banner area, header, and main navigation).

> [!CAUTION]
> Avoid overuse of landmarks to prevent clutter. Hearing 10 or more landmarks announced on a screen reader can be overwhelming and make it hard for a user to map a mental model. 

## Landmark Stamps and Details

### [Annotation Tiers](https://github.com/github/annotation-toolkit/blob/main/deep-dives/tiered-model.md)
- Difficulty Tier 2: **Moderate**
- Priority Tier 2: **Ideal**

<img src="Images/landmark_annotations.png" alt="A row of four annotations components: The first is a pink pin stamp with a label of header and a note number set to 1. The second is a pink bracket stamp with a label of main and a note number set to 2. The third is a pink lasso stamp which has a white and pink dashed outline attached to it, a label of footer, and a note number set to 3. The last annotation is a Landmark Details component for a div element with a note number set to 4. It is a white rectangular panel with pink accents. It contains properties for role and accessible name." width="1012">

### Elements

The labels and properties of Landmark annotations prioritize semantic HTML elements over implementations that use aria `role`. If you need the latter, you can toggle the **Show role** property.

#### \<header>

Identifies introductory content or site-wide information, such as branding or logos. It is usually positioned at the top of the page.
- **accessible name** is optional.
- **role** is set to `banner`.

<img src="Images/header-landmark.png" alt="A header lasso stamp component positioned next to a header landmark details annotation, both with a note number set to 1. In this example, the Has name and Show role properties are toggled on, resulting in the accessible name placeholder information and banner role information being displayed in the details annotation." width="557">

#### \<nav>

Identifies a section of the page containing links to other parts of the site or page, helping users quickly access key areas for browsing.
- **accessible name** is **required** and must be unique. Avoid including the word “navigation” or “nav”, as this will be announced based on the element/role. 
- **role** is set to `navigation`.

<img src="Images/nav_landmark.png" alt="A nav lasso stamp component positioned next to a navigation landmark details annotation, both with a note number set to 2. In this example, the Show role property is toggled on, resulting in the navigation role information being displayed in the details annotation." width="557">

#### \<search>

Identifies the site’s search functionality. This allows all users to quickly locate and operate site-wide or page-specific search tools.
- **accessible name** is **required** and must be unique. 
- **role** is set to `search`.

<img src="Images/search-landmark.png" alt="A search lasso stamp component positioned next to a search landmark details annotation, both with a note number set to 3. In this example, the Show role property is toggled on, resulting in the search role information being displayed in the details annotation." width="557">

#### \<main>

Contains the central content unique to the page between its header and footer. It allows assistive technologies to quickly identify and navigate to the primary content area. 
- There should only be one `<main>` landmark per page. It should not be contained within another landmark. 
- An accessible name is not needed.
- Skip links, which are used to bypass repetitive content, are often anchored to the `<main>` element. 
- **role** is set to `main`.

<img src="Images/main-landmark.png" alt="A main lasso stamp component positioned next to a main landmark details annotation, both with a note number set to 4. In this example, the Show role property is toggled on, resulting in the main role information being displayed in the details annotation." width="557">

#### \<section>

Defines a stand-alone group of elements and content. It is typically introduced by a **heading** to help organize a page into meaningful, logical parts. 
- **accessible name** is **required** and must be unique. Consider referring to the `section`’s heading as the accessible name.
- **role** is set to `region`. 

<img src="Images/section-landmark.png" alt="A section lasso stamp component positioned next to a section details annotation, both with a note number set to 5. In this example, the Show role property is toggled on, resulting in the section role information being displayed in the details annotation." width="557">


#### \<form>

Region that contains a collection of items and objects that, as a whole, combine to create a form when no other landmark is appropriate.
- **accessible name** is encouraged to help users understand the  form’s purpose, but required if multiple forms are on a page.
- **role** is set to `form`. 

<img src="Images/form-landmark.png" alt="A form lasso stamp component positioned next to a form details annotation, both with a note number set to 6. In this example, the Has name and Show role properties are toggled on, resulting in the accessible name and form role information being displayed in the details annotation." width="557">

#### \<aside>

Supporting section for main content, yet remains meaningful on its own. Often used for sidebars and content callouts. 
- **accessible name** is encouraged for all asides, and is **required** when multiple aside landmarks appear on a page. 
- **role** is set to `complementary`.

<img src="Images/aside-landmark.png" alt="An aside lasso stamp component positioned next to an aside details annotation, both with a note number set to 7. In this example, the Has name and Show role properties are toggled on, resulting in the accessible name and complementary role information being displayed in the details annotation." width="557">

#### \<footer>

Identifying common information at the bottom of each page, typically the “footer” of the page.  
- **accessible name** is optional.
- **role** is set to `contentinfo`.

<img src="Images/footer-landmark.png" alt="A footer lasso stamp component positioned next to a footer details annotation, both with a note number set to 8. In this example, the Has name and Show role properties are toggled on, resulting in the accessible name and contentinfo role information being displayed in the details annotation." width="557">

#### Custom landmark

A generic landmark container for content that is important enough that users should be able to navigate easily to this area. Can be helpful when a `<div>` element is needed rather than another semantic element that already has a **role** (proceed with caution).
- **element** is **required** and should match the stamp label.
- **accessible name** is **required** and must be unique.
- **role** is **required**.

<img src="Images/custom-landmark.png" alt="A div lasso stamp component positioned next to a landmark details annotation, both with a note number set to 9. The details annotation shows that an accessible name and role should be provided and that the selected element is a div." width="557">

### How to use these annotations
1. ​Add a **❖ Landmark Stamp** component from the asset panel. Place the stamp over the design frame and resize to extend pin, bracket, or lasso. Configure the component properties as needed:
- **Label position**: Set based on Stamp’s placement relative to the element being annotated.
- **Show number**: Toggle off if there’s no need for a matching Details annotation (in which case, skip step 2).
- **Note number**: Set this number in relative sequence with the other numbered Stamps placed over the same design.
- **Element**: Select the landmark element to ensure the Stamp is paired and labelled correctly.

<img src="Images/landmark-pin-stamp.png" alt="A section pin stamp and the corresponding Figma properties panel. The note number has been set to 9, with the label position set to left and settings to show the pin and number have been toggled on. At the end of the list of properties is a select element for selecting the specific landmark type." width="557">

2. ​Place a **❖ Landmark Details** component in the margins next to the design and configure the component properties as needed:
- **Element**: Select the applicable landmark element. 
- **Has name**: Accessible name is shown by default for many landmarks, and only needs to be enabled for `<header>` or `<footer>` in rare circumstances.
    - **Accessible Name**: Programmatic label for the landmark to help users quickly navigate to it. Unique names help differentiate landmarks of the same type from one another.
- **Show role**: Only needs to be enabled for other landmarks when not using the recommended semantic HTML element.
    - **Role**: Select the appropriate [landmark role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/landmark_role). This is set for many landmarks using the semantic element, but vital if using a custom landmark (especially when set to use the `<div>` element).
- **Note number:** Set this to match the corresponding **❖ Landmark Stamp**. This number should be unique and in relative sequence with other Details annotations on the same design.

<img src="Images/section-details-landmark.png" alt="A section details annotation and Figma properties panel. The note number has been set to 9, and the Show role property is activated, which shows the role of section in the component. The accessible name field is displayed with a placeholder." width="557">

## Design considerations
- Have all regions of the page been identified? 
- Does each landmark have a clear and unique purpose defined by the role and accessible name?
- Are there any redundant landmarks that are cluttering the page layout?
- In the case of multiple landmarks, do they each have unique and accessible names? For example, main navigation and secondary navigation.

## Resources

- [​Landmark roles - MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/landmark_role)
- [Foundations: Landmarks - TetraLogical](https://tetralogical.com/blog/2022/03/18/landmarks/)
- [Semantic Structure: Regions, Headings, and Lists - WebAIM](https://webaim.org/techniques/semanticstructure/)
- [WAI-ARIA landmarks - W3C](https://www.w3.org/WAI/ARIA/apg/)
