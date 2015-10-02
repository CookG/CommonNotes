# The Butterworth Filter Design
Filter is used to shape the frequency spectrum of a signal in communication or control systems. The shape or width of the roll-off also called the "transition band", for a simple first order filter may be too wide, so active filters designed with more than one order are required.

The complexity or **Filter Type** is defined by the filters "order", and which is dependent upon the number of reactive components such as capacitors or inductors within its design. For a simple first order filter it has a standard roll-off rate of 20 dB/decade or 6dB/octave. For a filter that has an $n^{th}$ number order, it will have a subsequent roll-off rate of 20n dB/decade or 6n dB/octave.

High-order filters, such as third, fourth, and fifth-order are usually formed by cascading together single first-order and second-order filters.

## Roll-off Rate
**Roll-off** is the steepness of a transmission function with frequency, it is usual to measure roll-off as a function of logarithmic frequency, the units of roll-off are either decibels per decade (dB/decade), where a decade is a 10-times increase in frequency, or decibels per octave (dB/octave), where an octave is 2-times increase in frequency.

Roll-off tends towards a constant gradient at frequencies well away from the cut-off point of the frequency curve. Roll-off enables the cut-off performance of such a filter network to be reduced to a single number.

### First Order Roll-off
For a nominal R-C network:
$$A=\dfrac{V_o}{V_i}=\dfrac{1}{1+i\omega RC}$$
**Frequency scaling** this to $\omega_c = \dfrac{1}{RC} = 1$ and forming the power ratio gives,
$$\left|A\right|^2=
\dfrac{1}{1+\left(\dfrac{\omega}{\omega_c}\right)^2}$$
In decibels this becomes,
$$10log\left(\dfrac{1}{1+\omega^2}\right)$$
or expressed as a **Loss** as
$$L=10log\left(1+\omega^2\right) dB$$
At frequencies well above $\omega=1$, this simplifies to,
$$L\approx10log\left(\omega^2\right)=20log\omega \hbox{ dB}$$
**Roll-off** is then given by 
$$\Delta L=20log\left(\dfrac{\omega_2}{\omega_1}\right) \hbox{ dB/interval$_{2,1}$}$$
For a decade it would be 
$$\Delta L=20\hbox{log}10=20\hbox{ dB/decade}$$
and for an octave
$$\Delta L=20\hbox{log}2=20\times 0.3=6\hbox{dB/octave}$$

**The overall gain of high order filters is fixed.**

## Filter Approximations 
An ideal filter would give use specifications of **maximum pass band gain and flatness**, **minimum stop band attenuation** and also **a very steep pass band to stop band roll-off(the transition band)**. This will require a large number of network responses that satisfy there requirement. Not surprisingly then that there are a number of **"approximation functions" in linear analogue filter design** that use a mathematical approach to best approximate the transfer function we require for the filter design.

Such designs are known as **Elliptical, Butterworth, Chebyshev, Bessel, Cauer** as well as many others. Of these five *classic* linear analogue filter approximation functions only the **Butterworth Filter** and especially the **low pass Butterworth filter** design is the most commonly used function.

## Low Pass Butterworth Filter Design
The frequency response of the **Butterworth Filter** approximation function is also often referred to as **maximally flat (no ripples)** response because the pass band is designed to have a frequency response which is as flat as mathematically possible from 0Hz (DC) until the cut-off frequency at -3dB with no ripples. Higher frequencies beyond the cut-off points rolls-off down to zero in the stop band at 20dB/decade or 6dB/octave.

One main disadvantage of the Butterworth filter is that it achieves this pass band flatness at the expense of a wide transition band as the filter changes from the pass band to the stop band. It also has poor phase characteristics as well.

Note that the higher the Butterworth filter order, the higher the number of cascaded stages there are within the filter design, and the closer the filter becomes to the ideal "brick wall" response.

# 