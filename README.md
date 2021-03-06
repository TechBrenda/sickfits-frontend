# Advanced-React

This is the frontend project for the Wesbos course on Advanced React and GraphQL.

# Daily Dev Flow
Run through Daily Dev Flow of backend first.

    npm run dev

# Emmet
Enable Emmet in VSCode with setting "emmet.includeLanguages": { "javascript": "javascriptreact" }.<br/>
Then, to create `<div className="foo-bar"></div>`, type **.foo-bar** and press Enter. Voilà.

## Shortcuts
    rcc
This creates a React component class with a render function.

# VSCode Hotkeys
* Prettier Auto-formatting: Shift-Alt-F
* For multiple cursors: place cursor, then hold Alt while clicking more cursor locations (Esc or click elsewhere to reset)
* Select all instances of a string: Put cursor in the string and press Shift-Ctrl-L
* To select multiple different strings at once: double-click string, hold Alt, and double click additional strings. These can be copy and pasted and typed around using Home and End.
* To move a whole line: place cursor on the line, hold Alt, and press up or down

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
Context came about in 16.3 and replaces the need for Redux. I read elsewhere that this feature was actually developed by the creator of Redux who was hired by Facebook shortly after announcing Redux.
* <a href="https://wesbos.com/react-context/">Wes' excellent explaination</a>
* <a href="https://reactjs.org/docs/context.html">React official explaination</a>

# Apollo Dev Tools (Chrome)
https://www.apollographql.com/docs/react/features/developer-tooling.html

# Cloudinary
See Settings for "sickfits" Upload Preset

# Stock Photos
Get great stock photos for example items from https://www.pexels.com.

# ToDo
1. Add a check in CreateItem.js so that the form does not submit until the image upload is complete.
2. Fix annoying NaN error on Price field on Sell page (CreateItem component).
3. Check Nextjs/Apollo sites for the ability to partially update cache, and check on the course again to see if there has been an update to video 23. Partial cache updating is not possible now and is preventing the site's page to load a new item after adding one without manually refreshing the page.
4. Intercept error in Signup component to create a user friendly error if the unique constraint fails.
5. Switch Signin and Signup so that you go to the Signin page to sign up rather than going to the Signup page to sign in.
6. Figure out why "Sign Out" button is slightly darker and smaller than the other Nav buttons
7. Redirect user to main page after login or password reset.

# Development WorkFlow
1. Add schema and resolver in backend.
2. Flip over to front end.
3. Build an interface.  
   a. Define a const to hold the Mutation or Query
   
   <pre><code>const NAME_MUTATION = gql\`\`;
   const NAME_QUERY = gql\`\`;</code></pre>
   
    
   b. Within the backtics put the mutation or query method that will call the mutation or query, respectively. This will have the same name as the const.
   
   <pre><code>mutation NAME_MUTATION($parameter: type) {}
   query NAME_QUERY($parameter: type) {}</code></pre>
    
   c. Within the curly brackets, use a method declared in the backend's schema.graphql (and defined in Mutation.js or Query.js, respectively). That file also give you the parameters and return values you need to include in your method (all layers of it). If the return value is an object, you can specify which member values will be returned.
   
   <pre><code>name(parameter: $parameter) {
     returnObject
   }</code></pre>
   
   If the return value is an object, you can specify which member values will be returned. These values are separated by newlines, not by commas!
   
   <pre><code>name(parameter: $parameter) {
     id
     name
     email
   }</code></pre>
   
4. Manage from there...