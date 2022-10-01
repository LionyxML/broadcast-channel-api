# broadcast-channel-api

An example on how to use the BroadcastChannel Javascript API

You can check its compatibility and docs here:
https://developer.mozilla.org/en-US/docs/Web/API/Broadcast_Channel_API

When served from the same origin, we can stabilish a BroadcastChannel to
communicate between different browser windows, tab pages, or browser contexts
under iframes.

Basic usage:

```
const channel = new Broadcastchannel("event_bus");

channel.postMessage("Hello! I am sending you this message!");

channel.onmessage = function (e) {
  console.log("Recieved message: ", e.data);
};

channel.close();

```

Explore the HTML examples in this repo.
