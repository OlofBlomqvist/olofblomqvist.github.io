# Introduction

I'm a software engineer located in Gothenburg, Sweden. 

This site is used for hosting various articles about topics that interest me, and documenting various personal projects.

You can contact me by email at <olof@twnet.se> ✉️ 

## For recruiters

Thanks for coming by! I get messages from recruiters every day and do not have time to respond to everyone; sorry if I haven't gotten back to you! 

> I am **NOT** actively looking to change jobs at this time.

# Technical History

## Early days

I started playing around with QBasic somewhere around 1995 and later explored Pascal, Perl, Bash & Python. At some point around 2000 I tried to learn C and hit a brick wall. It would be several years before I got back to learning system-level programming for real.

My time playing around with coding did however push me towards using Linux for everything non-gaming related ever since; starting with Storm Linux (1999).

## Studies

I studied electronics, microprocessors, operating systems & network infrastructure for four years of upper secondary school (sixth form / high school). After that I went on to study network security for two years (Higher Vocational Education) learning about different network protocols and how to understand and effectively analyze network traffic using tools such as Wireshark.

## Professional career

**tl;dr** - I started working in tech-support (1st through 3rd line) leading up to working as a "technical infrastructure specialist" for a couple of years before finally ending up working full-time as a software engineer.

### Technical Support & System Administration

During the first couple of years working professionally in tech, around 2009 to 2017, I was primarily tasked with technical support and infrastructure management (i.e. sys admin type of work). As a lazy person, it did not take long before starting to automate things and I became fairly good at using Powershell. It was also around that time that I started realizing that knowing C# would be very useful to me in many cases and started to spend a lot of time learning it and started using it professionally at work.

Having previously studied IT Security I was also able to take on tasks doing post incident reporting with respect to malware and intrusions, as well as network capture analysis, further improving my understanding of how networking actually works on (very) large networks. 

I worked for some time in different roles and ended up learning lot's of things such as:

- Writing technical documentation.
- SCCM Management: app deployments and os patching. 
- AD: Creating & Maintaining GPO's.
- Post-incident root cause analysis.
- Troubleshooting & Root cause analysis:
    - Active Directory GPO issues.
    - Network connectivity and performance issues (often firewall or proxy-server issues).
    - Figuring out why a subset of client's were misbehaving in some way or another.
    - Analysing memory dumps of Windows clients.
    - Analysing huge pcap/network capture files using Wireshark.

... I won't list all the different types of work I've done, but the time spent on this side of tech helped me gain both wide and deep knowledge of technical infrastructure and computers in general, which turned out to be extremely useful for me once I went over to become a full-time software engineer. This broad technical background has made it easier to design solutions and troubleshoot complex issues.

### Software engineering (part 1)

In late 2017, After working in tech for some 7-8 years and gaining confidence in my self-taught programming skills, I started working as a developer at a company providing a product for automating business workflows - built in C# & using PowerShell scripts for many automation tasks. Pretty much a perfect match for me since those were languages I was feeling very comfortable with already. 

Many of the automation tasks included communicating with different external systems but also a large amount of programmatically managing Active Directory, SCCM,Microsoft Exchange, or directly controlling Windows machines through WMI or PowerShell remoting.  All of which I had already had experience working with.

As was the case with most .NET based shops at the time, the tech stack consisted of WCF services and MSSQL databases but also included Windows Workflow Foundation and Service Bus.

While working here I had also been using F# for a bunch of different side-projects and was really getting in to the more functional style of programming. My go to scripting language had also quickly changed from python and powershell to F#.

I ended up implementing support in the product for using C# libraries rather than PS scripts as a way to power workflows in the application using reflection, which was not something I had seen as very useful before. 

### Software engineering (part 2)

Fast forwarding to 2019 having worked for some short years with system automation, I started working for a company in the hotel and travel industry. Like at my previous job I started as a full-stack developer, but after some time started focusing more and more on the backend side, as frontend development is not really that interesting to me.

*Like with my previous work in automation, message queues were used here to make for a reliable system - but unlike the mess that is Microsoft Windows Workflow Foundation and the related self-hosted service bus systems... The combination of Redis & RabbitMQ used for this product was like a dream to work with!*

The systems here (when I started that is) were based on .NET 4.8, Redis, RabbitMQ, MSSQL & WCF services. We started migrating slowly away from .NET 4.8 and since then switched between dotnet core 3 thru 8. The two largest internal services were moved from WCF to CoreWCF.

Having worked successfully with gRPC on a side-project previously I ended up pushing for using that instead of (Core)WCF for new internal projects, something that has been working out well so far.

### DevOps: PRs, CI, Kubernetes & Containerization

Being a bit annoyed with the somewhat slow, fragile and dated way we were deploying our services, I decided to make sure all of our projects were possible to compile and run in a containerized way, and set up Azure CI pipelines to compile and push images to a private image registry in the cloud. This worked well for setting up a small POC running the entire system using docker-compose as well as in my private kubernetes cluster.

The company already had a kubernetes cluster running on-prem for testing, using ArgoCD for easy deploys. As I already had modified the projects to work well with environment-variable based configurations, all I had to do was write argo application manifests and Helm charts for getting everything deployed; luckily I already knew how to do that!

As a way to push this way of working forward, I used a PR generator in ArgoCD and set things up such that it was possible to label a PR with 'preview' and ArgoCD would pick the images up from our internal registry and run the entire system, while also having CI set up to add comments on the PR with instructions on how to reach the services and access control it thru ArgoCD's web-ui. 

I don't usually enjoy the ops-side of DevOps very much, but working with Kubernetes this way to provide ephemeral environments on the fly felt very rewarding and I might look in to working more with Kubernetes and especially ArgoCD in the future.

## CTF's, Puzzles & Reverse engineering

Outside of software engineering, one of my main interests is puzzle solving—whether through Capture the Flag (CTF) challenges or tackling tricky problems in general.

Over the years, playing a few MMOs led me to experiment with DLL (or shared library) injection and network traffic decoding, building custom HUDs and maps for various games. This hands-on experience became one of the most enjoyable ways I learned reverse engineering. When Ghidra was released around 2019, I was excited to dive into it, and it’s since become one of my favorite tools in this field.

Though I don’t participate in timed CTFs—since I’m not a fan of the time pressure—the puzzles I’ve enjoyed most were (surprisingly) created by the Swedish National Defence Radio Establishment (FRA). Occasionally, they require applicants to solve these as part of the application process for SIGINT roles. While I’m not interested in applying myself, it’s been rewarding to tackle these just for the challenge. The difficulty range from very easy (30m) to fairly complicated (8h) in my experience so they are are fun way to stay sharp.

### Advent of Code

One event I look forward to each year is Advent of Code, a December-long series of programming puzzles that offers both challenge and a fun way to experiment with new languages. It’s been a fantastic opportunity to stretch my skills and test-drive languages I don’t typically work with, all while solving clever puzzles. I have a lot of respect for the work put into creating these challenges—it’s clear they’re designed with care and creativity!

Looking ahead, I do wonder how AI will change the landscape, especially with the growing accessibility of tools like OpenAI. While it’s great to have new tech on our side, I hope that the spirit of problem-solving stays alive and well, without AI shortcuts taking away the fun.

## Open Source

While I did not start working with code full-time until around 2017, I had been coding both on side-projects and contributed to different open-source projects as far back as 2009.

In 2019 I started looking in to learning Rust. A language that had many features I'd previously enjoyed in languages like F# and OCaml whilst also getting rid of the need for garbage collection and runtimes.

Realizing that Rust was far more interesting and fun to work with than anything I've used before it, I spent huge amounts of time learning it and even started working on some developer tooling for myself which I ended up open-sourcing: [odd-box](./projects/odd-box.md).

Having started the project as a learning exercise it is not particularly well-written, especially in older parts of the code, but it works **very** well for what I need it to do, and is a fun project to work on.

Below are a few of the projects I’ve published on GitHub, most of which you can read more about in the projects section on this page as well.

- [odd-box](./projects/odd-box.md) : A reverse proxy and basic web server. Initially started as a learning exercise, it might not be the cleanest code, especially in the older sections, but it performs exceptionally well for my needs and has been a rewarding project to develop.

- [GELF Load Balancer](./projects/gelf-lb.md): An application-layer load balancer for GELF over UDP, allowing efficient log aggregation for high-traffic environments.

- [Language Server Protocol (LSP)](./projects/cardano.md): A custom implementation of LSP, including a WASM-compatible client, aimed at improving the developer experience for custom DSLs.

- [DSL Parser + CBOR Encoder/Decoder](./projects/cardano.md): A versatile parser with a CBOR encoding/decoding layer for efficient data interchange in constrained environments.

- [Cardano Blockchain Tools]((./projects/cardano.md)): Includes a blockchain indexer for smart contracts on the Cardano blockchain, grapql services for querying and realtime events, and a suite of macros to streamline data handling, with some contributions to Cardano documentation.


## Blockchain

As a way to broaden my knowledge about blockchain, smart-contracts and decentralized systems in general, I decided to dive in to the Cardano blockchain. It is a really interesting project and I contribute as best I can here. Cardano is built around Haskell, something I think is their biggest mistake, but it did at least help me learn Haskell fairly well, even tho I would not choose to build anything with it myself.

Anyway.. through Cardano I got to work a lot with Nix, eventually leading me to NixOS; which was a real gamechanger for me as I was used to vanilla Linux dists (Arch btw) where things had a tendency to easily break when not careful. 

A combination of Nix, Rust & Devbox (by jetify) became my go-to tools for just about everything after having worked within the Cardano ecosystem. 

I should mention here that Cardano was not the only blockchain system I explored, but also Bitcoin, Ethereum & Solana.. all of which had better developer experiences but felt like toys in comparison.

## Front-end development

I've used a long list of technologies for building websites over the years: php, vanilla js ASP.NET MVC (c#/html/js), jquery (js), angular (js), react (typescript), yew (rust), elm, fable+elmish (f#).. and probably some more that I do not remember. The easiest work work with was ELM and elmish: easily the simplest to use frameworks and fastest tooling I have ever used in the front-end world. Unfortunately React is more popular in the industry and thus the technology I've worked with the most professionally. 

## Programming & Scripting Languages

Learning new basics of a new language is not really that hard when you already know how to program in another. Even so, there is a **huge** difference in understanding how a language (and possibly its runtime) works under the hood and just knowing it's syntax. 

> Most dotnet developers for example do not know how the async/await keywords de-sugar or how the task worker implementations actually work, leading to making simple mistakes causing deadlocks and other performance issues. At least the synchronization context issues are (mostly) no more - so that makes it all-right to not know what a continuation is or how basic things like async state machines actually work, right? 😡

While I now am fairly fluent in more than a few languages - these are the ones I am the most experienced with:

- F#
- C#
- Rust
- TypeScript
- PowerShell

Another language that I actually enjoy both reading and writing, but haven't had the opportunity to use that much, is Python. 

My favorite language to work today with is **Rust**.


<br/>
<hr/>
<br/>

<br/>

<center>
olof@twnet.se - 2024
</center>