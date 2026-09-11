# AIO-metadata-Formatter
A custom formatter to use with aiometadata 
Works with your debrid service and works for both p2p and https streams
![alt text](https://github.com/frasersimpson126/AIO-metadata-Formatter/blob/main/example.png)

Name template
{stream.resolution::exists["{stream.resolution::replace('2160p', '💎 4K')::replace('1440p','✨ 1440')::replace('1080p','🔥 1080p')::replace('720p','💿 720p')::replace('480p','💩 480p')}"||""]}
{?{service.shortName}?}{service.cached::istrue["⚡"||""]}{service.cached::isfalse["⏳"||""]}{service.name::exists[""||" {stream.seeders::>=0["🌱 {stream.seeders}"||""]}"]}
{addon.name::=Penguplay["⚡http "||""]}

Description template
{stream.size::exists["💾 {stream.size::bytes}"||"N/A"]}
{stream.quality::exists["🎬 {stream.quality} "||""]}
{addon.name::exists["ℹ️ {addon.name}"||"N/A"]}
