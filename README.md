Accessibility Conformance and Inclusive Quality Build Analyzation

Test Scope:

    The following pages will be tested for this analyzation:
            - Home Page
                - Contains essentially all of your major component types, including responsive hero and project images.
            - Projects Page
                - Isolates the project-card interaction pattern.
            - Contacts Page
                - Provides a different interaction pattern through LinkedIn, Behance, GitHub, and email links.

Semantic Structure

    Checking the structure of each webpage, they follow the traditional order, which is:

            - <header>
            - <nav>
            - <main>
            - <section>
            - <article>
            - <footer>


    After retesting for mistakes or accessibility problems:

    The landmarks for each page are also logically placed so that it can seperate each area.

    Along with this each page has unique titles, like "Aaron Lopez - Porfolio", "Aaron Lopez - Projects", and "Aaron Lopez - Contact". 

    Headings are appropiately used, as <h1>, <h2>, and <h3> are placed in logical order in terms of importance, as observed in the code.

    Links are appropriately used for navigation, project cards, social-media profiles, and email contact. Each of the link text that was created cleary communicates where each link goes.

    Buttons for the navigation and for the project/social cards are easily identifiable in terms of either doing an action or navigation. 

    Accessible text like image alt text and link are appropriately named to be distinguishable from each other, with link names like "project-cloud-cafe" and "project-nani". For alt names, an example includes "alt="Portrait of Aaron Lopez"


Keyboard and Focus

There is a visible keyboard focus state in the CSS: 

    :focus-visible {
    outline: solid rgb(2, 157, 230) 2px;
    outline-offset: 4px;
}

 Pressng the Tab key within the pages correctly focuses on each interactable element. A blue outline is used as the focus to make it more noticable. Besides this, the following was also tested:

    -Shift + Tab backwards.
    -Enter activates links.
    -Every project card can be activated without a mouse.
    -Social cards can be activated without a mouse.
    -Focus never becomes trapped.
    -aria-current="page" accurately represents the current page.


Zoom, Reflow, Text Spacing, and Contrast

    At 200% zoom, objects will get bigger but can still be read normally. Along with this, the site will also respond to smaller viewports by doing a narrow reflow, which will stack elements on top of each other to remove the potential of horizontal scrolling. 

    Text spacing for all of the text remains visible and organized, even when the viewport shrinks. However, the skills list still needs to be optimized for smaller viewports as it will grow longer horizontally. 

   Based on the colors in the current CSS, the site's main text contrast is strong. The chosen palette defines the primary red as #9E1C19, dark text as #1A1A1A, light card text as #F2F2F2, and the dark secondary background as #363131. Each piece of text in the different sections is either black or white to keep maxiumum visibility. Anything other color would be a risk.

Forms and Tables

    Forms: N/A. The current capstone does not contain form controls, so labels, instructions, validation errors, and required states are not applicable.

    Tables: N/A. The current capstone does not contain data tables, so captions, header cells, scope, and responsive-table strategies are not applicable.

    Reasoning: There are no current plans to implement a table or form into the portfolio as there will be no data or datasets involved in my projects. As for forms, I want to keep things a little more visual and simple, however my email is there in case someone wants to ask me a question.

Media, Motion, and Alternatives

    Motion was the only element that was implemented in the website via a hover state when hovering the cursor over the card elements (like the project and social cards). While this is a simple animation, a @media (prefers-reduced-motion: reduce) media query was applied just in case if the animation triggers a response in individuals who might be sensitive to increased motion.

    Alt text, as mentioned before, have been reviewed based on their purpose and includes appropriate wording.  

    The website does not currently use SVGs, audio, video, or embedded media, so labels, captions, transcripts, and embed titles are not applicable.

Automated and Manual Evidence

    For this section, I used Lighthouse for each page. Here are the results for each one:

           Home:
                -Performance: 95
                -Accessibility: 100
                -Best Practices: 96
                -SEO: 100  
           
            Projects:
                -Performance: 93
                -Accessibility: 98
                -Best Practices: 96
                -SEO: 100 
           
            Contact: 
                -Performance: 99
                -Accessibility: 98
                -Best Practices: 96
                -SEO: 100 

    Manual Evidence:

         Keyboard-only walkthrough: Navigated all three pages using Tab, Shift+Tab, and Enter.

         Browser stress test: Tested 200% zoom, narrow reflow, and increased text spacing; findings listed in "Zoom, Reflow, Text Spacing, and Contrast".  

         Semantic/visual review: Manually inspected heading order, landmarks, link purpose, alternative text, responsive behavior, and visible states.   

Screen Reader / Accessibility-Tree Sampling

        Screen-reader testing was performed on the website to check whether navigation links, headings, images, project links, and other important content were announced clearly and in a logical order. The test was used to identify elements that were missing or had unclear accessible names and to verify that the current page could be understood without relying only on visual information. The results show that everything was able to be read by the screen reader. Something to note was that the img and the link have a similar title, making the narration from the screen reader a little redundant (if that makese sense).

   

Remediation Log will be in a PDF


Conformance Summary
    
        Overall the portfolio seems to be ticking most of the boxes in terms of accessibility as far as the testing has done. It uses semantic HTML landmarks, appropriate page titles, logical heading structure, responsive design, visible keyboard focus, current page indicators, alt text on images, and has reduced motion. We've looked at the keyboard navigation, zoom, reflow, text spacing, contrast and screen reader behaviour across the Home, Projects and Contact pages.

        Several accessibility issues were found and fixed during testing (generic page titles, missing page level headings, a number of unnecessary keyboard focus stops due to tabindex, inaccurate alt text). Navigation was given an accessible name. The remaining items that should be checked prior to final release are that the project card overlay behaves in an equivalent way during keyboard focus and that the mailto on the Contact page is corrected to match the email address that is displayed.

        Forms, tables, audio, video, SVGs and embedded media are not used in this version of the accessibility review and so were not relevant. Prior to final release the site should be subjected to one final automated accessibility check and then one final manual review (keyboard, 200% zoom/reflow, contrast, reduced motion and screen reader) to ensure that the remaining fixes are all working correctly and that no new accessibility issues have been introduced.
    
AI Disclosure

        AI was used to scan the intial pages to see what issues it could find on each page. While it did figure out a couple of issues, it was up to me to verify the issues myself. When I found each issue, with the help of what the AI found, I 