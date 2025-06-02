# Automate-Responsive-Action-
Active Directory Project - The goal of this project is to create an active directory environment and integrate Splunk ,Slack, Shuffle to Automate Responsive Action

Start by creating logical diagram ( how i want to build up my lab) using Vultr virtual 

<img width="2281" alt="Image" src="https://github.com/user-attachments/assets/642d9ad8-a4e0-435c-a1c7-9b10476d04eb" />

I Created 3 virtual machines on Vultr Doman 

A.Splunk Ubuntu Server (Tobilab-Splunk)

B. Domain Controller Windows Server ( MYTOBIlab-ADDC01)

C.Test Machine Windows Server ( TobiTestLab)


<img width="2436" alt="Image" src="https://github.com/user-attachments/assets/3fd59b32-e336-49a1-96ce-b6805d3cdd8d" />


An external attacker scans the internet and discovers the test machine . Upon identifying valid credentials the attacker successfully authenicates .This activity triggers a Splunk alert , as telemetry from the test machine is being sent to the Splunk Server 
Then Splunk send a notification to slack ( indicating something has happened)


Will also trigger a playbook to Shuffle which will also send an email notification to Soc Analyst asking if they want to Disable users.


If Soc Analyst say No nothing will be done 

If Soc analyst say Yes ( will instruct shuffle to move to the next step, which is instructing the domain controller to disable domain user.

Install and Configure Splunk

Send Telemetry from windows

Create an that detect successful authentication 

<img width="2390" alt="Image" src="https://github.com/user-attachments/assets/9888aef1-d82d-4ee1-bc75-344efa495061" />



<img width="2229" alt="Image" src="https://github.com/user-attachments/assets/047e0dac-4936-4ba3-8505-1beed38a5004" />



<img width="2313" alt="Image" src="https://github.com/user-attachments/assets/dc86a09c-0a21-42f3-aa07-09d39736f0e4" />



<img width="2254" alt="Image" src="https://github.com/user-attachments/assets/4387079b-5025-4508-8de3-00f679fc047a" />



<img width="2409" alt="Image" src="https://github.com/user-attachments/assets/5badf1e9-0bce-44c9-8eba-7dd68c8a1f0b" />



<img width="1502" alt="Image" src="https://github.com/user-attachments/assets/ae9cad8b-4840-4864-b22f-7dab14bd62f7" />



Install and Configure Active Diectory into window server (MYTOBILAB-ADDC01)



<img width="2411" alt="Image" src="https://github.com/user-attachments/assets/d6586672-9b13-4838-a824-e5b39d308ebb" />



<img width="1455" alt="Image" src="https://github.com/user-attachments/assets/10e0a39a-3c40-4c78-8d0a-72c5b1c72667" />



<img width="1882" alt="Image" src="https://github.com/user-attachments/assets/1aca6e4c-9262-4e66-9ba6-84c8e4a08f77" />



<img width="1340" alt="Image" src="https://github.com/user-attachments/assets/79ad7e7a-b188-4992-a56b-aa8f45b26cfb" />



<img width="2410" alt="Image" src="https://github.com/user-attachments/assets/d07a6231-e16c-4399-8e70-85c41a1fc8c8" />



<img width="1109" alt="Image" src="https://github.com/user-attachments/assets/6d55450a-c380-46f8-a7ea-2abd7765c45f" />




Install and Configure TestLab(TobiTestLab)



<img width="2345" alt="Image" src="https://github.com/user-attachments/assets/3f7d9f96-fb32-4f70-a936-3e04ace4fb22" />




<img width="2403" alt="Image" src="https://github.com/user-attachments/assets/7107c62d-53bb-45c8-a8ec-cd4f7110e26f" />




<img width="2318" alt="Image" src="https://github.com/user-attachments/assets/200fde95-74f6-4f51-a383-264e4fb73076" />




<img width="2338" alt="Image" src="https://github.com/user-attachments/assets/1289a805-221b-4800-9b07-665789aebb8b" />




Next Install application , Splunk add on for windows 



<img width="2457" alt="Image" src="https://github.com/user-attachments/assets/8c4c2d8e-4db7-4103-a0a3-65702e87c0c8" />




<img width="1823" alt="Image" src="https://github.com/user-attachments/assets/749c3aaa-5e97-4e40-8bd3-e090e31db5d6" />






Next Step is to Install universal forwarder and recieving on both windows machine in other to send data to Splunk 



<img width="865" alt="Image" src="https://github.com/user-attachments/assets/da309fc0-5199-4aef-8697-48aa06ea84f5" />



<img width="973" alt="Image" src="https://github.com/user-attachments/assets/091411e4-51d8-4fe4-ab6f-0a65a53bc8a3" />




<img width="1152" alt="Image" src="https://github.com/user-attachments/assets/e5fb8f73-63f5-4ab3-ae49-d0070e7763e9" />





Create an alert that detect successful authenication 



<img width="2464" alt="Image" src="https://github.com/user-attachments/assets/c2ed6252-849e-4beb-92ed-0f29acfb3da6" />




You Observe there data moving from TOBITESTLAB into Splunk 



<img width="1532" alt="Image" src="https://github.com/user-attachments/assets/779edf80-67d2-457f-8029-ab490cbc09a5" />




<img width="2456" alt="Image" src="https://github.com/user-attachments/assets/4d8d67cd-992f-4b26-bc78-0ef87f93e4be" />




<img width="1492" alt="Image" src="https://github.com/user-attachments/assets/c8339265-95dc-40bd-becb-598efc9289e9" />



Alert is Created 


<img width="2550" alt="Image" src="https://github.com/user-attachments/assets/2bfc7a7f-ada6-4b5b-bcb1-734b330c0c8b" />




Integrate SLACK and SHUFFLE ( Build Mini Resposive Playblook 

Goal is disable user if Unauthorised Siccefful Login RDP

SPLunk Alerts will be connected to Slack, send a notification Slack 



<img width="2531" alt="Image" src="https://github.com/user-attachments/assets/c2f82abc-fd20-41de-a508-10a36ce32c8f" />



I created a new channel on Slack i called  Tobi Alerts , this is where all of my alerts will be posted in 



<img width="2526" alt="Image" src="https://github.com/user-attachments/assets/48eb0cad-f572-4a76-a94b-d77d8625b344" />



You can already see all the alerts coming in 



<img width="2526" alt="Image" src="https://github.com/user-attachments/assets/df24e802-561a-43ae-a319-1d54f5c1e485" />




Then an email notification will be send to your email from Shuffle support requesting if you would like to diable the user 




<img width="2248" alt="Image" src="https://github.com/user-attachments/assets/cb253cf0-5908-4d23-a33a-5f0a273579cd" />




If you click Yes , take you this link then diables the user.




<img width="2505" alt="Image" src="https://github.com/user-attachments/assets/900e74a3-1d6a-4343-96f4-1299cf90f035" />



