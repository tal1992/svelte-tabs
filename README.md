# svelte-tabs

- The Lightest, fastest and latest version of svelte-tabs.
- UnPacked size reduced to 5.7kb from 68kb in original.
- Packed size reduced to 2.4kb from 25kb in original.

## Installation

    npm install --save svelte-tabs-lite

## Basic usage

```html
<script>
  import { TabContainer, Option, TabNav, Description } from 'svelte-tabs-lite';
</script>

<TabContainer>
  <TabNav>
    <Option>One</Option>
    <Option>Two</Option>
    <Option>Three</Option>
  </TabNav>

  <Description>
    <h2>This is Tab One</h2>
  </Description>

  <Description>
    <h2>This is Tab Two</h2>
  </Description>

  <Description>
    <h2>This is Tab Three</h2>
  </Description>
</TabContainer>
```

## Props

- `selectedTabIndex` (number): The index of the tab to initially select, when the Tabs component is mounted.

## Overriding styling

svelte-tabs-lite is the light version of svelte-tabs and it comes with a basic default style, but it can be overridden. To override the styles to use your own, you will need to use global styles that have a higher specificity than the built-in styles.

To make sure your overridden styles have the most specificity, include the parent class `.svelte-tabs` in your selector, and include the element type (see below). An example selector would be `:global(.svelte-tabs li:focus)`.

Below are CSS selectors that can be used for the different components in this library:

- Tabs: `:global(.svelte-tabs)`
- Tab: `:global(.svelte-tabs li.svelte-tabs__tab)`
- Selected Tab: `:global(.svelte-tabs li:focus)`
- TabPanel: `:global(.svelte-tabs div.svelte-tabs__tab-panel)`

As a last resort, if you can't get the right specificity, you can always use `!important`.