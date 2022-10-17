# ALS - Another Looking-glass Server

[![docker image build](https://github.com/wikihost-opensource/als/actions/workflows/docker-image.yml/badge.svg)](https://github.com/wikihost-opensource/als/actions/workflows/docker-image.yml)

## Quick start

```
docker run -d --name looking-glass --restart always --network host gzmaxsum/looking-glass-server
```

[DEMO](http://lg.hk1-bgp.hkg.50network.com/)

## Host Requirements

- Can run docker (yes, only docker is required)

## Image Environment Variables

| Key                       | Example   | Default                         | Description                                    |
| ------------------------- | --------- | ------------------------------- | ---------------------------------------------- |
| HTTP_PORT                 | 80        | 80                              | which HTTP port should use                     |
| SPEEDTEST_FILE_LIST       | 100MB 1GB | 1MB 10MB 100MB 1GB              | size of static test files, separate with space |
| PUBLIC_IPV4               | 1.1.1.1   | (fetch from http://ifconfig.co) | The IPv4 address of the server                 |
| PUBLIC_IPV6               | fe80::1   | (fetch from http://ifconfig.co) | The IPv6 address of the server                 |
| DISPLAY_TRAFFIC           | true      | true                            | Toggle the streaming traffic graph             |
| ENABLE_SPEEDTEST          | true      | true                            | Toggle the speedtest feature                   |
| UTILITIES_PING            | true      | true                            | Toggle the ping feature                        |
| UTILITIES_TRACEROUTE      | true      | true                            | Toggle the traceroute feature                  |
| UTILITIES_IPERF3          | true      | true                            | Toggle the iperf3 feature                      |
| UTILITIES_IPERF3_PORT_MIN | 30000     | 30000                           | iperf3 listen port range - from                |
| UTILITIES_IPERF3_PORT_MAX | 31000     | 31000                           | iperf3 listen port range - to                  |

## Features

- [X] HTML 5 Speed Test
- [X] Traceroute - IPv4
- [X] Ping - IPv4
- [X] iPerf3 server
- [X] Streaming traffic graph

## TO-DO List

- [ ] Traceroute - IPv6
- [ ] Ping - IPv6

## Thanks to

https://github.com/librespeed/speedtest

## License

Code is licensed under MIT Public License.

* If you wish to support my efforts, keep the "Powered by LookingGlass" link intact.
