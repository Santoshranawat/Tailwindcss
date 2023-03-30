Hello ,I'm Santosh Kumar Ranawat welcome my github account. 
today we are lear how can install tailwind css and how can apply tailwindcss in our project.

let's start-------------

step 1st: create a folder and give name like tailwind-practice.
step 2nd: create index.html file and input.css file, output.css file in tailwind-practice folder.
step 3rd: Install tailwindcss via npm, run this comman "npm install -D tailwindcss". install tailwindcss in your project.
step 4th: open input.css file and paste this code and save-

@tailwind base;
@tailwind components;
@tailwind utilities;

step 5th: create your tailwind.config.js file. and paste this code -


/* @type {import('tailwindcss').Config} */
module.exports = {
    content: ["./index.html"],
    theme: {
      extend: {
          fontFamily: {
              'sans': ['Rubik','-apple-system','BlinkMacSystemFont','Arial','Roboto','Oxygen','Ubuntu','Cantarell','Fira Sans','Droid Sans','Helvetica Neue','sans-serif'],
          },
          container: {
              center: true,
          },
          colors: {
              blue: {
                  400: '#24bff5',
                  500: '#00a8e2',
                  600: '#6b7a8a',
                  800: '#4a5a6a',
                  900: '#34495f',
              },
              amber: {
                  500: '#f3a027',
              }
          },
          borderRadius: {
              DEFAULT: '5px',
          },
          screens: {
              'sm': '576px',
              'md': '768px',
              'lg': '992px',
              'xl': '1200px',
          },
      },
    },
    plugins: [],
  }

You can change fontFamily and text color as you wish.

step 6th: create package.json file in tailwind-practice folder. paste this code than save 

{
    "name": "tailwind-practice",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
      "dev": "npx tailwindcss -i ./input.css -o ./output.css --watch",
      "build": "npx tailwindcss -i ./input.css -o ./output.min.css --minify",
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    "keywords": [],
    "author": "",
    "license": "ISC",
    "devDependencies": {
      "tailwindcss": "^3.2.7"
    }
  }

you can change name, version and other property name as you wish.

step 7th: run cammand this "npm run dev".

step last: whrite tailwind class in index.html file and run.
congratulation your tailwindcss setup is done.