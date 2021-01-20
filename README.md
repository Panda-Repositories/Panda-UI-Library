# Panda UI Library Documentation
### *By Panda Technologies*

[![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](http://commonmark.org)

![Lua](https://img.shields.io/badge/Made%20With-Lua-blue)

![Discord](https://img.shields.io/discord/761754005906653245)

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/SkieAdmin/Panda-Respiratory/graphs/commit-activity)

---
### Load the UI Library
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SkieAdmin/Panda-Respiratory/main/Script/Libraries/Core"))()
```
---
### Add windows
```lua
local window = library:Window("Window")
```
---
### Add button
```lua
--example, callback

window:Button("Button name", function()
   print("pressed button")
end)
```
---
### Add toggle
```lua
--Name of the toggle, default state of the toggle, callback

window:Toggle("Example toggle", true, function(bool)
    print(bool) -- bool is true or false depending on the state of the toggle
end)
```
### Add color picker
---
```lua
--Name, default color (set to true to make the default rainbow), callback

window:ColorPicker("Color Picker", Color3.fromRGB(255, 255, 255), function(color)
   print(color)
end)
```
---
### Add slider
```lua
--Name of slider, minimum value, maximum value, default value, callback

window:Slider("Example Slider",0,100,20, function(value)
   print(value)
end)
```
---
### Add label
```lua
-- Text, color: setting color to true will give it a rainbow effect!

window:Label("Credits to SkieHacker and Intrer#0421", Color3.fromRGB(127, 143, 166))
```
---
### Add input box
```lua
-- Name, callback

window:Box("Walkspeed", function(text, focuslost)
   if focuslost then
   print(text)
   end
end)
-- The callback will be called with two arguments, the text that the player inputted and whether the player has stopped writing
```
---
### Add dropdown
```lua
-- Name, table with names of the button that you want, callback that will be called with the name of the button that was pressed

local dropdown = window:Dropdown("Example dropdown", {"Button 1", "Button 2", "Third button"}, function(name)
   print(name)
end)
```
#### Add buttons to dropdown
```lua
-- Name

dropdown:Button("New button")
```
#### Remove buttons from dropdown
```lua
-- Name

dropdown:Remove("Button")
```
---
### Add keybind to UI
```lua
-- Key

library:Keybind("P")
```
---
### Destroy UI
```lua
library:Destroy()
```
