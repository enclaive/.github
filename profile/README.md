# Welcome to enclaive - Home of Confidential Compute Containers 👋 

![GitHub Org's stars](https://img.shields.io/github/stars/enclaive?style=social)
[![Twitter Follow](https://img.shields.io/twitter/follow/enclaive_io?style=social)](https://twitter.com/enclaive_io)
[![YouTube Follow](https://img.shields.io/youtube/channel/views/UChuBVOzH6WY7d31UcqMgMLg?style=social)](https://www.youtube.com/channel/UChuBVOzH6WY7d31UcqMgMLg)
![enclaive.io](/images/container.jpeg)

# TL;TR
* 👂 We are enclaive, pronounced /ˈɛnkleɪv/ 
* 🔭 We build easy-to-use containers of the open-source stack with the extra power that the container application is fully memory encrypted at any moment in time during execution and can prove its confidential state to a third party like the owner of the container running it in the cloud
* 🕺 We combine Intel Security Guard Extension and open-source libOS technology to turn standard containers into confidential containers
* ❤️ We love open-source software and want that many more users benefit from the awesomeness
* 🤝 We aim to help open-source projects to extend their offerings with a managed, cost-effecitve, fully confidential and verifiable service thanks to the deployment in confidential containers in the public cloud
* 🤔 We're looking for open-source projects interested in collaborting with us to package their service in confidential containers
* 📫 How to reach us: Best way is via email (contact@enclaive.io)
* ⚡ Fun fact: the 'i' in enclaive stands for <u>i</u>nimitable pointing to the fact that whatever runs in confidential containers can't be copied

# enclaive Organization
### In a nutshell
<details>
<summary>Motivation </summary>
<br>
Let's be frank. Open-source software is awesome! So many projects have been created in the last decades that shaped the entire software industry. Even enterprises have realized the value and importance of open-source software. Instead of reinventing the wheel and writing proprietary software from scratch, enterprises deploy open-source software to build business applications. The enterprise-wide acceptance of open-source software has helped many community projects to establish a sustainable business model around, paving the ground to make a living out of a passionate idea. 
<br></br>
Open-source projects employ a variety of business models to solve the challenge of how to make money providing software that is by definition licensed free of charge. Each of these business strategies rests on the premise that users of open-source technologies are willing to purchase additional software features under proprietary licenses, or purchase other services or elements of value that complement the open-source software that is core to the business. This additional value can be, but not limited to, enterprise-grade features and up-time guarantees (often via a service-level agreement) to satisfy business or compliance requirements, performance and efficiency gains by features not yet available in the open source version, legal protection (e.g., indemnification from copyright or patent infringement), or professional support/training/consulting that are typical of proprietary software applications. 
<br></br>
In recent years we see a growing interest for <b>managed services</b>. Enterprises use the software without the burden of being in charge of the hosting infrastracture and its availability, as well as the updatability and security of the software. Although enterprises have numerous benefits from managed offerings, they are hesistant! The key reason is lack of control. Granting a third party the permission to manage software applications, raises a lot of trust, security, privacy and compliance issues what does not go along with enterprise policies. In some cases, in which IT resources are scarce, managed services are desperately desired, however they are ruled out strictly due to the named reasons. Software companies are thus left with the provisioning of first, second and third level support and are taken the ability to scale.
<br><br>
</details>
<details>
<summary>Mission </summary>
<br>
Our mission is to make open-source software deployable everywhere by everyone. By everyone we mean any individual, any business or any industry. By everywhere we mean any execution platform, be it private or be it public. 
We envision the further democratization of open-source software. The notion of free choice behind open-source software extends to free deployment. No one should be stopped from using open-source software anywhere. 
<br><br>
</details>
<details><summary>Confidential Containers</summary>
    <br>
    <details><summary>TL;TR</summary>
    <br>
        Confidenital Containers execute programs with the addition that 
         <br>
         <ul>
          <li>at any moment in time throughout the execution the process runs in encrypted memory  </li>    
          <li>the authenticity of the confidential execution is verifiable </li>
        </ul>
        They are compatible with Docker, Docker Swarm and Kubernetes.
        <br><br>
    </details>
    <details><summary>A Primer</summary>
        <br>        
        <p>Hardware-graded Security</p>
        Confidential Containers leverage Intel's Security Guard Extension (SGX) technology, enriching the processor architecture with special registers for key storage and cryptoraphic algorithms as well as a memory management unit with the ability to allocate physical memory for encrypted processes, called enclaves. It is important to note solely the CPU has the capability to decrypt processes running in encrypted memory;  key material is generated at random during boot and inaccessible through software.
        <br><br>
        <p>Threat Model</p>
        Exactly the hardware-graded isolation fortifies program executions in untrusted environments. By design Confidential Containers protect enclaved processes against malicious/corrupted   
        <br>
        <ul>
        <li>nested applications </li>
        <li>hypervisor </li>
        <li>kernel </li>
        <li>bootloader </li>
        </ul>   
        caused by attacks like container esacalation, buffer overflow, return oriented programing, spektre, meltdown, rowhammer and various forms of rootkits. 
        <br><br>
        <p>Local and Remote Attestation</p>
        In untrusted execution environments memory encryption is insufficient. Malicious environments may replace the container before execution. To this end, confindential containers have a unique cryptographic identity. During the container build process the author signs the application. With the corresponding key material one can verify the authenticity of the confidential container. Local attestation is a supported cryptographic protocol to locally verify the container authenticity. Here, the CPU takes the role of a trusted auditor. It measures the fingerprint of the enclaved application. Remote attestation goes one step further and allows a client to verify the authenticity. The protocol resembles the concept of local attestation and generate a cryptographic report (kinda an X.509 certificate). The aim is proving to a remote party that the platform has executed the right container. Thus, the ideal use case for remote attestation is the assurance of proper container execution in public clouds.   
        <br><br>
        <p>Key Management and Key Provisioning</p>
        Confidential containers load like off-the-shelf containers a program into the memory before execution. While remote attestation safeguards the authenticity and integrity, the approach does not prevent the untrusted environment from scrutinizing the container including the file system. For example, a Web server container is typically packaged with the server's SSL/TLS certificate and secret key. In the light of untrusted environments this approach is vulnerable and requires additional measures. A rule of thumb is to avoid to include any secrets to the confidential container. As argued before, the untrusted environment may reverse engineer the secret from the container image. The solution chosen for confidential containers is to load the application into the encrypted memory without secrets. Before running the program a pre-main process loads from a key management server the secrets through a secure channel protocol, stores them in the enclave, and continues with the main execution. A bit more concrete, the key management server first remotely attests it talks to the right container and that the container is within encrypted memory before establishing a TLS connection into the enclave to transport the secrets. The protocol is referred to as secret key provisioning and aims to mutually authenticate key provider and container before sending the secret.  
        <br><br>
    </details>  
    <details><summary>Platform Prerequisites</summary>
        <br>    
        Confidential Containers require
        <br>
        <ul>
        <li>SGX2 enabled CPUs (Intel skylake and newer)</li>
        <li>installed drivers (streamlined in Linux kernel 5.11+)</li>
        <li>docker, docker-compose, kubernetes or compatible container platform
        </ul>   
    </details>  
     <br>
</details>
<details><summary>Contribution</summary>
    <br>   
    enclaive solicites any contribution that brings confidential containers to application. 
    Get in touch with us via email (contact@enclaive.io) or twitter (enclaive_io).
    <br><br>
</details> 
<details><summary>Getting Started</summary>
    <br>    
   We suggest you look into the wiki (tbd) to familiarize with the underlying technology and get the first containers packaged by enclaive running.
   <br><br>
</details> 

### Our main projects

<table>
<tr>
    <td align="center">
    <a href="https://github.com/enclaive/enclaive-docker-arangodb-sgx">
        <img alt="arangodb-sgx" height=64px src="https://avatars.githubusercontent.com/u/5547849">
        </a> 
        <br>ArangoDB-SGX</td>  
    <td align="center">
         <a href="https://github.com/enclaive/enclaive-docker-mariadb-sgx">
             <img alt="mysql-sgx" height=64px src="https://www.vectorlogo.zone/logos/mariadb/mariadb-icon.svg">
        </a>
      <br>MariaDB-SGX</td>    
    <td align="center">
         <a href="https://github.com/enclaive/enclaive-docker-mongodb-sgx">
             <img alt="mongodb-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-plain.svg">
        </a>
      <br>MongoDB-SGX</td>    
    <td align="center">
         <a href="https://github.com/enclaive/enclaive-docker-redis-sgx">
             <img alt="redis-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-plain.svg">
        </a>
      <br>Redis-SGX</td>  
    <td align="center">
         <a href="https://github.com/enclaive/enclaive-docker-sqlite-sgx">
        <img alt="sqlite-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sqlite/sqlite-original.svg">
        </a>
      <br>SQlite-SGX</td>   
</tr>
    
<tr>
    <td align="center"><img alt="nodejs-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-plain.svg">
      <br>Nodejs-SGX</td>     
    <td align="center"><img alt="nginx-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg">
      <br>Nginx-SGX</td>             
</tr>
<tr>
     <td align="center"><img alt="python-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
      <br>Python-SGX</td>     
    <td align="center"><img alt="rust-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rust/rust-plain.svg">
      <br>Rust-SGX</td>   
    <td align="center"><img alt="go-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg">
      <br>Go-SGX</td> 
    <td align="center"><img alt="php-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg">
      <br>PHP-SGX</td>        
    <td align="center"><img alt="java-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg">
      <br>Java-SGX</td> 
    <td align="center"><img alt="c-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg"><br>C-SGX</td> 
    <td align="center"><img alt="cplusplus-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg"><br>Cpp-SGX</td>                                          
</tr>
<tr>
    <td align="center"><img alt="wordpress-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/wordpress/wordpress-plain.svg"><br>Wordpress-SGX</td>
    <td align="center"><img alt="umami-sgx" height=64px src="https://raw.githubusercontent.com/umami-software/umami/master/public/safari-pinned-tab.svg"><br>Umami-SGX</td>
</tr>
</table>

### Confidential Containers in Action
<table style="width:100%">
<tr>
    <td align="center" width:"25%">
        <a href="https://www.youtube.com/watch?v=DbxZuflYtC8"><img src="https://img.youtube.com/vi/DbxZuflYtC8/0.jpg"></img></a>
        <br>Wordpress</td> 
     </td>

 </tr>
 </table>
      
      
