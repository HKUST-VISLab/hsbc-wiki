
# Heterogeneous Data Sources in PRAISE-HK
The fusion of heterogeneous datasets coming from different sources. For example, the AQ data modelled and measured by Tasks 1 and 2 output air quality prediction. The transportation data obtained from Task 4, and the result of the transportation modelling is predicted traffic condition. We will also collect other data such as images and videos from mobile apps developed in Task 7. As follows, we will describe the data format. 


## Air-Quality Data

Air-quality data are collected from 14 weather station monitoring the air quality in different regions in Hong Kong, "CL"(Central), "CB"(Causeway Bay), "MK"(Mong Kok),  "TC"(Tung Chung), "YL"(Yuen Long), "TW"(Tsuen Wan), "KC"(Kwai Chung), "CW"(Central Western), "SP"(Sham Shui Po), "TP"(Tai Po), "ST"(Sha Tin), "KT"(Kwun Tong), "EN"(Eastern), "TM"(Tap Mun). There are also 5 automatic weather station. The following data format also works for both static AQ data and AQ prediction. 


### AQHI (Air Quality Health Index) provides a number from 1 to 10+ to indicate the level of health risk associated with local air quality.
<table width="100%">
<tbody width="100%">
   <tr>
		<th>**Health Risk**</th>
		<th>
		<p>**AQHI**</p>
		</th>
		<th>
		  <p>Health Messages (**Risk Population**)  </p>
		</th>
		<th>
		  <p>Health Messages (**General Population**)</p>
		</th>
   </tr>
    <tr>
		<th>**Low**</th>
		<th>
		<p>**1–3**</p>
		</th>
		<th>
		  <p>**Enjoy** your usual outdoor activities.</p>
		</th>
		<th>
		  <p>**Ideal** air quality for outdoor activities</p>
		</th>
   </tr>
   <tr>
		<th>**Moderate**</th>
		<th>
		<p>**4–6**</p>
		</th>
		<th>
		  <p>**Consider reducing** or rescheduling strenuous activities outdoors if you are experiencing symptoms.</p>
		</th>
		<th>
		  <p>**No need to modify** your usual outdoor activities unless you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th>**High**</th>
		<th>
		<p>**7-10**</p>
		</th>
		<th>
		  <p>**Reduce** or reschedule strenuous activities outdoors. Children and the elderly should also take it easy.</p>
		</th>
		<th>
		  <p>**Consider reducing** or rescheduling strenuous activities outdoors if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th>**Very high**</th>
		<th>
		<p>**Above 10**</p>
		</th>
		<th>
		  <p>**Avoid** strenuous activities outdoors. Children and the elderly should also avoid outdoor physical exertion.</p>
		</th>
		<th>
		  <p>**Reduce** or reschedule strenuous activities outdoors, especially if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr> 
   </tbody>
</table>   
	