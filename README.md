# ROBLOX WEBHOOK INTERIGATION

Due to the fact that cloudfare has banned ROBLOX webhooks from ROBLOX. We have to use a proxy server.

Note: It still works in studio.


# Why did they ban it?
They banned it due to ROBLOX Developers sending spammy things.


# Is it possible to get around?
Yes thats why we use a proxy server.

# What hosting app do we use?
Slack .

# Module Code
```
local HTTP = game:GetService("HttpService")
local URL = "ENTER URL HERE"

local BOTModule = {}

function BOTModule:SendMessage(Message)
	
	local SlackMessage = HTTP:JSONEncode({
		
		text = ""..Message..""
		
	})
	
	HTTP:PostAsync(URL, SlackMessage)
	
end

return BOTModule
```
This goes into server script storage.

# Script Code
```
local SS = game:GetService("ServerStorage")
local BOTModule = require(SS.BOTModule)

wait(5)

BOTModule:SendMessage("Hello world!")
```

Thank you for using this product from Developer Tech.
We do not have a tutorial on how to do this so here is a online tutorial: https://www.youtube.com/watch?v=r396DVbSyW8

©️ Developer Tech 2021
Support: https://discord.gg/bvaqRQPvm2
