# Advanced-React

This is the frontend project for the Wesbos course on Advanced React and GraphQL.

# Commands
npm run dev<br/>

# Emmet
Enable Emmet in VSCode with setting "emmet.includeLanguages": { "javascript": "javascriptreact" }.<br/>
Then, to create `<div className="foo-bar"></div>`, type **.foo-bar** and press Enter. Voilà.

## Shortcuts
    rcc
This creates a React component class with a render function.

# Styled Components
This is an ES6 thing.  First import 'styled' from 'styled-components'.  Create a const component and set it equal to styled.*whatever* then follow that with backtics (template literals) and end with semicolon.  Normal CSS goes between the backtics.  Finally, use the component in place of the *whatever* element you were going to use.

## Example
In this example "huge" is a prop that serves as toggle for whether to make the font-size 100 or 50 pixels.

    const MyButton = styled.button`
      background: red;
      font-size: ${props => (props.huge ? '100px' : '50px')};
      .pumpkin {
        font-size: 100px;
      }
    `;

    <MyButton huge>
      Click Me
      <span className="pumpkin">🎃</span>
    </MyButton>
    
## Server Side Rendering
Copy <a href="https://github.com/zeit/next.js/blob/master/examples/with-styled-components/pages/_document.js">_document.js</a> to your project in /pages directory.

# React Context
Context came about in 16.3 and replaces the need for Redux.<br />
<a href="https://wesbos.com/react-context/">Wes' excellent explaination</a><br />
<a href="https://reactjs.org/docs/context.html">React official explaination</a>

# Apollo Dev Tools (Chrome)
https://www.apollographql.com/docs/react/features/developer-tooling.html

