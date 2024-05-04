local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:Connect(function()
    if InfiniteJumpEnabled then
        game.Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
    end
end)

local vu = game:GetService("VirtualUser")
game.Players.LocalPlayer.Idled:Connect(function()
    vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    wait(1)
    vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)

game.StarterGui:SetCore("SendNotification", {
    Title = "Made by MrSh4dow"
})

wait(1)

game.StarterGui:SetCore("SendNotification", {
    Title = "Join my Discord Server",
    Text = "https://discord.gg/zcZvSsvxbY",
    Duration = 60
})

_G.HeadSize = 20
_G.Disabled = true

game:GetService('RunService').RenderStepped:Connect(function()
    if _G.Disabled then
        for _, player in ipairs(game:GetService('Players'):GetPlayers()) do
            if player.Name ~= game.Players.LocalPlayer.Name then
                pcall(function()
                    local humanoidRootPart = player.Character and player.Character:FindFirstChild("HumanoidRootPart")
                    if humanoidRootPart then
                        humanoidRootPart.Size = Vector3.new(_G.HeadSize, _G.HeadSize, _G.HeadSize)
                        humanoidRootPart.Transparency = 1 -- Make the player completely invisible
                        humanoidRootPart.CanCollide = false
                        
                        
                        local hitbox = Instance.new("Part")
                        hitbox.Name = "Hitbox"
                        hitbox.Size = Vector3.new(_G.HeadSize * 1.5, _G.HeadSize * 1.5, _G.HeadSize * 1.5)
                        hitbox.Transparency = 1 -- Make the hitbox completely invisible
                        hitbox.CanCollide = false
                        hitbox.Anchored = true  -- Ensures the hitbox doesn't move with the character
                        hitbox.Parent = player.Character
                    end
                end)
            end
        end
    end
end)
