# Paradise Nursery – Shopping Cart Application

**Project name:** Paradise Nursery Shopping Application

Paradise Nursery is an online houseplant shop built with **React**, **Redux Toolkit** and **Vite**.
Users can browse plants grouped by category, view each plant's image, name, description and price,
add plants to a shopping cart, and manage the cart by changing quantities or removing items while
the totals update dynamically.

## Live demo

https://smmk47.github.io/e-plantShopping/

## Features

### Landing page (`src/App.jsx`, `src/App.css`)
- Full-screen background image of a greenhouse.
- Company name **Paradise Nursery**, tagline and a **Get Started** button that opens the product listing.
- **About Us** section (`src/AboutUs.jsx`) describing the company.

### Product listing page (`src/ProductList.jsx`)
- Five plant categories (Air Purifying, Aromatic Fragrant, Insect Repellent, Medicinal, Low Maintenance),
  each with six plants showing a thumbnail, name, description and price.
- **Add to Cart** button on every plant that adds the plant to the Redux cart, becomes disabled and
  changes to *Added to Cart*, and increments the cart icon counter.
- Navbar shared with the cart page containing **Home**, **Plants** and **Cart** links, plus a cart icon
  that displays the total number of items dynamically.

### Shopping cart page (`src/CartItem.jsx`)
- Shows the total cart amount and total number of items.
- Each cart item shows its thumbnail, name, unit price, quantity and total cost for that plant.
- **+** and **−** buttons to increase or decrease the quantity (decreasing to zero removes the item).
- **Delete** button to remove an item from the cart.
- **Checkout** button that shows a "Coming Soon" style message.
- **Continue Shopping** button that returns to the product listing.

### State management (`src/CartSlice.jsx`, `src/store.js`)
- Redux slice with `addItem`, `removeItem` and `updateQuantity` reducers.

## Getting started

```bash
npm install
npm run dev
```

Build for production and deploy to GitHub Pages:

```bash
npm run build
npm run deploy
```

## Project structure

```
src/
├── App.jsx           # Landing page with Get Started button
├── App.css           # Landing page styles incl. background image
├── AboutUs.jsx       # About Us content
├── ProductList.jsx   # Product listing, navbar and cart icon
├── CartItem.jsx      # Shopping cart page
├── CartSlice.jsx     # Redux slice for the cart
├── store.js          # Redux store
└── main.jsx          # App entry point
```

## License

This project is based on the IBM Developer Skills Network starter template and is licensed under the
terms in the [LICENSE](LICENSE) file.
