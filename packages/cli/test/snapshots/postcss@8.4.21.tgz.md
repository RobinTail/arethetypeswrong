# postcss@8.4.21.tgz

```
$ attw postcss@8.4.21.tgz -f table-flipped


postcss v8.4.21

❓ The JavaScript appears to set both module.exports and module.exports.default for improved compatibility, but the types only reflect the latter (by using export default). This will cause TypeScript under the node16 module mode to think an extra .default property access is required, which will work at runtime but is not necessary. These types should export = an object with a default property instead of using export default. https://github.com/arethetypeswrong/arethetypeswrong.github.io/blob/main/docs/problems/MissingExportEquals.md

🐛 Import resolved to types through a conditional package.json export, but only after failing to resolve through an earlier condition. This behavior is a TypeScript bug (https://github.com/microsoft/TypeScript/issues/50762). It may misrepresent the runtime behavior of this import and should not be relied upon. https://github.com/arethetypeswrong/arethetypeswrong.github.io/blob/main/docs/problems/FallbackCondition.md

🎭 Import resolved to a CommonJS type declaration file, but an ESM JavaScript file. https://github.com/arethetypeswrong/arethetypeswrong.github.io/blob/main/docs/problems/FalseCJS.md

❌ Import resolved to JavaScript files, but no type declarations were found. https://github.com/arethetypeswrong/arethetypeswrong.github.io/blob/main/docs/problems/UntypedResolution.md

🕵️ TypeScript allows ESM named imports of the properties of this CommonJS module, but they will crash at runtime because they don’t exist or can’t be statically detected by Node.js in the JavaScript file. Use -f json to see the list of exports TypeScript can see but Node.js cannot. https://github.com/arethetypeswrong/arethetypeswrong.github.io/blob/main/docs/problems/NamedExports.md


┌──────────────────────────────────┬───────────────────────┬───────────────────────┬────────────────────────────┬────────────────────────────┐
│                                  │ node10                │ node16 (from CJS)     │ node16 (from ESM)          │ bundler                    │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss"                        │ ❓ Missing `export =` │ ❓ Missing `export =` │ 🐛 Used fallback condition │ 🐛 Used fallback condition │
│                                  │                       │                       │ 🎭 Masquerading as CJS     │                            │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/at-rule"            │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/comment"            │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/container"          │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/css-syntax-error"   │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/declaration"        │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/fromJSON"           │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/input"              │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/lazy-result"        │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/no-work-result"     │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/list"               │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/map-generator"      │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/node"               │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/parse"              │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/parser"             │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/postcss"            │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
│                                  │                       │                       │ 🕵️ Named exports           │                            │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/previous-map"       │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/processor"          │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/result"             │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/root"               │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/rule"               │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/stringifier"        │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/stringify"          │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/symbols"            │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/terminal-highlight" │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/tokenize"           │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/warn-once"          │ ❌ No types           │ ❌ No types           │ ❌ No types                │ ❌ No types                │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/lib/warning"            │ ❓ Missing `export =` │ ❓ Missing `export =` │ ❓ Missing `export =`      │ ❓ Missing `export =`      │
├──────────────────────────────────┼───────────────────────┼───────────────────────┼────────────────────────────┼────────────────────────────┤
│ "postcss/package.json"           │ 🟢 (JSON)             │ 🟢 (JSON)             │ 🟢 (JSON)                  │ 🟢 (JSON)                  │
└──────────────────────────────────┴───────────────────────┴───────────────────────┴────────────────────────────┴────────────────────────────┘


```

Exit code: 1