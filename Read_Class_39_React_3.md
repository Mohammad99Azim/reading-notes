# React Context

### What is React context?
React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.


### When should you use React context?

React context is great when you are passing data that can be used in any component in your application.

These types of data include:

- Theme data (like dark or light mode)
- User data (the currently authenticated user)
- Location-specific data (like user language or locale)

Data should be placed on React context that does not need to be updated often.

Why? Because context was not made as an entire state management system. It was made to make consuming data easier.

You can think of React context as the equivalent of global variables for our React components.


## What problems does React context solve?

React context helps us avoid the problem of props drilling.

Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.

Here is an example of props drilling. In this application, we have access to theme data that we want to pass as a prop to all of our app's components. [link](https://www.freecodecamp.org/news/react-context-for-beginners/)


# Assets, Metadata, and CSS

[link](https://nextjs.org/learn/basics/assets-metadata-css/layout-component)

### Layout Component

create a Layout component which will be shared across all pages.

```
export default function Layout({ children }) {
  return <div>{children}</div>;
}
```


 add an import for the Layout component, and make it the outermost component:
 
 
 ```
 import Head from 'next/head';
import Link from 'next/link';
import Layout from '../../components/layout';

export default function FirstPost() {
  return (
    <Layout>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </Layout>
  );
}

 ```
#### Adding CSS

Now, let’s add some styles to the Layout component. To do so, we’ll use CSS Modules, which lets you import CSS files in a React component.

Create a file called components/layout.module.css with the following content:

```
.container {
  max-width: 36rem;
  padding: 0 1rem;
  margin: 3rem auto 6rem;
}
```

**Important: To use CSS Modules, the CSS file name must end with .module.css.**



Assets, Metadata, and CSS
Layout Component
First, let’s create a Layout component which will be shared across all pages.

Create a top-level directory called components.
Inside components, create a file called layout.js with the following content:
export default function Layout({ children }) {
  return <div>{children}</div>;
}
Then, open pages/posts/first-post.js, add an import for the Layout component, and make it the outermost component:

import Head from 'next/head';
import Link from 'next/link';
import Layout from '../../components/layout';

export default function FirstPost() {
  return (
    <Layout>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </Layout>
  );
}
Adding CSS
Now, let’s add some styles to the Layout component. To do so, we’ll use CSS Modules, which lets you import CSS files in a React component.

Create a file called components/layout.module.css with the following content:

.container {
  max-width: 36rem;
  padding: 0 1rem;
  margin: 3rem auto 6rem;
}
Important: To use CSS Modules, the CSS file name must end with .module.css.

To use this container class inside components/layout.js, you need to:

- Import the CSS file and assign a name to it, like styles
- Use styles.container as the className

Open components/layout.js and replace its content with the following:

```
import styles from './layout.module.css';

export default function Layout({ children }) {
  return <div className={styles.container}>{children}</div>;
}
```




