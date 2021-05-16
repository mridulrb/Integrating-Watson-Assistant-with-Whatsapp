# Integrating IBM Watson Assistant with WhatsApp

Chatbots are everywhere these days, and most businesses aim to use them to increase productivity and provide a better customer experience. In this tutorial, my colleague Mridul Bhandari and I, Khalil Faraj will demonstrate how to extend a Watson Assistant chatbot's capabilities by connecting it to WhatsApp using Twilio. We will be using Twilio's sandbox to show how this integration works.

**Prerequisites**
-[IBM Cloud Account]()
-[Twilio Account]()

In this tutorial, we are assuming that you already know what Watson Assistant is and how it works. We will be only focusing on the integration part with WhatsApp. However, if you haven't used Watson before then you can get started [here](https://developer.ibm.com/tutorials/create-your-first-assistant-powered-chatbot/).

1.	Go to your Watson Assistant service in IBM Cloud. Let's first add a dialog skill to our Assistant. Go to this GitHub Repo and download it. It has the dialog skill that we will be using for our assistant. Once it's downloaded, import the skill in the Assistant.
![image](https://user-images.githubusercontent.com/12492961/118400998-023e5380-b675-11eb-8935-4ce597e1c972.png)
