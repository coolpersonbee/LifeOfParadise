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

local Tab = Window:CreateTab("Main", 4483362458) -- Title, Image

local Button = Tab:CreateButton({
   Name = "chat bypasser --copy text--",
   Callback = function()
   local gui = Instance.new("ScreenGui")
gui.Name = "Chat Bypasser"
gui.Parent = game.CoreGui

local main = Instance.new("Frame")
main.Size = UDim2.new(0.2, 0, 0.05, 0)
main.Position = UDim2.new(0.2, 0, 0.2, 0)
main.BackgroundColor3 = Color3.new(0, 0, 0.5)
main.BorderSizePixel = 0
main.Active = true
main.BackgroundTransparency = 0
main.Draggable = true
main.Parent = gui

local lbl = Instance.new("TextLabel")
lbl.Size = UDim2.new(0.62, 0, 1, 0)
lbl.Position = UDim2.new(0, 0, 0, 0)
lbl.BackgroundColor3 = Color3.new(0, 0, 0)
lbl.BorderSizePixel = 0
lbl.Text = "Mega big pencil cracked ):"
lbl.TextColor3 = Color3.new(255, 255, 255)
lbl.BackgroundTransparency = 1
lbl.Font = Enum.Font.ArialBold
lbl.TextSize = 15
lbl.Parent = main

local mi = Instance.new("TextButton")
mi.Size = UDim2.new(0.1, 0, 0.8, 0)
mi.Position = UDim2.new(0.89, 0, 0.1, 0)
mi.BackgroundColor3 = Color3.new(0, 0.3, 0.6)
mi.BorderSizePixel = 0
mi.Text = ">"
mi.TextColor3 = Color3.new(255, 255, 255)
mi.BackgroundTransparency = 0
mi.Font = Enum.Font.Arial
mi.TextSize = 15
mi.Visible = false
mi.Parent = main

local mr = Instance.new("TextButton")
mr.Size = UDim2.new(0.1, 0, 0.8, 0)
mr.Position = UDim2.new(0.89, 0, 0.1, 0)
mr.BackgroundColor3 = Color3.new(0, 0.3,0.6)
mr.BorderSizePixel = 0
mr.Text = "–"
mr.TextColor3 = Color3.new(255, 255, 255)
mr.BackgroundTransparency = 0
mr.Font = Enum.Font.Arial
mr.TextSize = 15
mr.Parent = main

local by = Instance.new("Frame")
by.Size = UDim2.new(1, 0, 5, 0)
by.Position = UDim2.new(0, 0, 1, 0)
by.BackgroundColor3 = Color3.new(0, 0, 0.2)
by.BorderColor3 = Color3.new(0, 0, 0)
by.BorderSizePixel = 0
by.Active = false
by.BackgroundTransparency = 0
by.Parent = main

local cre = Instance.new("TextLabel")
cre.Size = UDim2.new(0.9, 0, 0.1, 0)
cre.Position = UDim2.new(0, 0, 0, 0)
cre.BackgroundColor3 = Color3.new(0, 0, 0)
cre.BorderColor3 = Color3.new(0, 0, 0)
cre.BorderSizePixel = 0
cre.Text = "Cracked by:belb24"
cre.TextColor3 = Color3.new(255, 255, 255)
cre.BackgroundTransparency = 1
cre.Font = Enum.Font.Arial
cre.TextSize = 10
cre.Parent = by

local yt = Instance.new("TextLabel")
yt.Size = UDim2.new(0.38, 0, 0.1, 0)
yt.Position = UDim2.new(0, 0, 0.1, 0)
yt.BackgroundColor3 = Color3.new(0, 0, 0)
yt.BorderColor3 = Color3.new(0, 0, 0)
yt.BorderSizePixel = 0
yt.Text = "Youtube: belb24"
yt.TextColor3 = Color3.new(255, 255, 255)
yt.BackgroundTransparency = 1
yt.Font = Enum.Font.Arial
yt.TextSize = 10
yt.Parent = by

local box = Instance.new("TextBox")
box.Size = UDim2.new(0.9, 0, 0.3, 0)
box.Position = UDim2.new(0.05, 0, 0.25, 0)
box.BackgroundColor3 = Color3.new(0, 0, 1)
box.BorderSizePixel = 0
box.Text = ""
box.TextColor3 = Color3.new(1,1,1)
box.BackgroundTransparency = 0.8
box.Font = Enum.Font.SourceSans
box.TextSize = 15
box.PlaceholderText = "Enter Text..."
box.TextWrapped = true
box.ClearTextOnFocus = false
box.MultiLine = true
box.TextYAlignment = Enum.TextYAlignment.Top
box.TextXAlignment = Enum.TextXAlignment.Left
box.Parent = by

local send = Instance.new("TextButton")
send.Size = UDim2.new(0.9, 0, 0.2, 0)
send.Position = UDim2.new(0.05, 0, 0.6, 0)
send.BackgroundColor3 = Color3.new(0, 0.3, 0.6)
send.BorderSizePixel = 0
send.Text = "Send Text"
send.TextColor3 = Color3.new(255, 255, 255)
send.BackgroundTransparency = 0
send.Font = Enum.Font.Arial
send.TextSize = 15
send.Parent = by

mi.MouseButton1Click:connect(function()
    mi.Visible = false
    mr.Visible = true
    by.Visible = true
    end)

mr.MouseButton1Click:connect(function()
    mi.Visible = true
    mr.Visible = false
    by.Visible = false
    end)


local function convertText()
local text = box.Text
local convertedText = ""

local conversionTableUpper = {
    A = "Ạ", B = "Ḅ", C = "C", D = "Ḍ", E = "Ẹ",
    F = "F", G = "Ģ", H = "Ḥ", I = "Ị", J = "J",
    K = "Ḳ", L = "Ḷ", M = "Ṃ", N = "Ṇ", O = "Ọ",
    P = "Р", Q = "Q", R = "Ṛ", S = "Ṣ", T = "Ṭ",
    U = "Ụ", V = "Ṿ", W = "Ẉ", X = "Ẋ", Y = "Ỵ", Z = "Ẓ"
}

local conversionTableLower = {
    a = "ạ", b = "ḅ", c = "c", d = "ḍ", e = "ẹ",
    f = "f", g = "ɡ", h = "ḥ", i = "ị", j = "ј",
    k = "ḳ", l = "ḷ", m = "ṃ", n = "ṇ", o = "ọ",
    p = "р", q = "q", r = "ṛ", s = "ṣ", t = "ṭ",
    u = "ụ", v = "ṿ", w = "ẉ", x = "ẋ", y = "ỵ", z = "ẓ", ["|"] = "\r",
}

for char in text:gmatch(".") do
local convertedChar = conversionTableUpper[char] or conversionTableLower[char] or char
convertedText = convertedText .. convertedChar .. "̲"
end

box.Text = convertedText
end

send.MouseButton1Click:connect(function()
    local TextChatService = game:GetService("TextChatService")
    local Players = game:GetService("Players")

    local function sendMessage(msg)
    local player = Players.LocalPlayer
    if TextChatService.ChatInputBarConfiguration.TargetTextChannel then
    TextChatService.ChatInputBarConfiguration.TargetTextChannel:SendAsync(msg)
    else
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(msg, "All")
    end
    end
    convertText()
    sendMessage(box.Text)
    box.Text = ""
    end)

local conv = Instance.new("TextButton")
conv.Size = UDim2.new(0.9, 0, 0.1, 0)
conv.Position = UDim2.new(0.05, 0, 0.85, 0)
conv.BackgroundColor3 = Color3.new(0, 0.3, 0.6)
conv.BorderColor3 = Color3.new(0, 0, 0)
conv.BorderSizePixel = 0
conv.Text = "Convert"
conv.TextColor3 = Color3.new(255, 255, 255)
conv.BackgroundTransparency = 0
conv.Font = Enum.Font.Arial
conv.TextSize = 15
conv.Parent = by

conv.MouseButton1Click:connect(function()
convertText()
end)


local npfix = Instance.new("ScreenGui")
    npfix.Parent = game.CoreGui

    local MAIN = Instance.new("Frame")
    MAIN.Size = UDim2.new(0.25, 0, 0.3, 0)
    MAIN.Position = UDim2.new(0.7, 0, 0.65, 0)
    MAIN.BackgroundColor3 = Color3.new(0.1, 0.1, 0.1)
    MAIN.BorderColor3 = Color3.new(0, 0, 0)
    MAIN.BorderSizePixel = 0
    MAIN.Active = false
    MAIN.BackgroundTransparency = 0
    MAIN.Parent = npfix

    local CORN = Instance.new("UICorner")
    CORN.CornerRadius = UDim.new(0.1)
    CORN.Parent = MAIN

    local LABEL = Instance.new("TextLabel")
    LABEL.Size = UDim2.new(1, 0, 0.2, 0)
    LABEL.Position = UDim2.new(0, 0, 0, 0)
    LABEL.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)
    LABEL.BorderColor3 = Color3.new(0, 0, 0)
    LABEL.BorderSizePixel = 0
    LABEL.Text = "Mega big pencil cracked ): | FIXER"
    LABEL.TextColor3 = Color3.new(255, 255, 255)
    LABEL.BackgroundTransparency = 1
    LABEL.Font = Enum.Font.Arial
    LABEL.TextSize = 17
    LABEL.Parent = MAIN

    local SEC = Instance.new("Frame")
    SEC.Size = UDim2.new(1, 0, 0.02, 0)
    SEC.Position = UDim2.new(0, 0, 0.15, 0)
    SEC.BackgroundColor3 = Color3.new(0.25, 0.25, 0.25)
    SEC.BorderColor3 = Color3.new(0, 0, 0)
    SEC.BorderSizePixel = 0
    SEC.Active = false
    SEC.BackgroundTransparency = 0
    SEC.Parent = MAIN

    local CREDIT = Instance.new("TextLabel")
    CREDIT.Size = UDim2.new(1, 0, 0.1, 0)
    CREDIT.Position = UDim2.new(0, 0, 0.16, 0)
    CREDIT.BackgroundColor3 = Color3.new(0, 0, 0)
    CREDIT.BorderColor3 = Color3.new(0, 0, 0)
    CREDIT.BorderSizePixel = 0
    CREDIT.Text = "By: belb24 | Auto Loaded"
    CREDIT.TextColor3 = Color3.new(255, 255, 255)
    CREDIT.BackgroundTransparency = 1
    CREDIT.Font = Enum.Font.Arial
    CREDIT.TextSize = 10
    CREDIT.Parent = MAIN

    local KILL = Instance.new("TextButton")
    KILL.Size = UDim2.new(0.9, 0, 0.5, 0)
    KILL.Position = UDim2.new(0.05, 0, 0.3, 0)
    KILL.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)
    KILL.BorderColor3 = Color3.new(0, 0, 0)
    KILL.BorderSizePixel = 0
    KILL.Text = "Hide Gui"
    KILL.TextColor3 = Color3.new(255, 255, 255)
    KILL.BackgroundTransparency = 0
    KILL.Font = Enum.Font.Arcade
    KILL.TextSize = 25
    KILL.Parent = MAIN

    local CORNER = Instance.new("UICorner")
    CORNER.CornerRadius = UDim.new(0.2)
    CORNER.Parent = KILL

    local HIDE = Instance.new("TextBox")
    HIDE.Size = UDim2.new(0.01, 0, 0.01, 0)
    HIDE.Position = UDim2.new(0, 0, 90, 0)
    HIDE.BackgroundColor3 = Color3.new(0, 0, 0)
    HIDE.BorderColor3 = Color3.new(0, 0, 0)
    HIDE.BorderSizePixel = 0
    HIDE.Text = "hehe"
    HIDE.TextColor3 = Color3.new(255, 255, 255)
    HIDE.BackgroundTransparency = 0
    HIDE.Font = Enum.Font.Arial
    HIDE.TextSize = 15
    HIDE.Parent = npfix

    KILL.MouseButton1Click:connect(function()
        MAIN:Destroy()
        end)

    local function updateChatLogs(message)
    HIDE.Text = HIDE.Text .. "\n" .. message
    end

    local TextChatService = game:GetService("TextChatService")

    TextChatService.OnIncomingMessage = function(textChatMessage)
    local playerName = textChatMessage.TextSource.Name
    local messageContent = textChatMessage.Text
    updateChatLogs(playerName .. ": " .. messageContent)
    end

loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Anthonys-acl-ANTI-CHAT-LOGGER-7184"))()
   end,
})
