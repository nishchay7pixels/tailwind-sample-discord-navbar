# tailwind-sample-discord-navbar

To learn more about tailwind

## Setup (Manual)

1. Generate an JS project (React/Vue/Angular ... etc) we'll be using react here

2. install dependencies to add tailwind

```
npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9

// to override native post css configuration
npm install @craco/craco 
```

3. Replace the react scripts in the package.json as below

```
"scripts": {
    "start": "craco start",
    "build": "craco build",
    "test": "craco test",
    "eject": "react-scripts eject"
}
```

4. Create a craco config files named as *craco.config.js*

```
module.exports = {
    style: {
        postcss: {
            plugins: [
                require('tailwindcss'),
                require('autoprefixer'),
            ],
        }
    }
}
```

5.  run below command to generate a tailwind config in the root project

```
npx tailwindcss-cli@latest init
```

6. then in index.css file use tailwind directives to include tailwind css styles to out project

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```