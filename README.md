# Tailwind CSS Simple Starter

![cover](./assets/tailwind.png)

Tailwind is a CSS framework that provides us with single-purpose utility classes which are opinionated for the most part, and which help us design our web pages from right inside our markup or .js

Tailwind CSS works by scanning all of your HTML files, JavaScript components, and any other templates for class names, generating the corresponding styles and then writing them to a static CSS file.

It's fast, flexible, and reliable — with zero-runtime.

This is a simple setup to develop Tailwind projects, which will be used for Tailwind projects.

## 🦉 Official source

```
https://tailwindcss.com/
```

## 🦊 Usage

Open your terminal and install Tailwind CSS (you do need Node.js installed).

Create a package.json

```
npm init -y
```

Install Tailwind and dependencies with npm

```
npm install -D tailwindcss
```

Create a config file

```
npx tailwindcss init
```

Configure your template paths

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Create an input CSS file (input.css in the root)

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Create a npm script to start the Tailwind CLI build process (in package.json file)

```
  "scripts": {
    "build": "tailwindcss -i ./input.css -o ./css/style.css",
    "watch": "tailwindcss -i ./input.css -o ./css/style.css --watch"
  }
```

Run build command (it will create a css folder with style.css)

```
npm run build
```

Start using Tailwind in your HTML

```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/style.css">
    <title>Simple Tailwind Starter</title>
</head>
<body>
    <h1 class="text-3xl">Simple Tailwind Starter</h1>
</body>
</html>
```
