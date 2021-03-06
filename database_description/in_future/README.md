
# Heterogeneous Data Sources in PRAISE-HK
The fusion of heterogeneous datasets coming from different sources. For example, the AQ data modelled and measured by Tasks 1 and 2 output air quality prediction. The transportation data obtained from Task 4, and the result of the transportation modelling is predicted traffic condition. We will also collect other data such as images and videos from mobile apps developed in Task 7. As follows, we will describe the data format. 


## Air-Quality Data

Air-quality data are collected from 14 weather station monitoring the air quality in different regions in Hong Kong, "CL"(Central), "CB"(Causeway Bay), "MK"(Mong Kok),  "TC"(Tung Chung), "YL"(Yuen Long), "TW"(Tsuen Wan), "KC"(Kwai Chung), "CW"(Central Western), "SP"(Sham Shui Po), "TP"(Tai Po), "ST"(Sha Tin), "KT"(Kwun Tong), "EN"(Eastern), "TM"(Tap Mun). There are also 5 automatic weather station. The following data format also works for both static AQ data and AQ prediction. 


<blockquote><p> AQHI (Air Quality Health Index) provides a number from 1 to 10+ to indicate the air quality, which is grouped into five health risk categories with <a href="http://www.aqhi.gov.hk/en/health-advice/sub-health-advice.html">health advice from Hong Kong EPD</a>. </p></blockquote>
<table width="100%">
<tbody width="100%">
   <tr>
		<th><p><strong>Health Risk</strong></p></th>
		<th>
		<p><strong>AQHI</strong></p>
		</th>
		<th><p><strong>People with existing heart or respiratory illnesses</strong></p></th>
		<th><p><strong>Children and the Elderly</strong></p></th>
		<th><p><strong>Outdoor Workers </strong></p></th>
		<th>
		  <p><strong>General Public</strong></p>
		</th>
   </tr>
    <tr>
		<th>
		<a><img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/data_description/img/low.png"></a>
		 </th>
		<th>
		<p><strong>1–3</strong></p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
   </tr>
   <tr>
		<th><a><img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/data_description/img/moderate.png"></a></th>
		<th>
		<p><strong>4–6</strong></p>
		</th>
		<th>
		  <p>No response action is normally required. Individuals who are experiencing symptoms are advised to <strong>consider reducing</strong> outdoor physical exertion.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
   </tr>
   <tr>
		<th><a><img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/data_description/img/high.png"></a></th>
		<th>
		<p><strong>7</strong></p>
		</th>
		<th>
		  <p>People with existing heart or respiratory illnesses are advised to <strong> reduce</strong> outdoor physical exertion, and to <strong> reduce</strong> the time of their stay outdoors, especially in areas with heavy traffic. They should also seek advice from a medical doctor before participating in sport activities and take more breaks during physical activities.</p>
		</th>
		<th>
		  <p>Children and the elderly are advised to  <strong> reduce</strong> outdoor physical exertion, and to  <strong> reduce</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
		<th>
		  <p>No response action is required.</p>
		</th>
   </tr>
   <tr>
		<th><a><img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/data_description/img/very_high.png"></a></th>
		<th>
		<p><strong>8-10</strong></p>
		</th>
		<th>
		  <p>People with existing heart or respiratory illnesses are advised to <strong>reduce to the minimum</strong> outdoor physical exertion, and to <strong>reduce to the minimum</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>Children and the elderly are advised to <strong>reduce to the minimum</strong>  outdoor physical exertion, and to <strong>reduce to the minimum</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>Employers of outdoor workers performing heavy manual work are advised to assess the risk of outdoor work, and take appropriate preventive measures to protect the health of their employees such as <strong>reducing</strong> outdoor physical exertion, and <strong>reducing</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>The general public is advised to <strong>reduce</strong> outdoor physical exertion, and to <strong>reduce</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
   </tr> 
   <tr>
		<th><a><img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/data_description/img/serious.png"></a></th>
		<th>
		<p><strong>Above 10</strong></p>
		</th>
		<th>
		  <p>People with existing heart or respiratory illnesses are advised to <strong>avoid</strong> outdoor physical exertion, and to <strong>avoid</strong> staying outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>Children and the elderly are advised to <strong>avoid</strong> outdoor physical exertion, and to <strong>avoid</strong> staying outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>Employers of all outdoor workers are advised to assess the risk of outdoor work, and take appropriate preventive measures to protect the health of their employees such as <strong>reducing</strong> outdoor physicalexertion, and <strong>reducing</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
		<th>
		  <p>The general public is advised to <strong>reduce to the minimum</strong> outdoor physical exertion, and to <strong>reduce to the minimum</strong> the time of their stay outdoors, especially in areas with heavy traffic.</p>
		</th>
   </tr>    
   </tbody>
</table>   



<blockquote><p>Since the Air Quality Health Index (AQHI) issued by Hong Kong Environmental Protection Department is not comparable to other regions in the world, Weather Underground of Hong Kong refers to the Air Quality Index (AQI) issued by <a href="https://cfpub.epa.gov/airnow/index.cfm?action=aqibasics.aqi">U.S. Environmental Protection Agency</a> and calculates the Air Quality Index based on air pollutant concentration data issued by Hong Kong Environmenal Protection Department. AQI provides a number from 0-500 to indicate air quality, which is divided into six categories indicating increasing levels of health concern.</p> </blockquote>
<table width="100%">
<tbody width="100%">
   <tr>
		<th><p><strong>AQI</strong></p></th>
		<th>
		<p><strong>Levels of Health Concern</strong></p>
		</th>
		<th>
		  <p><strong>Health Advice</strong></p>
		</th>
		<th>
		  <p><strong>Color</strong></p>
		</th>
   </tr>
    <tr>
		<th><p><strong>0–50</strong></p></th>
		<th>
		<p><strong>Good</strong></p>
		</th>
		<th>
		  <p>Air quality is considered satisfactory, and air pollution poses little or no risk.</p>
		</th>
		<th>
		  <p>Green</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>51 to 100</strong></p></th>
		<th>
		<p><strong>Moderate</strong></p>
		</th>
		<th>
		  <p>Air quality is acceptable; however, for some pollutants there may be a moderate health concern for a very small number of people who are unusually sensitive to air pollution.</p>
		</th>
		<th>
		  <p>Yellow</p>
		</th>
   </tr>
   <tr> 
		<th><p><strong>101 to 150</strong></p></th>
		<th>
		<p><strong>Unhealthy for Sensitive Groups</strong></p>
		</th>
		<th>
		  <p>Members of sensitive groups may experience health effects. The general public is not likely to be affected. </p>
		</th>
		<th>
		  <p>Orange</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>151 to 200</strong></p></th>
		<th>
		<p><strong>Unhealthy</strong></p>
		</th>
		<th>
		  <p>Everyone may begin to experience health effects; members of sensitive groups may experience more serious health effects.</p>
		</th>
		<th>
		  <p>Red</p>
		</th>
   </tr> 
   <tr>
		<th><p><strong>201 to 300</strong></p></th>
		<th>
		<p><strong>Very Unhealthy</strong></p>
		</th>
		<th>
		  <p>Health alert: everyone may experience more serious health effects.</p>
		</th>
		<th>
		  <p>Purple</p>
		</th>
   </tr>    
   <tr>
		<th><p><strong>301 to 500</strong></p></th>
		<th>
		<p><strong>Hazardous</strong></p>
		</th>
		<th>
		  <p>Health warnings of emergency conditions. The entire population is more likely to be affected.</p>
		</th>
		<th>
		  <p>Maroon</p>
		</th>
   </tr>    
   </tbody>
</table>   



<blockquote><p><a href="http://www.EPA.gov">The United States EPA</a> maintain a table of breakpoints in calculating AQI.</p></blockquote>
<table>
<tbody>
	<tr>
		<td><b>AQI</b></td>
		<td rowspan="2"><b>Levels of Health Concern</b></td>
		<td><b>O<sub>3</sub> (ppb)</b></td>
		<td><b>O<sub>3</sub> (ppb)</b></td>
		<td><b>PM<sub>2.5</sub> (µg/m<sup>3</sup>)</b></td>
		<td><b>PM<sub>10</sub> (µg/m<sup>3</sup>)</b></td>
		<td><b>CO (ppm)</b></td>
		<td><b>SO<sub>2</sub> (ppb)</b></td>
		<td><b>NO<sub>2</sub> (ppb)</b></td>
	</tr>
	<tr>
		<td><i>I<sub>low</sub></i> - <i>I<sub>high</sub></i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i>- <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
		<td><i>C<sub>low</sub></i> - <i>C<sub>high</sub> (avg)</i></td>
	</tr>
	<tr>
		<td>0-50</td>
		<td style="background:#00e400;">Good</td>
		<td>0-54 (8-hr)</td>
		<td>-</td>
		<td>0.0-12.0 (24-hr)</td>
		<td>0-54 (24-hr)</td>
		<td>0.0-4.4 (8-hr)</td>
		<td>0-35 (1-hr)</td>
		<td>0-53 (1-hr)</td>
	</tr>
	<tr>
		<td>51-100</td>
		<td style="background:#ff0;">Moderate</td>
		<td>55-70 (8-hr)</td>
		<td>-</td>
		<td>12.1-35.4 (24-hr)</td>
		<td>55-154 (24-hr)</td>
		<td>4.5-9.4 (8-hr)</td>
		<td>36-75 (1-hr)</td>
		<td>54-100 (1-hr)</td>
	</tr>
	<tr>
		<td>101-150</td>
		<td style="background:#ff7e00;">Unhealthy for Sensitive Groups</td>
		<td>71-85 (8-hr)</td>
		<td>125-164 (1-hr)</td>
		<td>35.5-55.4 (24-hr)</td>
		<td>155-254 (24-hr)</td>
		<td>9.5-12.4 (8-hr)</td>
		<td>76-185 (1-hr)</td>
		<td>101-360 (1-hr)</td>
	</tr>
	<tr>
		<td>151-200</td>
		<td style="background:#f00; color:#fff;">Unhealthy</td>
		<td>86-105 (8-hr)</td>
		<td>165-204 (1-hr)</td>
		<td>55.5-150.4 (24-hr)</td>
		<td>255-354 (24-hr)</td>
		<td>12.5-15.4 (8-hr)</td>
		<td>186-304 (1-hr)</td>
		<td>361-649 (1-hr)</td>
	</tr>
	<tr>
		<td>201-300</td>
		<td style="background:#99004c; color:#fff;">Very Unhealthy</td>
		<td>106-200 (8-hr)</td>
		<td>205-404 (1-hr)</td>
		<td>150.5-250.4 (24-hr)</td>
		<td>355-424 (24-hr)</td>
		<td>15.5-30.4 (8-hr)</td>
		<td>305-604 (24-hr)</td>
		<td>650-1249 (1-hr)</td>
	</tr>
	<tr>
		<td>301-400</td>
		<td style="background:#7e0023; color:#fff;" rowspan="2">Hazardous</td>
		<td>-</td>
		<td>405-504 (1-hr)</td>
		<td>250.5-350.4 (24-hr)</td>
		<td>425-504 (24-hr)</td>
		<td>30.5-40.4 (8-hr)</td>
		<td>605-804 (24-hr)</td>
		<td>1250-1649 (1-hr)</td>
	</tr>
	<tr>
		<td>401-500</td>
		<td>-</td>
		<td>505-604 (1-hr)</td>
		<td>350.5-500.4 (24-hr)</td>
		<td>505-604 (24-hr)</td>
		<td>40.5-50.4 (8-hr)</td>
		<td>805-1004 (24-hr)</td>
		<td>1650-2049 (1-hr)</td>
	</tr>
	</tbody>
</table>


## GTS Data
There are two types of data: Regional_GTS_SYNOP and Regional_GTS_METAR. The former is mainly based on surface weather information (SYNOP) available on the GTS network, while the later is mainly based on hourly aviation weather reports (METAR).  

Regional_GTS_SYNOP contains data including Precipitation, Temperature, Dew Point, Sea Level Pressure, Wind Speed, Wind Direction, Relative Humidity and Visibility. Regional_GTS_METAR contains data including Temperature, Dew Point, Wind Speed, Wind Direction, Sea Level Pressure and Visibility. 

The former are updated once every three hours, while  the later is mainly based on hourly reports. 

## Satellite Data 
There are four types of images: Visible_South_China, Enhanced_Infra-red_South_China, Enhanced_Infra-red_Peral_River_Estuary and Aerosol_Optical_Depth_South_China. 

## Climate Data
There are the following types of data collection: 
 <a href="https://data.giss.nasa.gov/gistemp/tabledata_v3/GLB.Ts+dSST.txt">global temperature data</a>, 
 <a href="https://www.esrl.noaa.gov/gmd/ccgg/trends/#mlo_full">CO2 Monthly Data and Trend</a>, 
 <a href="http://eesc.columbia.edu/courses/ees/climate/labs/vostok/">Vostok Ice Core Data</a>, and 
 monthly rainfall data in Hong Kong,  
 
## HKO Warnings and Signals Data 
In Hong Kong, there are a <a href="http://www.hko.gov.hk/wxinfo/climat/warndb/warndb3_e.shtml">HKO Warnings and Signals Database</a> that stores Rainstorm Warnings, Historical Typhoon Warnings, as well as Historical Air Pollution Interesting Cases. Commencing 10 October 2011, the Warnings and Signals Database would also display the provisional records of recent warnings/signals in addition to the official records.  Provisional records will normally be checked during the first working day after the expiry or cancellation of the warning/signal for confirmation to be accepted as official records.

## Traffic Data

