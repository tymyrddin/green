# Flo: the cycle shared with strangers

In 2021 the US Federal Trade Commission
[settled with Flo Health](https://www.ftc.gov/news-events/news/press-releases/2021/06/ftc-finalizes-order-flo-health-fertility-tracking-app-shared-sensitive-health-data-facebook-google),
maker of a period- and fertility-tracking app used by more than a hundred million people,
after finding it had shared users' sensitive health data with Facebook, Google, and other
marketing and analytics firms while promising to keep that data private. The practice was
first exposed by a Wall Street Journal investigation in 2019.

## What left the app

When a user recorded a period or entered that she was trying to conceive, the app could pass
that event to its outside partners, tied to identifiers that let those firms recognise the
same person elsewhere. A menstrual cycle and an intention to become pregnant are about as
intimate as everyday data gets, and they were moving to companies the user had no dealing
with, for purposes the privacy policy had ruled out.

## A settlement without a fine

The order carried no monetary penalty. It required Flo to obtain affirmative consent before
sharing health information, to tell affected users what had happened, and to instruct the
third parties that had received the data to destroy it. Whether data can truly be recalled
once it has been matched and copied is a separate question the order could not answer.

## The pattern

Reproductive data is the sharpest form of the [inferred or collected sensitive
attribute](../objectives.md), and the route out was the [invisible third party](../attacks.md):
analytics code inside the app, gathering under the app's name and reporting elsewhere. A tool
for tracking a body became a feed for the ad market.

Last reviewed: 2026-07-16.
