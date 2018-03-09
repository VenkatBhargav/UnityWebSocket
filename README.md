# Web Sockets for Unity

For Unity developers looking to use Web Sockets in their Unity game / app.

## External dependencies
**First download the required dependencies and extract the contents into your Unity project "Assets" folder.**
- [WebSocket-Sharp](https://github.com/sta/websocket-sharp)

## :octocat: Download instructions
This project contains git submodule dependencies so use:

    `git clone --recursive https://github.com/Unity3dAzure/UnityWebSocket.git`

Or if you've already done a git clone then use:

    `git submodule update --init --recursive`

## Developer notes

When using Unity 2017.2.1p2 and the .NET 4.6 API (Experimental) player settings I tried the system [ClientWebSocket](https://msdn.microsoft.com/en-us/library/system.net.websockets.clientwebsocket%28v=vs.110%29.aspx?f=255&MSPPError=-2147217396). While this initially had some success the problem was that after 3 mins or so the following error would occur on the async/await connect function:

```
ObjectDisposedException: Cannot access a disposed object.
Object name: 'System.Net.Sockets.NetworkStream'
```

Therefore I opted for [WebSocket-Sharp](https://github.com/sta/websocket-sharp) which targets .NET Framework 3.5 and works in the Unity 2017 editor and doesn't seem to have the same issue.

Questions or tweet [@deadlyfingers](https://twitter.com/deadlyfingers)