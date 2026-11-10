<div align="center">

<p align="center">
  <img src="./parth-animated-hud.svg" width="100%" alt="Parth Khansali: animated developer HUD" />
</p>

# Parth Khansali

### `CSE STUDENT` · `NATIVE &amp; FULL-STACK BUILDER` · `SYSTEMS &amp; SIMULATION`

<p align="center">
  <b>Parth Khansali</b> (@ParthKhansali) · Computer Science &amp; Systems Developer · Dehradun, India
</p>

<br/>

<a href="https://github.com/ParthKhansali">
  <img src="https://img.shields.io/badge/GitHub-061008?style=for-the-badge&logo=github&logoColor=39ff6a" alt="GitHub" />
</a>
&nbsp;
<a href="https://www.linkedin.com/in/parth-khansali/">
  <img src="https://img.shields.io/badge/LinkedIn-061008?style=for-the-badge&logo=linkedin&logoColor=39ff6a" alt="LinkedIn" />
</a>
&nbsp;
<a href="mailto:parthkhansali@gmail.com">
  <img src="https://img.shields.io/badge/Email-061008?style=for-the-badge&logo=gmail&logoColor=39ff6a" alt="Email" />
</a>
&nbsp;
<a href="https://www.parthkhansali.tech/">
  <img src="https://img.shields.io/badge/Portfolio-061008?style=for-the-badge&logo=safari&logoColor=39ff6a" alt="Portfolio" />
</a>

<br/><br/>

<p align="center">
  <img src="./terminal-neofetch.svg" width="100%" alt="Parth Terminal Neofetch Telemetry" />
</p>

<p align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</p>

</div>

## `whoami`

> *"I build software that makes complicated things feel simple."*

I'm **Parth**, a third-year Computer Science student at **Graphic Era Hill University** (Class of 2028) in Dehradun, India.

When something doesn't work the way I think it should, my first instinct is to pull it apart, understand the internals, and see if I can make it better. What excites me isn't checking off framework boxes. I like tackling problems where the plumbing underneath is complex, but the product in the user's hand feels effortless.

That spans low-level native macOS networking in **Netwich**, designing campus-wide mobile systems in **GEHU Connect**, and running scientific simulations or geospatial pipelines for hackathons (**Project Aranya**, **MeghaVyuha**, and **ORVESS-PAT**).

Beyond code, I value clear communication. Leading my university's Model UN club as Director General taught me how to debate, organize teams, and explain technical ideas without hiding behind buzzwords.

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `systems.featured`

<div align="center">
  <img src="./netwich-schematic.svg" width="100%" alt="Netwich Architecture Schematic" />
</div>

<br/>

<table>
<tr>
<td width="50%" valign="top">

### `01` · <a href="https://www.parthkhansali.tech/projects/gehu-connect/">GEHU Connect</a>

**Sole Flagship · Campus Ecosystem Mobile Platform** · `[STATUS: IN TESTING]`

A student-first mobile platform bringing campus life into one unified space: peer community networking, academic resources, a student marketplace, and campus housing discovery.

**Technical Architecture:**
* React Native and Expo Router client with Redux Toolkit Query caching and SecureStore token handling.
* Java 21 / Spring Boot 3.5.9 REST backend with JWT authentication, PostgreSQL persistence, and STOMP WebSockets.
* Direct-to-Cloudflare R2 presigned object uploads via AWS SDK `S3Presigner` to keep media bytes off API worker threads.
* Layered L1 Caffeine + L2 Redis permission cache with stampede locks designed for spotty campus connectivity.

`React Native` `Expo` `Java` `Spring Boot` `Redis` `Cloudflare R2` `STOMP WebSockets`

<details>
<summary><b>View Engineering Deep Dive</b></summary>
<br/>
Organized around high-frequency student workflows: Home, Academics, Marketplace, Housing, and Profile. Built with bounded upload concurrency, layered caching, and session-scoped STOMP WebSocket auth. Source code is private; see the full architecture breakdown on <a href="https://www.parthkhansali.tech/projects/gehu-connect/">parthkhansali.tech</a>.
</details>

</td>
<td width="50%" valign="top">

### `02` · <a href="https://github.com/ParthKhansali/Netwich">Netwich</a>

**Native macOS Multi-Interface Network Utility** · `[STATUS: COMPLETED & RELEASED v0.1.0]`

Netwich is a lightweight Mac utility that distributes network traffic across multiple active connections (Wi-Fi, Ethernet, and phone USB tethering) and accelerates compatible downloads through parallel byte-range requests.

**Technical Architecture:**
* Discovers and monitors physical Darwin network interfaces dynamically (`en0`, `en4`, `en5`).
* Binds outbound TCP sockets to specific interfaces on macOS via `IP_BOUND_IF`.
* Maintains interface-scoped routes and EWMA link health scoring so tethering stays usable alongside Wi-Fi.
* Slices compatible downloads into concurrent byte-range chunks with graceful single-stream fallback.
* Native SwiftUI interface communicating through a local `127.0.0.1:1080` SOCKS5 proxy and browser extensions (`31` passing unit tests).

`Swift 6` `SwiftUI` `Darwin Networking` `IP_BOUND_IF` `SOCKS5`

<details>
<summary><b>View Releases &amp; Engineering Deep Dive</b></summary>
<br/>
Download <a href="https://github.com/ParthKhansali/Netwich/releases">Netwich v0.1.0 DMG &amp; Extensions</a> or read the <a href="https://www.parthkhansali.tech/projects/netwich/">case study on parthkhansali.tech</a>. On macOS, default routing tables funnel traffic through a single primary adapter; Netwich binds individual outbound streams onto specific interfaces without cloud relays.
</details>

</td>
</tr>
</table>

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `applied.intelligence & simulation`

<div align="center">
  <img src="./hackathon-telemetry.svg" width="100%" alt="Active Hackathon Telemetry" />
</div>

<br/>

<table>
<tr>
<td width="50%" valign="top">

### `03` · <a href="https://github.com/ParthKhansali/Project-Aranya">Project Aranya</a>

**Geospatial Wildlife Intelligence Platform** · `Ongoing Hackathon Project`

Geospatial decision-support platform for India focused on exploring human-wildlife conflict zones, movement corridors, and conservation hotspots across Uttarakhand's Rajaji and Corbett pilot landscape.

* Built on a CesiumJS 3D globe centered on India and Uttarakhand pilot corridors.
* Combines modular spatial layers, Mapbox Vector Tiles, and NASA GIBS MODIS NDVI canopy overlays.
* Breaks down risk zones transparently by corridor proximity, sightings recency, and habitat fragmentation.
* Links: <a href="https://project-aranya.vercel.app">Live Prototype</a> · <a href="https://www.parthkhansali.tech/projects/aranya/">Case Study</a>

`JavaScript` `CesiumJS` `Vite` `Vector Tiles` `Geospatial Data`

</td>
<td width="50%" valign="top">

### `04` · <a href="https://github.com/ParthKhansali/MeghaVyuha">MeghaVyuha</a>

**Weather Prediction Error Atlas & Analytics** · `Ongoing Hackathon Project (SIH26080)`

An interactive Error Atlas prototype investigating patterns where numerical monsoon rainfall forecasts diverge across synoptic regimes and Indian terrain.

* Next.js 15, React 19, deck.gl, and MapLibre GL forecast verification workspace.
* Compares candidate post-processing baselines (Raw NWP, Hurdle, CSG-EMOS) with an explicit Evidence Trace.
* Research prototype exploring complex discrepancy surfaces, not a replacement for operational weather advisories.
* Links: <a href="https://meghavyuha.vercel.app">Live Prototype</a> · <a href="https://www.parthkhansali.tech/projects/meghavyuha/">Case Study</a>

`Next.js 15` `TypeScript` `deck.gl` `MapLibre GL` `Python`

</td>
</tr>

<tr>
<td colspan="2" valign="top">

### `05` · <a href="https://www.parthkhansali.tech/projects/orvess-pat/">ORVESS-PAT</a>

**FSOC Coarse Pointing, Acquisition & Tracking Simulation** · `Ongoing Research Prototype (SIH26169)`

An ongoing Python simulation prototype in the Free Space Optical Communications (FSOC) coarse pointing, acquisition, and tracking domain.

* Models a 640x480 focal-plane array, optical attenuation/noise, sub-pixel centroiding, and an Adaptive-R Extended Kalman Filter.
* PySide6 + PyQtGraph desktop workbench comparing Baseline vs. Adaptive tracker configurations side by side.
* Synthetic simulation workbench built for repeatable experiments, not tested on physical laser bench hardware.

`Python 3.10+` `PySide6` `PyQtGraph` `NumPy` `SciPy` `OpenCV`

</td>
</tr>
</table>

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `tech.arsenal`

<p align="center">
  <img src="https://skillicons.dev/icons?i=swift,java,python,cpp,ts,js,react,nextjs,spring,nodejs,postgres,mongodb,mysql,aws,cloudflare,firebase,git,figma&theme=dark" alt="Tech Stack Icons" />
</p>

```text
SYSTEMS & NATIVE      Swift 6, SwiftUI, macOS Darwin Networking, IP_BOUND_IF, SOCKS5
CORE LANGUAGES        Java, Python, C++, TypeScript, JavaScript, SQL
FRONTEND & MOBILE     React Native, Expo, React, Next.js, Tailwind CSS
BACKEND & SERVICES    Spring Boot, Node.js, Express, REST APIs, STOMP WebSockets
DATABASES & CLOUD     PostgreSQL, Redis, MongoDB, MySQL, Cloudflare R2, AWS SDK, Firebase
SCIENTIFIC & GIS      CesiumJS, Mapbox Vector Tiles, deck.gl, MapLibre GL, PySide6, PyQtGraph, NumPy, SciPy, OpenCV
TOOLING & WORKFLOW    Git, GitHub Actions, Figma, Linux/Unix, Postman
```

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `engineering.philosophy`

```text
[01] TRICKY INTERNALS -> CLEAN UTILITY
     Deconstruct complex OS networking or system behavior into a focused tool (Netwich).

[02] REAL CAMPUS NEEDS -> COHESIVE PRODUCT
     Connect fragmented daily student life into a reliable mobile experience (GEHU Connect).

[03] SPATIAL & WEATHER DATA -> DECISION SUPPORT
     Translate geographic layers and prediction errors into visual intelligence (Aranya, MeghaVyuha).

[04] RIGOROUS SIMULATION -> EMPIRICAL EVIDENCE
     Test and measure technical hypotheses through repeatable scientific computing (ORVESS-PAT).
```

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `leadership & field`

```text
Director General: University Model UN Club
├── Hosts university Model UN conferences, committee ops, and delegate training
├── Led outreach workshops across 15+ schools in Dehradun
└── Delegate record: High Commendation at Lokvidhan MUN, delegate at IIT Roorkee MUN

Apple + Infosys: iOS Student Developer Program
└── Selective hands-on program in native iOS architecture, Swift, and Apple platform patterns
```

<div align="center">
  <img src="./hud-divider.svg" width="100%" alt="HUD Divider" />
</div>

## `connect`

<div align="center">

<a href="https://github.com/ParthKhansali">
  <img src="https://img.shields.io/badge/GitHub-061008?style=for-the-badge&logo=github&logoColor=39ff6a" alt="GitHub" />
</a>
&nbsp;
<a href="https://www.linkedin.com/in/parth-khansali/">
  <img src="https://img.shields.io/badge/LinkedIn-061008?style=for-the-badge&logo=linkedin&logoColor=39ff6a" alt="LinkedIn" />
</a>
&nbsp;
<a href="mailto:parthkhansali@gmail.com">
  <img src="https://img.shields.io/badge/Email-061008?style=for-the-badge&logo=gmail&logoColor=39ff6a" alt="Email" />
</a>
&nbsp;
<a href="https://www.parthkhansali.tech/">
  <img src="https://img.shields.io/badge/Portfolio-061008?style=for-the-badge&logo=safari&logoColor=39ff6a" alt="Portfolio" />
</a>

<br/><br/>

<p>
  <a href="https://www.parthkhansali.tech/">Portfolio Site</a> ·
  <a href="https://www.parthkhansali.tech/notes/">Engineering Notes</a> ·
  <a href="https://github.com/ParthKhansali/parthkhansali.tech">Portfolio Source Repo</a> ·
  <a href="https://www.youtube.com/@Its_Parth">YouTube</a> ·
  <a href="https://www.instagram.com/parth_khansali/">Instagram</a>
</p>

<br/>

```text
parth@workstation:~$ ./status --report
> BUILD USEFUL SOFTWARE. SHIP IT CLEAN.
```

</div>
