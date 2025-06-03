# 📱 React Phone Catalog

🔗 **Live Demo:** [moodddii.github.io/react_phone-catalog](https://moodddii.github.io/react_phone-catalog/)

This is a responsive and interactive phone catalog application built with **React**. It features dynamic routing, local storage, sorting, pagination, state management, and a fully modular structure following modern best practices.

---

## 🗂️ Project Structure

- All components are stored in `src/components`.
- Each component is organized in its own folder containing:
  - `index.ts`
  - `ComponentName.tsx`
  - `ComponentName.module.scss`
- Uses **CSS Modules** for styling.
- Modular structure with `src/modules`, which contains:
  - One folder per page (`HomePage`, `CartPage`, etc.)
  - A shared folder for reusable components, logic, and styles.
  - Each module has its own `components`, `hooks`, `constants`, etc.

---

## 🚀 Features

### 🔝 Header & Footer

- **Sticky Header** with logo, navigation links, Favorites, and Cart icons.
- **Footer** includes:
  - Link to GitHub repository.
  - Smooth "Back to Top" button.
- Page content has a consistent max width and centered layout.

---

### 🏠 Home Page (`/`)

- **Image Slider**:
  - Auto-switches every 5 seconds.
  - Manual navigation with arrows and dot indicators.
- **Hot Prices** slider:
  - Shows discounted products sorted by highest discount.
- **Shop by Category** block:
  - Links to `/phones`, `/tablets`, and `/accessories`.
- **Brand New** block:
  - Displays newest products based on release year.

---

### 📦 Category Pages (`/phones`, `/tablets`, `/accessories`)

- Displays a dynamic title: "Phones Page", "Tablets Page", etc.
- Shows product list filtered by category.
- Features:
  - Sorting: Newest, Alphabetically, Cheapest.
  - Pagination with 4, 8, 16, or all items per page.
  - Query params saved to the URL (`?sort=age`, `?page=2&perPage=8`).
  - Loader during fetch, error messages on failure.
  - Message shown when no products available.

---

### 📱 Product Details Page (`/product/:productId`)

- Shows full product details:
  - Image gallery, color and capacity selectors.
  - Description and technical specs.
- Includes:
  - Breadcrumbs (Home / Category / Product Name).
  - "You may also like" section with random suggestions.
  - Back button that mimics browser behavior.
  - Loader while fetching.
  - Message if product is not found.

---

### 🛒 Cart Page (`/cart`)

- List of added products with quantity management.
- Features:
  - Add/Remove items.
  - Increase/Decrease quantity (minimum 1).
  - Total count and price calculation.
  - Cart saved in `localStorage`.
  - Checkout button opens modal:
    - Confirms and clears cart or cancels.
  - Cart icon in header shows total quantity.

---

### ❤️ Favorites Page (`/favorites`)

- Product cards include a heart icon to add/remove from favorites.
- Favorite items are saved in `localStorage`.
- Header icon shows number of favorited items.

---

## ✨ Additional UI/UX Features

- Smooth hover effects on buttons and images.
- Image scaling by 10% on hover.
- Fully responsive layout.
- Custom 404 Not Found page for unmatched routes.
- All form elements and icons follow the UI Kit style.

---

## 🛠️ Tech Stack

- React
- TypeScript
- React Router
- CSS Modules
- LocalStorage
- Context API

---

## 📂 Getting Started (Optional)

To run the project locally:

```bash
git clone https://github.com/moodddii/react_phone-catalog.git
cd react_phone-catalog
npm install
npm start
