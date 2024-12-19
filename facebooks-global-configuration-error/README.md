<h1>
  <span class="headline">A+ Case Study</span>
  <span class="subhead">Facebook's Global Configuration Error</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to recall a real-world example of why the knowledge learned within the A+ course is essential to their future careers.

# The incident

On October 4, 2021, Facebook (now Meta) experienced a catastrophic six-hour outage that affected all its services, including WhatsApp, Instagram, and Oculus. What caused this massive shutdown? The root cause was an on-premise configuration change that accidentally disconnected all Facebook data centers globally from their network.

This seemingly minor maintenance error didn't just mean people couldn't refresh their Instagram feeds. Engineers couldn't even enter certain buildings because their electronic keycards stopped working.

By the time the error was resolved, billions of users worldwide had been affected, and Facebook lost an estimated $100 million in revenue.

What follows is a summary of the [details of the incident published by ThousandEyes](https://www.thousandeyes.com/blog/facebook-outage-analysis).

## The configuration change

The internet depends on a few critical systems. Two of those - DNS and BGP - were major players in this outage.

### Domain Name System (DNS)

Think of DNS like the contacts in your smartphone. You know a website by its name - facebook.com - but your device needs a numerical address to connect to it. DNS translates the friendly website name into an address, just like when you tap your friend's name in your contact list to call their number.

When DNS servers are unreachable, it's like having a phone with no contacts saved. You might technically have internet access, but unless you know the actual address of your destination, you won't be able to get there.

### Border Gateway Protocol (BGP)

Once a DNS server provides a numerical address, BGP is like a navigation app showing the best route to reach that address across a maze of digital roads. Without BGP routes, it's as if every street sign vanished. You know your destination exists, but you have no idea how to get there.

On the day of the incident, a routine maintenance change was made to the backbone network inside their data centers. This change withdrew the BGP routes that tell the global internet — and many of Facebook's own internal systems — where to find their DNS servers.

With the BGP "maps" gone, each of Facebook's data centers became an island, cut off from the global network. No one inside or outside Facebook knew how to reach its authoritative DNS servers. This meant there was no source of truth for translating facebook.com into an address.

## A cascade of failures

Facebook's DNS servers becoming unreachable led to a series of failures:

- With no DNS, user requests to access Facebook, Instagram, or WhatsApp couldn't find the right address.
- Authentication systems (the tools that confirm an employee's identity) failed. Employees and even automated systems within Facebook couldn't confirm who they were.
- Physical access control systems that rely on the network also went down. This meant doors wouldn't unlock, and on-site staff couldn't get into key areas.
- Even seemingly basic systems like conference room bookings and environmental monitoring inside data centers were impacted.

Engineers had to physically travel to data centers to fix the issues since remote management tools also depended on those now-broken networks. Hours of manual intervention were required to restore normal operations.

## Technical deep dive

1. Network infrastructure failure

   - BGP route advertisements were withdrawn.
   - DNS servers became unreachable.
   - Backbone connections dropped.
   - Internal tools stopped functioning.

2. Physical access issues

   - Electronic badge systems failed.
   - Conference room booking systems went down.
   - Environmental control monitoring was affected.
   - Data center access was restricted.

3. Cascading hardware problems

   - Server cooling systems lost remote monitoring.
   - Network diagnostic tools became unreachable.
   - Backup systems couldn't be accessed remotely.
   - Hardware management interfaces were inaccessible.

## What went wrong

Let's take a step back and identify the core issues at play in this incident and the lessons we can learn from those problems:

- It was too easy for a catastrophic configuration change to be made.
- Critical networking systems lacked redundancy.
- Multiple unrelated services depended on a single point of failure that was not fully understood or documented.
- Internal communication channels were disrupted, hindering recovery efforts.

> ❓ Is there anything that comes to mind as a way to remediate any of these issues?

## Why this matters

This case demonstrates crucial skills we'll learn while studying for the A+ exams. This case shows that a single, minor misconfiguration can topple massive infrastructures. In this course, you'll learn about the building blocks — hardware, networking, security, and change management — that can help prevent or mitigate these failures.

1. Hardware and infrastructure

   - Server systems
   - Network hardware
   - Physical security systems
   - Environmental controls
   - Service dependencies

2. Networking

   - DNS configuration
   - Network protocols
   - Routing and switching
   - Redundant systems
   - Network troubleshooting

3. Security

   - Access control systems
   - Authentication protocols
   - Physical security
   - Disaster recovery

4. Documentation and change management

   - Preventing communication breakdown
   - Configuration management
   - Change control procedures
   - System documentation
   - Recovery procedures

As you begin your A+ journey, remember that the fundamentals you learn - how hardware works, how networks communicate, how to secure systems, and how to manage changes - aren't just theories. They're the keys to keeping the digital world running smoothly.
