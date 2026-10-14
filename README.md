# 🌐 Static Routing with Kathará — Computer Networks

<p>
  <img alt="Kathará" src="https://img.shields.io/badge/Kathar%C3%A1-network%20emulation-1f2328?style=flat-square">
  <img alt="Course" src="https://img.shields.io/badge/Course-Computer%20Networks%20(RC)-1f2328?style=flat-square">
  <img alt="Year" src="https://img.shields.io/badge/2025%2F26-3rd%20year%2C%201st%20semester-1f2328?style=flat-square">
</p>

Assignment 3 of *Redes de Computadores* (Computer Networks), Computer Science degree at **NOVA School of Science and Technology (FCT NOVA)**.

## About

A network of **4 routers and 6 hosts** across several subnets, emulated with [Kathará](https://www.kathara.org/) (each device is a container). Every interface is addressed by hand and all routing is **static**, following given **routing policies** — for example, traffic between two networks must take one specific path through the routers, while the reverse direction may take another.

- `lab.conf` describes the devices and which network each interface is connected to.
- Each `*.startup` file configures a device: IP addresses, enabling IP forwarding on routers, and static routes (`ip route add … via …`).
- `shared/` has the packet captures (`.pcap`) taken on the routers to show the traffic following the required paths.

## Running it

Needs [Kathará](https://www.kathara.org/) and Docker.

```bash
kathara lstart        # start the lab
kathara connect h1    # open a shell on host h1, e.g. to ping or traceroute
kathara lclean        # stop the lab
```

Open the captures in `shared/` with Wireshark to inspect the packets.

## What I learned

- IP addressing and subnetting (including /30 point-to-point links)
- Static routing tables and how to enforce asymmetric routing policies
- Verifying paths with traceroute and packet captures

## Authors

- **Miguel Carmo** ([@MCCProgrammer](https://github.com/MCCProgrammer))
- **Tomás Ramos Alves** ([@Alvesss04](https://github.com/Alvesss04))

---

<sub>The assignment statement is not included in this repository, as it belongs to the course's teaching staff. This is a student project shared for portfolio purposes.</sub>
