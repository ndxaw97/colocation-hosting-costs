# Colocation Hosting: What You're Actually Renting, Why the Second-Year Bill Moves, and Whether Your Hardware Belongs in a Data Centre

Five line items make up a colocation bill: rack space, power allocation, bandwidth and IP transit, cross-connects, and on-site engineer time. Power allocation is the one that decides both what fits in your cabinet and what you pay every month; the rack itself is mostly a container. The hardware sits outside that bill and comes first, at €2,000–5,000 for a decent server, plus tens of thousands more if you want redundancy across servers, switches and storage before a single customer has paid you anything.

Below: how the service actually works, where the money goes, how to read an SLA without being flattered by it, and where the threshold sits between colocation, dedicated servers and cloud.

> **Quick verdict.** You own servers with useful life left and your capacity needs are predictable: colocation deserves a proper quote. You run one low-power box: dedicated hosting is simpler and often cheaper. Spin Servers prices US colocation from your hardware, power and bandwidth requirements rather than publishing a rate card, so 👉 [send them your requirements and ask for an itemised quote](https://bit.ly/Spinservers).

## What colocation hosting actually rents

You own the servers. The provider owns the building, the power path, the cooling, the doors and the network your kit plugs into. That is the entire trade: your hardware keeps its full specification, and the facility becomes somebody else's operational problem.

The line between colocation and dedicated hosting is short. Renting a dedicated server gets you the machine and the space it lives in. Colocation gets you only the space. The usual picture is a boat you already own and a berth you pay for: the hull stays yours, the harbour supplies the moorings, the shore power and the security, and you can turn up and work on the boat whenever you need to.

Handing hardware over is a project rather than a signup. The sequence that experienced buyers follow:

1. Inventory what you have: form factor, power draw, port count, redundancy requirements.
2. Pick the location. Physical reach for your own visits, latency to your users, a second site for disaster recovery, carrier density, data residency.
3. Choose the space unit: a single 1U or 2U slot, part of a shared cabinet, a full 42U rack, or several racks inside a locked cage.
4. Agree power and connectivity: allocation per feed, A+B dual feeds, bandwidth commit, IP addressing, cross-connects or private circuits.
5. Ship the hardware, mount it, cable it.
6. Test before cutover: remote access, monitoring, backups, failover.
7. Run it remotely through IPMI, KVM over IP and your existing monitoring.
8. Use remote hands for the physical jobs nobody can do from a laptop.

What you can put in a rack goes well beyond web servers: storage arrays and backup appliances, switches, routers and firewalls, hypervisor hosts and private cloud, GPU and AI nodes, HPC kit, disaster recovery systems. GPU and HPC deployments need a facility with the power and cooling headroom to match, which is a question about the site rather than the contract.

## What has to appear on the quote before you compare anyone

Headline rack prices tell you almost nothing, because the number that matters is assembled from several charges. Ask for an itemised quote that separates every one of them, then compare.

| Line item | What to ask | Why it moves the bill |
| --- | --- | --- |
| Space | Priced per U, per quarter or half rack, per full 42U cabinet, or per cage? | Sets your floor cost and the shape of future growth |
| Power allocation | Amps per feed, A+B dual feeds, what happens when you exceed the allocation? | The real capacity ceiling, and usually the largest monthly variable |
| Bandwidth and IP transit | Commit versus burst, port speed, how many IPv4 and IPv6 addresses are included | Overage is where surprise invoices come from |
| Cross-connects | How many are included, what the second one costs, who terminates it | The year-two line item that never appears in headline pricing |
| Remote hands | Included hours per month, hourly rate beyond that, response window | You will use it, and the included allowance runs out |
| Price lock | Are power and bandwidth rates fixed for the term, and for how long? | A locked rate protects you from increases and traps you when prices fall |
| Contract | Minimum term, notice period, renewal terms | Exit cost belongs in the total |

Two of those deserve a second look. A provider that locks electricity and bandwidth into a multi-month commitment is not doing you a favour if those markets soften later; you keep paying the old rate. And the second cross-connect is the classic year-two surprise: cheap or included on day one, billed monthly once you add a second carrier for redundancy.

Retail colocation, the model most mid-sized buyers encounter, covers deployments from a partial rack up to a handful of full cabinets, with contracts built around cabinet space, power and associated services. Wholesale colocation runs on the same infrastructure with a different commercial structure and a much larger footprint.

## The real cost of colocation hosting

The facility fee is the visible part. The full picture is hardware, rent, power, bandwidth, spare parts, travel to site and your own engineers' time. Add them all before you compare the total against dedicated servers or cloud, because a colocation quote that looks cheap next to a managed server often stops looking cheap once spares and staff time are in the same column.

Hardware capex comes first and is not refundable if the plan changes. A single serviceable server runs €2,000–5,000 or more. Redundancy across multiple servers, switches and storage pushes that into the tens of thousands. Buying too much leaves capacity idle; buying too little means an unplanned purchase eighteen months early. The alternative, renting dedicated hardware, moves that risk to the provider for a monthly fee.

Then there is what colocation does not include. Nobody takes backups for you, so an off-site copy is your design problem. Hardware warranties and spare parts stay with you. Adding capacity means procurement, shipping, racking and a change window measured in weeks, not the minutes a cloud console offers. Swapping a failed component in person means travelling to the facility, booking access, having staff pull the machine, and accepting that the business goes offline for at least a few minutes while it happens.

Self-building is the other comparison, and it is not close on capital: construction, UPS, generators, industrial cooling, fire suppression and physical security are a large upfront commitment before the first server is powered.

## How to tell whether a data centre is any good

The SLA is where providers compete on adjectives. Read it as a contract with five specific checks:

- **What availability is actually promised**, in precise wording rather than a marketing percentage.
- **How service credits are calculated**, and whether they are capped. A credit capped at a fraction of one month's fee rarely covers the outage that triggered it.
- **How faults are classified**, since severity tiers decide who gets attention first.
- **Whether the response target covers acknowledgement or resolution.** These are not interchangeable, and the difference is the whole value of the clause.
- **Whether the certificate scope covers the site you are renting**, not the group's flagship facility in another country.

Physical security works in layers: perimeter control, security staff, CCTV, controlled doors, biometric or card access, visitor procedures, cabinet locks, segregated cages. Which of those apply at your specific site, and how they are operated on an ordinary Tuesday, is the part worth asking about. "Redundant" and "secure" as adjectives carry almost no information; the design and the operating practice behind them carry all of it.

Power allocation deserves the same scepticism. It is what determines whether your planned hardware physically fits, what happens when you add a GPU node, and whether the provider can grow with you or asks you to move racks.

For regulated sectors, the practical benefit is narrower and more defensible than the marketing suggests: you can point to a known physical location and describe the controls around it. Finance, healthcare and public sector buyers mostly need that provability, not a vague claim that rules require data to sit on site.

## Cross-connects, peering and cloud on-ramps in plain terms

| Term | What it means for you |
| --- | --- |
| Bandwidth | How much data a connection carries over a period; usually sold as a monthly commit |
| IP transit | The route from your network out to the public internet |
| Cross-connect | A dedicated physical link from your rack to another network, carrier, customer or service in the same building |
| Peering | Two networks exchanging traffic directly, often through an internet exchange |
| BGP | The protocol that decides how traffic is routed between networks; multi-homed BGP across two or more upstreams buys redundancy and better path selection |
| Cloud on-ramp | Private or dedicated connectivity from the facility to a public cloud platform |

The practical value of a carrier-neutral facility is choice: you are not stuck with one upstream, and you can add a second provider without moving hardware. Multi-homed BGP turns that choice into resilience, and a cloud on-ramp turns it into a private path to workloads you keep in public cloud. Neither is free, and both require cross-connects, which is why the cross-connect count on the quote matters more than the rack price.

## Who should colocate, and who should not

Colocation fits when you already own servers with useful life left, when the office server room was designed for a smaller load than it now carries, when you need stronger physical security or clearer compliance evidence, when you need a second site for disaster recovery, when you are expanding into another region without buying a building, or when you need several carriers and a private route into public cloud. Predictable capacity requirements make the whole calculation work; so does a workload with specific hardware needs, such as GPU or AI nodes, dense storage, or custom network topology that no standard rented server offers.

It fits badly in three situations. A single low-power server is simpler and often less expensive on dedicated hosting. Highly unpredictable load belongs on a platform that can scale in minutes. And if what you actually want is a fully managed platform where somebody else handles the operating system, patching and backups, colocation adds work rather than removing it. Managed colocation exists and costs extra, but it is a separate purchase from the facility service.

There is a scale threshold, and older guides tend to undersell it. Colocation starts paying off when you are running a fleet rather than a server; below that, the per-machine cost of renting dedicated hardware usually wins, and above it the long-run saving per server can run to hundreds of euros a month. Be honest about which side of that line you are on.

## Where Spin Servers fits

Spin Servers sells managed colocation in the USA, built around three components: rack space, connectivity, and on-site support for your hardware. Pricing is quote-based. You describe your hardware, power draw and bandwidth requirements, and the team comes back with a package, which means there is no published rate card to compare before that conversation happens.

One constraint is worth knowing before you shortlist them. The standard colocation service is designed for servers bought from The Server Store, the company's own hardware business, so that spares can be held on site and support stays familiar with the kit. If your servers came from somewhere else, that is a sales conversation rather than a self-service order. For a buyer replacing ageing hardware anyway, it is a convenience; for a buyer with an existing estate from three different vendors, it is a question to raise early.

Remote management is handled through a client portal with operating system installation, power controls and remote console access. You can also request IPv6, private networking between your own servers, or announcement of your own IP address space, which matters if you are keeping a provider-independent addressing plan. 👉 [Check the current colocation service and what the quote covers](https://bit.ly/Spinservers).

What the public pages do not state: rates per U or per cabinet, power pricing, locations, SLA figures, contract terms. Ask for those in writing, in the itemised format above.

## Before you sign

Confirm the SLA wording, the power allocation per feed, the carrier list, the certificate scope for your actual site, the remote hands terms, and a quote that separates every charge including the second cross-connect. Document your own side too: which cable goes where, IP assignments, credentials, network diagram. If one administrator is the only person who knows the topology, the facility is not your weakest link.

The decision rule is short. Existing hardware plus predictable demand: colocate, and get three itemised quotes. One low-power server: rent dedicated. Demand that swings hard in either direction: public cloud, with colocation reserved for the steady base load. 👉 [Start a colocation quote with Spin Servers](https://bit.ly/Spinservers) once you can put real numbers on your hardware, power and bandwidth.
