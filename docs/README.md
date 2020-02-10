# Brendon's Docs

## How are these docs organized?


### 1. Step-by-step instructions

If you have a _specific question_ in mind, look here for the instructions. You can link from here to descriptive documents in the lower sections, but do not add unnecessary description / exposition when adding to these sections. Documentation pages should be organized by _purpose_ not topic.

- **Getting Started**: New hire orientation & setup
- **How to**: Step by step instructions for how to complete common tasks
- **How to fix**: Step by step instructions for how to bring the site back up


### 2. Rules you are expected to follow

You are expected to follow policies and rules established by development leadership. We have compiled these into one section so you can review them all in one place. Development managers are responsible for keeping these pages up to date.

- **Policies**: Rules that you are expected to follow
- **TL Policies**: Rules that every TL is expected to follow


### 3. General resources and descriptions

We have a lot of tools, systems, and best practices. You can come here to learn about how out platform works. When writing documentation in this section, don't write a lot of exposition. Try to think of specific questions a future developer might have, and stick to answering those questions.

- **Dev Resources**: Good-to-know reference material
- **Projects (Back End)**: High level overview of how our back-end projects work
- **Projects (Front End)**: High level overview of how our front-end projects work
- **Business Logic**: Details and troubleshooting information about Lendio business logic
- **Devops**: High level overview of how our infrastructure works
- **Franchise**: High level overview of how franchising works
- **Lender Services**: High level overview of how Lender Services works (multi-tenancy)
- **Tooling**: High level overview of some of the tools we use
- **Misc**: Not yet categorized


## How do I contribute to docs?

For Lendio Docs to obtain maximum usefulness, we all need to reference them frequently and keep them up-to-date. When you have a question, about your environment, or any of our projects, this should be your first stop. And if you find something wrong, outdated, or missing, take a few minutes to make the docs better. But before you can do that, you'll need to know some commands!

The Lendio Docs project is written in MarkDown and parsed with [Docsify](https://docsify.js.org/#/)

+ Github: https://github.com/LendioDevs/docs
+ Local: http://localhost:3000
+ Production: https://docs.lendio.com

### Local dev

- Start the dev process: `npm ci && npm start`
- Open local version at http://localhost:3000
- Write your documentation in MarkDown
- Update the corresponding folder's `_sidebar.md` to include a link to your new document


### Deploy

- Submit your changes in a PR
- Merge into master
- &lt;magic> (your changes will automatically be deployed in a few seconds by Netlify)
- Browse to https://docs.lendio.com to confirm your changes
