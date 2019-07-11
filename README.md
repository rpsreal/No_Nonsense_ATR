# No_Nonsense_ATR
## Overview

No Nonsense ATR is a tool designed to help the [NNFX Traders](https://nononsenseforex.com/) backtest strategies and trading in real time.

The indicator calculates the value of the SL/TP based on the [ATR](https://nononsenseforex.com/indicators/the-worlds-best-forex-indicator/) allowing to verify the historical data in a simple and practical way, showing not only the SL/TP values but also the place where they would be and if it was a gain or loss.

The No Nonsense ATR also calculates the trading volume required for each trade according to the desired risk, the SL and using the account currency for the calculation thus giving a more accurate value.


 ![overview](./Images/overview.gif)

## Installation:
gdhdfgh

 ![inicial](./Images/painel_inicial.png)
 
## How to Use:
sdksjfd

 ![inputs](./Images/painel_inputs.png)

### Fillted ATR:
Fillted ATR mode allows you to filter out extreme events that affect the ATR value, such as the flash crash of January 3, 2019. Extreme events are detected if the candle size is greater than the "STANDARD DEVIATION MULTIPLIER" * [Standard deviation](https://en.wikipedia.org/wiki/Standard_deviation) (sigma σ) + the average ATR.
The average ATR is calculated for the number of candles placed in the input "SAMPLE SIZE".
If an extreme event is detected the candle size value is replaced by the average ATR on that candle thus creating the filtered ATR.

### Live Mode:
The Live Mode is designed to make it easier to use the indicator when trading in real time.
In this mode, the values of SL/TP and trading volume are always fixed to the most recent value.
This mode can be activated in two ways: by clicking on the area without candles in the right part of the graph (another clicks to disable the live mode) or changing the input "LIVE MODE" to true.

### Simulators:
The No Nonsense ATR has been tested on the Soft4FX and FXBlue simulators and can be used together with the No Nonsense ATR without any problem. However, if the simulators stop at the opening of the candle and the result of the SL/TP and Trading volume will include the value of the candle newly opened for the calculation of the ATR. To display the values of the SL/TP and the Trading volume of the previous candle on the most recent candle just put the value 1 in the "SHIFT" input.

### iCustom:
The No Nonsense ATR offers 3 buffers. The NNFX_SL (SL), the NNFX_TP (TP), and the NNFX_TRADING_VOL (trading volume), which can be read externally through the function [iCustom](https://docs.mql4.com/indicators/icustom).

**Attention**: The buffer NNFX_TRADING_VOL can only be read in candle 0 (shift=0) when the input "TRADING_VOLUME"=true

 ![buffers](./Images/painel_buffers.png)

**Examples**

Save the SL value of the previous candle in the variable SL
```c++
double SL=iCustom(NULL,0,"No Nonsense ATR ",14,1.0,14,1.5,0,0,"==========================",False,3.0,200,"==========================",false,0,14,Gold,Gold,false,Black,"==========================",false,false,false,false,false,0,DeepSkyBlue,0,Red,"==========================",false,1,0,"","","==========================",false,0,0,1);
```
 Save the Filter TP value of the current candle in the variable TP
```c++
double TP=iCustom(NULL,0,"No Nonsense ATR ",14,1.0,14,1.5,0,0,"==========================",True,3.0,200,"==========================",false,0,14,Gold,Gold,false,Black,"==========================",false,false,false,false,false,0,DeepSkyBlue,0,Red,"==========================",false,1,0,"","","==========================",false,0,1,0);
```
 Save the trading volume value (account currency = EUR and Risk = 3%) in the variable VOL
```c++
double VOL=iCustom(NULL,0,"No Nonsense ATR ",14,1.0,14,1.5,0,0,"==========================",False,3.0,200,"==========================",false,0,14,Gold,Gold,false,Black,"==========================",false,false,false,false,false,0,DeepSkyBlue,0,Red,"==========================",true,3,2,"","","==========================",false,0,2,0);
```



Thank you VP for everything. Check the No Nonsense Forex strategy at: https://nononsenseforex.com/

Developed by Rui Silva, Porto, Portugal
