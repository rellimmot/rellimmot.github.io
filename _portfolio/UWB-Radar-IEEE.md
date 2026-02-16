---
title: "UWB Radar — IEEE 802.15.3a Standard Recommendation (2016)"
date: 2017-10-01
excerpt: "IEEE-format survey paper on ultra-wideband radar technology, history, and standardization — recommending a standard for IEEE 802.15.3a WPAN High Rate."
header:
  image: /assets/images/posts/uwb-radar/uwb-cardimage1.png
  teaser: /assets/images/posts/uwb-radar/uwb-cardimage2.png
sidebar:
  - title: "Academic Paper"
    image: /assets/images/posts/uwb-radar/uwb-cardimage2.png
    image_alt: "UWB radar module"
    text: "IEEE-format undergraduate survey paper on ultra-wideband radar communications and standardization."
  - title: "Details"
    text: "Author: Thomas Miller<br>University of New Orleans<br>July 24, 2016<br>IEEE 802.15.3a recommendation"
---
{% include toc title="Table of Contents" icon="file-text" %}

> **Ultra-Wideband Radar High Speed Communications: Recommending an IEEE 802.15.3a Standard**
>
> Thomas Miller, Electrical Engineering Undergraduate Student
> University of New Orleans, College of Engineering
>
> July 24, 2016
>
> *Index Terms — communication; distance ranging; impulse radar; localization; positioning; UWB radar; standards*

## Abstract

This document presents a broad overview on the history, definition, principles, technological progress, application, caveats, and discourse on the topic of UWB radar. Of particular objective in this document, we will analyze and choose a technology to be put forth into standardization for the IEEE 802.15.3a Wireless Personal Area Network (WPAN) UltraWideband Radio Task Group. The format and referencing for this paper will be in strictly IEEE research and journal publication format.

## Introduction

Ultra-Wideband (UWB) impulse based radar is of great potential for use in communication, medical instrumentation, surface penetrating radar, life detection in explosion debris sorting, medical imaging, non-destructive testing, GPS localization, distance ranging, low detection secure communication with high noise rejection, and sensor networks. Since the Federal Communications Commission (FCC) released the largest bandwidth ever in 2002 which covers a 7.5GHz band from 3.1-10.6GHz which allows for unlicensed use, the number of applications and speed of development of UWB increased significantly. Rapid advancement of solid-state integrated circuit components has made UWB radar and radio technology lucrative for consumer level low-power technology.

Developing communications standards for UWB technology has thus far been fraught with standoffs and turbulence. An eventual stalemate in standardization activities on the Institute of Electrical and Electronics Engineers (IEEE) 802.15.3a as a result of two competing technologies and concerns over interference has resulted from the conflict[^1].

## History of Impulse Based Radio Transmission and Progression to UWB

### History of Impulse Radio

The first radio wave transmissions and radar systems were based on impulse based short transmissions of electromagnetic energy. In 1886, Heinrich Hertz used the phenomena of what he came to find the radio noise generated in an electrical spark. This led to his creation of a UHF spark-gap transmitter which sent a spark through the air across two wire terminals and a tuned spark-gap detector that consisted of a loop of wire connected to a small gap at distance of a few meters. When the transmitter created a high-voltage spark that spanned the gap of two wires, small sparks also appeared across the receiver's spark gap that could be seen microscopically. This "Hertzian wave" radio phenomenon led to the development of larger scale spark gap systems capable of wireless telegraphy across miles of distance. Technologies that resulted of this form of impulse based electromagnetic transmission included a spark-gap transmitter that produced 10,000 sparks per second for use in telegraphy and spark-gap systems being used as an International distress frequency at 500kHz.

Continued use of this technology at the power levels required for long distances would not be possible because of the extremely "dirty" nature and high amplitude of the wide band signal emitted and transmitters and receivers communicating with this method would have to have great distances of separation[^2].

Impulse based radar systems were used by both Allies and Axis powers in World War II. Many aspects about the turnout of the war can be attributed to the early Electronic Warfare Systems based on this technology. Winston Churchill called the use of radar and countermeasures technology "Wizard Wars"[^3]. Frequency based radar systems hadn't begun development until the 1920s so impulse based systems were prevalent in use.

### Early Applications of UWB Radar

The development of UWB systems based on similar principles of the systems used today began in the 1960's and continued into the late 1980's with research conducted for the US Air Force. The early publications for UWB that resulted defined the technology in the public domain. Advancement of UWB technology followed at similar pace in the Soviet Union throughout this time. In the 1970's, testing of UWB radar systems brought the invention of ground penetrating radar systems for use in US Geological Survey (USGS) geophysical surveying, and technology similar in concept is being developed to date for military use in ground penetrating radar using high energy pulses ("chirps") with applications with both communication and landmine and IED detection[^4].

## Overview of Ultra-Wideband Radar

### Defining UWB

#### Basic Definition

The term Ultra-Wideband Radar or UWB, formally known as pulse radio, has developed into a definition for an electromagnetic means of propagating radio signal that is impulse based and carrier free (signal is not modulated upon another stronger carrier signal for transmission)[^5]. This technology is generally used with low transmission energy levels for short-range, high-bandwidth communications and radar spanning a wide portion of the radio frequency electromagnetic spectrum.

#### FCC Definition

From the US FCC 47 U.S.C. Section 15.503 Definitions:

> "Ultra-wideband (UWB) transmitter: An intentional radiator that, at any point in time, has a fractional bandwidth equal to or greater than 0.20 or has a UWB bandwidth equal to or greater than 500 MHz, regardless of the fractional bandwidth."
>
> "UWB Bandwidth. For the purpose of this subpart, the UWB bandwidth is the frequency band bounded by the points that are 10 dB below the highest radiated emission, as based on the complete transmission system including the antenna. The upper boundary is designated f<sub>H</sub> and the lower boundary is designated f<sub>L</sub>. The frequency at which the highest radiated emission occurs is designated f<sub>m</sub>."[^6]

#### IEEE Definition

From IEEE STD 1762: The AES UWB radar committee included the results of the FCC panel which established rules for unlicensed devices:

> "ultra-wideband: a. A term for a radar and communications technology utilizing simultaneously a band of frequencies that can span from hundreds of megahertz to the end of the microwave region. b. Per FCC rules, a fractional bandwidth ≥ 0.2 or a bandwidth ≥ 500 MHz c. A signal having a fractional bandwidth of 25% (DARPA) or 20% (FCC) or greater below a 1 GHz operational center frequency. Above 1 GHz, a signal with 25% (or perhaps 20%) or 500 MHz (whichever is smaller). See ultra-wideband device."[^7]

### Introduction to Ultra-Wideband Radar Theory

Ultra-wideband radar describes a signal whose fractional bandwidth is greater than 25% of its center frequency, which means that there is a high power narrow signal that has ripples of lower power signals that exponentially decrease in power around it. UWB signals are small in spatial resolution and have nonsinusoidal waveform (pulses of electricity rather than waves of electricity) at large bandwidth. UWB signals do not need a carrier signal, allowing for a significant decrease in transmit power requirements. In fact, UWB systems are opposite to traditional narrowband systems in that UWB requires low transmit power and high receive power while narrowband systems require high transmit power and low receive power[^8].

The large relative bandwidth of UWB radar can be described by the formula:

*η = Δf / f<sub>C</sub>*

where Δf is absolute bandwidth and f<sub>C</sub> is the carrier (center) frequency[^9].

### Signal Characteristics and Distinction

Pulse characteristics of the signals being transmitted, are that of which are short in time and rich in frequency. Typically, Gaussian pulses of high order derivatives are used. Bandwidth increases with the increasing order of Gaussian pulses. The use of a Gaussian pulse has the benefit of having a narrow pulse with as little side-pulse interference as possible.

With regard to low susceptibility to noise interference from other sources of radio waves such as cell phones or earth's magnetic fields, Ultra-Wideband signals have particular benefit in environments with a high "noise floor". The noise floor in this case can be defined as the sum of all noise within an environment. Relative to UWB, examples include mains electrical power, cell phones, Wi-Fi, and Bluetooth. Benefits are also seen in environments which have a high rate of multipath interference from objects such as in an indoors space populated with furniture[^10] [^11]. Multipath interference, the bouncing of signals back from objects of varying distance in an environment, is a nuisance that particularly effects most narrowband products like cell phones and Wi-Fi.

### Communication Signal Transmission

Signals are transmitted in very low energy single pulses. Timing sequences of these non-periodic pulses can represent symbols. Symbols are a group of information, such as the electronic equivalent to a sentence. A Pseudo Noise (PN) pattern of pulses can be used such that for example:

```
PN0 = 00100010110 could represent a binary '0'
PN1 = 10010101001 could represent a binary '1'
```

for a specified channel. A large number of channels numbering into the thousands could be had at the expense of bandwidth loss per n channels. Each channel can consist of independently representable binary combinations, so each device can effectively speak a different language that only the particular device and the host device know. The sequences of pulses can be altered in length and fill to add more channel complexity. Adding length, or longer binary code, lowers transmission rate but improves sensitivity. Adding fill, or longer signal pulses, results in fewer channels but improves sensitivity. With regard to code spread, orthogonal codes such as Walsh-Hadamard, Barker, Gold sequences, and Kasami sequences can be utilized to maximize emitted energy by smoothing out the spectrum of emission[^11] [^12].

UWB impulse generating circuits can be relatively simple with use in the Continuous Time Binary Value (CBTV) domain. A dual slope generator circuit with a two transistor delay element is used, which can transmit sufficient energy for short range use and be contained within a single modern computer chip. Without a carrier signal needed, little energy is used in the transmission of impulse-based UWB signals[^11] so the design of the computer chip can be minimal, especially relative to other modern transceiver (transmit and receive) systems.

### Signal Receiving

Receiving systems in time domain processing for UWB time-domain processed applications vary widely, but using an example, with signal pulses (letters) at < 200 picoseconds → 5GHz, forming 'chips' (words) of Δt = 10-100 nanoseconds → 10-100MHz, and binary value symbol (sentence) lengths of 100 nanoseconds to 1 microsecond → 1-10MHz, and in ranges similar, a RAKE receiver could be used. A RAKE receiver is beneficial to UWB because of its ability to discern a discrete signal in a low signal-to-noise ratio multipath environment. A RAKE receiver is helpful to collect many weak signals and combine them into one because it uses many receive antenna collectors at the same time. Several collectors, as in with a spatial full RAKE receiver, independently decode single chips into symbols based on received amplitude gathered from the receivers many "fingers", then integrate each signal's pseudo noise sequences into a cross correlative algorithm. Effectively, we combine many signals together and find slow moving patterns in the signals to filter out as background noise, then take the fast changing patterns and multiply them together to form symbols (sentences) of UWB.

Since the transmitted signal is very low in power, a highly sensitive receiver is not the only requirement for receiving UWB signals. Millions of pulses are collected with each transmitted symbol, thus multiplying and accumulating symbols received from direct and reflected paths is necessary to discern symbols from noise. The cross correlative method for symbol detection is statistical as such that it multiplies millions of signals against a template with each point in time in order to show probability of signal detection[^11]. Previous to modern advances in computing chip technology, this would comprise a rather large and expensive array of components. Today, as an example, all receiver and transmitter components can be on a single SoC ASIC chip such as the Novelda XeThru X2, a $65 single chip UWB radar transceiver that performs ranging in sub-millimeter accuracy even through walls and obstacles, performs sampling at 39 gigasamples per second, has power consumption < 120 milliwatts, handles full RAKE signal processing, and transmits its data via industry standard Serial Peripheral Interface (SPI).

### Current Implications of UWB Technology

- **Line-of-sight high resolution all-weather radar**
- **Subsurface radar and depth ranging** — snow depth, ice depth, water depth, subsurface cave mapping
- **Low flying target and counter-stealth radar detection**
- **Spread-spectrum radar and communication techniques with low intercept probability**
- **Medical instrumentation** — respiration and vital signs monitoring; high resolution imaging (like X-ray and CT) using scanning beams and multiple pulse generators to measure unique signal backscattering due to impedance differences in tissue; pneumothorax detection (blood in chest cavity)
- **Occupancy sensing, tracking, and counting**
- **Subsurface depth sensors such as stud finders** — Bosch D-Tect Wallscanner, Dewalt Handheld Radar Scanner
- **Simultaneous Localization and Mapping (SLAM)** — best when combined with other technologies such as GPS and LiDAR; can be applied to mapping rough terrain after explosion or contamination via ground or quadcopter; can be applied to a robot that can pre-sweep a target area for mapping and through-wall person detection in SWAT and military applications
- **Sensor networks** — low transmit power requirements make this especially suitable for "smart home" type sensor networks such as with smoke detectors, window/door breach alarm sensors, occupancy sensors, and temperature/humidity sensors in zoned climate control systems; unattended ground sensors in battlefield situations
- **Millimeter accuracy positioning and ranging with use of UWB transmitter and mote receiver networks** — potential for cell phone integration of UWB transmitter could allow for applications such as a store app (for example a Fastenal or Lowes) that allows a user to search an item and be guided directly to the item; Pozyx Breakout for Arduino uses the DecaWave DWM1000 IEEE 802.15.4-2011 compliant transceiver for this application
- **Wireless USB** — MB-OFDM is currently capable of 480-Mb/s data rates at 3.5m range

## Overview of UWB Communication Technology

UWB is capable of transferring a large amount of data over short distances (<10m is typical). The unlicensed-use spectral density assigned by the FCC spectral mask allows UWB to be readily applied to Personal Area Networks (PAN) or Body Area Networks (BAN) such as with medical biometric sensors. These sensor networks have an effective distance of less than 30 meters in most cases. Due to its extremely low power relative to other technologies that occupy its bandwidth, these applications can coexist with other technologies without causing interference[^1]. Typical power density is 1/10,000th of that of a cell phone, which allows most UWB to be operated at below the noise floor and is far more negligible in risk to harm in human tissue.

## IEEE Standardization and Implementation Issues

### Technical Criteria

Summarizing the technical requirements prescribed in[^13]:

1. **Unit manufacturing cost and complexity** must be minimal for it to be feasible for application to consumer grade products. Bluetooth standard would be a good benchmark for relative cost and complexity.

2. **Product design complexity** should be as such that an end-user product design engineer or technologist can develop on a UWB platform without extensive theory and background knowledge.

3. **Worldwide regulatory acceptance** is important to gauge when designing the UWB standard. Compliance with EU, UK, and Japanese guidelines for unlicensed use of UWB is optimum for worldwide industry adoption.

4. **Location awareness** could allow devices to connect to geofenced ad-hoc small communication networks. Additional framework addressing privacy should be included.

5. **Interference with coexisting technologies** is paramount in considerations for successful development of UWB technology that will not interfere with narrowband signals or other UWB signals.

6. **Form factor** should be accounted for as such that products will be able to be designed as compact as possible for integration into portable devices. Particular consideration should be addressed with possible integration into smartphones.

7. **Power use** should be minimal, as even if the UWB components are compact, if power consumption is high then battery size negates advantages of component size.

8. **Antenna design** should have a goal in mind as such that the antenna should not have to protrude from the device significantly.

### Coexisting with Shared Bandwidth

Many companies working in traditional narrowband systems have made it clear that they would not like to share their signal space with UWB. Of particular concern is those manufacturing GPS systems. One proposal is the use of notch filters to effectively avoid interference in high sensitivity bands, in which certain bands of frequency would not be allowed to be transmitted upon. This use of filtering would negate some of the benefits of UWB detrimentally. Another approach is the use of prescribed frequency bands for UWB systems. This multiband approach would allow simpler adaptation of UWB systems in different regulatory environments by switching on and off certain bands depending upon location. Real-time band switching could allow for flexible use when combined with smarter detection of other wireless systems in which interference could result. Many of the proposed IEEE 802.15.3a standards choose the multiband approach as a solution to concerns over interference because of its allowance for flexibility with coexistence with different technologies and regulatory environments.

### Channel Models and Multibanding

Many of the proposed IEEE 802.15.3a communications standards promoted the use of multibanding as a means to coexist with existing narrowband technologies without causing interference in excess of limits allowable for reliable use. These proposed standards varied widely in terms of number of bands, frequency ranges and bandwidths, null coexistence bands to which would be off-limits to UWB for other technologies such as WLAN and GPS, and variance in PRF (speed of pulses), order of modulation (pattern of sending pulse), and spread spectrum use (changing the frequency being used), each with their reasons for advantage or disadvantage.

Eventually the IEEE technical advisory group settled primary behind two proposals, one by WiMedia Alliance (promoted by TI and Intel) and one by XtremeSpectrum (promoted by Freescale [Motorola] and DecaWave).

#### WiMedia Alliance

WiMedia Alliance is the proposed standard for IEEE 802.15.3a which uses a multiband orthogonal frequency-division multiplexing (MB-OFDM) architecture. The focus of this approach was to have it be less susceptible to interference from other UWB systems. It focused the intention of UWB development toward short range multimedia transfer with low power needs. The UWB Forum noted that this approach was unnecessarily complicated, though it garnered enough backers to drive its competition with XtremeSpectrum.

#### XtremeSpectrum

XtremeSpectrum is the proposed standard for IEEE 802.15.3a which uses a dual band direct-sequencing (DS-UWB) pulse design and bi-phase modulation. DS-UWB has a very low spectral density, which begets low interference in shared bandwidth. Striking a balance with spectral performance and modulation efficiency, DS-UWB uses either Pulse Position Modulation (PPM) information encoding which modifies the time interval of pulses, or Binary Phase Shift Keying (BPSK) which reverses pulse phase in transmitted data to indicate binary values.

## IEEE Standardization Stalemate

### The TG3a Debate Between MB-OFDM and DS-UWB

A number of forums and votes were held which placed MB-OFDM at a majority vote in earlier votes and DS-UWB at a majority in later votes, but all votes failed to reach the 75% consensus required to exclude competing proposals.

Over concerns of WiMedia's standard not being in compliance with FCC regulations a declaratory ruling was requested by the competition, with which the FCC declared a ruling would be premature, given the ongoing activities with the IEEE standardization task group. The FCC has since remained passive in the argument for UWB standardization.

### Pushback Leading to the Tabling of Standardization

The author uses an excerpt from a public record email exchange with the 802.15.3a Advisory Group. Carl R. Stevenson, Chair of IEEE 802.18 Radio Regulatory Technical Advisory Group:

> "I hate to be blunt, but I was at the ITU-R TG-1/8 meeting in Geneva the week before last, and the story below is pure fiction, and I am being EXTREMELY polite and diplomatic in my choice of terminology. The fact of the matter is that there is a LOT of 'push-back' against UWB in the ITU-R, with virtually ALL of the services with allocations and entitlement to protection from interference from UWB and who would be overlaid by UWB (as well as a number of Administrations) presenting papers that show that the current limits for UWB are rather grossly inadequate to provide the degree of protection to which they are entitled (in many cases by the ITU Radio Regulations or existing ITU-R Recommendations). Once again, I find this sort of posturing in the trade press in an effort to 'make hay' in the 802.15.3a process to be reprehensible."[^14]

The author also uses an excerpt from Bob Heile, Chair of the IEEE TG3a advisory group, announcing withdrawal:

> "In a nutshell--- The process was in total deadlock. There were two technology proposals on the table backed by two different industry alliances. One of them was willing to move forward with a joint proposal the other was not and had sufficient votes to block forward progress. The task group finally agreed to duke it out in the market place. The Working Group concurred. The technology faces significant regulatory hurdles in addition. This was not a factor in this decision but from a standards perspective it probably was and is too early to write a UWB standard given the regulatory and market uncertainty in the world market. If there is a surviving approach in a year or two and the technology has proven itself to be commercially viable, then we can come back and revisit whether it makes sense to create an IEEE standard. The working group passed this motion unanimously at its interim meeting in January. A quorum was present. This item is being conditionally submitted to NesCom for action pending an affirming vote by the 802 Executive Committee at the March Plenary meeting in Denver."[^15]

### Tabling of 802.15.3a

By the end of 2004, the efforts to reach a consensus in TG3a ceased, the Task Group Chair (Bob Heile) resigned, and by 2006 the development of UWB technology was basically stalled due to the inability to reach an agreement for standardization. Also in 2006, the original Project Authorization request for UWB standardization was withdrawn which put IEEE 802.15.3a WPAN High Rate under "projects in hibernation"[^1].

### Impact on Unlicensed Use of UWB

It is important to note that the current failures of the standardization of UWB communication do not inhibit the unlicensed use of UWB technology for other purposes such as those outlined in Current Implications of UWB Technology above. UWB is actively in research for use in medical, localization, ranging, and radar uses among others, with commercial products currently in production using the technology. The use of UWB technologies in these low data rate and low power iterations could be considered insulting to the true capability of UWB systems. However, implementation of these technologies promotes continued development in UWB low-power systems and worldwide development of high-power systems which may raise motivation for an eventual IEEE standardization of WPAN High Rate communication using UWB.

Accepted standardization of IEEE 802.15.3a is not a requirement for developing communication devices using UWB either. Intel, Freescale/Motorola, and others have intentions to or have actualized research into production of UWB communication technologies outside the bounds of IEEE standardization.

## The Current State and Future of UWB

### Current Research and Interest

An analysis of number of publications, IEEE Xplore keyword searches, and available UWB products on the market indicate a steady decline for UWB technology from a peak of approximately 1700 yearly publications in the late 2000's to a current approximation of 1000 yearly publications[^1]. An analysis on Google Trends for "UWB" and "Ultra-Wideband" search terms indicate a very similar decline.

DigiKey remarked in an article "When will UWB be loved?", "Remember when UWB (ultra wideband) wireless communications was going to rule the world? It seems like only last year. Well … maybe two years ago. However, several promising UWB silicon vendors have since dissipated into the ether. T-Zero Technologies went to zero in February 2009; WiQuest ended its quest in November 2008; Intel abandoned the technical development end of the business and simply started wiring money to UWB startups. It is hard to remember that the WiMedia Alliance that developed the UWB communications standard once had 350 member companies. But the technology stubbornly remained a solution in search of a problem." Closing with the remark, "It has been a long fall for UWB – from the solution for all things wireless to the solution for one limited application"[^16].

### Currently Available Technologies and Standards

Despite the failure of IEEE 802.15.3a true UWB WPAN High Rate technology standardization, IEEE 802.15.4a WPAN Low Rate Alternative using DS-UWB has been commercialized for use in sensor network, asset localization, and distance ranging applications. MB-OFDM has had some success with development of wireless USB with transfer rates of 480 Mb/s at 3.5m range.

Super-resolution radar sensor networks, indoor localization, depth sensing "stud finders", intruder detection, autonomous navigation, and medical instrumentation are common high profile continued commercially developed products. Current trends would indicate that the use of UWB for communication has been overshadowed by its use in modern impulse based radar.

### Electronics Hobbyist UWB Development

Hobbyist electronics and common microprocessor development platforms such as Raspberry Pi and Arduino have recently seen an increase in the number of relatively affordable products available for UWB development. The DecaWave DWM1000 UWB indoor positioning system is used in the Pozyx and Loligo Arduino compatible breakout boards. The Novelda XeThru X2 IC is used in their X2M200 respiration sensor and X2M300 presence module which both interface well with Arduino and Raspberry Pi. However, search results on the arduino.cc, raspberrypi.org, sparkfun.com, and adafruit.com forums indicate few results for UWB discussion and development.

## Recommending a Standard

### Review of Objectives

It is the purview of this study to cover the following items:

- A thorough broad level novice overview of Ultra-Wideband impulse based high speed radio communications, and the history of the technology therein
- Convey the applications and implications of the use of UWB technology
- Review the standardization proposals and efforts put forth thus far by the IEEE 802.15.3a standardization task group
- Review the proposed standards and their continued relevance in the advancements of technology since the standardization of this technology was tabled by the discontinuance of the TG3a
- Recommend a technology to be put forth to the IEEE 802 Standards Commission for review and acceptance as the chosen standard for IEEE 802.15.3a WPAN High Speed Communication

### Applied Review of Proposed Standards with Modern Considerations

Today, UWB systems are in use and continue to be in development for systems used in through-wall radar imaging, medical imaging and instrumentation, low speed communications and sensor networks, and despite the formation of an 802 standard the technology is being developed for high speed communication.

Emphasis should be placed into consideration of the fact that from the period in which the Task Group 3a was disbanded, XtremeSpectrum primary backers Motorola & Freescale have dropped from the UWB forum, though it continues to develop its MB-OFDM technology for Wireless UWB systems.

Emphasis should be placed into the consideration of the fact that in 2007, The International Organization for Standardization (ISO) and International Electrotechnical Commission (IEC) selected WiMedia (DS-UWB) into standardization as ISO/IEC 26907 and ISO/IEC 26908[^17]. The British standards body, Ofcom also approved the use of unlicensed use of UWB technology and adopted the aforementioned standards chosen by ISO/IEC. The International Telecommunications Union Radiocommunication Sector (ITU-R) also submitted a Report and Recommendation in 2005 which chose WiMedia Alliance DS-UWB as their standard for UWB communication.

In a worldwide perspective which takes into consideration the sheer number of large policymaking bodies that have chosen WiMedia Alliance DS-UWB, there would be a disadvantage to choosing a different scheme of communication systems development that would be incompatible to preexisting technology developed against worldwide standards.

### Author's Recommendation

As prescribed in the outlined goals of this study, I was to pursue a recommendation without bias to each party or with that of international regulatory bodies. With this, the personal recommendation of the author follows.

**MB-OFDM standard proposed by XtremeSpectrum** is robust and highly adaptable to the considerations of many international regulatory bodies in the fact that its design accounts for many different variables in configuration. On the contrary the benefit of this system concept is also its downside. The complexity of development of this system requires a large number of band groups, time variant frequency hopping, a dependency on a much higher power full RAKE receiver, and nearly three times the processing power of DS-UWB. Some of these considerations were in account of the unknown with regard to international regulation, which thus far has been shown to choose the less complicated approach. This excessive robustness in technology becomes a weak point, in complexity of design and need for processing power far exceeding its competing DS-UWB.

**DS-UWB standard proposed by WiMedia Alliance** utilizes a split frequency spectrum with two bands of operation and a spread of channels within each band. The ability for a developer to either use Binary Phase Shift Keying or Quadrature Phase Shift Keying leaves much room for development as refinements in the technology makes this possible. The circuitry for DS-UWB is far simpler with less processing requirements, which will allow lower power consumption and simpler circuit development, which begets reliability in implemented technologies.

**Both technologies** have robust resistance to multipath interference, low power fading over similar distances, similar speed capacities, and similar signal coverage. In fact, the effective result in performance between these technologies is negligible.

**The author's recommendation**, in sole consideration of the factors outlined above, is to choose DS-UWB standard proposed by WiMedia Alliance as the standard of choice for the IEEE 802.15.3a WPAN High Speed Communication standard. The author's impartial recommendation has the additional benefit of being inline with current International standards that have been implemented, thus bolstering the development of UWB upon preexisting standards development. This convenience curtails industry need for massive redevelopment of US UWB technology and a need to cater to both a US and International market when designing a product for International sale and distribution.

## Summary and Conclusions

The merit of Ultra-Wideband systems capability of tremendous data capacity over short distances to solve many modern communications problems remains high. However, a turbulent regulatory stalemate regarding standardization and competing technologies filling the needs gap have nearly halted development of UWB systems. UWB development is a "project in hibernation" much like its standards task group despite its strong potential. In order for industry to adopt UWB in WPAN devices, a consensus for an accurate and robust channel model is necessary. Multiband approaches continue to be the frontrunner as a solution for curtailing interference with shared bandwidth narrowband communication systems.

The continued development of less powerful IEEE 802.15.4a products continue to see development but their potential pales in comparison to that of products that could result of the IEEE 802.15.3a standard. If an 802 standard cannot be developed, another solution similar to what was done with Bluetooth can bring true UWB communication to the market in which companies collaborate and develop technology with coherent methodology without IEEE standardization.

Continued development of UWB technology outpaces regulation, and the continued miniaturization of its transmit, receive, amplification, and signal processing components into CMOS form factor brings promise to the miniaturization of standardized communication devices for high speed short range networking.

International regulatory bodies spanning Europe and Asia have unanimously adopted DS-UWB by WiMedia Alliance as their standard of choice. These views, while not influencing a bias in the author's decision, are also in line with the recommendation set forth in the purview of this document.

In consideration of the aforementioned research, the author formally recommends DS-UWB by WiMedia Alliance as the IEEE 802.15.3a WPAN High Speed Communication as the standard of choice for industry to develop upon.

## Author Biography

**Thomas G Miller** is a Senior undergraduate student pursuing his B.S. degree in Electrical Engineering with Computer Engineering concentration and with minors in Computer Science and Mathematics from the University of New Orleans in New Orleans, Louisiana with a projected completion in Spring 2017.

From 2014 to now he has conducted research as an Instrumentation Engineer on laboratory and industrial scale cotton textile equipment at the US Department of Agriculture Southern Regional Research Center in New Orleans, with two publications pending submission in Near Infrared Spectrophotometry of Cotton Micronaire and Cotton Textile Energy Consumption of Differing Varietal Breeds. In 2015, he was awarded an internship with the Department of Energy Federal Energy Management Program internship and placed with the US Air Force Energy Office with the Office of the Secretary of the Air Force in The Pentagon. From 2006 to now, with a transition from Active Duty to Reservist in 2010, he has been continuing service in the US Air Force as an Electronic Warfare Avionics Systems Technician holding current rank of Technical Sergeant.

Mr. Miller has been a member of IEEE since 2014 and serves as Vice President of the student chapter of ISA at University of New Orleans. He holds the position of Lead Engineer for sensors and circuit systems design in the IEEE Robotics Club for IEEE Robotics Competition, and has been chosen for two years to participate in NASA's LaACES High Altitude Ballooning program as the lead mechanical, electrical, and microcomputer systems engineer. Mr. Miller was selected as a winner of 2016 InnovateUNO's research competition for his poster presentation on his USDA research on Micronaire Measurement of Gin Cotton with Near Infrared Spectroscopy In-Situ, which led to an award for the same research at the 2016 UL Academic Summit.

## References

[^1]: P. A. Catherwood and W. G. Scanlon, "Ultrawideband Communications — An Idea Whose Time has Still Yet to Come? [Wireless Corner]," *IEEE Antennas Propag. Mag.*, vol. 57, no. 2, pp. 38–43, Apr. 2015.

[^2]: John Harold Morecroft, A. Pinto, and W. A. Curry, "Spark Telegraphy". *Principles of Radio Communication*. Wiley, 1921.

[^3]: Greg Goebel, "WW2 & The Origins Of Radar," 01-Jan-2015. [Online]. Available: http://www.vectorsite.net/ttwiz.html.

[^4]: Stanislav Vitebskiy, "Ultra-Wideband, Short-Pulse Ground-Penetrating Radar: Simulation and Measurement," *IEEE Trans. Geosci. Remote Sens.*, vol. 35, no. 3, May 1997.

[^5]: Terence W. Barrett, "History of UltraWideband Radar & Communications: Pioneers and Innovators," *Prog. Electromagn. Symp.*, 2000.

[^6]: FCC, "47 U.S.C. Sections 154, 302a, 303, 304, 307, 336, and 544A." United States Federal Communications Commission (FCC).

[^7]: IEEE Aerospace and Electronic Systems Society, Ultrawideband Radar Committee, IEEE-SA Standards Board, and Institute of Electrical and Electronics Engineers, "IEEE standard for ultrawideband radar definitions," 2007.

[^8]: J. D. Taylor, "Ultrawideband radar progress," in *2012 IEEE Radar Conference*, 2012, pp. 190–195.

[^9]: M. G. Hussain, "Ultra-wideband impulse radar-an overview of the principles," *IEEE Aerosp. Electron. Syst. Mag.*, vol. 13, no. 9, pp. 9–14, 1998.

[^10]: H. Nikookar and R. Prasad, *Introduction to ultra wideband for wireless communications*. Berlin: Springer, 2009.

[^11]: S. Sudalaiyandi, H. A. Hjortland, Tuan-Anh Vu, O. Naess, and T. S. Lande, "Continuous-time high-precision IR-UWB ranging-system in 90 nm CMOS," 2012, pp. 349–352.

[^12]: Tor Sverre Lande, "Impulse-based ultra-wide-band (UWB) radio systems and applications," presented at the Google Tech Conference, 04-Jun-2008.

[^13]: Ellis, Siwiak, and Roberts, "802.15.3a — TG3a Technical Requirements." IEEE, 27-Dec-2002.

[^14]: "[802SEC] RE: &lt;802.15.3a&gt; ITU said to endorse Motorola-XtremeSpectrum UWB." [Online]. Available: http://grouper.ieee.org/groups/802/secmail/msg04604.html. [Accessed: 17-Jul-2016].

[^15]: Bob Heile, "Re. Withdrawal of the 802.15.3a PAR." IEEE.

[^16]: Steve Liebson, "When Will UWB Be Loved," DigiKey.

[^17]: "Ultra Wideband (UWB) Communications in the News, from SSS Online." [Online]. Available: http://sss-mag.com/uwb.html. [Accessed: 17-Jul-2016].
