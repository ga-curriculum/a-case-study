<h1>
  <span class="headline">A+ Case Study</span>
  <span class="subhead">Case Study: Facebook's Global Configuration Error</span>
</h1>

**Learning objective:** By the end of this lesson, students will have a real world example of why the knowledge learned within the A+ course is important.

# The Incident

On October 4, 2021, Facebook (now Meta) experienced a catastrophic six-hour outage that affected all its services including WhatsApp, Instagram, and Oculus. The root cause was an on-premise configuration change that accidentally disconnected all Facebook data centers globally from their network. This seemingly minor maintenance task cascaded into a $100 million revenue loss and affected billions of users worldwide.

## What Went Wrong

- A routine Border Gateway Protocol (BGP) configuration change accidentally withdrew routes to Facebook's DNS servers
- On-premise DNS servers became unreachable
- Authentication systems failed
- Physical access control systems were affected
- Engineers couldn't access buildings or servers remotely
- Even physical security badges stopped working

## Technical Deep Dive

1. Network Infrastructure Failure

- BGP route advertisements were withdrawn
- DNS servers became unreachable
- Backbone connections dropped
- Internal tools stopped functioning

2. Physical Access Issues

- Electronic badge systems failed
- Conference room booking systems went down
- Environmental control monitoring was affected
- Data center access was restricted

3. Cascading Hardware Problems

- Server cooling systems lost remote monitoring
- Network diagnostic tools became unreachable
- Backup systems couldn't be accessed remotely
- Hardware management interfaces were inaccessible

# Why This Matters

This case demonstrates crucial skills that we'll learn while studying for the A+ exam. For example:

1. Hardware and Infrastructure

- Server systems
- Network hardware
- Physical security systems
- Environmental controls

2. Networking

- DNS configuration
- Network protocols
- Routing and switching
- Network troubleshooting

3. Security

- Access control systems
- Authentication protocols
- Physical security
- Disaster recovery

4. Documentation and Change Management

- Configuration management
- Change control procedures
- System documentation
- Recovery procedures