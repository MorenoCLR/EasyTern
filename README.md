# Easytern

A Next.js project built with **Supabase** and deployed on **Vercel**.

This README will help you set up the project locally so everyone in the team can collaborate smoothly.

## Features

- Works across the entire [Next.js](https://nextjs.org) stack
  - App Router
  - Pages Router
  - Middleware
  - Client
  - Server
  - It just works!
- supabase-ssr. A package to configure Supabase Auth to use cookies
- Password-based authentication block installed via the [Supabase UI Library](https://supabase.com/ui/docs/nextjs/password-based-auth)
- Styling with [Tailwind CSS](https://tailwindcss.com)
- Components with [shadcn/ui](https://ui.shadcn.com/)
- Optional deployment with [Supabase Vercel Integration and Vercel deploy](#deploy-your-own)
  - Environment variables automatically assigned to Vercel project

## Prerequisites

Make sure you have these installed:

```bash
# Install Node.js (LTS version recommended)
https://nodejs.org/

# Check versions
node -v
npm -v
```

## Project Setup

Clone the repository

```bash
  git clone <repo-url>
  cd easytern
```

Install dependencies

```bash
  npm install
```
    
## Environment variables (`.env.local`)
  This project uses Supabase, so you need some secret keys to run it.
  
  ### Manual Setup
  In the repo, there should be a file named:

  ```bash
  .env.example
  ```

  Copy it and rename it to `.env.local`
  Open `.env.local` in any editor and fill in the real values

  ```env
  NEXT_PUBLIC_SUPABASE_URL=[INSERT SUPABASE PROJECT URL]
  NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=[INSERT SUPABASE PROJECT API PUBLISHABLE OR ANON KEY]
  ```

  ### Vercel CLI Setup
  Install Vercel CLI
  ```bash
  npm install -g vercel
  ```

  Log In
  ```bash
  vercel login
  ```

  Link the project
  ```bash
  vercel link
  ```

  Pull environment variables from Vercel
  ```bash
  vercel env pull .env.local
  ```

  > [!NOTE]
  > This example uses `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY`, which refers to Supabase's new **publishable** key format.
  > Both legacy **anon** keys and new **publishable** keys can be used with this variable name during the transition period. Supabase's dashboard may show `NEXT_PUBLIC_SUPABASE_ANON_KEY`; its value can be used in this example.
  > See the [full announcement](https://github.com/orgs/supabase/discussions/29260) for more information.

  Both `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` can be found in [your Supabase project's API settings](https://supabase.com/dashboard/project/_?showConnect=true)


## Local Development

To start the project locally:

```bash
  npm run dev
```

Then open:
```
  http://localhost:3000
```

> [!NOTE]
> The app should now be running. Any code changes you make will auto-refresh in the browser.

## Deployments (What Vercel Does)

You don’t need to manually deploy the app. Vercel is already connected to this GitHub repo.

Every push to main -> `Production` deployment

Live at:

https://easy-tern.vercel.app`


Every push to another branch / PR -> `Preview` deployment

URL looks like:

`https://easy-tern-<random>-morenoclrs-projects.vercel.app`

These URLs are also used for Supabase Auth redirects.

## FAQ

This template comes with the default shadcn/ui style initialized. If you instead want other ui.shadcn styles, delete `components.json` and [re-install shadcn/ui](https://ui.shadcn.com/docs/installation/next)

> Check out [the docs for Local Development](https://supabase.com/docs/guides/getting-started/local-development) to also run Supabase locally.

## Learn More

To learn more about Next.js and Supabase, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
- [Next.js Subscription Payments Starter](https://github.com/vercel/nextjs-subscription-payments)
- [Cookie-based Auth and the Next.js 13 App Router (free course)](https://youtube.com/playlist?list=PL5S4mPUpp4OtMhpnp93EFSo42iQ40XjbF)
- [Supabase Auth and the Next.js App Router](https://github.com/supabase/supabase/tree/master/examples/auth/nextjs)

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!