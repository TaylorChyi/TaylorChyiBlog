---
title: Fold Level
date: 2023-04-23
tags: 
- VSCode 
- ExtensionPack 
---

时间：2023-04-19
标签： #VSCode #ExtensionPack 

---

# Usage & Commands

Set shortcuts:
1. Press
    -   Mac: `Command + Shift + p`
    -   Win: `Ctrl + Shift + p`
2.  `Open Keyboard Shortcuts File`
3. Append:

```json
{    
	"key": "alt+1",    
	"command": "vikyd.FoldLevel.level1"
},
{    
	"key": "alt+2",    
	"command": "vikyd.FoldLevel.level2"
},
{    
	"key": "alt+3",    
	"command": "vikyd.FoldLevel.level3"
},
{    
	"key": "alt+4",    
	"command": "vikyd.FoldLevel.level4"
},
{    
	"key": "alt+5",    
	"command": "vikyd.FoldLevel.level5"
},
{    
	"key": "alt+6",    
	"command": "vikyd.FoldLevel.level6"
},
// ↓  optional
{    
	"key": "alt+-",    
	"command": "editor.foldAll"
},
// ↓  optional
{    
	"key": "alt+=",    
	"command": "editor.unfoldAll"
}
```