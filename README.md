# Advanced-React

This is the frontend project for the Wesbos course on Advanced React and GraphQL.

# Commands
npm run dev<br/>

# Emmet
Enable Emmet in VSCode with setting "emmet.includeLanguages": { "javascript": "javascriptreact" }.<br/>
Then, to create `<div className="foo-bar"></div>`, type **.foo-bar** and press Enter. Voilà.

# Styled Components
This is an ES6 thing.  First import 'styled' from 'styled-components'.  Create a const component and set it equal to styled.*whatever* then follow that with backtics and end with semicolon.  Normal CSS goes between the backtics.  Finally, use the component in place of the *whatever* element you were going to use.

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