# GDI HTML Slides Template

<!-- TOC start -->

- [GDI HTML Slides Template](#gdi-html-slides-template)
  - [Usage Instructions](#usage-instructions)
  - [Examples](#examples)
  - [Course Creation Tips](#course-creation-tips)
  - [Slide Markup](#slide-markup)
    <!-- TOC end -->
    <!-- TOC --><a name="gdi-html-slides-template"></a>

---

**Girl Develop It** uses a customized HTML slide template for its open-source course content.

Our slides are powered by [Reveal.js](https://revealjs.com/), the popular HTML presentation framework. For simplicity and ease of use, the Reveal.js files are served via CDN.

The template files reference a shared **`assets`** folder in the repo that contains the following folders:

- `css` - Contains the `gdi-theme.css`
- `imgs` - Contains GDI logo files and shared stock images
- `fonts` - Contains GDI's primary fonts `Gotham`, `League Gothic` and `Source Sans Pro`

:exclamation: DO NOT ADD MATERIAL TO THE **`assets`** FOLDER.:exclamation:

:exclamation: If you're using new images and/or custom CSS for your course, create a course-specific `images` folder and/or `style.css` file, and place them in the course folder.

---

## Usage Instructions

- To create a new course, duplicate the `_course-template` folder
  <br/>

- Rename the duplicate folder with your course title
  <br/>

- Review `demo-gdi-slides.html` for common and recommended ways we use Reveal.js features

  - Copy or model the demo slides and code snippets as needed
  - Preserve (rather than delete) the `demo-gdi-slides.html` for future reference
    <br/>

- To build content for a course with a single class, duplicate the `template_index.html` file and make the following edits:

  - Rename the file to `index.html`
  - Make updates as outlined in the file's instructions, for example:
    - Update course name in the `<title>` tag
    - Update course name in the `<footer>` tag
    - etc.
  - Create course slides - (Instructions are included in template file - See also [Slide Markup](#slide-markup) below)
    <br/>

- To build content for a course with more than one class / session -- also known as a **mini-cohort** _[2-3 classes]_ or a **cohort** _[4-6 classes]_:

  - Clone `template_cohort-index.html`
  - Rename to `index.html`; it serves as a cover page that links to all classes in the cohort
  - Clone `template_index.html` to create subsequent class files: `class1.html`, `class2.html`, etc.
    - OPTIONAL: Create an `intro.html` file for instructor and course introduction
  - Create course slides - Make updates as outlined in the file's instructions
    <br/>

- If using new images for your slides, create an `images` folder in your course folder

  - :exclamation: Do not add images to the shared or main `assets` folder
  - :bulb: Include credit /attribution to image(s) when possible
  - :bulb: Optimize images to reduce file size - Use an image compression tool such as tinypng.com
    <br/>

- Need or want to use custom CSS? Create a `style.css` file in your course folder and your custom code there

  - :exclamation: Do not add custom css to the shared or main `gdi-theme.css` file
  - Link the custom stylesheet to your course `html` file(s)
    <br/>

- _CHANGELOG - Description coming..._
  <br>

- **Recommended**: Update this `README` (delete original content first) with any of the following that can help future instructors teaching the course:

  - Course goals and objectives
  - Course outline or structure
  - Teaching tips
  - Suggested exercises
  - Resources
  - etc.

- **Optional**:
  - Create a `demos` and/or `exercises` folders
  - Create a `resources.html` file to curate recommended resources, links, etc cited in the course

## Examples

Cohort course folder structure:

- [CSS Grids Basic](https://github.com/girldevelopit/gdi-html-css/tree/main/css-grid-basics)

Single-class course folder structure:

- Intro to JavaScript (_Update in progress_)

## Course Creation Tips

- Use unstacked slides (rather than nested slides) for better readability

- Limit the amount of content on each slide

  - An image, a sentence, or a short code sample is more understandable than a long list of bullet points
  - Or split long text content into two slides

- Lean more towards visual content (images, gifs, videos) to support learning concepts

- To make the course curriculum useful/helpful for future instructors to use:

  - Add "teachers' notes" such as FAQs, class management tips/best practices to the course `README.md`
  - Add a `demos` and/or `exercises` folder to store exercises you've used or recommend for future classes

## Slide Markup

Markup heirarchy needs to be `<div class="reveal"> <div class="slides"> <section>` where the `<section>` represents one slide and can be repeated indefinitely.

```html
<div class="reveal">
  <div class="slides">
    <section>Slide 1</section>
    <section>Slide 2</section>
    <section>Slide 3</section>
  </div>
</div>
```
