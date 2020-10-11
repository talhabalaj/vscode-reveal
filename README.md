# VScode Reveal

## Features

Dims text after the selection by reducing the opacity of the text. 

Set a keybinding for `reveal.ToggleReveal`, search `Toggle Reveal` in the command palette, or use the `reveal.enabled` setting.

By default the extension will dim all lines after cursor. Use the `reveal.context` setting to show N lines after un-dimmed. 

![Context](images/context.gif)  

## Configuration

```
"reveal.enabled": {
    "default": false,
    "description": "When set to true, the extension will dim non-selected text."
},
"reveal.toggleRevealCommandScope": {
    "defualt": "user",
    "description": "Decides whether the `ToggleReveal` command will affect the user (global) or workspace (local) settings."
},
"reveal.opacity": {
    "default": 50,
    "description": "An integer between 0 and 100 used for the opacity percentage for the dimmed (non-selected) text."
},
"reveal.context": {
    "default": 0,
    "description": "Number of lines before and after the current line that are not dimmed. 0 will dim everything but lines with a selection and a negative number will dim everything except the curent selection. Defaults to 0."
},
"reveal.delay": {
    "default": 0,
    "description": "Delay in milliseconds for dimming the non-selected text to reduce number of API calls in the event of rapid selection changes. Defaults to 0, but set higher if it feels like it is causing problems."
}
```

### 2.0.0
- Dim on editor change (e.g. ctrl+tab). Thanks @roblourens
- Highlight context (n lines before/after). Thanks @rebornix
- Breaking: `reveal.dimSelectedLines` has been replaced by `reveal.context`. 

### 1.0.0

Initial release