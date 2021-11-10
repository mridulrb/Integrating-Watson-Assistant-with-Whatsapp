# Integrating IBM Watson Assistant with WhatsApp

Chatbots are everywhere these days, and most businesses aim to use them to increase productivity and provide a better customer experience. In this tutorial, we will demonstrate how to extend a Watson Assistant chatbot's capabilities by connecting it to WhatsApp using Twilio. We will be using Twilio's sandbox to show how this integration works.

## Workshop Resources
- Login/Sign Up for IBM Cloud: https://ibm.biz/IBMTwilio <br/>
- Hands-On Guide: https://ibm.biz/whatsapp-chatbot-lab <br/>
- Slides: https://ibm.biz/whatsapp-twilio-slides <br/>
- Twilio Sign Up: https://ibm.biz/tryTwilio <br/>
- Workshop Replay: https://www.crowdcast.io/e/whatsapp-chatbot <br/>
- New Watson Assistant Version: https://developer.ibm.com/tutorials/integrating-ibm-watson-assistant-with-whatsapp/

**Prerequisites**
- [IBM Cloud Account](http://ibm.biz/BdfyVx)
- [Twilio Account](www.twilio.com/referral/jO1067)

## Architecture Diagram
<img width="451" alt="Architecture_Diagram" src="https://user-images.githubusercontent.com/12492961/123856997-ce707200-d932-11eb-87be-65f91f0375bd.png">

In this tutorial, we are assuming that you already know what Watson Assistant is and how it works. We will be only focusing on the integration part with WhatsApp. However, if you haven't used Watson before then you can get started [here](https://developer.ibm.com/tutorials/create-your-first-assistant-powered-chatbot/).

1.	Go to your Watson Assistant service in IBM Cloud. Let's first add a dialog skill to our Assistant. Go to this GitHub Repo and download it. It has the dialog skill that we will be using for our assistant. Once it's downloaded, import the skill in the Assistant. <br/>
![1_jC7gVgmB80VjqIeaS_zw1A](https://user-images.githubusercontent.com/12492961/129473000-bf891ae7-f343-4499-b1b1-e4a85c9ee67a.png)

2. Under Integrations on the right side, choose WhatsApp with Twilio. <br/>
![2](https://user-images.githubusercontent.com/12492961/129473010-a606c9d3-7be8-438e-9cd9-18bdb8184761.png)

3. Choose WhatsApp with Twilio and then click Create. <br/>
![3](https://user-images.githubusercontent.com/12492961/129473017-43185803-26c4-420d-be9d-237c6759394d.png)

4. Now here we will need to set the Account SID and Auth token that we can get from Twilio. Go to your Twilio account (if you don't an account, you can create one [here](www.twilio.com/referral/jO1067)) and copy your Account SID and Auth token that are in the home dashboard. (Click on Show to reveal the token). <br/>
![4](https://user-images.githubusercontent.com/12492961/129473038-7c4f0aa7-40a5-4fca-84c2-a5ea5eaf830e.png)

5. Go back to your Watson Assistant and fill Account SID and Auth token with the values that you got from Twilio. <br/>
![5](https://user-images.githubusercontent.com/12492961/129473036-c1990e5c-bbc5-4191-834f-374e8a752bb6.png)
<br/> Click Sync Account and wait for it till it shows Synced. Once it's synced you will see a webhook URL generated in the WhatsApp Webhook field. Copy this URL and go back to Twilio. <br/>

6.	Now we need to set up and configure our Twilio sandbox to integrate it with Watson Assistant. In your Twilio Account, click on the icon that represents all products and services (it's below the home icon) on the left side go to Programmable Messaging from the expanded menu and select Try WhatsApp under the Try it out section. <br/>
![6](https://user-images.githubusercontent.com/12492961/129473035-46be850a-c392-446a-ad73-41c033b69af2.png)
<br/> We will be using this testing sandbox for our integration. Send the given code/message to the number provided by Twilio from your WhatsApp. <br/>
![6a](https://user-images.githubusercontent.com/12492961/118401223-e4bdb980-b675-11eb-885c-c0d8c71e7ba2.jpg) <br/> 
<br/> Once it's done, you should see Message Received on Twilio like this image. <br/>
![6b](https://user-images.githubusercontent.com/12492961/129473031-634099af-b17b-4696-8e26-86c36d4fe21e.png)
<br/> This means that now your phone number is connected to this Twilio-WhatsApp sandbox. <br/>

7.	Click Next. The second step is to set a template in case you're working with a One-Way Message case like appointment reminders, order notification and verification codes. So, in these cases, only the service is talking to the user. We are not interested in this step for this tutorial so you can click Next to move to the 3rd step which is Two-Way Messaging where both the user and the service can send messages which results in a conversation. The service triggers a 24-hour conversation window in which the conversation can take place. Send a reply to the message that you received on WhatsApp and click Next: Configure Your Sandbox. <br/>
![7](https://user-images.githubusercontent.com/12492961/129473029-4fc7947f-6aab-4d1e-858c-0e974bc4ef00.png)

8.	Paste the webhook URL that you have from Watson Assistant into the When a message comes in field. You should see your number in the sandbox participants and others can enter this sandbox by sending the code mentioned to the sandbox WhatsApp number (In the below image the code is join design-thumb). Once you're done click save. <br/>
![8](https://user-images.githubusercontent.com/12492961/129473023-57d35a4e-5c48-4fef-84f9-c0eda80a2296.png)

9.	All is set. Now the Assistant is integrated with WhatsApp through Twilio. From your device, send a WhatsApp message to the WhatsApp sandbox number and you will receive the assistant's response. <br/>
![9](https://user-images.githubusercontent.com/12492961/118401334-572e9980-b676-11eb-93eb-d9e6dfc8e119.jpg)

In this tutorial, you were able to successfully integrate your Watson Assistant with WhatsApp through Twilio. Since this is a tutorial, we were using WhatsApp-Twilio sandbox to show you how this integration work. If you want to use WhatsApp-Twilio with the Assistant for a real use case, then you will need to have a premium Twilio Account, a Facebook Business Manager ID and apply for permission. You can find more information about this [here](https://cloud.ibm.com/docs/assistant?topic=assistant-deploy-whatsapp). You can also check out the video for this tutorial [here](https://www.youtube.com/watch?v=UtB2klF1h7c).




