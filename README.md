jQuery defaultText plugin by Weixi Yen

**_jQuery 1.4+ support_** only (uses 'delegate' method)

**DESCRIPTION**
defaultText is a jQuery plugin that sets values to empty
input fields.  It was built for code efficiency and minimal
DOM traversal.

**WHY**
Most defaultText implementations are not practical and
require more DOM traversals than necessary.  This plugin
focuses on speed and performance with event delegation options
by providing an optional 'context' parameter.

**USAGE:**
Give your <input /> tags a title attribute.

	<input type="text title="enter your username" />

Simple example:
	
	// Input field will now show "enter your username" when empty
	// Input field will have a css class of "default"
	// If you submit the form, the input will autoclear itself
	// After autoclearing, the input field will automatically re-insert the title value

	$.defaultText();

Example with options:

	// All input fields inside a form will have defaultText behavior
	// Empty inputs displaying defaultText will have a class of 'myClass'
	// When #button2 or .link are clicked, inputs with default text will clear itself.
	// Clearing allows for forms to be submitted without default text data.
	
	$.defaultText({
		context: 'form',
		css: 'myClass',
		clearEvents: [
			{selector: '#button2', type:'click'},
			{selector: '.link3', type:'click'}
		]
	});
