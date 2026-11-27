---
layout: default
title: Mountain Weather: Summit Privacy Policy
permalink: /privacy
sw_section: privacy
---

# Privacy Policy

App: **Mountain Weather: Summit** for iPhone<br>
Published by: Tigran Barseghyan<br>
Effective from: 27 November 2026<br>
Questions: [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com)

This page follows each path that data can take inside the app. I run no server for it and I receive nothing from it. No personal data about you reaches me.

## Data flows at a glance

| Flow | Leaves the iPhone? | Who receives it |
|---|---|---|
| Your position | Only when you set a start from it, see 1 | MET Norway (rounded coordinates), Amazon Web Services (tile numbers), Apple (place name) |
| Weather requests | Yes: coordinates and elevation of your route points | MET Norway (Norwegian Meteorological Institute) |
| Terrain tile downloads | Yes, tile numbers only | Amazon Web Services (AWS Open Data) |
| The map view, place names and Apple Maps search | Yes, through iOS | Apple |
| Peak suggestions while you type, peaks near you | No, from an index on the phone | Nobody |
| Pro purchases | Yes, through iOS | Apple |
| Notifications | No, created on the phone | Nobody |
| GPX files you import | No | Nobody |
| PDF reports you export | Only where you send them | The app or person you pick |
| Usage statistics | Not gathered | Nobody |

## 1. Your position

Your location is used only when you ask for it: to centre the map, set a start or find peaks near you. A start you set from it is saved in your plan on this phone and sent, as coordinates, to the forecast service.

You ask for it on the Plan tab, with the location button, **Start at my location**, **Use my location** or **Peaks near you**. Opening the app or picking a summit does not read your position, even when you have allowed location. Once you have asked, Apple Maps shows you on the Plan tab's map until you close the app; the app keeps the position you asked for in memory until then, and uses it on the phone for the distances in the peak search and to offer **Use my location** for a summit within 50 km. You can say no to location, or switch the permission off later in iOS Settings; then you place the start by tapping the map, and everything else works the same.

The app never sets a start by itself. A start you set from your position, with **Start at my location** or **Use my location**, is a point of your plan like any other:

- it is saved in the plan on this phone when you show the plan's weather;
- its coordinates, rounded to four decimals, go to MET Norway in the forecast requests (section 2);
- it reaches the terrain tile server only as the number of the tile it lies in (section 3);
- its coordinates go to Apple when you set it, to look up the place's name (section 4).

Your position is not stored or sent otherwise. The location button only moves the map: the app sends your position to no one for it, and Apple Maps loads the area it then shows, as for any part of the map. Finding peaks near you and measuring distances happen on the phone.

## 2. Weather requests

To forecast your route, the app sends one request per point of the route (up to 40 points, about one per 150 m of climb or 500 m of trail; points within 300 m and 100 m of height of each other share one request) to MET Norway's public Locationforecast service at `api.met.no`. Each request carries the point's latitude and longitude, rounded to four decimal places (about 11 m), and its elevation. If your start was set from your location, that rounded position is among them. The requests also carry a plain app identifier as the User-Agent and, as with any web request, your IP address. The app adds no identifier for you, and MET Norway cannot tell which requests belong to the same person beyond what any web server sees. MET Norway's own terms and privacy policy govern what its servers log.

Because route coordinates may include your position, the App Store privacy label for the app lists **Location** as collected for app functionality, **not linked to you** and **not used for tracking**.

Forecast responses are cached on the phone so that the app can reopen a plan without a new request and respect the service's rate limits. The app makes no weather requests while it is in the background, except the alert check described in section 6.

## 3. Terrain tile downloads

The 3D mountain and the route profile need ground heights. The app fetches them from the public AWS Open Data Terrain Tiles bucket (`s3.amazonaws.com/elevation-tiles-prod`). Each request names a tile by its grid numbers; a tile covers a patch of several kilometres, not an exact point. Nothing is fetched before you have set both a start and a summit: then the tiles along the route are, and the rest when you show the route's weather. The request carries the same plain User-Agent and your IP address. Amazon's own policies decide what its servers log.

Downloaded heights stay in the app's cache so that the next plan and offline use need no fresh download. The three demo routes ship with their terrain inside the app.

## 4. The map view, place names and search

The map on the Plan tab is Apple Maps, drawn by iOS. Peak suggestions as you type come from an index stored on the phone and send nothing. Apple's place search runs only when you ask for it (**Search Apple Maps**, or Return when no peak matches); it receives the text you typed and the part of the map you are looking at. When you set a start or a summit, the app asks Apple for the place's name and time zone, with that point's coordinates. Apple handles these requests under its own privacy policy.

## 5. Pro purchases

Buying, renewing and restoring Pro run through Apple's StoreKit. Apple handles your payment and your Apple Account. I see no card details and no name. The app only learns from iOS whether Pro is active on the device.

## 6. Forecast change alerts

If you turn alerts on (Pro), the app watches your latest plan. iOS may wake the app a few times a day; iOS decides how often. The app then fetches the forecast for each point of that plan's route, the same requests as when you open the plan (section 2), works out the verdict as the app does, compares it with the last check, and shows a local notification when the verdict changes or a storm or high-wind hour appears at the summit within 48 hours. The notification is created on the phone; no notification service outside Apple's iOS is involved, and nothing about it is sent to me.

## 7. Files you import and export

GPX files you open in the app are read on the phone. The app keeps the track it needs with the plan and copies the file nowhere else.

A PDF report that you export goes only where you send it with the iOS share sheet. It contains your route's coordinates, elevations, times and the forecast. Share it with the same care as any location data.

## 8. What sits in the app's storage

- Saved plans: start and summit points, waypoints or the imported track, departure time, pace and settings.
- Cached terrain heights and forecast responses, and, for Pro users, the offline copy of each plan.
- Your settings: units, pace defaults, terrain exaggeration, alert choice.
- Crash and hang diagnostics that iOS gives the app are kept on the phone only, and are shared solely when you export them yourself from Settings → Help → Export diagnostics.

Removing the app from the phone erases all of this. Your normal iCloud or computer backup of the iPhone may contain this storage, as it would for any app.

## 9. Measurement and tracking

Version 1.0 has no analytics and no ad network. It has no account or sign-in and never asks for your email address. It does not follow you across other apps or websites, so it has no reason to show the App Tracking Transparency prompt. No data is sold, rented or handed to anyone.

Crash reports. iOS may hand the app a crash or hang report after the fact (Apple's MetricKit). The app stores it on your phone and nowhere else. It is shared only if you export it yourself from Settings → Help → Export diagnostics. No third-party crash reporter or analytics service is used.

If a later version ever adds analytics, this page and the App Store label will both be updated before that version is released.

## 10. Young users

The app is made for a general audience and does not target children under 13. It gathers no personal data from anyone of any age.

## 11. Questions and requests

I hold no record about you, so I have nothing to show, fix or erase on request. Your data lives on your iPhone, and you control it there. For any privacy question, email [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com).

## 12. Revisions to this policy

A revised policy will appear at this address with a new effective date. Larger revisions will also be mentioned in the app's release notes.
