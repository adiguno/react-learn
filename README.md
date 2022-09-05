# create new nextjs app with typescript and tailwind, yarn, prettier
- `create-next-app --example with-tailwindcss <project_name>`
- `yarn add -D prettier prettier-plugin-tailwindcss`

# react-learn
- __Client-side navigation__ means that the page transition happens using JavaScript, which is faster than the default navigation done by the browser.
-  Next.js automatically prefetches the code for the linked page in the background, in production build. 
- If you need to add attributes like, for example, `className`, add it to the `a` tag, __not__ to the Link tag

## images
- images must be placed in `public/images`

## favicon 
- must be place in `public/` directly

## Nextjs Image
- `layout='fill'` -> grow in both x and y to fill container

## Tailwind CSS
- light mode is the default, so only dark-mode specifier `dark:` needs to be added to support 2 modes