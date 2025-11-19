## Basics of React JS

1. Extension : .jsx

    - .js → Standard JavaScript files (most common in React projects)
    - .jsx → JavaScript files that contain JSX syntax (React’s HTML-like syntax). While JSX can live in .js files too, some teams prefer .jsx to make it clear
    - .ts → TypeScript files (if your React project uses TypeScript)
    - .tsx → TypeScript files with JSX inside

2. So, if you’re writing React components in plain JavaScript, you can use either:

    - Component.js
    - Component.jsx

3. If using TypeScript with React:

    - Component.ts (no JSX inside)
    - Component.tsx (with JSX inside)

4. JSX : JavaScript Syntex Extension

---

### Need of React

1. Whenever a webpage is loaded, Browser creates a tree like structure of HTML, called as DOM (Document object model)
2. With growing size of code, it becomes difficult to manage DOM
3. So, with React, webpage is defined using different re-usable components. And react handles the process of creating and updating DOM elements. E.g.
    1. When any dynamic value/state is updated, reach updates the same in Light weight Virtual DOM and checks the same with Actual DOM.
    2. If change is found, then only the actual (Browser) DOM is updated
4.
