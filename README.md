## Opta Network Security: Firewall & ACL Configurations


## Overview
This project focuses on securing Opta’s network using firewall rules and Access Control Lists (ACLs) to regulate traffic flow based on predefined security policies. The configuration ensures only authorized communication occurs between subnets while preventing unauthorized access from external sources.

## Objectives
- Allow only authorized traffic between subnets.
- Block inbound traffic from the Internet.
- Restrict internal users from accessing external networks.

## Network Topology & Components
The network consists of:
- **Cisco Firewall** – Implements perimeter security policies.
- **Router & Layer 3 Switch** – Controls traffic routing and segmentation.
- **Client PCs & File Server** – Used to test access control rules.
- **Packet Tracer** – Simulates and configures the network environment.

## Implementation Steps
1. **Set up the logical topology**
   The copper straight through cable was used to interconnect all the devices on the Opta's network.
   
  ![image](https://github.com/user-attachments/assets/4b35bd8b-eaed-44b1-bba0-a0b398d7d688)

2. **Configure the Router**

  ![image](https://github.com/user-attachments/assets/5a1441c1-fefc-4164-8f0e-58b88da12440)


3. **Configure the Cisco Firewall**

  ![image](https://github.com/user-attachments/assets/2d69180b-33cf-490a-b984-40a689feeba7)

4. **Firewall ACL Configuration**
   - Set up rules to block unauthorized inbound connections.
   - Allow internal communication based on security policies.

     ![image](https://github.com/user-attachments/assets/6ff6a915-fddd-461e-aa49-a20f902b9542)


5. **Router ACL Configuration**
   - Define ACL rules to control subnet traffic.
   - Restrict outbound Internet access for internal users.
  
      ![image](https://github.com/user-attachments/assets/ec90f143-877f-40d3-81b6-6e84da1fd09e)

6. **Configure IP Address (Static) for the Admin Office PC, Finance Office PC, and the File Server**
   - The Admin Office: 192.168.1.2
   - The Finance Office: 192.168.1.3
   - The File Server: 192.168.1.10
   - Ideally, the Default Gateway will be the firewall, since we want all traffic to go through the firewall: 192.168.1.1


7. **Testing & Validation**
   - Verify the PCs are able to communicate with the File Server by using the ping command

   - The Admin office PC is able to communicate with the server and the Finance office PC

   ![image](https://github.com/user-attachments/assets/69914ef2-9b83-4997-866a-e2a5a3fdff50)

- The Finance Office PC is able to communicate with the server and the Admin Office PC

  ![image](https://github.com/user-attachments/assets/91617da6-7f2d-479f-b33c-5a873942eeb4)


- The file server is able to communicate withh the Admin and Finance office PCs

   ![image](https://github.com/user-attachments/assets/75afdd0a-ca23-4d5e-89b1-dc95733fed46)

   - Test firewall rules against unauthorized access.
  
     ![image](https://github.com/user-attachments/assets/0739b6cd-90b4-45a6-b990-2d2def7bf619)

8. **Testing the Firewall rule to confirm that it was effective**

   - Ping the internet from the Admin's Office PC
     
     ![image](https://github.com/user-attachments/assets/c4381ae1-3cdd-4a0b-80e4-31454458fd49)

  - Ping the internet from the Finance Office PC
  
    ![image](https://github.com/user-attachments/assets/fa50a9c3-1006-481c-91a2-5d30c1d047d0)

  - Ping the internnet from the File Server

    ![image](https://github.com/user-attachments/assets/a5f3e11b-1892-4cdf-9344-5ed94c1b9d4d)


 ## Results & Findings
The implemented firewall and ACL rules successfully:
- Prevented inbound Internet traffic from reaching internal resources.
- Allowed only authorized communication between subnets.
- Blocked internal users from accessing external networks.

## Conclusion
This project demonstrates an effective approach to securing network traffic by implementing firewalls and ACLs. It ensures controlled access and strengthens network security against unauthorized access attempts.

