# Key System Gui 💡🔥

Let's start the new Key System Gui
This Key system is very simple 

install Key system 

```lua
local gui = Instance.new("ScreenGui")
gui.Name = ""
gui.Parent = game.Players.LocalPlayer.PlayerGui

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 200, 0, 200)
frame.Position = UDim2.new(0.5, -100, 0.5, -100)
frame.BackgroundColor3 = Color3.new(0, 0, 1)
frame.BorderColor3 = Color3.new(0, 1, 0)
frame.BorderSizePixel = 2
frame.Active = true
frame.Draggable = true
frame.Parent = gui

local nameLabel = Instance.new("TextLabel")
nameLabel.Size = UDim2.new(1, 0, 0, 30)
nameLabel.Position = UDim2.new(0, 0, 0, -30)
nameLabel.Text = "key system Gui"
nameLabel.Parent = frame

local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(0, 150, 0, 30)
textBox.Position = UDim2.new(0.5, -75, 0.5, -60)
textBox.Parent = frame

local getKeyButton = Instance.new("TextButton")
getKeyButton.Size = UDim2.new(0, 100, 0, 30)
getKeyButton.Position = UDim2.new(0.5, -50, 0.5, -15)
getKeyButton.Text = "Get Key"
getKeyButton.BackgroundColor3 = Color3.new(1, 0.5, 0.5)
getKeyButton.Parent = frame

local loadButton = Instance.new("TextButton")
loadButton.Size = UDim2.new(0, 100, 0, 30)
loadButton.Position = UDim2.new(0.5, -50, 0.5, 30)
loadButton.Text = "Load"
loadButton.BackgroundColor3 = Color3.new(1, 0.5, 0.5)
loadButton.Parent = frame

local closeButton = Instance.new("TextButton")
closeButton.Size = UDim2.new(0, 30, 0, 30)
closeButton.Position = UDim2.new(1, -30, 0, 0)
closeButton.Text = "X"
closeButton.BackgroundColor3 = Color3.new(1, 0.5, 0.5)
closeButton.Parent = frame

getKeyButton.MouseButton1Click:Connect(function()
   local key = "Hello"
   setclipboard(key)
end)

loadButton.MouseButton1Click:Connect(function()
    local key = "Hello"
    if textBox.Text == key then
        print("Chave válida! Abrindo o arquivo original.")
        gui:Destroy()
    else
        print("Chave inválida!")
    end
end)

closeButton.MouseButton1Click:Connect(function()
    gui:Destroy()
end)
```
