---
title: Demo: Code blocks
category: Site Guide
summary: Fenced code boxes with colored languages and a Copy button, and inline code.
authors: tau
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## A code box

Three backticks open a box and three close it. The name of a language after the opening backticks colors the code, and every box has a **Copy** button and shows the language in its bar.

```lua
-- a Lua example
local function greet(name)
  return "Hello, " .. name
end
print(greet("Iliac Bay"))
```

```json
{ "mod": "example", "version": 2, "enabled": true, "tags": ["ui", "audio"] }
```

```python
def renown(level):
    return level * 2 + 1
```

```bash
git clone https://github.com/example/mods.git
cd mods && ls -la
```

## No language

A box with no language shows the text as it is, uncolored:

```
Plain text.
    Indentation is kept.
```

## Tildes and longer fences

Three tildes work the same. A fence of four backticks lets the box hold a line of three:

````markdown
```lua
print("a box inside a box")
```
````

## Unknown language

A language the site does not color is shown plain, and the page check mentions it:

```madeup
this is not colored
```

## The languages the site colors

Each box below was written with the name shown in its top bar.

```powershell
# list the save files
Get-ChildItem -Path "C:\Games\Saves" -Recurse | Where-Object { $_.Length -gt 1MB }
```

```bat
@echo off
REM start the game
set GAME=daggerfall.exe
if exist "%GAME%" start "" "%GAME%"
```

```ini
; display settings
[Graphics]
resolution = 1920
fullscreen = true
```

```yaml
# a mod list
name: my-mod
mods:
  - audio-pack
  - map-fix
enabled: true
```

```js
// log a message
function greet(name) { return console.log("Hello, " + name); }
```

```cs
// a message
public class Greeter { public void Greet(string name) { Console.WriteLine($"Hello {name}"); } }
```

```xml
<!-- a config file -->
<settings enabled="true"><volume>80</volume></settings>
```

```markdown
## A heading
Some **bold** words, a `code` word, a [[Guide page]] link and a {{W}} key.
- a list item
```
