# Orange-Auth
This is a public library that will help you to avoid skids and protect your scripts.

## Booting the library

```lua
local OrangeAuth = loadstring(game:HttpGet("https://raw.githubusercontent.com/Moligrafi001/Orange-Auth/refs/heads/main/Auth.lua", true))()
```
Paste this in the top of your script. It works with any UI Library.
> [!NOTE]
> Make sure you won't use the `local OrangeAuth` again after you setting up this

### Settings
```lua
OrangeAuth.Initialize({
    Loadstring = true,
})
```
If you are using `loadstring` in ur script, set it to true. It will protect any possible loadstring hook that may harm the your code safety.

### Example
```lua
local OrangeAuth = loadstring(game:HttpGet("https://raw.githubusercontent.com/Moligrafi001/Hallow-Hub/main/extra/Auth.lua", true))()

OrangeAuth.Initialize({
    Loadstring = true,
})

if OrangeAuth.Check() then
    print("Safe Loadstring") -- You can replace with your loadstring
else
    game:GetService("Players").LocalPlayer:Kick("GET OUT!")
end
```
In the code above, if the auth returns true then it will print `Safe Loadstring` but if the auth detects a skid it will kick the player with the reason `GET OUT!`. 
