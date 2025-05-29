# Automate-Responsive-Action-
Active Directory Project - The goal of this project is to create an active directory environment and integrate Splunk ,Slack, Shuffle to Automate Responsive Action

Start by creating logical diagram ( how i want to build up my lab) using Vultr virtual 

<img width="2281" alt="Image" src="https://github.com/user-attachments/assets/642d9ad8-a4e0-435c-a1c7-9b10476d04eb" />

I Created 3 virtual machines on Vultr Doman 

A.Splunk Ubuntu Server (Tobilab-Splunk)

B. Domain Controller Windows Server ( MYTOBIlab-ADDC01)

C.Test Machine Windows Server ( TobiTestLab)


<img width="2436" alt="Image" src="https://github.com/user-attachments/assets/3fd59b32-e336-49a1-96ce-b6805d3cdd8d" />

An attacker is on the internet essentially scanning and finds test machine has the right credentials and successful authenticates, then generates a Splunk alert ( i will be sending telemetry from test machine to Splunk server)

Then Splunk send a notification to slack ( indicating something has happened)

Will also trigger a plaaybook to Shuffle which will also send an email notification to Soc Analyst asking if they want to Disable users.

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


Create an alert that detect successful authenication 



