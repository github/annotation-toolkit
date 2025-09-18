# Engineering Checklist

This checklist summarizes success criteria from Web Content Accessibility Guidelines (WCAG) 2.2 (Level A and AA, in addition to best practices identified by GitHub), and categorizes it based on key aspects of engineering. Where applicable, each section also contains suggested tools and recommended resources.

If you don't have a designer on your project, or are not working with an accessibility specialist, we highly recommend also referencing the [Annotation Toolkit Design Checklist](https://github.com/github/design/blob/main/inclusive-design/annotation-toolkit/checklists/designer-checklist.md). We tried to minimize duplicate content between lists so more can be covered!

---

## 1. Color

- [ ] **Use design system color tokens over one-off code** 
	- Ideally, your design system and designer have covered the specifics around color contrast.
- [ ] **Run a color contrast checker on code** 
	- If a designer has not utilized the checklist, check out [Part 1: Color](https://github.com/github/design/blob/main/inclusive-design/annotation-toolkit/checklists/designer-checklist.md#1-color) for specifics around graphical and text color contrast.

### Suggested Tools
- [Check color contrast - Figma Docs](https://help.figma.com/hc/en-us/articles/360041003774-Apply-paints-with-the-color-picker#h_01JQF1T71AC72G6VDXN27B77V0)
- [Web Color Contrast Checker - WebAIM](http://webaim.org/resources/contrastchecker/) 
- [Colour Contrast Analyzer for Mac and Windows -  TGPi](https://www.tpgi.com/color-contrast-checker/)

---

## 2. Hierarchy

- [ ] **No duplicate headings**
	- Duplicate headings may confuse screen readers, impair navigation, and disrupt understanding of page structure and content hierarchy.
- [ ] **Headings are used in a consecutive order** 
	- Heading levels should be sequential. Don’t skip levels (i.e. `<h2>` to `<h4>`).
	- Nested headings are encouraged and natural as content goes from more general to specific.
	- In certain cases, headings may be visually hidden. Levels and visual styling may deviate from one another (i.e. giving an `<h2>` the same visual treatment of an `<h3>`). Please consult the a11y design team in this case.
- [ ] **Landmarks are used properly**
	- Page has only one main section and one footer section.  
	- Leave out landmark identifiers when giving a unique name. e.g., use "Repository" instead of "Repository navigation". This prevents redundancy in screen readers that already read out the navigation landmark.

### Suggested Tools
- [Page Region tutorial - W3C WAI](https://www.w3.org/WAI/tutorials/page-structure/regions/)
- [HeadingsMap browser extension](https://www.accessibility-developer-guide.com/setup/helper-tools/browser-extensions/headingsmap/) to check the hierarchy of an existing site.


---

## 3. Content

- [ ] **Links can be determined from their text alone** 
	- While there are programmatic options available, we recommend using them sparingly.
- [ ] **There are multiple (at least two) ways to access the navigation** 
	- Examples include: a list of related pages, table of contents, site map, site search, and a list of all available web pages.
- [ ] **Elements that present text or images of text have an accessible name that includes the visible text** 
	- Examples include labels, alternative `alt` text, `aria-label`, etc.
- [ ] **The language of the page and sections that use a different language on the page are identified** 
	- Identifying page language and multilingual sections enables text-to-speech pronunciation, screen reader functionality, and translation tools.
- [ ] **Cognitive function tests can be bypassed or have an alternate way to solve** 
	- Not all users can complete things like CAPTCHA puzzles, which excludes them from essential services. If required, provide accessible alternatives.

### Suggested Tools
- [Microsoft Edge’s Immersive Reader - Microsoft](https://support.microsoft.com/en-us/topic/use-immersive-reader-in-microsoft-edge-78a7a17d-52e1-47ee-b0ac-eff8539015e1)
- [MacOS’s Text to Speech - University of Calgary](https://www.ucalgary.ca/student-services/access/current-students/resources-and-supports/assistive-software-how-videos/mac-text-speech). Includes other speech to text resources as well!


---

## 4. Images, graphics, and other media

- [ ] **Ensure all images have alt-text** 
	- Decorative images should use `alt=""` for `<img>` (fill in for functional images) and `aria-hidden="true"` for `<svg>`.
- [ ] **Alternative media is included where applicable** 
	- Potential content includes captions, audio descriptions, transcripts, etc.
- [ ] **Automatically moving or scrolling content can be paused, stopped, and played**
	- Allowing users to control moving content prevents disorientation and motion sickness, which helps those with cognitive, reading, or vestibular disorders.
- [ ] **No page content [flashes](https://webaim.org/articles/seizure/) more than 3 times per second**
	- Limiting content flashes prevents seizures and discomfort for people  with photosensitive epilepsy, ensuring safe digital experiences for all  users.

### Exercises

- Figure out if an image needs a description using [W3C’s alt-text decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/).

### Resources

- [Alt Text Guide - GitHub Workplace Accessibility](https://github.com/github/workplace-accessibility/blob/main/resources/content-accessibility/alt-text-guide.md)
- [Your Image Is Probably Not Decorative - Smashing Magazine](https://www.smashingmagazine.com/2021/06/img-alt-attribute-alternate-description-decorative/)
- [Images Tutorial - Web Accessibility Initiative (W3C)](https://www.w3.org/WAI/tutorials/images/)
- [Functional Images - Web Accessibility Initiative (W3C)](https://www.w3.org/WAI/tutorials/images/functional/)
- [Dungeons & Dragons taught me how to write alt text - Eric Bailey](https://ericwbailey.website/published/dungeons-and-dragons-taught-me-how-to-write-alt-text/)


---

## 5. Interactivity

- [ ] **HTML semantics used over** `<span>` **or** `<div>` 
	- Use ARIA sparingly; most use cases can be covered by HTML or JS.
- [ ] **Content that is available on hover must also be available on focus**
	- Remember that links change navigation, and buttons initiate actions.
- [ ] **Non-essential multi-point or gesture-based interactions offer a single-point activation or accessible alternatives**
	- It may be hard or impossible for disabled users to perform certain gestures. Unless it’s essential, all functionality that uses a multi-point gesture, a path-based gesture, or a dragging movement must be operable using a single pointer gesture that is not path-based.
	- Functionality that relies on moving the device or user movement can be disabled and accessed through interactive elements
	- There is an alternative way to move objects beyond single-pointer drag and drop functionality 
- [ ] **Pointer input target sizes are at least 24 by 24 CSS pixels** 
	- Note that there are several exceptions to this rule under [SC 2.5.8](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html).
- [ ] **When a user focuses on an element or inputs information, the interface stays consistent** 
	- Do not make substantial or sudden changes to the page, open pop-up windows, or change keyboard focus without the user opting in.
- [ ] **If a page has a time limit, give user the ability to turn off, adjust, or extend that time limit** 
	- Exceptions to the rule are real time events (i.e. an auction) or when the time limit is beyond 20 hours.

### Resources
- [Link & Button Guidance - GitHub Accessibility Playbook](https://accessibility-playbook.github.com/link-and-button-guidance)
- [Links and Buttons Overview - University of Washington](https://www.washington.edu/accesstech/checklist/links-buttons/)
- [Getting To The Bottom Of Minimum WCAG-Conformant Interactive Element Size - Smashing Magazine](https://www.smashingmagazine.com/2024/07/getting-bottom-minimum-wcag-conformant-interactive-element-size/)
- [Foundations: pointer gestures - TetraLogical](https://tetralogical.com/blog/2023/03/17/foundations-pointer-gestures/)
- [Understanding Target Size Minimum (SC 2.5.8) - WCAG](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html)


---

## 6. Forms

- [ ] **Inputs have clear labels and instructions**
- [ ] **Legal, financial, or test data can be reversed, verified, or confirmed**
- [ ] **Errors are clearly identified with feedback given in a timely manner**
- [ ] **Avoid redundant entry by offering autocomplete or single select**

### Resources
- [Form Pattern Documentation - Primer](https://primer.style/product/ui-patterns/forms/)
- [Structuring Accessible Forms - Rachel DiTullio](https://racheleditullio.com/blog/2021/09/structuring-accessible-forms/)


---

## 7. Layout

- [ ] **Web content is not restricted to only portrait or landscape** 
	- Does your design work as intended for a mobile screen as well as desktop?
- [ ] **A link to skipping repeated navigation across app or website is provided**
- [ ] **Navigation, information elements such as search, and help centers such as contact us are placed and labeled in a consistent way**
- [ ] **Each page has a descriptive and informative page title**
- [ ] **Pages are readable and functional when the page is zoomed from 50-400%** 
	- Is any content overlapped or obscured? 
- [ ] **No loss of content or functionality when user adapts paragraph spacing** 
	- Specifically, up to 2 times the font size, text line height/spacing to 1.5 times the font size, word spacing to 0.16 times the font size, and letter spacing to 0.12 times the font size.


---

## 8. Keyboard

- [ ] **All interactive elements must be keyboard navigable** 
	- This includes content on hover. Using <kbd>Tab</kbd>, <kbd>Shift+Tab</kbd>, <kbd>Space</kbd>, <kbd>Enter</kbd>, and <kbd>Esc</kbd> is a good start.
- [ ] **Meaningful sequence is logical and intuitive**
	- Remember that navigation and reading order is done by code order in the DOM.
- [ ] **There are no keyboard traps or points where keyboard focus falls to the background**
	- Double check your dialogs!
- [ ] **When elements receive keyboard focus, there is a focus order not obscured by content**
- [ ] **Check that keyboard shortcuts do not coincide with browser and/or assistive technology shortcuts**


---

## Additional Resources

- [ ] **Run a scan on your code** 
	- We recommend starting with free axe-tools, although beware that automated scans are NOT full-proof. A great example of this is [Building the most inaccessible site possible with a perfect Lighthouse score](https://www.matuzo.at/blog/building-the-most-inaccessible-site-possible-with-a-perfect-lighthouse-score/).
- [ ] **Consider adding accessibility linters and actions to your CI/CD pipeline** 
	- Adding accessibility tools into your code process is a great way to work on accessibility together.

## Suggested Tools

- [Free accessibility browser tools - Deque](https://www.deque.com/axe/browser-extensions/)
- [Alt-text bot - GitHub](https://github.com/github/accessibility-alt-text-bot)
