---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: myst
      format_version: '1.1'
      jupytext_version: 1.1.0
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---
<!-- 
+++ {"slideshow": {"slide_type": "slide"}}

# Tutorial slides

- Slides are optional (e.g., you may not use them if your presentation is via live coding).
- If the pre-recorded presentations will use slides, we request that you deposit the slides in this folder.

+++ {"slideshow": {"slide_type": "slide"}}

## Use text-based source

- We ask that you use text-based formats for your slides, e.g., markdown 
- This markdown file is an example source for slides using `nbconvert` and Reveal. See the GitHub action '.github/workflows/slides.yml' in this repo so see how this markdown file is converted to a HTML slide show and published on GitHub Pages - https://fawazsiddiqi.github.io/slides_to_pages

+++ {"slideshow": {"slide_type": "subslide"}}

## An example sub-slide

- Another option: you can write your slide content using markdown and use an app for slide design, like [Deckset](https://www.deckset.com) or similar.

+++ {"slideshow": {"slide_type": "slide"}}

## Naming convention and file list

- Use a **naming convention** where each file name starts with a number, reflecting the order of use in the presentation of the tutorial.
- List your slide files in a markdown, with a brief description.


+++ {"slideshow": {"slide_type": "slide"}} 
-->


**🌟 Overview** <br />
In this workshop, we will extend Watson Assistant chatbot's capabilities by connecting it to Whatsapp using Twilio. We will be using Twilio's sandbox to show how this integration works to build and have a conversation with a chatbot through Whatsapp.

🎓 What will you learn? <br />
• What is Watson Assistant <br />
• What is Twilio <br />
• How to integrate Watson Assistant with Whatsapp

👩‍💻 Who should attend? <br />
Anyone interested in AI and chatbots is welcome to attend the workshop, but it is preferred that you have some knowledge about Watson Assistant and chatbots since this workshop won't focus much on covering the basics of Watson Assistant.

+++ {"slideshow": {"slide_type": "subslide"}}

🎙️ Speakers <br />
- Mridul Bhandari, IBM Developer Advocate, https://www.linkedin.com/in/mridul-bhandari
- Khalil Faraj, IBM Developer Advocate, https://www.linkedin.com/in/khalilfaraj/
- Hashim Noor, IBM Technical Specialist, https://www.linkedin.com/in/hashim-noor/

🎈 Prerequisites <br />
☁ Register for a free IBM Cloud Account: https://ibm.biz/whatsapp-chatbot <br />
☁ Sign up for a Twilio account: https://ibm.biz/whatsapp-chatbot-twilio

🍉 Register for the live stream and replay on Crowdcast: https://www.crowdcast.io/e/whatsapp-chatbot <br />

👩‍💻Resources <br />
- Survey - https://ibm.biz/whatsapp-chatbot-survey
- GitHub Repository - https://ibm.biz/whatsapp-chatbot-repo
- Workshop Slides - https://ibm.biz/whatsapp-chatbot-slides
- Hands-on - https://ibm.biz/whatsapp-chatbot-lab
- Meetup page - https://www.meetup.com/IBM-Cloud-MEA/events/ 

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide1.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide2.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide3.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide4.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide5.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide6.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide7.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide8.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide9.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide10.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide11.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide12.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide13.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide14.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide15.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide16.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide17.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide18.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide19.jpeg?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/Integrating-Watson-Assistant-with-Whatsapp/blob/main/Images/slide_images/Slide20.jpeg?raw=true)


+++ {"slideshow": {"slide_type": "slide"}}
## License

**Recommend** that slides be shared under a [CC-BY](https://creativecommons.org/licenses/by/4.0/) license.
