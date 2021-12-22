# ROBLOX WEBHOOK INTERIGATION

Model Link:
```
https://www.roblox.com/library/8315010090/Roblox-Proxy-Integration
```
CloudFare has banned discord webhooks from being sent from ROBLOX. 

Note: It still works in studio.


# Why did they ban it?
They banned it due to ROBLOX Developers sending spammy things.


# Is it possible to get around?
Yes thats why we use a proxy server.

# What hosting app do we use?
Slack .

# What is Slack?
```
Slack is a proprietary business communication platform developed by American software company 
Slack Technologies and now owned by Salesforce. Slack offers many IRC-style features, including persistent chat rooms organized by topic,
private groups, and direct messaging.
```

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
Goes into server storage
Thank you for using this product from Developer Tech.
We do not have a tutorial on how to do this so here is a online tutorial: https://www.youtube.com/watch?v=r396DVbSyW8

©️ Developer Tech 2021
Support: https://discord.gg/bvaqRQPvm2
