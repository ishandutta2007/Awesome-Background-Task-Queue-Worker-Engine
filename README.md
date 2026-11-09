# Awesome-Background-Task-Queue-Worker-Engine

I can't create the file, commit, or push—I have no filesystem, no shell, and no Git credentials. Everything I produce is text. You will need to save and push it yourself.

I also have to flag what the search results actually support, because **"Zoho Worker" and "Celery Cloud" do not exist as products**, and **several entries are libraries, not SaaS platforms**.

## The data problems

**"Zoho Worker" does not exist as a background task queue.** Zoho's job scheduling is a feature of **Zoho Catalyst** (Job Scheduling for Job Functions, Webhooks, Circuits, and AppSail) . There is no standalone "Zoho Worker" product. **Remove it or reframe as "Zoho Catalyst Job Scheduling (feature)."**

**"Celery Cloud" does not exist.** Celery is a **BSD-3-Clause open-source library** you install and run on your own infrastructure—there is no hosted service, no account, no metering, and no billing relationship . Any "Celery Cloud" pricing you have seen is fabricated. **List Celery in the open-source section only.**

**Sidekiq Enterprise is $269/month starting**; Pro is **$99/month** . The Appliance license (for distribution to customers) is **$14,995/year for Pro** and **$39,995/year for Enterprise** .

**BullMQ Pro Standard is $116/month billed annually** (or $139 monthly); Embedded is **$995/month**; Enterprise is custom . The commercial license is per-organization, not per-deployment .

## What the search results actually contain

**SaaS pricing (verified):**

| Platform | Entry pricing | Metering |
|---|---|---|
| **Temporal Cloud** | **$50 per million actions**; $150 free credits for 90 days; no base fee; storage $0.042/GBhr active, $0.00105/GBhr retained  | Per action |
| **Trigger.dev** | **Free $0** (20 concurrent runs, $5 compute credits); **Hobby $10/mo** (50 concurrent); **Pro $50/mo** (200 concurrent, +$10/50)  | Per second compute + per run invocation |
| **Inngest** | **Free $0** (50K executions, 5 seats); **Pro $99/mo** (1M executions, 15 seats); **Business $499/mo** (10M executions)  | Per execution |
| **QStash (Upstash)** | **Free $0** (1,000 messages/day); **Pay-as-you-go $1 per 100K messages**; **Fixed 1M $180/mo**; **Fixed 10M $420/mo**  | Per message (retries free) |
| **Sidekiq Enterprise** | **$269/month** starting  | Per license |
| **BullMQ Pro** | **$116/month** annual (Standard)  | Per organization |
| **IronWorker** | **$4.99/month** starting  | Per month |
| **AWS SQS** | **Pay-per-request**; no minimum fee  | Per request (64KB chunks) |

**Open-source projects (verified):**

| Project | License | What it actually does |
|---|---|---|
| **Celery** | BSD-3-Clause | Distributed task queue library; no hosted service, no commercial tiers  |
| **Sidekiq (OSS)** | Open source | Ruby background job framework; Pro/Enterprise are commercial add-ons  |
| **BullMQ (OSS)** | Open source | Node.js job queue; Pro is commercial add-on  |
| **FastQ** | Open source (C) | Redis-backed job queue; claims 10x throughput and 90% less memory than BullMQ/Sidekiq; Pro adds cron, rate limiting, DAG workflows, metrics  |

## What I recommend

**Remove "Zoho Worker" and "Celery Cloud"**—neither exists. Reframe Zoho as a Catalyst feature, and list Celery as open source only.

**Split into two honest categories:**

**1. SaaS Background Job Platforms** (proprietary):
- **Temporal Cloud** — $50/M actions, no base fee 
- **Trigger.dev** — Free to Pro $50/mo 
- **Inngest** — Free to Business $499/mo 
- **QStash** — Free to Fixed 10M $420/mo 
- **AWS SQS** — pay-per-request 
- **Sidekiq Enterprise** — $269/mo 
- **BullMQ Pro** — $116/mo annual 
- **IronWorker** — $4.99/mo 

**2. Open-Source Job Queues:**
- **Celery** — BSD-3-Clause, library only 
- **Sidekiq OSS** — Ruby, Pro/Enterprise commercial 
- **BullMQ OSS** — Node.js, Pro commercial 
- **FastQ** — C/Redis, claims 10x throughput 

**Flag the metering differences explicitly:** per-action (Temporal) , per-execution (Inngest) , per-message (QStash) , per-request (SQS) , and per-compute-second (Trigger.dev)  produce incomparable costs at the same job volume.

If you paste your current `README.md` and confirm you want this framing, I will produce the complete file as text for you to save. I will not list Zoho Worker or Celery Cloud as products, fabricate pricing, or present libraries as SaaS platforms.
