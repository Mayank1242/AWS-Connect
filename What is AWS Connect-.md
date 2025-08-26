### **What is AWS Connect:-**



**Helps in automated call distribution:**

Like 100 calls per day to distribute them to diff agents.



**Interactive Voice Response(IVR):-**

Every one need IVR like from a small shop to big company.

Example:-

* Press 1 for sales
* Press 2 for Support
* Press 3 for talk to agent.





**Real time metrics and analytics:-**

Like you want to check from which location call is coming.

How much time for one call take.



**Integrate with Other AWS Service:-**

Like Lex we can connect with that like with S3.





### **IVR(Interactive Voice Response):-**



What IVR stands for ?



**Users:-**

We have to create multiple users.

Example:

we are having 2 agents on sales team who receive sales call and 4 agent on support team. For every agent we create user.



**Phone number:-**

We need a phone number from where diff people can Call.



**Queues:-**

We can create Queue.

Question : If there are 100 people calling do you think 2 agents of sales team can handle this on same time?

so we need queues for this.



**Hours of Operation:-**

What time your team available for what time.



**Flows:-**
Like when users call then it says thank you for calling us press 1 for this.



### **Building Own IVR:**



**Lets we have a company name Best Buy:-**

There are two agent **john work in sales** team, and **tom works in Support** team.



So best buy **give a phone number.**

then it ask:-
Thank you for call best buy.

Press 1 for sales.

Press 2 for Support.



When customer didn't press anything then again repeat this.

when timeout then call should disconnected.



Error case:- right now there is error call shortly.





### **AWS Connect give us 2 portal:-**



* Admin Portal : Manage the user and manage the agent and design the flow.
* Agent Portal : For agents where they can receive the call.





### **How to create IVR:**



* For that at first you need a phone Number claim.



1. Then create the agents or users.
2. Then now we gonna create a FLOW.

* *Play Prompt*
* *Get the customer Input.*
* *Set working Queue.* 
* *Set Working Queue.*
* *Assign to the agent.*
* *Disconnect.*



#### <b>FLOW:</b>



<i>ENTRY -> Play Prompt -> Get customer Input -> Set working Queue </i>





