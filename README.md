local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

Rayfield:Notify({
   Title = "Script Injecting",
   Content = "Please wait...",
   Duration = 6.5,
   Image = 7634887655,
})

local Window = Rayfield:CreateWindow({
   Name = "Life In Paradise",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Script Executed... Now loading",
   LoadingSubtitle = "by RemoteEven_t",
   Theme = "Bloom",

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "EnchantedStudios"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", 
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local MainTab = Window:CreateTab("Main🏡", nil) -- Title, Image

local Button = MainTab:CreateButton({
   Name = "Kill random",
   Callback = function()
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Store original position
local originalPosition = character.HumanoidRootPart.Position

-- Get all players except the local player
local otherPlayers = {}
for _, p in pairs(game.Players:GetPlayers()) do
    if p ~= player then
        table.insert(otherPlayers, p)
    end
end

-- Pick a random player
local randomPlayer = otherPlayers[math.random(1, #otherPlayers)]

-- Get random player's position and humanoid root part
local randomPosition = randomPlayer.Character.HumanoidRootPart.Position

-- Teleport 2 studs behind the random player
local offset = randomPlayer.Character.HumanoidRootPart.CFrame.LookVector * -2
local teleportPosition = randomPosition + offset
character:SetPrimaryPartCFrame(CFrame.new(teleportPosition))

-- Wait for a very short time (0.5 seconds)
wait(0.5)

-- Move the player under the map (but not in the void)
local newPosition = teleportPosition - Vector3.new(0, 50, 0) -- Move 50 studs under the map
character:SetPrimaryPartCFrame(CFrame.new(newPosition))

-- Unequip the "Stoller" immediately after teleporting under the map
local backpack = player.Backpack
local stroller = backpack:FindFirstChild("Stoller")
if stroller then
    stroller.Parent = nil
end

-- Create a blue part (5.5 long) under the player
local part = Instance.new("Part")
part.Size = Vector3.new(5.5, 1, 5.5) -- 5.5 studs long
part.Position = newPosition - Vector3.new(0, 1, 0) -- Align it just below the player
part.BrickColor = BrickColor.new("Bright blue")
part.Anchored = true
part.Parent = game.Workspace

-- Wait for 0.1 seconds before re-equipping the "Stoller"
wait(0.1)

-- Re-equip the "Stoller"
if stroller then
    stroller.Parent = character
end

-- Wait for another short time (1 second)
wait(1)

-- Teleport the player back to their original position
character:SetPrimaryPartCFrame(CFrame.new(originalPosition))







   end,
})
