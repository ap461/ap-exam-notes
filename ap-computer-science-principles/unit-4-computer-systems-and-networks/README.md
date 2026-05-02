# AP Computer Science Principles Unit 4: Computer Systems and Networks

> How computers connect, communicate, and share data through networks and the internet. This unit covers the difference between the internet and the World Wide Web, IP addresses, packets, routing, TCP/IP, fault tolerance, and parallel and distributed computing.

**Practice all Unit 4 questions, flashcards, and Create Task prep →** [apscore5.com/ap-computer-science-principles/unit-4-computer-systems-and-networks](https://www.apscore5.com/ap-computer-science-principles/unit-4-computer-systems-and-networks)

---

## What is Unit 4 about?

Unit 4 of AP Computer Science Principles studies how computers connect to each other and how the internet works. You'll learn the difference between the internet (a network of networks) and the World Wide Web (a service that runs on the internet), how data is broken into packets and routed across networks, what TCP/IP and HTTP do, why the internet is fault-tolerant, and how parallel and distributed computing enable modern systems. This unit makes up about 11–15% of the exam and shows up frequently in questions about how data travels, why networks are reliable, and how cloud computing scales.

---

## Microtopics in this unit

*Microtopic pages are being added. Check back soon, or visit the [full Unit 4 course on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-4-computer-systems-and-networks) for complete content.*

---

## Key concepts to master

### What is a network?

A **computer network** is two or more computers connected so they can share data and resources.

| Type | Description | Examples |
|---|---|---|
| **LAN (Local Area Network)** | Small geographic area | Home Wi-Fi, school network, office |
| **WAN (Wide Area Network)** | Large geographic area | The internet itself |
| **Wireless network** | Connects without cables | Wi-Fi, cellular, Bluetooth |
| **Wired network** | Connects with cables | Ethernet |

---

## The internet vs the World Wide Web

These two terms are often confused — they are **not** the same thing.

| Internet | World Wide Web |
|---|---|
| The global **network of networks** | A **service** that runs on the internet |
| Started in 1969 (ARPANET) | Started in 1989 (Tim Berners-Lee) |
| Carries all kinds of data (email, video, web, gaming) | Specifically about webpages and websites |
| Uses many protocols (TCP/IP, FTP, SMTP, etc.) | Uses HTTP/HTTPS |

**Memory tip:** the internet is the **highway**; the web is one type of **car** that drives on it.

---

## How data travels: packets and routing

When you send data online, it doesn't travel as one big chunk. It's broken into smaller pieces.

### Packets

| Concept | What it means |
|---|---|
| **Packet** | A small piece of data with metadata (source, destination, sequence number) |
| **Why packets?** | Smaller pieces are faster to send, easier to fix when corrupted, and can take different paths |
| **Reassembly** | Packets are reassembled in order at the destination |
| **Out of order** | Packets may arrive in any order; sequence numbers help reassemble correctly |

### Routing

The path a packet takes from source to destination.

| Concept | What it means |
|---|---|
| **Router** | A device that forwards packets toward their destination |
| **Path** | The series of routers a packet passes through |
| **Dynamic routing** | Each packet may take a different path based on traffic and availability |

**Example:** sending an email — it gets broken into packets, each packet may take a different path across the world, and they all reassemble in order on the recipient's mail server.

---

## IP addresses

Every device on the internet has an **IP (Internet Protocol) address** — a unique identifier.

| Version | Format | Total addresses | Why it exists |
|---|---|---|---|
| **IPv4** | `192.168.1.1` (4 numbers, each 0–255) | ~4.3 billion | Original; running out |
| **IPv6** | `2001:0db8:85a3::8a2e:0370:7334` (8 groups of 4 hex digits) | ~340 undecillion | Created to solve IPv4 shortage |

### Why we need IPv6

IPv4 has only 4.3 billion addresses — far fewer than the number of devices in use today (phones, laptops, smart TVs, IoT). IPv6 has so many addresses we'll never run out.

---

## Domain Name System (DNS)

DNS is the **internet's phonebook** — it translates human-readable domain names into IP addresses.

**Example:** when you type `apscore5.com`, DNS looks up the IP address (e.g., `76.76.21.21`) so your browser can connect.

| Concept | What it does |
|---|---|
| **DNS server** | Stores domain → IP mappings |
| **Domain name** | A human-readable address (apscore5.com) |
| **IP address** | The numerical address the computer needs |
| **DNS query** | The lookup process |

---

## Protocols

A **protocol** is a set of rules that governs how data is exchanged.

### Common internet protocols

| Protocol | What it does |
|---|---|
| **TCP (Transmission Control Protocol)** | Breaks data into packets, ensures all packets arrive, reassembles them |
| **IP (Internet Protocol)** | Handles addressing and routing of packets |
| **HTTP (HyperText Transfer Protocol)** | The protocol of the web — for sending webpages |
| **HTTPS** | Secure version of HTTP — encrypts data |
| **FTP (File Transfer Protocol)** | For transferring files |
| **SMTP** | For sending email |

### Why protocols matter

- They are **open standards** — anyone can use them without permission
- They allow different devices and operating systems to communicate
- They are the foundation of **interoperability** — Macs, PCs, phones, and servers can all talk to each other

---

## TCP/IP — the foundation of the internet

| Layer | What it does |
|---|---|
| **TCP** | Splits data into packets and verifies all arrive correctly |
| **IP** | Addresses and routes the packets |

**Together, TCP/IP makes reliable data transmission possible across the messy, unpredictable internet.**

---

## Bandwidth and latency

| Concept | What it means | Example |
|---|---|---|
| **Bandwidth** | How much data can be sent per unit time | Gigabits per second (Gbps) |
| **Latency** | How long a single packet takes to arrive | Milliseconds (ms) — "ping" |
| **Throughput** | Actual data transfer rate (lower than bandwidth in practice) | |

### High bandwidth ≠ low latency

A satellite connection can have high bandwidth (lots of data) but high latency (slow round trip). A local network can have low bandwidth but very low latency.

**Example:** filling a swimming pool with a fire hose vs a garden hose.
- **Bandwidth** = how wide the hose is.
- **Latency** = how long after turning it on water starts coming out.

---

## Fault tolerance

The internet is **fault-tolerant** — it keeps working even when parts of it fail.

### How fault tolerance is achieved

| Method | What it does |
|---|---|
| **Redundancy** | Multiple paths between any two points |
| **Dynamic routing** | Packets reroute around broken connections |
| **Decentralization** | No single point of failure (no single "internet headquarters") |
| **Error detection** | Detect lost or corrupted packets |
| **Retransmission** | Resend lost packets |

**Why it matters:** even if a server, cable, or entire region goes offline, the rest of the internet continues to function. This was a key design goal of the original ARPANET.

---

## Scalability

The internet is **scalable** — it can grow without breaking.

### How the internet scales

- New networks can be added without changing existing ones
- Open protocols (TCP/IP) work the same regardless of network size
- Hierarchical structure (DNS, IP addresses) allows efficient routing
- Distributed control — no single bottleneck

---

## Parallel and distributed computing

### Sequential computing

Steps are performed one after another. Easy to understand but limited in speed.

### Parallel computing

Multiple steps performed at the same time, usually on the **same computer** with multiple processors.

**Example:** a single laptop with 8 CPU cores running 8 tasks simultaneously.

### Distributed computing

Multiple computers work together across a network on parts of a problem.

**Example:** Google searches use thousands of servers across the world processing queries in parallel.

### Speedup

| Concept | What it means |
|---|---|
| **Speedup** | How much faster a parallel solution is vs sequential |
| **Speedup formula** | Sequential time ÷ parallel time |
| **Limit on speedup** | Some parts of a task can't be parallelized — these create bottlenecks |

### Real-world examples of distributed computing

- Cloud services (AWS, Google Cloud, Azure)
- Search engines (Google, Bing)
- Streaming platforms (Netflix, YouTube)
- Cryptocurrency mining
- Scientific projects (SETI@home, Folding@home)

---

## Cloud computing

Storing data and running programs on **remote servers** instead of your own computer.

| Benefit | Why it matters |
|---|---|
| **Scalability** | Add more capacity without buying hardware |
| **Accessibility** | Access from anywhere with internet |
| **Reliability** | Cloud providers run multiple backups |
| **Cost** | Pay only for what you use |

| Drawback | Why it matters |
|---|---|
| **Privacy** | Your data lives on someone else's servers |
| **Internet dependency** | No internet = no access |
| **Security risks** | Data breaches at cloud providers affect millions |

---

## Common AP exam mistakes

- **Confusing the internet and the World Wide Web** — internet is the network; web is a service on it
- **Thinking packets always take the same path** — they often take different routes
- **Saying packets always arrive in order** — they don't; sequence numbers reassemble them
- **Forgetting why redundancy is important** — it's the basis of fault tolerance
- **Confusing bandwidth with latency** — bandwidth is volume; latency is delay
- **Calling cloud computing "magic"** — it's just remote servers connected via networks
- **Saying parallel computing is always faster** — only when tasks can be split independently
- **Confusing TCP and IP** — TCP handles packet integrity; IP handles addressing/routing

---

## How Unit 4 connects to other units

- **Unit 1 (Creative Development)** — programs increasingly run across networks
- **Unit 2 (Data)** — data is what travels through networks; metadata helps route it
- **Unit 3 (Algorithms)** — routing algorithms decide packet paths
- **Unit 5 (Impact of Computing)** — networks raise privacy, security, and access issues

---

## Top exam topics to prepare

1. **Internet vs World Wide Web** — clearly explain the difference
2. **Packets and routing** — explain how data travels
3. **IP addresses (IPv4 vs IPv6)** — explain why IPv6 was needed
4. **DNS** — explain how domain names get translated to IP addresses
5. **Fault tolerance and redundancy** — explain why the internet keeps working
6. **Bandwidth vs latency** — distinguish and give examples
7. **Parallel vs distributed computing** — explain when each is used
8. **Speedup** — calculate or interpret speedup in a parallel scenario
9. **Cloud computing** — explain benefits and trade-offs

---

## Frequently asked

**How much of the AP exam is Unit 4?**
Unit 4 makes up about 11–15% of multiple-choice questions. Networking concepts (packets, routing, fault tolerance) and the differences between sequential, parallel, and distributed computing are the most-tested topics.

**What's the difference between the internet and the World Wide Web?**
The internet is the global network of computers — the physical and protocol-based infrastructure that lets devices communicate. The World Wide Web is just one **service** that runs on the internet — specifically, the system of webpages and websites accessed via HTTP. Email, video calls, gaming, and file sharing are all internet services that aren't the web.

**Why does the internet break data into packets?**
Breaking data into packets makes the internet faster, more reliable, and more efficient. Smaller pieces can be sent faster, can take different paths to avoid traffic, can be retransmitted individually if lost, and don't tie up the network. If everything was sent as one giant chunk and a single error happened, you'd have to resend everything.

**Why is the internet considered fault-tolerant?**
The internet was designed with **redundancy** — multiple paths exist between any two points. If one connection fails, packets automatically reroute through other paths. There's no single "internet headquarters" — the system is decentralized. This is why an outage in one country or region doesn't take down the whole internet.

**What's the difference between bandwidth and latency?**
Bandwidth is how much data can be transmitted per second (the size of the pipe). Latency is how long a single packet takes to travel (the delay). A satellite connection can have huge bandwidth but high latency because the signal has to travel up to space and back. A LAN cable has low latency because the distance is tiny.

**Why did we need IPv6?**
IPv4 only supports about 4.3 billion unique addresses. With phones, laptops, smart TVs, smart appliances, and IoT devices, we ran out of IPv4 addresses years ago. IPv6 supports roughly 340 undecillion addresses (a number with 36 zeros) — essentially unlimited for the foreseeable future.

**What's the difference between parallel and distributed computing?**
Parallel computing runs multiple operations at the same time on the **same computer** (with multiple cores or processors). Distributed computing splits work across **multiple computers** connected by a network. A laptop with 8 cores doing 8 tasks at once = parallel. A Google search that uses servers around the world = distributed.

**What is speedup?**
Speedup is how much faster a parallel or distributed solution is compared to a sequential one. If a sequential algorithm takes 100 seconds and the parallel version takes 25 seconds, the speedup is 4×. Speedup has limits — some parts of a task can't be split up, which creates bottlenecks. This is why doubling the processors doesn't always cut the time in half.

**Are domain names the same as IP addresses?**
No. Domain names (like `apscore5.com`) are human-readable, while IP addresses (like `76.76.21.21`) are what computers use to actually route traffic. DNS is the system that translates between them. Without DNS, you'd have to remember IP addresses for every website you visit.

---

## Practice this unit

- [Full Unit 4 guide on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-4-computer-systems-and-networks) — 50+ questions, flashcards, Create Task prep
- [Browse all AP CSP units](../)
- [AP CSP course overview](../../ap-computer-science-principles/)

---

*Notes synced from [apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-4-computer-systems-and-networks). Last updated: May 2026.*
