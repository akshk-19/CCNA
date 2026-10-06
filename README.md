# packet-tracer-labs

My networking notebook, in lab form. Every `.pkt` file I've built while studying for my **CCNA** lives here, along with the configs I typed, the mistakes I made, and what I learned from fixing them.

I'm Akshita, a B.Tech CSE student at Medi-Caps University, Indore. I started this repo because my Packet Tracer files were scattered across three folders and a USB drive, and I wanted one place where they'd actually make sense six months later.

> Built with Cisco Packet Tracer. Open any `.pkt` file in PT 8.x or newer.

---

## How this repo is organised

```
packet-tracer-labs/
├── 01-basics/            # cabling, IP addressing, first switch and router configs
├── 02-switching/         # VLANs, trunking, inter-VLAN routing, STP, EtherChannel
├── 03-routing/           # static routes, RIP, OSPF, default routes
├── 04-services/          # DHCP, DNS, NAT/PAT, NTP
├── 05-security/          # port security, ACLs, SSH, device hardening
├── 06-wireless-wan/      # WLAN basics, PPP, basic WAN links
├── 07-mini-projects/     # bigger multi-concept topologies
├── configs/              # raw running-configs as .txt, so you can read them on GitHub
├── screenshots/          # topology screenshots for each lab
└── notes/                # cheat sheets and "things I got wrong" write-ups
```

Each lab folder has the same shape:

```
lab-name/
├── lab-name.pkt          # the Packet Tracer file
├── topology.png          # what it looks like
├── config.txt            # device configs
└── README.md             # goal, addressing table, steps, verification
```

## Lab index

| # | Lab | Topics | Status |
|---|-----|--------|--------|
| 01 | Basic switch and router setup | hostname, banners, passwords, `show` commands | done |
| 02 | VLANs and trunking | VLAN creation, 802.1Q, access vs trunk ports | done |
| 03 | Inter-VLAN routing | router-on-a-stick, subinterfaces | done |
| 04 | Static and default routing | next-hop vs exit interface, floating statics | done |
| 05 | OSPF single area | neighbours, DR/BDR, router-id | done |
| 06 | DHCP and DNS | pools, exclusions, relay (`ip helper-address`) | done |
| 07 | NAT and PAT | static NAT, dynamic NAT, overload | done |
| 08 | ACLs | standard, extended, named | in progress |
| 09 | Port security and SSH | sticky MAC, violation modes, crypto key | in progress |
| 10 | Mini project | full campus-style network | planned |

*(Rename these rows to match your actual files; the table is just a map.)*

## Running a lab

1. Clone the repo
   ```bash
   git clone https://github.com/akshk-19/packet-tracer-labs.git
   ```
2. Open the `.pkt` file inside any lab folder with Cisco Packet Tracer.
3. Read that lab's `README.md` for the addressing table and goal.
4. Wait for the link lights to go green, then try the verification commands from the lab.

No Packet Tracer? Every lab's `config.txt` is plain text, so you can still read the configuration and paste it into GNS3, EVE-NG, or real gear.

## Commands I use constantly

```
show ip interface brief
show running-config
show vlan brief
show ip route
show ip ospf neighbor
show access-lists
ping / traceroute
```

## Habits that save me time

- Save the config (`copy running-config startup-config`) before closing a lab.
- Draw the topology and addressing table **before** touching a CLI.
- Fix the physical layer first. Nine times out of ten it's a wrong port or a shutdown interface.
- Keep a `notes/mistakes.md`. Reading your own mistakes is the fastest revision.

## Where this fits

Networking sits at the centre of what I'm learning: CCNA, a cybersecurity/IAM micro-internship with TATA Group, and a project of my own, the **Epidemic Alert Network**, which uses Packet Tracer topologies alongside C socket programming. These labs are the foundation under all of it.

## Roadmap

- [ ] Finish ACL and port-security labs
- [ ] Add IPv6 addressing and OSPFv3
- [ ] Add a first-hop redundancy lab (HSRP)
- [ ] Rebuild one lab in GNS3 to compare
- [ ] Write up each mini-project properly

## Contributing and feedback

This is a personal learning repo, but if you spot a wrong command or a better way to do something, open an issue or a PR. I'd genuinely like to know.

## Connect

- GitHub: [akshk-19](https://github.com/akshk-19)
- LinkedIn: [Akshita Kushwaha](https://linkedin.com/in/akshita-kushwaha-swe2006)

---

*Cisco and Packet Tracer are trademarks of Cisco Systems, Inc. This repo is for education and isn't affiliated with Cisco.*
