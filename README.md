# NetPractice

*This project has been created as part of the 42 curriculum by.*

## Description

NetPractice is a practical training project designed to help students understand and master the fundamentals of computer networking. The project consists of 10 progressive levels that simulate real-world network configuration scenarios.

**Goal**: Configure small-scale networks by correctly assigning IP addresses, subnet masks, and routing information to ensure proper communication between devices. Each level presents a network topology with missing or incorrect configurations that must be fixed to allow all devices to communicate successfully.

**Overview**: Through hands-on practice, students learn to:
- Understand TCP/IP addressing and how devices communicate
- Calculate and apply subnet masks correctly
- Configure routers to connect different networks
- Set up default gateways for proper routing
- Troubleshoot common network configuration errors

The project uses an interactive web interface where configurations can be tested in real-time, providing immediate feedback on whether the network is properly configured.

## Instructions

### Running the Training Interface

1. **Launch the interface**:
   - Open the `index.html` file in your web browser
   - Alternatively, if provided with a specific URL, navigate to the NetPractice training platform

2. **Navigate through levels**:
   - Start with Level 1 (easiest) and progress to Level 10 (most complex)
   - Each level presents a network diagram with input fields for configuration

3. **Configure the network**:
   - Fill in the empty fields with appropriate values:
     - IP addresses
     - Subnet masks (in CIDR notation or dotted decimal)
     - Default gateways
     - Routing table entries
   - Click "Check again" to verify your `configuration
   - The interface will indicate success (green) or errors (red)

4. **Export configurations**:
   - Once a level is successfully completed, click the "Get my config" button
   - This downloads a JSON file (e.g., `level1.json`, `level2.json`, etc.)
   - Save this file to your repository root

### Submission Requirements

Your Git repository must contain:
- **10 configuration files** at the root: `level1.json` through `level10.json`
- **This README.md** file
- All files must be properly named and contain valid configurations that pass their respective levels

**Note**: The configuration files are the proof that you completed each level successfully. Ensure all 10 files are present before submission.

## Resources

### Networking Concepts Studied

This project covers fundamental networking concepts essential for understanding modern computer networks:

- **TCP/IP Addressing**: Understanding IPv4 addresses, their structure (32-bit format), and how they identify devices on a network
- **Subnet Mask**: Learning to divide networks into subnets, calculating network and host portions, and understanding CIDR notation (/24, /30, etc.)
- **Default Gateway**: Configuring the router interface that devices use to communicate with other networks
- **Routers**: Understanding how routers connect different networks and forward packets based on routing tables
- **Switches**: Learning the difference between Layer 2 (switches) and Layer 3 (routers) devices
- **OSI/TCP-IP Layers**: Understanding the layered approach to networking, particularly the Network and Internet layers
- **Routing Tables**: Configuring static routes and understanding destination/next-hop relationships
- **Network vs Broadcast Addresses**: Identifying special addresses that cannot be assigned to hosts

### Classic References

**Official Documentation**:
- [RFC 791 - Internet Protocol](https://tools.ietf.org/html/rfc791) - The foundational specification for IPv4
- [RFC 1918 - Address Allocation for Private Internets](https://tools.ietf.org/html/rfc1918) - Private IP address ranges
- [RFC 950 - Internet Standard Subnetting Procedure](https://tools.ietf.org/html/rfc950) - Subnet mask specification

**Books and Tutorials**:
- *TCP/IP Illustrated, Volume 1* by W. Richard Stevens - Comprehensive guide to TCP/IP protocols
- [Cisco Networking Academy](https://www.netacad.com/) - Free networking courses and materials
- [Subnet Calculator and Documentation](https://www.subnet-calculator.com/) - Interactive subnet calculation tools
- [Professor Messer's Network+ Course](https://www.professormesser.com/network-plus/n10-008/n10-008-video/n10-008-training-course/) - Free video tutorials on networking fundamentals

**Interactive Learning**:
- [Subnetting Practice](https://subnettingpractice.com/) - Practice subnet calculations
- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) - Network simulation tool

### AI Usage

**AI tools were used for the following tasks**:

1. **Concept Clarification**: Used Claude/ChatGPT to understand complex networking concepts such as:
   - How subnet masks work in binary
   - Routing table configuration logic
   - Difference between routers and switches

2. **Subnet Calculations**: Verified subnet calculations and IP range determinations for accuracy

3. **Troubleshooting Guidance**: When stuck on specific levels, asked AI to explain why certain configurations were failing

4. **README Documentation**: AI assisted in structuring this README and explaining technical concepts clearly

**Parts of the project completed independently**:
- All 10 level configurations were solved through personal understanding and practice
- Network topology analysis and problem-solving for each level
- Testing and validation of all configurations

**Learning Approach**: AI was used as a learning aid and reference tool, similar to consulting documentation or tutorials, but all practical problem-solving and configuration work was done independently to ensure genuine understanding of networking principles.

## Tips for Success

- **Start Simple**: Begin with understanding a /24 network before moving to more complex subnets
- **Think in Binary**: Subnet calculations become much easier when you understand binary operations
- **Check Your Math**: Always verify that your IP addresses are within the valid range for your subnet
- **Gateway Rules**: Remember that the default gateway must be an IP address on the same network as your device
- **Router Interfaces**: Each router interface should be on a different network
- **Use /30 for Routers**: When connecting two routers, use /30 subnets (provides exactly 2 usable IPs)

## Common Mistakes to Avoid

- ❌ Using network address (e.g., 192.168.1.0) or broadcast address (e.g., 192.168.1.255) for devices
- ❌ Having devices on the same network with different subnet masks
- ❌ Setting a gateway that's not on the same network as the device
- ❌ Forgetting to configure routing tables in routers

---

**Project Status**: ✅ Completed

**Difficulty Level**: Intermediate

**Estimated Time**: 15-20 Days (depending on prior networking knowledge)