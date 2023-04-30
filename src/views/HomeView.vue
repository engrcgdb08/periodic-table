<template>
  <div class="home" :inline="true" style="align:center; width: 100%; height:auto;" >
<!-- fieldset buttons -->

<div class="container" :inline="true" style="margin:10px; display:flex; justify-content:center;">
<fieldset><legend><el-button type="info" plain style="font-weight:bold" @click="toggle2"> Metals </el-button></legend>
<el-button style="font-weight: bold; border-color: rgb(247, 210, 3); margin:5px;" @click="isAlkali = !isAlkali">Alkali Metals</el-button>
<el-button style=" font-weight: bold; border-color: rgb(244, 92, 216); margin:5px;" @click="isActinide = !isActinide">Actinide</el-button>
<el-button style=" font-weight: bold; border-color: rgb(230, 248, 63); margin:5px;" @click="isLanthanide = !isLanthanide">Lanthanide</el-button>
<el-button style="font-weight: bold; border-color: rgb(255, 148, 66); margin:5px;" @click="isTransitionMetals = !isTransitionMetals">Transition Metals</el-button>
<el-button style=" font-weight: bold; border-color: rgb(207, 153, 52); margin:5px;" @click="isTransitionMetalsEarth = !isTransitionMetalsEarth">Transition Earth Metals</el-button>
<el-button style=" font-weight: bold; border-color: rgb(122, 255, 204); margin:5px;"  @click="isPostTransitionMetals = !isPostTransitionMetals">Post-transition Metals</el-button>
</fieldset>


<legend><el-button type="warning" plain @click="isMetalloids = !isMetalloids" style="font-weight:bold;"> Metalloids </el-button></legend>

<fieldset><legend><el-button type="success" plain style="font-weight:bold" @click="toggle"> Non Metals</el-button></legend>
<el-button  @click="isnobleGas = !isnobleGas">Noble Gases</el-button>
<el-button  @click="isReactiveNonMetals = !isReactiveNonMetals">Reactive Non-Metals</el-button>
</fieldset>


<legend><el-button type="warning" plain  @click="isUnknown = !isUnknown" style="font-weight:bold;"> Unknown </el-button></legend>


<legend><el-button type="primary" plain @click="isLiquid = !isLiquid" style="font-weight:bold;"> Liquid </el-button></legend>

<legend><el-button type="success" plain @click="isGas = !isGas" style="font-weight:bold;"> Gas </el-button></legend>

<legend><el-button type="info" plain @click="isSolid = !isSolid" style="font-weight:bold;"> Solid </el-button></legend>

</div>
<div class="group1">
  <h3>1</h3>

   <el-button :class="{gas:isGas , reactiveNonMetals: isReactiveNonMetals}" class="box-card" style="margin-bottom:5px;border:5px solid; border-color: rgb(237, 100, 255);" @click="hydrogenVisible">
  <div class="header">
    <span class="atomicNumber">1</span>
    <span class="atomicMass" >1.0079</span>
  </div>
  <div class="symbol">
    <span>H</span>
  </div>
  <div class="atomicName">
  <span>Hydrogen</span>
  <br/>
  </div>
 </el-button>
 <br/>

 <el-button :class="{solid:isSolid, alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="lithiumVisible">
  <div class="header">
    <span class="atomicNumber">3</span>
    <span class="atomicMass" >6.941</span>
  </div>
  <div class="symbol">
    <span>Li</span>
  </div>
  <div class="atomicName">
  <span>Lithium</span>
  <br/>
  </div>
 </el-button>
  <br/>


     <el-button :class="{solid:isSolid, alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="sodiumVisible">
  <div class="header">
    <span class="atomicNumber">11</span>
    <span class="atomicMass" >22.9897</span>
  </div>
  <div class="symbol">
    <span>Na</span>
  </div>
  <div class="atomicName">
  <span>Sodium</span>
  <br/>
  </div>
  </el-button>
  <br/>

   <el-button :class="{solid:isSolid, alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="potassiumVisible">

  <div class="header">
    <span class="atomicNumber">19</span>
    <span class="atomicMass" >39.0983</span>
  </div>
  <div class="symbol">
    <span>K</span>
  </div>
  <div class="atomicName">
  <span>Potassium</span>
  <br/>
  </div>
   </el-button>
   <br/>


      <el-button :class="{solid:isSolid,alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="rubidiumVisible">
  <div class="header">
    <span class="atomicNumber">37</span>
    <span class="atomicMass" >85.4678</span>
  </div>
  <div class="symbol">
    <span>Rb</span>
  </div>
  <div class="atomicName">
  <span>Rubidium</span>
  <br/>
  </div>
      </el-button>
      <br/>



 <el-button :class="{solid:isSolid, alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="cesiumVisible">
  <div class="header">
    <span class="atomicNumber">55</span>
    <span class="atomicMass" >132.91</span>
  </div>
  <div class="symbol">
    <span>Cs</span>
  </div>
  <div class="atomicName">
  <span>Cesium</span>
  <br/>
  </div>
 </el-button>
 <br/>


 <el-button :class="{solid:isSolid,alkali:isAlkali}" class="box-card" style="border:5px solid; border-color: rgb(247, 210, 3);" @click="franciumVisible">
  <div class="header">
    <span class="atomicNumber">87</span>
    <span class="atomicMass" >223</span>
  </div>
  <div class="symbol">
    <span>Fr</span>
  </div>
  <div class="atomicName">
  <span>Francium</span>
  <br/>
  </div>
 </el-button>
 <br/>


</div>



<div class="group2">
  <h3>2</h3>

   <el-button :class="{solid:isSolid,transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="berylliumVisible">
   
  <div class="header">
    <span class="atomicNumber">4</span>
    <span class="atomicMass" >9.0122</span>
  </div>
  <div class="symbol">
    <span>Be</span>
  </div>
  <div class="atomicName">
  <span>Beryllium</span>
  <br/>
  </div>
   </el-button>
<br/>

   <el-button :class="{solid:isSolid, transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="magnesiumVisible">
  <div class="header">
    <span class="atomicNumber">12</span>
    <span class="atomicMass" >24.305</span>
  </div>
  <div class="symbol">
    <span>Mg</span>
  </div>
  <div class="atomicName">
  <span>Magnesium</span>
  <br/>
  </div>
   </el-button>
   <br/>


<el-button :class="{solid:isSolid, transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="calciumVisible">
  <div class="header">
    <span class="atomicNumber">20</span>
    <span class="atomicMass" >40.078</span>
  </div>
  <div class="symbol">
    <span>Ca</span>
  </div>
  <div class="atomicName">
  <span>Calcium</span>
  <br/>


  </div>
</el-button>
<br/>
<el-button :class="{solid:isSolid, transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="strontiumVisible">
  <div class="header">
    <span class="atomicNumber">38</span>
    <span class="atomicMass" >87.62</span>
  </div>
  <div class="symbol">
    <span>Sr</span>
  </div>
  <div class="atomicName">
  <span>Strontium</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{solid:isSolid, transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="bariumVisible">
  <div class="header">
    <span class="atomicNumber">56</span>
    <span class="atomicMass" >137.327</span>
  </div>
  <div class="symbol">
    <span>Ba</span>
  </div>
  <div class="atomicName">
  <span>Barium</span>
  <br/>
  </div>
</el-button>
<br/>

 <el-button :class="{solid:isSolid,transitionMetalsEarth:isTransitionMetalsEarth}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="radiumVisible">
  <div class="header">
    <span class="atomicNumber">88</span>
    <span class="atomicMass" >226</span>
  </div>
  <div class="symbol">
    <span>Ra</span>
  </div>
  <div class="atomicName">
  <span>Radium</span>
  <br/>
  </div>
 </el-button>
<br/>

</div>


<div class="group3">
  <h3>3</h3>
  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Scandium">
  <div class="header">
    <span class="atomicNumber">21</span>
    <span class="atomicMass" >44.9559</span>
  </div>
  <div class="symbol">
    <span>Sc</span>
  </div>
  <div class="atomicName">
  <span>Scandium</span>
  <br/>
  </div>
  </el-button>
  <br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Yttrium">
  <div class="header">
    <span class="atomicNumber">39</span>
    <span class="atomicMass" >88.9059</span>
  </div>
  <div class="symbol">
    <span>Y</span>
  </div>
  <div class="atomicName">
  <span>Yttrium</span>
  <br/>
  </div>
  </el-button>
  <br/>



  <el-button class="box-card2" style="border:5px solid; border-color: rgb(0,0,0);">
  <div class="header">
    <span class="atomicNumber"></span>
    <span class="atomicMass" ></span>
  </div>
  <div style="margin-top:20px;">
    <span style="font-size: 25px;">57-71</span>
  </div>
  <div class="atomicName">
  <span></span>
<span></span>
  </div>
</el-button>
<br/>


  <el-button class="box-card2" style="border:5px solid; border-color: rgb(0,0,0);">
  <div class="header">
    <span class="atomicNumber"></span>
    <span class="atomicMass" ></span>
  </div>
  <div style="margin-top:20px;">
    <span style="font-size: 25px;">89-103</span>
  </div>
  <div class="atomicName">
  <span></span>
<span></span>
  </div>
</el-button>
<br/>

</div>

<div class="group4">
  <h3>4</h3>
<el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Titanium">
  <div class="header">
    <span class="atomicNumber">22</span>
    <span class="atomicMass" >47.867</span>
  </div>
  <div class="symbol">
    <span>Ti</span>
  </div>
  <div class="atomicName">
  <span>Titanium</span>
  <br/>
  </div>
</el-button>
<br/>

  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Zirconium">
  <div class="header">
    <span class="atomicNumber">40</span>
    <span class="atomicMass" >91.224</span>
  </div>
  <div class="symbol">
    <span>Zr</span>
  </div>
  <div class="atomicName">
  <span>Zirconium</span>
  <br/>
  </div>
</el-button>
<br/>


<el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Hafnium">
  <div class="header">
    <span class="atomicNumber">72</span>
    <span class="atomicMass" >178.49</span>
  </div>
  <div class="symbol">
    <span>Hf</span>
  </div>
  <div class="atomicName">
  <span>Hafnium</span>
  <br/>
  </div>
</el-button>
<br/>


  <el-button :class="{unknown:isUnknown , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Rutherfordium">
  <div class="header">
    <span class="atomicNumber">104</span>
    <span class="atomicMass" >261</span>
  </div>
  <div class="symbol">
    <span>Rf</span>
  </div>
  <div class="atomicName">
  <span>Rutherfordium</span>
  <br/>
  </div>
  </el-button>
  <br/>

<br/><br/>


<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Lanthanum">
  <div class="header">
    <span class="atomicNumber">57</span>
    <span class="atomicMass" >138.9055</span>
  </div>
  <div class="symbol">
    <span>La</span>
  </div>
  <div class="atomicName">
  <span>Lanthanum</span>
  <br/>
  </div>
</el-button>
<br/>


<el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Actinium">
  <div class="header">
    <span class="atomicNumber">89</span>
    <span class="atomicMass" >227</span>
  </div>
  <div class="symbol">
    <span>Ac</span>
  </div>
  <div class="atomicName">
  <span>Actinium</span>
  <br/>
  </div>
</el-button>
<br/>
</div>

<div class="group5">
  <h3>5</h3>
  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Vanadium">
  <div class="header">
    <span class="atomicNumber">23</span>
    <span class="atomicMass" >50.9415</span>
  </div>
  <div class="symbol">
    <span>V</span>
  </div>
  <div class="atomicName">
  <span>Vanadium</span>
  <br/>
  </div>
  </el-button>
  <br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Niobium">
  <div class="header">
    <span class="atomicNumber">41</span>
    <span class="atomicMass" >92.9064</span>
  </div>
  <div class="symbol">
    <span>Nb</span>
  </div>
  <div class="atomicName">
  <span>Niobium</span>
  <br/>
  </div>
  </el-button>
  <br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Tantalum">
  <div class="header">
    <span class="atomicNumber">73</span>
    <span class="atomicMass" >180.9479</span>
  </div>
  <div class="symbol">
    <span>Ta</span>
  </div>
  <div class="atomicName">
  <span>Tantalum</span>
  <br/>
  </div>
  </el-button>
  <br/>


  <el-button :class="{unknown:isUnknown , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Dubnium">
  <div class="header">
    <span class="atomicNumber">105</span>
    <span class="atomicMass" >262</span>
  </div>
  <div class="symbol">
    <span>Db</span>
  </div>
  <div class="atomicName">
  <span>Dubnium</span>
  <br/>
  </div>
  </el-button>
 <br/> 

<br/><br/>


<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Cerium">
  <div class="header">
    <span class="atomicNumber">58</span>
    <span class="atomicMass" >140.116</span>
  </div>
  <div class="symbol">
    <span>Ce</span>
  </div>
  <div class="atomicName">
  <span>Cerium</span>
  <br/>
  </div>
</el-button>
<br/>

    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Thorium">
  <div class="header">
    <span class="atomicNumber">90</span>
    <span class="atomicMass" >232.0381</span>
  </div>
  <div class="symbol">
    <span>Th</span>
  </div>
  <div class="atomicName">
  <span>Thorium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>

<div class="group6">
  <h3>6</h3>

     <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Chromium">
  <div class="header">
    <span class="atomicNumber">24</span>
    <span class="atomicMass" >51.9961</span>
  </div>
  <div class="symbol">
    <span>Cr</span>
  </div>
  <div class="atomicName">
  <span>Chromium</span>
  <br/>
  </div>
     </el-button>
     <br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Molybdenum">
  <div class="header">
    <span class="atomicNumber">42</span>
    <span class="atomicMass" >95.94</span>
  </div>
  <div class="symbol">
    <span>Mo</span>
  </div>
  <div class="atomicName">
  <span>Molybdenum</span>
  <br/>
  </div>
  </el-button>
  <br/>

<el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Tungsten">
  <div class="header">
    <span class="atomicNumber">74</span>
    <span class="atomicMass" >183.84</span>
  </div>
  <div class="symbol">
    <span>W</span>
  </div>
  <div class="atomicName">
  <span>Tungsten</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{unknown:isUnknown , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Seaborgium">
  <div class="header">
    <span class="atomicNumber">106</span>
    <span class="atomicMass" >266</span>
  </div>
  <div class="symbol">
    <span>Sg</span>
  </div>
  <div class="atomicName">
  <span>Seaborgium</span>
  <br/>
  </div>
</el-button>
<br/>


<br/><br/>

    <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Praseodymium">
  <div class="header">
    <span class="atomicNumber">59</span>
    <span class="atomicMass" >140.9077</span>
  </div>
  <div class="symbol">
    <span>Pr</span>
  </div>
  <div class="atomicName">
  <span>Praseodymium</span>
  <br/>
  </div>
    </el-button>
    <br/>


    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Protactinium">
  <div class="header">
    <span class="atomicNumber">91</span>
    <span class="atomicMass" >231.0359</span>
  </div>
  <div class="symbol">
    <span>Pa</span>
  </div>
  <div class="atomicName">
  <span>Protactinium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>

<div class="group7">
  <h3>7</h3>

 <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Manganese">
  <div class="header">
    <span class="atomicNumber">25</span>
    <span class="atomicMass" >54.938</span>
  </div>
  <div class="symbol">
    <span>Mn</span>
  </div>
  <div class="atomicName">
  <span>Manganese</span>
  <br/>
  </div>
 </el-button>
 <br/>

<el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Technetium">
  <div class="header">
    <span class="atomicNumber">43</span>
    <span class="atomicMass" >98</span>
  </div>
  <div class="symbol">
    <span>Tc</span>
  </div>
  <div class="atomicName">
  <span>Technetium</span>
  <br/>
  </div>
</el-button>
<br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Rhenium">
  <div class="header">
    <span class="atomicNumber">75</span>
    <span class="atomicMass" >186.207</span>
  </div>
  <div class="symbol">
    <span>Re</span>
  </div>
  <div class="atomicName">
  <span>Rhenium</span>
  <br/>
  </div>
  </el-button>
  <br/>

  
    <el-button :class="{unknown:isUnknown , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);"  @click="Bohrium">
  <div class="header">
    <span class="atomicNumber">107</span>
    <span class="atomicMass" >264</span>
  </div>
  <div class="symbol">
    <span>Bh</span>
  </div>
  <div class="atomicName">
  <span>Bohrium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>

<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);"  @click="Neodymium">
  <div class="header">
    <span class="atomicNumber">60</span>
    <span class="atomicMass" >144.24</span>
  </div>
  <div class="symbol">
    <span>Nd</span>
  </div>
  <div class="atomicName">
  <span>Neodymium</span>
  <br/>
  </div>
</el-button>
<br/>

 
    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);"  @click="Uranium">
  <div class="header">
    <span class="atomicNumber">92</span>
    <span class="atomicMass" >238.0289</span>
  </div>
  <div class="symbol">
    <span>U</span>
  </div>
  <div class="atomicName">
  <span>Uranium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>


<div class="group8">
  <h3>8</h3>
      <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);"  @click="Iron">
  <div class="header">
    <span class="atomicNumber">26</span>
    <span class="atomicMass" >55.845</span>
  </div>
  <div class="symbol">
    <span>Fe</span>
  </div>
  <div class="atomicName">
  <span>Iron</span>
  <br/>
  </div>
      </el-button>
      <br/>

 
  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);"  @click="Ruthenium">
  <div class="header">
    <span class="atomicNumber">44</span>
    <span class="atomicMass" >101.07</span>
  </div>
  <div class="symbol">
    <span>Ru</span>
  </div>
  <div class="atomicName">
  <span>Ruthenium</span>
  <br/>
  </div>
  </el-button>
  <br/>


  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);"  @click="Osmium">
  <div class="header">
    <span class="atomicNumber">76</span>
    <span class="atomicMass" >190.23</span>
  </div>
  <div class="symbol">
    <span>Os</span>
  </div>
  <div class="atomicName">
  <span>Osmium</span>
  <br/>
  </div>
  </el-button>
  <br/>


  
    <el-button :class="{unknown:isUnknown , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Hassium">
  <div class="header">
    <span class="atomicNumber">108</span>
    <span class="atomicMass" >277</span>
  </div>
  <div class="symbol">
    <span>Hs</span>
  </div>
  <div class="atomicName">
  <span>Hassium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>


    <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Promethium">
  <div class="header">
    <span class="atomicNumber">61</span>
    <span class="atomicMass" >145</span>
  </div>
  <div class="symbol">
    <span>Pm</span>
  </div>
  <div class="atomicName">
  <span>Promethium</span>
  <br/>
  </div>
    </el-button>
    <br/>

 
    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Neptunium">
  <div class="header">
    <span class="atomicNumber">93</span>
    <span class="atomicMass" >237</span>
  </div>
  <div class="symbol">
    <span>Np</span>
  </div>
  <div class="atomicName">
  <span>Neptunium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>


<div class="group9">
  <h3>9</h3>

    <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Cobalt">
  <div class="header">
    <span class="atomicNumber">27</span>
    <span class="atomicMass" >58.9332</span>
  </div>
  <div class="symbol">
    <span>Co</span>
  </div>
  <div class="atomicName">
  <span>Cobalt</span>
  <br/>
  </div>
    </el-button>
    <br/>


  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Rhodium">
  <div class="header">
    <span class="atomicNumber">45</span>
    <span class="atomicMass" >102.9055</span>
  </div>
  <div class="symbol">
    <span>Rh</span>
  </div>
  <div class="atomicName">
  <span>Rhodium</span>
  <br/>
  </div>
  </el-button>
  <br/>

  <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Iridium">
  <div class="header">
    <span class="atomicNumber">77</span>
    <span class="atomicMass" >196.9665</span>
  </div>
  <div class="symbol">
    <span>Ir</span>
  </div>
  <div class="atomicName">
  <span>Iridium</span>
  <br/>
  </div>
  </el-button>
  <br/>

 
    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Meitnerium">
  <div class="header">
    <span class="atomicNumber">109</span>
    <span class="atomicMass" >268</span>
  </div>
  <div class="symbol">
    <span>Mt</span>
  </div>
  <div class="atomicName">
  <span>Meitnerium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>


<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Samarium">
  <div class="header">
    <span class="atomicNumber">62</span>
    <span class="atomicMass" >150.36</span>
  </div>
  <div class="symbol">
    <span>Sm</span>
  </div>
  <div class="atomicName">
  <span>Samarium</span>
  <br/>
  </div>
</el-button>
<br/>


 <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Plutonium">
  <div class="header">
    <span class="atomicNumber">94</span>
    <span class="atomicMass" >244</span>
  </div>
  <div class="symbol">
    <span>Pu</span>
  </div>
  <div class="atomicName">
  <span>Plutonium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>


<div class="group10">
  <h3>10</h3>

     <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Nickel">
  <div class="header">
    <span class="atomicNumber">28</span>
    <span class="atomicMass" >58.6934</span>
  </div>
  <div class="symbol">
    <span>Ni</span>
  </div>
  <div class="atomicName">
  <span>Nickel</span>
  <br/>
  </div>
     </el-button>
     <br/>


  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Palladium">
  <div class="header">
    <span class="atomicNumber">46</span>
    <span class="atomicMass" >106.42</span>
  </div>
  <div class="symbol">
    <span>Pd</span>
  </div>
  <div class="atomicName">
  <span>Palladium</span>
  <br/>
  </div>
  </el-button>
  <br/>


    <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Platinum">
  <div class="header">
    <span class="atomicNumber">78</span>
    <span class="atomicMass" >192.217</span>
  </div>
  <div class="symbol">
    <span>Pt</span>
  </div>
  <div class="atomicName">
  <span>Platinum</span>
  <br/>
  </div>
    </el-button>
    <br/>

    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Darmstadtium">
  <div class="header">
    <span class="atomicNumber">110</span>
    <span class="atomicMass" >261.9</span>
  </div>
  <div class="symbol">
    <span>Ds</span>
  </div>
  <div class="atomicName">
  <span>Darmstadtium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>

 
       <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Europium">
  <div class="header">
    <span class="atomicNumber">63</span>
    <span class="atomicMass" >151.964</span>
  </div>
  <div class="symbol">
    <span>Eu</span>
  </div>
  <div class="atomicName">
  <span>Europium</span>
  <br/>
  </div>
       </el-button>
       <br/>

     
       <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Americium">
  <div class="header">
    <span class="atomicNumber">95</span>
    <span class="atomicMass" >243</span>
  </div>
  <div class="symbol">
    <span>Am</span>
  </div>
  <div class="atomicName">
  <span>Americium</span>
  <br/>
  </div>
       </el-button>
       <br/>

</div>

<div class="group11">
  <h3>11</h3>
  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Copper">
  <div class="header">
    <span class="atomicNumber">29</span>
    <span class="atomicMass" >63.546</span>
  </div>
  <div class="symbol">
    <span>Cu</span>
  </div>
  <div class="atomicName">
  <span>Copper</span>
  <br/>
  </div>
  </el-button>
  <br/>


   <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Silver">
  <div class="header">
    <span class="atomicNumber">47</span>
    <span class="atomicMass" >107.8682</span>
  </div>
  <div class="symbol">
    <span>Ag</span>
  </div>
  <div class="atomicName">
  <span>Silver</span>
  <br/>
  </div>
   </el-button>
   <br/>

<el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Gold">
  <div class="header">
    <span class="atomicNumber">79</span>
    <span class="atomicMass" >195.078</span>
  </div>
  <div class="symbol">
    <span>Au</span>
  </div>
  <div class="atomicName">
  <span>Gold</span>
  <br/>
  </div>
</el-button>
<br/>

 
    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Roentgenium">
  <div class="header">
    <span class="atomicNumber">111</span>
    <span class="atomicMass" >271.8</span>
  </div>
  <div class="symbol">
    <span>Rg</span>
  </div>
  <div class="atomicName">
  <span>Roentgenium</span>
  <br/>
  </div>
    </el-button>
   <br/> 

<br/><br/>


     <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Gadolinium">
  <div class="header">
    <span class="atomicNumber">64</span>
    <span class="atomicMass" >157.25</span>
  </div>
  <div class="symbol">
    <span>Gd</span>
  </div>
  <div class="atomicName">
  <span>Gadolinium</span>
  <br/>
  </div>
     </el-button>
     <br/>

  
<el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Curium">
  <div class="header">
    <span class="atomicNumber">96</span>
    <span class="atomicMass" >247</span>
  </div>
  <div class="symbol">
    <span>Cm</span>
  </div>
  <div class="atomicName">
  <span>Curium</span>
  <br/>
  </div>
</el-button>
<br/>

</div>


<div class="group12">
  <h3>12</h3>
  <el-button :class="{solid:isSolid, transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Zinc">
  <div class="header">
    <span class="atomicNumber">30</span>
    <span class="atomicMass" >65.39</span>
  </div>
  <div class="symbol">
    <span>Zn</span>
  </div>
  <div class="atomicName">
  <span>Zinc</span>
  <br/>
  </div>
  </el-button>
  <br/>


   <el-button :class="{solid:isSolid,transitionMetals:isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Cadmium">
  <div class="header">
    <span class="atomicNumber">48</span>
    <span class="atomicMass" >112.411</span>
  </div>
  <div class="symbol">
    <span>Cd</span>
  </div>
  <div class="atomicName">
  <span>Cadmium</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{liquid:isLiquid , transitionMetals: isTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Mercury">
  <div class="header">
    <span class="atomicNumber">80</span>
    <span class="atomicMass" >200.59</span>
  </div>
  <div class="symbol">
    <span>Hg</span>
  </div>
  <div class="atomicName">
  <span>Mercury</span>
  <br/>
  </div>
</el-button>
<br/>


    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Copernicium">
  <div class="header">
    <span class="atomicNumber">112</span>
    <span class="atomicMass" >285</span>
  </div>
  <div class="symbol">
    <span>Cn</span>
  </div>
  <div class="atomicName">
  <span>Copernicium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>

 <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Terbium">
  <div class="header">
    <span class="atomicNumber">65</span>
    <span class="atomicMass" >158.9253</span>
  </div>
  <div class="symbol">
    <span>Tb</span>
  </div>
  <div class="atomicName">
  <span>Terbium</span>
  <br/>
  </div>
 </el-button>
 <br/>


<el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Berkelium">
  <div class="header">
    <span class="atomicNumber">97</span>
    <span class="atomicMass" >247</span>
  </div>
  <div class="symbol">
    <span>Bk</span>
  </div>
  <div class="atomicName">
  <span>Berkelium</span>
  <br/>
  </div>
</el-button>
<br/>

</div>


<div class="group13">
  <h3>13</h3>


  <el-button :class="{solid:isSolid, metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Boron">
  <div class="header">
    <span class="atomicNumber">5</span>
    <span class="atomicMass" >10.811</span>
  </div>
  <div class="symbol">
    <span>B</span>
  </div>
  <div class="atomicName">
  <span>Boron</span>
  <br/>
  </div>
  </el-button>
  <br/>

<el-button :class="{solid:isSolid, postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Aluminium">
  <div class="header">
    <span class="atomicNumber">13</span>
    <span class="atomicMass" >65.39</span>
  </div>
  <div class="symbol">
    <span>Al</span>
  </div>
  <div class="atomicName">
  <span>Aluminium</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{solid:isSolid, postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Gallium">
  <div class="header">
    <span class="atomicNumber">31</span>
    <span class="atomicMass" >69.723</span>
  </div>
  <div class="symbol">
    <span>Ga</span>
  </div>
  <div class="atomicName">
  <span>Gallium</span>
  <br/>
  </div>
</el-button>
<br/>


  <el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Indium">
  <div class="header">
    <span class="atomicNumber">49</span>
    <span class="atomicMass" >114.818</span>
  </div>
  <div class="symbol">
    <span>In</span>
  </div>
  <div class="atomicName">
  <span>Indium</span>
  <br/>
  </div>
  </el-button>
  <br/>

   
    <el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Thallium">
  <div class="header">
    <span class="atomicNumber">81</span>
    <span class="atomicMass" >204.3833</span>
  </div>
  <div class="symbol">
    <span>Tl</span>
  </div>
  <div class="atomicName">
  <span>Thallium</span>
  <br/>
  </div>
    </el-button>
    <br/>


     <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Nihonium">
  <div class="header">
    <span class="atomicNumber">113</span>
    <span class="atomicMass" >286</span>
  </div>
  <div class="symbol">
    <span>Nh</span>
  </div>
  <div class="atomicName">
  <span>Nihonium</span>
  <br/>
  </div>
     </el-button>

<br/><br/><br/>

  
<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Dysprosium">
  <div class="header">
    <span class="atomicNumber">66</span>
    <span class="atomicMass" >162.5</span>
  </div>
  <div class="symbol">
    <span>Dy</span>
  </div>
  <div class="atomicName">
  <span>Dysprosium</span>
  <br/>
  </div>
</el-button>
<br/>


    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Californium">
  <div class="header">
    <span class="atomicNumber">98</span>
    <span class="atomicMass" >251</span>
  </div>
  <div class="symbol">
    <span>Cf</span>
  </div>
  <div class="atomicName">
  <span>Californium</span>
  <br/>
  </div>
    </el-button>
    <br/>

</div>

<div class="group14">
  <h3>14</h3>


  <el-button :class="{solid:isSolid, reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Carbon">
  <div class="header">
    <span class="atomicNumber">6</span>
    <span class="atomicMass" >12.0107</span>
  </div>
  <div class="symbol">
    <span>C</span>
  </div>
  <div class="atomicName">
  <span>Carbon</span>
  <br/>
  </div>
    </el-button>
    <br/>

 
    <el-button :class="{solid:isSolid, metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Silicon">
  <div class="header">
    <span class="atomicNumber">14</span>
    <span class="atomicMass" >28.0855</span>
  </div>
  <div class="symbol">
    <span>Si</span>
  </div>
  <div class="atomicName">
  <span>Silicon</span>
  <br/>
  </div>
    </el-button>
    <br/>



   <el-button :class="{solid:isSolid, metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Germanium">
  <div class="header">
    <span class="atomicNumber">32</span>
    <span class="atomicMass" >72.64</span>
  </div>
  <div class="symbol">
    <span>Ge</span>
  </div>
  <div class="atomicName">
  <span>Germanium</span>
  <br/>
  </div>
   </el-button>
   <br/>


    <el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Tin">
  <div class="header">
    <span class="atomicNumber">50</span>
    <span class="atomicMass" >118.71</span>
  </div>
  <div class="symbol">
    <span>Sn</span>
  </div>
  <div class="atomicName">
  <span>Tin</span>
  <br/>
  </div>
    </el-button>
    <br/>

  
 <el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Lead">
  <div class="header">
    <span class="atomicNumber">82</span>
    <span class="atomicMass" >207.2</span>
  </div>
  <div class="symbol">
    <span>Pb</span>
  </div>
  <div class="atomicName">
  <span>Lead</span>
  <br/>
  </div>
 </el-button>
 <br/>


     <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Flerovium">
  <div class="header">
    <span class="atomicNumber">114</span>
    <span class="atomicMass" >289</span>
  </div>
  <div class="symbol">
    <span>Fl</span>
  </div>
  <div class="atomicName">
  <span>Flerovium</span>
  <br/>
  </div>
     </el-button>
     <br/>

<br/><br/>


  <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Holmium">
  <div class="header">
    <span class="atomicNumber">67</span>
    <span class="atomicMass" >164.9303</span>
  </div>
  <div class="symbol">
    <span>Ho</span>
  </div>
  <div class="atomicName">
  <span>Holmium</span>
  <br/>
  </div>
  </el-button>
  <br/>

 
  <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Einsteinium">
  <div class="header">
    <span class="atomicNumber">99</span>
    <span class="atomicMass" >252</span>
  </div>
  <div class="symbol">
    <span>Es</span>
  </div>
  <div class="atomicName">
  <span>Einsteinium</span>
  <br/>
  </div>
  </el-button>
  <br/>

</div>

<div class="group15">
  <h3>15</h3>


<el-button :class="{gas:isGas , reactiveNonMetals: isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Nitrogen">
  <div class="header">
    <span class="atomicNumber">7</span>
    <span class="atomicMass" >14.0067</span>
  </div>
  <div class="symbol">
    <span>N</span>
  </div>
  <div class="atomicName">
  <span>Nitrogen</span>
  <br/>
  </div>
</el-button>
<br/>

  
    <el-button :class="{solid:isSolid,reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255);" @click="Phosphorus">
  <div class="header">
    <span class="atomicNumber">15</span>
    <span class="atomicMass" >30.9738</span>
  </div>
  <div class="symbol">
    <span>P</span>
  </div>
  <div class="atomicName">
  <span>Phosphorus</span>
  <br/>
  </div>
    </el-button>
    <br/>


 
  <el-button :class="{solid:isSolid, metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Arsenic">
  <div class="header">
    <span class="atomicNumber">33</span>
    <span class="atomicMass" >74.9216</span>
  </div>
  <div class="symbol">
    <span>As</span>
  </div>
  <div class="atomicName">
  <span>Arsenic</span>
  <br/>
  </div>
  </el-button>
  <br/>

     <el-button :class="{solid:isSolid,metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Antimony">
  <div class="header">
    <span class="atomicNumber">51</span>
    <span class="atomicMass" >121.76</span>
  </div>
  <div class="symbol">
    <span>Sb</span>
  </div>
  <div class="atomicName">
  <span>Antimony</span>
  <br/>
  </div>
     </el-button>
     <br/>

<el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Bismuth">
  <div class="header">
    <span class="atomicNumber">83</span>
    <span class="atomicMass" >208.9804</span>
  </div>
  <div class="symbol">
    <span>Bi</span>
  </div>
  <div class="atomicName">
  <span>Bismuth</span>
  <br/>
  </div>
</el-button>
<br/>

    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Moscovium">
  <div class="header">
    <span class="atomicNumber">115</span>
    <span class="atomicMass" >288</span>
  </div>
  <div class="symbol">
    <span>Mc</span>
  </div>
  <div class="atomicName">
  <span>Moscovium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>


<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Erbium">
  <div class="header">
    <span class="atomicNumber">68</span>
    <span class="atomicMass" >167.259</span>
  </div>
  <div class="symbol">
    <span>Er</span>
  </div>
  <div class="atomicName">
  <span>Erbium</span>
  <br/>
  </div>
</el-button>
<br/>


<el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Fermium">
  <div class="header">
    <span class="atomicNumber">100</span>
    <span class="atomicMass" >257</span>
  </div>
  <div class="symbol">
    <span>Fm</span>
  </div>
  <div class="atomicName">
  <span>Fermium</span>
  <br/>
  </div>
</el-button>
<br/>

</div>


<div class="group16">
  <h3>16</h3>


    <el-button :class="{gas:isGas , reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Oxygen">
  <div class="header">
    <span class="atomicNumber">8</span>
    <span class="atomicMass" >15.9994</span>
  </div>
  <div class="symbol">
    <span>O</span>
  </div>
  <div class="atomicName">
  <span>Oxygen</span>
  <br/>
  </div>
    </el-button>
    <br/>


    <el-button :class="{solid:isSolid,reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255);" @click="Sulfur">
  <div class="header">
    <span class="atomicNumber">16</span>
    <span class="atomicMass" >32.065</span>
  </div>
  <div class="symbol">
    <span>S</span>
  </div>
  <div class="atomicName">
  <span>Sulfur</span>
  <br/>
  </div>
    </el-button>
    <br/>


 <el-button :class="{solid:isSolid, reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Selenium">
  <div class="header">
    <span class="atomicNumber">34</span>
    <span class="atomicMass" >78.96</span>
  </div>
  <div class="symbol">
    <span>Se</span>
  </div>
  <div class="atomicName">
  <span>Selenium</span>
  <br/>
  </div>
 </el-button>
 <br/>


  <el-button :class="{solid:isSolid, metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Tellurium">
  <div class="header">
    <span class="atomicNumber">52</span>
    <span class="atomicMass" >127.6</span>
  </div>
  <div class="symbol">
    <span>Te</span>
  </div>
  <div class="atomicName">
  <span>Tellurium</span>
  <br/>
  </div>
  </el-button>
  <br/>

     
<el-button :class="{solid:isSolid,postTransitionMetals:isPostTransitionMetals}" class="box-card" style="border:5px solid; border-color: rgb(122, 255, 204);" @click="Polonium">
  <div class="header">
    <span class="atomicNumber">84</span>
    <span class="atomicMass" >209</span>
  </div>
  <div class="symbol">
    <span>Po</span>
  </div>
  <div class="atomicName">
  <span>Polonium</span>
  <br/>
  </div>
</el-button>
<br/>


    <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Livermorium">
  <div class="header">
    <span class="atomicNumber">116</span>
    <span class="atomicMass" >293</span>
  </div>
  <div class="symbol">
    <span>Lv</span>
  </div>
  <div class="atomicName">
  <span>Livermorium</span>
  <br/>
  </div>
    </el-button>
    <br/>

<br/><br/>

  <el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Thulium">
  <div class="header">
    <span class="atomicNumber">69</span>
    <span class="atomicMass" >168.9342</span>
  </div>
  <div class="symbol">
    <span>Tm</span>
  </div>
  <div class="atomicName">
  <span>Thulium</span>
  <br/>
  </div>
  </el-button>
  <br/>

 
      <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Mendelevium">
  <div class="header">
    <span class="atomicNumber">101</span>
    <span class="atomicMass" >258</span>
  </div>
  <div class="symbol">
    <span>Md</span>
  </div>
  <div class="atomicName">
  <span>Mendelevium</span>
  <br/>
  </div>
      </el-button>
      <br/>

</div>

<div class="group17">
  <h3>17</h3>

  <el-button :class="{gas:isGas , reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Fluorine">
  <div class="header">
    <span class="atomicNumber">9</span>
    <span class="atomicMass" >18.9984</span>
  </div>
  <div class="symbol">
    <span>F</span>
  </div>
  <div class="atomicName">
  <span>Fluorine</span>
  <br/>
  </div>
</el-button>
<br/>


 <el-button :class="{gas:isGas , reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Chlorine">
  <div class="header">
    <span class="atomicNumber">17</span>
    <span class="atomicMass" >35.453</span>
  </div>
  <div class="symbol">
    <span>Cl</span>
  </div>
  <div class="atomicName">
  <span>Chlorine</span>
  <br/>
  </div>
 </el-button>
 <br/>


 <el-button :class="{liquid:isLiquid , reactiveNonMetals: isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color: rgb(237, 100, 255);" @click="Bromine">
  <div class="header">
    <span class="atomicNumber">35</span>
    <span class="atomicMass" >79.904</span>
  </div>
  <div class="symbol">
    <span>Br</span>
  </div>
  <div class="atomicName">
  <span>Bromine</span>
  <br/>
  </div>
 </el-button>
 <br/>


<el-button :class="{solid:isSolid, reactiveNonMetals:isReactiveNonMetals}" class="box-card" style="border:5px solid; border-color:rgb(237, 100, 255) ;" @click="Iodine">
  <div class="header">
    <span class="atomicNumber">53</span>
    <span class="atomicMass" >126.9045</span>
  </div>
  <div class="symbol">
    <span>I</span>
  </div>
  <div class="atomicName">
  <span>Iodine</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{solid:isSolid,metalloids:isMetalloids}" class="box-card" style="border:5px solid; border-color: #41ff5a;" @click="Astatine">
  <div class="header">
    <span class="atomicNumber">85</span>
    <span class="atomicMass" >210</span>
  </div>
  <div class="symbol">
    <span>At</span>
  </div>
  <div class="atomicName">
  <span>Astatine</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Tennessine">
  <div class="header">
    <span class="atomicNumber">117</span>
    <span class="atomicMass" >260.9</span>
  </div>
  <div class="symbol">
    <span>Ts</span>
  </div>
  <div class="atomicName">
  <span>Tennessine</span>
  <br/>
  </div>
</el-button>

<br/><br/><br/>

<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Ytterbium">
  <div class="header">
    <span class="atomicNumber">70</span>
    <span class="atomicMass" >173.04</span>
  </div>
  <div class="symbol">
    <span>Yb</span>
  </div>
  <div class="atomicName">
  <span>Ytterbium</span>
  <br/>
  </div>
</el-button>
<br/>



<el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Nobelium">
  <div class="header">
    <span class="atomicNumber">102</span>
    <span class="atomicMass" >259</span>
  </div>
  <div class="symbol">
    <span>No</span>
  </div>
  <div class="atomicName">
  <span>Nobelium</span>
  <br/>
  </div>
</el-button>
<br/>

</div>


<div class="group18">
  <h3>18</h3>


<el-button :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Helium">
  <div class="header">
    <span class="atomicNumber">2</span>
    <span class="atomicMass" >4.0026</span>
  </div>
  <div class="symbol">
    <span>He</span>
  </div>
  <div class="atomicName">
  <span>Helium</span>
  <br/>
  </div>
</el-button>
<br/>

<el-button :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Neon">
  <div class="header">
    <span class="atomicNumber">10</span>
    <span class="atomicMass" >20.1797</span>
  </div>
  <div class="symbol">
    <span>Ne</span>
  </div>
  <div class="atomicName">
  <span>Neon</span>
  <br/>
  </div>
</el-button>
<br/>

  <el-button  :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Argon">
  <div class="header">
    <span class="atomicNumber">18</span>
    <span class="atomicMass" >39.948</span>
  </div>
  <div class="symbol">
    <span>Ar</span>
  </div>
  <div class="atomicName">
  <span>Argon</span>
  <br/>
  </div>
  </el-button>
  <br/>

  <el-button :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Krypton">
  <div class="header">
    <span class="atomicNumber">36</span>
    <span class="atomicMass" >83.8</span>
  </div>
  <div class="symbol">
    <span>Kr</span>
  </div>
  <div class="atomicName">
  <span>Krypton</span>
  <br/>
  </div>
  </el-button>
  <br/>

 <el-button :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Xenon">
  <div class="header">
    <span class="atomicNumber">54</span>
    <span class="atomicMass" >131.293</span>
  </div>
  <div class="symbol">
    <span>Xe</span>
  </div>
  <div class="atomicName">
  <span>Xenon</span>
  <br/>
  </div>
 </el-button>
 <br/>


 <el-button :class="{gas:isGas , nobleGas:isnobleGas}" class="box-card" style="border:5px solid; border-color:rgb(60, 255, 229) ;" @click="Radon">
  <div class="header">
    <span class="atomicNumber">86</span>
    <span class="atomicMass" >222</span>
  </div>
  <div class="symbol">
    <span>Rn</span>
  </div>
  <div class="atomicName">
  <span>Radon</span>
  <br/>
  </div>
 </el-button>
 <br/>


  <el-button :class="{unknown:isUnknown}" class="box-card" style="border:5px solid; border-color: rgb(255, 148, 66);" @click="Oganesson">
  <div class="header">
    <span class="atomicNumber">118</span>
    <span class="atomicMass" >294</span>
  </div>
  <div class="symbol">
    <span>Og</span>
  </div>
  <div class="atomicName">
  <span>Oganesson</span>
  <br/>
  </div>
  </el-button>
  <br/>

<br/><br/>

<el-button :class="{lanthanide:isLanthanide}" class="box-card" style="border:5px solid; border-color: rgb(243, 254, 148);" @click="Lutetium">
  <div class="header">
    <span class="atomicNumber">71</span>
    <span class="atomicMass" >174.967</span>
  </div>
  <div class="symbol">
    <span>Lu</span>
  </div>
  <div class="atomicName">
  <span>Lutetium</span>
  <br/>
  </div>
</el-button>
<br/>

    <el-button :class="{actinide:isActinide}" class="box-card" style="border:5px solid; border-color: rgb(244, 92, 216);" @click="Lawrencium">
  <div class="header">
    <span class="atomicNumber">103</span>
    <span class="atomicMass" >262</span>
  </div>
  <div class="symbol">
    <span>Lr</span>
  </div>
  <div class="atomicName">
  <span>Lawrencium</span>
  <br/>
  </div>
    </el-button>
    <br/>
</div>


<el-dialog
  :title="this.title"
  :visible.sync="dialogVisible"
  width="30%"
  :before-close="handleClose"
  style="font-size:25px" >
   <img :src="this.image" style="width:300px; height: 300px; border-radius: 50%">
   
    <el-card align="center">
<span style="float:left; font-size:25px">Series:</span>  <span style="float:right; font-size:25px"> {{this.series}} </span>
   <br/><br/>
  <span style="float:left; font-size:25px">Symbol:</span>  <span style="float:right; font-size:25px"> {{this.symbol}} </span>
   <br/><br/>
      <span style="float:left; font-size:25px">Atomic Number:</span>  <span style="float:right; font-size:25px"> {{this.atomicNumber}} </span>
   <br/><br/>
  <span style="float:left; font-size:25px">Atomic Mass:</span>  <span style="float:right; font-size:25px"> {{this.atomicMass}} </span>
   <br/><br/>
      <span style="float:left; font-size:25px">Discovered By:</span>  <span style="float:right; font-size:25px"> {{this.discoveredBy}} </span>
   <br/><br/>
      <span style="float:left; font-size:25px">Discovery Year:</span>  <span style="float:right; font-size:25px"> {{this.discovery}} </span>

<br/><br/>
      <span style="float:left; font-size:25px">Group:</span>  <span style="float:right; font-size:25px"> {{this.group}} </span>
      <br/><br/>
      <span style="float:left; font-size:25px">Period:</span>  <span style="float:right; font-size:25px"> {{this.period}} </span>
      <br/><br/>
      <span style="float:left; font-size:25px">Blocks:</span>  <span style="float:right; font-size:25px"> {{this.blocks}} </span>
<br/><br/>
      <span style="float:left; font-size:25px">Phyisical State:</span>  <span style="float:right; font-size:25px"> {{this.physicalState}} </span>
      <br/><br/>
      <span style="float:left; font-size:25px">Electronic Configuration:</span>  <span style="float:right; font-size:25px"> {{this.electronicConfiguration}} </span>
      <br/><br/>
      <span style="float:left; font-size:25px">Number of Isotopes:</span>  <span style="float:right; font-size:25px"> {{this.isotopes}} </span>
      <br/><br/>
      <span style="float:left; font-size:25px">Boiling Point:</span>  <span style="float:right; font-size:25px"> {{this.boilingPoint}} </span>
<br/><br/>
      <span style="float:left; font-size:25px">Melting Point:</span>  <span style="float:right; font-size:25px"> {{this.meltingPoint}} </span>

   </el-card>
  
  <span slot="footer" class="dialog-footer">
    <el-button @click="dialogVisible = false">Cancel</el-button>
    <el-button type="primary" @click="dialogVisible = false">Confirm</el-button>
  </span>
</el-dialog>


</div>
</template>


<script>

// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {

  },
  data(){
      return {
        
          
          dialogVisible: false,
          image: '',
          title: '',
          electronicConfiguration: '',
          isotopes: '',
          boilingPoint: '',
          meltingPoint: '',
          discoveredBy: '',
          discovery: '',
          series: '',
          period:'',
          group:'',
          blocks: '',
          atomicMass: '',
          atomicNumber: '',
          symbol: '',  
          physicalState: '',

        //  metals
          isAlkali: false,
          isActinide: false,
          isLanthanide: false,
          isTransitionMetals: false,
          isTransitionMetalsEarth: false,
          isPostTransitionMetals: false,
        
        //  metalloids

          isMetalloids: false,

        //  non metals

          isNonMetals: false,
          isnobleGas: false,
          isReactiveNonMetals: false,
        
          // state

          isUnknown: false,
          isLiquid: false,
          isGas: false,
          isSolid: false
         

         
      }
  },
  methods: {

    handleClose(done){
      done()
    },

   toggle() {
  this.isNonMetals = this.isNonMetals ? false : true;
  this.isnobleGas = this.isnobleGas ? false : true
  this.isReactiveNonMetals = this.isReactiveNonMetals ? false : true
   },

  toggle2() {
  this.isMetals = this.isMetals ? false : true;
  this.isAlkali = this.isAlkali ? false : true
  this.isActinide = this.isActinide ? false : true
  this.isLanthanide = this.isLanthanide ? false : true
  this.isTransitionMetals = this.isTransitionMetals ? false : true
  this.isTransitionMetalsEarth = this.isTransitionMetalsEarth ? false : true
  this.isPostTransitionMetals = this.isPostTransitionMetals ? false : true
   }
   ,
    hydrogenVisible(){
    
     this.dialogVisible = true
     this.atomicNumber = '1'
     this.title = 'Hydrogen'
     this.image = 'https://media4.giphy.com/media/VbQk7UzSrryWjuF7Yb/giphy.gif'
     this.symbol = 'H'
     this.atomicMass = '1.0079'
     this.discoveredBy = 'Henry Cavendish'
     this.meltingPoint = '−259.16°C'
     this.boilingPoint = '−252.879°C'
     this.electronicConfiguration = '1s¹'
     this.physicalState = 'Gas'
     this.discovery = '1776'
     this.blocks = 'S Block'
     this.period = '1'
     this.group = '1'
     this.series = 'Reactive Non-Metals'
     this.isotopes = '3'
    },

    lithiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '3'
     this.title = 'Lithium'
     this.image = 'https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/b4bcc8ed-56dc-462d-b549-c56e5dc33c56/d1k88cs-b52c92d6-5a6a-456d-92ba-1ac707da8bf4.gif?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2I0YmNjOGVkLTU2ZGMtNDYyZC1iNTQ5LWM1NmU1ZGMzM2M1NlwvZDFrODhjcy1iNTJjOTJkNi01YTZhLTQ1NmQtOTJiYS0xYWM3MDdkYThiZjQuZ2lmIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.6rQhcnWCMMzKvgrdpYFg-aGo-HpKuYRmZ1niPkRpqW4'
     this.symbol = 'Li'
     this.atomicMass = '6.941'
     this.discoveredBy = 'Johann Artvedson'
     this.meltingPoint = '180.54 °C'
     this.boilingPoint = '1342 °C'
     this.electronicConfiguration = '[He] 2s¹'
     this.physicalState = 'Solid'
     this.discovery = '1817'
     this.blocks = 'S block'
     this.period = '2'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '2'
    },

     sodiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '11'
     this.title = 'Sodium'
     this.image = 'https://i.pinimg.com/originals/9f/28/84/9f2884774bb82f515e62fa7f1444669b.gif'
     this.symbol = 'Na'
     this.atomicMass = '22.9897'
     this.discoveredBy = 'Humphry Davy'
     this.meltingPoint = '97.79 °C'
     this.boilingPoint = '882.8 °C'
     this.electronicConfiguration = '[Ne] 3s¹'
     this.physicalState = 'Solid'
     this.discovery = '1807'
     this.blocks = 'S block'
     this.period = '3'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '13'
    },

    potassiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '19'
     this.title = 'Potassium'
     this.image = 'https://64.media.tumblr.com/345570fcfad7a7ef00660f4f5f14ad03/tumblr_pr4592JRbt1uag7foo1_400.gifv'
     this.symbol = 'K'
     this.atomicMass = '39.0983'
     this.discoveredBy = 'Humphry Davy'
     this.meltingPoint = '63.5 °C'
     this.boilingPoint = '758.8 °C'
     this.electronicConfiguration = '[Ar] 4s¹'
     this.physicalState = 'Solid'
     this.discovery = '1807'
     this.blocks = 'S block'
     this.period = '4'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '26'
    },


 rubidiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '37'
     this.title = 'Rubidium'
     this.image = 'https://thumbs.gfycat.com/BoringHarmfulAfricanmolesnake-max-1mb.gif'
     this.symbol = 'Rb'
     this.atomicMass = '85.4678'
     this.discoveredBy = 'Robert Bunsen and Gustav Kirchhoff'
     this.meltingPoint = '39 ºC'
     this.boilingPoint = '688 °C'
     this.electronicConfiguration = '[Kr] 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1861'
     this.blocks = 'S block'
     this.period = '5'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '32, 2 naturally occuring, 85Rb(72.2%) & 87Rb (27.8%)'
    },

    cesiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '37'
     this.title = 'Cesium'
     this.image = 'https://media3.giphy.com/media/KEGb7LBipW1pVcPt4v/200w.gif?cid=6c09b952w0kzjrywvqf5rdpo46kfycl4y2nmf1g1gchhx1tr&rid=200w.gif&ct=g'
     this.symbol = 'Cs'
     this.atomicMass = '132.90545'
     this.discoveredBy = 'Robert Wilhelm Bunsen and Gustav Robert Kirchhoff'
     this.meltingPoint = '28.44 °C'
     this.boilingPoint = '670.8 °C'
     this.electronicConfiguration = '[Xe] 6s¹'
     this.physicalState = 'Liquid'
     this.discovery = '1860'
     this.blocks = 'S block'
     this.period = '6'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '40'
    },

      franciumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '87'
     this.title = 'Francium'
     this.image = 'https://media2.giphy.com/media/l3ISoedvSdHw6lBi01/giphy.gif?cid=ecf05e47tz9jghg3oiw6opzzlehn6i7m11xgy1ay1llu6vex&rid=giphy.gif&ct=g'
     this.symbol = 'Fr'
     this.atomicMass = '223'
     this.discoveredBy = 'Marguerite Perey'
     this.meltingPoint = '27 °C'
     this.boilingPoint = '677°C '
     this.electronicConfiguration = '[Rn] 7s¹'
     this.physicalState = 'Solid'
     this.discovery = '1939'
     this.blocks = 'S block'
     this.period = '5'
     this.group = '1'
     this.series = 'Alkali Metals'
     this.isotopes = '34'
    },
  

   berylliumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '4'
     this.title = 'Beryllium'
     this.image = 'https://i.pinimg.com/originals/2e/75/5e/2e755eaff1fd09f1b102a0a44f6ddcbd.gif'
     this.symbol = 'Be'
     this.atomicMass = '9.0122'
     this.discoveredBy = 'Nicholas Louis Vauquelin'
     this.meltingPoint = '1,287 °C'
     this.boilingPoint = '2,469 °C'
     this.electronicConfiguration = '[He] 2s²'
     this.physicalState = 'Solid'
     this.discovery = '1797'
     this.blocks = 'S block'
     this.period = '2'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '1 stable'
    },

    magnesiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '12'
     this.title = 'Magnesium'
     this.image = 'https://media2.giphy.com/media/J3F4e60xtJBvUM0neh/giphy.gif?cid=ecf05e47bsetex2lxwps2e9ufsab6knifo7uhmeemhhrz36d&rid=giphy.gif&ct=g'
     this.symbol = 'Mg'
     this.atomicMass = '24.305'
     this.discoveredBy = 'Joseph Black'
     this.meltingPoint = '650 °C'
     this.boilingPoint = '1,091 °C'
     this.electronicConfiguration = '[Ne] 3s²'
     this.physicalState = 'Solid'
     this.discovery = '1755'
     this.blocks = 'S block'
     this.period = '3'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '3, 24Mg, 25Mg and 26Mg'
    },


calciumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '20'
     this.title = 'Calcium'
     this.image = 'https://periodictable.com/Samples/020.6/s7s.JPG'
     this.symbol = 'Ca'
     this.atomicMass = '40.078'
     this.discoveredBy = 'Sir Humphry Davy'
     this.meltingPoint = '842 °C'
     this.boilingPoint = '1,484 °C'
     this.electronicConfiguration = '[Ar]4s²'
     this.physicalState = 'Solid'
     this.discovery = '1808'
     this.blocks = 'S block'
     this.period = '5'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '6'
    },

strontiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '38'
     this.title = 'Strontium'
     this.image = 'https://media1.giphy.com/media/hX7PZDkJhmMahFaQhu/giphy.gif'
     this.symbol = 'Sr'
     this.atomicMass = '87.62'
     this.discoveredBy = 'Adair Crawford'
     this.meltingPoint = '777 °C'
     this.boilingPoint = '1382°C'
     this.electronicConfiguration = '[Kr] 5s²'
     this.physicalState = 'Solid'
     this.discovery = '1790'
     this.blocks = 'S block'
     this.period = '5'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '4 stable'
    },

// to be change
bariumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '56'
     this.title = 'Barium'
     this.image = 'https://periodictable.com/Samples/056.1/s9s.JPG'
     this.symbol = 'Ba'
     this.atomicMass = '137.327'
     this.discoveredBy = 'Humphry Davy'
     this.meltingPoint = '727 °C'
     this.boilingPoint = '1870  °C'
     this.electronicConfiguration = '[Xe] 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1808'
     this.blocks = 'S block'
     this.period = '6'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '7'
    },

    radiumVisible (){
     this.dialogVisible = true
     this.atomicNumber = '88'
     this.title = 'Radium'
     this.image = 'https://media0.giphy.com/media/humNLTdJt5Ha0e104L/200w.gif?cid=82a1493b0mhbdpllgzcqub565eh3h40gmzdrg36k6v8ti9jv&rid=200w.gif&ct=g'
     this.symbol = 'Ra'
     this.atomicMass = '85.4678'
     this.discoveredBy = 'Robert Bunsen and Gustav Kirchhoff'
     this.meltingPoint = '700  ºC'
     this.boilingPoint = '1737 °C'
     this.electronicConfiguration = '[Rn] 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1898'
     this.blocks = 'S block'
     this.period = '7'
     this.group = '2'
     this.series = 'Alkaline Earth Metals'
     this.isotopes = '1'
    },

 Scandium (){
     this.dialogVisible = true
     this.atomicNumber = '21'
     this.title = 'Scandium'
     this.image = 'https://periodictable.com/Samples/021.8/s9s.JPG'
     this.symbol = 'Sc'
     this.atomicMass = '44.9559'
     this.discoveredBy = 'Lars Frederik Nilson'
     this.meltingPoint = '1541  ºC'
     this.boilingPoint = '2830 °C'
     this.electronicConfiguration = '[Ar] 3d¹ 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1879'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '3'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },

    Yttrium (){
     this.dialogVisible = true
     this.atomicNumber = '39'
     this.title = 'Yttrium'
     this.image = 'https://periodictable.com/Samples/039.11/s9s.JPG'
     this.symbol = 'Y'
     this.atomicMass = '88.9059'
     this.discoveredBy = '[Kr] 4d¹ 5s²'
     this.meltingPoint = '1526  ºC'
     this.boilingPoint = '3345 °C'
     this.electronicConfiguration = '[Kr] 4d¹ 5s²'
     this.physicalState = 'Solid'
     this.discovery = '1794'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '3'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
    Titanium (){
     this.dialogVisible = true
     this.atomicNumber = '22'
     this.title = 'Titanium'
     this.image = 'https://media2.giphy.com/media/KN1yUueXTXzjylLi5r/giphy.gif'
     this.symbol = 'Ti'
     this.atomicMass = '47.867'
     this.discoveredBy = 'William Gregor'
     this.meltingPoint = '39 ºC'
     this.boilingPoint = '688 °C'
     this.electronicConfiguration = '[Ar] 3d² 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1791'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '4'
     this.series = 'Transition Metals'
     this.isotopes = '5'
    },
    Zirconium (){
     this.dialogVisible = true
     this.atomicNumber = '40'
     this.title = 'Zirconium'
     this.image = 'https://periodictable.com/Samples/040.17/s9s.JPG'
     this.symbol = 'Zr'
     this.atomicMass = '91.224'
     this.discoveredBy = 'Martin Klaproth'
     this.meltingPoint = '1855 ºC'
     this.boilingPoint = '4409 °C'
     this.electronicConfiguration = '[Kr] 4d² 5s²'
     this.physicalState = 'Solid'
     this.discovery = '1789'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '4'
     this.series = 'Transition  Metals'
     this.isotopes = '5'
    },
    
    Hafnium (){
     this.dialogVisible = true
     this.atomicNumber = '72'
     this.title = 'Hafnium'
     this.image = 'https://cdn.mos.cms.futurecdn.net/476mwLnFvNQhpUyNpNu2zn.jpg'
     this.symbol = 'Hf'
     this.atomicMass = '178.49'
     this.discoveredBy = 'George Charles de Hevesy and Dirk Coster'
     this.meltingPoint = '2233  ºC'
     this.boilingPoint = '4603  °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d² 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1923'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '4'
     this.series = 'Transition Metals'
     this.isotopes = '6'
    },

    Rutherfordium (){
     this.dialogVisible = true
     this.atomicNumber = '104'
     this.title = 'Rutherfordium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Rutherfordium-2.jpg'
     this.symbol = 'Rf'
     this.atomicMass = '261'
     this.discoveredBy = 'Georgy Flerov and colleague and independently by Albert Ghiorso and colleagues'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d² s²'
     this.physicalState = 'Unknown'
     this.discovery = '1964'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '4'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
    Lanthanum (){
     this.dialogVisible = true
     this.atomicNumber = '57'
     this.title = 'Lanthanum'
     this.image = 'https://theodoregray.com/periodictable/Samples/Jensan.Bastnasite/s11s.JPG'
     this.symbol = 'La'
     this.atomicMass = '138.9055'
     this.discoveredBy = 'Carl Gustav Mosander'
     this.meltingPoint = '920 ºC'
     this.boilingPoint = '3464  °C'
     this.electronicConfiguration = '[Xe] 5d¹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1839'
     this.blocks = 'F block'
     this.period = '5'
     this.group = 'Lanthanides'
     this.series = 'Lanthanides'
     this.isotopes = '2'
    },
    Actinium (){
     this.dialogVisible = true
     this.atomicNumber = '89'
     this.title = 'Actinium'
     this.image = 'https://periodictable.com/Samples/089.4/s9s.JPG'
     this.symbol = 'Ac'
     this.atomicMass = '227'
     this.discoveredBy = 'Andre Debierne'
     this.meltingPoint = '1050 ºC'
     this.boilingPoint = '3200 °C'
     this.electronicConfiguration = '[Rn] 6d¹ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1899'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },

    Vanadium (){
     this.dialogVisible = true
     this.atomicNumber = '23'
     this.title = 'Vanadium'
     this.image = 'https://media1.giphy.com/media/YQGc6X8pUi55X4ll7Y/giphy.gif'
     this.symbol = 'V'
     this.atomicMass = '50.9415'
     this.discoveredBy = 'Nils Sefstrom'
     this.meltingPoint = '1910  ºC'
     this.boilingPoint = '3407 °C'
     this.electronicConfiguration = '[Ar] 3d³ 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1830'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '4'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },
    Niobium (){
     this.dialogVisible = true
     this.atomicNumber = '41'
     this.title = 'Niobium'
     this.image = 'https://periodictable.com/Samples/041.13/s9s.JPG'
     this.symbol = 'Nb'
     this.atomicMass = '92.9064'
     this.discoveredBy = 'Charles Hatchett'
     this.meltingPoint = '2477 ºC'
     this.boilingPoint = '4744 °C'
     this.electronicConfiguration = '[Kr] 4d⁴ 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1801'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '5'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
    Tantalum (){
     this.dialogVisible = true
     this.atomicNumber = '73'
     this.title = 'Tantalum'
     this.image = 'https://periodictable.com/Samples/073.8/s9s.JPG'
     this.symbol = 'Ta'
     this.atomicMass = '180.9479'
     this.discoveredBy = '5458'
     this.meltingPoint = '3017 ºC'
     this.boilingPoint = '5458 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d³ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1802'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '5'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },


    Dubnium (){
     this.dialogVisible = true
     this.atomicNumber = '105'
     this.title = 'Dubnium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Dubnium-2.jpg'
     this.symbol = 'Db'
     this.atomicMass = '85.4678'
     this.discoveredBy = 'Scientists at both Berkeley, California, USA, and Dubna, near Moscow, Russia'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d³ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1967'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '5'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },

    Cerium (){
     this.dialogVisible = true
     this.atomicNumber = '58'
     this.title = 'Cerium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/0/0d/Cerium2.jpg'
     this.symbol = 'Ce'
     this.atomicMass = '140.116'
     this.discoveredBy = 'Jöns Jacob Berzelius and Wilhelm Hisinger'
     this.meltingPoint = '798 ºC'
     this.boilingPoint = '3360 °C'
     this.electronicConfiguration = '[Xe] 4f¹ 5d¹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1803'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '4'
    },
    Thorium (){
     this.dialogVisible = true
     this.atomicNumber = '90'
     this.title = 'Thorium'
     this.image = 'https://media0.giphy.com/media/JRg8ZQF2aBmfoc8NxG/200w.gif?cid=82a1493b3ov53htx5mhee0peyfqx5ja43rjct0z4fqcsdon8&rid=200w.gif&ct=g'
     this.symbol = 'Th'
     this.atomicMass = '232.0381'
     this.discoveredBy = 'Jöns Jacob Berzelius'
     this.meltingPoint = '1750 ºC'
     this.boilingPoint = '4820 °C'
     this.electronicConfiguration = '[Rn] 6d² 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1829'
     this.blocks = 'F block'
     this.period = '5'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
    Chromium (){
     this.dialogVisible = true
     this.atomicNumber = '24'
     this.title = 'Chromium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/a/a1/Chromium.jpg'
     this.symbol = 'Cr'
     this.atomicMass = '85.4678'
     this.discoveredBy = 'Vaughlin'
     this.meltingPoint = '1907 ºC'
     this.boilingPoint = '2671 °C'
     this.electronicConfiguration = '[Ar] 3d⁵ 4s¹'
     this.physicalState = 'Solid'
     this.discovery = '1797'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '6'
     this.series = 'Transition Metals'
     this.isotopes = '4'
    },
    Molybdenum (){
     this.dialogVisible = true
     this.atomicNumber = '42'
     this.title = 'Molybdenum'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/3/32/Molybdenum_crystaline_fragment_and_1cm3_cube.jpg'
     this.symbol = 'Mo'
     this.atomicMass = '95.94'
     this.discoveredBy = 'Peter Jacob Hjelm'
     this.meltingPoint = '2623 ºC'
     this.boilingPoint = '4639 °C'
     this.electronicConfiguration = '[Kr] 4d⁵ 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1781'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '6'
     this.series = 'Transition Metals'
     this.isotopes = '7'
    },
    Tungsten (){
     this.dialogVisible = true
     this.atomicNumber = '74'
     this.title = 'Tungsten'
     this.image = 'https://media4.giphy.com/media/YnNf0IZRXO7eEi2pZG/giphy.gif?cid=ecf05e47pp8mbils73em0el53uoh8x5057u3jcjc082625og&rid=giphy.gif&ct=g'
     this.symbol = 'W'
     this.atomicMass = '183.84'
     this.discoveredBy = 'Fausto and Juan Jose de Elhuyar'
     this.meltingPoint = '3422 ºC'
     this.boilingPoint = '5555 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d⁴ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1783'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '6'
     this.series = 'Transition Metals'
     this.isotopes = '5'
    },
    Seaborgium (){
     this.dialogVisible = true
     this.atomicNumber = '106'
     this.title = 'Seaborgium'
     this.image = 'https://www.chemistrylearner.com/wp-content/uploads/2018/01/Seaborgium.jpg'
     this.symbol = 'Sg'
     this.atomicMass = '266'
     this.discoveredBy = 'Albert Ghiorso and named it after the Nuclear chemist Glenn T. Seaborg'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d⁴ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1974'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '6'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },

    Praseodymium (){
     this.dialogVisible = true
     this.atomicNumber = '59'
     this.title = 'Praseodymium'
     this.image = 'https://media0.giphy.com/media/f7esW3jp8afC5thJqE/giphy.gif?cid=ecf05e47pfwqm5mfj7bs2d2kkv6osiouk7ognr4bp56z3nae&rid=giphy.gif&ct=g'
     this.symbol = 'Pr'
     this.atomicMass = '140.9077'
     this.discoveredBy = 'Carl Auer von Welsbach'
     this.meltingPoint = '931 ºC'
     this.boilingPoint = '3290 °C'
     this.electronicConfiguration = '[Xe] 4f³ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1885'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '1'
    },
    Protactinium (){
     this.dialogVisible = true
     this.atomicNumber = '91'
     this.title = 'Protactinium'
     this.image = 'https://media3.giphy.com/media/St9xgX9pLcGyI6z0Wv/giphy.gif?cid=ecf05e47rrgykbg2oke7tl4rjfxaf5c3a7134jzybov13coe&rid=giphy.gif&ct=g'
     this.symbol = 'Pa'
     this.atomicMass = '231.0359'
     this.discoveredBy = 'K. Kajans and O.H. Gohring'
     this.meltingPoint = '1572 ºC'
     this.boilingPoint = '4000 °C'
     this.electronicConfiguration = '[Rn] 5f² 6d¹ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1913'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
    Manganese (){
     this.dialogVisible = true
     this.atomicNumber = '25'
     this.title = 'Manganese'
     this.image = 'https://media0.giphy.com/media/gJu1FqzdVDHUFzIIx3/giphy.gif?cid=ecf05e47ueya000kieskfdubqvldi0e8sb71rhx2koirvees&rid=giphy.gif&ct=g'
     this.symbol = 'Mn'
     this.atomicMass = '54.938'
     this.discoveredBy = 'Johan Gottlieb Gahn'
     this.meltingPoint = '1246 ºC'
     this.boilingPoint = '2061 °C'
     this.electronicConfiguration = '[Ar] 3d⁵ 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1774'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '7'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
    Technetium (){
     this.dialogVisible = true
     this.atomicNumber = '43'
     this.title = 'Technetium'
     this.image = 'https://www.daviddarling.info/images3/technetium.jpg'
     this.symbol = 'Tc'
     this.atomicMass = '98'
     this.discoveredBy = 'Carlo Perrier and Emilio Segre'
     this.meltingPoint = '2157 ºC'
     this.boilingPoint = '4265 °C'
     this.electronicConfiguration = '[Kr] 4d⁵ 5s²'
     this.physicalState = 'Solid'
     this.discovery = '1937'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '7'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
     Rhenium (){
     this.dialogVisible = true
     this.atomicNumber = '75'
     this.title = 'Rhenium'
     this.image = 'https://www.chemicool.com/elements/images/300-columbite.jpg'
     this.symbol = 'Re'
     this.atomicMass = '186.207'
     this.discoveredBy = 'Walter Noddack, Ida Tacke and Otto Berg'
     this.meltingPoint = '3186 ºC'
     this.boilingPoint = '5596 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d⁵ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1925'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '7'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },
     Bohrium (){
     this.dialogVisible = true
     this.atomicNumber = '107'
     this.title = 'Bohrium'
     this.image = 'https://images.allthescience.org/slideshow-mobile-small/close-view-of-bismuth.jpg'
     this.symbol = 'Bh'
     this.atomicMass = '264'
     this.discoveredBy = 'Peter Armbruster, Gottfried Münzenberg, and colleagues'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d⁵ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1981'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '7'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
     Neodymium (){
     this.dialogVisible = true
     this.atomicNumber = '60'
     this.title = 'Neodymium'
     this.image = 'https://media2.giphy.com/media/Jmh4MQB5dieTXrGYDO/giphy.gif?cid=ecf05e4724qu09zbvwtx5vwrwzp6937wnklwuf15wyd6ilff&rid=giphy.gif&ct=g'
     this.symbol = 'Nd'
     this.atomicMass = '144.24'
     this.discoveredBy = 'Robert Bunsen and Gustav Kirchhoff'
     this.meltingPoint = '1021 ºC'
     this.boilingPoint = '3.1×103 °C'
     this.electronicConfiguration = '[Xe] 4f⁴ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1885'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '7'
    },
     Uranium (){
     this.dialogVisible = true
     this.atomicNumber = '92'
     this.title = 'Uranium'
     this.image = 'https://media3.giphy.com/media/J3y2WnZau1hfH3xyeV/giphy.gif?cid=ecf05e47j3n7voxrimfzlkhrlhklzyk2210ilvzhpv6woyo2&rid=giphy.gif&ct=g'
     this.symbol = 'U'
     this.atomicMass = '238.0289'
     this.discoveredBy = 'Martin Heinrich Klaproth'
     this.meltingPoint = '1135 ºC'
     this.boilingPoint = '3927 °C'
     this.electronicConfiguration = '[Rn] 5f³ 6d¹ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1789'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '3'
    },

     Iron (){
     this.dialogVisible = true
     this.atomicNumber = '26'
     this.title = 'Iron'
     this.image = 'https://periodictable.com/Samples/026.32/s9s.JPG'
     this.symbol = 'Fe'
     this.atomicMass = '55.845'
     this.discoveredBy = 'The Ancient'
     this.meltingPoint = '1538 ºC'
     this.boilingPoint = '2861 °C'
     this.electronicConfiguration = '[Ar] 3d⁶ 4s²'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '8'
     this.series = 'Transition Metals'
     this.isotopes = '4'
    }, 
    
    Ruthenium (){
     this.dialogVisible = true
     this.atomicNumber = '44'
     this.title = 'Ruthenium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/2/2c/Ruthenium_a_half_bar.jpg'
     this.symbol = 'Ru'
     this.atomicMass = '101.07'
     this.discoveredBy = 'Karl Klaus'
     this.meltingPoint = '2334 ºC'
     this.boilingPoint = '4150 °C'
     this.electronicConfiguration = '[Kr] 4d⁷ 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1844'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '8'
     this.series = 'Transition Metals'
     this.isotopes = '7'
    },
     Osmium (){
     this.dialogVisible = true
     this.atomicNumber = '76'
     this.title = 'Osmium'
     this.image = 'https://periodictable.com/Samples/076.8/s9s.JPG'
     this.symbol = 'Os'
     this.atomicMass = '190.23'
     this.discoveredBy = 'Smithson Tennant'
     this.meltingPoint = '3033 ºC'
     this.boilingPoint = '5012 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d⁶ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1803'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '8'
     this.series = 'Transition Metals'
     this.isotopes = '7'
    },
     Hassium (){
     this.dialogVisible = true
     this.atomicNumber = '108'
     this.title = 'Hassium'
     this.image = 'https://www.chemistrylearner.com/wp-content/uploads/2018/03/Hassium.jpg'
     this.symbol = 'Hs'
     this.atomicMass = '277'
     this.discoveredBy = 'Peter Armbruster and Gottfried Muizenberg'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d⁶ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1984'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '8'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
     Promethium (){
     this.dialogVisible = true
     this.atomicNumber = '61'
     this.title = 'Promethium'
     this.image = 'https://media0.giphy.com/media/duQKVmRxTDV0V4RZWe/giphy.gif?cid=ecf05e47bdhru9k3f7407xvd3hghlrxgzcrit1zw2frvwg2c&rid=giphy.gif&ct=g'
     this.symbol = 'Pm'
     this.atomicMass = '145'
     this.discoveredBy = 'Mariinsky'
     this.meltingPoint = '1.1×103 ºC'
     this.boilingPoint = '3×103 °C'
     this.electronicConfiguration = '[Xe] 4f⁵ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1945'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '1'
    },
     Neptunium (){
     this.dialogVisible = true
     this.atomicNumber = '93'
     this.title = 'Neptunium'
     this.image = 'https://media4.giphy.com/media/hqZxCqLQpqgsHEgQWA/giphy.gif?cid=ecf05e47na4rhkn503sb0cfwx67ljjqs3tn09m71ysyrk9n6&rid=giphy.gif&ct=g'
     this.symbol = 'Np'
     this.atomicMass = '237'
     this.discoveredBy = 'Edwin McMillan and Philip Abelson'
     this.meltingPoint = '644 ºC'
     this.boilingPoint = '4×103 °C'
     this.electronicConfiguration = '[Rn] 5f⁴ 6d¹ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1940'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
     Cobalt (){
     this.dialogVisible = true
     this.atomicNumber = '27'
     this.title = 'Cobalt'
     this.image = 'https://media3.giphy.com/media/KZYUwFy1Oay5IxBC8a/giphy.gif?cid=ecf05e47lwtsgwhb1evzo8vuos3glg7ce2udwxq7a74m6dig&rid=giphy.gif&ct=g'
     this.symbol = 'Co'
     this.atomicMass = '58.9332'
     this.discoveredBy = 'Georg Brandt'
     this.meltingPoint = '1495 ºC'
     this.boilingPoint = '2927 °C'
     this.electronicConfiguration = '[Ar] 3d⁷ 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1735'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '9'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    }, 
    
    Rhodium (){
     this.dialogVisible = true
     this.atomicNumber = '45'
     this.title = 'Rhodium'
     this.image = 'https://cdn.mos.cms.futurecdn.net/9fQnwuCCKJDLQDxJMkZEYG.jpg'
     this.symbol = 'Rh'
     this.atomicMass = '102.9055'
     this.discoveredBy = 'William Wollaston'
     this.meltingPoint = '1964 ºC'
     this.boilingPoint = '3695 °C'
     this.electronicConfiguration = '[Kr] 4d⁸ 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1803'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '9'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
     Iridium (){
     this.dialogVisible = true
     this.atomicNumber = '77'
     this.title = 'Iridium'
     this.image = 'https://media1.giphy.com/media/Wtb8sAmL4Vi22nTwTF/giphy.gif?cid=ecf05e470hc9xmelsnmdvkm5zqfkdj57wz8pelx20l1cqt5t&rid=giphy.gif&ct=g'
     this.symbol = 'Ir'
     this.atomicMass = '196.9665'
     this.discoveredBy = 'Ghiorso'
     this.meltingPoint = '2466 ºC'
     this.boilingPoint = '4428 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d⁷ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1952'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '9'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },

     Meitnerium (){
     this.dialogVisible = true
     this.atomicNumber = '109'
     this.title = 'Meitnerium'
     this.image = 'https://4.bp.blogspot.com/-A50yMId9oDA/VhNCtU6sNhI/AAAAAAAAamA/rH9Aos9NCZw/s1600/not%2BMeitnerium.jpg'
     this.symbol = 'Mt'
     this.atomicMass = '268'
     this.discoveredBy = 'Gesellschaft fur Schwerionenforschung'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d⁷ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1982'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '9'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Samarium (){
     this.dialogVisible = true
     this.atomicNumber = '62'
     this.title = 'Samarium'
     this.image = 'https://media4.giphy.com/media/ighOG4POrV89X7JvyB/giphy.gif?cid=ecf05e4737jy7isfxpro3nj318q7loo3nsi8vnh4lcv3hkp6&rid=giphy.gif&ct=g'
     this.symbol = 'Sm'
     this.atomicMass = '150.36'
     this.discoveredBy = 'Paul-Émile Lecoq de Boisbaudran'
     this.meltingPoint = '1072 ºC'
     this.boilingPoint = '1803 °C'
     this.electronicConfiguration = '[Xe] 4f⁶ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1879'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '7'
    },
     Plutonium (){
     this.dialogVisible = true
     this.atomicNumber = '94'
     this.title = 'Plutonium'
     this.image = 'https://media3.giphy.com/media/hpG4gBUbCk5r058aKb/giphy.gif?cid=ecf05e47mwzt5vxyegn83y1h48j0v75ss8rqj0cwdihlhcl2&rid=giphy.gif&ct=g'
     this.symbol = 'Pu'
     this.atomicMass = '244'
     this.discoveredBy = 'G.T. Seaborg'
     this.meltingPoint = '640 ºC'
     this.boilingPoint = '3230 °C'
     this.electronicConfiguration = '[Rn] 5f⁶ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1940'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
     Nickel (){
     this.dialogVisible = true
     this.atomicNumber = '28'
     this.title = 'Nickel'
     this.image = 'https://media3.giphy.com/media/eNYe5fkB63We8jRhvP/giphy.gif?cid=ecf05e47e2mztcf187036kkir42t04tz55tr97z3p2m8d7d8&rid=giphy.gif&ct=g'
     this.symbol = 'Ni'
     this.atomicMass = '58.6934'
     this.discoveredBy = 'Axel Fredrik Cronstedt'
     this.meltingPoint = '1455 ºC'
     this.boilingPoint = '2913 °C'
     this.electronicConfiguration = '[Ar] 3d⁸ 4s²'
     this.physicalState = 'Solid'
     this.discovery = '1751'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '10'
     this.series = 'Transition Metals'
     this.isotopes = '5'
    },
     Palladium (){
     this.dialogVisible = true
     this.atomicNumber = '46'
     this.title = 'Palladium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/d/d7/Palladium_%2846_Pd%29.jpg'
     this.symbol = 'Pd'
     this.atomicMass = '106.42'
     this.discoveredBy = 'William Hyde Wollaston'
     this.meltingPoint = '1554.9 ºC'
     this.boilingPoint = '2963 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰'
     this.physicalState = 'Solid'
     this.discovery = '1803'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '10'
     this.series = 'Transition Metals'
     this.isotopes = '6'
    },
     Platinum (){
     this.dialogVisible = true
     this.atomicNumber = '78'
     this.title = 'Platinum'
     this.image = 'https://media0.giphy.com/media/SVO4P6rsf88QACW86o/giphy-downsized-large.gif?cid=6c09b952054647a58c0fccc0da822ef70b5f4aa1378bb4f1&rid=giphy-downsized-large.gif&ct=g'
     this.symbol = 'Pt'
     this.atomicMass = '192.217'
     this.discoveredBy = 'Julius Scaliger'
     this.meltingPoint = '1768.3 ºC'
     this.boilingPoint = '3825 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d⁹ 6s¹'
     this.physicalState = 'Solid'
     this.discovery = '1803'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '10'
     this.series = 'Transition Metals'
     this.isotopes = '6'
    },
     Darmstadtium (){
     this.dialogVisible = true
     this.atomicNumber = '110'
     this.title = 'Darmstadtium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Darmstadtium-2.jpg'
     this.symbol = 'Ds'
     this.atomicMass = '261.9'
     this.discoveredBy = 'Gesellschaft für Schwerionenforschung'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d⁹ 7s¹'
     this.physicalState = 'Unknown'
     this.discovery = '1994'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '10'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Europium (){
     this.dialogVisible = true
     this.atomicNumber = '63'
     this.title = 'Europium'
     this.image = 'https://media4.giphy.com/media/TJsGKAnVPuo8vT54cu/giphy.gif?cid=ecf05e477vpgx4pqnnmhv77vas91c9m2lzhmt50nn0pjrbwt&rid=giphy.gif&ct=g'
     this.symbol = 'Eu'
     this.atomicMass = '151.964'
     this.discoveredBy = 'Eugène-Anatole Demarçay'
     this.meltingPoint = '822 ºC'
     this.boilingPoint = '1527 °C'
     this.electronicConfiguration = '[Xe] 4f⁷ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1901'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '2'
    },

     Americium (){
     this.dialogVisible = true
     this.atomicNumber = '95'
     this.title = 'Americium'
     this.image = 'https://media4.giphy.com/media/rud8KkvmY7fMQGgQxN/giphy.gif?cid=ecf05e47vazmle4rxatp12isr1azcvj6ytrk1tjuxtbf8dxs&rid=giphy.gif&ct=g'
     this.symbol = 'Am'
     this.atomicMass = '243'
     this.discoveredBy = 'Glenn Seaborg and colleagues.'
     this.meltingPoint = '1176 ºC'
     this.boilingPoint = '2011 °C'
     this.electronicConfiguration = '[Rn] 5f⁷ 7s²'
     this.physicalState = 'Solid'
     this.discovery = '1944'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
     Copper (){
     this.dialogVisible = true
     this.atomicNumber = '29'
     this.title = 'Copper'
     this.image = 'https://media3.giphy.com/media/iILbRWewmvIv2kVGMe/giphy.gif?cid=ecf05e47iecxfhzm7f6ebsn6z8aqeodslfaopgtpi1domdsf&rid=giphy.gif&ct=g'
     this.symbol = 'Cu'
     this.atomicMass = '63.546'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '1084.62 ºC'
     this.boilingPoint = '2927 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s¹'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '11'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },
     Silver (){
     this.dialogVisible = true
     this.atomicNumber = '47'
     this.title = 'Silver'
     this.image = 'https://media3.giphy.com/media/eP9ROpNQDdThOnOe9p/giphy.gif?cid=ecf05e4708pcor7skjnsgyxzhf97sn763sufu0jpegqyrlig&rid=giphy.gif&ct=g'
     this.symbol = 'Ag'
     this.atomicMass = '107.8682'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '961.78 ºC'
     this.boilingPoint = '2162 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s¹'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '11'
     this.series = 'Transition Metals'
     this.isotopes = '2'
    },
     Gold (){
     this.dialogVisible = true
     this.atomicNumber = '79'
     this.title = 'Gold'
     this.image = 'https://media1.giphy.com/media/VEzBh8xUleVRjYMZhR/giphy.gif?cid=ecf05e47mta2fhgn5vfcuguz8tb2ueeq4f59xh2e0o53gqx9&rid=giphy.gif&ct=g'
     this.symbol = 'Au'
     this.atomicMass = '195.078'
     this.discoveredBy = 'James W. Marshall'
     this.meltingPoint = '1064.18 ºC'
     this.boilingPoint = '2856 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s¹'
     this.physicalState = 'Solid'
     this.discovery = '1735'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '11'
     this.series = 'Transition Metals'
     this.isotopes = '1'
    },
     Roentgenium (){
     this.dialogVisible = true
     this.atomicNumber = '111'
     this.title = 'Roentgenium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Roentgenium-2.jpg'
     this.symbol = 'Rg'
     this.atomicMass = '271.8'
     this.discoveredBy = 'Peter Armbruster and Gottfried Münzenberg'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹⁰ 7s¹'
     this.physicalState = 'Unknown'
     this.discovery = '1994'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '11'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Gadolinium (){
     this.dialogVisible = true
     this.atomicNumber = '64'
     this.title = 'Gadolinium'
     this.image = 'https://media3.giphy.com/media/h7jTSG03ijLT2NSBkT/giphy.gif?cid=ecf05e47x3fghkmtjqxof92239s5xgchy7bqb0a3j9rvqu7p&rid=giphy.gif&ct=g'
     this.symbol = 'Gd'
     this.atomicMass = '157.25'
     this.discoveredBy = 'Jean Charles Galissard de Marignac'
     this.meltingPoint = '1313 ºC'
     this.boilingPoint = '3250 °C'
     this.electronicConfiguration = '[Xe] 4f⁷ 5d¹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1880'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '7'
    },
     Curium (){
     this.dialogVisible = true
     this.atomicNumber = '96'
     this.title = 'Curium'
     this.image = 'https://media0.giphy.com/media/kDC2trsnt9ubDUm0xo/giphy.gif?cid=ecf05e47wp2x19qsurt9cm7pbwwj1nwvst0tu21xc2sxaun0&rid=giphy.gif&ct=g'
     this.symbol = 'Cm'
     this.atomicMass = '247'
     this.discoveredBy = 'G.T. Seaborg'
     this.meltingPoint = '1345 ºC'
     this.boilingPoint = '3110 °C'
     this.electronicConfiguration = '[Rn] 5f⁷ 6d¹ s²'
     this.physicalState = 'Solid'
     this.discovery = '1944'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    }, 
    
    Zinc (){
     this.dialogVisible = true
     this.atomicNumber = '30'
     this.title = 'Zinc'
     this.image = 'https://media3.giphy.com/media/gLQslDCTCupVZa6apV/giphy.gif?cid=ecf05e47a9z6k8qxfuoqak8gh7n6am84uauq992uruvaj4mv&rid=giphy.gif&ct=g'
     this.symbol = 'Zn'
     this.atomicMass = '65.39'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '419.53 ºC'
     this.boilingPoint = '907 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s²'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'D block'
     this.period = '4'
     this.group = '12'
     this.series = 'Transition Metals'
     this.isotopes = '5'
    },

     Cadmium (){
     this.dialogVisible = true
     this.atomicNumber = '48'
     this.title = 'Cadmium'
     this.image = 'https://media4.giphy.com/media/cKJblApSczRONTOZdP/giphy.gif?cid=ecf05e47mpcbs1mcbzgyo5eqqzes2fdoalllxbyd383z2hso&rid=giphy.gif&ct=g'
     this.symbol = 'Cd'
     this.atomicMass = '112.411'
     this.discoveredBy = 'Friedrich Stromeyer'
     this.meltingPoint = '321.07 ºC'
     this.boilingPoint = '767 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s²'
     this.physicalState = 'Solid'
     this.discovery = '1817'
     this.blocks = 'D block'
     this.period = '5'
     this.group = '12'
     this.series = 'Transition Metals'
     this.isotopes = '8'
    },
     Mercury (){
     this.dialogVisible = true
     this.atomicNumber = '80'
     this.title = 'Mercury'
     this.image = 'https://static.sciencelearn.org.nz/images/images/000/003/377/original/CER_ITV_TEMP_BoilingMercuryThermometer.jpg?1674170672'
     this.symbol = 'Hg'
     this.atomicMass = '200.59'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '-38.83 ºC'
     this.boilingPoint = '356.73 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s²'
     this.physicalState = 'Liquid'
     this.discovery = 'Ancient'
     this.blocks = 'D block'
     this.period = '6'
     this.group = '12'
     this.series = 'Transition Metals'
     this.isotopes = '7'
    },

    Copernicium (){
     this.dialogVisible = true
     this.atomicNumber = '112'
     this.title = 'Copernicium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Copernicium-2.jpg'
     this.symbol = 'Cn'
     this.atomicMass = '285'
     this.discoveredBy = 'Gesellschaft fur Schwerionenforschung'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹⁰ 7s²'
     this.physicalState = 'Unknown'
     this.discovery = '1996'
     this.blocks = 'D block'
     this.period = '7'
     this.group = '12'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
    Terbium (){
     this.dialogVisible = true
     this.atomicNumber = '65'
     this.title = 'Terbium'
     this.image = 'https://media3.giphy.com/media/WQHYy2Xr4UIeREN3sS/giphy.gif?cid=ecf05e47ujxmi4ailge5tyl9jlo8alt71npjhvw8f30sm81v&rid=giphy.gif&ct=g'
     this.symbol = 'Terbium'
     this.atomicMass = '158.9253'
     this.discoveredBy = 'Carl Gustav Mosander'
     this.meltingPoint = '1356 ºC'
     this.boilingPoint = '3230 °C'
     this.electronicConfiguration = '[Xe] 4f⁹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1861'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '1'
    },
    Berkelium (){
     this.dialogVisible = true
     this.atomicNumber = '97'
     this.title = 'Berkelium'
     this.image = 'https://media0.giphy.com/media/hSXBfOQYT5ukk8FUgO/giphy.gif?cid=ecf05e473ygrxishxys9v322gtno1grqggvptu8jmnu0mgul&rid=giphy.gif&ct=g'
     this.symbol = '247'
     this.atomicMass = '85.4678'
     this.discoveredBy = 'Stanley Thompson, Albert Ghiorso, and Glenn Seaborg'
     this.meltingPoint = '1050 ºC'
     this.boilingPoint = 'N/A °C'
     this.electronicConfiguration = '[Rn] 5f⁹ s²'
     this.physicalState = 'Solid'
     this.discovery = '1949'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
    Boron (){
     this.dialogVisible = true
     this.atomicNumber = '5'
     this.title = 'Boron'
     this.image = 'https://media3.giphy.com/media/Kg1ttGFEuMc9QvuYVa/giphy.gif?cid=ecf05e47qgg7afa08k0v281wvo91djlwieiu980q2v0ctvew&rid=giphy.gif&ct=g'
     this.symbol = 'B'
     this.atomicMass = '10.811'
     this.discoveredBy = 'Joseph Louis Gay-Lussac'
     this.meltingPoint = '2075 ºC'
     this.boilingPoint = '4000 °C'
     this.electronicConfiguration = '[He] 2s² 2p¹'
     this.physicalState = 'Solid'
     this.discovery = '1861'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '18'
     this.series = 'Metalloid'
     this.isotopes = '2'
    },
    Aluminium (){
     this.dialogVisible = true
     this.atomicNumber = '13'
     this.title = 'Aluminium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/5/5d/Aluminium-4.jpg'
     this.symbol = 'Al'
     this.atomicMass = '13'
     this.discoveredBy = 'Hans Christian Oersted'
     this.meltingPoint = '660.32 ºC'
     this.boilingPoint = '2519 °C'
     this.electronicConfiguration = '[Ne] 3s² 3p¹'
     this.physicalState = 'Solid'
     this.discovery = '1825'
     this.blocks = 'P block'
     this.period = '33'
     this.group = '1'
     this.series = 'Post Transition Metals'
     this.isotopes = '1'
    },
    Gallium (){
     this.dialogVisible = true
     this.atomicNumber = '31'
     this.title = 'Gallium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/9/92/Gallium_crystals.jpg'
     this.symbol = 'Ga'
     this.atomicMass = '69.723'
     this.discoveredBy = 'Robert Bunsen and Gustav Kirchhoff'
     this.meltingPoint = '39 ºC'
     this.boilingPoint = '688 °C'
     this.electronicConfiguration = '[Kr] 5s¹'
     this.physicalState = 'Solid'
     this.discovery = '1861'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '13'
     this.series = 'Post Transition Metals'
     this.isotopes = '2'
    },
    Indium (){
     this.dialogVisible = true
     this.atomicNumber = '49'
     this.title = 'Indium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/b/b8/Indium.jpg'
     this.symbol = 'In'
     this.atomicMass = '114.818'
     this.discoveredBy = 'Ferdinand Reich'
     this.meltingPoint = '156.6 ºC'
     this.boilingPoint = '2072 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p¹'
     this.physicalState = 'Solid'
     this.discovery = '1863'
     this.blocks = 'P block'
     this.period = '5'
     this.group = '13'
     this.series = 'Post Transition Metals'
     this.isotopes = '2'
    },
    Thallium (){
     this.dialogVisible = true
     this.atomicNumber = '81'
     this.title = 'Thallium'
     this.image = 'https://chemicool.com/elements/images/300-thallium.jpg'
     this.symbol = 'Tl'
     this.atomicMass = '204.3833'
     this.discoveredBy = 'Sir William Crookes'
     this.meltingPoint = '304 ºC'
     this.boilingPoint = '1473 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p¹'
     this.physicalState = 'Solid'
     this.discovery = '1861'
     this.blocks = 'P block'
     this.period = '6'
     this.group = '13'
     this.series = 'Post Transition Metals'
     this.isotopes = '2'
    },
    Nihonium (){
     this.dialogVisible = true
     this.atomicNumber = '113'
     this.title = 'Nihonium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Nihonium-2.jpg'
     this.symbol = 'Nh'
     this.atomicMass = '286'
     this.discoveredBy = 'Scientists from the Joint Institute for Nuclear Research in Dubna, Russia, and Lawrence Livermore National Laboratory in California'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹⁰ 7s² 7p¹'
     this.physicalState = 'Unknown'
     this.discovery = '2003'
     this.blocks = 'P block'
     this.period = '7'
     this.group = '13'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
    Dysprosium (){
     this.dialogVisible = true
     this.atomicNumber = '66'
     this.title = 'Dysprosium'
     this.image = 'https://timebusinessnews.com/wp-content/uploads/Dysprosium.jpg'
     this.symbol = 'Dy'
     this.atomicMass = '162.5'
     this.discoveredBy = 'Dysprosium was discovered by Paul-Émile Lecoq de Boisbaudran'
     this.meltingPoint = '1412 C'
     this.boilingPoint = '2567 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁰ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1886'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '7'
    },
    Californium (){
     this.dialogVisible = true
     this.atomicNumber = '98'
     this.title = 'Californium'
     this.image = 'https://www.ccdc.cam.ac.uk/media/elements/Californium.jpg'
     this.symbol = 'Cf'
     this.atomicMass = '251'
     this.discoveredBy = 'Stanley Thompson, Kenneth Street, Jr., Albert Ghiorso, and Glenn Seaborg'
     this.meltingPoint = '900 ºC'
     this.boilingPoint = 'N/A'
     this.electronicConfiguration = '[Rn] 5f¹⁰ s²'
     this.physicalState = 'Solid'
     this.discovery = '1950'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
    Carbon (){
     this.dialogVisible = true
     this.atomicNumber = '6'
     this.title = 'Carbon'
     this.image = 'https://media3.giphy.com/media/Z8k6qo0AVIsPdROQNd/giphy.gif?cid=ecf05e47vj1rw4wc1w8rjr5xft7da73xx0q7kwu062s4cocm&rid=giphy.gif&ct=g'
     this.symbol = 'C'
     this.atomicMass = '12.0107'
     this.discoveredBy = ' Lavoisier proposed carbon'
     this.meltingPoint = '3550 ºC'
     this.boilingPoint = '4027 °C'
     this.electronicConfiguration = '[He] 2s² 2p²'
     this.physicalState = 'Solid'
     this.discovery = '1789'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '14'
     this.series = 'Reactive nonmetals'
     this.isotopes = '3'
    },
    Silicon (){
     this.dialogVisible = true
     this.atomicNumber = '14'
     this.title = 'Silicon'
     this.image = 'https://media2.giphy.com/media/WTXIBTyOtiXUquSt1u/giphy.gif?cid=ecf05e47f1qsd7psz1hg4w4raha8tvek4gcaod5hmr7ovhdp&rid=giphy.gif&ct=g'
     this.symbol = 'Si'
     this.atomicMass = '28.0855'
     this.discoveredBy = 'Jöns Jacob Berzelius'
     this.meltingPoint = '1414 ºC'
     this.boilingPoint = '2.9×103 °C'
     this.electronicConfiguration = '[Ne]3s² 3p²'
     this.physicalState = 'Solid'
     this.discovery = '1824'
     this.blocks = 'P block'
     this.period = '3'
     this.group = '14'
     this.series = 'Metalloid'
     this.isotopes = '3'
    },
    Germanium (){
     this.dialogVisible = true
     this.atomicNumber = '32'
     this.title = 'Germanium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Polycrystalline-germanium.jpg/220px-Polycrystalline-germanium.jpg'
     this.symbol = 'Ge'
     this.atomicMass = '72.64'
     this.discoveredBy = 'Clemens Winkler'
     this.meltingPoint = '938.3 ºC'
     this.boilingPoint = '2820°C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s² 4p²'
     this.physicalState = 'Solid'
     this.discovery = '1886'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '14'
     this.series = 'Metalloid'
     this.isotopes = '5'
    },
    Tin (){
     this.dialogVisible = true
     this.atomicNumber = '50'
     this.title = 'Tin'
     this.image = 'https://media0.giphy.com/media/VFenXo78YC7X5TvUGg/giphy.gif?cid=ecf05e47juh4k6um00m2vkxi5uimpfqbyda0uykv64rtnxvn&rid=giphy.gif&ct=g'
     this.symbol = 'Sn'
     this.atomicMass = '118.71'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '231.93 ºC'
     this.boilingPoint = '2602 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p²'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '5'
     this.group = '14'
     this.series = 'Post Transition Metals'
     this.isotopes = '10'
    },
    Lead (){
     this.dialogVisible = true
     this.atomicNumber = '82'
     this.title = 'Lead'
     this.image = 'https://media0.giphy.com/media/SwBpCOZYXVz6jOe8je/giphy.gif?cid=ecf05e47b3vcd6h0v2d2zth7s3axpdwng8y66nskr1l27yu2&rid=giphy.gif&ct=g'
     this.symbol = 'Pb'
     this.atomicMass = '207.2'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '327.46 ºC'
     this.boilingPoint = '1749 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p²'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '6'
     this.group = '14'
     this.series = 'Post Transition Metals'
     this.isotopes = '4'
    },
    Flerovium (){
     this.dialogVisible = true
     this.atomicNumber = '114'
     this.title = 'Flerovium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Flerovium-2.jpg'
     this.symbol = 'Fl'
     this.atomicMass = '289'
     this.discoveredBy = 'Scientists from the Joint Institute for Nuclear Research in Dubna, Russia and the Lawrence Livermore National Laboratory, California, USA'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Kr] 5s¹'
     this.physicalState = 'Unknown'
     this.discovery = '1998'
     this.blocks = 'P block'
     this.period = '7'
     this.group = '14'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
    Holmium (){
     this.dialogVisible = true
     this.atomicNumber = '67'
     this.title = 'Holmium'
     this.image = 'https://periodictable.com/Samples/067.4/s9s.JPG'
     this.symbol = 'Ho'
     this.atomicMass = '164.9303'
     this.discoveredBy = 'Per Teodor Cleve at Uppsala, Sweden and independently by Marc Delafontaine and Louis Soret in Switzerland.'
     this.meltingPoint = '1474 ºC'
     this.boilingPoint = '2700 °C'
     this.electronicConfiguration = '[Xe] 4f¹¹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1867'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '1'
    },
    Einsteinium (){
     this.dialogVisible = true
     this.atomicNumber = '99'
     this.title = 'Einsteinium'
     this.image = 'https://media1.giphy.com/media/ENOQ49YGjmxPzkhuYJ/giphy.gif?cid=ecf05e473v30een6yxl16dpn2eqcwn8ssaq41z4oabt2kgzi&rid=giphy.gif&ct=g'
     this.symbol = 'Es'
     this.atomicMass = '252'
     this.discoveredBy = 'Einsteinium was discovered as a component of the debris of the first hydrogen bomb explosion in'
     this.meltingPoint = '860 ºC'
     this.boilingPoint = 'N/A'
     this.electronicConfiguration = '[Rn] 5f¹¹ s²'
     this.physicalState = 'Solid'
     this.discovery = '1952'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
    Nitrogen (){
     this.dialogVisible = true
     this.atomicNumber = '7'
     this.title = 'Nitrogen'
     this.image = 'https://periodictable.com/Samples/007.8/s7s.JPG'
     this.symbol = 'N'
     this.atomicMass = '14.0067'
     this.discoveredBy = 'Daniel Rutherford'
     this.meltingPoint = '-210.1 ºC'
     this.boilingPoint = '195.79 °C'
     this.electronicConfiguration = '[He] 2s² 2p³'
     this.physicalState = 'Gas'
     this.discovery = '1772'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '15'
     this.series = 'Reactive nonmetals'
     this.isotopes = '2'
    },
    Phosphorus (){
     this.dialogVisible = true
     this.atomicNumber = '15'
     this.title = 'Phosphorus'
     this.image = 'https://media3.giphy.com/media/q3Yd4oczhE2iGQFDR9/giphy.gif?cid=ecf05e47gm5vffganka0y26u6v3p33imeodfk53fl5ulnvf7&rid=giphy.gif&ct=g'
     this.symbol = 'P'
     this.atomicMass = '30.9738'
     this.discoveredBy = 'Hennig Brandt'
     this.meltingPoint = '44.2 ºC'
     this.boilingPoint = '280.5 °C'
     this.electronicConfiguration = '[Ne] 3s² 3p³'
     this.physicalState = 'Solid'
     this.discovery = '1669'
     this.blocks = 'P block'
     this.period = '3'
     this.group = '15'
     this.series = 'Reactive nonmetals'
     this.isotopes = '1'
    },
    Arsenic (){
     this.dialogVisible = true
     this.atomicNumber = '33'
     this.title = 'Arsenic'
     this.image = 'https://media0.giphy.com/media/gH2RV00WIBEzebvTgN/giphy.gif?cid=ecf05e47145huldbkdopkdgr9e6sl90pzb5hxsppr20aga7r&rid=giphy.gif&ct=g'
     this.symbol = 'As'
     this.atomicMass = '74.9216'
     this.discoveredBy = 'Albertus Magnus'
     this.meltingPoint = '817 ºC'
     this.boilingPoint = '614 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s² 4p³'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '15'
     this.series = 'Metalloid'
     this.isotopes = '1'
    },
    Antimony (){
     this.dialogVisible = true
     this.atomicNumber = '51'
     this.title = 'Antimony'
     this.image = 'https://media2.giphy.com/media/MdB0ixWdagVYZG0gkD/giphy.gif?cid=ecf05e47cvl7xev77sye8f11dfxy3bqy58xxu9e53d2qxkyu&rid=giphy.gif&ct=g'
     this.symbol = 'Sb'
     this.atomicMass = '121.76'
     this.discoveredBy = 'The Ancients'
     this.meltingPoint = '630.63 ºC'
     this.boilingPoint = '1587 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p³'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '5'
     this.group = '15'
     this.series = 'Metalloid'
     this.isotopes = '2'
    },
    Bismuth (){
     this.dialogVisible = true
     this.atomicNumber = '83'
     this.title = 'Bismuth'
     this.image = 'https://media0.giphy.com/media/gFsfVMDEDiHGcBp7BO/giphy.gif?cid=ecf05e47jg2359y1l4ewgxm8uymtw59kqn5rtfqisg5xq8og&rid=giphy.gif&ct=g'
     this.symbol = 'Bi'
     this.atomicMass = '208.9804'
     this.discoveredBy = 'Claude Geoffroy the Younger.'
     this.meltingPoint = '271.3 ºC'
     this.boilingPoint = '1564 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p³'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '6'
     this.group = '15'
     this.series = 'Post Transition Metals'
     this.isotopes = '1'
    },

     Moscovium (){
     this.dialogVisible = true
     this.atomicNumber = '115'
     this.title = 'Moscovium'
     this.image = 'https://media0.giphy.com/media/HYnkSyWa8z5O3UgESz/giphy.gif?cid=ecf05e47w625cfz77bnb0mf8v9ggnmheag7vy26fzn7bvs3i&rid=giphy.gif&ct=g'
     this.symbol = 'Mc'
     this.atomicMass = '288'
     this.discoveredBy = 'Joint Institute for Nuclear Research'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Kr] 5s¹'
     this.physicalState = 'Unknown'
     this.discovery = '2010'
     this.blocks = 'P block'
     this.period = '7'
     this.group = '15'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Erbium (){
     this.dialogVisible = true
     this.atomicNumber = '68'
     this.title = 'Erbium'
     this.image = 'https://periodictable.com/Samples/068.5/s9s.JPG'
     this.symbol = 'Er'
     this.atomicMass = '167.259'
     this.discoveredBy = 'Nobel Institute for Physics'
     this.meltingPoint = '1497 ºC'
     this.boilingPoint = '2868 °C'
     this.electronicConfiguration = '[Xe] 4f¹² 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1842'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '6'
    },
     Fermium (){
     this.dialogVisible = true
     this.atomicNumber = '100'
     this.title = 'Fermium'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Fermium-Ytterbium_Alloy.jpg/220px-Fermium-Ytterbium_Alloy.jpg'
     this.symbol = 'Fm'
     this.atomicMass = '257'
     this.discoveredBy = 'Albert Ghiorso and colleagues'
     this.meltingPoint = '1527 ºC'
     this.boilingPoint = 'N/A'
     this.electronicConfiguration = '[Rn] 5f¹² s²'
     this.physicalState = 'Solid'
     this.discovery = '1952'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
     Oxygen (){
     this.dialogVisible = true
     this.atomicNumber = '8'
     this.title = 'Oxygen'
     this.image = 'https://media4.giphy.com/media/W2KU5PKZJHnbF4pwc2/giphy.gif?cid=ecf05e477ts7h6vrg2n2wbu7kim9oouxkvwd1xc7nh5c6eks&rid=giphy.gif&ct=g'
     this.symbol = 'O'
     this.atomicMass = '15.9994'
     this.discoveredBy = 'Joseph Priestly'
     this.meltingPoint = '-218.3ºC'
     this.boilingPoint = '-218.3 °C'
     this.electronicConfiguration = '[He] 2s² 2p⁴'
     this.physicalState = 'Gas'
     this.discovery = '1774'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '16'
     this.series = 'Reactive nonmetals'
     this.isotopes = '3'
    },
     Sulfur (){
     this.dialogVisible = true
     this.atomicNumber = '16'
     this.title = 'Sulfur'
     this.image = 'https://media1.giphy.com/media/Te1DYtRJ77XbYqsJDx/giphy.gif?cid=ecf05e47uazzpew611kanwesp4sme3acc39r7cvx5tt46itf&rid=giphy.gif&ct=g'
     this.symbol = 'S'
     this.atomicMass = '32.065'
     this.discoveredBy = 'Antoine Lavoisier'
     this.meltingPoint = '115.21 ºC'
     this.boilingPoint = '444.72 °C'
     this.electronicConfiguration = '[Ne] 3s² 3p⁴'
     this.physicalState = 'Solid'
     this.discovery = 'Ancient'
     this.blocks = 'P block'
     this.period = '3'
     this.group = '16'
     this.series = 'Reactive nonmetals'
     this.isotopes = '4'
    },
     Selenium (){
     this.dialogVisible = true
     this.atomicNumber = '34'
     this.title = 'Selenium'
     this.image = 'https://periodictable.com/Samples/034.12/s9s.JPG'
     this.symbol = 'Se'
     this.atomicMass = '78.96'
     this.discoveredBy = 'Jöns Jacob Berzelius'
     this.meltingPoint = '221 ºC'
     this.boilingPoint = '685 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s² 4p⁴'
     this.physicalState = 'Solid'
     this.discovery = '1817'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '16'
     this.series = 'Reactive nonmetals'
     this.isotopes = '6'
    },
     Tellurium (){
     this.dialogVisible = true
     this.atomicNumber = '52'
     this.title = 'Tellurium'
     this.image = 'https://theodoregray.com/periodictable/Samples/052.4/s13s.JPG'
     this.symbol = 'Te'
     this.atomicMass = '127.6'
     this.discoveredBy = 'Franz Muller von Reichenstein'
     this.meltingPoint = '449.51 ºC'
     this.boilingPoint = '988 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p⁴'
     this.physicalState = 'Solid'
     this.discovery = '1783'
     this.blocks = 'P block'
     this.period = '5'
     this.group = '16'
     this.series = 'Metalloid'
     this.isotopes = '8'
    },
     Polonium (){
     this.dialogVisible = true
     this.atomicNumber = '84'
     this.title = 'Polonium'
     this.image = 'https://periodictable.com/Samples/084.8/s9s.JPG'
     this.symbol = 'Po'
     this.atomicMass = '209'
     this.discoveredBy = 'Pierre and Marie Curie'
     this.meltingPoint = '254ºC'
     this.boilingPoint = '962 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p⁴'
     this.physicalState = 'Solid'
     this.discovery = '1898'
     this.blocks = 'P block'
     this.period = '6'
     this.group = '16'
     this.series = 'Post Transition Metals'
     this.isotopes = '1'
    },
     Livermorium (){
     this.dialogVisible = true
     this.atomicNumber = '116'
     this.title = 'Livermorium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Livermorium-2.jpg'
     this.symbol = 'Lv'
     this.atomicMass = '293'
     this.discoveredBy = 'Joint Institute for Nuclear Research and Lawrence Livermore National Laboratory'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = 'Unknown'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹⁰ 7s² 7p⁴'
     this.physicalState = 'Unknown'
     this.discovery = '2000'
     this.blocks = 'p block'
     this.period = '7'
     this.group = '16'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Thulium (){
     this.dialogVisible = true
     this.atomicNumber = '69'
     this.title = 'Thulium'
     this.image = 'https://periodictable.com/Samples/069.1/s9s.JPG'
     this.symbol = 'Tm'
     this.atomicMass = '168.9342'
     this.discoveredBy = 'Per Theodor Cleve'
     this.meltingPoint = '1545 ºC'
     this.boilingPoint = '1950 °C'
     this.electronicConfiguration = '[Xe] 4f¹³ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1879'
     this.blocks = 'f block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '1'
    },
     Mendelevium (){
     this.dialogVisible = true
     this.atomicNumber = '101'
     this.title = 'Mendelevium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Mendelevium-2.jpg'
     this.symbol = 'Md'
     this.atomicMass = '258'
     this.discoveredBy = 'G.T. Seaborg'
     this.meltingPoint = '827 ºC'
     this.boilingPoint = 'N/A °C'
     this.electronicConfiguration = '[Rn] 5f¹³ s²'
     this.physicalState = 'Solid'
     this.discovery = '1955'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },
     Fluorine (){
     this.dialogVisible = true
     this.atomicNumber = '9'
     this.title = 'Fluorine'
     this.image = 'https://media1.giphy.com/media/Xf1zV6oOrMs0vMDz7V/giphy.gif?cid=ecf05e476xs32py6p566gz4590f02mvwsb25eqe2hhk06aww&rid=giphy.gif&ct=g'
     this.symbol = 'F'
     this.atomicMass = '18.9984'
     this.discoveredBy = 'Henri Moissan'
     this.meltingPoint = '-219.6 °C'
     this.boilingPoint = '-188.12 °C'
     this.electronicConfiguration = '[He] 2s² 2p⁵'
     this.physicalState = 'Gas'
     this.discovery = '1886'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '17'
     this.series = 'Reactive nonmetals'
     this.isotopes = '1'
    },
     Chlorine (){
     this.dialogVisible = true
     this.atomicNumber = '17'
     this.title = 'Chlorine'
     this.image = 'https://www.chemedx.org/sites/www.chemedx.org/files/styles/large/public/halite.jpg?itok=_9hVV-Q-'
     this.symbol = 'Cl'
     this.atomicMass = '35.453'
     this.discoveredBy = 'Carl Wilhelm Scheele'
     this.meltingPoint = '-101.5 ºC'
     this.boilingPoint = '-34.04 °C'
     this.electronicConfiguration = '[Ne] 3s² 3p⁵'
     this.physicalState = 'Gas'
     this.discovery = '1774'
     this.blocks = 'p block'
     this.period = '3'
     this.group = '17'
     this.series = 'Reactive nonmetals'
     this.isotopes = '2'
    },
     Bromine (){
     this.dialogVisible = true
     this.atomicNumber = '35'
     this.title = 'Bromine'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/3/35/Bromine_vial_in_acrylic_cube.jpg'
     this.symbol = 'Br'
     this.atomicMass = '79.904'
     this.discoveredBy = 'Johan Gottlieb Gahn'
     this.meltingPoint = '-7.3 ºC'
     this.boilingPoint = '59 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s² 4p⁵'
     this.physicalState = 'Liquid'
     this.discovery = '1826'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '17'
     this.series = 'Reactive nonmetals'
     this.isotopes = '2'
    },
     Iodine (){
     this.dialogVisible = true
     this.atomicNumber = '53'
     this.title = 'Iodine'
     this.image = 'https://media4.giphy.com/media/hvGeeLiwlGPByRYiho/giphy.gif?cid=ecf05e475dfkjhcvavjb756ig16h8ce10nsb1czdpf2ydnnp&rid=giphy.gif&ct=g'
     this.symbol = 'I'
     this.atomicMass = '126.9045'
     this.discoveredBy = 'Bernard Courtois'
     this.meltingPoint = '113.7 ºC'
     this.boilingPoint = '184.3 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p⁵'
     this.physicalState = 'Solid'
     this.discovery = '1811'
     this.blocks = 'P block'
     this.period = '5'
     this.group = '17'
     this.series = 'Reactive nonmetals'
     this.isotopes = '1'
    },
     Astatine (){
     this.dialogVisible = true
     this.atomicNumber = '85'
     this.title = 'Astatine'
     this.image = 'https://media0.giphy.com/media/VEsyJ5aXRh2KEXhICr/giphy.gif?cid=ecf05e47y1ao1hp100vs3epi243cfwogmke1teux57v23gy3&rid=giphy.gif&ct=g'
     this.symbol = 'At'
     this.atomicMass = '210'
     this.discoveredBy = 'Dale R. Corson, Kenneth Ross MacKenzie, Emilio Segrè'
     this.meltingPoint = '302 ºC'
     this.boilingPoint = '350 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p⁵'
     this.physicalState = 'Solid'
     this.discovery = '1940'
     this.blocks = 'P block'
     this.period = '6'
     this.group = '17'
     this.series = 'Metalloid'
     this.isotopes = '1'
    },
     Tennessine (){
     this.dialogVisible = true
     this.atomicNumber = '117'
     this.title = 'Tennessine'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Tennessine-2.jpg'
     this.symbol = 'Ts'
     this.atomicMass = '260.9'
     this.discoveredBy = 'Scientists from the Joint Institute for Nuclear Research, Russia, and the USA.'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = '80±30 °C'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹⁰ 7s² 7p⁵'
     this.physicalState = 'Unknown'
     this.discovery = '1861'
     this.blocks = 'S block'
     this.period = '7'
     this.group = '17'
     this.series = 'Unknown'
     this.isotopes = '1'
    }, 
    
    Ytterbium (){
     this.dialogVisible = true
     this.atomicNumber = '70'
     this.title = 'Ytterbium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Ytterbium-21.jpg'
     this.symbol = 'Yb'
     this.atomicMass = '173.04'
     this.discoveredBy = 'Ytterbium was discovered by Jean Charles Galissard de Marignac'
     this.meltingPoint = '819 ºC'
     this.boilingPoint = '1196 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1878'
     this.blocks = 'F block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '7'
    },

     Nobelium (){
     this.dialogVisible = true
     this.atomicNumber = '102'
     this.title = 'Nobelium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Nobelium-2.jpg'
     this.symbol = 'No'
     this.atomicMass = '259'
     this.discoveredBy = 'Nobel Institute for Physics'
     this.meltingPoint = '827 ºC'
     this.boilingPoint = 'N/A °C'
     this.electronicConfiguration = '[Rn] 5f¹⁴ s²'
     this.physicalState = 'Solid'
     this.discovery = '1958'
     this.blocks = 'F block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    }, 
    
    Helium (){
     this.dialogVisible = true
     this.atomicNumber = '2'
     this.title = 'Helium'
     this.image = 'https://media2.giphy.com/media/YPEXWPopZcBKiEbWgq/giphy.gif?cid=ecf05e47dbjkl3c8jwf337uc0xuuys6vt1oud9zv4mv2shre&rid=giphy.gif&ct=g'
     this.symbol = 'He'
     this.atomicMass = '4.0026'
     this.discoveredBy = 'Sir William Ramsay in London, Per Teodor Cleve and Nils Abraham Langlet.'
     this.meltingPoint = '-272.2 ºC'
     this.boilingPoint = '-268.928 °C'
     this.electronicConfiguration = '1s²'
     this.physicalState = 'Gas'
     this.discovery = '1895'
     this.blocks = 'S block'
     this.period = '1'
     this.group = '18'
     this.series = 'Noble Gases'
     this.isotopes = '2'
    },
     Neon (){
     this.dialogVisible = true
     this.atomicNumber = '10'
     this.title = 'Neon'
     this.image = 'https://media1.giphy.com/media/nqh2NNyuwGMhjUK17h/giphy.gif?cid=ecf05e47z6o4tk69sbkdbsf8yyq2rwtfk3hjoqq7bx9oieuu&rid=giphy.gif&ct=g'
     this.symbol = 'Ne'
     this.atomicMass = '20.1797'
     this.discoveredBy = 'Sir William Ramsay and Morris Travers'
     this.meltingPoint = '-248.59 ºC'
     this.boilingPoint = '-246.08 °C'
     this.electronicConfiguration = '[He] 2s² 2p⁶'
     this.physicalState = 'Gas'
     this.discovery = '1898'
     this.blocks = 'P block'
     this.period = '2'
     this.group = '18'
     this.series = 'Noble Gases'
     this.isotopes = '3'
    },

     Argon (){
     this.dialogVisible = true
     this.atomicNumber = '18'
     this.title = 'Argon'
     this.image = 'https://media1.giphy.com/media/YlZK330IGhhf5DxyKx/giphy.gif?cid=ecf05e47fa0w6cohzjcpnfq7vsmdmcyk6qa14g30leoxb0q1&rid=giphy.gif&ct=g'
     this.symbol = 'Ar'
     this.atomicMass = '39.948'
     this.discoveredBy = 'Humphry Davy'
     this.meltingPoint = '-189.3 ºC'
     this.boilingPoint = '-185.8 °C'
     this.electronicConfiguration = '[Ne] 3s² 3p⁶'
     this.physicalState = 'Gas'
     this.discovery = '1894'
     this.blocks = 'P block'
     this.period = '3'
     this.group = '18'
     this.series = '1894'
     this.isotopes = '3'
    }, 
    
    Krypton (){
     this.dialogVisible = true
     this.atomicNumber = '36'
     this.title = 'Krypton'
     this.image = 'https://upload.wikimedia.org/wikipedia/commons/5/50/Krypton_discharge_tube.jpg'
     this.symbol = 'Kr'
     this.atomicMass = '83.8'
     this.discoveredBy = 'Sir William Ramsay and Morris Travers'
     this.meltingPoint = '-157.36 ºC'
     this.boilingPoint = '-153.22 °C'
     this.electronicConfiguration = '[Ar] 3d¹⁰ 4s² 4p⁶'
     this.physicalState = 'Gas'
     this.discovery = '1898'
     this.blocks = 'P block'
     this.period = '4'
     this.group = '18'
     this.series = 'Noble Gases'
     this.isotopes = '6'
    },
     Xenon (){
     this.dialogVisible = true
     this.atomicNumber = '54'
     this.title = 'Xenon'
     this.image = 'https://media0.giphy.com/media/MCvKi08Bs5Es0jVCfC/giphy.gif?cid=ecf05e47sfuzjrzblh8sdbywf2pitmxpfbn4qmvmoc4wb3va&rid=giphy.gif&ct=g'
     this.symbol = 'Xe'
     this.atomicMass = '131.293'
     this.discoveredBy = 'William Ramsay'
     this.meltingPoint = '-111.8 ºC'
     this.boilingPoint = '-108 °C'
     this.electronicConfiguration = '[Kr] 4d¹⁰ 5s² 5p⁶'
     this.physicalState = 'Gas'
     this.discovery = '1898'
     this.blocks = 'p block'
     this.period = '5'
     this.group = '18'
     this.series = 'Noble Gases'
     this.isotopes = '9'
    },
     Radon (){
     this.dialogVisible = true
     this.atomicNumber = '86'
     this.title = 'Radon'
     this.image = 'https://media2.giphy.com/media/XGDzpt2vFeciNAqO8B/giphy.gif?cid=ecf05e47q6upesawkxer0lr7hcru6u1kl4dghkmebkt1muit&rid=giphy.gif&ct=g'
     this.symbol = 'Rn'
     this.atomicMass = '222'
     this.discoveredBy = 'Friedrich Ernst Dorn'
     this.meltingPoint = '-71 ºC'
     this.boilingPoint = '-61.7 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹⁰ 6s² 6p⁶'
     this.physicalState = 'Gas'
     this.discovery = '1861'
     this.blocks = 'p block'
     this.period = '6'
     this.group = '18'
     this.series = 'Noble Gases'
     this.isotopes = '1'
    },
     Oganesson (){
     this.dialogVisible = true
     this.atomicNumber = '118'
     this.title = 'Oganesson'
     this.image = 'https://whatmaster.com/wp-content/uploads/2020/11/periodic-table-element-ununtrium-icon-vector-11228447-min-4.jpg'
     this.symbol = 'Og'
     this.atomicMass = '294'
     this.discoveredBy = 'Joint Institute for Nuclear Research and Lawrence Livermore National Laboratory'
     this.meltingPoint = 'Unknown'
     this.boilingPoint = '80±30 °C'
     this.electronicConfiguration = '[Rn] 7s² 7p⁶ 5f¹⁴ 6d¹⁰'
     this.physicalState = 'Unknown'
     this.discovery = '1861'
     this.blocks = 'P block'
     this.period = '7'
     this.group = '18'
     this.series = 'Unknown'
     this.isotopes = '1'
    },
     Lutetium (){
     this.dialogVisible = true
     this.atomicNumber = '71'
     this.title = 'Lutetium'
     this.image = 'https://theodoregray.com/periodictable/Samples/071.3/s14s.JPG'
     this.symbol = 'Lu'
     this.atomicMass = '174.967'
     this.discoveredBy = 'George Urbain'
     this.meltingPoint = '1663 °C'
     this.boilingPoint = '3402 °C'
     this.electronicConfiguration = '[Xe] 4f¹⁴ 5d¹ 6s²'
     this.physicalState = 'Solid'
     this.discovery = '1907'
     this.blocks = 'D block'
     this.period = '6'
     this.group = 'Lanthanides'
     this.series = 'Lanthanoids'
     this.isotopes = '2'
    },
     Lawrencium (){
     this.dialogVisible = true
     this.atomicNumber = '103'
     this.title = 'Lawrencium'
     this.image = 'https://cdn1.byjus.com/wp-content/uploads/2018/08/Lawrencium-2.jpg'
     this.symbol = 'Lr'
     this.atomicMass = '262'
     this.discoveredBy = 'Albert Ghiorso'
     this.meltingPoint = '1627 ºC'
     this.boilingPoint = 'N/A'
     this.electronicConfiguration = '[Rn] 5f¹⁴ 6d¹ s²'
     this.physicalState = 'Solid'
     this.discovery = '1961'
     this.blocks = 'D block'
     this.period = '7'
     this.group = 'Actinides'
     this.series = 'Actinoids'
     this.isotopes = '1'
    },



   submit(){
     if(this.atomicNumber === 1) {
      this.dialogVisible = false
     } else if (this.atomicNumber === 3) {
      this.dialogVisible = false
     }
   }
  }
  }

</script>


<style scoped>


.alkali {
  padding: 0%;
  background: linear-gradient(90deg, rgb(252, 194, 5), rgb(248, 225, 14)) !important;
  border-color: rgb(247, 210, 3);
  margin: 0 auto;
}
.alkali:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}


.actinide {
  padding: 0%;
  background: linear-gradient(90deg, rgb(248, 90, 209), rgb(252, 50, 191)) !important;
  border-color: rgb(244, 92, 216);
  margin: 0 auto;
}
.actinide:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}


.lanthanide {
  padding: 0%;
   background: linear-gradient(90deg, rgb(239, 255, 12), rgb(204, 152, 9)) !important;
  border-color: rgb(230, 248, 63);
  margin: 0 auto;
}
.lanthanide:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.transitionMetals {
  padding: 0%;
background: linear-gradient(90deg, rgb(252, 194, 5), rgb(245, 103, 9)) !important;
  border-color: rgb(255, 148, 66);
  margin: 0 auto;
}
.transitionMetals:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.transitionMetalsEarth {
  padding: 0%;
 background: linear-gradient(90deg, rgb(187, 145, 9), rgb(255, 130, 46)) !important;
  border-color: rgb(207, 153, 52) ;
  margin: 0 auto;
}
.transitionMetalsEarth:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.postTransitionMetals {
  padding: 0%;
 background: linear-gradient(90deg, rgb(152, 255, 241), rgb(9, 204, 253)) !important;
  border-color: rgb(122, 255, 204);
  margin: 0 auto;
}
.postTransitionMetals:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.metalloids {
  padding: 0%;
  background: linear-gradient(90deg, rgb(82, 236, 95), rgb(92, 255, 247)) !important;
  border-color: linear-gradient(90deg, rgb(56, 107, 248), rgb(53, 10, 245)) !important;
  margin: 0 auto;
}
.metalloids:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}


.nobleGas {
  padding: 0%;
  background: linear-gradient(90deg, rgb(8, 255, 222), rgb(51, 231, 255)) !important;
  border-color: rgb(60, 255, 229);
  margin: 0 auto;
}
.nobleGas:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.reactiveNonMetals {
  padding: 0%;
  background: linear-gradient(90deg, rgb(236, 12, 180), rgb(250, 120, 211)) !important;
  border-color: rgb(237, 100, 255);
  margin: 0 auto;
}
.reactiveNonMetals:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}



.unknown {
  padding: 0%;
   background: linear-gradient(90deg, rgb(248, 125, 54), rgb(209, 99, 26)) !important;
  border-color: rgb(255, 148, 66);
  margin: 0 auto;
}
.unknown:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}


.liquid {
  padding: 0%;
   background: linear-gradient(90deg, rgb(31, 253, 179), rgb(20, 176, 204)) !important;
  border-color: rgb(83, 192, 255);
  margin: 0 auto;
}

.liquid:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.gas {
  padding: 0%;
  background: linear-gradient(90deg, rgb(250, 83, 200), rgb(248, 131, 190)) !important;
  border-color: rgb(252, 67, 83);
  margin: 0 auto;
}

.gas:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}

.solid {
  padding: 0%;
  background: linear-gradient(90deg, rgb(73, 124, 145), rgb(164, 222, 245)) !important;
  border-color: rgb(181, 196, 191) ;
  margin: 0 auto;
}

.solid:hover {
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.5);
}



.box-card {
  padding: 0%;
  background-color: white;
  transition: transform .2s; /* Animation */
  width: 118px;
  height: 118px;
  margin: 0px auto;
}
.box-card:hover{
  background: rgb(255, 255, 255);
  font-weight: bold;
   transform: scale(1.2);
}
.el-button:hover{
  color:black
}
.el-button{
  margin-bottom:5px;
  color:black
}

.box-card2 {
  padding: 0%;
  background-color: white;
   border-color: rgb(0, 0, 0);
  width: 118px;
  height: 118px;
  margin: 1.5px auto;
}

.atomicNumber {
float: left; 
font-weight: bold; 


}

.atomicMass{
  float: right; 

}

.header{
  display: flex;
  justify-content: space-between;
  padding:0%;
  margin-bottom: 5px;
}

.symbol{
  font-weight:bold;
  font-size: 40px;
  align-content: center;
}
.atomicName{
  font-size: 12px;
  margin-bottom: 15px;
  margin-left: -3px;
  padding-bottom: 10px;
}

.group1{
  float: left;
  margin-left: 25px;

  
}
.group2{
  float: left;
  margin: 5px;
  margin-top: 124px;
}
.group3{
  float: left;
 margin: 5px;
  margin-top: 370px;
}
.group4{
  float: left;
  margin: 5px;
  margin-top: 370px;
}

.group5{
  float: left;
  margin: 5px;
  margin-top: 370px;
}

.group6{
  float: left;
 margin: 5px;
  margin-top: 370px;
}

.group7{
  float: left;
  margin: 5px;
  margin-top: 370px;
}

.group8{
  float: left;
 margin: 5px;
  margin-top: 370px;
}

.group9{
  float: left;
  margin: 5px;
  margin-top: 370px;
}

.group10{
  float: left;
 margin: 5px;
  margin-top: 370px;
}

.group11{
 float: left;
 margin: 5px;
  margin-top: 370px;
}

.group12{
 float: left;
 margin: 5px;
  margin-top: 370px;
}

.group13{
 float: left;
  margin: 5px;
  margin-top: 124px;
}

.group14{
float: left;
  margin: 5px;
  margin-top: 124px;
}

.group15{
 float: left;
   margin: 5px;
  margin-top: 124px;
}


.group16{
 float: left;
   margin: 5px;
  margin-top: 124px;
}

.group17{
  float: left;
  margin: 5px;
  margin-top: 124px;
}

.group18{
  float: left;
}
.span{
  font-size: 25px;
}
.container{
  display: flex;
  justify-content: left;
  font-size: 15px;
  
}
.container2{
  display: flex;
  justify-content: left;
  font-size: 15px;
  
}
.fieldset{
    margin: 15px;
}
.el-card{

align-items: center;
 
}

.home{
  width: 100%;
  height: auto
}

</style>
