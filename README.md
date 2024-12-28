local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local function callback(Text)
end

local NotificationBindable = Instance.new("BindableFunction")
NotificationBindable.OnInvoke = callback

game.StarterGui:SetCore("SendNotification", {
    Title = "Script Injecting";
    Text = "May Take Around 5-20 seconds...";
    Duration = "5";
    Callback = NotificationBindable;
})

local Window = Rayfield:CreateWindow({
   Name = "literal baseplate script",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Loading script",
   LoadingSubtitle = "by RayfieldComplier",
   Theme = "AmberGlow", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
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

local Tab = Window:CreateTab("Script", 4483362458) -- Title, Image

local Button = Tab:CreateButton({
   Name = "Destroy UI",
   Callback = function()
   -- Assuming you have access to the Rayfield library and its GUI components

-- Function to destroy the entire Rayfield GUI
local function destroyRayfieldUI()
    -- If you have a reference to the Rayfield GUI, you can destroy it
    -- This assumes the Rayfield UI is initialized in some variable, such as 'Rayfield'

    if Rayfield then
        -- Assuming Rayfield has a method to destroy or clear all its components
        -- (adjust based on your specific implementation)
        Rayfield:Destroy()
    else
        warn("Rayfield GUI not found.")
    end
end

-- Example usage
destroyRayfieldUI()

   end,
})

local Button = Tab:CreateButton({
   Name = "Indicator",
   Callback = function()
   print("RayfieldComplier GUI is working...")
   end,
})
