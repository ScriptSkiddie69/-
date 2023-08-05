## Lua selfbot documentation
Lua Selfbot is a module made by ou1z, modified by gaming#5410
## Defining the module
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
```
## Making a new client
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
local Client = LuaSelfbot.Client.new()
```
## Client ready event
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
local Client = LuaSelfbot.Client.new()
Client:on('ready', function()
    print('bot is ready')
end)
```
## Client On Message
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
local Client = LuaSelfbot.Client.new()

Client:on('messageCreate', function(message)
if message.author.id == Client.User.id then -- remove this if statement if u want everyone to use the bot
if message.content == "/reset" then -- detects if client sent a message "/reset"
game.Players.LocalPlayer.Character.Head:Destroy()
elseif message.content == "/reply" then
message.reply('i replied!') -- replies to the discord message
       end
    end
end)
```

## Logging on client
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
local Client = LuaSelfbot.Client.new()
Client:login("TOKEN HERE")
```

## All of the script at once
```lua
local LuaSelfbot = loadstring(game:HttpGet('https://raw.githubusercontent.com/ScriptSkiddie69/-/main/Source'))()
local Client = LuaSelfbot.Client.new()

Client:on('messageCreate', function(message)
if message.author.id == Client.User.id then -- remove this if statement if u want everyone to use the bot
if message.content == "/reset" then -- detects if client sent a message "/reset"
game.Players.LocalPlayer.Character.Head:Destroy()
elseif message.content == "/reply" then
message.reply('i replied!') -- replies to the discord message
       end
    end
end)

Client:login("TOKEN HERE")
```
