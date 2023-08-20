# Virtualization_Load_balancing_scalability
# Project Summary: Virtualization Infrastructure Upgrade

## Project Objective
Upgrade [Mock Company]'s existing infrastructure to a virtualized environment for improved scalability, performance, and security.

## Technical Details

### 1. Virtualization Platform
Implement VMware vSphere with ESXi hosts.

### 2. Virtual Hosts
- **DC01:** Deploy Windows Server 2019 Standard as the domain controller for [Mock Company]. Hosts DNS and DHCP services.
- **IIS01 and IIS02:** Set up Windows Server 2019 Datacenter for web servers with NIC teaming and load balancing.
- **WIN10:** Configure Windows 10 Enterprise as a remote access point.
- **PfSense:** Establish a virtual router for the network gateway.

### 3. Networking
- Utilize vSwitch per VLAN for layer 2 isolation.
- Define firewall rules through Active Directory for security.
- Apply access control lists (ACLs) based on profiles for the principle of least privilege.

### 4. Security Groups
- Create unique Security Groups with the principle of least privilege.
- Monitor changes in group composition and activities.
- Implement a strong password policy.

### 5. Performance Tuning
- Implement NIC teaming for higher throughput.
- Use NLB for traffic load balancing.
- Monitor CPU, memory, and network throughput.

### 6. Load Balancing
- Integrate load balancing at the infrastructure level using Azure.
- Utilize Standard tier load balancers for traffic routing.
- Implement Gateway Load balancers for security against DDoS attacks.

### 7. Testing Strategy
- Test user connectivity and monitor server health in the NLB pool.
- Ensure latency consistency across regions/availability zones.

## Proof-of-Concept Implementation Build

### Phase 1
- Server named ESX-1 with port groups "DEV," "SysADMIN," and "Public" using VLAN ID 2, 3, 0 respectively.
![Picture17](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/39b97e8c-01f1-4a98-ba46-d9769cd7ac82)
### Phase 2
- VM Server named DC01 with Windows Server 2019 Standard provisioned. Domain Controller for augustacrissy.lab.
![Picture18](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/5b4ee3ba-6f6b-4af4-b208-a68e2d7cf8c7)

### Phase 3
- VM Server named Router with pfSense.
  
![Picture19](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/2accf732-123a-4590-bb07-cb10946dd1ed)

![Picture20](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/25c72772-bb20-4073-af98-be21fd78fead)

### Phase 4
- 2 VM Servers named IIS01 and IIS02 with Windows Server 2019 Datacenter.
![Picture21](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/e1f55536-f6d8-4096-86a0-2d2dadd04508)

![Picture22](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/0fa92229-f917-4b9b-876d-e6136430d65a)

### Phase 5
- Network Load Balancing between IIS01 and IIS02.
  
![Picture23](https://github.com/jbdjerhy/Virtualization_Load_balancing_scalability/assets/142699688/bd194875-7cd2-4665-bb33-c44aef4c577b)

This project aims to enhance [Mock Company]'s infrastructure by migrating to a virtualized environment, ensuring improved performance, security, and scalability while adhering to best practices in network management and security.
