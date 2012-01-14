#Solving the Option + Space in OS X pain
Developing on OS X has its upsides but also a few downsides. I've been tearing my hair at one obscure downside for quite some time now. Imagine the following code block:

	if(foo == 'bar') {
		//Baz
	}

On a swedish keyboard you need to use Option + Shift 8 to produce a {. If you mistakenly press Option before the space between ) and {, you get a non-breaking space instead. This will of course cause syntax errors and can be pretty hard to track down, especially without "Show Invisible Characters" enabled in your `$EDITOR` of choice. The same issue can of course occur in other places than `) {`, but that's been the most common case for me.

Thankfully, this is easily fixable. You need to edit your `DefaultKeyBinding.dict` file located in your `~/Library/KeyBindings` folder. If you haven't edited that file before, you likely won't have a `KeyBindings` folder. Once that's created, create (or append) your `DefaultKeyBinding.dict` with the following content:

	{
	"~ " = ("insertText:", " ");
	}

This will tell all Cocoa apps to detect the non-breaking space key event and instert a regular space instead. You might need to restart the Cocoa apps you want this to work in.

If you want to read more about Cocoa Keybindings, check out this informative page: ["Customizing the Cocoa Text System"](http://www.hcs.harvard.edu/~jrus/site/cocoa-text.html)