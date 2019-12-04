# `react-use-is-scrolling`

A simple React hook to track whether or not the window is currently being scrolled.

```tsx
const ScrollIndicator:React.FunctionComponent = () => {
  const { isScrolling } = useIsScrolling()
  return (
    <div>{isScrolling ? "scrolling" : "stopped"}</div>
  )
}
```

**Note** - This is not a hook to track the current scroll position. For that, you can check out libraries like [`react-use-scroll-position`](react-use-scroll-position).

There are some other properties that can be used to track 

```ts
const {
  isScrolling, // boolean, true if currently scrolling
  isScrollingX, // boolean, true if scrolling horizontally
  isScrollingY, // boolean, true if scrolling vertically
  scrollDirectionX, // 'none', 'left', 'right'
  scrollDirectionY, // 'none', 'up', 'down'
} = useIsScrolling()
```

## Usage

### Install the Library

```sh
yarn add react-use-is-scrolling
```

or

```sh
npm install react-use-is-scrolling
```

### Use the Hook


```tsx
import { useIsScrolling } from 'react-use-is-scrolling'

const ScrollIndicator:React.FunctionComponent = () => {
  const { isScrollingX, isScrollingY, scrollDirectionX, scrollDirectionY } = useIsScrolling()
  return (
    <>
      {isScrollingX && (<div>Scrolling: {scrollDirectionX}</div>)}
      {isScrollingY && (<div>Scrolling: {scrollDirectionY}</div>)}
    </>
  )
}
```
