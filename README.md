# Fall 2022 Vue Content

## List Rendering

### Key Information

- create a list in a div that could be cut out of the page
- add text grouped in 2 tags inside each `<li></li>` (do 3)
  - text should be static
- recreate the text in an array (only use 1 item from each list element)
- Loop through that array with a v-for

### Arrays of Objects

- Turn your simple array into an array of objects
  - have 2 key-value pairs in it
- Loop through the array
- use the key in your moustache syntax with the iterator term to render each
  value

### Componentize

- create list component
  - add content and logic to it
  - set up props
  - make sure props text is the same as text in the template
- Import component to page
  - pass array to component with a v-bind (names of things are important here)

---

### What we need to be able to do

- Render a list of strings
- Control formatting in each list item
- render nested arrays <-- where our design is currently not optimized
  - render objects

#### Solution for a flexible list component

- [ x ] Conditional statement to render an array if it's passed one -> simple
  flat arrays
  - used `v-if=list !=''"`
- [ x ]if no array passed, then use a slot and control output more specifically
  - used `v-else`
- [ x ] AppList Component handles styles and general layout, renders content if
  array is passed
  - AppListItem is redundant, delete or use for something else (maybe
    FooterListItem and use AppLink inside)
- [ x ] AppListItemKv to handle key/value pair content

### Step by Step for Hardened/Versatile List Component

1. AppList gets a if/else logic to handle default vs non default layout
2. Create AppListItem to specifically handle the key value pair layout
3. On Home page wrap the AppListItem in AppList (this gives the ul layout and
   css formatting)
4. Put a v-for loop on the AppListItem to iterate through the array of objects
5. bind the key value pair values to the AppListItem

---

## Intro

We will use this repo and a set of branches for the first steps of learning
VueJS and the basics of javascript frameworks.

Go to the bottom of this file for Eslint and Prettier Information

## Branches

- main branch:
  - Most boiler plate code removed
  - Tailwind Added
- utils branch:
  - prettier and eslint configured for a minimally intrusive but helpful
    workflow
- develop branch:
  - based on utils, where we will work on code in class

## Purpose of this Repo

- To store our in class examples
- To provide a place to explore and experiment

## Notes

Keep in mind that in this repo we are using [Vue](https://vuejs.org). Later we
will switch to [NuxtJS](https://v3.nuxtjs.org) which is built around Vue. Nuxt
automates a lot of things that we do manually in Vue.

Remember to check the [Vue Docs](https://vuejs.org/guide/introduction.html) when
you run into difficulties.

---

## Eslint and Prettier

- [This guide will be enough to get you going](https://vueschool.io/articles/vuejs-tutorials/eslint-and-prettier-with-vite-and-vue-js-3/)
- [This will help you set up the tailwind prettier plugin](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier)
- Note the .json config files and the .ignore files used for eslint and prettier
- If it's not autoformatting, check
  [these settings](https://i.stack.imgur.com/DINkP.png) and make sure to
  configure the default formatter
