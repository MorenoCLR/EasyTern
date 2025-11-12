# Easytern

A Next.js project built with **Supabase** and deployed on **Vercel**.

This README will help you set up the project locally so everyone in the team can collaborate smoothly.

## Tech Stack

- **Frontend:** Next.js (React)  
- **Backend / Database:** Supabase  
- **Deployment:** Vercel  
- **Package Manager:** npm

## Prerequisites

Make sure you have these installed:

```bash
# Install Node.js (LTS version recommended)
https://nodejs.org/

# Check versions
node -v
npm -v
```
## Installation

Install EasyTern with npm

```bash
  cd easytern
  npm install
```
    
## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`NEXT_PUBLIC_SUPABASE_URL=key`
`NEXT_PUBLIC_SUPABASE_ANON_KEY=key`
`NEXT_PUBLIC_SITE_URL=http://localhost:3000`
`NODE_ENV=development`

Optional Server Only
`SUPABASE_SERVICE_ROLE_KEY=key`


## Deployment

To deploy this project run

```bash
  npm run dev
```

## Next.JS Section

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
