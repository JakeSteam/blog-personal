---
title: "Verifying identity on Companies House with GOV.UK One Login: A walkthrough of the upcoming requirement's process"
image: /assets/images/banners/govuk-identity.png
tags:
  - Government
  - Verification
  - Walkthrough
  - UK
---

On the 8th April, the UK Government released the ability to verify your identity if you control a UK company. Since this will eventually become a requirement, I went through the surprisingly smooth process!

The [GOV.UK page](https://www.gov.uk/guidance/verifying-your-identity-for-companies-house) has plenty of information, clarifying who needs to verify (any director / person with control / company secretary / etc), and why (to improve reliability / trust of company data). Since I set my own company up quite a while ago I couldn't remember the process, so was pretty surprised identities weren't already verified somehow!

Since I have a UK passport, and a phone, and sole ownership of a company, the whole process was painless. As such, it seemed valuable to document the process for those who eventually are required to do it later this year.

## UK government services login

For those who haven't interacted with the UK government's digital services before, they're fragmented, but anything on `GOV.UK` is typically extremely high quality. It won a "[Design of the Year](https://www.bbc.co.uk/news/entertainment-arts-22164715)" award upon release a decade ago, and I've had very positive experiences every time a service has been needed.

However, you'll end up with a different account for each government service, with the issue becoming even worse if you own a company! Even my minimal government interaction has resulted in separate accounts for Personal Tax, Company Tax, Driving Licence, background checks, Companies House, Land Registry, and probably more I've forgotten about.

When combined with various 2FA and secret codes some of these services require, it's always a struggle to know exactly which login is needed! Luckily the government realised this is a mess, and introduced [GOV.UK One Login](https://www.sign-in.service.gov.uk/), currently in beta and rolling out governmental service by service.

There's [a full list of supported services](https://www.gov.uk/using-your-gov-uk-one-login/services) available, and the sheer variety here highlights what a massive task a unified login is. Apprenticeships, Welsh fishing permits, Veteran cards, cancelling passports, violent crime compensation, turns out a government does a lot!

## Creating a GOV.UK One Login

First up, you'll be prompted to enter an email for your new, unified login. This is all pretty standard, with email verification and password setting.

As a nice surprise, 2FA appeared to be _required_ to create the account. Since this is a brand-new login system that will likely be around for decades, guaranteeing all users are as secure as possible is a very sensible move.

As a fun quirk, the new "GOV.UK One Login" shows a "Capital One" icon in Authy (presumably due to the name), not quite right!

[![GOV.UK One Login create account prompt](/assets/images/2025/govuk-createaccount.png)](/assets/images/2025/govuk-createaccount.png)

### Email mismatch

I was then prompted for the password to my Companies House account, but that uses another email address. Oops. After a little struggle to escape this impossible-to-complete password request I ended up using incognito mode for the rest of the process.

Whilst this does seem a bad experience, it was entirely my own fault! The previous page warned me, in bold, and I apparently skim read it and ignored the instructions entirely. Proof you can't completely idiot-proof anything, huh?

[![GOV.UK One Login using same email](/assets/images/2025/govuk-sameemail.png)](/assets/images/2025/govuk-sameemail.png)

Anyway, once the Companies House password for the email used for the new account is entered, we're on to the next step.

## Verifying identity (web)

### First steps

Here's probably the biggest pain point, I'm asked a question I don't know the answer to, and no way of finding out.

On the surface "Has your identity been verified for Companies House?" seems easy to answer, but it's unclear what exactly verified means. Given the account was created 7-8 years ago, I've no idea what verification I did!

Since I'm connecting 2 Government service (One Login & Companies House) they know the answer better than me, so this isn't ideal. I worked on the assumption that by "verified" it means this brand-new system, so selected "No", presumably correctly.

[![GOV.UK One Login have verified question](/assets/images/2025/govuk-haveverified.png)](/assets/images/2025/govuk-haveverified.png)

### Preparing to verify

Now that I've confirmed I haven't verified before, it's unsurprisingly time to verify! There's a bit of preamble here, and it's great to see there are ways to complete verification without installing an app, or even without a phone at all.

I intended to use the app, although I'm very curious what questions would be asked to verify my identity that would be anywhere near as secure as scanning my passport's NFC and my face.

[![GOV.UK One Login verify info](/assets/images/2025/govuk-verifyinfo-thumbnail.png)](/assets/images/2025/govuk-verifyinfo.png)

I'm now taken to a rapid-fire series of eligibility questions, to check the app is suitable for me. My scenario is very simple (UK resident, up-to-date documents, etc) so I suspect this is mostly the "happy path" through (besides needing to handover to my phone). Anyway, the questions were:

1. Do you live in the UK / Channel Islands / Isle of Man? (Yes)
2. Do you have a valid passport, driving licence, or one of various similar documents? (Yes)
3. Are you on a computer or tablet? (Yes, image below)
4. Do you have an Android / iOS / other phone? (Yes)
5. Do you have a passport? (Yes)
6. Does the passport have the biometric data symbol? (Yes)

And with that, I'm recommended to install the app to verify further:

|                                                          On computer?                                                          |                                                      Use the app!                                                       |
| :----------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------: |
| [![GOV.UK One Login on computer question](/assets/images/2025/govuk-oncomputer.png)](/assets/images/2025/govuk-oncomputer.png) | [![GOV.UK One Login prompt to use the app](/assets/images/2025/govuk-useapp.png)](/assets/images/2025/govuk-useapp.png) |

### Installing app

Next up, I'm shown a unique QR code to scan with my phone. This takes me to the [Play Store page for GOV.UK ID Check](https://play.google.com/store/apps/details?id=uk.gov.documentchecking), with a bit of tracking to make the web to app handover smoother.

So, into the app we go!

## Verifying identity (app)

Here's a preview of the next few steps:

|                                                              Analytics prompt                                                              |                                                            App linking                                                            |                                                                    Passport reading                                                                     |                                                                 Review prompt                                                                 |
| :----------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: |
| [![GOV.UK One Login analytics prompt](/assets/images/2025/govuk-app-analytics-thumbnail.jpg)](/assets/images/2025/govuk-app-analytics.jpg) | [![GOV.UK One Login app linking](/assets/images/2025/govuk-app-linking-thumbnail.jpg)](/assets/images/2025/govuk-app-linking.jpg) | [![GOV.UK One Login passport scanning](/assets/images/2025/govuk-app-passportreading-thumbnail.jpg)](/assets/images/2025/govuk-app-passportreading.jpg) | [![GOV.UK One Login review prompt](/assets/images/2025/govuk-app-reviewprompt-thumbnail.jpg)](/assets/images/2025/govuk-app-reviewprompt.jpg) |

### Preparing app

Once the app is installed, a remarkably smooth process kicks off! I've verified my identity with at least 4-5 services (banks etc) via my phone, and the quality varies dramatically. This was easily the best.

First up, we get a prompt to share analytics. The rationale before displaying the prompt is very neutral, with both options progressing to the next screen.

On the next screen, we _somehow_ link the app to our previous web session on a PC. The app opens a new tab in your browser with a single "Link app to continue" button, taking you back into the app. I believe this does something very clever, depending on whether it has managed to figure out where you came from:

1. If you **have** downloaded the app via GOV.UK's QR code, I noticed some IDs in the referral URL. I assume this is attribution data, containing information about my account. Once back in the app, I can progress.
2. If you **haven't** downloaded the app via GOV.UK's QR code, the site itself looks identical, but once back in the app you need to scan a QR code (presumably with the same attribution info) from the website. I assume once "linked", the rest of the flow is identical.

### Passport verification

Next up, taking a photo of the passport. Although hard to describe, this was the best passport scanner I've used! It displayed a real-time overlay of the data (e.g. name) it had managed to read, and was very forgiving with working out where the edges of the passport where. It also didn't mess around with taking a photo then scanning it, asking if I wanted to retake etc, it just looked at it in real-time and we're done!

Then, the biometric data needs scanning via NFC. Whilst I have seen this particular trick before, I really liked that the app showed me the scanned data once it was done as a reassurance. I didn't know it was possible to pull my photo in high quality directly from my passport (assuming that's what happened), if so it explains why passport NFC & face scan is enough for most third party identity verifications.

### Face verification

Now I need to verify that my passport face is the same as... my actual face. This step typically fails around half the time for me (including at airport passport gates!), due to non-humans being confused by my appearance changes since my 5-6 year old passport picture:

1. I had typical length hair then, shaved head now.
2. I was clean-shaven then, beard now.
3. I've aged 5-6 years, unsurprisingly!

This scan was different to usual, with no silly phrases / head moving, and instead flashing a series of lights on my face. As with the passport scan, it did an interesting overlay of my features (although all I could really see was facial hair!), providing a little reassurance that it's working as expected.

### Verified

All done! The app can now be uninstalled and presumably never used again, but I was surprised they had a review prompt for a one-time use app (I [added it to an app recently](https://blog.jakelee.co.uk/play-store-rating-prompt/) and it massively boosted rating). This really highlights how high quality the app is, with even this entirely optional bonus feature being implemented. The app would have exactly as many users if the store rating was 1/5 or 5/5 since it is a legal requirement, yet the effort has been made to earn a high rating (4.7). Very impressive.

Now, back to the web for a few final pieces.

## Finishing up (web)

I'd left the previous tab open whilst performing the app steps, and it had automatically changed to a success message!

[![GOV.UK One Login successfully verified](/assets/images/2025/govuk-successfullyverified.png)](/assets/images/2025/govuk-successfullyverified.png)

### Final checks

Next up, a soft Experian credit check (image below)! This was pretty unexpected, but it makes sense due to the likely highly accurate and comprehensive data credit agencies hold (plus their awareness of fraud markers etc). To quote the information box, again with useful rationale:

> We'll check your details with Experian. This is because companies like Experian have access to information about interactions you've previously had with other organisations.

If you think about it too hard it's a little scary that a company you might never have interacted with likely holds more information on you than the government, so don't think too hard!

First my current address was needed, along with the date moved. This is fairly common when performing a credit lookup, so I suspect it's to ensure the correct person is being looked up. The results weren't shown to me, just a loading screen then a successful verification message (image below).

I was given a new personal code (in the format `ABC-D123-4567`), which goes alongside the [company code](https://www.gov.uk/guidance/company-authentication-codes-for-online-filing) for future filings. This is a little confusing, but it's understandable that verifying I'm me, and verifying I can act on the company's behalf are different codes. It's also good to see this code is fairly long, unlike the previous 5 digit company authentication codes.

Finally, I made my way to the list of services in One Login, and yep, there's Companies House. Hopefully there'll be lots more services (all?) in the future, although some are under different email addresses so that'll be fun!

|                                                           Experian credit check                                                            |                                                                     Verification complete                                                                     |                                                            One Login services                                                            |
| :----------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------: |
| [![GOV.UK One Login credit check warning](/assets/images/2025/govuk-creditcheck-thumbnail.png)](/assets/images/2025/govuk-creditcheck.png) | [![GOV.UK One Login verification complete](/assets/images/2025/govuk-verificationcomplete-thumbnail.png)](/assets/images/2025/govuk-verificationcomplete.png) | [![GOV.UK One Login list of services](/assets/images/2025/govuk-yourservices-thumbnail.png)](/assets/images/2025/govuk-yourservices.png) |

We're done! There's a bit of further commentary below, but my identity is fully verified.

## Engineering notes

As an Android engineer, I was very, very impressed with the handover both to and from the app. The overall identity verifying process was also _far_ less problematic than [my recent ordeal with Google Play](https://blog.jakelee.co.uk/publishing-on-google-play-without-exposing-info/)!

It's clear that significant effort has been put in to ensure the user always has a route to follow. Even if a seemingly base requirement like having a phone or a passport fails, the steps proceed as if every path is equally expected.

For example, in my scenario I started on my PC so had to be transferred to my phone. To me this seems the obvious, normal route, but for many (more?) people, starting on their phone and navigating between apps will be the obvious route! The process works smoothly regardless.

It's a shame about the [initial misstep](#email-mismatch) with the wrong email address, since even though it is entirely my fault, getting stuck without the ability to try another email is a shame. If it wasn't for this the entire thing would have been flawless! I'd love to see a diagram or flow chart of every possible path through this process, since there must be some extremely convoluted edge cases.

Finally, I was extremely surprised that most (all?) of the One Login source code [is public on GitHub](https://github.com/govuk-one-login), including [the Android app](https://github.com/govuk-one-login/mobile-android-one-login-app)! This is a solid "money where your mouth is" piece of evidence that the government truly does care about high quality software, as is [the detailed technical documentation](https://docs.sign-in.service.gov.uk/quick-start/#run-the-example-service-with-the-gov-uk-one-login-simulator-using-docker-compose).

## Design notes

Throughout this process, a few excellent pieces of design become obvious even to my engineering-first brain:

1. **Consistent design**: Every page across every service, and the app itself, is extremely consistent. Same fonts, same design principles, it contributes significantly to feeling like one smooth process.
2. **Clear guidance**: Unlike many processes where it's easy to get lost, or go round in circles, I only ever had 1 decision to make at a time. This might be allowing analytics data, or selecting if I have a passport, or just tapping a big green button to go to the next screen. Due to this, I know I am on an expected route, and it'll likely work.
3. **Confident tone of voice**: Finally, each screen's text was confident without being arrogant. It is aware that you _need_ to complete this process, so instead of using convincing language (e.g. "Please tap...") it uses authoritative language ("Return to the GOV.UK window..."). This confidence is reassuring, it shows that the creator is confident in the next steps, and your ability to complete them, instead of pandering or using marketing speak.

Similarly to the open sourced code, there are [Figma user flows](https://www.figma.com/design/raCO0C9Lq0cNJ2VKC5jwy5/GOV.UK-One-Login-sign-in-user-journey-maps?node-id=1-49&p=f) available, and [an overall Government design system](https://design-system.service.gov.uk/), it's great to see the government using industry standard tools for design as well as engineering!

## Conclusion

Turns out, it's possible to be impressed by a governmental identity verification process!

Both from an engineering, design, and messaging perspective, GOV.UK's One Login system is an excellent experience, especially considering the decades of older systems it inevitably has to work with.

The fact they've managed to get 50 government services onboard in 3 years ([as of Oct 2024](https://gds.blog.gov.uk/2024/11/12/gov-uk-one-login-celebrating-50-services/)) is a strong indicator of its success, and the article contains some interesting stats (again, as of Oct '24):

> - over 3 million One Login accounts have been created
> - over 6.2 million identities issued
> - over 8.8 million downloads of our ID check app
> - now 50 services and counting onboarded

Hopefully this'll be the only time I need to create a "One" account, and eventually it becomes the most important account I own!
