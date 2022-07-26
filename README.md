# PRT-New_Donchians

## Summary
This is an implementation of the Donchian channel indicator for ProRealTime v10.3.

## Usage
Usage of this indicator should be fairly easy;

- install the New_Donchians indicator on your version of ProRealTime (v10.3), either by directly inputting the source code to a new indicator or by importing the .itl file provided.
- open a chart of the instrument you want to monitor
- Click on the 'Price' tab
- select 'Add indicator' from the drop-down menu
- select 'New_Donchians' from the list of indicators
- you will then be shown a window where you can modify the appearance of the indicator on your chart

To remove the New_Donchians indicator from your chart, press the 'Alt' key and click the New_Donchians tab on the chart.

## What it does
The Donchian channel is an indicator used in market trading developed by Richard Donchian. It is formed by taking the highest high and the lowest low of the last n periods. It can be considered as an indicator for the price volatility of the instrument being monitored.

## Advanced usage
By default the New_Donchians indicator indicates the highest price and  the lowest price that an instrument has displayed in the last 6 time periods. If you want to change the number of time periods that are covered by this indicator then you can change the value of the **SAMPLEPERIOD variable** in line 1.

This indicator returns the values of the highest price value, the lowest price value and the 'midpoint' of those as variables that can be used by other indicators. It does this by reurning the following variables:
- DonHI - the value of the upper Donchian band
- DonLO - the value of the lower Donchian band
- DonMID - the 'simple' halfway value between DonHI and DonLo ie.  (DonHI - DonLO) / 2

# Why was this indicator created?
The first version of ProRealTime I used was v10.3 on a candlestick chart. I noticed that sometimes a candlestick would either mark a high above the upper Donchian band or, a low below the lower band. The Donchian band would be marked correctly from the next candlestick.

![ProRealTime 10.3](donchian-103.png "Donchianchannel in PRTv10.3") ![ProRealTime 11.1](donchian-111.png "Donchianchannel in PRTv11.1")
