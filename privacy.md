---
layout: default
title: Mountain Weather: Summit Privacy Policy
permalink: /privacy
sw_section: privacy
---

# Privacy Policy

App: **Mountain Weather: Summit** for iPhone<br>
Published by: Tigran Barseghyan<br>
Effective from: 10 November 2026<br>
Questions: [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com)

This page follows each path that data can take inside the app. I run no server for it and I receive nothing from it. No personal data about you reaches me.

## Data flows at a glance

| Flow | Leaves the iPhone? | Who receives it |
|---|---|---|
| Your position | Only as route coordinates, see 1 and 2 | MET Norway (weather requests) |
| Weather requests | Yes: coordinates and elevation of your route points | MET Norway (Norwegian Meteorological Institute) |
| Terrain tile downloads | Yes, tile numbers only | Amazon Web Services (AWS Open Data) |
| The map view and peak search | Yes, through iOS | Apple |
| Pro purchases | Yes, through iOS | Apple |
| Notifications | No, created on the phone | Nobody |
| GPX files you import | No | Nobody |
| PDF reports you export | Only where you send them | The app or person you pick |
| Usage statistics | Not gathered | Nobody |

## 1. Your position

If you allow it, the app reads your location to set the start point of a plan where you stand and to list peaks near you. It reads location only while the app is in use. You can say no, or switch the permission off later in iOS Settings; then you place the start by tapping the map, and everything else works the same.

Your position is not stored by itself. It becomes the start point of a plan only when you choose that, and it then travels with the plan as described in section 2.

## 2. Weather requests

To forecast your route, the app sends one request per elevation step of the route (typically 8 to 15 points) to MET Norway's public Locationforecast service at `api.met.no`. Each request carries the point's latitude and longitude, rounded to four decimal places (about 11 m), and its elevation. If your start point is your current location, that rounded position is among them. The requests also carry a plain app identifier as the User-Agent and, as with any web request, your IP address. The app adds no identifier for you, and MET Norway cannot tell which requests belong to the same person beyond what any web server sees. MET Norway's own terms and privacy policy govern what its servers log.

Because route coordinates may include your position, the App Store privacy label for the app lists **Location** as collected for app functionality, **not linked to you** and **not used for tracking**.

Forecast responses are cached on the phone so that the app can reopen a plan without a new request and respect the service's rate limits. The app makes no weather requests while it is in the background, except the one summit check described in section 6.

## 3. Terrain tile downloads

The 3D mountain and the route profile need ground heights. The app fetches them from the public AWS Open Data Terrain Tiles bucket (`s3.amazonaws.com/elevation-tiles-prod`). Each request names a tile by its grid numbers; a tile covers a patch of several kilometres, not an exact point. The request carries the same plain User-Agent and your IP address. Amazon's own policies decide what its servers log.

Downloaded heights stay in the app's cache so that the next plan and offline use need no fresh download. The three demo routes ship with their terrain inside the app.

## 4. The map view and peak search

The map on the Plan tab is Apple Maps, drawn by iOS. Typing a peak name uses Apple's place search. Apple handles those requests under its own privacy policy.

## 5. Pro purchases

Buying, renewing and restoring Pro run through Apple's StoreKit. Apple handles your payment and your Apple Account. I see no card details and no name. The app only learns from iOS whether Pro is active on the device.

## 6. Forecast change alerts

If you turn alerts on for a plan (Pro), iOS wakes the app a few times a day. The app then fetches the forecast for the plan's summit point only, compares it with the last check, and shows a local notification when the verdict changes or a storm or high-wind hour appears within 48 hours. The notification is created on the phone; no notification service outside Apple's iOS is involved, and nothing about it is sent to me.

## 7. Files you import and export

GPX files you open in the app are read on the phone. The app keeps the track it needs with the plan and copies the file nowhere else.

A PDF report that you export goes only where you send it with the iOS share sheet. It contains your route's coordinates, elevations, times and the forecast. Share it with the same care as any location data.

## 8. What sits in the app's storage

- Saved plans: start and summit points, waypoints or the imported track, departure time, pace and settings.
- Cached terrain heights and forecast responses, and, for Pro users, the offline copy of each plan.
- Your settings: units, pace defaults, appearance, alert choice.

Removing the app from the phone erases all of this. Your normal iCloud or computer backup of the iPhone may contain this storage, as it would for any app.

## 9. Measurement and tracking

Version 1.0 has no analytics, no crash reporter and no ad network. It has no account or sign-in and never asks for your email address. It does not follow you across other apps or websites, so it has no reason to show the App Tracking Transparency prompt. No data is sold, rented or handed to anyone.

If a later version ever adds analytics, this page and the App Store label will both be updated before that version is released.

## 10. Young users

The app is made for a general audience and does not target children under 13. It gathers no personal data from anyone of any age.

## 11. Questions and requests

I hold no record about you, so I have nothing to show, fix or erase on request. Your data lives on your iPhone, and you control it there. For any privacy question, email [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com).

## 12. Revisions to this policy

A revised policy will appear at this address with a new effective date. Larger revisions will also be mentioned in the app's release notes.
