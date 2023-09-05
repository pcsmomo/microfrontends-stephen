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

- Cons:
  - Easy to setup and understand!
- Pros:
  - Container has to be re-deployed every time ProductsList is updated
  - Tempting to tightly couple the Container + ProductsList together

</details>
