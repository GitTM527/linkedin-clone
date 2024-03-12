# Hay I am Building a Linked Clone from Scratch

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

## Links
So I followed a Video Tutorial (https://www.youtube.com/watch?v=xP3cxbDUtrc&list=PL-J2q3Ga50oMQa1JdSJxYoZELwOJAXExP&index=2)
and found out alot of improvement is happened in the tech space;
A good example is importation of Components from React dependences and implimentaton method.
Thanks to Documntation from (https://bobbyhadz.com/blog/component-is-not-a-route-component-react-router)
This help me resolve the challenge


### Code, Challenge Solved so Far
(from Video)
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
function App() {
  return (
    <div className="App">
      <Router>
        <Routes>
          <Route exact path="/"> 
             <Login />
          <Route>
        </Routes>
      </Router>
    </div>
  );
}

export default App;

The above returned error [Login] not a component of Route due to upgraged version of react-route-dom dependencies

(My Solution)
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
function App() {
  return (
    <div className="App">
      <Router>
        <Routes>
          <Route exact path="/" element={<Login />} />
        </Routes>
      </Router>
    </div>
  );
}

export default App;

I decleared the Login Component using "element."
