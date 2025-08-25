---
title: "The struggles of custom roms -  Contactless payments"
date: "2025-08-25T1:00:00-02:00"
tags: ["technology", "phones", "mini-blog"]
title-images: []
ending-images: []
author: "NaomiTheAshenOne"
draft: false
table-of-contents: true
toc-auto-numbering: true
---
<!-- introduction -->
![thumbnail](/the-struggles-of-custom-roms/whatsthecatch.png)
*This post will be targeted towards people who already use custom android roms or are interested in doing so, if not feel free to skip to the rambles at the end :D*
## The Problem
Ever since I started using custom roms one feature was always missing - Contactless/NFC payments.

As Gpay and Apple pay gained popularity over the years there became less and less reasons for banks to implement their own NFC payment systems. And worst competitors to these services are few and far between with often the same issues as Gpay.
<!--more-->
<!-- rest of the content -->
Over the years there has been ways to get Gpay to work on custom roms, with the most notable method being gapps + Play Integrity fix module. This did however come with the drawback of requiring your phone to be rooted in order to install the module (although I do believe crDroid shipped with it up until recently). Unfortunately recent changes made by google mean that this fix no longer works forcing us to look for alternative methods.
## The fix?
[Curve Pay](https://www.curve.com/). Its a UK based Gpay alternative that works with every bank. Most importantly to us, this app has the ability of making contactless payments and does not directly rely off Gpay to do so!

Sounds great but whats the catch? Lets do some testing:
### Testing table:

| Device      | OS                                                                       | Important Features                                              | Result                                              |
| ----------- | ------------------------------------------------------------------------ | --------------------------------------------------------------- | --------------------------------------------------- |
| Samsung S10 | [crDroid 11.7](https://crdroid.net/beyond1lte/11)                        | Gapps installed                                                 | Works                                               |
| Oneplus 3T  | [Lineage OS 18.1](https://wiki.lineageos.org/devices/oneplus3/variant2/) | Gapps installed                                                 | Works                                               |
| Pixel 7     | [Graphene](https://grapheneos.org/)                                      | Sandboxed Play Services                                         | Works                                               |
| Pixel 7a    | [crDroid 11.6](https://crdroid.net/lynx/11)                              | MicroG (installed no config)                                    | The application boots however NFC does not function |
| Pixel 7a    | [crDroid 11.6](https://crdroid.net/lynx/11)                              | MicroG setup with full permissions and google account connected | The application boots however NFC does not function |
| Pixel 7a    | [crDroid 11.6](https://crdroid.net/lynx/11)                              | No google re-implementation installed                           | App does not boot                                   |

## Results:

While Curve pay does not rely on Gpay to function it is clear that it still requires google services to be present to function correctly. This means that if you want to use contactless pay you will have to have a google re-implementation installed on your device which of course has the usual google related privacy concerns. The best way to have NFC pay work with Curve would be to use Graphene OS, thanks to its compatibility layer for google play it allows you to use its services in a sand-boxed environment and prevents google from having overreaching system permissions on your device. If you are not concerned with google privacy issues though any custom rom should work assuming it supports NFC and you have installed Gapps :D    

While the MicroG setup did not work for NFC it may still be useful to some as Curve allows for reward cards to be added, which is a life saver when apps like Tescos try to block being used on custom roms and screenshots. (You can use android studio to screenshot the bar-code too tho X3)
### The fine print
But Naomi, what about the privacy implications of having a third-party see your payment records? 

Curve does have a handy privacy policy that you can view [here](https://www.curve.com/legal/privacy/), the TLDR is that they do collect data about your transactions and this data can be given over to social media sites and advertising companies. However, you can contact privacyrequests@imaginecurve.com to request the data does not be used in that way, and they do also claim that data is aggregated and anonymised. 

At the end of the day if this concerns you then you shouldn't be using cards in the first place, as most banks can and will sell your transaction data ^^'.
## Final Thoughts
Uhhhhh just put your card in the back of your case?

![handsomeman](/the-struggles-of-custom-roms/handsomeman.png)
### Special Thanks
Zoobdude - Orginally asked me if Curve Pay would work on Custom Roms

GalacticeAce - Tested Curve pay on Graphene OS

You - Thanks for reading :D
## Ending rambles
Hey there! Its been min since I have posted on here, I have had quite a lot going on recently. This is just a short blog documenting some recent findings, I have some more projects in the works and hopefully I will be able to share them in the not *too* distant future x3

I recently replaced my Pixel 7a's battery as it was defective [(see here to check if your battery will explode XD)](https://support.google.com/pixelphone/workflow/15767701?visit_id=638768598049292721-161654573&p=pixel7a_battery_flow&rd=1) I managed to score a "Coral" back plate for cheap so also put that on it instead, I now present to you the Gordon Freeman phone!:
![handsomeman](/the-struggles-of-custom-roms/thefreemanphone.png)

Since writing this I have also gotten a Pixel 7 Pro for £18, may make a blog about restoring it in the future as its in pretty poor shape XD 

As always if you want to discuss anything for any reason feel free to message me on discord @naomi.the.ashen.one

I'm not super active on there anymore but I don't have any other way to be contacted rn :P
