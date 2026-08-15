---
layout: ../../layouts/MarkdownPostLayout.astro
title: 'First Blog Post'
pubDate: 2026-08-15
description: 'This is a test post aroind which to style and test stuff.'
author: 'Toby Eglesfield'
image:
    url: 'https://docs.astro.build/assets/rose.webp'
    alt: 'The Astro logo on a dark background with a pink glow.'
tags: ["blogging", "making-a-blog"]
---

Hello,
This is my first blog post. I'll be using this as part of my process of documenting my progress with an eye on making a tutorial from it. So far I've set up some of the basics. The Astro tutorial was really great but I'm stripping things back just a little. The tutorial shows non-framework approaches, and then replaces the duplicated elements of that with components. For my approach I'm going to skip the steps where the non-framework parts are added and then removed, instead going straight to the component based stucture. I had to think a little about how I'd achieve that. The order so far has been informed by that thinking and at this point I've got up having a basic page laoyout with a header and footer component. The header component contains a navigation component. This basic page layout itself is a layout component. So far, it's used by the only page, which is the index(home page). 

Next up I'm creating this blog post within an md file, which can be brought into a new page layout, whcih i'll create after this. I made a diagram to help me with how the data flows work - the key piece in there is having a page add additional content into the page layout, which will appear in position of the page layout's slot. The diagram shows the flow with the example of the index page being the sole page, and the following: Page layout is imported into the index page, then the index page uses the page layout html tags to add an h2 to the page layout - this is then sent to the page layout, which then goes to render. The diagram needs verification but it includes the aspect of the page layout being the last port of call for data before it renders the final page to the browser.
