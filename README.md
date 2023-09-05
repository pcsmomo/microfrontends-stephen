# microfrontends-stephen

Microfrontends with React: A Complete Developer's Guide by Stephen Grider

# Details

<details open>
  <summary>Click to Contract/Expend</summary>

## Section 1: The Basics of Microfrontends

### 5. Understanding Build-Time Integration

#### Major Categories of Integration

- Build-Time Integration (Compile-Time Integration)
  - **Before** Container gets loaded in the browser, it gets access to ProductsList source code
- Run-Time Integration (Client-Side Integration)
  - **After** Container gets loaded in the browser, it gets access to ProductsList source code
- Server Integration (we won't consider much)
  - While sending down JS to load up Container, a server decides on whether or not to include ProductsList source

#### Build-Time Integration

- Engineering team develops ProductsList
- Time to deploy!
- Publish ProductsList as an NPM package
  - NPM Registry
    - ProductsList
- Team in charge of Container installs ProductsList as a dependency
- Container team builds their app
- Output bundle that includes all the code for ProductsList

##### Pros and Cons

- Pros:
  - Easy to setup and understand!
- Cons:
  - Container has to be re-deployed every time ProductsList is updated
  - Tempting to tightly couple the Container + ProductsList together

### 6. A Run-Time Integration

#### Run-Time Integration

- Engineering team develops ProductsList
- Time to deploy!
- ProductsList code deployed at https://my-app.com/productslist.js
- User navigates to my-app.com, Container app is loaded
- Container app fetches productslist.js and executes it

##### Pros and Cons

- Pros:
  - ProductsList can be deployed independentaly at any time
  - Different versions of ProductsList can be deployed and Container can decide which one to use
- Cons:
  - Tooling + setup is far more complicated

#### This course is focused on Run-Time Integration using Webpack Module Federation

- Hardest to setup + understand - makes sense to cover it in great detail!
- Most flexible and performant solution around right now
- Be aware - we will spend a lot of time focusing on Webpack and how it works

</details>
