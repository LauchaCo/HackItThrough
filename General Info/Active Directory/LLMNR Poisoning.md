## Definition
__LLMNR Poisoning__ is an attack that relies in the [LLMNR](</General Info/Tecnologias/Active Directory/LLMNR>) protocol being active. The attack consists in the attacker listening for LLMNR requests and, when a broadcast packet reaches its machine because of a DNS failure, he responds with their own IP address (or any other IP to redirect the traffic). This can lead to credential theft and relay attacks in AD.

## Sample walkthrough

### Step 1:
The attacker has to run this command in order to make the [lgandx's Responder](https://github.com/lgandx/Responder) tool listen for incoming [LLMNR](</General Info/Tecnologias/Active Directory/LLMNR>) broadcast packets.
```
sudo responder -I ens33 -dwP
```
![Responder_message](</Resources/Responder_message.png>)
### Step 2:
Wait for an event to occur in the Network and Triggers LLMNR<br>![LLMNR_Event](</Resources/LLMNR_Event.png>)
Once this event occurs and the tool automatically responds maliciously, the attacker will obtain sensitive information, including:
- The IP of the victim
- The domain\username of the victim
- The victim's password hash
With this last one piece of information you can attempt to crack this hash offline with tools like ([JohnTheRipper](</General Info/Tools/JohnTheRipper.md>), [Hashcat](</General Info/Tools/Hashcat.md>))
### Step 3:
Running one of the previously mentioned tools (Hashcat in this case) 

