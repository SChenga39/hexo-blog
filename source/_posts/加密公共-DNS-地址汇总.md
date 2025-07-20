---
title: 加密公共 DNS 地址汇总
date: 2023-01-26 00:00:00
tags: [DNS, 隐私保护]
---

## 国内

### 阿里

支持 ECS，即使通过 DoH 访问仍然有污染

- DoH：支持 DoH3
  - <https://dns.alidns.com/dns-query>
  - <https://223.5.5.5/dns-query>
  - <https://223.6.6.6/dns-query>
- DoT：`dns.alidns.com`

### 腾讯

不完全支持 ECS，有些地址没有解析到最近的服务器

- DoH：不支持 DoH3
  - <https://doh.pub/dns-query>
  - <https://120.53.53.53/dns-query>
  - <https://1.12.12.12/dns-query>
- DoT：`dot.pub`

### IPv6 DNS

2025-07-20 更新：已不可用

~~IPv4 到 IPv6 时代的过渡 DNS，解析准确度与阿里 DNS 相当~~

- ~~DoH：不支持 DoH3~~
  - ~~<https://dns.ipv6dns.com/dns-query>~~
- ~~DoT：`dns.ipv6dns.com`~~

### Easymos DNS

公益 DNS，上游使用国内的阿里和 DNSPod、国外的 Opendns 和 Google DNS 等，国内国外解析效果均可

- DoH：不支持 DoH3
  - <https://doh.apad.pro/dns-query>

### iQDNS

2025-07-20 更新：已不可用

~~隐私至上的公益 DNS，可在 <https://iqiq.io/servers.html> 查看完整服务器列表~~

~~已知缺点：大概率会将 bilibili 负载均衡域名 `i0.hdslb.com` 解析到香港导致大陆 bilibili 图片加载缓慢~~

- ~~DoH：不支持 DoH3~~
  - ~~<https://cn-east.iqiqzz.com/dns-query>~~
- ~~DoT：`cn-east.iqiqzz.com`~~
- ~~DoQ：`cn-east.ovo.glass`~~

### 清华 Tuna DNS

不支持 ECS，大多数域名都会解析到北京附近

- DoH：不支持 DoH3
  - <https://101.6.6.6:8443/dns-query>

## 国外

### Google DNS

支持 ECS

- DoH：支持 DoH3
  - <https://dns.google/dns-query>
  - <https://8.8.8.8/dns-query>
  - <https://8.8.4.4/dns-query>
- DoT：`dns.google`

### Cloudflare DNS

注重隐私，不支持 ECS

- DoH：支持 DoH3
  - <https://1dot1dot1dot1.cloudflare-dns.com>
  - <https://1.1.1.1/dns-query>
  - <https://1.0.0.1/dns-query>
- DoT：`cloudflare-dns.com`

### OpenDNS

支持 ECS

- DoH：不支持 DoH3
  - <https://doh.opendns.com/dns-query>

### CleanBrowsing

支持 ECS

- DoH
  - 不屏蔽成人内容：<https://doh.cleanbrowsing.org/doh/security-filter>
  - 屏蔽部分成人内容：<https://doh.cleanbrowsing.org/doh/adult-filter>
  - 屏蔽所有成人内容：<https://doh.cleanbrowsing.org/doh/family-filter>
- DoT
  - 不屏蔽成人内容：`security-filter-dns.cleanbrowsing.org`
  - 屏蔽部分成人内容：`adult-filter-dns.cleanbrowsing.org`
  - 屏蔽所有成人内容：`family-filter-dns.cleanbrowsing.org`

### DNS.SB

注重隐私保护，不支持 ECS

- DoH
  - <https://doh.dns.sb/dns-query>

### AdGuard DNS

- DoH
  - 过滤广告：<https://dns.adguard.com/dns-query>
  - 家庭保护：<https://dns-family.adguard.com/dns-query>
  - 不过滤：<https://dns-unfiltered.adguard.com/dns-query>
- DoT / DoQ
  - 过滤广告：`dns.adguard.com`
  - 家庭保护：`dns-family.adguard.com`
  - 不过滤：`dns-unfiltered.adguard.com`
