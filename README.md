<h1 align="center">The Magic Trips</h1>
<h2>Table of Contents</h2>
  - [Medusa](#medusa)
  - [Storefront](#storefront)

## Features
- **Sleek, Modern Design**: The storefront boasts a minimalist, contemporary design that perfectly reflects **Sofa Society's** commitment to modern aesthetics and sustainability.
- **Dynamic Materials and Colors**: Add richness to your product offerings by defining **materials** and **colors** for each product. Colors will be displayed using their corresponding hex codes, and each material can have multiple color options. Customers first select a material, then a color, with dynamic pricing based on their choices.
- **Customizable Collections**: Easily customize the content and images for each collection. Each product page also features images and a CTA for the collection it belongs to, which can be personalized as well, creating a fully branded shopping experience.
- **Premade Inspiration Page**: A beautiful, ready-to-use inspiration page helps customers explore the latest trends and styles, showcasing Sofa Society's furniture in real-world settings.
- **About Page**: Share your brand’s story, values, and commitment to sustainability with a pre-built about page that captures the essence of **Sofa Society**.
- **Streamlined Checkout Flow**: The checkout process is designed to be fast, intuitive, and frictionless, providing a seamless shopping experience for your customers from start to finish.
- **Fully Responsive Design**: Optimized for mobile, tablet, and desktop devices, ensuring a smooth, consistent experience across all platforms.
- **Stripe Integration for Payments**: Accept payments effortlessly by integrating **Stripe**. Simply add your Stripe API key to `medusa/.env` and the publishable key to `storefront/.env` to get started.
- **Full E-commerce Functionality**: The starter includes all the essential e-commerce features you need, including product pages, a shopping cart, a checkout process, and order confirmation.
- **Next.js and Tailwind CSS**: Built with **Next.js** v14 app router and **Tailwind CSS**, the starter is highly performant, customizable, and easy to extend with additional features.

## Prerequisites
- Node >= 20
- Yarn >= 3.5
- Docker and Docker Compose
- Stripe account (for payments)

## Quickstart

```bash
git clone git@github.com:Agilo/fashion-starter.git
```

### Medusa

```bash
cd medusa
cp .env.template .env
yarn
docker-compose up -d
yarn build
yarn medusa db:migrate
yarn seed
yarn medusa user -e "admin@medusa.local" -p "supersecret"
yarn dev
```

At this point, you should be able to access the Medusa admin at http://localhost:9000/app with the credentials you just created. After logging in, you should go to http://localhost:9000/app/settings/publishable-api-keys, copy the publishable key, and paste it into the `NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY` env variable in the `storefront/.env.local` file.

### Storefront

```bash
cd storefront
cp .env.template .env.local
yarn
yarn dev
```

You should now be able to access the storefront at http://localhost:8000.

<a href="https://agilo.com" target="_blank">
</a>
