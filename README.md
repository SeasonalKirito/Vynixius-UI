


# Define Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SeasonalKirito/Vynixius-UI/main/Source.lua"))()
```
This will be defineing the library so it can be used.
# Create Window
```lua
local Window = Library:AddWindow({
	title = {"Vynixius", "UI Library"},
	theme = {
		Accent = Color3.fromRGB(0, 255, 0)
	},
	key = Enum.KeyCode.RightControl,
	default = true
})
```
This will be createing the window with all the instances and code.
# Create Tab
```lua
local Tab = Window:AddTab("Tab", {default = false})
```
This is createing a tab which will hold certain contents of your desire
# Create Section
```lua
local Section = Tab:AddSection("Section", {default = false})
```
This will create a section for certain stuff that is packed in a tab you defined.
# Create Button
```lua
local Button = Section:AddButton("Button", function()
	print("Button has been pressed")
end)
```
This will create a button that load a piece of code when interated with.
# Create Tab
```lua
local Toggle = Section:AddToggle("Toggle", {flag = "Toggle_Flag", default = false}, function(bool)
	print("Toggle set to:", bool)
end)
```
This will create a toggle which and can let a piece of code only run when its true.
# Create Label
```lua
local Label = Section:AddLabel("Label")
```
This will create a label with the desired text in it.
# Create DualLabel
```lua
local DualLabel = Section:AddDualLabel({"Dual", "Label"})
```
This will create a label with a label to the side of it.
# Create ClipboardLabel
```lua
local ClipboardLabel = Section:AddClipboardLabel("ClipboardLabel", function()
	return "ClipboardLabel"
end)
```
This will create a label and when interacted with it will copy a desired text to the users clipboard
# Create TextBox
```lua
local Box = Section:AddBox("Box", {fireonempty = true}, function(text)
	print(text)
end)
```
This will put whatever you type into the box into the text bool and you can use it for things.
# Create Bind
```lua
local Bind = Section:AddBind("Bind", Enum.KeyCode.RightShift, {toggleable = true, default = false, flag = "Bind_Flag"}, function(keycode)
	Window:SetKey(keycode)
end)
```
This will set when ever you press the keybind it will run the piece of code desired.
# Create Slider
```lua
local Slider = Section:AddSlider("Slider", 1, 100, 50, {toggleable = true, default = false, flag = "Slider_Flag", fireontoggle = true, fireondrag = true, rounded = true}, function(val, bool)
	print("Slider value:", val, " - Slider toggled:", bool)
end)
```
This will have a value binded to a slider and you could use this for example with a walkspeed bypasss.
# Create Dropdown
```lua
local Dropdown = Section:AddDropdown("Dropdown", {"Item1", "Item2", "Item3"}, {default = "Item1"}, function(selected)
	print(selected)
end)
```
This will have multiple options in a dropdown and you can choose which one you want.
# Color Picker
```lua
local Picker = Section:AddPicker("Picker", {color = Color3.fromRGB(255, 0, 0)}, function(color)
	Window:SetAccent(color)
end)
```
This will set the color of your desinated path.
