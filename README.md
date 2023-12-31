
2. Next, you need to setup the `.env` file found in the root with the appropriate API Keys & credentials from the following service providers:

- [Google Firebase](https://firebase.google.com/)
- [MongoDB Atlas](https://cloud.mongodb.com)

3. Install all the dependency packages found in the `package.json` file by running `yarn install` or `npm install` from the project root directory.

4. To start the development server of the application, run `npm run dev` or `yarn dev`. This should log some start-up application information & display the development server url: `http://localhost:3000`. Visit http://localhost:3000 to view your application.

## Usage

### General

This application was built reflecting the MVC architecture and the main dependencies(all found in the `package.json`) of the application are organised as so:

- Front-end User Interface(UI): [React.js](https://reactjs.org), [Chakra UI](https://chakra-ui.com)
- Backend Integration: [NextJS API(serverless functions)](https://nextjs.org/docs/api-routes/introduction) (basically [NodeJS](https://nodejs.org/))
- Database Management: [MongoDB](https://mongodb.com)
- File Storage: [Firebase Storage](https://firebase.google.com/products/storage/)

Other important services & dependency libraries of the application include:

- [axios](https://www.npmjs.com/package/axios): An http client to fetch urls and make api calls or requests within the application.
- [swr](https://swr.vercel.app/): To fetch and revalidate data on the client-side of the application while keeping the UI reactive.
- [react-hook-form](https://react-hook-form.com/): A lightweight Javascript library for form validation and form data capturing.
- [compressorjs](https://fengyuanchen.github.io/compressorjs/): Javascript image compressor to compress images before uploading them to storage to have an optimized and servable version.
- [moment](https://momentjs.com): A javacript library to format and manipulate Date objects.
- [react-simple-star-rating](https://www.npmjs.com/package/react-simple-star-rating): A react component to easily integrate a star-rating styled component.
- [testing-library](https://testing-library.com/): This library provides simple and complete testing utilities to be implement in our test scripts.
- [jest](https://jestjs.io/): A JavaSript Testing Framework to run test scripts in the virtual environment of our application.

### Directives

The application is organized from the root(`.`) as follows:

- `./page/` folder(integrated by NextJS) contains the UI Views for the application with the exception of the `./page/api/*` sub-folder.
- `./page/api` sub-folder(integrated by NextJS) contains serverless and NodeJS backend code for the application.
- `./firebase/` folder contains the Firebase initialization configurations and the logical operation to upload images to Firebase Storage.
- `./mongodb/` folder contains the MongoDB Client variable used to establish connections to the MongoDB Atlas server.
- `./components/` folder contains coded UI layouts to be used through out the application.
- `./assets/` folder contains pre-defined data selections to be used by the appliction.
- `./styles/` folder(integrated by NextJS) contains the global style of the application accessible by all components.
- `./public/` folder(integrated by NextJS) contains global files to be shared through the application. You can store static images here.

Absolute imports to any of these folders through the application are configured in the `jsconfig.json` file in the root.

The application's code source contains inline comments which will provide further help and guidance on how an important piece of module or component works. The code quality was tested with [JSLint](https://www.jslint.com/)

### Deployment

You may eventually want to deploy a live version of your app in a future instance. [Vercel](https://vercel.com/) platform is suitably built fo the deployment of NextJS application and more as they have an integrated environment to deploy directly from your own [Github Repository](https://github.com/new).

### Tests

The `tests` folder contains some major component Unit Test scripts which have been passed successfully to ensure the application functions and renders as it is intended to. Only the major components have been tested. You can decide to add more tests on your personal end.

To run a test, type npm run test or yarn test including the test script you want to run ex:

```bash
yarn test index
```

The `jest.config.js` file contains the configuration options for our [Jest](https://jestjs.io/) Test Runner.


