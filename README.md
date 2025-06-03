#🛍️ Live Demo

This is a responsive phone catalog built with React, featuring routing, local state management, dynamic pages, persistent storage, and a modular component structure.

##📁 Project Structure
All components are placed in src/components. Each component has its own folder with index.ts, ComponentName.tsx, and ComponentName.module.scss.

Styles are handled using CSS Modules.

Extended structure: src/modules with per-page folders (e.g. HomePage, CartPage, etc.) and a shared folder for common logic and UI.

Each module contains its own components, and optionally hooks, constants, etc.

##🧭 Navigation
Sticky Header with logo, navigation, favorites, and cart icons.

Footer with a GitHub repo link and a "Back to top" button (with smooth scroll).

Page content is centered and has consistent max width.

##🏠 Home Page (/)
Image Slider that auto-rotates every 5s and supports manual navigation with arrows and dots.

Hot Prices Slider — discounted products sorted by largest absolute discount.

Shop by Category block with links to /phones, /tablets, /accessories.

Brand New block with the newest products based on release year.

##📦 Category Pages (/phones, /tablets, /accessories)
Display products by type with a dynamic heading.

Sort by newest, alphabetically, or by price (discounted).

Pagination and items-per-page selector (4, 8, 16, all) with URL synchronization.

Loader during data fetch, error handling, and messages for empty lists.

##📱 Product Details Page (/product/:productId)
Detailed product view: gallery, colors, capacities, tech specs, and description.

"You may also like" section with random suggested products.

Breadcrumbs with links to Home and category.

Back button (mimics browser back).

Handles invalid product IDs with a "Product was not found" message.

##🛒 Cart Page (/cart)
Add/remove products with quantity controls.

Cart stored in localStorage and persists between reloads.

Total quantity and price calculation.

"Checkout" button opens confirmation dialog (simulated).

Cart icon shows the current number of items.

##❤️ Favorites Page (/favorites)
Add/remove products from favorites via a heart icon.

Favorite count displayed in the header.

Favorites are stored in localStorage.
