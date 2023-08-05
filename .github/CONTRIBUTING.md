# Contributing

Want to contribute to docs? Here's how you can get started:

1. Clone this repo
2. Run `pnpm i`
3. Run `pnpm dev` to start the local server
4. Visit `http://localhost:3000/contribute/` to get started 🥳

Reach out to us on [Discord](https://discord.com/invite/tauri) on the `#dev-documentation` channel if you have any questions!

## Previewing API References

If you'd like to view the API references locally then you must run `pnpm dev:setup` before `pnpm dev` to initialize all of the submodules.

Now you should have the `http://localhost:3000/2/reference/` routes available for preview.

So, you want to write a doc? You've come to the right place!

![Join us gif](https://media.giphy.com/media/3ohhwznAY9PN08m0H6/giphy.mp4)

## Prerelease Writing Guidelines

- Refer to Tauri 2.0 like it's released now (so that copy doesn't need to be updated upon release)
- Write any code so that it works **now** but...
- Annotate any 2.0 code with `{/* FIXME: 2.0 */}` (.mdx files) or `<!-- FIXME: 2.0 -->` (.md files) so that we can easily find and fix any of those upon release (feel free to add in what the code would be upon release in additional comments)

## Writing Style

We're not quite there yet and are still finding our voice...

<Stub />

## Translations (i18n)

While we plan to support translations in the future, we are not currently accepting them until Tauri 2.0 is a bit more stable.

Once translations are enabled you can check the [translation status page](/contribute/translate-status).

## Types of Documentation

We have the following types of documents that roughly follow the types defined by [Diátaxis](https://diataxis.fr/index.html):

- **[Guide](#guide)**: Learning-oriented
- **[Recipe](#recipe)**: Task-oriented
- **[Reference](#recipe)**: Information-oriented
- **[Blog Post](#blog-post)**: Understanding-oriented

Use this chart to help you figure out where the right place for your content is:

| If the content describes… | …and serves the user's… | …then it must belong to…  |
| ------------------------- | ----------------------- | ------------------------- |
| practical steps           | study                   | [a guide](#guide)         |
| practical steps           | work                    | [a recipe](#recipe)       |
| theoretical knowledge     | work                    | [a reference](#reference) |
| theoretical knowledge     | study                   | [a blog post](#blog-post) |

:::tip[What is Diátaxis?]

[Diátaxis](https://diataxis.fr/index.html#) is a technical documentation system that helps with documentation quality and information hierarchy. Since Tauri is such a large project we do our best to organize information as best as possible.

You can dive into the Diátaxis system if you'd like or feel free to start writing and we can guide you along the way.

:::

### Guide

Located in [`/src/content/docs/2/guide/`](https://github.com/tauri-apps/tauri-docs/tree/starlight/src/content/docs/2/guide)

Guides are learning-oriented and take the reader through a specific journey such as starting a new project, and overview of a specific feature, or how to follow a specific flow such as building and bundling their app. They follow a similar philosophy to [tutorials in Diátaxis](https://diataxis.fr/tutorials.html).

The reader should be familiar with the concepts covered by the end of the guide and should set them up with the knowledge required to being experimenting with that topic themselves.

### Recipe

Located in [`/src/content/docs/2/recipe/`](https://github.com/tauri-apps/tauri-docs/tree/starlight/src/content/docs/2/recipe)

Recipes are designed to guide the reader through a specific task similar and have a clear outcome and objective. This could be something like setting up authentication using Firebase, adding a Python binary using sidecar, or requesting admin access on a user's machine. They are similar to [how-to guides in Diátaxis](https://diataxis.fr/how-to-guides.html) (not to be confused with our own guides mentioned above).

The prerequisites for a recipe should be clearly stated. If there are a lot of steps required before getting into the relevant information about the recipe then you may want to link out to another guide, recipe, or external resource and state those as a prerequisite at the top of the recipe.

### Reference

Located in [`/src/content/docs/2/reference/`](https://github.com/tauri-apps/tauri-docs/tree/starlight/src/content/docs/2/reference), although they should be auto-generated when possible.

References are where all the nuts and bolts of Tauri's API are documented. These should be generated from upstream repos when possible and written following the best practices described by [references in Diátaxix](https://diataxis.fr/reference.html).

These should be as succinct and to the point as possible so that the reader can quickly find the relevant information.

### Blog Post

Not yet created, will be added in the future.

Topics that are around understanding something can be written as a blog post (we welcome submissions to the Tauri blog from anyone). Blog posts are a good option because they help the reader understand that information is accurate at the time of writing (and of course can always be updated later if it becomes stale). Blog posts follow the goals of [explanation in Diátaxis](https://diataxis.fr/explanation.html), but not all blog posts necessarily fit this specific format.