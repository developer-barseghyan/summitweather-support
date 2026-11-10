---
layout: default
title: Mountain Weather: Summit Help
permalink: /
sw_section: help
---

# Mountain Weather: Summit help

**Mountain Weather: Summit** tells you what the weather will be along your climb, at every elevation of the route, at the hour you will actually be there. You pick a start point and a summit (or import a GPX track), set a departure time and pace, and the app draws the mountain in 3D with the cloud base, the freezing line, the sun and the wind for any hour you choose. Then it answers the question every hiker asks: **will the summit be clear when I get there?**

All the terrain and route maths happens on your iPhone. Forecasts come from a public weather service, one request per elevation step of your route. There is no account, and your plans stay on the device.

Questions and bug reports go to [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com).

## What this app cannot know

> The forecast is a weather model, downscaled to a 30 m terrain model. Models in most mountain ranges have a grid of 7 to 9 km, so a narrow valley or a single ridge can behave differently from what the app shows. Mountain weather can change faster than any model.
>
> The terrain model is bare earth with one height sample roughly every 30 m. It has **no snow cover, no trees and no buildings**, and it smooths sharp summits by some metres.
>
> Treat every screen as a planning aid. Check the official mountain forecast and warnings for your area, and turn back when the mountain tells you to, not the phone.

## Plan a climb in four steps

1. **Pick the start and the summit.** On the Plan tab, tap **Start** and then the map (or use your location), tap **Summit** and then the peak, or type its name into **Search a peak**. **Peaks near you** lists the highest summits within 30 km. Pro users can also **Import GPX** or open a GPX file from Files, Mail or AirDrop.
2. **Shape the route if you like.** The default route is a straight line. Tap **Bend** and drag to add waypoints, or tap **Suggest route** for a slope-aware path across the terrain. It is a suggestion, not a trail.
3. **Set departure and pace.** Choose the date and time you leave and one of three paces (Easy, Normal, Fast). The card shows distance, ascent, time up and your summit ETA.
4. **Tap Show weather on the mountain.** The app downloads the terrain and the forecast for your route (a few hundred kilobytes) and opens the Mountain tab.

## The Mountain tab

The 3D view looks up-slope from your start towards the summit. Drag to orbit, pinch to zoom, and tap the target button to return to the framed view.

- **Elevation cards** sit beside the route. Each shows an elevation, the time you reach it, the temperature (blue when it is at or below 0°), the wind and a one-word condition for the hour on the slider.
- **Cloud deck.** A translucent grey plane sits at the forecast cloud base. If the summit is above it, you will have a view. If the plane cuts through the mountain below the summit, the top is in cloud.
- **Freezing line.** The terrain above the hour's 0° level is tinted cold blue.
- **Sun and shadow.** The light on the terrain follows the real sun for the slider hour. At night the scene darkens.
- **Wind arrows** appear on exposed ridges and point downwind.
- **Time slider.** Drag it through the day. Markers show your start, summit ETA, return and sunset. Day chips above it switch to another day of the week.
- The line at the bottom says when the forecast was fetched. The ⓘ button opens the data sources and the full disclaimers.

## The Profile tab

The chart draws your route's elevation against distance and colours each stretch with the weather **at the hour you pass it**: green for clear, blue for rain, pale grey-blue for snow, grey for cloud. A dashed blue line is the 0° level; a grey line is the cloud base; a red dashed line marks where a storm risk begins.

Below the chart, the steps along the route carry notes such as "Rain turns to snow here", "Sun on this slope from 08:10" or "Wind chill −18°, be below 3 500 m by 13:00". Gusts marked with an asterisk are estimated from the mean wind (see *Accuracy* below).

The share button at the top exports a one-page **PDF report** (Pro) with the chart, the step table, the verdict and the data sources.

## The Verdict tab

One plain answer for your plan: **clear**, **in cloud**, **storm risk**, **high wind** or **extreme cold**, with two or three lines of why (cloud base trend, freezing level, storm hour, summit wind). Under it: the **turnaround time**, which is one hour before the first storm-risk hour at the summit or late enough to get down before dark, whichever is earlier, and the daylight left after the summit.

**This week at the summit** shows the verdict for each of the next seven days at your departure time. Tap a day to recompute the whole plan for it. The **best window** (Pro) names the clearest stretch of hours in the week.

**Alert me when the forecast changes** (Pro) checks the summit a few times a day, when iOS allows it, and sends a notification when the verdict changes or a storm or high-wind hour appears within 48 hours. iOS decides when background checks run, so this is a convenience, not a guarantee.

## Accuracy and gaps in the data

Weather model
: Forecasts come from MET Norway's Locationforecast service. Inside the Nordic countries it uses a 2.5 km model; elsewhere it uses the global ECMWF model at about 9 km. The app asks for each point at its true elevation and interpolates between points along your route. Hourly values cover about the first two days; after that the model steps every six hours, and the app fills the hours in between and shows them lighter.

Gusts and probabilities
: Outside the Nordic area the service provides no gust speed and no rain or thunder probability. The app estimates gusts as 1.5 × the mean wind and marks them with an asterisk. Storm risk relies on the model's thunder symbols, so it is a hint, not a count.

Cloud base
: Computed from temperature and dew point at each elevation step and combined with the model's low-cloud cover. Expect it to be right to a few hundred metres, not tens.

Terrain
: Samples lie about 30 m apart. For most land the height error stays under 16 m; sharp summits are smoothed by 10 to 30 m. The app uses the terrain for the 3D view, the route profile, the true sunrise on each slope and the exposure of ridges.

## Units, offline use and saved plans

- Metric or imperial in **Settings**; the default follows your region.
- A plan you have shown once is saved. With Pro, every plan is stored for **offline** use: terrain and forecast reopen without a signal, and the Mountain tab says how old the forecast is. Free users keep their latest plan, which reopens from the ordinary cache while iOS keeps it.
- Plans stay on this iPhone. There is no sync between devices in version 1.0.

## Free features and Pro

Free for everyone: the 3D mountain, the profile and the verdict for one saved plan, with forecasts up to 48 hours ahead.

Pro adds:

- forecasts for the full range the model provides (about 9 days), so the week strip and the **best window** work;
- as many saved plans as you like;
- **GPX import**;
- **forecast change alerts** for the summit;
- **offline** terrain and forecast for every saved plan;
- the one-page **PDF report**.

US pricing: **$14.99 once for lifetime access**, or **$9.99 per year**. The app shows the price in your local currency before you pay. There is no free trial.

On a new phone, open **Settings** and tap **Restore purchases** while signed in with the Apple Account that paid. The same link sits at the foot of the Pro screen. The yearly plan is managed in your Apple Account settings, not inside the app.

## Reporting a forecast that seems off

Email me and attach:

1. A screenshot of the Verdict tab and of the Profile tab for the plan.
2. The start and summit coordinates (or the GPX), the departure time and the pace you chose.
3. What you actually met on the mountain, with the time, and your source if it was another forecast or a weather station.

Three causes come up most often. The model grid is coarse, so a local inversion or valley cloud may be missing. The departure time or pace may put you at a point an hour earlier or later than you really were, and the weather moved in that hour. Or the summit's true height differs from the terrain model, which shifts the freezing-line and cloud-base comparison.

## Data sources

Weather: MET Norway Locationforecast 2.0 (CC BY 4.0). Elevation: AWS Open Data Terrain Tiles, the Mapzen merge of SRTM, GMTED2010, ETOPO1, USGS NED and other public sources. Map: Apple Maps.
