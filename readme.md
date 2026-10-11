# [SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection with MATLAB Code

In the figure, the SAR platform flies at a speed v along the azimuth direction with an oblique angle of θ. The range over which the beam sweeps is the imaging area. The linear frequency modulation (LFM) signal, which is commonly used in the SAR system, has its time domain form as follows:
where A is the amplitude of the signal, Tp is the time width, f c is the carrier frequency, and K is the linear frequency modulation. Differentiating equation (2.1) with respect to time t reveals that its instantaneous frequency is linear. Due to this property, LFM signals have a much higher time-bandwidth product than general signals, allowing them to cover a larger range of beams while still meeting the requirements for distance resolution in most imaging scenarios. Therefore, they are often used as both transmitters and receivers in SAR imaging systems [1].
When the SAR system emits an LFM signal in the range direction and receives echoes for data processing into digital signals, it enters the matching filtering process. Its essence is to make the echoes meet the maximum output signal-to-noise ratio (MSNR) criterion by designing a linear filter whose response function satisfies the conjugate relationship with the energy spectrum of the signal. This approach enhances the amplitude-frequency characteristics of the echo signals, thereby increasing signal energy and suppressing clutter or interference signals [38-40].
The expression for receiving the range-direction echo signals from the SAR is known. By utilizing the conjugate characteristic of the spectrum, a pulse response that meets the MSNR criterion can be designed to achieve real-time matching filtering. Matched filters are widely used in LFM signal processing processes today [1]. The specific steps involve first using the principle of stationary phase (PSP) to convert the LFM time domain signal to the frequency domain,
where the pulse response function of the matched filter in the frequency domain can be represented as,
and finally, after Fourier inverse transformation, it can be transformed back into a single pulse form, resulting in the imaging position being exactly at the original range-direction location of the target.
When the SAR system is flying along the azimuth direction, the distance-time received echoes at the same range cell also exhibit the same properties as LFM signals. Therefore, performing azimuth matching filtering for each range cell can determine the imaging position of the target in the azimuth direction, ultimately forming a two-dimensional SAR image [41].
SAR-GMTI Basic Principles - In the aircraft platform section of Section 2.2.1, the SAR-GMTI system is mounted, and its spatial geometric model is shown in Figure 2.2.
The green dot in the figure represents the moving target, which moves along a straight line at constant velocity along the dashed line. The distance-to-velocity ratio is vr, and the azimuth-to-velocity ratio is v a. The platform flies at an azimuth speed of v, with the beam angle of incidence being θ. At the zero azimuth moment, the SAR-GMTI beam center points towards the moving target. At this time, the radar's distance to the moving target is R0, and R(ta) represents the radar's distance to the moving target at any azimuth moment.
In the formula, wr(.) and wa(.) represent the distance and azimuth envelopes respectively, t r is the fast time in the distance direction, ta is the slow time in the azimuth direction, f c is the carrier frequency, Kr is the linear modulation frequency, c is the speed of light, T a is the pixel time.
According to the basic principle of SAR imaging, after distance-domain processing, the envelope information of the signal is ignored. Its time domain expression is as follows:
Observation of equation (2.9) reveals that the moving target has already been focused in the distance direction, and its azimuth signal is...
According to Section 2.2.1, the backscattered signals received by SAR exhibit LFM signal characteristics in the azimuth direction. The backscatter signals received by the SAR-GMTI system are essentially the same as those of the SAR, thus their Doppler center frequency is...
The frequency of the phase shift in the azimuth direction is.
It can be observed that the Doppler center frequency and azimuth modulation frequency of signals are both related to the target's motion speed. However, the velocity of moving targets is not clear before imaging processing, and cannot be compensated for, leading to deviations in the final imaging results. Specifically, the Doppler center frequency offset causes the azimuth position of moving targets displayed on the image to differ from their actual positions. If the azimuth modulation frequency changes too drastically due to the movement of the target, it becomes uncompensable, resulting in the failure of focusing on the azimuth direction of moving targets, leading to blurred trailing phenomena. Among these, whether the target is focused is not a concern for the SAR-GMTI system; the system ultimately needs to detect and locate moving targets, thus requiring secondary image processing.
The earliest moving target detection technology used was based on the Doppler spectral difference between the moving target echo and the surrounding stationary scene echoes, which could be achieved directly by using the Doppler center frequency domain detection method or the azimuth modulation slope self-focusing detection method [42]. Based on this, an improved moving target detection algorithm based on symmetrical Doppler views has been developed, which has enhanced the efficiency and capability of detecting moving targets, but fails because the clutter energy is stronger than that of the moving targets, and only detects the presence of moving targets without being able to locate them [43]. To address these issues, multichannel SAR-GMTI systems are commonly used, and techniques such as the Displaced Phase Center Antenna (DPCA) technology and Along-Track Interferometric (ATI) technology are utilized for moving target detection and location [44]. The system (using three channels as an example) flowchart is as follows:
In the subsequent introduction of multi-channel SAR-GMTI interference methods in this article, the workflow of the SAR-GMTI system is the same as the above process. After channel data undergoes distance distortion correction and distance compression, it first passes through DPCA technology to suppress environmental clutter. The motion target is detected by selecting an appropriate threshold or CFAR technique. Finally, the interference phase processing is carried out using ATI technology to estimate the target's radial velocity and correct the target's azimuth position.
MATLAB simulation results

## Images

![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](01.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](02.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](03.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](04.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](05.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](06.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](07.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](08.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](09.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](10.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](11.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](12.jpg)
![[SAR Imaging] Three-Channel SAR-GMTI System for Moving Target Detection [Attached MATLAB Code]](13.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
