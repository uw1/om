[[hosting]]
[[deploy]]
[[docker]]

# web
[更好用的 Web 服务器：Caddy - 知乎](https://zhuanlan.zhihu.com/p/144208057)
caddy [超越 Nginx！号称下一代 Web 服务器，用起来够优雅！ - 掘金](https://juejin.cn/post/7085519712901136392)

# ci
[Work with GitHub Actions in Your Terminal with GitHub CLI | Hacker News](https://news.ycombinator.com/item?id=26822169)
[PipedreamHQ/pipedream: Connect APIs, remarkably fast. Free for developers.](https://github.com/PipedreamHQ/pipedream)

# local virtual machine
[建议人手一套：个人专属多节点Linux环境打造，Linux操作系统学习实验环境安装配置视频教程 -B站](https://www.bilibili.com/video/BV1bA411b7vs)

# aws/docker
[The Architecture Behind A One-Person Tech Startup](https://anthonynsimon.com/blog/one-man-saas-architecture/)
# vps
[Ask HN: What novel tools are you using to write web sites/apps? | Hacker News](https://news.ycombinator.com/item?id=26693959)
	No SQL database; I just keep everything in memory in native data structures and flush to disk periodically; I have a big swap file set up so that I can keep a working set bigger than the RAM

# free
[Stack on a Budget – A collection of services with free tiers | Hacker News](https://news.ycombinator.com/item?id=27022075)
	Good for hobby or personal projects, but not if you’re building something for work. Many of these “free” tiers are designed to vendor lock you before they walk you off a pricing cliff.
	Take Auth0. Free for up to 7,000 user but then it jumps to about $250/month. Migrating from Auth0 is a pain. You should really only consider these “free” services if you think you’ll always be in the free tier, and if you’d use the service even if it wasn’t free.
# cheap
[https://www.hetzner.com/cloud](https://www.hetzner.com/cloud)
	I didn't know Hetzner Cloud, an first thought, "wow, it's even cheaper than OVH, which is already a bargain" ([https://www.ovhcloud.com/fr/vps/](https://www.ovhcloud.com/fr/vps/)).
	But then I realized you are limited in bandwithd to 20 TB, while OVH provides, for barely more €, unmetered traffic. It's huge because you never have to worry about a random spike day, a bot doing something stupid, an attack, or a use case switch (ex: video streaming).
	OVH might give you 'unmetered' traffic, but their connectivity \_sucks\_. Hetzner's 20TB/mo is equivalent to a constant measly ~60Mbps, but at least you'll reliably get this rate to most of the Internet, and very often will be able to saturate your link speed for peak usage.