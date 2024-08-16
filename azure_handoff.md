# Introduction

In the chemiSOLO project, I implemented four main components: the Nav Bar, Home Screen, Imaging Parameters, and Gallery. Below, I provide a detailed explanation of each implementation. My focus was primarily on the frontend, with limited time spent on backend integration.

## Pre-Implementation
To prevent my local server from being stuck in an infinite loading loop, I commented out certain code sections (refer to section 6 in the [onboarding information](https://github.com/oliviaxjiang/azurebiosystems_chemiSOLO-onboarding) for details).

## Nav Bar
The Nav Bar was customized primarily within `components/Layout.vue`, with minor adjustments in `App.vue`. In `Layout.vue`, I removed the `HeaderNav` component, as it was no longer needed, and added custom CSS directly in the file. New components included the top logo (since `HeaderNav` was no longer referenced) and version information at the bottom.

Note: Since the Nav Bar occupies the left side of the screen, shifting everything else to the right, I encountered difficulty centering the right-side components. As a temporary solution, I added padding through a CSS class named `test` in `App.vue` (see line 3 in `App.vue` and lines 4280-4282 in `style/styles.css`).

## Home
To align with the new design, I removed much of the selection-related code that was previously in `Home/Chemiluminscent.vue` and `Home/VisibleImaging.vue`.

For improved testing, I modified the navigation in `Home/index.vue`, linking my new implementations of Imaging Parameters and Gallery View to the Chemiluminescence Imaging and Visible Imaging buttons.

## Imaging Parameters
I created `ChemiluminescenceForm.vue` to accommodate the new design for Imaging Parameters, implementing both the left-side forms and the right-side auto-save button.

This form has not yet been connected to the backend, which is a next step. I attempted to link this page to the image capture functionality (see line 140 in the file).

All CSS styles are embedded within the Vue file itself.

## Gallery
I implemented the basic structure and style of the new gallery page design in a new file, `GalleryView.vue`. All associated CSS styles are included within the Vue file.

## Additional Changes

### Navigation
I added routes in `src/router/index.js` to the new Imaging Parameters and Gallery screens (see lines 84-96 in the file).

### Onboarding Documentation
I also wrote an onboarding document compiling instructions, potential challenges, and solutions for navigating the codebase. See the [onboarding information](https://github.com/oliviaxjiang/azurebiosystems_chemiSOLO-onboarding) for details.
