### Redux Reducers and Selectors

- **Redux Docs: Structuring Reducers**  
  http://redux.js.org/docs/recipes/StructuringReducers.html  
  Comprehensive information on writing reducers and structuring data, covering reducer composition, use of `combineReducers`, normalizing data, proper immutable updating, and more.

- **"How to dynamically load reducers for code splitting in a Redux application?"**  
  http://stackoverflow.com/questions/32968016/how-to-dynamically-load-reducers-for-code-splitting-in-a-redux-application  
  Dan Abramov gives a basic exapmle of how to rebuild and replace the root reducer function at runtime

- **The Power of Higher-Order Reducers**  
  http://slides.com/omnidan/hor#/  
  A slideshow from the author of redux-undo and other libraries, explaining the concept of higher-order reducers and how they can be used

- **Taking Advantage of `combineReducers`**  
  http://randycoulman.com/blog/2016/11/22/taking-advantage-of-combinereducers/  
  Examples of using `combineReducers` multiple times to produce a state tree, and some thoughts on tradeoffs in various approaches to reducer logic.

- **State Snapshots in Redux**  
  http://kyleshevlin.com/state-snapshots-in-redux/  
  Describes a useful technique for saving copies of state slices on command, and re-applying those copies at a later point to ensure a known starting point for further actions.

- **Reducer composition with Higher Order Reducers**  
  https://medium.com/@mange_vibration/reducer-composition-with-higher-order-reducers-35c3977ed08f  
  Some great examples of writing small functions that can be composed together to perform larger specific reducer tasks, such as providing initial state, filtering, updating specific keys, and more.

- **Higher Order Reducers - It just sounds scary**  
  https://medium.com/@danielkagan/high-order-reducers-it-just-sounds-scary-2b9e5dbfc705  
  Explains how reducers can be composed like Lego bricks to create reusable and testable reducer logic.

- **A small trick to write clean reducers**  
  https://hackernoon.com/a-small-trick-to-write-clean-reducers-a0b1b1eff3d2  
  Shows a contrived example of updating deeply nested state, and discusses use of `lodash/fp` to simplify the update logic instead.

- **Combine Redux reducers like a Tetris ninja**  
  https://engineering.legalstart.fr/combine-redux-reducers-like-a-tetris-ninja-6f4eb690aed5  
  Discusses the intended use case and limitations of `combineReducers`, and presents a custom utility called `combineMultiKeyReducers` that will pass along specified slices of state to a reducer.

- **Querying a Redux Store**  
  https://medium.com/@adamrackis/querying-a-redux-store-37db8c7f3b0f  
  A look at best practices for organizing and storing data in Redux, including normalizing data and use of selector functions.
  
- **Normalizing Redux Stores for Maximum Code Reuse**  
  https://medium.com/@adamrackis/normalizing-redux-stores-for-maximum-code-reuse-ae6e3844ae95  
  Thoughts on how normalized Redux stores enable some useful data handling approaches, with examples of using selector functions to denormalize hierarchical data.

- **Practical Redux: Using Redux-ORM**  
  http://blog.isquaredsoftware.com/2016/10/practical-redux-part-1-redux-orm-basics/  
  http://blog.isquaredsoftware.com/2016/10/practical-redux-part-2-redux-orm-concepts-and-techniques/  
  A look at how Redux-ORM can help manage normalized data in a Redux store, including use cases, basic usage, key concepts, and advanced techniques.
  
- **"How do you add/remove to a redux store generated with normalizr?**  
  http://stackoverflow.com/questions/34954726/how-do-you-add-remove-to-a-redux-store-generated-with-normalizr  
  Stack Overflow discussion of how to handle updates to normalized data

- **"Any deep-dive/advanced tutorials on reselect?"**  
  https://www.reddit.com/r/reactjs/comments/5dxasp/any_deepdiveadvanced_tutorials_on_reselect/  
  Discussion on passing arguments to Reselect selectors, and how to use "factory functions" to define per-component selectors for Redux `mapState` functions

- **ReactCasts #8: Selectors in Redux**  
  https://www.youtube.com/watch?v=frT3to2ACCw  
  A great overview of why and how to use selector functions to retrieve data from the store, and derive additional data from store values

- **Use Selectors in Redux for Great Good**  
  https://medium.com/@TomasEhrlich/use-selectors-in-redux-for-great-good-59286ce2e2a1  
  A short article explaining the importance of selectors, with a few examples of how they benefit applications and how to use them.

### Redux Middleware

- **A Beginner's Guide to Redux Middleware**  
  https://www.codementor.io/reactjs/tutorial/beginner-s-guide-to-redux-middleware  
  A useful explanation of middleware use cases, with numerous examples

- **Understanding Redux Middleware**  
  https://medium.com/@meagle/understanding-87566abcfb7a  
  Breaks down Redux's applyMiddleware function line-by-line, and explains the concepts involved

- **Building Redux Middleware**  
  https://reactjsnews.com/redux-middleware  
  Demonstrates building a basic Redux middleware

- **Redux Middleware Tutorial**  
  http://www.pshrmn.com/tutorials/react/redux-middleware/  
  An overview of what middleware is, how `applyMiddleware` works, and how to write middleware.

- **Redux Middleware: Behind the Scenes**  
  http://briantroncone.com/?p=529  
  Digs into the concepts and implementation of middleware.
  
- **Middlewares and React Redux Lifecycle**  
  https://medium.com/@rajaraodv/using-middlewares-in-react-redux-apps-f7c9652610c6  
  A description of what a middleware is, and how it works in Redux

- **Workshop Slides: Redux Middleware**  
  http://www.slideshare.net/visualengin/workshop-22-reactredux-m  
  A slideshow that explains how Redux middleware work, with several helpful visualizations
  
- **Understanding Redux Middleware and Writing Custom Ones**  
  https://dev.to/imwiss/understanding-redux-middleware-and-writing-custom-ones  
  Describes the concept of middleware in Redux, possible use cases, and gives an example of writing a middleware to handle caching.

### Middleware Techniques

- **Redux Hack: Custom Thunk APIs**  
  http://chrispearce.co/redux-quick-hack-custom-thunk-apis/  
  Demonstrates writing a custom thunk middleware that injects additional dependencies into thunks.

- **Connecting Redux to your API**  
  https://blog.boldlisting.com/connecting-redux-to-your-api-eac51ad9ff89  
  Describes imperative and declarative approaches to managing request data and metadata
  
- **You Aren't Using Redux Middleware Enough**  
  https://medium.com/@jacobp100/you-arent-using-redux-middleware-enough-94ffe991e6  
  Suggestions for using middleware to solve a number of interesting use cases
  
  
- **"Do I always need to return a value from a Redux middleware?"**  
  https://stackoverflow.com/questions/45964129/do-i-always-need-to-return-a-value-from-a-redux-middleware/45964310#45964310  
  My answer to a question about whether middleware should do `return next(action)`.  Short version: yes, always, unless you want to alter expected behavior.
  
- **Practical Advanced Redux Webinar: Redux Middleware**  
  https://www.youtube.com/watch?v=DqWiuvuK_78  
  A recorded screenshare livestream that discusses the usefulness of Redux middleware, and demonstrates building middleware for fetching data, logging, and throttling.