## Vue.js

- Vuejs is a JavaScript **FRAMEWORK** used for building user interfaces, particularly for single-page applications (SPAs). It is designed to be incrementally adaptable and can be easily integrated into other projects.

### Why Vue.js?

#### Ease of Learning

- VueJs is known for its simplicity and ease of learning, making it a great choice for beginners in web development.

#### Flexibility

- Vues is designed to be incrementally adaptable. You can use as much or as
  little of it as you need in your project.

#### Component-Based Architecture

- Vues promotes a component-based architecture, which is a widely adopted
  and efficient way to build user interfaces.

#### Reactivity

- Vues provides a reactive data-binding system, simplifying the process of
  keeping the Ul in sync with the application state.

#### Growing Ecosystem

- Vue.js has a growing ecosystem of libraries, tools, and plugins developed by the community.

#### Performance

Vues is designed with performance in mind. Its reactivity system and virtual
DOM help optimize rendering, making it suitable for building efficient and
fast applications.

#### Job Opportunities

As Vue js gains popularity, the demand for developers with Vue.js skills is
increasing. Learning Vue.js can enhance your job prospects, especially if
you're interested in working on modern web development projects.

#### Integration with Other Technologies

Vue js can be easily integrated with other libraries and frameworks. For
example, you can use Vue.js alongside Vuex for state management or Vue
Router for routing.

### What Is Component?

- A component is a reusable and self-contained unit that encapsulates a
  specific piece of functionality or user interface. Components are a
  fundamental building block of Vue applications, and they allow you to
  organize and structure your code in a modular way.

#### Why Components?

##### Modularity

- Components allow you to break down your application into smaller, reusable
  pieces. Each component is responsible for a specific feature or functionality,
  making it easier to understand and maintain your code.

##### Reusability

- Components can be reused across different parts of your application or even
  in multiple projects. This reusability reduces redundancy in your code and
  speeds up development.

##### Maintainability

- With components, it's easier to manage and maintain your codebase. Each
  component is a self-contained unit with its own functionality, making it
  simpler to troubleshoot and update.

### Text Interpolation {{}}

- Text interpolation in refers to the process of dynamically `binding data` to the content of an HTML element in your template. It allows you to display the value of a JavaScript expression or a variable within the markup.

```javascript
syntax;
{
  {
    data;
  }
}
```

#### Attribute Bindings :

Attribute binding is a way to bind HTML `attributes` to data in Vue instance.

- old Way

  - v-bind:attr

- new way
  - :attr

### Day1

- 00:00 - Intro
- 00:16 - What is Vue.js?
- 03:10 - Side Talk
- 05:28 - Installations
- 10:46 - Folder Structure
- 18:32 - Component In Depth
- 32:43 - Text Interpolation
- 38:55 - Attribute Bindings
- 44:48 - Dynamic Bindings
- 47:17 - Styling In Depth

---

#### Reactivity?

- Reactivity means that the framework can automatically update ( Ul) when the information behind it changes. It's a core concept that allows you to create `dynamic` and `Responsive` applications without manually manipulating the DOM.

### Way to achive Reactive State.

- reactive()
- ref()

#### reactive()

- The reactive function is used to create reactive objects. A
  reactive object is an object where changes to its properties
  are automatically detected, `(triggering updates)` in the user
  interface. It is a way to make an object "reactive" in Vue.js.

- Can't store primitive data types

#### ref()

- ref() is used to create a reactive reference to a value. Unlike
  the reactive function, which is used for creating reactive
  objects, ref is specifically designed for creating reactive `single values`

- You can store any value you want

### Computed Properties

- A computed property is a special kind of variable that `automatically updates` itseif whenever the data it depends on changes.

- It's like a little worker that watches certain data, performs some work on it, and always gives you the most up-to-date result.

### Conditional Rendering

- Conditional rendering is refers to the ability to
  conditionally display or hide elements in the user
  interface based on certain `conditions` OR `Expressions`

- v-if( `condition`)
- v-else-if( `condition`)
- v-else
- v-show

#### v-show

- v-show directive is used for conditional rendering. It toggles the visibility of an element based on the truthiness of the provided expression. Unlike v-if, which completely adds or removes the element from the DOM, v-show toggles the CSS display property of the element to control its visibility while keeping it in the DOM.

### List Rendering

#### v-for

- The v-for directive is used to `iterative over` an array or an object and render a template for each item in the collection.

##### Efficient DOM Updates

- When Vue renders a list of elements, it uses a virtual DOM to determine the most
  efficient way to update the actual DOM. The key helps Vue identify which elements
  have changed, been added, or been removed.

- Without keys, Vue may need to recreate the entire DOM structure for each update,
  which can be less efficient

##### Avoiding Common Pitfalls

- Using key can help avoid common pitfalls, such as duplicate key warnings in the
  console or incorrect rendering when items are rearranged in the list.

- Vue relies on keys to track the identity of elements, and using unique keys for each
  item ensures that Vue can accurately update the DOM based on changes in the list.

### Day2

- 1:00:08 - Event Handlers In Vue
- 1:11:33 - Reactivity & Reactive
- 1:19:40 - ref()
- 1:29:34 - Computed Properties
- 1:35:12 - Conditional Rendering
- 1:50:18 - v-for

### v-model

- v-model is a directive that provides two-way data binding on an input, textarea, or select element. It creates a `Connection` between the data in your component and the input field, allowing changes in one to automatically update the other and vice versa.

#### Two Way Binding?

- Two-way binding means that changes irt your code `automatically` update what you see on the screen, and vice versa. It's like a live
  connection between your data and the user interface, making it easy to keep them in sync without writing a lot of extra code.

### Props?

- "props" (short for properties) are a way to pass data from a parent component to child component. Props allow you to communicate between components by allowing the parent component to pass data down to its child components. This is useful for creating reusable and modular components.

- Props are immutable. we cannot change props value

### Component Event?

- Component events are a way for child components to
  communicate with their `parent components`. They allow
  child components to emit events (custom events) that can be listened to and handled by their parent components.

#### Child Component Emits an Event

- Inside a child component, you can use the $emit method to trigger a custom event. This event can carry data that you want to send to the parent.

#### Parent Component Listens to the Event

- In the parent component's template, you can use the v-on directive (or the shorthand @) to listen for the custom event emitted by the child.

### Slot

- A slot is like `space in a component` here you can put
  different things. It allow you to create reusable components that can accept different content while maintaining a consistent structure.

#### Fallback / Default Content

- Fallback content in slots refers to the default content that is displayed when no content is provided for a particular slot. It's a way to ensure that a component still has `meaningful content`, even if the parent component does not pass any content to a specific slot.

#### Named Slots

- A named slot is a way to assign a specific name to a slot in a component. Unlike the default slot, which is unnamed and used when no explicit name is provided, named slots allow you to have multiple slots in a component and specify where the content should be inserted based on the slot's name.

### Day3

- 2:11:57 - v-model
- 2:18:58 - Props
- 2:46:16 - Component Event
- 2:56:04 - Slots
- 3:07:16 - Provide & Inject
