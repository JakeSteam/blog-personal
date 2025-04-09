---
title: "Verifying identity on Companies House with GOV.UK One: A walkthrough of the upcoming requirement's process"
image: /assets/images/2025/
tags:
  - Government
  - Identity
---

intro

context

- Original URL: https://www.gov.uk/guidance/verifying-your-identity-for-companies-house
- Links to: https://www.gov.uk/guidance/verify-your-identity-for-companies-house

## Creating a GOV.UK One Login

- Image 1
- Verify email
- Set password
- Add 2FA (displayed as Capital One in Authy for some reason!)

### Email mismatch

- Requested to connect to companies house, but uses different email!
- It did warn me... (image 2)
- Tried to start again with companies house email, no luck, so incognito

## Verifying identity (web)

- Has identity been verified? I don't know (image 3). Selected no.
- Taken to verify identity (image 4)
  - Do live in UK / Channel Islands / Isle of Man
  - Do have passport / driving license etc
  - Are you on computer (some require phone, image 5)
  - Do you have android / ios / none
  - Do you have passport
  - Does passport have symbol on cover
  - Told to use app (image 5)
  - Scan QR code takes to personalised URL that links to store
  - Install app

## Verifying identity (app)

Here's a preview of the next few steps:

|                                             Analytics prompt                                              |                                              App linking                                              |                                                   Passport reading                                                    |                                                  Review prompt                                                  |
| :-------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------: |
| [![](/assets/images/2025/govuk-app-analytics-thumbnail.jpg)](/assets/images/2025/govuk-app-analytics.jpg) | [![](/assets/images/2025/govuk-app-linking-thumbnail.jpg)](/assets/images/2025/govuk-app-linking.jpg) | [![](/assets/images/2025/govuk-app-passportreading-thumbnail.jpg)](/assets/images/2025/govuk-app-passportreading.jpg) | [![](/assets/images/2025/govuk-app-reviewprompt-thumbnail.jpg)](/assets/images/2025/govuk-app-reviewprompt.jpg) |

### Preparing app

Once the app is installed, a remarkably smooth process kicks off! I've verified my identity with at least 4-5 services (banks etc) via my phone, and the quality varies dramatically. This was easily the best.

First up, we get a prompt to share analytics. The rationale before displaying the prompt is very neutral, with both options progressing to the next screen.

On the next screen, we _somehow_ link the app to our previous web session on a PC. The app opens a new tab in your browser with a single "Link app to continue" button, taking you back into the app. I believe this does something very clever, depending on whether it has managed to figure out where you came from:

1. If you **have** downloaded the app via GOV.UK's QR code, I noticed some IDs in the referral URL. I assume this is attribution data, containing information about my account. Once back in the app, I can progress.
2. If you **haven't** downloaded the app via GOV.UK's QR code, the site itself looks identical, but once back in the app you need to scan a QR code (presumably with the same attribution info). I assume once "linked", the rest of the flow is identical.

### Passport verification

Next up, taking a photo of the passport. Although hard to describe, this was the best passport scanner I've used! It displayed a real-time overlay of the data (e.g. name) it had managed to read, and was very forgiving with working out where the edges of the passport where. It also didn't mess around with taking a photo then scanning it, asking if I wanted to retake etc, it just looked at it in real-time and we're done!

Then, the biometric data needs scanning via NFC. Whilst I have seen this particularly trick before, I really liked that the app showed me the scanned data once it was done as reassurance. I didn't know it was possible to pull my photo in high quality directly from my passport, if so it explains why passport NFC & face scan is enough for third party identity verification.

### Face verification

Now I need to verify that my passport face is the same as... my actual face. This step fails around half the time for me (including at airport passport gates!), due to non-humans being confused by my appearance changing since my 5-6 year old passport picture:

1. I had typical length hair then, shaved head now.
2. I was clean-shaven then, beard now.
3. I've aged 5-6 years, unsurprisingly!

This scan was different to usual, with no silly phrases / head moving, and instead flashing a series of lights on my face. As with the passport scan, it did an interesting overlay of my features (although all I could really see was facial hair!), providing a little reassurance that it's working as expected.

### Verified

All done! The app can now be uninstalled and presumably never used again, but I was surprised they had a review prompt for a one-time use app (I [added it to an app recently](https://blog.jakelee.co.uk/play-store-rating-prompt/) and it massively boosted rating). This really highlights how high quality the app is, with even this entirely optional bonus feature being implemented. The app would have exactly as many users if the store rating was 1/5 or 5/5 since it is a legal requirement, yet the effort has been made to earn a high rating (4.7). Very impressive.

Now, back to the web for a few final pieces.

## Finishing up (web)

- Back to PC, automatically updated (image 7)
  - Enter address, date moved
  - Experian credit check (image 8)
  - All done (image 9)
- Services available: https://www.gov.uk/using-your-gov-uk-one-login/services
- Finished account (image 10)

## Engineering notes

## Other notes

- Tone of voice is confident, reassuring

## Conclusion

[![](/assets/images/2024/example_thumbnail.png)](/assets/images/2024/example.png)
