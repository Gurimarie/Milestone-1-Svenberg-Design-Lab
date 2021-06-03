# SVENBERG DESIGN LAB
## Code Institute - Milestone Project 1
This website has been designed to showcase the work of Svenberg Design Lab, and to be a place for prospective customers and collabortors to explore the previous work of the company.
The target audience consists of two groups; the private customer who has a design-wish to be fulfulled, and the professional customer looking for a design-company for collaboration.

![Picture of different view-port-displays]()

Click here to view the website

## User Experience (UX)

### User stories:

### First time visitor goals
To find information about a company I'm curious about. To see their projects and their style. To confirm the quality and trustworthyness of the company.

### Returning visitor goals
To be able to find the project I'm looking for quicly. Perhaps look at different projects and different design-areas than on my first visit. Get a feel for the company as a whole.

### Frequent user goals
To be able to find the project I'm looking for quicly, and to be able to see all projects in each design-area on one page, in order to compare and find what is interesting.

### Site owner goals
To show prospective customers and partners what we do, our style and our high quality. As we work in several different design-areas, it is important that the visitor understands that they are at the right company-site regardless of what area they first have come in contact with. Therefore the different ares must be shown as equals, and not (for instance) primarily interior-design, and the other areas as additions. 
Another important reason behind the site is simply to collect and showcase previous project in one coherent space. 

## Design

### Colour scheme:

### Typography:
Font Poppins for headlines and Open Sans for other text.  
<br>
Poppins is a straight-forward, easily-approachable font, that is both elegant and simple, and that has rounded shapes that makes it feel trustworthy. We want a font that is elegant, but not old-fashioned, and not too avant-guard. Poppins is just the right mix.  
<br>
Open Sans works well with Poppins, as it has much of the same overall feeling, a simple, nicely spaced look (not too narrow), and with lovely old-fashioned g's that gives it a nice, comforting feeling.

![Picture of sample Poppins and Open Sans](assets/images/readme-images/fonts-poppins-and-open-sans.JPG)

### Imagery:


## Wireframes



## Features

- Need "Sorry, page not working, click here to go back" for when form on contact-page is submitted, and the action-page does not exist.
- Need "I'm working on it" for when form on contact-page is submitted
- Need perhaps also "I'm working on it" for when a nav-button is clicked?
- Click "out of" nav-hamburger without selecting anything (now it stays open until you select a link)
- Add a video- or audio-file somewhere (required)
- Fix images, good quality, but as small and easy-loadable as possible




#### Future features:
- Feedback from previous customers
- Search-button with the possibility to search for keywords within the website.

## Issues overcome


## Technology used
### Programming languages:
- html
- css
- Bootstrap (JavaScript?)

### Frameworks, libraries and programs:
- Bootstrap
- Google Fonts
- Font-awsome

## Testing

### Validation:

### Testing for user stories in UX-section:

### Further testing:

### Fixed bugs:

#### Navbar dropdown-issues
![Picture of nav-bar with nav-items not nested](assets/images/readme-images/problem-undercategories-dropdown-menu.JPG)

- Nav-dropdown part 1: No drop-down-list under each design-heading in nav-bar.
- Fix: Made correction from "data-toggle" to "data-bs-toggle" as an attribute of the a-element that is the parent of the nested list, and the sublists now function. Has been fixed with info from https://getbootstrap.com/docs/5.0/components/navbar/
- Addition: The bootstrap-docs use ul-element and li-elements also in the nested lists (here under Fashion Design, Interior Design etc.) but it seems to work fine with ul-element and li-elements for the main nav-bar-list and just div (class: dropdown-menu) + a (class: dropdown-item) in the sublist. At first I kept fashion and interior with ul/li, and product and art with div/a, and it did seem to work both ways, but I decided to go with ul/li in all sub-lists as well, as it seems more orderly and more semantically correct. 

- Nav-dropdown part 2: Each design-heading shows up separately in the nav-bar, instead of as categories in a dropdown-menu under Design-areas.
- Fix: Partially fixed through trial-and-error by comparisons with previously used nav-dropdowns and nested lists in the course-material, and with searches on nav-elements and lists in the Bootstrap-documentation. I finally simplified the whole nested list to the bare minimum, and started to work my way up. The nested list is now in order, but it does not collaps, so that will be part 3 of this navbar-dropdown-fixing.

![Picture of nav-bar with nav-items not nested](assets/images/readme-images/nav-dropdown-doesnt-collapse.JPG)

- Nav-dropdown part 3: After the fix part 2, the dropdown-menu is now situated under the Design-areas-nav-heading, but it does not collapse.
- Fix: I went back through the bootstrap-documentation from Nav-dropdown-bug part 1 (https://getbootstrap.com/docs/5.0/components/navbar/), and after correcting some missing dropdown-classes and adding id to the top category, the nav-dropdown now is loaded in as it should be, with the top subject (Design-areas) on the nav-bar, and a dropdown-menu.

![Picture og white dropdown with invisible tekst](assets/images/readme-images/dropdown-white-bg-white-text.JPG)
- Nav-dropdown part 4: The dropdown-box has white background, and the text is white (because of dark nav-bar), so the text is invisible.
- Fix: Simply add class .dropdown-menu-dark to the ul that holds the dropdown-menu. I found the information here: https://getbootstrap.com/docs/5.0/components/dropdowns/#dark-dropdowns

- Nav-dropdown part 5: The categories in the nav-dropdown do not collapse. Ideally the dropdown should open with only the 4 design-areas visible, and the sub-categories should only be visible after clicking the dropdown-toggle. 
- Fix: Finally solved mainly with two css-rules with help from https://bootstrap-menu.com/detail-multilevel.html! Hiding the subcategories until the mouse hovers over the parent-category, and then displaying them on the side, so as to not cover or hide other the parent-list. The ul-elements of the sub-lists also needed the addition of the attribute aria-labelled-by the id of their parent-category and all the classes that the ul-elements of the main-list had, pluss an additional class sub-dropdown, that is used to aim the css-rules.
![Picture of nav-dropdown with sub-categories on the sade while hovering over parent](assets/images/readme-images/nav-dropdown-fixed.JPG)

#### Alignment-issues
![Picture of inline-boxes not in alignment](assets/images/readme-images/alignment-problem-inline-boxes.JPG)
 - Alignment-problem with inline-blocks on frontpage (the 4 design-areas).
 - Fix: I gave the surrounding div-container the class of "d-flex", to use the bootstrap flex-box-classes to align and evenly distribute the inline-boxes. I found information about this on: https://getbootstrap.com/docs/5.0/utilities/flex/". It worked so well, so I also used it for the footer.

 ![Picture of white space on the right side of web-page](assets/images/readme-images/white-space-on-right-side.JPG)
 - Problem with white space (the div's not streaching over the full viewport-area). 
 - Fix: I previously had div-elements with container-fluid-class and thought that should stretch the whole way, but looking at the "Whiskey-drop"-project I saw row and col-12 used for that purpose, so with a little bit of experimenting, I found the right combination. 




### Unfixed bugs:

- Nav-dropdown part 5: The Nav-drop-down is again not working. Not dropping down at all. Need to go through old commits, and see when it last worked, and what has been changed afterwards.

 - Problem: The footer is migrating up on the page when there is not enough content to push it down.
 - Fix: adding a margin-top of -50px and ............? Need more work...
 I found the info here: https://css-tricks.com/couple-takes-sticky-footer/


- There is still a question regarding the categories in the nav-dropdown, regarding the fact that both the 4 main-categories and the sub-categories are links to other pages. As the other pages are not yet 

- The inline-blocks on the frontpage (the 4 design-areas) align nicely now on larger displays with the d-flex-class on the parent-container, but they do not adjust well to smaller displays. More work required.

## Deployment

### Github pages:

### Forking the GitHub repository:

### Making a local clone:


## Credits

### Code:

- https://github.com/PaulFrankling/discover-north-yorks used for README-structure.
- Code Institute courses for everything

### Content:

### Media used:

### Acknowledgements:




