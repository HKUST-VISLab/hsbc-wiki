
# Heterogeneous Data Sources in PRAISE-HK
The fusion of heterogeneous datasets coming from different sources. For example, the AQ data modelled and measured by Tasks 1 and 2 output air quality prediction. The transportation data obtained from Task 4, and the result of the transportation modelling is predicted traffic condition. We will also collect other data such as images and videos from mobile apps developed in Task 7. As follows, we will describe the data format. 


## Air-Quality Data

Air-quality data are collected from 14 weather station monitoring the air quality in different regions in Hong Kong, "CL"(Central), "CB"(Causeway Bay), "MK"(Mong Kok),  "TC"(Tung Chung), "YL"(Yuen Long), "TW"(Tsuen Wan), "KC"(Kwai Chung), "CW"(Central Western), "SP"(Sham Shui Po), "TP"(Tai Po), "ST"(Sha Tin), "KT"(Kwun Tong), "EN"(Eastern), "TM"(Tap Mun). There are also 5 automatic weather station. The following data format also works for both static AQ data and AQ prediction. 


<blockquote><p> AQHI (Air Quality Health Index) provides a number from 1 to 10+ to indicate the air quality, which is grouped into five health risk categories with <a href="http://www.aqhi.gov.hk/en/health-advice/sub-health-advice.html"><strong>health advice from Hong Kong EPD</strong> </a>. </p></blockquote>
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



<blockquote><p> AQI (Air Quality Index) provides a number from 0-500 to indicate air quality, which is divided into six categories indicating increasing levels of health concern and providing health advice by <a href="www.EPA.gov">The United States EPA</a>.</p></blockquote>
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
		  <p>空氣污染風險很少</p>
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
		  <p>空氣質素可以接受</p>
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
		  <p>高危人士可能出現健康反應。公眾暫時未受影響。</p>
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
		  <p>高危人士可能出現較嚴重健康反應，部分公眾亦可能出現健康反應。</p>
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
		  <p>公眾出現健康反應。</p>
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
		  <p>部分公眾可能出現較嚴重健康反應。</p>
		</th>
		<th>
		  <p>Maroon</p>
		</th>
   </tr>    
   </tbody>
</table>   



<blockquote><p><a href="www.EPA.gov">The United States EPA</a> maintain a table of breakpoints in calculating AQI.</p></blockquote>
<table width="100%">
<tbody width="100%">
   <tr>
		<th><p><strong>O_3 (ppb)</strong></p></th>
		<th><p><strong>O_3 (ppb)</strong></p></th>
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
		  <p>空氣污染風險很少</p>
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
		  <p>空氣質素可以接受</p>
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
		  <p>高危人士可能出現健康反應。公眾暫時未受影響。</p>
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
		  <p>高危人士可能出現較嚴重健康反應，部分公眾亦可能出現健康反應。</p>
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
		  <p>公眾出現健康反應。</p>
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
		  <p>部分公眾可能出現較嚴重健康反應。</p>
		</th>
		<th>
		  <p>Maroon</p>
		</th>
   </tr>    
   </tbody>
</table>   
	