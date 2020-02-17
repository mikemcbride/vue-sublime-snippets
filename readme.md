# Vue Sublime Snippets

Useful snippets for working on Vue.js applications in Sublime Text 3. It is a port of my [Vue snippets for Atom](https://github.com/mikemcbride/vuejs-atom-snippets.git). 

## Install

Clone or download the repo, then copy the snippets into your Sublime User Packages folder. On macOS that should be something like:

```
~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User/
```

## The Snippets

### Vue Single File Components

> Scope for these is within a `.vue` file.

| Command | Output |
| ------- | ------ |
| `vscaffold` | Scaffolds out a full Vue SFC with the options I am most likely to use. Options are ordered according to the Vue styleguide to prevent lint errors. |
| `vbase` | Scaffolds out a Vue SFC with just a name. |
| `vimport` | Imports a local Vue component. `import MyComponent from '@/components/MyComponent'` |
| `vcomponents` | Sets up the `components` option |
| `vfilters` | Sets up the `filters` option |
| `vprops` | Sets up the `props` option |
| `vdata` | Sets up the `data` option |
| `vcomputed` | Sets up the `computed` option |
| `vwatchers` | Sets up the `watch` option |
| `vcreated` | Sets up the `created` hook |
| `vmounted` | Sets up the `mounted` hook |
| `vdestroyed` | Sets up the `destroyed` hook |
| `vmethods` | Sets up the `methods` option |

### Vuex

> Scope for these is a JavaScript file.

| Command | Output |
| ------- | ------ |
| `vstore` | A blank slate Vuex store setup. |
| `vmodule` | A full Vuex module, with state, getters, actions, and mutations. |

### Transitions

This one is a little different because it needs to be able to be executed in multiple contexts. This snippet should work in any CSS, SCSS, Sass, or LESS file as well as within the `<style>` block of a Vue SFC.

Command: `vtransition` scaffolds out this block of code:

```css
.${1:transition-name}-enter-active,
.${1:transition-name}-leave-active {
	${2:transition}: ${3:all} ${4:.2s} ${5:ease};
}

.${1:transition-name}-enter,
.${1:transition-name}-leave-to {
  ${6:property}: ${7:value};
}
```

## License

MIT
