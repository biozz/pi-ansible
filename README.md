# pi-ansible

This project is heavily inspired by [geerlingguy/internet-pi](https://github.com/geerlingguy/internet-pi). It does basically the same with the following differences:

- [showwin/speedtest-go](https://github.com/showwin/speedtest-go) and [speedtest-go-prometheus](https://github.com/biozz/speedtest-go-prometheus) instead of [MiguelNdeCarvalho/speedtest-exporter](https://github.com/MiguelNdeCarvalho/speedtest-exporter) - because it produces a compact binary with a non-blocking metrics endpoint, speed checking is done in the background
- [0xERR0R/blocky](https://github.com/0xERR0R/blocky) instead of [pi-hole/pi-hole](https://github.com/pi-hole/pi-hole) - because also written in go and I don't need pretty admin interface, having ansible doing all of the config automation
- no shelly plug stuff, starlink, ping host (I might add ping in the future) or any other stuff except mentioned above
- strong default configuration with minimal options set

## Caveats

- blocky dashboard has a hardcoded host `blocky.in`, that's what I usually setup in my router for internal domains
- containers restart is not predictable after you change templates and configs, manual removal helps
