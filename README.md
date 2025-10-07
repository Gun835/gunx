# gunx
nope
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("gunx", "DarkTheme")
local Tab = Window:NewTab("Teleport")
local Section = Tab:NewSection("find arrow")
Section:NewButton("start Find", "Find arrow", function()
local player = game.Players.LocalPlayer
local char = player.Character or player.CharacterAdded:Wait()
local hrp = char:WaitForChild("HumanoidRootPart")

local positions = {
    CFrame.new(1035.03333, 6.34141445, 1580.60962, 1, 0, 0, 0, 1, 0, 0, 0, 1),      
    CFrame.new(82.9516525, 14.5710411, 2488.86523, 1, 0, 0, 0, 1, 0, 0, 0, 1),     
    CFrame.new(-897.769653, -2.35301805, 2426.7749, 1, 0, 0, 0, 1, 0, 0, 0, 1),  
    CFrame.new(-2999.31152, -3.68041444, 940.210449, 1, 0, 0, 0, 1, 0, 0, 0, 1),
    CFrame.new(281.031128, 18.3180428, 835.79834, 1, 0, 0, 0, 1, 0, 0, 0, 1),      
    CFrame.new(-1527.25574, -1.66190243, 1711.01221, 1, 0, 0, 0, 1, 0, 0, 0, 1),     
    CFrame.new(-183.278809, -0.0684723854, 1421.67981, 1, 0, 0, 0, 1, 0, 0, 0, 1)
}

while true do
    for i, pos in ipairs(positions) do
        hrp.CFrame = pos
        task.wait(2)
    end
end    
end)
