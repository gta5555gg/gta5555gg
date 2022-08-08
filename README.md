local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("deedee", "DarkTheme")
local Tab = Window:NewTab("MENU")
local Section = Tab:NewSection("TELEPORT")
Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end
local drop = Section:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Section:NewButton("Click To TP", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end)

Section:NewButton("Refresh Dropdown","Refresh Dropdown", function()
  drop:Refresh(Plr)
end)

Section:NewButton("SPAWN", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(572.363159, 14.2332211, 184.700058, 0.821146309, 9.10135043e-08, 0.570717752, -7.66174963e-08, 1, -4.92350729e-08, -0.570717752, -3.29776406e-09, 0.821146309)
end)

Section:NewButton("Level 11-15", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(33.7879906, 36.4180069, -4496.93115, 0.91909498, 5.69405927e-08, 0.394036055, -5.60090143e-08, 1, -1.386418e-08, -0.394036055, -9.32707334e-09, 0.91909498)
end)
