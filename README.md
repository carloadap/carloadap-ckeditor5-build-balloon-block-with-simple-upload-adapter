CKEditor 5 balloon block editor build
==============================================

[![Join the chat at https://gitter.im/ckeditor/ckeditor5](https://badges.gitter.im/ckeditor/ckeditor5.svg)](https://gitter.im/ckeditor/ckeditor5?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-balloon-block.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-build-balloon-block)
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-build-balloon-block/status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-balloon-block)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-build-balloon-block/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-balloon-block?type=dev)

The balloon editor build for CKEditor 5. Read more about the [balloon editor build](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/overview.html#balloon-block-editor) and see the [demo](https://ckeditor.com/docs/ckeditor5/latest/examples/builds/balloon-block-editor.html).

![CKEditor 5 balloon editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-balloon-block.png)

## Documentation

See:

* [Installation](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/installation.html) for how to install this package and what it contains.
* [Basic API](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/basic-api.html) for how to create an editor and interact with it.
* [Configuration](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/configuration.html) for how to configure the editor.
* [Creating custom builds](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/development/custom-builds.html) for how to customize the build (configure and rebuild the editor bundle).

## Quick start

First, install the build from npm:

```bash
npm install --save @ckeditor/ckeditor5-build-balloon-block
```

And use it in your website:

```html
<div id="editor">
	<p>This is the editor content.</p>
</div>
<script src="./node_modules/@ckeditor/ckeditor5-build-balloon-block/build/ckeditor.js"></script>
<script>
	BalloonBlockEditor
		.create( document.querySelector( '#editor' ) )
		.then( editor => {
			window.editor = editor;
		} )
		.catch( err => {
			console.error( err.stack );
		} );
</script>
```

Or in your JavaScript application:

```js
import BalloonEditor from '@ckeditor/ckeditor5-build-balloon-block';

// Or using the CommonJS version:
// const BalloonBlockEditor = require( '@ckeditor/ckeditor5-build-balloon-block' );

BalloonBlockEditor
	.create( document.querySelector( '#editor' ) )
	.then( editor => {
		window.editor = editor;
	} )
	.catch( err => {
		console.error( err.stack );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application, it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Advanced setup guide](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/advanced-setup.html).

**Note:** We recommend to adjust the position of the block toolbar button using CSS (see the example below) to your liking. By default, the block toolbar button will be attached directly to the boundary of the editable content area.

```html
<style>
	/* Give the block toolbar button some space, moving it a few pixels away from the editable area. */
	.ck.ck-block-toolbar-button {
		transform: translateX( -10px );
	}
</style>
```

**Note:** You can configure the block toolbar items using the {@link module:core/editor/editorconfig~EditorConfig#blockToolbar `config.blockToolbar`} option.

## License

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the `LICENSE.md` file.
