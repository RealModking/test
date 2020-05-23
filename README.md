-- Gui to Lua
-- Version: 3.2

-- Instances:

local Evildead = Instance.new("ScreenGui")
local Mainframe = Instance.new("Frame")
local Topbar = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local TextButton = Instance.new("TextButton")
local jumpsc = Instance.new("TextButton")
local dupemoney = Instance.new("TextButton")
local Openframe = Instance.new("Frame")
local Open = Instance.new("TextButton")

--Properties:

Evildead.Name = "Evil dead"
Evildead.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
Evildead.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Mainframe.Name = "Main frame"
Mainframe.Parent = Evildead
Mainframe.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Mainframe.BackgroundTransparency = 0.0
Mainframe.Position = UDim2.new(0.420271188, 0, 0.201405138, 0)
Mainframe.Size = UDim2.new(0, 247, 0, 509)
Mainframe.Visible = false
Mainframe.Draggable = true

Topbar.Name = "Topbar"
Topbar.Parent = Mainframe
Topbar.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Topbar.BackgroundTransparency = 1.000
Topbar.Size = UDim2.new(0, 247, 0, 38)

TextLabel.Parent = Topbar
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Size = UDim2.new(0, 201, 0, 38)
TextLabel.Font = Enum.Font.Garamond
TextLabel.Text = "Evil Dead"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

TextButton.Parent = Topbar
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.BackgroundTransparency = 1.000
TextButton.Position = UDim2.new(0.813765168, 0, 0, 0)
TextButton.Size = UDim2.new(0, 46, 0, 38)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "X"
TextButton.TextColor3 = Color3.fromRGB(255, 0, 0)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextWrapped = true
TextButton.MouseButton1Down:connect(function()
Openframe.Visible = true
Mainframe.Visible = false
end)

jumpsc.Name = "jumpsc"
jumpsc.Parent = Mainframe
jumpsc.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
jumpsc.Position = UDim2.new(0.0931174085, 0, 0.0864440054, 0)
jumpsc.Size = UDim2.new(0, 200, 0, 33)
jumpsc.Font = Enum.Font.SourceSansItalic
jumpsc.Text = "Infinite jump"
jumpsc.TextColor3 = Color3.fromRGB(0, 0, 0)
jumpsc.TextScaled = true
jumpsc.TextSize = 14.000
jumpsc.TextWrapped = true
jumpsc.MouseButton1Down:connect(function()
local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';

_G.JumpHeight = 50;

function Action(Object, Function) if Object ~= nil then Function(Object); end end

UIS.InputBegan:connect(function(UserInput)
    if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.Space then
        Action(Player.Character.Humanoid, function(self)
            if self:GetState() == Enum.HumanoidStateType.Jumping or self:GetState() == Enum.HumanoidStateType.Freefall then
                Action(self.Parent.HumanoidRootPart, function(self)
                    self.Velocity = Vector3.new(0, _G.JumpHeight, 0);
                end)
            end
        end)
    end
end)
end)

dupemoney.Name = "dupe money"
dupemoney.Parent = Mainframe
dupemoney.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
dupemoney.Position = UDim2.new(0.0931174085, 0, 0.212180749, 0)
dupemoney.Size = UDim2.new(0, 200, 0, 33)
dupemoney.Font = Enum.Font.SourceSansItalic
dupemoney.Text = "dupe money"
dupemoney.TextColor3 = Color3.fromRGB(0, 0, 0)
dupemoney.TextScaled = true
dupemoney.TextSize = 14.000
dupemoney.TextWrapped = true
dupemoney.MouseButton1Down:connect(function()
-- Objects

local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local SaveSlot = Instance.new("TextButton")
local DMoney = Instance.new("TextButton")
local Store = Instance.new("TextButton")
local Restore = Instance.new("TextButton")
local DropAxes = Instance.new("TextButton")
local Load = Instance.new("TextButton")
local CountAxes = Instance.new("TextButton")
local Slot = Instance.new("TextBox")

-- Properties

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "LT2DupeGui"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.new(0.282353, 0.278431, 0.278431)
MainFrame.BorderColor3 = Color3.new(0.588235, 0.588235, 0.588235)
MainFrame.BorderSizePixel = 3
MainFrame.Position = UDim2.new(0.111687116, 0, 0.167118713, 0)
MainFrame.Size = UDim2.new(0, 230, 0, 258)
MainFrame.Active = true
MainFrame.Draggable = true

SaveSlot.Name = "SaveSlot"
SaveSlot.Parent = MainFrame
SaveSlot.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
SaveSlot.BorderSizePixel = 2
SaveSlot.Position = UDim2.new(0.040079806, 0, 0.302941561, 0)
SaveSlot.Size = UDim2.new(0, 95, 0, 40)
SaveSlot.Font = Enum.Font.SourceSans
SaveSlot.Text = "Save Slot"
SaveSlot.TextColor3 = Color3.new(0, 0, 0)
SaveSlot.TextSize = 14

DMoney.Name = "DMoney"
DMoney.Parent = MainFrame
DMoney.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
DMoney.BorderSizePixel = 2
DMoney.Position = UDim2.new(0.0410686359, 0, 0.774269283, 0)
DMoney.Size = UDim2.new(0, 95, 0, 40)
DMoney.Font = Enum.Font.SourceSans
DMoney.Text = "Dupe Money"
DMoney.TextColor3 = Color3.new(0, 0, 0)
DMoney.TextSize = 14

Store.Name = "Store"
Store.Parent = MainFrame
Store.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
Store.BorderSizePixel = 2
Store.Position = UDim2.new(0.514908552, 0, 0.299316287, 0)
Store.Size = UDim2.new(0, 95, 0, 40)
Store.Font = Enum.Font.SourceSans
Store.Text = "Store Axe"
Store.TextColor3 = Color3.new(0, 0, 0)
Store.TextSize = 14

Restore.Name = "Restore"
Restore.Parent = MainFrame
Restore.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
Restore.BorderSizePixel = 2
Restore.Position = UDim2.new(0.51270771, 0, 0.528562546, 0)
Restore.Size = UDim2.new(0, 95, 0, 40)
Restore.Font = Enum.Font.SourceSans
Restore.Text = "Restore Axe"
Restore.TextColor3 = Color3.new(0, 0, 0)
Restore.TextSize = 14

DropAxes.Name = "Drop Axes"
DropAxes.Parent = MainFrame
DropAxes.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
DropAxes.BorderSizePixel = 2
DropAxes.Position = UDim2.new(0.514981687, 0, 0.774269283, 0)
DropAxes.Size = UDim2.new(0, 95, 0, 40)
DropAxes.Font = Enum.Font.SourceSans
DropAxes.Text = "Drop Axes"
DropAxes.TextColor3 = Color3.new(0, 0, 0)
DropAxes.TextSize = 14

Load.Name = "Load"
Load.Parent = MainFrame
Load.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
Load.BorderSizePixel = 2
Load.Position = UDim2.new(0.0410686135, 0, 0.530083239, 0)
Load.Size = UDim2.new(0, 95, 0, 40)
Load.Font = Enum.Font.SourceSans
Load.Text = "Load Slot"
Load.TextColor3 = Color3.new(0, 0, 0)
Load.TextSize = 14

CountAxes.Name = "Count Axes"
CountAxes.Parent = MainFrame
CountAxes.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
CountAxes.BorderSizePixel = 2
CountAxes.Position = UDim2.new(0.510633886, 0, 0.0688429475, 0)
CountAxes.Size = UDim2.new(0, 95, 0, 40)
CountAxes.Font = Enum.Font.SourceSans
CountAxes.Text = "Count Axes"
CountAxes.TextColor3 = Color3.new(0, 0, 0)
CountAxes.TextSize = 14

Slot.Name = "Slot"
Slot.Parent = MainFrame
Slot.BackgroundColor3 = Color3.new(0.411765, 0.411765, 0.411765)
Slot.BorderSizePixel = 2
Slot.Position = UDim2.new(0.0410686322, 0, 0.0697674453, 0)
Slot.Size = UDim2.new(0, 94, 0, 39)
Slot.Font = Enum.Font.SourceSans
Slot.Text = "Slot Number"
Slot.TextColor3 = Color3.new(0, 0, 0)
Slot.TextSize = 14

--Locals
local MoneyCooldown = false
local CurrentSlot = game.Players.LocalPlayer:WaitForChild("CurrentSaveSlot").Value
local ScriptLoadOrSave = false
local CurrentlySavingOrLoading = game.Players.LocalPlayer:WaitForChild("CurrentlySavingOrLoading")

--Functions
local function CheckIfSlotAvailable(Slot)
	for a,b in pairs(game.ReplicatedStorage.LoadSaveRequests.GetMetaData:InvokeServer(game.Players.LocalPlayer)) do 
		if a == Slot then 
			for c,d in pairs(b) do 
				if c == "NumSaves" and d ~= 0 then 
					return true
				else
					return false
				end
			end
		end
	end
end

local function CheckSlotNumber() --Checks if the slot number is right
    if Slot.Text == "1" or Slot.Text == "2" or Slot.Text == "3" or Slot.Text == "4" or Slot.Text == "5" or Slot.Text == "6" then
		local SlotNumber = tonumber(Slot.Text)
		return SlotNumber
		else return false
	end
end

local function SendNotification(Title,Text,Duration) -- Sends Notification in the bottom right of the screen
	game.StarterGui:SetCore("SendNotification", {
		Title = Title;
		Text = Text;
		Icon = nil;
		Duration = Duration
	})
end

SaveSlot.MouseButton1Down:connect(function() --Saves the slot that you want
	local CheckSlot = CheckSlotNumber()
	if CheckSlot ~= false then
		if CurrentSlot ~= -1 then
			ScriptLoadOrSave = true
			local SaveSlot = game.ReplicatedStorage.LoadSaveRequests.RequestSave:InvokeServer(CheckSlot)
			if SaveSlot == true then
				SendNotification("Save Notification", "Saved your Slot", 2)
				wait(.5)
				ScriptLoadOrSave = false
			elseif SaveSlot == false then
				SendNotification("Already Saving", "Saving/Loading is currently in Progress", 1)
				wait(.5)
				ScriptLoadOrSave = false
			end
		else
			SendNotification("Error", "Load Your Slot First before saving", 1)
		end
	else
		SendNotification("Incorrect Slot", "Enter a number in the upper field", 1)
	end
end)

Load.MouseButton1Down:connect(function() --Loads the slot you want
	ScriptLoadOrSave = true
	local CheckSlot = CheckSlotNumber()
	if CheckSlot ~= false then
		if CheckIfSlotAvailable(CheckSlot) == true then
			local LoadSlot = game.ReplicatedStorage.LoadSaveRequests.RequestLoad:InvokeServer(CheckSlot)
			if LoadSlot == false then
				SendNotification("Cooldown Notification", "You aren't abled to load now", 1)
			end
			if LoadSlot == true then 
				SendNotification("Reload Notification", "Loaded Your Slot", 2)
				CurrentSlot = CheckSlot
			end
		else
			SendNotification("Slot not Available", "This Slot is not Available, please choose another slot", 2)
		end
	else
		SendNotification("Incorrect Slot", "Enter a Valid number in the upper field", 1)
	end
	ScriptLoadOrSave = false
end)

Store.MouseButton1Down:connect(function() --Stores the Axes somewhere so you can restore them later
	Amount = 0
	for a,b in pairs(game.Players.LocalPlayer.Backpack:GetChildren())do
		if b.Name ~= "BlueprintTool" and b.Name == "Tool" then
			b.Parent = game.Players.LocalPlayer
			Amount = Amount + 1
		end
	end
	SendNotification("Store Notification", "Stored "..Amount.." Axes, you can restore them later", 2)
end)

Restore.MouseButton1Down:connect(function() --Restores the axes that you stored with the Store function
	Amount = 0
	for a,b in pairs(game.Players.LocalPlayer:GetChildren()) do
		if b.Name ~= "BlueprintTool" and b.Name == "Tool" then
			b.Parent = game.Players.LocalPlayer.Backpack
			Amount = Amount + 1
		end
	end
	SendNotification("Restore Notification", "Restored "..Amount.." Axes that you Stored", 2)
end)

CountAxes.MouseButton1Down:connect(function() --Counts Axes in your Backpack (Equiped Axes dont Count)
	Amount = 0
	for a,b in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
		if b.Name ~= "BlueprintTool" and b.Name == "Tool" then
			Amount = Amount + 1
		end
	end
	SendNotification("Axe Amount", "You have "..Amount.." Axes in your Backpack",2)
end)

DropAxes.MouseButton1Down:connect(function() --Drops all your Axes
	Amount = 0
	for a,b in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
		if b.Name ~= "BlueprintTool" and b.Name == "Tool" then
			game.ReplicatedStorage.Interaction.ClientInteracted:FireServer(b, "Drop tool", game.Players.LocalPlayer.Character.Head.CFrame)
			Amount = Amount + 1
		end
	end
	SendNotification("Axe Dropped", "Dropped "..Amount.." Axes from your Backpack",5)
end)

DMoney.MouseButton1Down:connect(function() --Sends the money and will come back after around 2 mins
	if MoneyCooldown == true then
		SendNotification("Cooldown Notification", "Wait for your Money to come back",2)
		return
	elseif MoneyCooldown == false then
		MoneyCooldown = true
		SendNotification("Money Sent", "Wait about 2 minutes for your Money to come back", 5)
		game.ReplicatedStorage.Transactions.ClientToServer.Donate:InvokeServer(game.Players.LocalPlayer, game.Players.LocalPlayer.leaderstats.Money.Value, 1)
		SendNotification("Money Received", "You received your money that you have sent earlier", 5)
		MoneyCooldown = false
	end
end)

--Anti Overwrite Slot (Sub-Function)
while wait(.15) do
	if CurrentlySavingOrLoading.Value == true and ScriptLoadOrSave == false then
		repeat 
		wait(1)
		until CurrentlySavingOrLoading.Value == false
		wait(1)
		CurrentSlot = game.Players.LocalPlayer.CurrentSaveSlot.Value
		print(CurrentSlot)
	end
end
end)

Openframe.Name = "Open frame"
Openframe.Parent = Evildead
Openframe.BackgroundColor3 = Color3.fromRGB(127, 127, 127)
Openframe.Position = UDim2.new(0, 0, 0.373536289, 0)
Openframe.Size = UDim2.new(0, 246, 0, 53)

Open.Name = "Open"
Open.Parent = Openframe
Open.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Open.BackgroundTransparency = 1.000
Open.Position = UDim2.new(0.0926062092, 0, 0.188679531, 0)
Open.Size = UDim2.new(0, 200, 0, 33)
Open.Font = Enum.Font.GothamBlack
Open.Text = "Open"
Open.TextColor3 = Color3.fromRGB(177, 38, 232)
Open.TextScaled = true
Open.TextSize = 14.000
Open.TextWrapped = true
Open.MouseButton1Down:connect(function()
Mainframe.Visible = true
Openframe.Visible = false
end)
