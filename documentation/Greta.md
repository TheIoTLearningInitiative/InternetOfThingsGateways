Greta
==

# Gateways 

## Theory

### Definition

> Gateways are “Traffic controllers” that bridge data generation to support a range of connectivity protocols and satisfy complex management. Gateways are also called middleware development devices because they are found "in the middle" of an IoT solution. They can filter and aggregate data, secure remote management, save temporal data, have cloud connectivity and device interconnectivity.



>http://www.intel.com/content/www/us/en/internet-of-things/gateway-solutions.html

>To be added (links, information)

### Architecture

> The architecture of an Intel gateway consists in 4 basic layers with their correspondant suplayeers. At the bottom we have an Intel Board and Modules (Intel Quark SoC, Intel Atom SoC, Intel Core SoC). Above this layer we have a Wind River Linux Operating System. Above this Operating System layer we have the modules that make a gateway a data controller solution. In this layer we have hardware (discrete TPM and Secure Boot), Run-Time Environment which could be Lua, Java, Python or OSGi, Manageability with Wind River Helix Device, OMA DM, TR-069, and web configuration. There we have too a security layer that has enabled OpenSSL, iptables, encrypted storage, DM-Crypt and an IPsec VPN. 

http://www.windriver.com/announces/intel-gateway-solutions-for-iot/resources/IDP_XT_Product_Overview.pdf



### Justification

> Gateways give developers the flexibility to create and deploy innovative, cost-effective and secure Internet of Things solutions for a wide array of business segments.

> Connectivity is critical to generating intelligence.
Without connectivity, there is no either Smart or Internet in the IoT.

>Can:
* Reduce the cost of backend cloud
* Reduce latency, actions executed immediately
* Prefer having data locally than in the cloud
* Protocol Consolidation
* Edge to Cloud Connectivity
* Remote I/O
* Scalability
* Support for multiple protocols
* Application Software




> https://www-ssl.intel.com/content/www/us/en/embedded/solutions/iot-gateway/overview.html
> http://www.windriver.com/announces/intel-gateway-solutions-for-iot/

### Applications

> Buildings: Adaptive analytics can improve the accuracy and performance of systems used to monitor and manage energy consumption, climate control, lighting, mechanical equipment and security.
> Energy: Devices can adjust the speed and blade pitch of wind turbines to improve efficiency and reduce wear.
> Transportation
Smart control systems can tell trains to slow down based on a variety of constantly changing external data inputs, such as weather, topography, location, distance from destination, track conditions, or car-to-car communication indicating another train is ahead.

> http://www.windriver.com/announces/intel-gateway-solutions-for-iot/

## Hands-On

1. Review the following gateways models
   1.1 Intel DK50, DK100, DK200, DK300.
   1.2 Dell Edge Gateway 5000
   1.3 Advantech UTX-3115
2. List the Communications and Connectivity found in the above gateways
3. What are the Operating Systems supported by different the gateways?
4. 
5. http://www.intel.com/content/www/us/en/embedded/solutions/iot-gateway/development-kits.html

# Wind River 

## Intelligent Device Platform XT

### Theory

#### Definition

> Is a customizable middleware development environment that provides security, connectivity, rich networking options, and device management. It simplifies the development, integration, and deployment for the Internet of Things.

- Extract value and transform your business
- Intelligent gateways provides a smooth interface between devices and the cloud
- Extend legacy systems with intelligent gateways
- Compute capacity powers growth
- Gateways enable new capabilities
- Ensure connectivity with gateways
- Remotely manage and troubleshoot devices
- More connectivity requires greater security
- Trust your network, trust your data
- Transform your business today

#### Architecture

> To be added (links, information)
> To be structure what are the components, etc e.g. https://www.youtube.com/watch?v=yj5gGxncPlA

#### Differences

##### Operating Systems
>  Intel® IoT Gateways offer a choice of Intel® processors for different application needs, support for multiple operating systems (Wind River and Ubuntu* Linux,* Microsoft Windows* 10, etc.), and robust device management capabilities.
> * Intel® IoT Gateways are the result of Intel’s collaboration with McAfee and Wind River. By providing pre-integrated, pre-validated hardware and software building blocks, the gateways connect legacy and new systems, and enable seamless and secure data flow between edge devices and the cloud.

##### Security McAffee

> McAfee Embedded Control* maximizes security by dynamically monitoring and managing whitelists. 
> Verify system integrity at the hardware level to protect critical data throughout the device lifecycle.
http://www.intel.com/content/www/us/en/embedded/solutions/iot-gateway/development-kits.html


## Wind River Company

1. What is Wind River®?
World leader in embedded software for intelligent connected systems.
Delivers the technology and expertise that enables the innovation and deployment of safe, secure, and reliable intelligent systems.
2. Products of Wind River
Portfolio of software solutions for harnessing intelligence 
to drive innovation and business transformation.
Developers and device manufacturers can create the safe, 
secure, and reliable intelligent systems that make up IoT.
Also, move the data generated by these systems–from 
the secure and managed devices, through the gateway, 
across the critical network infrastructure, and up into the cloud. 
Wind River Helix: The Software Foundation for the Internet of Things
* Operating Systems
* Network Infrastructure
* Gateways
* Edge Management
* Simulation
* Open Networks

## Wind River IoT Building Blocks

> Devices: The “things” in the Internet of Things. 
By 2020, these data generators and gatherers will number 26 billon, 
all connected to the Internet and providing businesses with endless data from which to analyze and extract value and meaning.
> Gateways: “Traffic controllers” bridge data generation to support an ever-broadening range of connectivity protocols and satisfy complex management.
> Networks: This complex interconnected infrastructure for delivering data to every corner of industry and enterprise networks must be optimized for maximum agility, scalability, flexibility, and security.
> Cloud: Comprising public, private, and hybrid forms, this off-premise storage faces a daunting surge in analytic, security, and reliability challenges to keep pace with the uptime demands of critical infrastructure and trusted systems designed to leverage IoT.


Abraham to add more data

# Security 

## Importance of Security

> To be added (links, information)
> As the IoT grows, so do the security vulnerabilities of the linked objects.
> With the arrival of IoT several new types of devices are connected to IP networks.
-Medical equipment
-Buildings
-Cameras
-Industrial sensors
-Many other devices.

All these devices need management Access to transport data securely over the internet.


## Security in Non IoT Solutions Vs IoT Solutions

> To be added (links, information)
> 
> How can new enterprise implementations secure their data flow?

## Secure Data Traffic

> To be added (links, information)
> Focuses on protecting critical data.
> Any data traffic between a device and the cloud (including information transmitted via mobile apps) should be examined to make sure it is secured.


## Cryptography Protocols

Review Secure Sockets Layer (SSL) Transport Layer Security (TLS)

## Hardware Security Solutions

> To be added (links, information)

## Software Security Solutions

### Mocana NanoSSL

> To be added (links, information)

### WolfSSL

> To be added (links, information)

### Mosquitto and Mosquitto SSL

> To be added (links, information)

## Hands-On

1. ...
2. ...


# Helix Cloud

