---
tags:
  - web
  - dev
---
[https://www.learnui.design/blog/spice-up-designs.html](https://www.learnui.design/blog/spice-up-designs.html)

# Modules
- For splitting files

## import
`import defaultExport from "module-name";`
`import { export1, export2 } from "module-name";`

- Read-only live bindings
	- Exported from another module
- Come in strict mode

### Dynamic Import
- Conditionally or on demand

`import('/modules/module.js')`
	`.then((module) => {`
		`// Do something`
	`});`

`let module = await import('/modules/module.js');`

## Export
- Stick in front of statements

`export const name = 'square';`
`export function …`
`export { name, draw, reportArea, reportPerimeter };`