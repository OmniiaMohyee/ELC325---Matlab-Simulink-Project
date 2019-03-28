


Simulating the Performance of Different Modulation Schemes: **BPSK** ,**QPSK** ,**FSK** ,**QAM(16-64)** in an AWGN environment.

## To reproduce the figures:
1. to every model, a Constellation diagram is added  before and after the channel to produce the scatter plots.
2. to produce the BER graphs, write bertool in MATLAB commandline.
3. choose the required model and choose the modulation scheme to produce the theoretical BER plot.
4. choose the monte carlo mode to plot the actual BER.

## General Blocks used for all Modulation Schemes

1. AWGN Channel with bits per symbol varied with each modulation scheme.
2. Random Integer Generator with M-ary Number varied with each modulation scheme, sample time =1 and samples per frame = 100.
3. Constellation Diagram for the signal before and after the channel.
4. Error Rate Calculation
5. To WorkSpace : used to plot the BER.
6. Display : used to Display the BER, number of samples with error, number of total samples. 


## Modulation Schemes

### BPSK
Binary phase shift keying is the simplest form of phase shift keying. It uses two phases which are seperated by 180 degrees. 
Because of this large Phase Separation, the BPSK has the higest robustness to Noise between PSK modulation schemes.

#### Parameters used :
1. Random integer generator : M-ary Number = 2

#### Schematic
<img src="/WithoutRaisedCosine/BPSK/BPSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithoutRaisedCosine/BPSK/beforeNoise.png">

**After Noise:** 
<img src="/WithoutRaisedCosine/BPSK/AFTERNOISE.PNG">

#### BER diagram 
<img src="/WithoutRaisedCosine/BPSK/BER.png">


------------------------------------------------------------------------------------------------------------------------------

### QPSK 
Quadrature phase shift keying is a type of phase shift keying that can encode two bits per symbol and used for different phase shifts for encoding (0,90,180,270). it allows to carry twice as much of the information using the same bandwidth.

#### Parameters used :
1. Random integer generator : M-ary Number = 4
2. AWGN Channel : bits per symbol = 2

#### Schematic
<img src="/WithoutRaisedCosine/QPSK/QPSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithoutRaisedCosine/QPSK/beforeNoise.png">

**After Noise:** 
<img src="/WithoutRaisedCosine/QPSK/afterNoise.png">

#### BER diagram 
<img src="/WithoutRaisedCosine/QPSK/BER.png">


------------------------------------------------------------------------------------------------------------------------------


### FSK
Frequency Shift keying is a frequency modulation scheme where the information is transmitted through discrete frequency changes of a carrier siganl. M-FSK uses M different frequencies to modulate the signal.

#### parameters used :
1. Random integer generator : M-ary Number = 8
2. AWGN Channel : bits per symbol = 3
3. M-FSK modulator and De-Modulator : M-ary Number = 8

#### Schematic
<img src="/WithoutRaisedCosine/FSK/FSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithoutRaisedCosine/FSK/beforeNoise.png">

**After Noise:** 
<img src="/WithoutRaisedCosine/FSK/afterNoise.png">

#### BER diagram 
<img src="/WithoutRaisedCosine/FSK/BER.png">

------------------------------------------------------------------------------------------------------------------------------


### QAM
Quadrature Amplitude Modulation is an Amplitude Modulation Technique in which the signal is carried on two carriers shifted in phase by 90 degrees. QAM is done with many different Orders, As the Order of the Modulation increases, the amount of information that can be transmitted increases, but that it gives a low noise margin.

#### Types
1. QAM 16 
2. QAM 64

------------------------------------------------------------------------------------------------------------------------------

### QAM 16

#### parameters used
1.  Random Integer Generator : M-ary Number  = 16
2. AWGN Channel : bits per symbol = 4

#### Schematic
<img src="/WithoutRaisedCosine/QAM-16/QAM16.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithoutRaisedCosine/QAM-16/beforeNoise.png">

**After Noise:** 
<img src="/WithoutRaisedCosine/QAM-16/afterNoise.png">

#### BER diagram 
<img src="/WithoutRaisedCosine/QAM-16/BER.png">

------------------------------------------------------------------------------------------------------------------------------

### QAM 64

#### parameters used
1.  Random Integer Generator : M-ary Number  = 64
2. AWGN Channel : bits per symbol = 6

#### Schematic
<img src="/WithoutRaisedCosine/QAM-64/QAM64.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithoutRaisedCosine/QAM-64/beforeNoise.png">

**After Noise:** 
<img src="/WithoutRaisedCosine/QAM-64/afterNoise.png">

#### BER diagram 
<img src="/WithoutRaisedCosine/QAM-64/BER.png">

-------------------------------------------------------------------------------------------------------------------

# Modulation Schemes with raised-Cosine pulse Shaping

The raised-Cosine Filter is a filter frequently used for pulse shaping in digital modulation due to its ability to minimize intersymbol interference.

## General Blocks used for all Modulation Schemes with raised-cosine pulse shaping

1. Raised-Cosine Transmit filter.
2. Raised-Cosine Recieve filter.

## General Parameters

1. Raised-Cosine Transmit and Recieve Filters: filter span in symbol = 8, Decimation factor = 8
2. Error Rate Calculation : Recieve Delay = 8 ( to compensate for the delay introduced by the raised-cosine filters)

**Other parameters are the same as used in modulation without raised-cosine pulse shaping**


## Modulation Schemes

### BPSK

#### Schematic
#### Schematic
<img src="/WithRaisedCosine/BPSK/BPSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithRaisedCosine/BPSK/beforeNoise.png">

**After Noise:** 
<img src="/WithRaisedCosine/BPSK/afterNoise.png">

#### BER diagram 
<img src="/WithRaisedCosine/BPSK/BER.png">

----------------------------------------------------------------------------------------------------------------------------
### QPSK

#### Schematic
<img src="/WithRaisedCosine/QPSK/QPSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithRaisedCosine/QPSK/beforeNoise.png">

**After Noise:** 
<img src="/WithRaisedCosine/QPSK/afterNoise.png">

#### BER diagram 
<img src="/WithRaisedCosine/QPSK/BER.png">

----------------------------------------------------------------------------------------------------------------------------
### FSK

#### Schematic
<img src="/WithRaisedCosine/FSK/FSK.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithRaisedCosine/FSK/beforeNoise.png">

**After Noise:** 
<img src="/WithRaisedCosine/FSK/afterNoise.png">

#### BER diagram 
<img src="/WithRaisedCosine/FSK/BER.png">

----------------------------------------------------------------------------------------------------------------------------
### QAM 16

#### Schematic
<img src="/WithRaisedCosine/QAM16/QAM16.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithRaisedCosine/QAM16/beforeNoise.png">

**After Noise:** 
<img src="/WithRaisedCosine/QAM16/afterNoise.png">

#### BER diagram 
<img src="/WithRaisedCosine/QAM16/BER.png">

----------------------------------------------------------------------------------------------------------------------------
### QAM 64 

#### Schematic
<img src="/WithRaisedCosine/QAM64/QAM64.png">

#### Scatter Plots
**Before Noise:**
<img src="/WithRaisedCosine/QAM64/beforeNoise.png">

**After Noise:** 
<img src="/WithRaisedCosine/QAM64/afterNoise.png">

#### BER diagram 
<img src="/WithRaisedCosine/QAM64/BER.png">














```python

```
