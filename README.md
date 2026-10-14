*This project has been created as part of the 42 curriculum by mlorenz.*

# NetPractice

## Description

NetPractice is a practical introduction to the basics of computer networking.
The goal is to make a series of small, simulated networks function correctly by
configuring the available devices. Across 10 levels of increasing difficulty,
the network diagrams start out broken and must be repaired by adjusting IP
addresses, subnet masks, gateways and routes so that all hosts can communicate
as required by the objectives shown for each level.

The project focuses on understanding rather than on large-scale implementation:
there is no server to deploy, only configurations to reason about. The target
is a solid, hands-on understanding of how IP addressing, subnetting and routing
work together to move traffic between devices.

## Instructions

### Requirements

- A Unix-like system (Linux or macOS)
- `python3` (used to serve the web interface)
- A modern web browser

### Running the training interface

The training interface is a set of static web pages that must be served by a
local web server.

1. Enter the `net_practice/` directory that came with the project.
2. Run the provided script:

   ```bash
   ./run.sh
   ```

   The script starts a local web server on a free port and opens your default
   browser at `http://localhost:<port>`.

3. If `run.sh` does not work, start the server manually and open the URL
   yourself:

   ```bash
   python3 -m http.server 49242
   ```

   Then navigate to `http://localhost:49242` (any free port may be used).

4. In the interface, enter your **login** in the field provided so that your
   personal configuration is used.

### Solving and exporting a level

- For each level, adjust the unshaded fields until the objectives at the top of
  the window are met.
- Use **[Check again]** to test the current configuration.
- Use the log area at the bottom of the page to understand why a configuration
  is rejected (for example a missing gateway or an invalid IP address).
- When a level is solved, a button to proceed to the next level appears.
- Use **[Get my config]** to download the configuration for the current level.
  Export the configuration *before* moving on to the next level.

### Submission details

- The assignment is submitted as a Git repository.
- The repository root must contain 10 exported configuration files, one per level
  (`level1.json` … `level10.json`).
- The login used in the training interface must be the same one used for the
  submission.

## Resources

- [Cisco – IP Addressing and Subnetting for New Users](https://www.cisco.com/c/en/us/support/docs/ip/routing-information-protocol-rip/13788-3.html)
- [Cloudflare Learning Center – What is a subnet mask?](https://www.cloudflare.com/learning/network-layer/what-is-a-subnet/)
- [Cloudflare Learning Center – What is the OSI model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)

**Concepts studied:** TCP/IP addressing, subnet masks (and CIDR notation),
default gateways, routers and switches, the OSI layer model, and the way these
pieces combine so that hosts on the same or different networks can communicate.

**AI usage:** AI assistants were used for understanding networking concepts
such as subnet masks, default gateways and routing, for debugging incorrect
configurations, and for drafting this README. The level configurations and
their subnet calculations were worked out and verified manually.
