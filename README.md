# Njawdi Enterprises website

A responsive website for a cooking-oil supplier based in Abuja, FCT. It includes a product catalogue, pack-size selection, an on-device supply-list builder, company information, and a contact section.

## Before publishing

1. Open `src/data/business.ts`.
2. Add the official business phone number, WhatsApp number, and email address. Use an international phone format for `phone`; for `whatsapp`, use digits only, for example `2348012345678` (do not use this example as your own number).
3. Review the product descriptions and all guide prices in `src/data/catalog.ts`. Prices are sample guide prices from the supplied project and should be verified before launch.
4. Check the product photos, business claims, delivery wording, and service area.

The site intentionally does not invent a phone number, email address, or street address. Until you fill the contact settings, the contact section explains which details need to be added.

## Run locally

You need Node.js 20 or newer and npm.

```bash
npm install
npm run dev
```

Open the local address shown by Vite. To check a production build:

```bash
npm run build:dev
```

## Publish on Vercel

1. Extract this ZIP and upload the project to a new GitHub repository.
2. Sign in to Vercel and choose **Add New → Project**.
3. Import the GitHub repository.
4. Keep the framework/build settings detected from the project. The repository includes `vercel.json` for its install command.
5. Deploy, then open the generated URL and test the site on a phone and desktop.
6. Add your real business contact details and verified prices, commit the changes, and redeploy.

You can also use another host that supports Vite/TanStack Start, but follow that host's requirements for server-side routes and production builds. Do not publish until you have verified the contact details and prices.

## Important notes

- The supply-list request is saved in the visitor's browser on that device. It does **not** automatically send the request to Njawdi Enterprises or create a central order record. Customers should use the contact details you configure to contact the business.
- The catalogue uses guide prices. Confirm all prices, stock, pack sizes, and delivery charges before accepting an order.
- Do not add private customer information to public source files.
