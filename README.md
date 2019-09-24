# react-tailwind-postcss

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Setup

There are severeal ways to setup TailwindCSS to React.

The most common approach I found on the web was to add Tailwind/PostCSS CLI and add a build step npm script to compile CSS. While this works, I don't think it's the best solution out there.

To get the best integration and workflow, my choice was to add Tailwind as a PostCSS plugin via [postcss-loader](https://github.com/postcss/postcss-loader) in webpack. This is the preferred way to install Tailwind, as stated in its [documentation](https://tailwindcss.com/docs/installation/#webpack).

The downside of this approach is that since CRA don't expose webpack settings, you need to eject it.

After ejecting, add ```require('tailwindcss')``` to postcss-loader config and any other plugins you wish, like [postcss-import](https://github.com/postcss/postcss-import). Then, simply follow the next instructions in their docs.

SASS support, although not essencial, is provided out of the box by CRA by adding node-sass.

[Stylelint](https://github.com/stylelint/stylelint) is also configured using Tailwind provided rules to guarantee css consistency.