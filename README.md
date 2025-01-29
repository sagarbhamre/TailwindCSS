# TailwindCSS : v3.x


steps to run project:


> npm install -D tailwindcss@3


> npx tailwindcss init


In tailwind.config.js file , modify the contents: [] as below:
content: ["./src/**/*.{html,js}"],

In package.json file modify the "scripts" section as below:
"scripts": {
    "tw:build": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch",  // <==== this is new entry
    "test": "echo \"Error: no test specified\" && exit 1"
  },

Create input.css file and paste below code:
@tailwind base;
@tailwind components;
@tailwind utilities;


add below two entries to index.html :
<script defer src="./assets/fontawesome/js/fontawesome.min.js" crossorigin="anonymous"></script>
<script defer src="./assets/fontawesome/js/solid.min.js" crossorigin="anonymous"></script>


> npm run tw:build   // <====== this is a command for running project
You will see '/dist/output.css' file in the project that is newly generated. 
