#                 Ansible controlNode and Node configuration

---

Step1:
---

- Start two instance on aws .

    Connect to the linux machine and run the

  

---


![step1](/images/step1.PNG)

Step2
---
- Open the Terminal window with Ansible Control Node Tab

- Connect with ubuntu machine with ip address using the following command

        ssh ubuntu@ip

![step2](/images/1.png)

---

Step 3

 Connect the ubuntu machine with ip address using the following command


   ``` Sudo apt update``` 
    
(system tracks changes to each package when a new 
            version is released.)

---

![step3](/images/2.png)

---

Step 4

- Follow the steps for installing installing ansible in the control node

         sudo apt update
         sudo apt install software-properties-common -y
         sudo apt install ansible -y
         sudo add-apt-repository --yes --update ppa:ansible/ansible


![step4](/images/3.png)

---

---

![step5](/images/4.png)

---

---

![step6](/images/5.png)

---

---

Step 5:

### Add the user in the present machine 

- By using Sudo module we can add user  with same name  in the three different machines 
```
 sudo adduser devops
```

![step7](/images/6.png)

---

---

Step 6: 


- Give the user acesss permissions using visudo admin module



![step8](/images/7.png)

---

Step7:

Configure the sshd file using the following command

         sudo vi /etc/ssh/sshd-config
---

![step9](/images/8.png)

---
Step 8:


- Connect the machine with user we have created for example user name is devops using the  following command

        ssh devops@ip


---

![step10](/images/9.png)

---

Step 9:

Then exit from the user for checking purpose
---

![step11](/images/10.png)

---
Step 10:

- Again connect to the machine from another node1

---

![step13](/images/12.png)

---

---

Step 11:

Generate Keygen for the users to connect 

![step14](/images/13.png)

---

---
Step 12: 

- Check the directory for the SSH key
by using the following commad

```
cd ./.ssh/

```
Step 13

- check the directory of ssh 

![step15](/images/14.png)

---

Step 14:


- Copy the ssh- key id to the diffent node 

---

![step16](/images/15.png)

---

---
Step 15:

Copy the ssh- key id to the diffent node from Redhat


![step17](/images/16.png)

---

---
Step 16:

- check the directory

![step18](/images/17.png)

---

---

Step 17:

- Ping all the hosts by giving the following commands

    ```ansible -m ping -i host all```

![step19](/images/18.png)

---

Step 18:
 
 - edit the inventory files with diffrent nodes and save with the following command

 ``` sudo vi/home/devops/host ```
---

![step20](/images/19.png)

---

---

Installation Successfull

---

![step21](/images/20.png)

---






