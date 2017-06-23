
# Heterogeneous Data Sources in PRAISE-HK
The fusion of heterogeneous datasets coming from different sources. For example, the AQ data modelled and measured by Tasks 1 and 2 output air quality prediction. The transportation data obtained from Task 4, and the result of the transportation modelling is predicted traffic condition. We will also collect other data such as images and videos from mobile apps developed in Task 7. As follows, we will describe the data format. 


## Air-Quality Data

Air-quality data are collected from 14 weather station monitoring the air quality in different regions in Hong Kong, "CL"(Central), "CB"(Causeway Bay), "MK"(Mong Kok),  "TC"(Tung Chung), "YL"(Yuen Long), "TW"(Tsuen Wan), "KC"(Kwai Chung), "CW"(Central Western), "SP"(Sham Shui Po), "TP"(Tai Po), "ST"(Sha Tin), "KT"(Kwun Tong), "EN"(Eastern), "TM"(Tap Mun). There are also 5 automatic weather station. The following data format also works for both static AQ data and AQ prediction. 


<blockquote><p> AQHI (Air Quality Health Index) provides a number from 1 to 10+ to indicate the level of health risk associated with local air quality. The AQHIs are grouped into five AQHI health risk categories with health advice provided:</p></blockquote>
<table width="100%">
<tbody width="100%">
   <tr>
		<th><p><strong>Health Risk</strong></p></th>
		<th>
		<p><strong>AQHI</strong></p>
		</th>
		<th>
		  <p>Health Messages (<p><strong>Risk Population</strong>)  </p>
		</th>
		<th>
		  <p>Health Messages (<p><strong>General Population</strong>)</p>
		</th>
   </tr>
    <tr>
		<th><p><strong>Low</strong></p></th>
		<th>
		<p><strong>1–3</strong></p>
		</th>
		<th>
		  <p><strong>Enjoy</strong> your usual outdoor activities.</p>
		</th>
		<th>
		  <p><strong>Ideal</strong> air quality for outdoor activities</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>Moderate</strong></p></th>
		<th>
		<p><strong>4–6</strong></p>
		</th>
		<th>
		  <p><strong>Consider reducing</strong> or rescheduling strenuous activities outdoors if you are experiencing symptoms.</p>
		</th>
		<th>
		  <p><strong>No need to modify</strong> your usual outdoor activities unless you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>High</strong></p></th>
		<th>
		<p><strong>7-10</strong></p>
		</th>
		<th>
		  <p><strong>Reduce</strong> or reschedule strenuous activities outdoors. Children and the elderly should also take it easy.</p>
		</th>
		<th>
		  <p><strong>Consider reducing</strong> or rescheduling strenuous activities outdoors if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>Very high</strong></p></th>
		<th>
		<p><strong>Above 10</strong></p>
		</th>
		<th>
		  <p><strong>Avoid</strong> strenuous activities outdoors. Children and the elderly should also avoid outdoor physical exertion.</p>
		</th>
		<th>
		  <p><strong>Reduce</strong> or reschedule strenuous activities outdoors, especially if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr> 
   </tbody>
</table>   



<blockquote><p> AQI (Air Quality Index) provides a number from 1 to 10+ to indicate the level of health risk associated with local air quality. </p></blockquote>
<table width="100%">
<tbody width="100%">
   <tr>
		<th><p><strong>Health Risk</strong></p></th>
		<th>
		<p><strong>AQHI</strong></p>
		</th>
		<th>
		  <p>Health Messages (<p><strong>Risk Population</strong>)  </p>
		</th>
		<th>
		  <p>Health Messages (<p><strong>General Population</strong>)</p>
		</th>
   </tr>
    <tr>
		<th><p><strong>Low</strong></p></th>
		<th>
		<p><strong>1–3</strong></p>
		</th>
		<th>
		  <p><strong>Enjoy</strong> your usual outdoor activities.</p>
		</th>
		<th>
		  <p><strong>Ideal</strong> air quality for outdoor activities</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>Moderate</strong></p></th>
		<th>
		<p><strong>4–6</strong></p>
		</th>
		<th>
		  <p><strong>Consider reducing</strong> or rescheduling strenuous activities outdoors if you are experiencing symptoms.</p>
		</th>
		<th>
		  <p><strong>No need to modify</strong> your usual outdoor activities unless you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>High</strong></p></th>
		<th>
		<p><strong>7-10</strong></p>
		</th>
		<th>
		  <p><strong>Reduce</strong> or reschedule strenuous activities outdoors. Children and the elderly should also take it easy.</p>
		</th>
		<th>
		  <p><strong>Consider reducing</strong> or rescheduling strenuous activities outdoors if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr>
   <tr>
		<th><p><strong>Very high</strong></p></th>
		<th>
		<p><strong>Above 10</strong></p>
		</th>
		<th>
		  <p><strong>Avoid</strong> strenuous activities outdoors. Children and the elderly should also avoid outdoor physical exertion.</p>
		</th>
		<th>
		  <p><strong>Reduce</strong> or reschedule strenuous activities outdoors, especially if you experience symptoms such as coughing and throat irritation.</p>
		</th>
   </tr> 
   </tbody>
</table>   
	