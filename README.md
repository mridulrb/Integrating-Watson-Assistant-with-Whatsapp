# Integrating IBM Watson Assistant with WhatsApp

Chatbots are everywhere these days, and most businesses aim to use them to increase productivity and provide a better customer experience. In this tutorial, we will demonstrate how to extend a Watson Assistant chatbot's capabilities by connecting it to WhatsApp using Twilio. We will be using Twilio's sandbox to show how this integration works.

**Prerequisites**
- [IBM Cloud Account](http://ibm.biz/BdfyVx)
- [Twilio Account](www.twilio.com/referral/jO1067)

In this tutorial, we are assuming that you already know what Watson Assistant is and how it works. We will be only focusing on the integration part with WhatsApp. However, if you haven't used Watson before then you can get started [here](https://developer.ibm.com/tutorials/create-your-first-assistant-powered-chatbot/).

1.	Go to your Watson Assistant service in IBM Cloud. Let's first add a dialog skill to our Assistant. Go to this GitHub Repo and download it. It has the dialog skill that we will be using for our assistant. Once it's downloaded, import the skill in the Assistant. <br/>
![1](https://user-images.githubusercontent.com/12492961/118401066-46315880-b675-11eb-8ec9-424cc64cc0cd.png)

2. Under Integrations on the right side, choose WhatsApp with Twilio. <br/>
![2](https://user-images.githubusercontent.com/12492961/118401100-6103cd00-b675-11eb-85cb-01b1f059781b.png)

3. Choose WhatsApp with Twilio and then click Create. <br/>
![3](https://user-images.githubusercontent.com/12492961/118401118-7547ca00-b675-11eb-8469-32cec99e733e.png)

4. Now here we will need to set the Account SID and Auth token that we can get from Twilio. Go to your Twilio account (if you don't an account, you can create one [here](www.twilio.com/referral/jO1067)) and copy your Account SID and Auth token that are in the home dashboard. (Click on Show to reveal the token). <br/>
![4](https://user-images.githubusercontent.com/12492961/118401162-93adc580-b675-11eb-97e3-28cea6ccab3e.png)

5. Go back to your Watson Assistant and fill Account SID and Auth token with the values that you got from Twilio. <br/>
![5](https://user-images.githubusercontent.com/12492961/118401166-9e685a80-b675-11eb-9334-d10b02f1b230.png)
<br/> Click Sync Account and wait for it till it shows Synced. Once it's synced you will see a webhook URL generated in the WhatsApp Webhook field. Copy this URL and go back to Twilio. <br/>

6.	Now we need to set up and configure our Twilio sandbox to integrate it with Watson Assistant. In your Twilio Account, click on the icon that represents all products and services (it's below the home icon) on the left side go to Programmable Messaging from the expanded menu and select Try WhatsApp under the Try it out section. <br/>
![6](https://user-images.githubusercontent.com/12492961/118401202-c061dd00-b675-11eb-9472-8367940d716e.png)
<br/> We will be using this testing sandbox for our integration. Send the given code/message to the number provided by Twilio from your WhatsApp. <br/>
![6a](https://user-images.githubusercontent.com/12492961/118401223-e4bdb980-b675-11eb-885c-c0d8c71e7ba2.jpg)
<br/> Click [here](https://api.whatsapp.com/send?phone=+1(415)523-8886&text=join%20design-thumb) to send the message to given number or Scan this QR Code. <br/>
![WA](https://user-images.githubusercontent.com/12492961/118401683-a2957780-b677-11eb-88aa-93adb2b79271.png)
<br/> Once it's done, you should see Message Received on Twilio like this image. <br/>
![6b](https://user-images.githubusercontent.com/12492961/118401243-fb641080-b675-11eb-927f-43188c4efbe2.png)
<br/> This means that now your phone number is connected to this Twilio-WhatsApp sandbox. <br/>

7.	Click Next. The second step is to set a template in case you're working with a One-Way Message case like appointment reminders, order notification and verification codes. So, in these cases, only the service is talking to the user. We are not interested in this step for this tutorial so you can click Next to move to the 3rd step which is Two-Way Messaging where both the user and the service can send messages which results in a conversation. The service triggers a 24-hour conversation window in which the conversation can take place. Send a reply to the message that you received on WhatsApp and click Next: Configure Your Sandbox. <br/>
![7](https://user-images.githubusercontent.com/12492961/118401293-3108f980-b676-11eb-808f-8aac814be54b.png)

8.	Paste the webhook URL that you have from Watson Assistant into the When a message comes in field. You should see your number in the sandbox participants and others can enter this sandbox by sending the code mentioned to the sandbox WhatsApp number (In the below image the code is join design-thumb). Once you're done click save. <br/>
![8](https://user-images.githubusercontent.com/12492961/118401309-44b46000-b676-11eb-9c2b-e4ae7c990e74.png)

9.	All is set. Now the Assistant is integrated with WhatsApp through Twilio. From your device, send a WhatsApp message to the WhatsApp sandbox number and you will receive the assistant's response. <br/>
![9](https://user-images.githubusercontent.com/12492961/118401334-572e9980-b676-11eb-93eb-d9e6dfc8e119.jpg)

In this tutorial, you were able to successfully integrate your Watson Assistant with WhatsApp through Twilio. Since this is a tutorial, we were using WhatsApp-Twilio sandbox to show you how this integration work. If you want to use WhatsApp-Twilio with the Assistant for a real use case, then you will need to have a premium Twilio Account, a Facebook Business Manager ID and apply for permission. You can find more information about this [here](https://cloud.ibm.com/docs/assistant?topic=assistant-deploy-whatsapp).




