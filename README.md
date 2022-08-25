# catscript
local pp = Instance.new("Part")
local starterGui = game:GetService("StarterGui")
pp.Parent = workspace
pp.Anchored = true
pp.Position = Vector3.new(2948.31, 831.4, -720.93)
pp.Size = Vector3.new(667.43, 0.09, 714.8)



noclip = false
game:GetService('RunService').Stepped:connect(function()
if noclip then
game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
end
end)
plr = game.Players.LocalPlayer
mouse = plr:GetMouse()
mouse.KeyDown:connect(function(key)
 
if key == "e" then
noclip = not noclip
game.Players.LocalPlayer.Character:MoveTo(pp.Position)
game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
end
end)
starterGui:SetCore("SendNotification", {
    Title = "press E to cat",
    Text = "Reign hell upon worlds",
    Icon = "rbxassetid://8645011774"
})

