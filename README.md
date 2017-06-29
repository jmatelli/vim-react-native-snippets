# Vim React Native Snippets

A Vim snippet library for React Native in ES6. You may also want to check out [vim-es2015-snippets](https://github.com/epilande/vim-es2015-snippets).

Requires [UltiSnips](https://github.com/SirVer/ultisnips).

## Installation

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
" React Native code snippets
Plug 'tellijo/vim-react-native-snippets'
```

## Usage
In a JavaScript or JSX file, type a trigger name while in Insert mode, then press Ultisnips trigger key. In my case I have it mapped to `<C-l>`.

For example, let's say we have `ListItem.js`

In Insert mode

```javascript
rncc<C-l>
```

Will expand to

```javascript
import React, { Component } from 'react'
import { PropTypes } from 'prop-types'
import { View, StyleSheet } from 'react-native'
import styles from './ListItem.css'

class ListItem expends Component {
	static propTypes = {
		children: PropTypes.node,
		className: PropTypes.string
	}
	
	constructor(props) {
		super(props);
	}

	render() {
		return (
			<View style={styles.container}>
				
			</View>
		);
	}
}

const styles = StyleSheet.create({
	container: {}
})

export default ListItem
```

Check out [`UltiSnips/javascript.snippets`](UltiSnips/javascript.snippets) to see all snippets.


## Snippets

#### Skeleton

| Trigger  | Content |
| -------: | ------- |
| `rrcc→`  | React Native Class Component |
