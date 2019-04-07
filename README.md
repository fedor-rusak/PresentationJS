# PresentationJS

[![license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Simple one-page HTML/CSS/JS approach to make slides-based interactive documents.

## Hot to use

Just open [PresentationJS.html](PresentationJS.html) in your browser to see something like slide with top menu!

## Problem

Some information can be captured as a series of diagrams, words, images i.e. to simplify knowledge sharing or collaboration.

While your particular situation may require custom functionality, most proprietary solutions may lack extensibility/alternative for desired feature. For example you want ti integrate some programmince code evaluation right into your slide.

How to describe presentation-like document to inspire collaboration, experimentation and easy way of sharing it?

## Proposed solution

Nothing beats web-page without dependencies as a convenient way to show and share documents. You know about internet, right?

But to make such page we would need some steps:

1. prepare presentation scenario (know your audience, domain, purpose)
2. codify slides in JSON
2. tweak visual design properties (typography, colors, sizes)
4. visualize your first JSON slide data with chosen style (JS, HTML5, CSS, DOM)
5. add some interactivity to move between slides (JS)
6. PROFIT!

Actually understanding intent of your presentation is more important than presentation itself. What idea you want to share and who are the people you want to share it with?

I assume you are developer or at least JSON does not scare you away. So you will modify default inputData JSON value to describe slides you want.

Visual design parts are just CSS and if you need some starting point you can check [LearnLayout.com](http://learnlayout.com/).

Visualizing with DOM, JS can be quite a pain so this part is neatly packaged inside separate stateless module with minimalistic API.

Interactivity and event listener part is sort of hard. You should track events, state, and call API for modifying visualization. But if you really want to get some fun features you can't avoid this coding part.

## How to use

1. Copy [PresentationJS.html](PresentationJS.html) file to your local machine.
2. Modify inputData variable.
3. Reload browser to check results.
4. Modify other parts (JS, HTML, JSON) content as you wish.
5. Get back to step 3 before you are satisfied.

## Technical decisions

Usually presentation shows only predefined slide content on you whole screen. But I consider presentation to be more of a collaboration format so some information must be added.

What is the title of presentation? Can it be summarized in one-two words? Like default presentation is about PresentationJS itself and you would always see it left top corner.

If you describe topic with 30 slides, would it make sense to divide it in some sections/chapters|whatever. I do think it may be useful to show what is a specific idea behind certain group of slides. And for sure it depends on your audince and intent. Default presentation definitely uses this approach.

Your slide is just some html markup, content and styles. So there are many ways to get to the goal. In my approach I decided to you some absolute positioning for div elements to control layout of slide content. It can be SVG, it be some more responsive layout but it is beyond minimal simple presentation document.

## History

### 0.1
 - documentation improved
 - static HTML/CSS part of PresentationJS implemented