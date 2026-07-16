# The pixel in the waiting room

In June 2022 the investigative newsroom The Markup
[found the Meta Pixel on the websites of 33 of the top 100 hospitals in the US](https://themarkup.org/pixel-hunt/2022/06/16/facebook-is-receiving-sensitive-medical-information-from-hospital-websites),
sending details of patients' appointments to Meta. Inside the password-protected patient
portals of seven health systems, the same tool was collecting data on prescriptions,
conditions, and sexual orientation.

## What a pixel does

The Meta Pixel is a small piece of code a website adds so it can measure how its adverts
perform. It reports a visitor's actions back to Meta, tied where possible to that person's
Facebook identity. On a shopping site the reported action is a purchase. On a hospital
booking page it is the scheduling of a doctor's appointment, and the tracker sent Meta a
packet of data the moment the button was clicked.

## The fallout

Within months of the reporting, at least 28 hospitals removed the pixel or blocked it from
sending patient information. Class action lawsuits followed, and former regulators told the
newsroom the arrangement may have breached US health-privacy law. The hospitals
had installed the code themselves, for ordinary marketing reasons, without evident awareness
of what it was carrying out of the building.

## The pattern

This is the [invisible third party](../attacks.md) at work, and the [browser
vector](../vectors.md) at its plainest. The hospital was the [first-party
collector](../adversaries.md), the on-ramp; the party receiving the medical data was one the
patient had never chosen and could not see.

Last reviewed: 2026-07-16.
