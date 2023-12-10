---
title: "Making a Website"
date: 2023-12-10T03:30:25Z
draft: false
tags: ['Libre Software']
---

# Overview
I recommend everyone set up their own personal website as a space on the internet to share their ideas, publicise their work and give updates about their life. The cost is very little and you don't need to be a particularly technical person to get started.

In creating this website, I followed the [LandChad](https://landchad.net/) guide written primarily by [Luke Smith](https://lukesmith.xyz/). It's very detailed and describes the process step by step, starting from scratch all the way to having a running HTTPS website. On this page, I'm not going to repeat what's already in the [LandChad](https://landchad.net/) guide, but just try to point things I did differently that worked better for me. If you prefer following along with a video, you can see [Luke Smith](https://lukesmith.xyz/) roughly following his guide (and a bit more) on YouTube [here](https://www.youtube.com/watch?v=3dIVesHEAzc).

# DNS
I bought and registered my domain name with [GoDaddy](https://www.godaddy.com/). I don't particularly recommend them over any other registrar, it's just that it was the simplest option for me to go for and they tend to have very reasonable prices (as long as you don't opt-in to any of their extra features garbage). The only annoying thing about [GoDaddy](https://www.godaddy.com/) is that they stop you from logging-in if you're using a VPN connection.

# VPS
Choosing who hosts your VPS is actually an important decision unlike choosing your DNS provider. [Luke Smith](https://lukesmith.xyz) is a bit of a [Vultr](https://www.vultr.com/) shill (and potentially receives referral fees from them), however I did not have a very good experience with them. Your three main considerations when choosing a VPS are three Ps:
- Price: If you're not expecting heavy traffic or high usage, then you can find VPSs for less than £20 a month.
- Privacy: You preferably want to have the servers that your VPS runs on in a country which respects privacy (i.e. not [Five Eyes](https://dhitma.neocities.org/html/eyes)). A lot of VPS hosts also take payment in [Bitcoin](https://bitcoin.org/) or [more privacy-protecting cryptocurrencies](https://www.getmonero.org/), which is always a big plus.
- Ports: If you want to also run your own email server on your VPS, then have to allow it as part of their Terms of Service and be willing to unblock the relevant ports (specifically port 25) on your VPS.

[Vultr](https://www.vultr.com/) fails mainly on the last P and are generally unwilling to unblock the email port 25 for most people. Many people have [complained](https://github.com/LukeSmithxyz/emailwiz/issues/172), but [Luke Smith](https://lukesmith.xyz) still continues to recommend them. Personally, I use [Host1](https://host1.no) for my VPS. They're based in Norway and accept payment in [Bitcoin](https://bitcoin.org/). Their current cheapest VPS option is 249 Norwegian Crowns per month, which as of 2023/12/10 translates to £18.20 per month. They also were and potentailly still are the host for [WikiLeaks](https://wikileaks.org/). Be aware that their website is entirely in Norwegian (although they do provide translations) and you will be receiving emails in Norwegian.

I also chose to have my VPS run [Arch Linux](https://archlinux.org/) as opposed to [Debian](https://www.debian.org/) which is the typical recommendation, simply because I am running [Arch](https://archlinux.org/) on my personal PC and so am more familiar with it. I also found that using [pacman](https://wiki.archlinux.org/title/pacman) for installing packages lead to fewer issues. Almost all VPS hosts offer to install both [Debian](https://www.debianorg/) and [Arch](https://archlinux.org/) on their VPSs.

# Securing your VPS
If you follow the [LandChad](https://landchad.net/) guide successfully, you should end up with a simple website, whose files are in ``/var/www/*website_name*``, being served by [NGINX](https://www.nginx.com/), open to HTTPS connections, whose TLS certificate is signed by [Let's Encrypt](https://letsencrypt.org/) via [Certbot](https://certbot.eff.org/). I would then recommend following this [SSH Keys LandChad guide](https://landchad.net/sshkeys/) in order to stop chinese hackers constantly trying to guess your ``root`` user password and completely disable password log-in for your VPS.

# Hugo
From this point, you can choose to go old-school and write your own HTML and CSS files. Instead, I would recommend using a static-site generator [Hugo](https://gohugo.io/). This allows your to create pages for your website using [Markdown](https://www.markdownguide.org/), and [Hugo](https://gohugo.io/) will handle creating the relevant HTML and CSS files. You can also very easily use a wide variety of [Hugo themes](https://themes.gohugo.io/), that will handle how your pages should be displayed and their formatting.

For this website, I use [Luke Smith's](https://lukesmith.xyz) Hugo theme --- [Lugo](https://github.com/LukeSmithxyz/lugo). He has a YouTube video explaining his theme and how to use [Hugo](https://gohugo.io/) in general [here](https://www.youtube.com/watch?v=ZFL09qhKi5I). [Hugo](https://gohugo.io) leads to the best of both worlds, where you can create good-looking, minimalist websites, which are completely static and don't depend on bloated dynamic content.

# Email Server
You can also host your own email server on your VPS. This is more than merely having your own email address domain. It means that programs running on your VPS handle both the sending and receiving of emails, and whatever email client you use connects only to your VPS. The LandChad guide on setting up an email server running [Dovecot](https://www.dovecot.org/) and [Postfix](https://www.postfix.org/) can be found [here](https://landchad.net/mail/smtp/). The instructions in the guide are quite reliant on starting off with specific default config files, which aren't necessary the case and change with new updates. Thus you'll probably have to do some bug-fixing even after following the guide.

# LaTeX
Having [LaTeX](https://www.latex-project.org/) render properly on [Hugo](https://gohugo.io/) websites is actually quite easy using the [KaTeX API](https://katex.org/). I found [this guide](https://mertbakir.gitlab.io/hugo/math-typesetting-in-hugo/) by [Mert Bakir](https://mertbakir.gitlab.io/) very useful.

# RSS
One of the great parts of using the [Lugo](https://github.com/LukeSmithxyz/lugo) theme is that an [RSS](https://www.rssboard.org/) feed is automatically created for your website, which you can see for yourself at the bottom of this page. This means that people using an RSS reader can easily subscribe and be notified when you create any new pages on your website. It's considered old-school tech now-a-days, but if people start using [RSS](https://www.rssboard.org/) conscientiously, then most social media websites would become obsolete. Imagine a world where news and updates from your friends or people/projects you care about get aggregated and sent directly to you where you can view and organise everything in one program you run on your PC. No ads, no tracking, no profit-incentive.

# Git
I'd recommend version controlling the relevant files for your website using [Git](https://git-scm.com/), and hosting the files somewhere publicly accessible. For example, the files for this website are hosted on [GitHub](https://github.com/) [here](https://github.com/IzaacMammadov/personal_website). It allows people to easily make pull requests or issues regarding mistakes or out-of-date information. The best personal websites tend to be collaborative efforts.
