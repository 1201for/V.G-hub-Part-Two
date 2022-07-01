local Config = {
    WindowName = "V.G Hub",
	Color = Color3.fromRGB(255,128,64),
	Keybind = Enum.KeyCode.RightControl
}
repeat wait() until game:IsLoaded() wait()
game:GetService("Players").LocalPlayer.Idled:connect(function()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)

repeat wait() until game.Players.LocalPlayer
game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Chat")

game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame.Visible = true
game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatBarParentFrame.Position =
    game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame.Position +
    UDim2.new(UDim.new(), game:GetService("Players").LocalPlayer.PlayerGui.Chat.Frame.ChatChannelParentFrame.Size.Y)


local NoNos = {
    "CHECKER_1",
    "TeleportDetect",
    "OneMoreTime"
}
Table ={
WalkSpeed,JumpPower
}

local OldNameCall
OldNameCall = hookmetamethod(game, "__namecall", function(...)
    local Args = {...}
    if (getnamecallmethod() == "FireServer"  and table.find(NoNos, Args[2])) then
        return
    end
     if getnamecallmethod()=="IsStudio"  then
        return true
    end
    if (not checkcaller() and getfenv(2).crash) then
        hookfunction(getfenv(2).crash, function()
            return nil
        end)
    end
    return OldNameCall(...)
end)

local OldNameCall
OldNameCall = hookmetamethod(game, "__newindex", function(A, B, C)
    if (not checkcaller() and A.ClassName == "Humanoid" and (B == "WalkSpeed" or B == "JumpPower")) then
        Table[B] = C
        return
    end
    return OldNameCall(A, B, C)
end)

local HospitalJob = game:GetService("Workspace").Ignored.HospitalJob
shop = {}
for i,v in pairs(game:GetService("Workspace").Ignored.Shop:GetChildren()) do
if v.ClassName == "Model" and v:FindFirstChild("ClickDetector") then
table.insert(shop, v.Name)
end end 

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/1201for/V.G-Hub/main/im-retarded-3"))()
local Window = Library:CreateWindow(Config, game:GetService("CoreGui"))

local Tab1 = Window:CreateTab("Da Hood")
local Tab2 = Window:CreateTab("UI Settings")

local Section1 = Tab1:CreateSection("")
local Section2 = Tab1:CreateSection("")
local SectionA = Tab1:CreateSection("")
local Section3 = Tab2:CreateSection("Menu")
local Section4 = Tab2:CreateSection("Background")
local Toggle1 = Section1:CreateToggle("Auto Grab Cash V2!!111", nil, function(State)
getgenv().Start = State
while wait(0.2) and getgenv().Start do
    pcall(
        function()
            
            for i, v in pairs(game:GetService("Workspace").Cashiers:GetChildren()) do
                if v:IsA("Model") and v.Humanoid.Health >= 0 and v.Humanoid.Health > 5 then
                    repeat
                        wait(0.2)
                        if game.Players.LocalPlayer.Character.Humanoid.Sit == true then
                            game.Players.LocalPlayer.Character.Humanoid.Jump = true 
                        end 
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Open.CFrame * CFrame.new(0, 0, 2)
                        if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Combat") then wait(5)
                            game.Players.LocalPlayer.Character.Humanoid:EquipTool(
                                game:GetService("Players").LocalPlayer.Backpack.Combat
                            )
                        end
                        game:GetService("VirtualUser"):ClickButton1(Vector2.new(9e9, 9e9))
                    until v.Head.Crash.Playing or not getgenv().Start and game:GetService("Players").LocalPlayer.DataFolder.Information.Jail.Value == 0
                    for i, v in pairs(game:GetService("Workspace").Ignored.Drop:GetChildren()) do
                        if
                            v:IsA("BasePart") and v.Name == "MoneyDrop" and
                                (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude <=
                                    50 
                         then
                            repeat
                                wait()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
                                if
                                    (v.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <=
                                        12 and v:FindFirstChildWhichIsA("ClickDetector")
                                 then
                                    fireclickdetector(v:FindFirstChildWhichIsA("ClickDetector"))
                                    wait(1)
                                end
                            until not v:FindFirstChildWhichIsA("ClickDetector") or not getgenv().Start and game:GetService("Players").LocalPlayer.DataFolder.Information.Jail.Value == 0
                        end
                    end
                end
            end
        end
    )
end
end)
local Toggle1 = Section1:CreateToggle("Auto Grab Cash", nil, function(State)
getgenv().CashGrab = State

game:GetService('RunService').Stepped:connect(function()
if getgenv().CashGrab then
game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):ChangeState(11)
end end)
while getgenv().CashGrab do
    wait()
    pcall(
        function()
            for i, v in pairs(game:GetService("Workspace").Ignored.Drop:GetChildren()) do
                if v.ClassName == "Part" and v:FindFirstChild("ClickDetector") then
                    wait(1)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
                    wait(1)
                    fireclickdetector(v.ClickDetector)
                    wait(1)
                end
            end
        end
    )
end
end)
local Toggle1 = Section1:CreateToggle("Auto HospitalJob", nil, function(State)
getgenv().HospitalJob = State
while getgenv().HospitalJob do
    wait(2)
    if HospitalJob:FindFirstChild("Can I get the Red bottle") then
        fireclickdetector(HospitalJob.Red.ClickDetector)
        wait(.1)
        fireclickdetector(HospitalJob["Can I get the Red bottle"].ClickDetector)
    elseif HospitalJob:FindFirstChild("Can I get the Green bottle") then
        fireclickdetector(HospitalJob.Green.ClickDetector)
        wait(.1)
        fireclickdetector(HospitalJob["Can I get the Green bottle"].ClickDetector)
    elseif HospitalJob:FindFirstChild("Can I get the Blue bottle") then
        fireclickdetector(HospitalJob.Blue.ClickDetector)
        wait(.1)
        fireclickdetector(HospitalJob["Can I get the Blue bottle"].ClickDetector)
    end
end

end)
local Toggle1 = Section1:CreateToggle("AutoFarm Shoes", nil, function(State)
getgenv().AutoShoe = State
game.RunService.Stepped:Connect(
    function()
        if getgenv().AutoShoe then
            fireclickdetector(
                game:GetService("Workspace").Ignored["Clean the shoes on the floor and come to me for cash"].ClickDetector
            )
            for i, v in pairs(workspace.Ignored.Drop:GetChildren()) do
                if v.Transparency == 0 and v:IsA("MeshPart") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.Position = v.Position
                    wait()
                    fireclickdetector(v.ClickDetector)
                end
            end
        end
    end
)

end)


local Slider2 = Section2:CreateSlider("Gravity", 0,50,nil,false, function(Value)
head = Value
end)


local Toggle1 = Section1:CreateToggle("Hitbox Extender Players", nil, function(State)
HEAD = State
game.RunService.Stepped:Connect(
    function()
        for i, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
            pcall(
                function()
                    if HEAD then
                    if v.ClassName == "Part" or v.ClassName == "MeshPart" then
                        v.CanCollide = false
                    end
                    end
                end
            )
        end
    end
)
while HEAD do
    wait()
    for i, v in pairs(game.Players:GetPlayers()) do
        if v.Name ~= game.Players.LocalPlayer.Name then
            pcall(
                function()
                    v.Character.LowerTorso.CanCollide = false
                    v.Character.LowerTorso.Material = "Neon"
                    v.Character.LowerTorso.Transparency = 0.5
                    v.Character.LowerTorso.Size = Vector3.new(head, head, head)
                    v.Character.HumanoidRootPart.Size = Vector3.new(head, head, head)
                end
            )
        end
    end
end
end)

local Toggle1 = Section1:CreateToggle("infinite Stamina", nil, function(State)
getgenv().infinite = State

while getgenv().infinite and wait() do
    game:GetService "Players".LocalPlayer.Character:WaitForChild("BodyEffects"):WaitForChild("Defense").Value =
        math.huge
    game:GetService "Players".LocalPlayer.Character:WaitForChild("BodyEffects"):WaitForChild("Reload").Value = false

    for _, v in next, game:GetService "Players".LocalPlayer.Character:WaitForChild("BodyEffects"):WaitForChild(
        "Movement"
    ):GetChildren() do
        if v then
            v:Destroy()
        end
    end
end
end)
local Toggle1 = Section1:CreateToggle("Godmode", nil, function(State)
sex = State
while sex do
    wait()
    game:GetService("Players").LocalPlayer.Character.BodyEffects:WaitForChild("Attacking"):Destroy()
end
end)

local Button1 = Section1:CreateButton("Buy Selected Item", function()
local Save = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame 
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Ignored.Shop[shop].Head.CFrame wait(0.5)
fireclickdetector(game:GetService("Workspace").Ignored.Shop[shop].ClickDetector) wait(0.5)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Save
end)
local Dropdown1 = Section1:CreateDropdown("Select Item To Buy")
Dropdown1:AddToolTip("Select Item To Buy")
for i,v in next, shop do
Dropdown1:AddOption(v, function(String)
shop = String
end)
end 

local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/1201for/V.G-Hub/main/Karrot-Esp"))()

local Toggle1 = Section1:CreateToggle("Player Esp", nil, function(State)
    ESP:Toggle(State)
end)
local Toggle1 = Section1:CreateToggle("Tracers Esp", nil, function(State)
    ESP.Tracers = State
end)
local Toggle1 = Section1:CreateToggle("Name Esp", nil, function(State)
    ESP.Names = State
end)
local Toggle1 = Section1:CreateToggle("Boxes Esp", nil, function(State)
    ESP.Boxes = State
end)


local TextBox1 = Section2:CreateTextBox("WalkSpeed", "Only numbers", true, function(Value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
end)
local TextBox1 = Section2:CreateTextBox("JumpPower", "Only numbers", true, function(Value)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
end)
local Slider2 = Section2:CreateSlider("Gravity", 0,196.2,nil,false, function(Value)
game.Workspace.Gravity = Value
end)
local Toggle1 = Section2:CreateToggle("Infinite Jump", nil, function(State)
Infinite = State
game:GetService("UserInputService").JumpRequest:connect(function()
	if Infinite then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end) end)




local Toggle1 = Section2:CreateToggle("FullBright", nil, function(State)
FullBright = State
game.Lighting.Changed:connect(function()
if FullBright then
game.Lighting.TimeOfDay = "14:00:00"
game.Lighting.FogEnd = 9999
game.Lighting.Brightness = 2
game.Lighting.ColorCorrection.Brightness = 0.1
game.Lighting.ColorCorrection.Saturation = 0.1
game.Lighting.Bloom.Intensity = 0.1
end end) end)


local Toggle1 = Section2:CreateToggle("G PlatFormNoclip", nil, function(State)
yes44 = State
noclip = false
game:GetService("RunService").Stepped:connect(
    function()
        if noclip then
            game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
        end
    end
)
game.Players.LocalPlayer:GetMouse().KeyDown:connect(
    function(key)
        if key == "g" then
            if yes44 then
                noclip = not noclip
                game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end
)
end)
local Toggle1 = Section2:CreateToggle("N NonePlatFormNoclip", nil, function(State)
hoe = State
game.Players.LocalPlayer:GetMouse().KeyDown:connect(
    function(v)
        if v == "n" then
            NoClip = not NoClip
            game:GetService("RunService").Stepped:connect(
                function()
                    if NoClip then
                     if hoe then
                        for i, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                            pcall(
                                function()
                                    if v.ClassName == "Part" or v.ClassName == "MeshPart" then
                                        v.CanCollide = false
                                    end
                                end
                            )
                        end
                    end
                end
            end
            )
        end
    end
)
end)



local Toggle1 = Section2:CreateToggle("B Fly", nil, function(State)
sex2 = State
local Max = 0
local Players = game.Players
local LP = Players.LocalPlayer
local Mouse = LP:GetMouse()
Mouse.KeyDown:connect(function(k)
if k:lower() == 'b' then
Max = Max + 1
getgenv().Fly = false
if sex2 then
local T = LP.Character.UpperTorso
local S = {
F = 0,
B = 0,
L = 0,
R = 0
}
local S2 = {
F = 0,
B = 0,
L = 0,
R = 0
}
local SPEED = 5
local function FLY()
getgenv().Fly = true
local BodyGyro = Instance.new('BodyGyro', T)
local BodyVelocity = Instance.new('BodyVelocity', T)
BodyGyro.P = 9e4
BodyGyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
BodyGyro.cframe = T.CFrame
BodyVelocity.velocity = Vector3.new(0, 0.1, 0)
BodyVelocity.maxForce = Vector3.new(9e9, 9e9, 9e9)
spawn(function()
repeat
wait()
LP.Character.Humanoid.PlatformStand = true
if S.L + S.R ~= 0 or S.F + S.B ~= 0 then
SPEED = 200
elseif not (S.L + S.R ~= 0 or S.F + S.B ~= 0) and SPEED ~= 0 then
SPEED = 0
end
if (S.L + S.R) ~= 0 or (S.F + S.B) ~= 0 then
BodyVelocity.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (S.F + S.B)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(S.L + S.R, (S.F + S.B) * 0.2, 0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
S2 = {
F = S.F,
B = S.B,
L = S.L,
R = S.R
}
elseif (S.L + S.R) == 0 and (S.F + S.B) == 0 and SPEED ~= 0 then
BodyVelocity.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (S2.F + S2.B)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(S2.L + S2.R, (S2.F + S2.B) * 0.2, 0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
else
BodyVelocity.velocity = Vector3.new(0, 0.1, 0)
end
BodyGyro.cframe = game.Workspace.CurrentCamera.CoordinateFrame
until not getgenv().Fly
S = {
F = 0,
B = 0,
L = 0,
R = 0
}
S2 = {
F = 0,
B = 0,
L = 0,
R = 0
}
SPEED = 0
BodyGyro:destroy()
BodyVelocity:destroy()
LP.Character.Humanoid.PlatformStand = false
end)
end
Mouse.KeyDown:connect(function(k)
if k:lower() == 'w' then
S.F = 1
elseif k:lower() == 's' then
S.B = -1
elseif k:lower() == 'a' then
S.L = -1
elseif k:lower() == 'd' then
S.R = 1
end
end)
Mouse.KeyUp:connect(function(k)
if k:lower() == 'w' then
S.F = 0
elseif k:lower() == 's' then
S.B = 0
elseif k:lower() == 'a' then
S.L = 0
elseif k:lower() == 'd' then
S.R = 0
end
end)
FLY()
if Max == 2 then
getgenv().Fly = false
Max = 0
end
end
end
end)
end)
local Button1 = Section2:CreateButton("Anti Lag", function()
for _,v in pairs(game:GetService("Workspace"):GetDescendants()) do
if v:IsA("BasePart") and not v.Parent:FindFirstChild("Humanoid") then --- i stole this from the actual game LOL >-<
v.Material = Enum.Material.SmoothPlastic;
if v:IsA("Texture") then
v:Destroy();
end end;		
end;
end)

local Button1 = Section2:CreateButton("Teleport to RandomPlayer", function()
local randomPlayer = game.Players:GetPlayers()
[math.random(1,#game.Players:GetPlayers())]

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(randomPlayer.Character.Head.Position.X, randomPlayer.Character.Head.Position.Y, randomPlayer.Character.Head.Position.Z)) end)
local Button1 = Section2:CreateButton("Lag Switch F3", function()
local a = false
local b = settings()

game:service'UserInputService'.InputEnded:connect(function(i)
if i.KeyCode == Enum.KeyCode.F3 then
a = not a
b.Network.IncomingReplicationLag = a and 10 or 0
end
end) end) 
local Button1 = Section2:CreateButton("Rejoin", function()
game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").LocalPlayer) end)

local Toggle3 = Section3:CreateToggle("UI Toggle", nil, function(State)
	Window:Toggle(State)
end)
Toggle3:CreateKeybind(tostring(Config.Keybind):gsub("Enum.KeyCode.", ""), function(Key)
	Config.Keybind = Enum.KeyCode[Key]
end)
Toggle3:SetState(true)
Section3:CreateLabel("Credits DekuDimz#7960")
Section3:CreateLabel("Credits AlexR32#3232 Ui")
Section3:CreateLabel("Credits Stefanuk12")
Section3:CreateLabel("Credits e621")
local Colorpicker3 = Section3:CreateColorpicker("UI Color", function(Color)
	Window:ChangeColor(Color)
end)
Colorpicker3:UpdateColor(Config.Color)
-- credits to jan for patterns
local Dropdown3 = Section4:CreateDropdown("Image")
local Option7 = Dropdown3:AddOption("Default", function(String)
	Window:SetBackground("2151741365")
end)
local Option8 = Dropdown3:AddOption("Hearts", function(String)
	Window:SetBackground("6073763717")
end)
local Option9 = Dropdown3:AddOption("Abstract", function(String)
	Window:SetBackground("6073743871")
end)
local Option10 = Dropdown3:AddOption("Hexagon", function(String)
	Window:SetBackground("6073628839")
end)
local Option11 = Dropdown3:AddOption("Circles", function(String)
	Window:SetBackground("6071579801")
end)
local Option12 = Dropdown3:AddOption("Lace With Flowers", function(String)
	Window:SetBackground("6071575925")
end)
local Option13 = Dropdown3:AddOption("Floral", function(String)
	Window:SetBackground("5553946656")
end)
Option7:SetOption()

local Colorpicker4 = Section4:CreateColorpicker("Color", function(Color)
	Window:SetBackgroundColor(Color)
end)
Colorpicker4:UpdateColor(Color3.new(1,1,1))

local Slider3 = Section4:CreateSlider("Transparency",0,1,nil,false, function(Value)
	Window:SetBackgroundTransparency(Value)
end)
Slider3:SetValue(0)

local Slider4 = Section4:CreateSlider("Tile Scale",0,1,nil,false, function(Value)
	Window:SetTileScale(Value)
end)
Slider4:SetValue(0.5)
