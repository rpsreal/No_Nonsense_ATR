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
sdksjfd

### Live Mode:
sdksjfd

### iCustom:
The No Nonsense ATR offers 3 buffers. The NNFX_SL (SL), the NNFX_TP (TP), and the NNFX_TRADING_VOL (trading volume), which can be read externally through the function iCustom.

**Attention** The buffer NNFX_TRADING_VOL can only be read in candle 0 (shift=0) when the input "TRADING_VOLUME"=true

 ![buffers](./Images/painel_buffers.png)


**EXAMPLES**
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
