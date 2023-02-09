# Astro - Build A Blog

The tutorial from [Astro's website](https://docs.astro.build/en/tutorial/0-introduction/).

## Demo

[Live Site](https://adieastroblog.netlify.app/)


## What Did I Learn❓❓❓

### What's an Astro?

- Astro is a JavaScript framework (make room! make room!) made for static, 'content rich' MPA such as blogs, marketing sites, documentation sites to name a few.
- Version 2 was released in Jan 2023, so it's very shiny and new (at time of typing).
- They claim "Astro 2.0 is the first major web framework to deliver complete type-safety for Markdown and MDX."
- It seems to have many similarities to Next.js but has more of a focus on 'content' compared to the web application focus of Next.js. So if you want to make fancy things like chat apps, todo lists (never heard of them) or The New Facebook, Astro isn't for you.
- If you're comfortable with HTML, CSS, JavaScript or TypeScript, Astro should fit like a warm glove.
- Astro is for MPA with SSR.
- It supports many UI frameworks like React, Svelte, Vue to render component 'islands' and you can even mix and match different frameworks, if you're feeling fruity.

That's just a few cool things.

### What Does the Tutorial Teach You?

- The Astro setup wizard (`npm create astro@latest`) asks if you'd like to use TS and at what strictness, which is nice.
- Links use the good old `<a href ...>` format.
- It uses file-based routing. Each file in your src/pages/ directory becomes an endpoint on your site based on its file path.
- It has in-build markdown support.
- You can create layouts to re-use common `<body>` and `<head>` tags for example.
```javascript
<MySiteLayout>
  <p>My page content, wrapped in a layout!</p>
</MySiteLayout>
```
- Data at the top of MD files inside code fences is called **frontmatter** and is in **YAML** format.
- Astro's templating is similar to JSX syntax.
- You can set global CSS styles are also have `<style>` blocks in individual pages or components. With conflicting styles, the local rule overrides the global one.
- Props - yes, it has those too, using Astro.props. Eg. `const { platform, username } = Astro.props`
- You can use `<script>` tags directly or link to an external JS file, if vanilla JS is your jam. This was used in the tut to make the hamburger menu clickable.
- An Astro `<slot>` appears to be another name for 'children'.
- You can access data using `Astro.glob()`, eg. `const allPosts = await Astro.glob('../pages/posts/*.md')` which is this case returns an array of of blog post objects.
- The function `getStaticPaths()` is used for dynamic page routing and in the tut is used to return an array of page routes based on the tags of the blog posts.
- There's an Astro package to create RSS feeds - `npm install @astrojs/rss`.
- It gives an example of using the UI framework Preact to create an interactive greeting component. They call these kind of components Astro Islands.
- Said component is rendered with the directive `client:load`, which hydrates it. 🚿

That's it for now! I shall be returning for more one day.