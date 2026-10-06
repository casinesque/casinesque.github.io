+++
draft = false
title = 'GL.Inet-Beryl-AX'
weight = 1
tags = ["tech","2026"]
showtoc = false
author= [""]
showCodeCopyButtons = false
ShowPostNavLinks = false
ShowBreadCrumbs =false
ShowCodeCopyButtons = false
ShowWordCount = false
ShowRssButtonInSectionTermList = false
UseHugoToc = false
disableSpecial1stPost = false
disableScrollToTop = false
comments = false
hidemeta = false
hideSummary = false
tocopen = false
ShowReadingTime = false
ShowShareButtons = false
+++

**# Your best tech mate on travels!**

As someone working remotely, having a portable tech stack is essential. I am pretty minimal about it: I usually just bring my YODOIT portable screen and a GL.iNet Beryl AX travel router. In particular, the Beryl AX has become more than essential to me, since it solves a very practical problem: keeping my network setup consistent wherever I am.

This post is not meant to be a clever product review. It is more about the problem I was trying to solve, why a small travel router helped, and how this kind of setup can make remote work less annoying when you move between different places.

## The problem with working from random networks

When you work from home, your devices usually live in a known environment. Your laptop knows the Wi-Fi, your phone connects automatically, your tablet is already configured, and maybe you also have some DNS filtering, VPN rules, or local devices you rely on.

When you travel, that disappears.

One day you are on a hotel Wi-Fi, the next day in a coworking space, then in an Airbnb, then maybe using your phone as a hotspot because the available network is bad or not trustworthy enough. Every place has its own SSID, captive portal, signal quality, restrictions, and security assumptions.

Of course, you can just connect each device manually every time and most people do exactly that, but after a while it becomes annoying, especially if you care about security, use several devices, or want your setup to behave in a predictable way.

The idea I wanted was simple: instead of making all my devices adapt to every network I find, I wanted one small device to adapt for them.

## The basic idea: bring your own network

This is where the GL.iNet Beryl AX comes in.

The concept is straightforward: my laptop, phone, tablet and other devices only know one Wi-Fi network, the one created by the Beryl AX. Wherever I am, they keep connecting to the same SSID, with the same password and the same basic rules.

Then the Beryl AX takes care of connecting to the outside world.

That outside connection can change. It can be a hotel Wi-Fi, an Ethernet cable, my phone through USB tethering, or another temporary network. But my devices do not need to care. They stay behind the router, on my own small network.

This makes the setup much more predictable. I do not need to save random Wi-Fi credentials on all my devices. I do not need to reconfigure everything every time I move. I can also keep a clearer separation between the network I am using as an internet source and the network where my own devices live.

For remote work, that is often the real win.

## Why I chose the GL.iNet Beryl AX

I ended up getting two GL.iNet Beryl AX units, also known as the GL-MT3000. Partly because I have some specific needs around networking, security, and mobility. Partly because I like understanding how things are made, and sometimes that means making my own life slightly more complicated.

The Beryl AX is small enough to carry around, but it is not a toy. It is a Wi-Fi 6 travel router based on GL.iNet's custom OpenWrt firmware. That matters because it gives you two different levels of use.

On one side, you get a simple web interface for the things most people actually need: connecting to another Wi-Fi, setting up your own SSID, using Ethernet, enabling USB tethering, configuring VPNs, changing DNS settings, and updating the device.

On the other side, because OpenWrt is underneath, you are not completely locked into a simplified consumer interface. If you need more advanced configuration, LuCI is available, and you can install additional packages.

That balance is the reason I like it. It can be easy when I just need to get online, but it does not become useless when I want more control.

## The connection modes that matter in practice

The most useful part of this setup is that the Beryl AX can get internet in different ways.

The first one is USB tethering. I can connect my phone to the router with a cable and use the phone's mobile data connection as the uplink. This is much cleaner than enabling the phone hotspot and connecting every device to it. The phone just provides connectivity, while the router continues to manage my actual network.

The second one is Wi-Fi repeater mode. The Beryl AX connects to an existing Wi-Fi network, such as a hotel, coworking space, office, or rented apartment network, and then creates my own separate Wi-Fi for my devices. This is probably the mode most people will use while travelling.

The third one is Ethernet. If there is a wired connection available, I can plug it into the router and use that as the uplink. This is often the best option when stability matters, for example during long work sessions, video calls, or large downloads.

The important part is that these modes all keep the same logic: my devices stay connected to my network, and the router deals with whatever network is available outside.

## Isolation is more important than convenience

The convenience is nice, but the bigger reason I care about this setup is isolation.

When I connect directly to a random Wi-Fi, my device becomes part of that environment. Maybe the network is fine, maybe it is badly configured, maybe it is crowded, maybe it has restrictions, maybe I simply do not know enough about it.

With the Beryl AX, I can treat that network as an uplink instead of a place where all my devices live directly. My laptop, phone, and other devices stay on my own side of the router.

This does not magically make every network safe, and it does not replace common sense. I still use VPNs where appropriate, keep devices updated, and avoid trusting unknown networks more than necessary. But having a small router between my devices and the outside network gives me a cleaner boundary.

For me, that boundary is worth carrying one more device.

## DNS filtering and VPNs

Another reason the Beryl AX is useful is that it can run services that normally would need to be configured device by device.

One example is AdGuard Home. The Beryl AX supports it, which means DNS filtering can happen directly on the router. Instead of installing and maintaining filtering rules on every device, I can apply them at the network level. That can help reduce tracking, block unwanted domains, and keep the browsing environment a bit cleaner.

Then there are VPNs. The Beryl AX supports WireGuard and OpenVPN, and this is very useful for remote work. You can configure the router as a VPN client so that the devices connected to it go through a tunnel, even if those devices do not have their own VPN client installed. 
Anyway, if you just need to navigate with a different IP, most likely from your home country, you could also rely on tailscale with its Exit Node feature, but if i'm not wrong this isn't supported on beryl AX.

This can be useful for connecting back home, reaching company resources, using a VPS as an exit point, or simply keeping a more consistent network path while travelling.

Again, the key point is not that the router does something impossible. The key point is that it centralizes the setup. Configure it once on the router, and the devices behind it benefit from that configuration.

## The hardware is enough for real use

For a small travel router, the Beryl AX has very respectable hardware. It has Wi-Fi 6, a MediaTek dual-core processor, 512 MB of RAM, 256 MB of flash storage, a 2.5G Ethernet port, a Gigabit Ethernet port, and USB 3.0.

Those specs matter because this kind of device becomes frustrating very quickly if the hardware is too limited. If you want to run VPNs, DNS filtering, multiple clients, and maybe some additional OpenWrt packages, you need a bit of headroom.

The Beryl AX has enough for the kind of mobile setup I care about. It is still a small router, so expectations should be realistic, but it does not feel like a fragile emergency gadget.

## Why I have two

Having two units is not necessary for most people, but it makes sense for how I like to work.

One can stay in a more stable location and i used it as an additional AP since my carrier's appliance was very limited, while the other stays in my backpack. One can be used as the main device, while the other can be used for testing, backup, or experimenting without breaking the setup I actually rely on.

If you only want a simple travel network, one is enough. If you like to test configurations or keep a fallback ready, a second one is useful.

## Who this setup is for

This setup is probably useful if you often work away from home, use multiple devices, care about not connecting everything directly to random networks, or want your Wi-Fi environment to remain the same wherever you go and is also useful if you enjoy having control over DNS, VPNs, routing, and network behavior without carrying a full networking lab with you.

It is probably not necessary if you only travel occasionally and are happy using your phone hotspot. In that case, the Beryl AX might be more than you need.

But if you have ever arrived somewhere, connected to a bad Wi-Fi, reconfigured three devices, fought with a captive portal, enabled a VPN manually, and wished your setup was less improvised, then a travel router like this starts to make a lot of sense.

## Final thoughts

The GL.iNet Beryl AX is useful because it solves a boring problem in a very practical way. It lets you carry your own small network with you.

That means fewer repeated configurations, more predictable behavior, better separation from guest networks, and a central place to manage things like DNS filtering and VPNs.

For me, it has become part of the basic remote work kit, next to my portable screen. Not because it is flashy, but because it removes friction every time I need to work from somewhere that is not home.

And when you work while moving around, removing friction is often exactly what makes the difference.
