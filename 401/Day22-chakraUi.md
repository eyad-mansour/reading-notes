## What is a Chakra UI?

Chakra UI is a component-based library. It's made up of basic building blocks that can help you build the front-end of your web application.

It is customizable and reusable, and most importantly it supports ReactJs, along with some other libraries too.

## Is Chakra UI better than material UI?

The Material UI React library provides users with a handful of UI layout tools but is most famous for its large breadth of pre-styled UI components to which developers can apply custom styles to override out-of-the-box base styles. Chakra UI is a more robust, layout-focused library that also provides developers with UI components similar to those that Material UI provides, but has a greater focus on the creation of flexible, composable, and scalable code.

## How to use Chakra UI?

`npm i @chakra-ui/react @emotion/react@^11 @emotion/styled@^11 framer-motion@^4`

For ChakraUI to get initialised you first need to add <ChakraProvider> in your index.js file.

```import React from "react"

// 1. import `ChakraProvider` component
import { ChakraProvider } from "@chakra-ui/react"

function App({ Component }) {
// 2. Use at the root of your app
return (
<ChakraProvider>
<Component />
</ChakraProvider>
)
}
```
