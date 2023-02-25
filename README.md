local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("function Hub", "Midnight")

local speed = Window:NewTab("CframeSpeed")
local rs = speed:NewSection("function Hub")
rs:NewButton("CFrame Speed (C)", "ButtonInfo", function()
        repeat
        wait()
    until game:IsLoaded()
    local L_134_ = game:service('Players')
    local L_135_ = L_134_.LocalPlayer
    repeat
        wait()
    until L_135_.Character
    local L_136_ = game:service('UserInputService')
    local L_137_ = game:service('RunService')
    getgenv().Multiplier = 0.5
    local L_138_ = true
    local L_139_
    L_136_.InputBegan:connect(function(L_140_arg0)
        if L_140_arg0.KeyCode == Enum.KeyCode.LeftBracket then
            Multiplier = Multiplier + 0.01
            print(Multiplier)
            wait(0.2)
            while L_136_:IsKeyDown(Enum.KeyCode.LeftBracket) do
                wait()
                Multiplier = Multiplier + 0.01
                print(Multiplier)
            end
        end
        if L_140_arg0.KeyCode == Enum.KeyCode.RightBracket then
            Multiplier = Multiplier - 0.01
            print(Multiplier)
            wait(0.2)
            while L_136_:IsKeyDown(Enum.KeyCode.RightBracket) do
                wait()
                Multiplier = Multiplier - 0.01
                print(Multiplier)
            end
        end
        if L_140_arg0.KeyCode == Enum.KeyCode.C then
            L_138_ = not L_138_
            if L_138_ == true then
                repeat
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.Humanoid.MoveDirection * Multiplier
                    game:GetService("RunService").Stepped:wait()
                until L_138_ == false
            end
        end
    end)
end)

rs:NewSlider("CFrame Speed ", "SliderInfo", 3, 0, function(s) -- 300 (MaxValue) | 0 (MinValue)
    getgenv().Multiplier = s
end)
rs:NewKeybind("Toggle UI", "KeybindInfo", Enum.KeyCode.F1, function()
    Library.ToggleUI()
end)
local speed = Window:NewTab("esp/unesp")
local rs = speed:NewSection("function Hub")
rs:NewButton("espV1", "ButtonInfo", function()
_G.Hee = true
while _G.Hee do wait()
    local Player = game:GetService("Players"):GetChildren()
    local highlight = Instance.new("Highlight")
    highlight.FillColor = Color3.fromRGB(255, 255, 255)
    highlight.FillTransparency = 0.5
    highlight.Name = "Highlight"
    for i, v in pairs(Player) do
        repeat wait() until v.Character
        if not v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = v.Character
            highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlightClone.Name = "Highlight"
        end
    end
    game.Players.PlayerAdded:Connect(function(Plr)
        repeat wait() until Plr.Character
        if not Plr.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
            local highlightClone = highlight:Clone()
            highlightClone.Adornee = v.Character
            highlightClone.Parent = v.Character:FindFirstChild("HumanoidRootPart")
            highlightClone.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
            highlightClone.Name = "Highlight"
        end
    end)
end
end)
rs:NewButton("unespV1", "ButtonInfo", function()
	_G.Hee = false
    game.Players.PlayerRemoving:Connect(function(PlrRemoved)
    PlrRemoved.Character:FindFirstChild("HumanoidRootPart").Highlight:Destroy()
end)
local Player = game:GetService("Players"):GetChildren()
for i, v in pairs(Player) do
    repeat wait() until v.Character
    if v.Character:FindFirstChild("HumanoidRootPart"):FindFirstChild("Highlight") then
        v.Character:FindFirstChild("HumanoidRootPart").Highlight:Destroy()
    end
end
end)
rs:NewButton("EspV2)", "ButtonInfo", function()
    local Esp = loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/x114/RobloxScripts/main/OpenSourceEsp"))()
-- Boxes --
Esp.Box = true
Esp.BoxColor = Color3.fromRGB(255,255,255)
Esp.BoxOutline = true
Esp.BoxOutlineColor = Color3.fromRGB(0,0,0)
-- HealthBars --
Esp.HealthBar = true
Esp.HealthBarSide = "Left" -- Left,Bottom,Right
-- Names --
Esp.Names = true
Esp.NamesColor = Color3.fromRGB(255,255,255)
Esp.NamesOutline = true
Esp.NamesFont = 2
Esp.NamesSize = 13
end)
local speed = Window:NewTab("aimbot/FOV")
local rs = speed:NewSection("function Hub")
rs:NewButton("aimbot)", "ButtonInfo", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/functionHubX/lock/main/README.md"))()
end)
rs:NewButton("HitBox)", "ButtonInfo", function()
    local HitboxSize = Vector3.new(10,10,10) --too big wont work
local speed = Window:NewTab("Infinite Yield")
local rs = speed:NewSection("function Hub")
rs:NewButton("Infinite Yield)", "ButtonInfo", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
end)
rs:NewButton("reJoin)", "ButtonInfo", function()
    game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").LocalPlayer)
end)
