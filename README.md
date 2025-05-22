# CCI-Dual-DMI-Strategy
somaye CCI + Dual DMI Strategy
CCI + Dual DMI Strategy Documentation
Overview
This script implements a trading strategy using the Commodity Channel Index (CCI) and two Directional Movement Index (DMI) indicators. The strategy aims to identify potential buy and sell signals based on the crossover of these indicators.

Strategy Components
Inputs
The strategy allows users to customize the following parameters:

CCI Length: The period for calculating the CCI. Default is 20.
First DMI Length: The period for the first DMI calculation. Default is 20.
Second DMI Length: The period for the second DMI calculation. Default is 40.
CCI Overbought Level: The threshold for the CCI to indicate overbought conditions. Default is +100.
CCI Oversold Level: The threshold for the CCI to indicate oversold conditions. Default is -100.
Indicator Calculations
CCI Calculation:

The CCI is calculated using the closing prices over the specified cciLength.
DMI Calculations:

Two DMI indicators are calculated:
First DMI: Calculated using the dmiLength1 (20).
Second DMI: Calculated using the dmiLength2 (40).
Entry Conditions (Buy)
A long position is entered when the following conditions are met:

The CCI crosses above the overbought level.
The first DMI's +DI crosses above -DI (indicating a bullish trend).
The second DMI's +DI is greater than -DI (confirming the bullish trend).
Exit Conditions (Sell)
A long position is exited when the following conditions are met:

The CCI crosses below the overbought level.
The first DMI's +DI crosses below -DI (indicating a bearish trend).
The second DMI's +DI is less than -DI (confirming the bearish trend).
Strategy Execution
The strategy enters a long position when enterLong conditions are met.
The strategy closes the long position when exitLong conditions are met.
Plotting
The script visualizes the following on the chart:

CCI line in blue.
Overbought and oversold levels as horizontal lines (red and green, respectively).
The first DMI's +DI and -DI lines in green and red.
The second DMI's +DI and -DI lines in lime and maroon, respectively.
Buy signals are indicated by green triangle-up shapes below the bars.
Sell signals are indicated by red triangle-down shapes above the bars.
