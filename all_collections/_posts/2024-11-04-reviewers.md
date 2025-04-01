---
title: What is an in-depth review?
date: 2025-04-01 16:00:00 +0200
categories: [Monitors]
permalink: /in-depth-review/
---

Monitor specsheets can tell you basic characteristics of a display, but not how it fully performs. In-depth reviews include some form of GTG response time and color accuracy testing.

**Response time**

Advertised 1 ms LCD response time is never real. On (LCD) monitors, pixels are typically made up of 3 subpixels for the red, green and blue channels where all of these subpixels are internally just gray with a color filter on top. Gray-to-gray (GTG) response time refers to how long it takes for a (sub)pixel to change from one shade of gray to another, 0% being black and 100% being white. This controls the shade of each primary color for a pixel. On LCDs, response time isn't uniform and depends on the starting shade and target shade for each (sub)pixel. Response time testing usually includes going through some test patterns of different gray values and forming a heatmap of how long a transition takes. Response times longer than the refresh interval of a display will cause trails on moving objects (ghosting) or visible artifacts when missing the target shade with over/undershoot from aggressive overdrive.

VESA specification is to measure the total response time from some starting luminosity and target luminosity, and then discard the first and last 10%, meaning 10-90% of the total luminosity change is the transition. However, you'll notice most reviews don't use percentages but 0 for black and 255 for white (8-bit color allows for 256 distinct shades), typically due to the use of gamma correction as eyes don't perceive shades from black to white linearly and can tell differences in darker shades better than light ones. OSRTT is the industry-standard measurement tool, but others may include LDAT or custom photodiode-based tools. Different reviewers may have different configurations for any, such as use of gamma correction or tolerances (e.g. measurement concludes when value +- 3-10 GtG from target). Thus, the numbers from different reviewers often aren't directly comparable.

Other motion clarity tools include panning images (pursuit photos) such as TestUFO, Smooth Frog and Rtings Test Bench 2.0 Pursuit, which aim to provide a "what you see is what you get" picture of GtG-related ghosting and refresh rate related moving picture response time (MPRT). These have separate indicators for whether the pursuit photo was taken properly (dots form vertical lines), but many reviewers crop this out in their photos.

**Color accuracy**

Most internet content is mastered to an old color standard called sRGB. However, many gaming monitors are much wider gamut, often around 95%+ DCI-P3 which ends up oversaturated for sRGB content. This is technically not accurate, but might still be preferred as sRGB covers a relatively small amount of the visible spectrum. Basically all gaming monitor reviews use consumer or prosumer grade colorimeters (e.g. Calibrite, Spyder) to measure adherence to some color gamut (sRGB, DCI-P3, Rec.2020), color temperature / white point and  EOTF (electro-optical transfer function, also known as a tone reproduction curve, TRC, or gamma). However, much of the whitepoint depends on spectral power density emitted by the display which varies between panels. Colorimeters include generic spectral corrections but you can't be sure without a custom spectral correction measured via spectrometer. However, Spyder models don't support loading external spectral corrections making them far less accurate compared to a separately profiled colorimeter. Furthermore, they have worse low light accuracy compared to most (i1D3-based) Calibrite/X-Rite/ColorMunki probes, making contrast measurements questionable.

A general rule of thumb is to prioritize white point accuracy and gamma curve (either 2.2 or piecewise sRGB) while gamut / oversaturation is more of a matter of taste.

(WIP - sRGB piecewise vs flat 2.2 gamma, adding links for further reading dispay color theory)

Some in-depth reviewers, in subjective order of best first:
- [Monitors Unboxed](<https://www.youtube.com/@monitorsunboxed>)
- [Rtings](<https://www.rtings.com/monitor>) with [Test Bench 2.0](<https://www.rtings.com/monitor/learn/research/pursuit-photo>) (ignore scoring, read data)
- [小雪人评测](<https://www.youtube.com/@%E5%B0%8F%E9%9B%AA%E4%BA%BA%E8%AF%84%E6%B5%8B>)
- [好屏如潮](<https://space.bilibili.com/700608201/>)
- [TFTCentral](<https://tftcentral.co.uk/>) + [YouTube](<https://www.youtube.com/@tftcentral>)
- [Techless](<https://www.youtube.com/@techlessYT>)
- [TechteamGB](<https://techteamgb.co.uk/category/content/reviews/monitors/>) + [YouTube](<https://www.youtube.com/@TechteamGB>)
- [KitGuru](<http://www.kitguru.net/reviews/?category_name=monitors>)
- [TotallydubbedHD](<https://www.youtube.com/@TotallydubbedHD>)
- [Stilgar from moreleTV](<https://www.youtube.com/@MoreleTV>)
- [Aperture Grille](<https://aperturegrille.com/reviews/>) + [YouTube](<https://www.youtube.com/@ApertureGrille>)
- [PC monitors](<https://pcmonitors.info/reviews/>) + [YouTube](<https://www.youtube.com/@PCMonitors>)
- [io-tech](<https://www.io-tech.fi/category/artikkelit/naytot/>)

Some useful information (Spyder, OSRTT, etc.):
- [optimumtech](<https://www.youtube.com/@optimumtech>)
- [GTID](<https://www.youtube.com/@GTID>)
- [颠佬评测](<https://space.bilibili.com/12145493/>)
- [数玩工场 / inteceh Digit Workshop](<https://www.youtube.com/@cgbdw>)
