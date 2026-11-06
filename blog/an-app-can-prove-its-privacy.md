# An app can prove its privacy. Here's how to check ours.

Source: https://reground.pro/blog/an-app-can-prove-its-privacy/
Summary: 92% of depression apps studied sent data to a third party. App Store privacy labels are wrong most of the time. Here's the evidence, and a five-minute way to check any app yourself.

Essay 8 min read

Mental-health apps have earned distrust with data, not paranoia. Privacy promises are cheap, and even official App Store labels are often wrong. Verification beats trust. This essay shows the receipts on the industry, then shows you how to verify any app, including ours, in about five minutes.

## The record

Distrust of mental-health apps is not a vibe. It is a documented pattern, repeated across every independent audit anyone has run.

The category deserves more scrutiny than a shopping app, not less. A journal entry or a mood log sits closer to a medical record than to a shopping preference. It is easy to tie back to the person who wrote it, and that is exactly the data these audits went looking for.

In 2019, researchers tested 36 depression and smoking-cessation apps and watched what data actually left the phone. Thirty-three of them, 92%, transmitted user data to a third party.[1] Of the ones sharing with Google or Facebook specifically, only 59% disclosed that sharing anywhere in their privacy policy.[1] The same audit found that only 25 of the 36 apps, 69%, published a privacy policy at all.[1]

Ninety-two percent of the depression and smoking-cessation apps studied sent data to a third party. Fewer than six in ten of those bothered to say so.[1]

Mozilla ran a comparable test on the wellness category in 2022, checking 32 popular mental-health apps against its own privacy and security standards. Twenty-eight of them, 88%, earned Mozilla's *Privacy Not Included warning label.[2] Twenty-five of the 32, 78%, failed Mozilla's own Minimum Security Standards, meaning basics like encrypting data in transit weren't guaranteed.[2] The retest a year later found little had improved: of 27 apps reviewed both times, 8 got better and 17 got worse or stayed the same.[3]

Two of the largest platforms in the category have already paid for exactly this kind of behavior. BetterHelp paid the Federal Trade Commission $7.8 million in 2023 for sharing users' health questionnaires, and email and IP addresses, with Facebook, Snapchat, Criteo, and Pinterest for advertising.[4] Cerebral paid $7.1 million in 2024, after tracking pixels sent sensitive data on more than 3.1 million users to Snapchat, LinkedIn, and TikTok.[5]

None of this is abstract to the people the apps are for. In one survey of patients considering a mental-health app, 59.1% named data-privacy concerns as a reason they hesitated.[6] The distrust is earned, and it is costing the category the people it exists to help.

## Even the labels lie

Apple's App Store privacy label was supposed to fix this. It hasn't.

A 2024 audit of app privacy labels found that 97% of apps marked "Data Not Collected" had a privacy policy that said otherwise.[7] The same audit checked roughly 475,000 apps and found 228,000 of them, 48%, had a privacy policy suggesting more data collection than the label disclosed.[7] A separate study of iOS apps found 67% of privacy labels were inconsistent with what the app actually did.[8] The label you check before downloading is, most of the time, decorative.

That matters because the label is the only privacy information most people ever see. It sits right on the download screen, before the price, before the reviews, and it is designed to be read in three seconds and trusted. The research above says that trust is misplaced far more often than not.

Our own App Store label also says "Data Not Collected." Per that same research, that is exactly the kind of claim you should not take on faith, ours included. So don't. Check it yourself. Here's how.

## What proof looks like

A privacy policy is a promise. An architecture is a constraint, and constraints are provable in a way promises aren't.

Reground has no account, so there is no identity attached to what you write. It has no server of ours, so there is nothing of ours to breach. It carries no third-party SDKs, so no analytics company's code is running on your phone, phoning anything anywhere. Your journal, your mood log, your settings, all of it stays in on-device storage, full stop.

Each of those is a thing removed, not a feature added. No account means no sign-up screen and no password to leak. No server means no database anywhere with your name next to your entries. No SDKs means no advertising or analytics vendor sitting quietly inside the app, collecting whatever it's built to collect.

None of that is a claim about our intentions. A privacy policy describes intentions, and intentions can change, or lie, or simply be wrong, as the studies above show. An architecture describes what the software can physically do. Ours can't leak what it never touches.

## Check us. It takes five minutes

You don't have to take the paragraph above on faith. You can test it yourself, on your own phone, in about five minutes, with no special tools beyond your Settings app.

Four checks follow, from easiest to most technical. Do the first one even if you skip the rest, it alone rules out an entire category of hidden behavior.

Put your phone in airplane mode, then open the app. Write a journal entry, log a mood, run a breathing technique. Everything keeps working, including the journal, because there is no server to reach. A cloud-backed app can't fake that, it needs the network, and airplane mode removes it.

For a second look, open Settings → Privacy & Security → App Privacy Report and check Reground's network activity. The only domains you'll see are Apple's own App Store endpoints, logged when you make a purchase, nothing else.

If you know how to run a network proxy, mitmproxy or Charles both work, route the app's traffic through it. The only calls you'll capture are StoreKit's, Apple's own purchase framework. There is nothing else to see, because there is nothing else running.

And read the privacy policy itself. It's one page, because there's nothing to enumerate, no data categories, no third-party list, no retention schedule, because none of those things exist here.

None of these checks require trusting our word for anything. Airplane mode is a fact about physics, not a promise. A network log either shows a call or it doesn't. A one-page policy is either short because there's nothing to say, or it's hiding something behind vague language, read it and judge for yourself.

Run the same four checks on any wellness app already on your phone, including ones you pay for. Most will fail the first one before you finish reading this sentence.

## The honest limits

None of this is unlimited proof, and pretending otherwise would undercut everything above.

Apple sees that you bought the app. StoreKit is Apple's payment rail, not ours, and that transaction is genuinely outside our reach. If you back up your phone to iCloud, that backup includes our local data too, governed by your iCloud settings, not by any promise of ours. And "no analytics" cuts both ways: we don't know how many people use Reground, which techniques help, or where anyone gets stuck. That is a real cost, and we accept it, because the alternative is knowing by watching you.

Saying this plainly is what makes the rest of this essay worth anything. A company that only tells you what makes it look good is doing marketing. This is an attempt at something else.

It also shapes how we build. Without usage data, we can't quietly A/B-test a paywall or watch a drop-off funnel and optimize against it. Decisions get made from what people tell us directly, in reviews and emails, which is slower and noisier than a dashboard, and the trade we chose on purpose.

The point of this essay was never only Reground. Run any wellness app on your phone through the same four checks: airplane mode, the App Privacy Report, a proxy if you have one, and an honest read of the policy. An app that survives all four has earned something a label can't fake.

A disclosure, kept to the end on purpose: we make [Reground](https://reground.pro/). Treat everything above as testimony, not neutral reporting, which is exactly why this essay spent its length showing you how to check it yourself, instead of asking you to believe it. Our App Store label happens to say "Data Not Collected" honestly. Read the [privacy policy](https://reground.pro/privacy) yourself, then decide.

## Sources

1. [Data sharing and privacy practices of smartphone apps for depression and smoking cessation, JAMA Network Open, 2019.](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2730782)
2. [*Privacy Not Included: mental health apps review, Mozilla Foundation, 2022.](https://www.mozillafoundation.org/en/blog/shady-mental-health-apps-inch-toward-privacy-and-security-improvements-but-many-still-siphon-personal-data/)
3. [Are mental health apps better or worse at privacy in 2023? Mozilla Foundation, 2023.](https://www.mozillafoundation.org/en/privacynotincluded/articles/are-mental-health-apps-better-or-worse-at-privacy-in-2023/)
4. [FTC final order banning BetterHelp from sharing sensitive health data for advertising, Federal Trade Commission, 2023.](https://www.ftc.gov/news-events/news/press-releases/2023/07/ftc-gives-final-approval-order-banning-betterhelp-sharing-sensitive-health-data-advertising)
5. [FTC proposed order prohibiting Cerebral from using or disclosing sensitive data, Federal Trade Commission, 2024.](https://www.ftc.gov/news-events/news/press-releases/2024/04/proposed-ftc-order-will-prohibit-telehealth-firm-cerebral-using-or-disclosing-sensitive-data)
6. [Data-privacy concerns as a barrier to mental health app use, patient survey, JMIR Mental Health, 2019.](https://mental.jmir.org/2019/1/e11334/)
7. [Honesty is the best policy: comparing App Store privacy labels against privacy policies, Proceedings on Privacy Enhancing Technologies Symposium, 2024.](https://arxiv.org/abs/2306.17063)
8. [Audit of iOS privacy label accuracy across 5,102 apps, Proceedings on Privacy Enhancing Technologies Symposium, 2023.](https://crysp.petsymposium.org/popets/2024/popets-2024-0111.pdf)

iOS verification steps described above use Settings → Privacy & Security → App Privacy Report, available on iOS 15.2 and later.

Sources reviewed · July 2026

Check ours the way this page describes.

No account, no analytics, no network calls to audit. Install it, open the App Privacy Report, and watch it stay empty.

Free to try. $5.99 once for all 22 techniques, no subscription.

[Download Reground on the App Store](https://apps.apple.com/app/id6790840763)

---

Reground is a self-care toolkit, not medical care. If you're struggling, a mental-health professional can help in ways an app can't. If you're in crisis, contact your local emergency number.
