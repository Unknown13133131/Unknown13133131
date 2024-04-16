-- Noxulico Hub ❄️ - Source code

wait(1.2)

game.StarterGui:SetCore("SendNotification", {

Title = "Credits"; -- the title (ofc)

Text = "Auto Parry 100% Made by SumitScripts,"; -- what the text says (ofc)

Icon = ""; -- the image if u want.

Duration = 5; -- how long the notification should in secounds

})

local Library = loadstring(Game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()

local Window = Library:NewWindow("Noxulico Hub ❄️")
local Section = Window:NewSection("Made by SumitScripts")

Section:CreateToggle("Auto Parry V1", function(value)
getgenv().config = getgenv().config or {
    hit_time = 0.5, -- // recommended 0.25 to 0.75 \ --
 
    mode = 'Always', -- // Hold , Toggle , Always \ --
    deflect_type = 'Remote', -- // Key Press , Remote \ --
    notifications = true,
    keybind = Enum.KeyCode.V
}
 
loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3ABlade%20Ball%20Parry%20V4.0.0",true))()
print(value)
end)

Section:CreateToggle("Auto Parry V2", function(value)
loadstring(game:HttpGet(('https://scriptblox.com/raw/Blade-Ball-Opensource-autoparry-8123'),true))()
print(value)
end)

Section:CreateDropdown("Parry Mod", {"TryHard", "Normal",}, 2, function(text)
print(text)
end)

Section:CreateButton("OP Manual Spam", function()
local gui, frame, button = Instance.new("ScreenGui", game.CoreGui), Instance.new("Frame"), Instance.new("TextButton")
gui.ResetOnSpawn = false
frame.Size, frame.Position, frame.BackgroundColor3, frame.BorderSizePixel, frame.Active, frame.Draggable, frame.Parent = UDim2.new(0, 150, 0, 75), UDim2.new(0, 10, 0, 10), Color3.new(0, 0, 0), 0, true, true, gui
button.Text, button.Size, button.Position, button.BackgroundColor3, button.BorderColor3, button.BorderSizePixel, button.Font, button.TextColor3, button.TextSize, button.Parent = "Manual spam", UDim2.new(1, -20, 1, -20), UDim2.new(0, 10, 0, 10), Color3.new(0, 0, 0), Color3.new(), 2, Enum.Font.SourceSans, Color3.new(1, 1, 1), 16, frame

local activated = false

local function toggle()
    activated, button.Text = not activated, activated and "Off" or "On"
    
    while activated do
        local args = {1.5, CFrame.new(-254.29, 112.14, -119.27) * CFrame.Angles(-2.03, 0.57, 2.31), {["2617721424"] = Vector3.new(-273.40, -724.80, -20.92)}, {910, 154}}
        game:GetService("ReplicatedStorage").Remotes.ParryAttempt:FireServer(unpack(args))
        game:GetService("RunService").Heartbeat:Wait()
        button.BorderColor3 = Color3.new(math.random(), math.random(), math.random())
    end
end

local function showNotification()
    game.StarterGui:SetCore("SendNotification", {Title = "Manual Spam", Text = "Made By SumitScripts", Duration = 5})
end

button.MouseButton1Click:Connect(function()
    toggle()
    showNotification()
end)
print("Clicked")
end)

Section:CreateButton("Fps Booster", function()
-- Made by RIP#6666
_G.Settings = {
    Players = {
        ["Ignore Me"] = true, -- Ignore your Character
        ["Ignore Others"] = true -- Ignore other Characters
    },
    Meshes = {
        Destroy = false, -- Destroy Meshes
        LowDetail = true -- Low detail meshes (NOT SURE IT DOES ANYTHING)
    },
    Images = {
        Invisible = true, -- Invisible Images
        LowDetail = false, -- Low detail images (NOT SURE IT DOES ANYTHING)
        Destroy = false, -- Destroy Images
    },
    ["No Particles"] = true, -- Disables all ParticleEmitter, Trail, Smoke, Fire and Sparkles
    ["No Camera Effects"] = true, -- Disables all PostEffect's (Camera/Lighting Effects)
    ["No Explosions"] = true, -- Makes Explosion's invisible
    ["No Clothes"] = true, -- Removes Clothing from the game
    ["Low Water Graphics"] = true, -- Removes Water Quality
    ["No Shadows"] = true, -- Remove Shadows
    ["Low Rendering"] = true, -- Lower Rendering
    ["Low Quality Parts"] = true -- Lower quality parts
}
loadstring(game:HttpGet("https://raw.githubusercontent.com/CasperFlyModz/discord.gg-rips/main/FPSBooster.lua"))()
print("Clicked")
end)

Section:CreateButton("Speed up", function()
game.StarterGui:SetCore("SendNotification", { Title = "Strongest Battleground Script Loaded"; Text = "Made by JN HH Gaming. Subscribe him on youtube"; Icon = ""; Duration = 20; }) function isNumber(str) if tonumber(str) ~= nil or str == 'inf' then return true end end local tspeed = 1 local hb = game:GetService("RunService").Heartbeat local tpwalking = true local player = game:GetService("Players") local lplr = player.LocalPlayer local chr = lplr.Character local hum = chr and chr:FindFirstChildWhichIsA("Humanoid") while tpwalking and hb:Wait() and chr and hum and hum.Parent do if hum.MoveDirection.Magnitude > 0 then if tspeed and isNumber(tspeed) then chr:TranslateBy(hum.MoveDirection * tonumber(tspeed)) else chr:TranslateBy(hum.MoveDirection) end end end
print("Clicked")
end)

Section:CreateButton("inf jump", function()
--script made by Youtube: MrGabbe.   Discord: Mr_G_Curry #6982
local infjmp = true
game:GetService("UserInputService").jumpRequest:Connect(function()
    if infjmp then
        game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass"Humanoid":ChangeState("Jumping")
    end
end)
print("Clicked")
end) 
