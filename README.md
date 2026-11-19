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

    Motion was the only element that was implemented in the website via a hover state when hovering the cursor over the card elements (like the project and social cards).