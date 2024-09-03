# code

```lua
local httpService = game:GetService("HttpService")
local button = script.Parent
local url = "your discord webhook url"
local plr = game:GetService("Players")

plr.PlayerAdded:Connect(function(player)
    httpService:PostAsync(url, httpService:JSONEncode({
        content = "Hello From Discord!", -- you can change this string
    }))
end)
```

## example usage

```lua
local httpService = game:GetService("HttpService")
local button = script.Parent
local url = "https://discord.com/api/webhooks/1280476554899488891/yvVWkclGuAeMRA-8N5NYgMFH09-7on95-qHEOWZZzxyivteMn5oYGitTBSGyVNtq33Ku"
local plr = game:GetService("Players")

plr.PlayerAdded:Connect(function(player)
    local plruser = player.username
    local plrage = player.AccountAge
    httpService:PostAsync(url, httpService:JSONEncode({
        content = "someone has joined server: "..plruser.. "account age: "..plrage,
        username = "test"
    }))
end)
```

sends message of player username and account age


![image](https://github.com/user-attachments/assets/3e5c1f61-15ac-4065-b7f0-c8ff6c3d55a8)

for more information about webhook check this

https://gist.github.com/Birdie0/78ee79402a4301b1faf412ab5f1cdcf9
