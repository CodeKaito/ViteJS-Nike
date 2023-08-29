# Nike Website in Next.js 13 and Tailwind CSS

![Nike Website](screenshot.png)

Welcome to this guide on building a Nike-themed website using Next.js 13 with Server Side Components (SSC) and basic Tailwind CSS integration. In this tutorial, we will create a simple and stylish website that showcases the power of Next.js 13 and the convenience of Tailwind CSS.

## Prerequisites

Before you begin, make sure you have the following installed:

- Node.js (v16 or later recommended)
- npm (Node Package Manager)
- Git

## Getting Started

### 1. Create a Next.js Project

```bash
npx create-next-app nike-website
cd nike-website
```

### 2. Install Required Dependencies

Install the necessary packages for Server Side Components and Tailwind CSS:

```bash
npm install next@13 tailwindcss
```

### 3. Configure Tailwind CSS

Generate a Tailwind CSS configuration file:

```bash
npx tailwindcss init -p
```

In the generated `tailwind.config.js` file, update the `purge` property to include your project files:

```javascript
module.exports = {
  purge: ['./src/**/*.{js,ts,jsx,tsx}'],
  // ...rest of the config
}
```

### 4. Create Components

Create a `components` folder in the `src` directory. Inside the `components` folder, create reusable components for your Nike website. For example, you can create a `Header.js` component:

```jsx
// src/components/Header.js

import React from 'react';

const Header = () => {
  return (
    <header className="bg-gray-900 text-white py-4">
      <div className="container mx-auto">
        <h1 className="text-2xl font-semibold">Nike</h1>
      </div>
    </header>
  );
};

export default Header;
```

### 5. Create Server Side Components

In the `pages` directory, create a new file named `_components.js`. This file will house your Server Side Components:

```jsx
// pages/_components.js

import Header from '../components/Header';

export const components = {
  Header,
};
```

### 6. Create Pages

Create pages for your website in the `pages` directory. For instance, you can create an `index.js` file for the homepage:

```jsx
// pages/index.js

import React from 'react';

const Home = () => {
  return (
    <div>
      <Header />
      <main className="container mx-auto py-8">
        {/* Add your content here */}
      </main>
    </div>
  );
};

export default Home;
```

### 7. Style Your Website

Use Tailwind CSS classes to style your components and pages. You can apply classes directly in your component files or use CSS modules.

## Run the Project

Start your Next.js project:

```bash
npm run dev
```

Your Nike-themed website should now be accessible at `http://localhost:3000`.

## Conclusion

Congratulations! You've successfully created a Nike-themed website using Next.js 13 with Server Side Components and basic Tailwind CSS integration. This project demonstrates the power of Next.js for building efficient and dynamic websites, along with the convenience of Tailwind CSS for styling.

Feel free to expand upon this project by adding more pages, components, and custom styles to create a unique and engaging website.

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Server Side Components in Next.js 13](https://nextjs.org/blog/next-13#server-side-components)
- [GitHub Repository for this Project](https://github.com/yourusername/nike-website-nextjs)

Happy coding! 🚀
