# Lab 1 README
### Jacob Sandling
### RCSID: sandlj
### GitHub: jbsandling

## Reflection and Thoughts
This lab was a good way to get back into designing webpages with just HTML and CSS. I worked on a couple projects this summer using React and NextJs, and I clearly got a little to comfortable relying on more powerful tools and external libaraies to handle lots of the construction and styling, so this was a good exercise to get used to the basics again. All in all it was pretty straightforward. One thing that was interesting was the research I did to meet the 5 extra HTML and CSS items requirement, as it forced me to not only look for new tools I wasn't familiar with, but also helped me to focus on the semantic side of HTML (not just div's everywhere), which is something I always knew was out there, but just hadn't looked into enough. I had a similar experience on the CSS side, where some CSS rules, like scroll-behavior, really seem like something that would require Javascript or at least a larger CSS library, but are readily available if you look for them. As I used these new tags and rules I learned their requirements and quirks through equal parts documenation, trial and error, and validation checks, which is pretty much my standard process, although ever since programming in C and relying on the man pages I have newfound appreciation for good documentation. Looking at more of the sematic tags also tied well into the portion of the lab on microformats, as both are embedding more easily machine-readable aspects into your code. Another consideration I had was that if all of our pages were supposed to be based on the same stylesheet, that all of us individually creating personal pages and writing css classes and ids might cause some overlap and to try to combat this I labeled all my CSS identifiers as "j_name". Another interesting thing I learned (from source 8) is that one of my old favorite tricks, an anchor that opens a new tab, actually comes with some security concerns related to phishing or tabnabbing, so that's definitely something to watch out for going forward.

## 5 New HTML5 Tags
As a preface, I found several of these tags from looking through w3Schools' list of tags (source 1), as well as Ken Bellow's article on semantic HTML (source 2). 
1. `<section>`
    Section is a semantic tag that denotes different sections of a document. While this seems pretty basic, it seems to be a much more descriptive way of organizing content than a bunch of stacked divs. I a section as the container for each "section" of my page (i.e. Introduction, Education, ...)
2. `<nav>`
    Nav is another semantic tag that gives more description to a pile of anchor tags, making these assorted links into a defined navigation menu. Once again, while it seems to serve the same purpose as a div around anchors to an outsider, it is far more descriptive. I used the nav tag for the links in my page's header
3. `<details>`
    The details tag works in conjunction with the `<summary>` tag discussed next. Together they create a system of dropdowns, where summaries serve as the heading for the dropdown, and details contains the summary as well as all of the hidden information. I chose to user details for my education section because I wanted to highlight my experience at RPI (which I set to "open" by default), because I'm not sure that high school is super relevant to clients and recruiters.
4. `<summary>`
    As alluded to above, summary serves as the header for a details element, the content that is always visible. In my case, this was the name of each school and the dates attended. One validation issue I ran into here is that you can't include spans or divs inside of a summary, so you may have to approach styling slightly differently.
5.  `<abbr>`
    The abbr tag is for abbreviations or acronyms, and it will display the full name of an acronym when the acronym is hovered over. This just makes the page more readable, allowing me to not have to type out every acronym every time, but allowing viewers not familiar with what I'm refering to to get clarification. 

## 5 New CSS3 Rules
1. `*:not()`
    This *:not() syntax allows you to define attributes that apply to all objects except those epcified in the not() clause. This is a super handy trick I wish I knew previously, as it allows you to apply a change to large parts of the page without copying tons of CSS code. I used this to apply padding to the content of my sections, while allowing the headings to remain without padding so they stood out better, and made the sections more distinguishable.
2. `text-decorator`
    I have always disliked the default look of HTML anchor tags, something about the blue underlined text feels so "old-internet". Making buttons is always an option, but doesn't always fit in your design, so this tag, the text-decorator, can help with that, by adding a couple stylistic changes. I used this to remove the underline from anchor tags, and only add an underline when a viewer is hovering over the link, creating the illusion of a more dynamic webpage.
3. `opacity`
    This is an attibute that I always knew existed, but had never really used before. It is pretty simple, it makes the object, in my case a series of icons, more or less visible by adjusting opacity. I used this to create 50% opaque Email, GitHub, and LinkedIn icons in my footer, set to increase to 100% opacity when a viewer hovered over them. This just draws the viewers attention to what they have selected, but it does this in a really easy-to-implement way.
4. `background-attachment`
    This property is used to lock the background image in place. Since I am not great with design, I have made a couple pages with image backgrounds (like my portfolio), but too often when you scroll you find seams in the images that are distracting and unprofessional. With this tag, the background image is locked in place, so when you scroll, it stays staic, which prevents these hiccups and image issues.
5. `scroll-behavior`
    This is another tag that just makes the page feel more dynamic to a user. What it does is when you click on a link to another part of the page, it will cause your browser to scroll smoothly to that point rather than the default jumpiness. I did have some issues getting this to work, as I could only get the effect to happen when it was applied to `html{...}`, which might not be ideal if all of your pages didn't need this styling.

## Sources Used:
1. https://www.w3schools.com/tags/ref_byfunc.asp
2. https://dev.to/kenbellows/stop-using-so-many-divs-an-intro-to-semantic-html-3i9i (Written by an RPI Alum, that's cool!)
3. https://www.w3docs.com/snippets/html/how-to-create-an-anchor-link-to-jump-to-a-specific-part-of-a-page.html
4. https://css-tricks.com/how-to-create-a-shrinking-header-on-scroll-without-javascript/
5. https://css-tricks.com/lets-look-50-interesting-css-properties-values/
6. http://microformats.org/wiki/hcard#note2
7. https://css-tricks.com/almanac/properties/s/scroll-behavior/
8. https://www.freecodecamp.org/news/how-to-use-html-to-open-link-in-new-tab/
9. https://www.w3schools.com/howto/howto_css_equal_height.asp (For columns on the group page)