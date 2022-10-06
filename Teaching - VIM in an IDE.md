---
theme: consult
height: 540
margin: 0
maxScale: 4
---

<!-- slide template="[[footer]]" -->

# Teaching - VIM in an IDE
## Introduction

This is a short teaching how to use VIM in an IDE. 


::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
:::

---

<!-- slide template="[[agenda]]" -->
::: title
## Agenda
::: 

::: left
1. Installation
2. Setting and config
3. Usage examples
4. Special commands 
5. Plugins
::: 

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
::: 

---

<!-- slide template="[[tpl-con-2-1-box]]" -->
::: title
### Installation
:::

::: left
![[Marketplace.png|1500]]
:::

::: right
- For this demo I have chosen the VIM integration in Eclipse.   
- The VIM Plugin for Eclipse is called **Vrapper** .  
- The installation can be performed via the Eclipse Marketplace. 
- _additional: The **Relative Line Number** plugin can be also helpful_
:::

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
::: 

---

<!-- slide template="[[tpl-con-2-1-box]]" -->

::: title
## Settings
::: 

<style>
.scaled-picture { 
   height: 38%;
}
</style>

::: left
![[vrapperrc_file.png]]<!-- element class="scaled-picture" -->
![[vrapperrc.png]]
::: 

::: right
- Configuration of the Vrapper plugin 
	- via .vrapperrc file (_vrapperrc for Windows ) in your home directory
- [Documentation](https://vrapper.sourceforge.net/documentation/?topic=configuration)
:::

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
:::

---

<!-- slide template="[[tpl-con-2-1-box]]" -->
::: title
## Example - Create artifact ( program / class ... )
::: 

::: left
![[package_tabnew.png]]
::: 

::: right
- create a new package in Eclipse
	- using ` :tabnew `
- select: ` ABAP Package `
- adding a package name
- if needed add the super package
::: 

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
:::

---

<!-- slide template="[[tpl-con-2-1-box]]" -->
::: title
## Example - Moving code at place
:::

::: left
![[move_code.png]]
:::

::: right
- move methods ( setup ) to the appropriate place
	- select Block `SHFIT + V`
	- move to line 189 `:m189`
- copy code below the current line
	- copy line 25 till 29 `25,29t.`
:::

---

<!-- slide template="[[tpl-con-2-1-box]]" -->
::: title
## Example - Navigating in code
:::

::: left
![[implement_method.png]]
:::

::: right
- test method -> create implementation
	- write test method phrase
	- jump back to name `SHIFT + F _`
	- press `ALT + 1` for Quick Assist
:::

---

<!-- slide template="[[agenda]]" -->
::: title
## Special commands
::: 

::: left

| Command     | Description                         |
| ----------- | ----------------------------------- |
| `:regs`     | open the registers overview         |
| `:tabnew`   | create a new programming artifact   |
| `:only`     | close all tabs expect the current   |
| `:marks`    | list all marks                      |
| `gt` / `gT` | switches to the next / previous tab |
|             |                                     |

:::

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
::: 

---

<!-- slide template="[[tpl-header_with_2_panes]]" -->
::: title
## Plugins
:::

For the Vrapper plugin in Eclipse exists plugins itself. I will mention just 2 of the best.  
The installation of the plugins takes also place in the marketplace view or via update function of an already installed Vrapper instance.  

::: right
#### Split editor plugin
The split editor plugin enables the user to add split in the editor window with VIM command line commands. Some of them are described below.  
| Command    | Description                                       |
| ---------- | ------------------------------------------------- |
| `CTRL+W v` | creates a vertical split inside the code editor   |
| `CTRL+W s` | creates a horizontal split inside the code editor |
| `CTRL+W w` | switches between the splits                       |
| `CTRL+W o` | close other split                                 |   
::: 

::: left
#### Surround VIM
The surround vim plugin provides the ability to surround particular texts with special characters ( e.g. braces, parentheses etc.)
| Command | Description                                                         |
| ------- | ------------------------------------------------------------------- |
| `ysi((` | add a new pair of parentheses inside the current parentheses        |
| `csm|"` | surround the text inside the pipes with quotes instead of the pipes |
| `cs"}`  | change the surrounding quotes against braces                        |
| `ds{`   | delete surrounding braces                                                                    |
:::

::: footer
##### Teaching - VIM in an IDE - Matthias Bartsch
:::