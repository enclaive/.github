# Welcome to enclaive - Home of Confidential Compute Containers 👋 

![GitHub Org's stars](https://img.shields.io/github/stars/enclaive?style=social)
[![Twitter Follow](https://img.shields.io/twitter/follow/enclaive_io?style=social)](https://twitter.com/enclaive_io)
[![Discord Shield](https://discordapp.com/api/guilds/1019995230130413668/widget.png?style=shield)](https://discord.com/invite/AqWbg7Aw?utm_source=Discord%20Widget&utm_medium=Connect)
![enclaive.io](/images/container.jpeg)


# TL;TR
* 👂 We are enclaive, pronounced /ˈɛnkleɪv/ 
* 🔭 We build easy-to-use containers of the open-source stack with the extra power that the container application is fully memory encrypted at any moment in time during execution and can prove its confidential state to a third party like the owner of the container running it in the cloud
* :100: Why/when use confidential containers
  * You care about data and application security and privacy, respectively
  * You distrust the hosting/cloud provider
  * You run in a multi-cloud environement and want to reduce the hardware complexity with hardware-graded software (instead of hardware) isolation
  * You have unused compute ressources (e.g. private data center) and want to share the ressources while giving users the necessary trust
  * You have built some super cool application, your users insists to host the application on premise, you fear of giving away the code ("intelectual property protection")
  * You have built another super cool application, you host the application in the cloud, and you and/or your users fear disclosing personal data ("data privacy", "data sovereignty")
  * You have built yet another super application, you host the application, and fear the security costs ("security expenses reduction")
* 🕺 We combine Intel Security Guard Extension and open-source libOS technology to turn standard containers into confidential containers
* ❤️ We love open-source software and want that many more users benefit from the awesomeness
* 🤝 We aim to help open-source projects to close the last mile :100:
* 🤔 We're looking for devs, devops, and (open-source) projects interested in collaborting with us to deploy their service in confidential containers
* 📫 How to reach us: Best way is via email (contact@enclaive.io) or  <a href="https://discord.com/invite/AqWbg7Aw?utm_source=Discord%20Widget&utm_medium=Connect">discord</a>
* ⚡ Fun fact: the 'i' in enclaive stands for <u>i</u>nimitable pointing to the fact that whatever runs in confidential containers can't be copied

# TL;DR
 <a href="https://www.youtube.com/channel/UChuBVOzH6WY7d31UcqMgMLg">
 <img src="https://img.shields.io/youtube/channel/views/UChuBVOzH6WY7d31UcqMgMLg?style=social">
 </a>
<table style="width:100%">
<tr>
    <td align="center" width:"25%">
        <a href="https://www.youtube.com/watch?v=LZ10X1AlnJs"><img src="https://img.youtube.com/vi/LZ10X1AlnJs/0.jpg"></img></a>
        <br>104s introduction to confidential compute</td> 
     </td>

 </tr>
 </table>
      

# Organization

<div align=center>
 <table>
    <tr> 
      <td align="center">
        <a href="https:/enclaive.io">
<img alt="enclaive-logo" height=64px src="https://avatars.githubusercontent.com/u/79869513">
</a>
        <br>enclaive.io</td>     
      </td>  
    </tr>
    </table>
</div>

<h3 align="center">Home of Confidential Compute Containers</h3>

  <p align="center">
    <a href="https://github.com/enclaive/.github/edit/main/profile/README.md#confidential-containers-in-action">Demo Videos</a>
    ·
    <a href="https:/enclaive.io">Web Site </a>
    ·
    <a href="https://twitter.com/enclaive_io">Twitter</a>
    ·
    <a href="https://www.youtube.com/channel/UChuBVOzH6WY7d31UcqMgMLg">Youtube</a>
    <br><br>
 Community Page
 <br>
     <a href=https://enclaive.io/community/write-for-enclaive/)">Write for us</a>
    ·
    <a href="https://enclaive.io/community/introduction-articles/">Introduction Articles</a>
    ·
    <a href="https://enclaive.io/community/tutorials">Tutorials</a>
    
                                            


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
<details><summary>Confidential Containers Technology explained</summary>
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
    <details><summary>A Primer: How does it work?</summary>
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
        caused by attacks leading to container esacalation including buffer overflow, return oriented programing, spectre, meltdown, rowhammer and various forms of rootkits. 
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
    Get in touch with us via email (contact@enclaive.io), twitter (enclaive_io) or discord.
    <br><br>
</details> 
<details><summary>Getting Started</summary>
    <br>    
   We suggest you look into the wiki (tbd) to familiarize with the underlying technology and get the first containers packaged by enclaive running.
   <br><br>
</details> 

### Our main projects ("The Base")

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
      <!--
    <td align="center">
         <a href="https://github.com/enclaive/enclaive-docker-sqlite-sgx">
        <img alt="sqlite-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sqlite/sqlite-original.svg">
        </a>
      <br>SQlite-SGX</td> 
      -->
</tr>
<tr>
 <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-nodejs-sgx">
      <img alt="nodejs-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-plain.svg">
     </a>
      <br>Nodejs-SGX</td>   
     <td align="center">
      <a href="https://github.com/enclaive/enclaive-docker-python-sgx">
       <img alt="python-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
      </a>
      <br>Python-SGX</td>     
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-rust-sgx">
     <img alt="rust-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rust/rust-plain.svg">
     </a>
      <br>Rust-SGX</td>   
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-go-sgx">
     <img alt="go-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg">
     </a>
      <br>Go-SGX</td> 
      <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-php-sgx">
     <img alt="php-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg">
     </a>
      <br>PHP-SGX</td> 
    </tr>
    <tr>
     <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-ruby-sgx">
     <img alt="ruby-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/ruby/ruby-plain.svg">
     </a>
      <br>Ruby-SGX</td>
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-java-sgx">
     <img alt="java-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg">
     </a>
      <br>Java-SGX</td> 
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-c-sgx">
     <img alt="c-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg">
     </a>
     <br>C-SGX</td> 
     <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-cpp-sgx">
     <img alt="cplusplus-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg">
     </a>
      <br>Cpp-SGX</td> 
     <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-cs-sgx">
     <img alt="csharp-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
     </a>
      <br>Csharp-SGX</td> 
</tr>
<tr>      
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-mosquitto-sgx">
     <img alt="mosquitto-sgx" height=64px src="https://raw.githubusercontent.com/eclipse/mosquitto/master/logo/mosquitto-logo-min.svg">
     </a>
      <br>Mosquitto-SGX</td> 
          <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-nginx-sgx">
      <img alt="nginx-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg">
     </a>
      <br>Nginx-SGX</td>    
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-wordpress-sgx">
     <img alt="wordpress-sgx" height=64px src="https://raw.githubusercontent.com/devicons/devicon/master/icons/wordpress/wordpress-plain.svg">
     </a>
      <br>Wordpress-SGX</td>
    <td align="center">
     <a href="https://github.com/enclaive/enclaive-docker-umami-sgx">
     <img alt="umami-sgx" height=64px src="https://raw.githubusercontent.com/umami-software/umami/master/public/safari-pinned-tab.svg">
     </a>
     <br>Umami-SGX</td>
</tr>
</table>

### Videos: Confidential Containers in Action
<table style="width:100%">
<tr> 
     <td width="25%" halign="center" valign="top">
      <a href="https://youtu.be/SoKIo0kIg_4"><img    src="https://img.youtube.com/vi/SoKIo0kIg_4/0.jpg"></img></a>
        <br>Dumping the Redis Memory while in Use (<a href="https://github.com/enclaive/enclaive-docker-redis-sgx/tree/demo">read more</a>)</td>
     <td width="25%" halign="center" valign="top">
         <a href="https://youtu.be/PI2PosrdrCk"><img  src="https://img.youtube.com/vi/PI2PosrdrCk/0.jpg"</img></a>
         <br>MariaDB Data-in-Use encryption of SQL queries (<a href="https://github.com/enclaive/enclaive-docker-mariadb-sgx/tree/demo">read more</a>)
    </td>
     <td width="25%" halign="center" valign="top">
        <a href="https://www.youtube.com/watch?v=3FCULfBqFN0"><img  src="https://img.youtube.com/vi/3FCULfBqFN0/0.jpg"</img></a>
        <br>MongoDB Data-in-Use encyption of password insertion (<a href="https://github.com/enclaive/enclaive-docker-mongodb-sgx/tree/demo">read more</a>)
         <td width="25%" halign="center" valign="top">
      <a href="https://youtu.be/v0CmPF9YzQ4"><img    src="https://img.youtube.com/vi/v0CmPF9YzQ4/0.jpg"></img></a>
        <br>ArangoDB Data-in-Use Encryption (<a href="https://github.com/enclaive/enclaive-docker-arangodb-sgx/tree/demo">read more</a>)</td>
        <tr>
        <td width="25%" halign="center" valign="top">
        <a href="https://youtu.be/Q9EGCAQUC4U"><img  src="https://img.youtube.com/vi/Q9EGCAQUC4U/0.jpg"></img></a>
        <br>NodeJS Express and Protection against Runtime Leakage (<a href="https://github.com/enclaive/enclaive-docker-nodejs-sgx/tree/demo">read more</a>)</td>
               <td width="25%" halign="center" valign="top">
      <a href="https://youtu.be/RnZjhZinOE8"><img    src="https://img.youtube.com/vi/RnZjhZinOE8/0.jpg"></img></a>
        <br>Attempt to modify protected Volume/Files (<a href="https://github.com/enclaive/enclaive-docker-cs-sgx/tree/demo">read more</a>)</td>
       <td width="25%" halign="center" valign="top">
      <a href="https://youtu.be/KrFgXp5BelI"><img    src="https://img.youtube.com/vi/KrFgXp5BelI/0.jpg"></img></a>
        <br>Write a file into shared protected Volume (<a href="https://github.com/enclaive/enclaive-docker-ruby-sgx/tree/demo">read more</a>)</td>
                                                                                                                               <td width="25%" halign="center" valign="top">
      <a href="https://www.youtube.com/watch?v=GCe4HKyq1X0"><img    src="https://img.youtube.com/vi/GCe4HKyq1X0/0.jpg"></img></a>
        <br>HTTPS server prevents the access to X.509 certificate private key (<a href="https://github.com/enclaive/enclaive-docker-go-sgx/tree/demo">read more</a>)
     </td>
                                                                                                                                                     </tr><tr>
                                                                                                                                                             <td width="25%" halign="center" valign="top">
        <a href="https://www.youtube.com/watch?v=DbxZuflYtC8"><img  src="https://img.youtube.com/vi/DbxZuflYtC8/0.jpg"></img></a>
        <br>Wordpress anonymizes the IP-to-geolocation lookup (<a href="https://github.com/enclaive/enclaive-docker-wordpress-sgx/tree/demo">read more</a>)</td></tr>                                                                                                                                   
                                                                                                                                            </table> <br> ... for more examples check also out the demo branch of other repos 
   
   
## For AMA, join Discord 

We believe in community efforts. If you want to stop by for some java, get to know us, get pointers to how get started, seek support or help with your own project, you find us on ...
<br>
<br>
<a href="https://discord.com/invite/AqWbg7Aw?utm_source=Discord%20Widget&utm_medium=Connect">
<img src="https://discordapp.com/api/guilds/1019995230130413668/widget.png?style=banner4" alt="Discord Banner 4"/>
</a>      
