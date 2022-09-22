# create new nextjs app with typescript and tailwind, yarn, prettier
- `create-next-app --example with-tailwindcss <project_name>`
- `yarn add -D prettier prettier-plugin-tailwindcss`

# next js 
- __Client-side navigation__ means that the page transition happens using JavaScript, which is faster than the default navigation done by the browser.
-  Next.js automatically prefetches the code for the linked page in the background, in production build. 
- If you need to add attributes like, for example, `className`, add it to the `a` tag, __not__ to the Link tag

## API
- any files in `/pages/api` to mapped to `/api*` endpoint
- api routes will be affected by `pageExtensions` config in `next.config.js`
- need a default function to handle request and response
    - `req`: http.IncomingMessage + pre-built middlewares
    - `res`: http.ServerResponse + helper functions
        - ts: `import type { NextApiRequest, NextApiResponse } from "next";`
- api routes do not specify CORS headers, aka same-origin only by default
    - can be changed by wrapping the request handler with the CORS request helpers

## images
- images must be placed in `public/images`

## favicon 
- must be place in `public/` directly

## Nextjs Image
- `layout='fill'` -> grow in both x and y to fill container

# CSS
- design and analyze the layout first
- separate content and layout
- review the basics again
- when learning, dont try to design, use a design

## Tailwind CSS
- light mode is the default, so only dark-mode specifier `dark:` needs to be added to support 2 modes

# Prisma
- install using: `npm install prisma --save-dev` or `yarn add prisma --dev`
- initialize the driver: `npx prisma init --datasource-provider mysql`
- set `DATABASE_URL` in the `.env` file
- run `npx prisma db pull` to turn db schema into a Prisma schema
- run `npx prisma studio` to open the UI and inspect your table
- run `npx prisma generate` to generate the Prisma client
    - to be used in the code:
        ```ts
        import { PrismaClient } from '@prisma/client'
        const prisma = new PrismaClient()
        ```

# Planet Scale
- copy username and password
- copy connection string url
- replace *** in the connection string with the password
- is there only 1 password for prod and non-prod branches?
- if using primsa, copy `shcema.prisma` into project