# Plug-N-Meet - Scalable, Open source web conferencing system.

Plug-N-Meet is an open source web conferencing system based on high performance WebRTC
infrastructure [livekit](https://github.com/livekit/livekit-server).

![](./github_files/banner.png)

## Features:

1) Compatible with all devices. Browser recommendation: Google Chrome, Firefox. For iOS: Safari.
2) WebRTC based secured & encrypted communication.
3) Scalable and high performance system written in Go programming language which made it possible to distributed as a
   [single binary](https://github.com/mynaparrot/plugNmeet-server/releases) file!
4) **Simulcast** and **Dynacast** features will allow you to continue online conferencing even if your internet
   connection is slow!
5) Easy integration with any existing website or system.
6) Easy customization with functionality, URL, logo, and branding colors.
7) HD audio, video call and Screen sharing.
8) **Shared notepad** and **Whiteboard** for live collaboration.
9) **Virtual background** for webcams.
10) Lock settings.
11) Raise hand.
12) Chatting with File sharing.
13) MP4 Recordings.
14) RTMP Broadcasting

And many more!

The components of Plug-N-Meet are as follows:

1) [plugNmeet-server](https://github.com/mynaparrot/plugNmeet-server), the main backend server written in go.

2) [plugNmeet-client](https://github.com/mynaparrot/plugNmeet-client), which is the main interface/frontend. It's built
   with React and Redux.

3) [plugNmeet-recoder](https://github.com/mynaparrot/plugNmeet-recorder), a node module for recording/rtmp broadcasting
   which is written in TypeScript.

**Demo:**

https://demo.plugnmeet.com/login.html

## Requirements

1) Livekit configured with Redis.
2) `plugNmeet-server` configured with same Redis instance using for livekit.
3) Mariadb server for data storage.

We've created an easy to install script which can be used to install all the necessary components in 5 minutes.
Check [plugNmeet-install](https://github.com/mynaparrot/plugNmeet-install) repo.

## SDKs & Tools

**SDK**

1) [PHP](https://github.com/mynaparrot/plugNmeet-sdk-php)

Following ready to use extensions:

1) [Joomla component](https://github.com/mynaparrot/plugNmeet-joomla)
2) [Moodle Plugin](https://github.com/mynaparrot/plugNmeet-moodle)
3) [Wordpress Plugin](https://github.com/mynaparrot/plugNmeet-wordpress)

Docker:

1. [plugnmeet-server](https://hub.docker.com/r/mynaparrot/plugnmeet-server)

Examples:

1) [Example of API](https://github.com/mynaparrot/plugNmeet-server/wiki/API-Information-(examples))

## Manually

Create `config.yaml`
from [config_sample.yaml](https://raw.githubusercontent.com/mynaparrot/plugNmeet-server/main/config_sample.yaml) &
change necessary info

***Using docker***

```
docker run --rm -p 8080:8080 \
    -v $PWD/config.yaml:/config.yaml \
    mynaparrot/plugnmeet-server \
    --config /config.yaml \
```

You can also
follow [docker-compose_sample.yaml](https://raw.githubusercontent.com/mynaparrot/plugNmeet-server/main/docker-compose_sample.yaml)
file.

You can manually download server from [release](https://github.com/mynaparrot/plugNmeet-server/releases) page too.

## Development

Please follow [this wiki](https://github.com/mynaparrot/plugNmeet-server/wiki/Development) for details.