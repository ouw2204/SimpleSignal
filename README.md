# SimpleSignal
```lua
local SignalLoader = require(ReplicatedStorage.Packages.SimpleSignal)
local Signal = SignalLoader.new()
```
## Connect
```lua
local Connection = Signal:Connect(function(...)

end)
task.wait(2)
Connection:Disconnect();
```
Optionally pass a table as the second argument; the connection will be removed from it on `:Disconnect()`:
```lua
Signal:Connect(function(...) end, MyConnectionsTable)
```
## Once
Connects a listener that auto-disconnects after firing once.
```lua
Signal:Once(function(...)

end)
```
## Fire
```lua
Signal:Fire("Message")
```
## BasicFire
Fires without `task.spawn` — listeners run synchronously on the firing thread.
```lua
Signal:BasicFire("Message")
```
## SafeFire
Waits until a connection is established before firing
```lua
Signal:SafeFire("Message")
```
## Wait
Yields the current thread until the signal next fires, returning the fired arguments. Pass an optional `timeout` (seconds); on timeout, returns `nil`.
```lua
local result = Signal:Wait(5)
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
### Wally
```
SimpleSignal = "mountaindouw/simplesignal@1.2.3"
```
### Github
Download `SimpleSignal.rbxm` from this repository and drag it into Roblox Studio.
