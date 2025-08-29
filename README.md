<h1>Goodwe AA55 Status Request Using Node Red
</h1>
        
Goodwe inverters communicate via UDP, by default running on port 8899. The ES/EM/BP inverter family use a native 'AA55' protocol (and ModBus protocol). This Node Red flow packages and sends three types of pre-canned AA55 status request to the inverter.  
  
0x2 - Device Version Request  
0x6 - Device Running Data Request  
0x9 - Device Status Data Request  

Message buffer structure.  

Byte | Value
------------- | -------------
0 | 0xAA
1 | 0x55
2 | Source Address - default is 0xC0
3 | Destination Address - default is 0x7F
4 | Control Code
5 | Function Code
6 | Length
7-n | Data 0,1 ..N
n+1 | Checksum
n+2 | Checksum


<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>
