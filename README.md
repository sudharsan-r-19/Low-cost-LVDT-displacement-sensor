[LVDT.md](https://github.com/user-attachments/files/31099075/LVDT.md)
# Design, Fabrication and Experimental Characterization of a Low-Cost LVDT-Based Linear Displacement Sensor



## Overview

This project presents the design, fabrication, and experimental characterization of a low-cost **Linear Variable Differential Transformer (LVDT)** for linear displacement measurement.

The prototype was developed to demonstrate the practical relationship between:

**Mechanical displacement → magnetic coupling → mutual inductance → induced voltage → electrical measurement**

The sensor was fabricated using AWG 32 copper enameled wire, a PVC pipe/former(diameter = 1 inch), a movable metallic core(<1 inch), mechanical supports(wooden box), connectors(H-type screw terminal strips CH2), and connecting insulated wires. A 230 Vac to 12-0-12 V, 750 mA step-down transformer was used as the AC excitation source. The secondary output was connected to a rectifier circuit and verified using a digital multimeter.





## Objectives

* Understand the operating principle of an LVDT.
* Study electromagnetic induction and mutual inductance.
* Design and fabricate a low-cost LVDT prototype.
* Investigate the effect of core displacement on output voltage.
* Develop an AC excitation and output measurement arrangement.
* Rectify and measure the sensor output using a multimeter.
* Characterize the displacement-voltage relationship experimentally.
* Identify practical limitations and sources of error.





## LVDT Working Principle

A conventional LVDT consists of one primary winding, two secondary windings, and a movable magnetic core.

An AC excitation is applied to the primary winding. This produces an alternating magnetic field. The magnetic flux links with the secondary windings and induces voltages according to Faraday's law:

Faraday's Law of Electromagnetic Induction



The basic operating principle of an LVDT is electromagnetic induction.



e(t)=−N\*(dΦ(t)/dt)



where:



e(t) = instantaneous induced EMF (V)

N = number of turns

Φ(t) = magnetic flux (Wb)



When the core moves, the magnetic coupling between the primary and secondary windings changes. Consequently, the induced secondary voltages change.

For a differential LVDT:


V\_out =V\_S1 - V\_S2


where V\_S1 and V\_S2 are the voltages induced in the two secondary windings.



## Mutual Inductance

Mutual inductance is the main electromagnetic concept behind the sensor.

It can be represented as:



M=k\*(sqrt\_L1\*​L2)​

​

where:

* (M) = mutual inductance
* (k) = coefficient of magnetic coupling
* (L\_1) = inductance of winding 1
* (L\_2) = inductance of winding 2

The movable core changes the magnetic coupling and therefore changes the mutual inductance.



The fundamental sensing chain is:



Core Displacement
↓
Change in Magnetic Coupling
↓
Change in Mutual Inductance
↓
Change in Induced Secondary Voltage
↓
Measured Electrical Output





## Prototype Construction

The fabricated prototype consists of:

* PVC cylindrical former
* AWG 32 copper enameled wire
* Movable metallic rod/core
* Mechanical holders
* Wooden mounting base
* Electrical connectors
* Insulated connecting wires
* Rectifier circuit
* Step-down transformer
* Digital multimeter
* Breadboard for circuit connections



The movable core is positioned along the axis of the coil assembly. Proper axial alignment is important because eccentric movement can affect magnetic coupling and measurement repeatability.





## Component Specifications

|Component|Specification|Function|
|-|-|-|
|Copper magnet wire|AWG 32(0.202mm)|Coil winding|
|PVC pipe/former|1 inch (2.54 cm)|Coil former|
|Step-down transformer|230 VAC → 12-0-12 VAC, 750 mA|AC excitation|
|Metallic rod/core|1.27 cm|Movable magnetic core|
|Plastic holder|Fabricated|Mechanical support|
|Connector|H-type screw terminal strips CH2|Electrical connection|
|Connecting wires|Insulated|Circuit interconnection|
|Rectifier circuit|1N4007 diode, 1kohm,10kohm load|AC-to-DC conversion|
|Breadboard|Standard type|Prototype circuit|
|Digital multimeter|DT-830D|Voltage measurement|
|Wooden base|5\*5 inches|Mechanical mounting|

### 

### AWG 32 Wire

The nominal conductor diameter of AWG 32 copper wire is approximately **0.202 mm**.

The actual **winding resistance** should be experimentally measured because it depends on the total wire length, temperature, winding construction, and manufacturing tolerance.



### Excitation Transformer

* Primary: 230 VAC
* Secondary: 12-0-12 VAC
* Secondary configuration: Center-tapped
* Rated secondary current: 750 mA

The 750 mA value is the transformer's rated maximum secondary current, not necessarily the actual current consumed by the LVDT.



## Electrical Measurement Arrangement

The basic experimental signal path is:



230 VAC
↓
12-0-12 VAC Step-Down Transformer
↓
AC Excitation
↓
LVDT Coil Assembly
↓
Secondary Output
↓
Rectifier Circuit
↓
Digital Multimeter
↓
Output Voltage



The rectifier converts the induced AC signal into a measurable DC quantity.

For very small signals, a simple diode rectifier can introduce significant measurement error because the diode forward voltage can be comparable to the sensor output. A precision rectifier would be preferable for a future version.



## Experimental Procedure

1. Assemble the LVDT coil and mechanical core.
2. Verify all electrical connections.
3. Connect the low-voltage AC excitation source.
4. Place the movable core at the reference position.
5. Connect the sensor output to the rectifier circuit.
6. Connect the digital multimeter.
7. Move the core in controlled displacement increments.
8. Record displacement and corresponding output voltage.
9. Repeat measurements where possible.
10. Plot output voltage versus displacement.
11. Determine the maximum output and useful operating region.
12. Analyze sensitivity, linearity, repeatability, and possible errors.

\---

## Experimental Results

The following measurements were obtained from the fabricated prototype:

|Displacement (cm)|Output Voltage (mV)|
|-:|-:|
|0|0|
|1|0.1|
|2|0.2|
|3|6.56|
|4|43.96|
|5|**71.13**|
|6|67.63|
|7|34.16|
|8|7.30|
|9|0.133|

### 

### Maximum measured output

The above measurement is only for forward direction, Negative output voltage is obtained for backward direction.

&#x20;

## Experimental Analysis

The output increases rapidly from approximately 3 cm to 5 cm, reaches a maximum near 5 cm, and then decreases toward 9 cm.

The measured response is therefore approximately bell-shaped rather than the ideal signed linear differential LVDT response.

This behavior may be influenced by:

* Non-identical secondary windings
* Winding geometry
* Core geometry and material
* Core alignment
* Magnetic leakage
* Excitation frequency
* Measurement of rectified magnitude rather than signed differential voltage
* Rectifier characteristics
* Limited multimeter resolution
* Mechanical positioning accuracy

Therefore, the measured curve should be treated as the experimental characteristic of this prototype rather than an ideal LVDT transfer function.



## Sensitivity

Sensitivity is defined as:



Sensitivity describes the change in output voltage for a given displacement.



S=ΔVout/Δx





### Parameters to be Measured

The following parameters should be added to the documentation after experimental verification:

|Parameter|Symbol|Value|Unit|Measurement Method|
|-|-|-:|-|-|
|Excitation voltage|(V\_P)|12-0-12|VAC|Datasheet|
|Excitation frequency|(f)|50|Hz|Datasheet|
|Excitation current|(I\_P)|750|mA|Datasheet|
|Primary resistance|(R\_P)|150-350|Ω|Datasheet|
|Secondary resistance|(R\_S)|1.5-3.2|Ω|Datasheet|
|Primary inductance|(L\_P)|\~2-6|H|Datasheet|
|Secondary inductance|(L\_S)|\~22-66|mH|Datasheet|
|Number of turns|(N)|\~4000-5000|turns|Count|
|Coil length|(L\_C)|\~500|m|Datasheet|
|PVC outer diameter|(D\_O)|\~33.4|mm|Datasheet|
|PVC inner diameter|(D\_I)|\~26|mm|Datasheet|
|Core diameter|(D\_C)|\~1.2|cm|scale|
|Core length|(L\_C)|\~7-8|cm|Scale|
|Maximum range|(x\_max)|9|cm|Experimental|
|Maximum output|(V\_max)|71.13|mV|Multimeter|

## 

## Sources of Error

### Electrical

* Transformer voltage variation
* Excitation frequency variation
* Coil resistance
* Contact resistance
* Rectifier diode voltage drop
* Breadboard contact resistance
* Multimeter resolution

### Magnetic

* Core material
* Magnetic hysteresis
* Leakage flux
* Eddy-current effects
* Non-uniform winding
* Unequal secondary coupling

### Mechanical

* Core misalignment
* Friction
* Backlash
* Displacement-reading error
* Inconsistent core positioning

### Environmental

* Temperature variation
* Electromagnetic interference
* Nearby ferromagnetic objects



## Limitations

This is a low-cost experimental prototype and should not be considered a precision industrial LVDT.

The present output characteristic is nonlinear over the complete 0–9 cm displacement range. The simple rectifier and direct multimeter measurement also limit the accuracy of very small output voltages.

The primary purpose of this prototype is to demonstrate:

* Electromagnetic induction
* Mutual inductance
* Magnetic coupling
* Displacement transduction
* Experimental sensor characterization



## Future Improvements

### Mechanical

* Precision coil former
* Matched secondary windings
* Improved core alignment
* Low-friction core guide
* Calibrated displacement scale
* Improved winding uniformity

### Electrical

* Differential amplifier
* Precision rectifier
* Low-pass filter
* Instrumentation amplifier
* Higher-resolution ADC
* Microcontroller-based digital output

### Data Analysis

* Multiple readings per position
* Mean and standard deviation
* Increasing/decreasing displacement sweeps
* Hysteresis calculation
* Repeatability analysis
* Linearity error
* Calibration curve
* Uncertainty analysis

\---

## Proposed Improved Signal-Conditioning System



LVDT
↓
Differential Amplifier
↓
Precision Rectifier
↓
Low-Pass Filter
↓
ADC
↓
Microcontroller
↓
Digital Displacement Display



The future system can convert the sensor voltage into a calibrated displacement value in millimeters or centimeters.



## Safety

The transformer primary is connected to **230 VAC mains voltage** and must be treated as hazardous.



Safety precautions:

* Use proper insulation and enclosure.
* Do not expose mains terminals.
* Disconnect power before modifying wiring.
* Avoid touching energized circuits.
* Use appropriate fusing/protection.
* Keep the low-voltage experimental section isolated from the mains side.
* Perform modifications only when power is disconnected.



## Key Concepts

* Linear Variable Differential Transformer (LVDT)
* Electromagnetic Induction
* Faraday's Law
* Mutual Inductance
* Magnetic Coupling
* AC Excitation
* Inductive Transducers
* Signal Conditioning
* Rectification
* Linear Displacement Measurement
* Experimental Characterization
* Sensor Calibration



## Project Status

**Prototype fabricated and experimentally tested**

* Tested displacement range: **0–9 cm**
* Maximum measured output: **71.13 mV**
* Maximum output position: **approximately 5 cm**
* Measurement instrument: **Digital multimeter**
* Excitation: **12-0-12 VAC transformer**
* Winding wire: **AWG 32 copper magnet wire**



## Conclusion

A low-cost LVDT-based displacement sensor was fabricated and experimentally characterized using copper magnet wire, a PVC former, a movable metallic core, a step-down transformer, a rectifier circuit, and a digital multimeter.

The experiment demonstrates how mechanical movement of a magnetic core changes the magnetic coupling and mutual inductance of the sensor, resulting in a measurable electrical output.

The prototype produced a maximum measured output of 71.13 mV at approximately 5 cm displacement. The observed nonlinear response provides useful insight into the practical effects of coil geometry, magnetic coupling, core alignment, rectification, and measurement limitations.

The project provides a foundation for developing a more accurate LVDT system using precision signal conditioning, differential amplification, ADC-based measurement, calibration, and digital signal processing.



## Author

**ECE student**

This repository documents the design, fabrication, experimental testing, and analysis of a low-cost LVDT displacement sensor.

