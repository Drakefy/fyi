---
title: What is an in-depth review?
date: 2025-04-01 16:00:00 +0200
categories: [Monitors]
permalink: /in-depth-review/
---

Monitor specsheets can tell you basic characteristics of a display, but not how it fully performs. In-depth reviews include some form of GtG response time and color accuracy testing.

**In-depth reviews**

Some in-depth reviewers, in subjective order of best first:
- [Monitors Unboxed](<https://www.youtube.com/@monitorsunboxed>)
- [Rtings](<https://www.rtings.com/monitor>) with [Test Bench 2.0](<https://www.rtings.com/monitor/learn/research/pursuit-photo>)
  - Focus on data, scores can be arbitrary and weights nonsensical
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
  - LDAT VESA style response time measurement is not very useful
- [GTID](<https://www.youtube.com/@GTID>)
  - OSRTT but no RGB tolerance specified, TestUFO with gray backgrounds
- [颠佬评测](<https://space.bilibili.com/12145493/>)
  - Calman Ultimate for color accuracy but unclear response time methodology and cropped TestUFO vertical lines
- [数玩工场 / inteceh Digit Workshop](<https://www.youtube.com/@cgbdw>)
  - Spyder measurements

**Response time**

Advertised 1 ms LCD response time is never real. On (LCD) monitors, pixels are typically made up of 3 subpixels for the red, green and blue channels where all of these subpixels are internally just gray with a color filter on top. Gray-to-gray (GtG) response time refers to how long it takes for a (sub)pixel to change from one shade of gray to another, 0% being black and 100% being white. This controls the shade of each primary color for a pixel. On LCDs, response time isn't uniform and depends on the starting shade and target shade for each (sub)pixel. Response time testing usually includes going through some test patterns of different gray values and forming a heatmap of how long a transition takes. Response times longer than the refresh interval of a display will cause trails on moving objects (ghosting) or visible artifacts when missing the target shade with over/undershoot from aggressive overdrive.

<div style="text-align: center; font-size: 0;">
  <img src="{{site.baseurl}}/assets/images/tftcentral_rt.gif" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <div style="text-align: left; font-size: 14px; margin-top: 4px; margin-bottom: 20px;">VESA-style response time measurement for one transition. Credit: <a href="https://tftcentral.co.uk/articles/response_time_testing" target="_blank">TFTCentral</a></div>
</div>

VESA specification is to measure the total response time from some starting luminosity and target luminosity, and then discard the first and last 10%, meaning 10-90% of the total luminosity change is the transition. However, you'll notice most reviews don't use percentages but 0 for black and 255 for white (8-bit color allows for 256 distinct shades), typically due to the use of gamma correction as eyes don't perceive shades from black to white linearly and can tell differences in darker shades better than light ones. OSRTT is the industry-standard measurement tool, but others may include LDAT or custom photodiode-based tools. Different reviewers may have different configurations for any, such as use of gamma correction or tolerances (e.g. measurement concludes when value +- 3-10 shades from target). Thus, the numbers from different reviewers often aren't directly comparable.

<div style="text-align: center; font-size: 0;">
  <img src="{{site.baseurl}}/assets/images/q27g3xmn_monitors_unboxed.png" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <img src="{{site.baseurl}}/assets/images/q27g3xmn_rtings.png" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <div style="text-align: left; font-size: 14px; margin-top: 4px; margin-bottom: 20px;">Gamma-corrected response time testing by <a href="https://www.youtube.com/watch?v=XbQ8Pe4WVxc" target="_blank">Monitors Unboxed</a> and <a href="https://www.rtings.com/monitor/reviews/aoc/q27g3xmn" target="_blank">Rtings</a> for the same model. Note different results.</div>
</div>

For in-depth information on this topic, see the following:
- Aperture Grille: [How LCD Response Times are Measured, and Why 10% to 90% GtG Measurements are Moderately Deceptive](<https://www.youtube.com/watch?v=MbZUgKpzTA0>)
- TFTCentral: [Response Time Testing – Pitfalls, Improvements and Updating Our Methodology](<https://tftcentral.co.uk/articles/response_time_testing>)
- Blur Busters: [GtG versus MPRT: Frequently Asked Questions About Pixel Response On Displays](<https://blurbusters.com/gtg-versus-mprt-frequently-asked-questions-about-display-pixel-response/>)

Other motion clarity tools include panning images (pursuit photos) such as [TestUFO](<https://testufo.com/ghosting>), [Smooth Frog](<https://www.aperturegrille.com/software/>) and [Rtings Test Bench 2.0 Pursuit](<https://testufo.com/rtings>), which aim to provide a "what you see is what you get" picture of GtG-related ghosting and refresh rate related moving picture response time (MPRT). These have separate indicators for whether the pursuit photo was taken properly (dots form vertical lines), but many reviewers crop this out in their photos.



<div style="text-align: center; font-size: 0;">
  <img src="{{site.baseurl}}/assets/images/testufo_discorz.png" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <img src="{{site.baseurl}}/assets/images/xb252q_blurbusters.apng" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <div style="text-align: left; font-size: 14px; margin-top: 4px; margin-bottom: 20px;">Simulated TestUFO with instant 0ms response time (left). Credit: <a href="https://forums.blurbusters.com/memberlist.php?mode=viewprofile&u=5224" target="_blank">Discorz</a> Ghosting and overshoot on flawed GtG response (right). Credit: <a href="https://blurbusters.com/faq/lcd-overdrive-artifacts/" target="_blank">Blur Busters</a></div>.
</div>

For in-depth information on this topic, see the following:
- Blur Busters: [HOWTO: Pursuit Camera With Motion Tests](<https://blurbusters.com/motion-tests/pursuit-camera/>)
- Aperture Grille: [Smooth Frog: An Updated Version of Frog Pursuit](<https://www.youtube.com/watch?v=1KF_1fYT8ZA>)
- Rtings: [How Our New Pursuit Pattern Makes Comparing Monitors Easier](<https://www.rtings.com/monitor/learn/research/pursuit-photo>)


**Color accuracy**

Most internet content is mastered to an old color standard called sRGB. However, many gaming monitors are much wider gamut, often around 95%+ DCI-P3 which ends up oversaturated for sRGB content. This is technically not accurate, but might still be preferred as sRGB covers a relatively small amount of the visible spectrum. Basically all gaming monitor reviews use consumer or prosumer grade colorimeters (e.g. Calibrite, Spyder) to measure adherence to some color gamut (sRGB, DCI-P3, Rec.2020), color temperature / white point and  EOTF (electro-optical transfer function, also known as a tone reproduction curve, TRC, or gamma). However, much of the whitepoint depends on spectral power density emitted by the display which varies between panels.

<div style="text-align: center; font-size: 0;">
  <img src="{{site.baseurl}}/assets/images/aw2725q_spd.png" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <img src="{{site.baseurl}}/assets/images/27g850a_spd.png" height="270px" style="margin: 0; vertical-align: bottom; display: inline-block;" />
  <div style="text-align: left; font-size: 14px; margin-top: 4px; margin-bottom: 20px;">Spectral power distribution for QD-OLED and Nano-IPS. Credit: <a href="https://www.youtube.com/@%E5%B0%8F%E9%9B%AA%E4%BA%BA%E8%AF%84%E6%B5%8B/" target="_blank">小雪人评测</a></div>
</div>

Colorimeters include generic spectral correction profiles which may not match the measured monitor. Custom spectral corrections can be created using a spectrometer and most models can be found on the [DisplayCAL Color Corrections database](https://colorimetercorrections.displaycal.net/). However, Spyder models don't support loading external spectral corrections making them far less accurate compared to a separately profiled colorimeter. Furthermore, they have worse low light accuracy compared to most (i1D3-based) Calibrite/X-Rite/ColorMunki probes, making contrast measurements questionable.

A general rule of thumb is to prioritize white point accuracy and gamma curve (either 2.2 or piecewise sRGB) while gamut / oversaturation is more of a matter of taste.

(WIP - sRGB piecewise vs flat 2.2 gamma, adding links for further reading on display color theory)

Further reading:
- Andrew Rodney: [The color of white](<http://digitaldog.net/files/22Thecolorofwhite.pdf>)
- Eaglshadow: [Creator's intent is a little bit broken when it comes to SDR gaming](<https://www.avsforum.com/threads/creators-intent-is-a-little-bit-broken-when-it-comes-to-sdr-gaming.3276018/>)
- ArgyllCMS Documentation: [Topical Discussions](https://www.argyllcms.com/doc/ArgyllDoc.html)
- [MHC2](<https://github.com/dantmnf/MHC2>)

