# SimpleSignal
```lua
local SignalLoader = requrie(ReplicatedStorage.Packages.SimpleSignal)
local Signal = SignalLoader.new()
```
## Connect
```lua
local Connection = Signal:Connect(function(...)

end)
task.wait(2)
Connection:Disconnect();
```
## Fire
```lua
Signal:Fire("Message")
```
## SafeFire
Waits until a connection is established before firing
```lua
Signal:SafeFire("Message")
```
## Destroy
```lua
Signal:Destroy()
```
## DisconnectAll
```lua
Signal:DisconnectAll()
```
Removes all current connections
## Installation
### Roblox

### Wally
```
SimpleSignal = "prophetouw/simplesignal@1.0.14"
```
### Github
