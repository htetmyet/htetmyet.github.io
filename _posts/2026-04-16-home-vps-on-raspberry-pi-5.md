# One Raspberry Pi, Many Small Wins

![](../images/pi5-home-vps-setup.svg)

I didn’t plan to turn a Raspberry Pi into a mini hosting business.
I just wanted to stop burning money on cloud bills for small apps.

So I started with one Raspberry Pi 5 (8 GB RAM) on my desk, an SSD, and a weekend mindset of: "let me see how far this can go."

It went farther than I expected.

Today this same home VPS runs:

- my personal web apps
- lightweight AI/ML apps
- a home media server
- CRM and sales tools for several SME clients

And that stack now gives me subscription side income every month.

## The Moment I Decided to Build It

Every time I launched a tiny product, I repeated the same pattern:

- spin up cloud resources
- pay for convenience
- underuse most of it

I wanted a setup where I could own the system and keep monthly cost predictable.
Not "free," just predictable.

That is why I built a personal VPS at home and treated it seriously from day one.

## My Hardware (Simple but Reliable)

- Raspberry Pi 5
- 8 GB RAM
- SSD over USB 3
- broadband connection
- UPS for power stability
- active cooling case

Nothing exotic.
The real difference is operational discipline, not expensive hardware.

## What I Actually Run on It

### Personal Web Apps

These are my experiments and utility products: small dashboards, internal tools, landing pages, and client prototypes.

I keep every app isolated in containers, with separate env vars and logs.
If one app breaks, the others keep running.

### AI/ML Apps

![](../images/pi5-home-vps-architecture.svg)

I do not train giant models here.
This box is for practical AI work:

- document parsing and workflow automation
- embeddings + semantic search for small knowledge bases
- lightweight local model inference
- scheduled jobs and integrations

The Pi is perfect when I optimize for useful outcomes, not benchmark scores.

### Home Media Server

This started as a personal convenience project.
Now it is my testbed for monitoring, access control, and backup routines before I apply the same ops habits to client apps.

### SME CRM + Sales Systems

This became the most interesting part.

A few SME owners asked for affordable CRM and sales tracking.
They didn’t need enterprise complexity.
They needed clarity:

- customer records in one place
- deal stage visibility
- invoice and follow-up tracking
- simple reports they can trust

That problem fit this setup very well.

## How I Handle Multi-Client Hosting

I keep things boring and structured:

- one reverse proxy as the front door
- separate containers per project/client
- isolated data boundaries (DB/schema level)
- HTTPS for all domains
- daily backups with retention

It is not flashy architecture.
It is architecture I can maintain at 2 AM.

## Running on 8 GB RAM: My Rules

I survive on constraints.

- avoid heavy frameworks where simple stacks work
- set memory limits for containers
- offload heavy/background work to queues
- cache aggressively
- rotate logs and clean storage on schedule
- watch resource usage before it becomes an incident

When hardware is limited, planning is performance.

## Reliability and Security (Non-Negotiable)

If people pay subscriptions, I can’t run this like a hobby.

Reliability baseline:

- uptime checks and alerts
- auto-restart policies
- encrypted backups
- off-device backup copies

Security baseline:

- SSH keys only
- strict firewall rules
- brute-force protection
- automatic patching
- least-privilege access
- no secrets in git

These are small habits that prevent expensive mistakes.

## Side Income: What I Learned

![](../images/pi5-home-vps-side-income.svg)

I package services as monthly subscriptions:

- hosting
- maintenance
- backups
- minor support
- upgrade path when they grow

The lesson: clients don’t care about the Raspberry Pi model.
They care that their business system is up, safe, and understandable.

I’m not selling a server.
I’m selling continuity.

## Honest Limits

This setup is not for:

- high-concurrency consumer platforms
- compute-heavy AI training
- strict enterprise compliance workloads

But for personal products and focused SME operational software, it is more than enough.

## Final Thought

This project started with curiosity and cost control.
Now it is part lab, part production, part side business.

One Raspberry Pi 5 (8 GB).
A lot of careful decisions.
Real value for real users.
