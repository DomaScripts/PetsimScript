local RunService = game:GetService("RunService")
local breakablesFolder = game.Workspace:FindFirstChild("SlimeFactory"):FindFirstChild("Breakables")

local function clickAllBreakables()
    if breakablesFolder then
        for _, obj in pairs(breakablesFolder:GetChildren()) do
            if obj:FindFirstChild("ClickDetector") then
                fireclickdetector(obj.ClickDetector)
            end
        end
    end
end

local lastTime = 0
local clickInterval = 0.1

RunService.Heartbeat:Connect(function(_, dt)
    lastTime = lastTime + dt
    if lastTime >= clickInterval then
        clickAllBreakables()
        lastTime = 0
    end
end)
