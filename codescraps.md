
<article>
  <a href="{{ site.github.url }}{{ post.url }}">
    <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><span>{{ post.title }}</span></h2>
    </div>
  </a>
</article>

<!-- <section>
  {% if site.posts[0] %}

    {% capture currentyear %}{{ 'now' | date: "%Y" }}{% endcapture %}
    {% capture firstpostyear %}{{ site.posts[0].date | date: '%Y' }}{% endcapture %}
    {% if currentyear == firstpostyear %}
        <h3>This year's posts</h3>
    {% else %}  
        <h3>{{ firstpostyear }}</h3>
    {% endif %}

    {%for post in site.posts %}
      {% unless post.next %}
        <ul>
      {% else %}
        {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
        {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
        {% if year != nyear %}
          </ul>
          <h3>{{ post.date | date: '%Y' }}</h3>
          <ul>
        {% endif %}
      {% endunless %}
        <li><time>{{ post.date | date:"%d %b" }} - </time>
          <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">
            {{ post.title }}
          </a>
        </li>
    {% endfor %}
    </ul>

  {% endif %}
</section> -->

<!--
<ul>
  {% for post in site.posts %}
      <li>
      <div class="featured-post" {% if post.image %}style="background-image:url({{ site.github.url }}/assets/img/{{ post.image }})"{% endif %}>
      <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
      <p>{{ post.content | strip_html | truncatewords:50 }}</p>
      </li>
  {% endfor %}
</ul>
-->



@import "normalize";
@import "fonts";
@import "rouge-base16-dark";
@import url("https://fonts.googleapis.com/css2?family=Martian+Mono:wght@100..800&display=swap");


html { 

  font:14px/22px 'Courier New', monospace, 'Martian Mono',Arial,  "Lucida Sans Unicode", verdana, lucida, sans-serif; 
   height:100vh;
  background-color: #002DE0; /* For browsers that do not support gradients 
    background-image: linear-gradient(#002DE0, #0032A0); 
    background: rgb(0,45,224);
  background: linear-gradient(90deg, rgba(0,45,224,1) 0%, rgba(0,50,160,1) 90%);
  */background: url(https://eoimages.gsfc.nasa.gov/images/imagerecords/153000/153466/pyramidlake_oli2_20241008_lrg.jpg) no-repeat 0 0 fixed; 
  background-size: cover;
   line-height: 1.5;
   -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh;
  width: 100vw;
  column-fill: balance;
  word-break: break-all;
  font-variation-settings:
  "wdth" 100;
}

body {


}
.paginator {

  width: 100vw;

}

.featured-post {
  height: 400px;
  margin: 0px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.featured-post h2 {
  bottom: 0;
  margin: 0;
  padding: 10px;
  position: absolute;
}
.featured-post h2 span {
  display: inline-block;
  color: white;
  font: bold 24px/45px Helvetica, Sans-Serif;
  letter-spacing: -1px;
  background: rgb(0, 0, 0); /* fallback color */
  background: rgba(0, 0, 0, 0.7);
  padding: 10px;
}
.featured-post span a {
  color: white;
}
.featured-post h1 {
  margin: 10px;
}


#content {
  flex-direction: column;
  display: flex;
  flex-wrap: wrap;
  border-radius: 0px 0px 0px 0px;
  width: 85vh; 
padding: 0px;
  margin-bottom: 40px;
  margin-right: auto;
  margin-left: auto;
  margin-top: -188px;
  line-height: 1.5;
/* opera does not like 'margin:20px auto' */
/* background: #666; */
border: 1px solid white;
background: url(https://mars.nasa.gov/msl-raw-images/proj/msl/redops/ods/surface/sol/04329/opgs/edr/ncam/NLB_781808042EDR_F1091998NCAM00354M_.JPG) no-repeat 0 0 fixed;
/* https://developer.mozilla.org/en-US/docs/Web/CSS/background-size */
background-size: cover;

/* background: url(https://mars.nasa.gov/mars2020-raw-images/pub/ods/surface/sol/01046/ids/edr/browse/rcam/RRF_1046_0759804806_506ECM_N0495338RHAZ02420_01_295J01_800.jpg) no-repeat 0 0 fixed; */
/* https://developer.mozilla.org/en-US/docs/Web/CSS/background-size */

text-align:left; 
/* part 2 of 2 centering hack */
voice-family: "\"}\"";
voice-family:inherit;
 

box-shadow: rgba(255,255,255, 0.4) 5px 5px, rgba(255,255,255, 0.3) 10px 10px, rgba(255,255,255, 0.2) 15px 15px, rgba(255,255,255, 0.1) 20px 20px, rgba(255,255,255, 0.05) 25px 25px;font-family: 'Martian Mono',-apple-system, Ariel, Verdana; 
/* color: #c9ff23;  */
overflow-y: auto;
}

#footer {
  flex-wrap: wrap;
  
  display: inline;
  grid-template-rows: auto auto auto;
  background-color: black;
  color: white;
  padding: 5px;
 
  }

img {
  width: 100%;
  height: auto;
  object-fit: contain;
/* or
  object-fit: cover; */
} 


  img[src*="cloudfront"] {width: 100%;
    border-bottom:solid 10px  #FCE30070;}
  img[alt*="USGS"] {width: 100%;
    border-bottom:solid 10px  #BF785E;}
  /* matches selection in URL/src */
  img[src*="nasa.gov"] {width: 100%;
    border-bottom:solid 10px  #c9ff2340;}
  img[alt="kk"] {
    width: 100%;
    
  }
  img[alt="whiteslavery"] {
    max-width: 15%;
    float: right;
  }
  img[alt="whiteslavery40"] {
    max-width: 40%;
    transform: rotate(45deg);
  }
  
  

  
svg { width:100%;}
.jumpmenu {  font-family: Verdana, Arial, Helvetica, sans-serif; font-size: 14px; background-color: #0dd9c4; color: #3df28b; border: #3df28b; border-top-width: 1px; border-right-width: 1px; border-bottom-width: 1px; border-left-width: 1px; font-weight: bold
  ;}
  
p {
margin-top:10px;
margin-bottom:10px;
display: block;
text-align: left;
width:100%;
color: white;
background: transparent
url(https://raw.githubusercontent.com/ThakaRashard/bubblegumpop/gh-pages/img/halfscreen-black.gif)
center repeat;
/* background: black; */
/* background: linear-gradient(90deg, black 0%, rgba(38,38,38,0.7049194677871149) 35%, rgba(89,89,89,0.5900735294117647) 100%); */
border-left: 1px solid #26a7de ;
column-count: auto;
column-fill: balance-all;
word-break: break-all;
hyphens: auto;
margin: 20px;
display:block;}

p:first-of-type {
   color:dodgerblue; 
  }


  a:hover,
  a:visited a:hover {
    font-size: 110%; 
    color: #63c0f5;
    text-shadow: 0 0 5px rgba(104, 182, 255, 0.5);
    
    
  
  }
  
  a {
    padding: 0px;
    color:#29F247 ;
    text-shadow: 0 0 5px rgba(41, 242, 71, 0.5);
    transition: all .4s ease-out;
  
  
  }
  
  
  a small {
    font-size:11px;
    color:#cffe14;
    margin-top:-0.6em;
    display:block;
  }

.mermaid { width: 100%;}


h1 {
  font: bolder 14px/18px 'Martian Mono',Arial,  "Lucida Sans Unicode", verdana, lucida, sans-serif; 
  
  font-size: 2em;
  color: white;
  text-shadow: rgba(255,255,255,1) 0px 0px 6px;
  /* background: linear-gradient(45deg, 
 #F2D338 25%, #262626 0, #262626 50%,
 #F2D338 0, #F2D338 75%, #262626 0);
background-size: 80.4px 80.4px; */

}


h2 {
  word-spacing: -.2ch;
  font-kerning: auto;
  letter-spacing: 2pt;
  background: transparent
   url(https://photojournal.jpl.nasa.gov/jpeg/PIA20753.jpg) center repeat;
    color: white;     
}



h3 {
  
  text-shadow:
  0 0 7px white,
  0 0 10px #2e97f2,
  0 0 21px white,
  0 0 42px white;


}
h1,
h2,
h3,
h4,
h5,
h6 {
  color: white;
  background: transparent
    url(https://raw.githubusercontent.com/ThakaRashard/bubblegumpop/gh-pages/img/halfscreen-black.gif)
    center repeat;
  font-weight: 900;
  margin: 5px;
  padding: 5px;

}



p, ul, ol, table, pre, dl {
  margin:0 0 20px;
}

h1, h2, h3 {
  line-height:1.1;
}

h1 {
  font-size:28px;
  color:white;
}

h2 {
  font-size: 24px;
  color:white;
}

h3, h4, h5, h6 {
  color:white;
}

h3 {
  font-size: 18px;
  line-height: 24px;
}




ul{
  list-style-image:url('../images/bullet.png');
}

strong {
  font-weight: bold;
  color: #14e4ff;
}

.wrapper {
  width:650px;
  margin:0 auto;
  position:relative;

}

section img {
  max-height: auto;
  max-width: 100%;



}


content img {
  max-height: auto;
  max-width: 100%;



}

 
.floatright img:nth-child(odd) {
  float: right;
}
.floatleft img:nth-child(even) {
  float: left;
  border-bottom: solid 10px #ffffff50;
}

blockquote {
  border-left:1px solid #ffcc00;
  margin:0;
  padding:0 0 0 20px;
  font-style:italic;
  color: white;
  text-shadow: rgba(255,255,255,1) 0px 0px 6px;
}

code {
  font-family: 'Martian Mono', Monaco, Bitstream Vera Sans Mono, Lucida Console, Terminal;
  font-size:13px;
  color:#efefef;
  text-shadow: 0px 1px 0px #000;
  margin: 0 4px;
  padding: 2px 6px;
  background: #33333350;
  border-radius: 2px;
}
/*
pre {
  padding:8px 15px;
  background: #333333;
  border-radius: 3px;
  border:1px solid #c7c7c7;
  overflow: auto;
  overflow-y: hidden;

  code {
    margin: 0px;
    padding: 0px;
  }
}
*/
pre {
  padding:8px 15px;
    border-radius: 3px;
  border:1px solid #b5e853;
  overflow: auto;
  overflow-y: hidden;
  background: transparent
  url(https://raw.githubusercontent.com/ThakaRashard/bubblegumpop/gh-pages/img/halfscreen-black.gif)
  center repeat;
  font: bold 14px/18px 'Martian Mono',Arial,  "Lucida Sans Unicode", verdana, lucida, sans-serif; 
  color:white;
  code {
    margin: 0px;
    padding: 0px;
  }
}


kbd {
  background-color: #fafbfc;
  border: 1px solid #c6cbd1;
  border-bottom-color: #959da5;
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 #959da5;
  color: #444d56;
  display: inline-block;
  font-size: 11px;
  line-height: 10px;
  padding: 3px 5px;
  vertical-align: middle;
}

table {
  width:100%;
  border-collapse:collapse;
}

th {
  text-align:left;
  padding:5px 10px;
  border-bottom:1px solid #e5e5e5;
  color: #444;
}

td {
  text-align:left;
  padding:5px 10px;
  border-bottom:1px solid #e5e5e5;
  border-right: 1px solid #ffcc00;

  &:first-child {
    border-left: 1px solid #ffcc00;
  }
}

hr {
  border: 0;
  outline: none;
  height: 11px;
  background: transparent url('../images/hr.gif') center center repeat-x;
  margin: 0 0 20px;
}

dt {
  color:#444;
  font-weight:700;
}

header {
 /* padding: 25px 20px 40px 20px;
  margin: 0;
  position: fixed;
  top: 0;
  left:0;
  right:0;
  width: 100%;
  text-align: center;
  background: url(../images/background.png) #4276b6;
  box-shadow: 1px 0px 2px rgba(0,0,0,.75);
  z-index:99;
  -webkit-font-smoothing:antialiased;
  min-height: 76px; */

  h1 {
    font: 40px/48px 'Martian Mono','Copse', "Helvetica Neue", Helvetica, Arial, sans-serif;
    color: #f3f3f3;
    text-shadow: 0px 2px 0px #235796;
    margin: 0px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    -o-text-overflow: ellipsis;
    -ms-text-overflow: ellipsis;
  }

  p {
    color: #d8d8d8;
    text-shadow:rgba(#000, 0.2) 0 1px 0;
    font-size: 18px;
    margin: 0px;
  }
}


  

small {
  font-size:12px;
}

nav {
  width: 230px;
  position: fixed;
  top: 220px;
  left:50%;
  margin-left:-580px;
  text-align: right;

  ul {
    list-style: none;
    list-style-image:none;
    font-size: 14px;
    line-height:24px;

    li {
      padding: 5px 0px;
      line-height: 16px;
      // padding-right:17px;
      // position:relative;
      // right:-12px;

      &.tag-h1 {
        font-size: 1em;
        text-decoration:none;
        font-weight:600;

        a:hover {
          font-size: 120%; 
          color: #63c0f5;
          text-shadow: 0 0 5px rgba(104, 182, 255, 0.5);
          
                 
        }
        a {
          font-weight: bold;
          color: white;
          transition: all .2s ease-out;
        }

        + .tag-h2 {

        }
      }

      &.tag-h2 {

        + .tag-h1 {
          margin-top:10px;
        }
      }
    }



    // .active {
    //   border-right:solid 4px #39C;
    //   padding-right:13px;
    // }
  }
}








@media print, screen and (max-width: 1060px) {

  div.wrapper {
    width:auto;
    margin:0;
  }

  nav{
    display: none;
  }

  header, section, content, footer {
    float:none;

    h1 {
      white-space: nowrap;
      background-color: #002DE0;
      overflow: hidden;
      text-overflow: ellipsis;
      -o-text-overflow: ellipsis;
      -ms-text-overflow: ellipsis;
    }
  }

  #banner {
    width: 100%;

    .downloads {
        margin-right: 60px;
      }

    .fork {
    }

    #logo {
      margin-right: 15px;
    }
  }

  section {
    border:1px solid #e5e5e5;
    border-width:1px 0;
    padding:20px 0;
    margin: 190px auto 20px;
    max-width: 600px;
  }

  content {
    border:1px solid #e5e5e5;
    border-width:1px 0;
    padding:20px 0;
    margin: 190px auto 20px;
    max-width: 600px;
  }

  footer{
    text-align: center;
    margin: 20px auto;
    position: relative;
    left:auto;
    bottom:auto;
    width:auto;
    }
}

@media print, screen and (max-width: 1000px) {
  body {
    word-wrap:break-word;
  }

  header {
    padding:0px 0px;
    margin: 0;

    h1 {
      font-size: 32px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      -o-text-overflow: ellipsis;
      -ms-text-overflow: ellipsis;
    }

    p { display: none;}
  }

  #banner {
    top: 80px;

    .fork {
      float: left;
      display: inline-block;
      margin-left: 0px;
    position:fixed;
    left:20px;

      }
  }

  section {
    margin-top: 0px;
    margin-bottom: 0px;
    width: auto;
  }

  content {
    margin-top: 0px;
    margin-bottom: 0px;
    width: auto;
  }

  header ul, header p.view {
    position:static;
  }
}

@media print, screen and (max-width: 1024px) {
  body {
  }

  header{
    position: relative;
    padding: 0px 0px;
    min-height: 0px;

    h1 {
      font-size: 24px;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      -o-text-overflow: ellipsis;
      -ms-text-overflow: ellipsis;
    }
  }
  section {
    margin-top: 0px;
  }
  content {
    margin-top: 0px;
  }
  #banner { display: none;}
  header ul {
    display:none;
  }
}

@media print {
  body {
    padding:0.4in;
    font-size:12pt;
    color:#444;
  }
}

@media print, screen and (max-height: 680px) {

  footer {
    text-align: center;
    margin: 20px auto;
    position: relative;
    left:auto;
    bottom:auto;
    width:auto;
  }
}

@media print, screen and (max-height: 480px) {
  nav {
    display: none;
  }

  footer {
    text-align: center;
    margin: 20px auto;
    position: relative;
    left:auto;
    bottom:auto;
    width:auto;
  }
}





.gallery-wrap {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  width: 100%;
  height: 70vh;
}

.item {
  flex: 1;
  height: 100%;
  background-position: center;
  background-size: cover;
  transition: flex 0.8s ease;
  
  &:hover{
    flex: 7;
  }
}

.item-1 { 
  background-image: url('https://mars.nasa.gov/msl-raw-images/proj/msl/redops/ods/surface/sol/04200/opgs/edr/ncam/NLB_770345493EDR_F1072484NCAM00256M_.JPG');
}

.item-2 { 
  background-image: url('https://mars.nasa.gov/msl-raw-images/msss/04202/mcam/4202MR1059130272102870C00_DXXX.jpg');
}

.item-3 { 
  background-image: url('https://mars.nasa.gov/msl-raw-images/proj/msl/redops/ods/surface/sol/04250/opgs/edr/ncam/NRB_774801663EDR_F1080222NCAM00200M_.JPG');
}

.item-4 { 
  background-image: url('https://mars.nasa.gov/msl-raw-images/msss/04202/mcam/4202ML1059130291702010C00_DXXX.jpg');
}

.item-5 { 
  background-image: url('https://mars.nasa.gov/msl-raw-images/proj/msl/redops/ods/surface/sol/04251/opgs/edr/ncam/NLB_774875074EDR_F1080438NCAM00274M_.JPG');
}



video {
  height: auto !important;
  width: 100% !important;
 /* margin-left: 1em;
  margin-right: 1em;
  border-radius: .3em; */
  display: block;
  background: repeating-linear-gradient(
			to left,
			transparent,
			transparent 54px,
			black 55px,
			black 55px
		),
		repeating-linear-gradient(
			to bottom,
			transparent,
			transparent 54px,
			grey 55px,
			grey 55px
		),
		linear-gradient(45deg, grey, black);
	
	background-attachment:fixed;
  transition: 3s cubic-bezier(0.1, 0.2, 0.3, 0.4);
  /*  transition: 4s cubic-bezier(.25,.1,.2,3); */
}

embed {
  
  width: 100%;
min-height: max-content;
}

iframe {
  margin:0px;
  width: 100%;
}



.twoPanelSpread {
  margin: 0px;
  padding: 0px;
  background: url(https://raw.githubusercontent.com/ThakaRashard/bubblegumpop/gh-pages/img/810MATRiX.webp)
    center repeat;
}

.row {
  border-radius: 0px;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  width: 100%;
}

.panelColumn {
  display: flex;
  flex-direction: column;
  flex-basis: 100%;
  flex: 1;
  overflow: hidden;
}

.leftColumn {
  /* background-color: #2470FF; */
  width: 100%;
}

.leftColumn img {
  flex-shrink: 0;
  min-width: 100%;
  min-height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.rightColumn {
  /* background-color: #c9ff23; */
}
.rightColumn img {
  flex-shrink: 0;
  min-width: 100%;
  min-height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}




.top-container {

  padding: 0px;
  align-content: center;
 	max-width: 900px; 
	padding: 0px;
	margin-right: auto;
	margin-left: auto; 	
	/* opera does not like 'margin:20px auto' */
	/* background: #666; */
  width: 50%; /* ie5win fudge begins */
	text-align:left; 
}

/* 3_TO_6 panel spread ##LAUREN_IS_MY_WIFE_AS_WELL_as_LAURA */

/* FLEX_BOX_FOR_3_IMAGES */
.greenlineflex-container {

  display: flex;
   align-items: stretch; 
   flex-flow: row wrap;  
  flex-direction: row; 
  justify-content: center;
  align-content: stretch;
  height: auto;
width:100%;
  gap: 5px;

}

.greenlineflex-container > div{
 
  border: 1px solid #c9ff23;
  border-radius: 1px;
  padding: 8px;
}


:root {
  --magnifier: 8;
  --gap: 0vmax;
  --transition: 0.5s;
}

.pinupGallery {
  display: block;
  width: 100%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  gap: 0px;
  object-fit: contain;
}
.expandingGallery {
  width: 100%;
  height: 25vh;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--gap);
}

.expandingGallery > img {
  --brightness: 0.75;
  --grayscale: 1;
  transition: flex var(--transition), filter var(--transition);
  height: 100%;
  object-fit: cover;
  overflow: hidden;
  flex: 1;
}

.expandingGallery > img:hover {
  flex: var(--magnifier);
}


.twitterbox {
  display:flex;
  flex-flow: row wrap;
  max-width: 1100px;
} 


.tweet {

  flex: 1 1 400px;

}


/* i like the formatting here
img[alt="whiteslavery"] { max-width: 30%; float:left;}
img[alt="whiteslavery40"] { max-width: 40%; transform: rotate(45deg);}
*/





@keyframes slideInFromRight {
  0% {
      transform: translateX(100%);
  }
  100% {
      transform: translateX(0);
  }
}
@keyframes slideInFromLeft {
  0% {
      transform: translateX(-100%);
  }
  100% {
      transform: translateX(0);
  }
}

@keyframes blur {
  0% {
      filter: blur(1.5rem);
  }
  100% {
      filter: blur(0rem);
  }
}

@keyframes flip {
  0% {
      filter: blur(1.5rem);
    transform: rotateZ(90deg);
  }
  100% {
      filter: blur(0rem);
    transform: rotateZ(0deg);
  }
}
@keyframes saturate {
  0% {

    filter: saturate(7);
  }
  100% {

    filter: saturate(3);
  }
}

@keyframes scale {
  0% {

    transform: scale( 2, 2);
  }
  100% {

    transform: scale(4, 1);
    
  }
}

@keyframes rotate {
  0% {

    transform: rotate(300.142rad);
  }
  100% {

    transform: rotate(0rad);
    
  }
}












.swatch {

  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: wrap;
  width: 100%;
 position:relative;
  opacity: 1;
  max-width: max-content;
}


.swatch div {

flex: 1 1 auto;
padding: 10px;

}






.swatch div:nth-child(1) {
background: #352EF2;
border-radius:0px
}
.swatch div:nth-child(2) {
background: #446FF2;
border-radius:0px
}

.swatch div:nth-child(3) {
background: #2E97F2;
border-radius:0px
}

.swatch div:nth-child(4) {
background: #3DF28B;
border-radius:0px
}
.swatch div:nth-child(5) {
background: #29F247;
border-radius:0px
}
.swatch div:nth-child(6){ background: #CE0058; }
.swatch div:nth-child(7){ background: #E10098; }
.swatch div:nth-child(8){ background: #BB29BB; }
.swatch div:nth-child(9){ background: #440099; }
.swatch div:nth-child(10){ background: #10069F; }
.swatch div:nth-child(11){ background: #1489; }
.swatch div:nth-child(12){ background: #0085CA; }
.swatch div:nth-child(13){ background: #00AB84; }
.swatch div:nth-child(14){ background: #2D2926; }
.swatch div:nth-child(15){ background: #F2F0A1; }
.swatch div:nth-child(16){ background: #FCAEBB; }
.swatch div:nth-child(17){ background: #F1B2DC; }
.swatch div:nth-child(18){ background: #BF9BDE; }
.swatch div:nth-child(19){ background: #74D1EA; }
.swatch div:nth-child(20){ background: #9DE7D7; }
.swatch div:nth-child(21){ background: #9E978E; }
.swatch div:nth-child(22){ background: #009ACE; }
.swatch div:nth-child(23){ background: #44D62C; }
.swatch div:nth-child(24){ background: #FFE900; }
.swatch div:nth-child(25){ background: #FFAA4D; }
.swatch div:nth-child(26){ background: #FF7276; }
.swatch div:nth-child(27){ background: #FF3EB5; }
.swatch div:nth-child(28){ background: #EA27C2; }
.swatch div:nth-child(29){ background: #84754E; }
.swatch div:nth-child(30){ background: #85714D; }
.swatch div:nth-child(31){ background: #866D4B; }
.swatch div:nth-child(32){ background: #8B6F4E; }
.swatch div:nth-child(33){ background: #87674F; }
.swatch div:nth-child(34){ background: #8B634B; }
.swatch div:nth-child(35){ background: #8A8D8F; }
.swatch div:nth-child(36){ background: #FFD900; }
.swatch div:nth-child(37){ background: #FF5E00; }
.swatch div:nth-child(38){ background: #F93822; }
.swatch div:nth-child(39){ background: #CE0056; }
.swatch div:nth-child(40){ background: #D62598; }
.swatch div:nth-child(41){ background: #4E008E; }
.swatch div:nth-child(42){ background: #00239C; }
.swatch div:nth-child(43){ background: #0084CA; }
.swatch div:nth-child(44){ background: #00B08B; }
.swatch div:nth-child(45){ background: #222223; }
.swatch div:nth-child(46){ background: #F6EB61; }
.swatch div:nth-child(47){ background: #F7EA48; }
.swatch div:nth-child(48){ background: #FCE300; }
.swatch div:nth-child(49){ background: #C5A900; }
.swatch div:nth-child(50){ background: #AF9800; }
.swatch div:nth-child(51){ background: #897A27; }
.swatch div:nth-child(52){ background: #F5E1A4; }
.swatch div:nth-child(53){ background: #ECD898; }
.swatch div:nth-child(54){ background: #EED484; }
.swatch div:nth-child(55){ background: #F4DA40; }
.swatch div:nth-child(56){ background: #F2CD00; }
.swatch div:nth-child(57){ background: #F1C400; }
.swatch div:nth-child(58){ background: #CBA052; }
.swatch div:nth-child(59){ background: #F9E547; }
.swatch div:nth-child(60){ background: #FBE122; }
.swatch div:nth-child(61){ background: #FEDB00; }
.swatch div:nth-child(62){ background: #FFD100; }
.swatch div:nth-child(63){ background: #DAAA00; }
.swatch div:nth-child(64){ background: #AA8A00; }
.swatch div:nth-child(65){ background: #9C8412; }
.swatch div:nth-child(66){ background: #FAE053; }
.swatch div:nth-child(67){ background: #FBDD40; }
.swatch div:nth-child(68){ background: #FDDA24; }
.swatch div:nth-child(69){ background: #FFCD00; }
.swatch div:nth-child(70){ background: #C99700; }
.swatch div:nth-child(71){ background: #AC8400; }
.swatch div:nth-child(72){ background: #897322; }
.swatch div:nth-child(73){ background: #F3DD6D; }
.swatch div:nth-child(74){ background: #F3D54E; }
.swatch div:nth-child(75){ background: #F3D03E; }
.swatch div:nth-child(76){ background: #F2A900; }
.swatch div:nth-child(77){ background: #CC8A00; }
.swatch div:nth-child(78){ background: #A07400; }
.swatch div:nth-child(79){ background: #6C571B; }
.swatch div:nth-child(80){ background: #F8E08E; }
.swatch div:nth-child(81){ background: #FBD872; }
.swatch div:nth-child(82){ background: #FFC845; }
.swatch div:nth-child(83){ background: #FFB81C; }
.swatch div:nth-child(84){ background: #C69214; }
.swatch div:nth-child(85){ background: #AD841F; }
.swatch div:nth-child(86){ background: #886B25; }
.swatch div:nth-child(87){ background: #FBDB65; }
.swatch div:nth-child(88){ background: #FDD757; }
.swatch div:nth-child(89){ background: #FED141; }
.swatch div:nth-child(90){ background: #FFC72C; }
.swatch div:nth-child(91){ background: #EAAA00; }
.swatch div:nth-child(92){ background: #B58500; }
.swatch div:nth-child(93){ background: #9A7611; }
.swatch div:nth-child(94){ background: #FFC600; }
.swatch div:nth-child(95){ background: #FFB500; }
.swatch div:nth-child(96){ background: #D19000; }
.swatch div:nth-child(97){ background: #B47E00; }
.swatch div:nth-child(98){ background: #73531D; }
.swatch div:nth-child(99){ background: #5A4522; }
.swatch div:nth-child(100){ background: #4B3D2A; }
.swatch div:nth-child(101){ background: #D29F13; }
.swatch div:nth-child(102){ background: #B78B20; }
.swatch div:nth-child(103){ background: #9F7D23; }
.swatch div:nth-child(104){ background: #967126; }
.swatch div:nth-child(105){ background: #8F6A2A; }
.swatch div:nth-child(106){ background: #7D622E; }
.swatch div:nth-child(107){ background: #6C5D34; }
.swatch div:nth-child(108){ background: #FDD26E; }
.swatch div:nth-child(109){ background: #FFC658; }
.swatch div:nth-child(110){ background: #FFBF3F; }
.swatch div:nth-child(111){ background: #FFA300; }
.swatch div:nth-child(112){ background: #DE7C00; }
.swatch div:nth-child(113){ background: #AF6D04; }
.swatch div:nth-child(114){ background: #74531C; }
.swatch div:nth-child(115){ background: #FDD086; }
.swatch div:nth-child(116){ background: #FFC56E; }
.swatch div:nth-child(117){ background: #FFB549; }
.swatch div:nth-child(118){ background: #FF9E1B; }
.swatch div:nth-child(119){ background: #D57800; }
.swatch div:nth-child(120){ background: #996017; }
.swatch div:nth-child(121){ background: #6E4C1E; }
.swatch div:nth-child(122){ background: #F2C75C; }
.swatch div:nth-child(123){ background: #F1BE48; }
.swatch div:nth-child(124){ background: #F1B434; }
.swatch div:nth-child(125){ background: #ED8B00; }
.swatch div:nth-child(126){ background: #CF7F00; }
.swatch div:nth-child(127){ background: #A76D11; }
.swatch div:nth-child(128){ background: #715C2A; }
.swatch div:nth-child(129){ background: #F6BE00; }
.swatch div:nth-child(130){ background: #F0B323; }
.swatch div:nth-child(131){ background: #FEAD77; }
.swatch div:nth-child(132){ background: #E6A65D; }
.swatch div:nth-child(133){ background: #D38235; }
.swatch div:nth-child(134){ background: #DC8633; }
.swatch div:nth-child(135){ background: #C16C18; }
.swatch div:nth-child(136){ background: #BD9B60; }
.swatch div:nth-child(137){ background: #D69A2D; }
.swatch div:nth-child(138){ background: #DB8A06; }
.swatch div:nth-child(139){ background: #CD7925; }
.swatch div:nth-child(140){ background: #AD6433; }
.swatch div:nth-child(141){ background: #89532F; }
.swatch div:nth-child(142){ background: #775135; }
.swatch div:nth-child(143){ background: #D78825; }
.swatch div:nth-child(144){ background: #D3832B; }
.swatch div:nth-child(145){ background: #C67D30; }
.swatch div:nth-child(146){ background: #B67233; }
.swatch div:nth-child(147){ background: #A7662B; }
.swatch div:nth-child(148){ background: #9E6A38; }
.swatch div:nth-child(149){ background: #835D32; }
.swatch div:nth-child(150){ background: #FCC89B; }
.swatch div:nth-child(151){ background: #FDBE87; }
.swatch div:nth-child(152){ background: #FDAA63; }
.swatch div:nth-child(153){ background: #F68D2E; }
.swatch div:nth-child(154){ background: #EA7600; }
.swatch div:nth-child(155){ background: #D45D00; }
.swatch div:nth-child(156){ background: #BE4D00; }
.swatch div:nth-child(157){ background: #FECB8B; }
.swatch div:nth-child(158){ background: #FFC27B; }
.swatch div:nth-child(159){ background: #FFB25B; }
.swatch div:nth-child(160){ background: #FF8200; }
.swatch div:nth-child(161){ background: #E57200; }
.swatch div:nth-child(162){ background: #BE6A14; }
.swatch div:nth-child(163){ background: #9B5A1A; }
.swatch div:nth-child(164){ background: #EFD19F; }
.swatch div:nth-child(165){ background: #EFBE7D; }
.swatch div:nth-child(166){ background: #ECA154; }
.swatch div:nth-child(167){ background: #E87722; }
.swatch div:nth-child(168){ background: #CB6015; }
.swatch div:nth-child(169){ background: #A1561C; }
.swatch div:nth-child(170){ background: #603D20; }
.swatch div:nth-child(171){ background: #FFAE62; }
.swatch div:nth-child(172){ background: #FF8F1C; }
.swatch div:nth-child(173){ background: #FF6900; }
.swatch div:nth-child(174){ background: #B94700; }
.swatch div:nth-child(175){ background: #94450B; }
.swatch div:nth-child(176){ background: #653819; }
.swatch div:nth-child(177){ background: #FFB990; }
.swatch div:nth-child(178){ background: #FFA06A; }
.swatch div:nth-child(179){ background: #FF7F32; }
.swatch div:nth-child(180){ background: #FF6A13; }
.swatch div:nth-child(181){ background: #D86018; }
.swatch div:nth-child(182){ background: #A65523; }
.swatch div:nth-child(183){ background: #8B4720; }
.swatch div:nth-child(184){ background: #FFBE9F; }
.swatch div:nth-child(185){ background: #FF9D6E; }
.swatch div:nth-child(186){ background: #FF7F41; }
.swatch div:nth-child(187){ background: #FF671F; }
.swatch div:nth-child(188){ background: #E35205; }
.swatch div:nth-child(189){ background: #BE531C; }
.swatch div:nth-child(190){ background: #73381D; }
.swatch div:nth-child(191){ background: #DB864E; }
.swatch div:nth-child(192){ background: #E07E3C; }
.swatch div:nth-child(193){ background: #DC6B2F; }
.swatch div:nth-child(194){ background: #DC582A; }
.swatch div:nth-child(195){ background: #C05131; }
.swatch div:nth-child(196){ background: #864A33; }
.swatch div:nth-child(197){ background: #674736; }
.swatch div:nth-child(198){ background: #FFA38B; }
.swatch div:nth-child(199){ background: #FF8D6D; }
.swatch div:nth-child(200){ background: #FF6A39; }
.swatch div:nth-child(201){ background: #FC4C02; }
.swatch div:nth-child(202){ background: #DC4405; }
.swatch div:nth-child(203){ background: #A9431E; }
.swatch div:nth-child(204){ background: #833921; }
.swatch div:nth-child(205){ background: #FFB3AB; }
.swatch div:nth-child(206){ background: #FF8674; }
.swatch div:nth-child(207){ background: #FF5C39; }
.swatch div:nth-child(208){ background: #FA4616; }
.swatch div:nth-child(209){ background: #CF4520; }
.swatch div:nth-child(210){ background: #963821; }
.swatch div:nth-child(211){ background: #6B3529; }
.swatch div:nth-child(212){ background: #C4622D; }
.swatch div:nth-child(213){ background: #BA5826; }
.swatch div:nth-child(214){ background: #AF5C37; }
.swatch div:nth-child(215){ background: #9E5330; }
.swatch div:nth-child(216){ background: #924C2E; }
.swatch div:nth-child(217){ background: #7B4D35; }
.swatch div:nth-child(218){ background: #5C4738; }
.swatch div:nth-child(219){ background: #D4B59E; }
.swatch div:nth-child(220){ background: #C07D59; }
.swatch div:nth-child(221){ background: #B15533; }
.swatch div:nth-child(222){ background: #9D432C; }
.swatch div:nth-child(223){ background: #7C3A2D; }
.swatch div:nth-child(224){ background: #6B3D2E; }
.swatch div:nth-child(225){ background: #5C3D31; }
.swatch div:nth-child(226){ background: #D14124; }
.swatch div:nth-child(227){ background: #BD472A; }
.swatch div:nth-child(228){ background: #B33D26; }
.swatch div:nth-child(229){ background: #8D3F2B; }
.swatch div:nth-child(230){ background: #83412C; }
.swatch div:nth-child(231){ background: #7B4931; }
.swatch div:nth-child(232){ background: #674230; }
.swatch div:nth-child(233){ background: #E4D5D3; }
.swatch div:nth-child(234){ background: #E1BBB4; }
.swatch div:nth-child(235){ background: #D6938A; }
.swatch div:nth-child(236){ background: #C26E60; }
.swatch div:nth-child(237){ background: #A4493D; }
.swatch div:nth-child(238){ background: #823B34; }
.swatch div:nth-child(239){ background: #683431; }
.swatch div:nth-child(240){ background: #DDBCB0; }
.swatch div:nth-child(241){ background: #CA9A8E; }
.swatch div:nth-child(242){ background: #BC8A7E; }
.swatch div:nth-child(243){ background: #A37F74; }
.swatch div:nth-child(244){ background: #866761; }
.swatch div:nth-child(245){ background: #6B4C4C; }
.swatch div:nth-child(246){ background: #583D3E; }
.swatch div:nth-child(247){ background: #EABEB0; }
.swatch div:nth-child(248){ background: #C09C83; }
.swatch div:nth-child(249){ background: #B46A55; }
.swatch div:nth-child(250){ background: #AB5C57; }
.swatch div:nth-child(251){ background: #A45248; }
.swatch div:nth-child(252){ background: #9A6A4F; }
.swatch div:nth-child(253){ background: #8A391B; }
.swatch div:nth-child(254){ background: #ECC3B2; }
.swatch div:nth-child(255){ background: #ECBAA8; }
.swatch div:nth-child(256){ background: #EAA794; }
.swatch div:nth-child(257){ background: #E8927C; }
.swatch div:nth-child(258){ background: #DA291C; }
.swatch div:nth-child(259){ background: #9A3324; }
.swatch div:nth-child(260){ background: #653024; }
.swatch div:nth-child(261){ background: #FFB1BB; }
.swatch div:nth-child(262){ background: #FF808B; }
.swatch div:nth-child(263){ background: #FF585D; }
.swatch div:nth-child(264){ background: #E03C31; }
.swatch div:nth-child(265){ background: #BE3A34; }
.swatch div:nth-child(266){ background: #81312F; }
.swatch div:nth-child(267){ background: #FFA3B5; }
.swatch div:nth-child(268){ background: #FF8DA1; }
.swatch div:nth-child(269){ background: #F8485E; }
.swatch div:nth-child(270){ background: #EE2737; }
.swatch div:nth-child(271){ background: #D22630; }
.swatch div:nth-child(272){ background: #AF272F; }
.swatch div:nth-child(273){ background: #7C2529; }
.swatch div:nth-child(274){ background: #FCAFC0; }
.swatch div:nth-child(275){ background: #FB637E; }
.swatch div:nth-child(276){ background: #F4364C; }
.swatch div:nth-child(277){ background: #CB333B; }
.swatch div:nth-child(278){ background: #A4343A; }
.swatch div:nth-child(279){ background: #643335; }
.swatch div:nth-child(280){ background: #C66E4E; }
.swatch div:nth-child(281){ background: #C04C36; }
.swatch div:nth-child(282){ background: #B7312C; }
.swatch div:nth-child(283){ background: #AB2328; }
.swatch div:nth-child(284){ background: #93272C; }
.swatch div:nth-child(285){ background: #8A2A2B; }
.swatch div:nth-child(286){ background: #802F2D; }
.swatch div:nth-child(287){ background: #E1523D; }
.swatch div:nth-child(288){ background: #C63527; }
.swatch div:nth-child(289){ background: #A72B2A; }
.swatch div:nth-child(290){ background: #9E2A2B; }
.swatch div:nth-child(291){ background: #6D3332; }
.swatch div:nth-child(292){ background: #633231; }
.swatch div:nth-child(293){ background: #572D2D; }
.swatch div:nth-child(294){ background: #E6BAA8; }
.swatch div:nth-child(295){ background: #E56A54; }
.swatch div:nth-child(296){ background: #E04E39; }
.swatch div:nth-child(297){ background: #CD545B; }
.swatch div:nth-child(298){ background: #B04A5A; }
.swatch div:nth-child(299){ background: #9B2242; }
.swatch div:nth-child(300){ background: #651D32; }
.swatch div:nth-child(301){ background: #FABBCB; }
.swatch div:nth-child(302){ background: #FC9BB3; }
.swatch div:nth-child(303){ background: #F65275; }
.swatch div:nth-child(304){ background: #E4002B; }
.swatch div:nth-child(305){ background: #C8102E; }
.swatch div:nth-child(306){ background: #A6192E; }
.swatch div:nth-child(307){ background: #76232F; }
.swatch div:nth-child(308){ background: #ECC7CD; }
.swatch div:nth-child(309){ background: #E89CAE; }
.swatch div:nth-child(310){ background: #DF4661; }
.swatch div:nth-child(311){ background: #D50032; }
.swatch div:nth-child(312){ background: #BA0C2F; }
.swatch div:nth-child(313){ background: #9D2235; }
.swatch div:nth-child(314){ background: #862633; }
.swatch div:nth-child(315){ background: #F8A3BC; }
.swatch div:nth-child(316){ background: #F67599; }
.swatch div:nth-child(317){ background: #EF426F; }
.swatch div:nth-child(318){ background: #E40046; }
.swatch div:nth-child(319){ background: #BF0D3E; }
.swatch div:nth-child(320){ background: #9B2743; }
.swatch div:nth-child(321){ background: #782F40; }
.swatch div:nth-child(322){ background: #F5B6CD; }
.swatch div:nth-child(323){ background: #F59BBB; }
.swatch div:nth-child(324){ background: #EF4A81; }
.swatch div:nth-child(325){ background: #E0004D; }
.swatch div:nth-child(326){ background: #C5003E; }
.swatch div:nth-child(327){ background: #A6093D; }
.swatch div:nth-child(328){ background: #8A1538; }
.swatch div:nth-child(329){ background: #F5DADF; }
.swatch div:nth-child(330){ background: #F7CED7; }
.swatch div:nth-child(331){ background: #F9B5C4; }
.swatch div:nth-child(332){ background: #F890A5; }
.swatch div:nth-child(333){ background: #EF6079; }
.swatch div:nth-child(334){ background: #E03E52; }
.swatch div:nth-child(335){ background: #CB2C30; }
.swatch div:nth-child(336){ background: #F2D4D7; }
.swatch div:nth-child(337){ background: #F4C3CC; }
.swatch div:nth-child(338){ background: #F2ACB9; }
.swatch div:nth-child(339){ background: #E68699; }
.swatch div:nth-child(340){ background: #D25B73; }
.swatch div:nth-child(341){ background: #B83A4B; }
.swatch div:nth-child(342){ background: #9E2A2F; }
.swatch div:nth-child(343){ background: #ECB3CB; }
.swatch div:nth-child(344){ background: #E782A9; }
.swatch div:nth-child(345){ background: #E0457B; }
.swatch div:nth-child(346){ background: #CE0037; }
.swatch div:nth-child(347){ background: #A50034; }
.swatch div:nth-child(348){ background: #861F41; }
.swatch div:nth-child(349){ background: #6F263D; }
.swatch div:nth-child(350){ background: #F99FC9; }
.swatch div:nth-child(351){ background: #F57EB6; }
.swatch div:nth-child(352){ background: #F04E98; }
.swatch div:nth-child(353){ background: #E31C79; }
.swatch div:nth-child(354){ background: #CE0F69; }
.swatch div:nth-child(355){ background: #AC145A; }
.swatch div:nth-child(356){ background: #7D2248; }
.swatch div:nth-child(357){ background: #F4CDD4; }
.swatch div:nth-child(358){ background: #E06287; }
.swatch div:nth-child(359){ background: #E24585; }
.swatch div:nth-child(360){ background: #B52555; }
.swatch div:nth-child(361){ background: #A4123F; }
.swatch div:nth-child(362){ background: #971B2F; }
.swatch div:nth-child(363){ background: #6A2C3E; }
.swatch div:nth-child(364){ background: #D6C9CA; }
.swatch div:nth-child(365){ background: #C4A4A7; }
.swatch div:nth-child(366){ background: #C16784; }
.swatch div:nth-child(367){ background: #C63663; }
.swatch div:nth-child(368){ background: #BC204B; }
.swatch div:nth-child(369){ background: #912F46; }
.swatch div:nth-child(370){ background: #7E2D40; }
.swatch div:nth-child(371){ background: #EABEDB; }
.swatch div:nth-child(372){ background: #E56DB1; }
.swatch div:nth-child(373){ background: #DA1884; }
.swatch div:nth-child(374){ background: #A50050; }
.swatch div:nth-child(375){ background: #910048; }
.swatch div:nth-child(376){ background: #6C1D45; }
.swatch div:nth-child(377){ background: #936D73; }
.swatch div:nth-child(378){ background: #934054; }
.swatch div:nth-child(379){ background: #8E2C48; }
.swatch div:nth-child(380){ background: #732E4A; }
.swatch div:nth-child(381){ background: #582D40; }
.swatch div:nth-child(382){ background: #502B3A; }
.swatch div:nth-child(383){ background: #EF95CF; }
.swatch div:nth-child(384){ background: #EB6FBD; }
.swatch div:nth-child(385){ background: #DF1995; }
.swatch div:nth-child(386){ background: #D0006F; }
.swatch div:nth-child(387){ background: #AA0061; }
.swatch div:nth-child(388){ background: #890C58; }
.swatch div:nth-child(389){ background: #672146; }
.swatch div:nth-child(390){ background: #F4A6D7; }
.swatch div:nth-child(391){ background: #F277C6; }
.swatch div:nth-child(392){ background: #E93CAC; }
.swatch div:nth-child(393){ background: #C6007E; }
.swatch div:nth-child(394){ background: #A20067; }
.swatch div:nth-child(395){ background: #840B55; }
.swatch div:nth-child(396){ background: #EAD3E2; }
.swatch div:nth-child(397){ background: #E6BCD8; }
.swatch div:nth-child(398){ background: #DFA0C9; }
.swatch div:nth-child(399){ background: #D986BA; }
.swatch div:nth-child(400){ background: #C6579A; }
.swatch div:nth-child(401){ background: #AE2573; }
.swatch div:nth-child(402){ background: #960051; }
.swatch div:nth-child(403){ background: #E5CEDB; }
.swatch div:nth-child(404){ background: #E3C8D8; }
.swatch div:nth-child(405){ background: #DEBED2; }
.swatch div:nth-child(406){ background: #C996B6; }
.swatch div:nth-child(407){ background: #B06C96; }
.swatch div:nth-child(408){ background: #994878; }
.swatch div:nth-child(409){ background: #7C2855; }
.swatch div:nth-child(410){ background: #E4C6D4; }
.swatch div:nth-child(411){ background: #DCB6C9; }
.swatch div:nth-child(412){ background: #D0A1BA; }
.swatch div:nth-child(413){ background: #BE84A3; }
.swatch div:nth-child(414){ background: #A76389; }
.swatch div:nth-child(415){ background: #893B67; }
.swatch div:nth-child(416){ background: #612141; }
.swatch div:nth-child(417){ background: #EBBECB; }
.swatch div:nth-child(418){ background: #E8B3C3; }
.swatch div:nth-child(419){ background: #E4A9BB; }
.swatch div:nth-child(420){ background: #D592AA; }
.swatch div:nth-child(421){ background: #84344E; }
.swatch div:nth-child(422){ background: #6F2C3F; }
.swatch div:nth-child(423){ background: #572932; }
.swatch div:nth-child(424){ background: #E2BCCB; }
.swatch div:nth-child(425){ background: #DCA9BF; }
.swatch div:nth-child(426){ background: #C9809E; }
.swatch div:nth-child(427){ background: #B55C80; }
.swatch div:nth-child(428){ background: #A73A64; }
.swatch div:nth-child(429){ background: #9B3259; }
.swatch div:nth-child(430){ background: #872651; }
.swatch div:nth-child(431){ background: #E9CDD0; }
.swatch div:nth-child(432){ background: #E4BEC3; }
.swatch div:nth-child(433){ background: #D7A3AB; }
.swatch div:nth-child(434){ background: #C48490; }
.swatch div:nth-child(435){ background: #B46B7A; }
.swatch div:nth-child(436){ background: #984856; }
.swatch div:nth-child(437){ background: #893C47; }
.swatch div:nth-child(438){ background: #F2C6CF; }
.swatch div:nth-child(439){ background: #F1BDC8; }
.swatch div:nth-child(440){ background: #E9A2B2; }
.swatch div:nth-child(441){ background: #DC8699; }
.swatch div:nth-child(442){ background: #8F3237; }
.swatch div:nth-child(443){ background: #7F3035; }
.swatch div:nth-child(444){ background: #5D2A2C; }
.swatch div:nth-child(445){ background: #E9C4C7; }
.swatch div:nth-child(446){ background: #E5BAC1; }
.swatch div:nth-child(447){ background: #DAA5AD; }
.swatch div:nth-child(448){ background: #C6858F; }
.swatch div:nth-child(449){ background: #7A3E3A; }
.swatch div:nth-child(450){ background: #6A3735; }
.swatch div:nth-child(451){ background: #512F2E; }
.swatch div:nth-child(452){ background: #DFC2C3; }
.swatch div:nth-child(453){ background: #DBB7BB; }
.swatch div:nth-child(454){ background: #CCA1A6; }
.swatch div:nth-child(455){ background: #B07C83; }
.swatch div:nth-child(456){ background: #9C6169; }
.swatch div:nth-child(457){ background: #874B52; }
.swatch div:nth-child(458){ background: #3F2021; }
.swatch div:nth-child(459){ background: #F1A7DC; }
.swatch div:nth-child(460){ background: #EC86D0; }
.swatch div:nth-child(461){ background: #E45DBF; }
.swatch div:nth-child(462){ background: #DB3EB1; }
.swatch div:nth-child(463){ background: #C5299B; }
.swatch div:nth-child(464){ background: #AF1685; }
.swatch div:nth-child(465){ background: #80225F; }
.swatch div:nth-child(466){ background: #EFBAE1; }
.swatch div:nth-child(467){ background: #E277CD; }
.swatch div:nth-child(468){ background: #D539B5; }
.swatch div:nth-child(469){ background: #C800A1; }
.swatch div:nth-child(470){ background: #B0008E; }
.swatch div:nth-child(471){ background: #9E007E; }
.swatch div:nth-child(472){ background: #830065; }
.swatch div:nth-child(473){ background: #EAB8E4; }
.swatch div:nth-child(474){ background: #E59BDC; }
.swatch div:nth-child(475){ background: #DD7FD3; }
.swatch div:nth-child(476){ background: #C724B1; }
.swatch div:nth-child(477){ background: #BB16A3; }
.swatch div:nth-child(478){ background: #A51890; }
.swatch div:nth-child(479){ background: #80276C; }
.swatch div:nth-child(480){ background: #A56E87; }
.swatch div:nth-child(481){ background: #A83D72; }
.swatch div:nth-child(482){ background: #8A1B61; }
.swatch div:nth-child(483){ background: #722257; }
.swatch div:nth-child(484){ background: #6A2A5B; }
.swatch div:nth-child(485){ background: #5E2751; }
.swatch div:nth-child(486){ background: #E7BAE4; }
.swatch div:nth-child(487){ background: #DD9CDF; }
.swatch div:nth-child(488){ background: #C964CF; }
.swatch div:nth-child(489){ background: #AD1AAC; }
.swatch div:nth-child(490){ background: #981D97; }
.swatch div:nth-child(491){ background: #72246C; }
.swatch div:nth-child(492){ background: #EBC6DF; }
.swatch div:nth-child(493){ background: #E6BEDD; }
.swatch div:nth-child(494){ background: #E2ACD7; }
.swatch div:nth-child(495){ background: #D48BC8; }
.swatch div:nth-child(496){ background: #93328E; }
.swatch div:nth-child(497){ background: #833177; }
.swatch div:nth-child(498){ background: #612C51; }
.swatch div:nth-child(499){ background: #EEDAEA; }
.swatch div:nth-child(500){ background: #CCAED0; }
.swatch div:nth-child(501){ background: #D59ED7; }
.swatch div:nth-child(502){ background: #B288B9; }
.swatch div:nth-child(503){ background: #A277A6; }
.swatch div:nth-child(504){ background: #9F5CC0; }
.swatch div:nth-child(505){ background: #963CBD; }
.swatch div:nth-child(506){ background: #D7A9E3; }
.swatch div:nth-child(507){ background: #C98BDB; }
.swatch div:nth-child(508){ background: #AC4FC6; }
.swatch div:nth-child(509){ background: #9B26B6; }
.swatch div:nth-child(510){ background: #87189D; }
.swatch div:nth-child(511){ background: #772583; }
.swatch div:nth-child(512){ background: #653165; }
.swatch div:nth-child(513){ background: #948794; }
.swatch div:nth-child(514){ background: #A2789C; }
.swatch div:nth-child(515){ background: #A15A95; }
.swatch div:nth-child(516){ background: #8E3A80; }
.swatch div:nth-child(517){ background: #6E2B62; }
.swatch div:nth-child(518){ background: #6A3460; }
.swatch div:nth-child(519){ background: #5D3754; }
.swatch div:nth-child(520){ background: #D5C2D8; }
.swatch div:nth-child(521){ background: #C9B1D0; }
.swatch div:nth-child(522){ background: #BA9CC5; }
.swatch div:nth-child(523){ background: #A57FB2; }
.swatch div:nth-child(524){ background: #642F6C; }
.swatch div:nth-child(525){ background: #59315F; }
.swatch div:nth-child(526){ background: #4B3048; }
.swatch div:nth-child(527){ background: #DBCDD3; }
.swatch div:nth-child(528){ background: #D0BEC7; }
.swatch div:nth-child(529){ background: #C6B0BC; }
.swatch div:nth-child(530){ background: #AF95A6; }
.swatch div:nth-child(531){ background: #86647A; }
.swatch div:nth-child(532){ background: #66435A; }
.swatch div:nth-child(533){ background: #4A3041; }
.swatch div:nth-child(534){ background: #D8C8D1; }
.swatch div:nth-child(535){ background: #D3C0CD; }
.swatch div:nth-child(536){ background: #BFA5B8; }
.swatch div:nth-child(537){ background: #9B7793; }
.swatch div:nth-child(538){ background: #7E5475; }
.swatch div:nth-child(539){ background: #693C5E; }
.swatch div:nth-child(540){ background: #512A44; }
.swatch div:nth-child(541){ background: #DFC8E7; }
.swatch div:nth-child(542){ background: #D7B9E4; }
.swatch div:nth-child(543){ background: #CAA2DD; }
.swatch div:nth-child(544){ background: #B580D1; }
.swatch div:nth-child(545){ background: #8031A7; }
.swatch div:nth-child(546){ background: #702F8A; }
.swatch div:nth-child(547){ background: #572C5F; }
.swatch div:nth-child(548){ background: #D6BFDD; }
.swatch div:nth-child(549){ background: #C6A1CF; }
.swatch div:nth-child(550){ background: #8C4799; }
.swatch div:nth-child(551){ background: #6D2077; }
.swatch div:nth-child(552){ background: #642667; }
.swatch div:nth-child(553){ background: #5D285F; }
.swatch div:nth-child(554){ background: #51284F; }
.swatch div:nth-child(555){ background: #CBA3D8; }
.swatch div:nth-child(556){ background: #B884CB; }
.swatch div:nth-child(557){ background: #A05EB5; }
.swatch div:nth-child(558){ background: #84329B; }
.swatch div:nth-child(559){ background: #702082; }
.swatch div:nth-child(560){ background: #5F2167; }
.swatch div:nth-child(561){ background: #9991A4; }
.swatch div:nth-child(562){ background: #8D6E97; }
.swatch div:nth-child(563){ background: #7A4183; }
.swatch div:nth-child(564){ background: #6B3077; }
.swatch div:nth-child(565){ background: #653279; }
.swatch div:nth-child(566){ background: #5E366E; }
.swatch div:nth-child(567){ background: #5C4E63; }
.swatch div:nth-child(568){ background: #C1A0DA; }
.swatch div:nth-child(569){ background: #A77BCA; }
.swatch div:nth-child(570){ background: #8246AF; }
.swatch div:nth-child(571){ background: #5C068C; }
.swatch div:nth-child(572){ background: #500778; }
.swatch div:nth-child(573){ background: #470A68; }
.swatch div:nth-child(574){ background: #3C1053; }
.swatch div:nth-child(575){ background: #D7C6E6; }
.swatch div:nth-child(576){ background: #C1A7E2; }
.swatch div:nth-child(577){ background: #9063CD; }
.swatch div:nth-child(578){ background: #753BBD; }
.swatch div:nth-child(579){ background: #5F259F; }
.swatch div:nth-child(580){ background: #582C83; }
.swatch div:nth-child(581){ background: #512D6D; }
.swatch div:nth-child(582){ background: #C5B4E3; }
.swatch div:nth-child(583){ background: #AD96DC; }
.swatch div:nth-child(584){ background: #9678D3; }
.swatch div:nth-child(585){ background: #7D55C7; }
.swatch div:nth-child(586){ background: #330072; }
.swatch div:nth-child(587){ background: #2E1A47; }
.swatch div:nth-child(588){ background: #B4B5DF; }
.swatch div:nth-child(589){ background: #9595D2; }
.swatch div:nth-child(590){ background: #7474C1; }
.swatch div:nth-child(591){ background: #24135F; }
.swatch div:nth-child(592){ background: #211551; }
.swatch div:nth-child(593){ background: #201747; }
.swatch div:nth-child(594){ background: #221C35; }
.swatch div:nth-child(595){ background: #A7A4E0; }
.swatch div:nth-child(596){ background: #8B84D7; }
.swatch div:nth-child(597){ background: #685BC7; }
.swatch div:nth-child(598){ background: #2E008B; }
.swatch div:nth-child(599){ background: #280071; }
.swatch div:nth-child(600){ background: #201547; }
.swatch div:nth-child(601){ background: #6E7CA0; }
.swatch div:nth-child(602){ background: #686E9F; }
.swatch div:nth-child(603){ background: #615E9B; }
.swatch div:nth-child(604){ background: #565294; }
.swatch div:nth-child(605){ background: #514689; }
.swatch div:nth-child(606){ background: #4C4184; }
.swatch div:nth-child(607){ background: #535486; }
.swatch div:nth-child(608){ background: #DDDAE8; }
.swatch div:nth-child(609){ background: #B6B8DC; }
.swatch div:nth-child(610){ background: #A7A2C3; }
.swatch div:nth-child(611){ background: #8986CA; }
.swatch div:nth-child(612){ background: #5D4777; }
.swatch div:nth-child(613){ background: #4B384C; }
.swatch div:nth-child(614){ background: #41273B; }
.swatch div:nth-child(615){ background: #878CB4; }
.swatch div:nth-child(616){ background: #7C7FAB; }
.swatch div:nth-child(617){ background: #7566A0; }
.swatch div:nth-child(618){ background: #6F5091; }
.swatch div:nth-child(619){ background: #68478D; }
.swatch div:nth-child(620){ background: #563D82; }
.swatch div:nth-child(621){ background: #523178; }
.swatch div:nth-child(622){ background: #E5E1E6; }
.swatch div:nth-child(623){ background: #E0DBE3; }
.swatch div:nth-child(624){ background: #C6BCD0; }
.swatch div:nth-child(625){ background: #A192B2; }
.swatch div:nth-child(626){ background: #7C6992; }
.swatch div:nth-child(627){ background: #614B79; }
.swatch div:nth-child(628){ background: #3F2A56; }
.swatch div:nth-child(629){ background: #D8D7DF; }
.swatch div:nth-child(630){ background: #C6C4D2; }
.swatch div:nth-child(631){ background: #B3B0C4; }
.swatch div:nth-child(632){ background: #8D89A5; }
.swatch div:nth-child(633){ background: #595478; }
.swatch div:nth-child(634){ background: #403A60; }
.swatch div:nth-child(635){ background: #1E1A34; }
.swatch div:nth-child(636){ background: #C5CFDA; }
.swatch div:nth-child(637){ background: #BBC7D6; }
.swatch div:nth-child(638){ background: #A2B2C8; }
.swatch div:nth-child(639){ background: #8E9FBC; }
.swatch div:nth-child(640){ background: #1B365D; }
.swatch div:nth-child(641){ background: #1F2A44; }
.swatch div:nth-child(642){ background: #1C1F2A; }
.swatch div:nth-child(643){ background: #D9E1E2; }
.swatch div:nth-child(644){ background: #A4BCC2; }
.swatch div:nth-child(645){ background: #98A4AE; }
.swatch div:nth-child(646){ background: #768692; }
.swatch div:nth-child(647){ background: #425563; }
.swatch div:nth-child(648){ background: #253746; }
.swatch div:nth-child(649){ background: #B9D3DC; }
.swatch div:nth-child(650){ background: #A3C7D2; }
.swatch div:nth-child(651){ background: #8DB9CA; }
.swatch div:nth-child(652){ background: #6BA4B8; }
.swatch div:nth-child(653){ background: #003D4C; }
.swatch div:nth-child(654){ background: #00313C; }
.swatch div:nth-child(655){ background: #072B31; }
.swatch div:nth-child(656){ background: #BFCED6; }
.swatch div:nth-child(657){ background: #B7C9D3; }
.swatch div:nth-child(658){ background: #A6BBC8; }
.swatch div:nth-child(659){ background: #7A99AC; }
.swatch div:nth-child(660){ background: #5B7F95; }
.swatch div:nth-child(661){ background: #4F758B; }
.swatch div:nth-child(662){ background: #081F2C; }
.swatch div:nth-child(663){ background: #D1DDE6; }
.swatch div:nth-child(664){ background: #C6D6E3; }
.swatch div:nth-child(665){ background: #9BB8D3; }
.swatch div:nth-child(666){ background: #7DA1C4; }
.swatch div:nth-child(667){ background: #5E8AB4; }
.swatch div:nth-child(668){ background: #236192; }
.swatch div:nth-child(669){ background: #002E5D; }
.swatch div:nth-child(670){ background: #DBE2E9; }
.swatch div:nth-child(671){ background: #CED9E5; }
.swatch div:nth-child(672){ background: #A7BCD6; }
.swatch div:nth-child(673){ background: #7D9BC1; }
.swatch div:nth-child(674){ background: #326295; }
.swatch div:nth-child(675){ background: #003A70; }
.swatch div:nth-child(676){ background: #2554; }
.swatch div:nth-child(677){ background: #DDE5ED; }
.swatch div:nth-child(678){ background: #C8D8EB; }
.swatch div:nth-child(679){ background: #B1C9E8; }
.swatch div:nth-child(680){ background: #7BA4DB; }
.swatch div:nth-child(681){ background: #407EC9; }
.swatch div:nth-child(682){ background: #3594; }
.swatch div:nth-child(683){ background: #001A70; }
.swatch div:nth-child(684){ background: #BDC5DB; }
.swatch div:nth-child(685){ background: #89ABE3; }
.swatch div:nth-child(686){ background: #8094DD; }
.swatch div:nth-child(687){ background: #7BA6DE; }
.swatch div:nth-child(688){ background: #5F8FB4; }
.swatch div:nth-child(689){ background: #3A5DAE; }
.swatch div:nth-child(690){ background: #606EB2; }
.swatch div:nth-child(691){ background: #CBD3EB; }
.swatch div:nth-child(692){ background: #9FAEE5; }
.swatch div:nth-child(693){ background: #485CC7; }
.swatch div:nth-child(694){ background: #1E22AA; }
.swatch div:nth-child(695){ background: #171C8F; }
.swatch div:nth-child(696){ background: #151F6D; }
.swatch div:nth-child(697){ background: #141B4D; }
.swatch div:nth-child(698){ background: #B8CCEA; }
.swatch div:nth-child(699){ background: #5C88DA; }
.swatch div:nth-child(700){ background: #0047BB; }
.swatch div:nth-child(701){ background: #06038D; }
.swatch div:nth-child(702){ background: #1871; }
.swatch div:nth-child(703){ background: whitesmoke; }
.swatch div:nth-child(704){ background: #071D49; }
.swatch div:nth-child(705){ background: #C3D7EE; }
.swatch div:nth-child(706){ background: #A7C6ED; }
.swatch div:nth-child(707){ background: #307FE2; }
.swatch div:nth-child(708){ background: #001A72; }
.swatch div:nth-child(709){ background: #1E4460; }
.swatch div:nth-child(710){ background: #13294B; }
.swatch div:nth-child(711){ background: #ABCAE9; }
.swatch div:nth-child(712){ background: #8BB8E8; }
.swatch div:nth-child(713){ background: #418FDE; }
.swatch div:nth-child(714){ background: cyan; }
.swatch div:nth-child(715){ background: #00205B; }
.swatch div:nth-child(716){ background: #441E43; }
.swatch div:nth-child(717){ background: #92C1E9; }
.swatch div:nth-child(718){ background: #6CACE4; }
.swatch div:nth-child(719){ background: #0072CE; }
.swatch div:nth-child(720){ background: #0033A0; }
.swatch div:nth-child(721){ background: #3087; }
.swatch div:nth-child(722){ background: #002D72; }
.swatch div:nth-child(723){ background: #0C2340; }
.swatch div:nth-child(724){ background: #94A9CB; }
.swatch div:nth-child(725){ background: #6787B7; }
.swatch div:nth-child(726){ background: #426DA9; }
.swatch div:nth-child(727){ background: #385E9D; }
.swatch div:nth-child(728){ background: #2C5697; }
.swatch div:nth-child(729){ background: #1D4F91; }
.swatch div:nth-child(730){ background: #1D428A; }
.swatch div:nth-child(731){ background: #C6DAE7; }
.swatch div:nth-child(732){ background: #BDD6E6; }
.swatch div:nth-child(733){ background: #A4C8E1; }
.swatch div:nth-child(734){ background: #7BAFD4; }
.swatch div:nth-child(735){ background: #003C71; }
.swatch div:nth-child(736){ background: #3057; }
.swatch div:nth-child(737){ background: #00263A; }
.swatch div:nth-child(738){ background: #B9D9EB; }
.swatch div:nth-child(739){ background: #9BCBEB; }
.swatch div:nth-child(740){ background: #69B3E7; }
.swatch div:nth-child(741){ background: #003DA5; }
.swatch div:nth-child(742){ background: #002F6C; }
.swatch div:nth-child(743){ background: #2855; }
.swatch div:nth-child(744){ background: #041C2C; }
.swatch div:nth-child(745){ background: #8DC8E8; }
.swatch div:nth-child(746){ background: #62B5E5; }
.swatch div:nth-child(747){ background: #009CDE; }
.swatch div:nth-child(748){ background: #0057B8; }
.swatch div:nth-child(749){ background: #004C97; }
.swatch div:nth-child(750){ background: #3865; }
.swatch div:nth-child(751){ background: #00263E; }
.swatch div:nth-child(752){ background: #71C5E8; }
.swatch div:nth-child(753){ background: #41B6E6; }
.swatch div:nth-child(754){ background: #00A3E0; }
.swatch div:nth-child(755){ background: #005EB8; }
.swatch div:nth-child(756){ background: #004B87; }
.swatch div:nth-child(757){ background: #003B5C; }
.swatch div:nth-child(758){ background: #002A3A; }
.swatch div:nth-child(759){ background: #4698CB; }
.swatch div:nth-child(760){ background: #298FC2; }
.swatch div:nth-child(761){ background: #0076A8; }
.swatch div:nth-child(762){ background: #6298; }
.swatch div:nth-child(763){ background: #5587; }
.swatch div:nth-child(764){ background: #4976; }
.swatch div:nth-child(765){ background: #01426A; }
.swatch div:nth-child(766){ background: #99D6EA; }
.swatch div:nth-child(767){ background: #5BC2E7; }
.swatch div:nth-child(768){ background: #00A9E0; }
.swatch div:nth-child(769){ background: #0077C8; }
.swatch div:nth-child(770){ background: #00629B; }
.swatch div:nth-child(771){ background: #004F71; }
.swatch div:nth-child(772){ background: #3E4451; }
.swatch div:nth-child(773){ background: #7BA7BC; }
.swatch div:nth-child(774){ background: #6399AE; }
.swatch div:nth-child(775){ background: #4E87A0; }
.swatch div:nth-child(776){ background: #41748D; }
.swatch div:nth-child(777){ background: #34657F; }
.swatch div:nth-child(778){ background: #165C7D; }
.swatch div:nth-child(779){ background: #5776; }
.swatch div:nth-child(780){ background: #BBDDE6; }
.swatch div:nth-child(781){ background: #71B2C9; }
.swatch div:nth-child(782){ background: #4298B5; }
.swatch div:nth-child(783){ background: #0086BF; }
.swatch div:nth-child(784){ background: #007DBA; }
.swatch div:nth-child(785){ background: #00558C; }
.swatch div:nth-child(786){ background: #002B49; }
.swatch div:nth-child(787){ background: #9ADBE8; }
.swatch div:nth-child(788){ background: #59CBE8; }
.swatch div:nth-child(789){ background: #00B5E2; }
.swatch div:nth-child(790){ background: #006BA6; }
.swatch div:nth-child(791){ background: #00587C; }
.swatch div:nth-child(792){ background: #003B49; }
.swatch div:nth-child(793){ background: #A4DBE8; }
.swatch div:nth-child(794){ background: #8BD3E6; }
.swatch div:nth-child(795){ background: #4EC3E0; }
.swatch div:nth-child(796){ background: #00AFD7; }
.swatch div:nth-child(797){ background: #0095C8; }
.swatch div:nth-child(798){ background: #0082BA; }
.swatch div:nth-child(799){ background: #0067A0; }
.swatch div:nth-child(800){ background: #48A9C5; }
.swatch div:nth-child(801){ background: #009CBD; }
.swatch div:nth-child(802){ background: #0085AD; }
.swatch div:nth-child(803){ background: #7096; }
.swatch div:nth-child(804){ background: #006A8E; }
.swatch div:nth-child(805){ background: #00617F; }
.swatch div:nth-child(806){ background: #5670; }
.swatch div:nth-child(807){ background: #B8DDE1; }
.swatch div:nth-child(808){ background: #9BD3DD; }
.swatch div:nth-child(809){ background: #77C5D5; }
.swatch div:nth-child(810){ background: #3EB1C8; }
.swatch div:nth-child(811){ background: #0093B2; }
.swatch div:nth-child(812){ background: #7396; }
.swatch div:nth-child(813){ background: #005F83; }
.swatch div:nth-child(814){ background: #6AD1E3; }
.swatch div:nth-child(815){ background: #05C3DE; }
.swatch div:nth-child(816){ background: #00A9CE; }
.swatch div:nth-child(817){ background: #0092BC; }
.swatch div:nth-child(818){ background: #007FA3; }
.swatch div:nth-child(819){ background: #00677F; }
.swatch div:nth-child(820){ background: #4851; }
.swatch div:nth-child(821){ background: #68D2DF; }
.swatch div:nth-child(822){ background: #00C1D5; }
.swatch div:nth-child(823){ background: #00AEC7; }
.swatch div:nth-child(824){ background: #008EAA; }
.swatch div:nth-child(825){ background: #00778B; }
.swatch div:nth-child(826){ background: #6272; }
.swatch div:nth-child(827){ background: #004F59; }
.swatch div:nth-child(828){ background: #63B1BC; }
.swatch div:nth-child(829){ background: #00A7B5; }
.swatch div:nth-child(830){ background: #0097A9; }
.swatch div:nth-child(831){ background: #00859B; }
.swatch div:nth-child(832){ background: #007D8A; }
.swatch div:nth-child(833){ background: #7680; }
.swatch div:nth-child(834){ background: #6269; }
.swatch div:nth-child(835){ background: #B1E4E3; }
.swatch div:nth-child(836){ background: #88DBDF; }
.swatch div:nth-child(837){ background: #2DCCD3; }
.swatch div:nth-child(838){ background: #009CA6; }
.swatch div:nth-child(839){ background: #008C95; }
.swatch div:nth-child(840){ background: #7377; }
.swatch div:nth-child(841){ background: #005F61; }
.swatch div:nth-child(842){ background: #A0D1CA; }
.swatch div:nth-child(843){ background: #40C1AC; }
.swatch div:nth-child(844){ background: #00B0B9; }
.swatch div:nth-child(845){ background: #00A3AD; }
.swatch div:nth-child(846){ background: #7398; }
.swatch div:nth-child(847){ background: #005F86; }
.swatch div:nth-child(848){ background: #005A70; }
.swatch div:nth-child(849){ background: #7EDDD3; }
.swatch div:nth-child(850){ background: #5CB8B2; }
.swatch div:nth-child(851){ background: #279989; }
.swatch div:nth-child(852){ background: #7681; }
.swatch div:nth-child(853){ background: #487A7B; }
.swatch div:nth-child(854){ background: #0D5257; }
.swatch div:nth-child(855){ background: #244C5A; }
.swatch div:nth-child(856){ background: #B6CFD0; }
.swatch div:nth-child(857){ background: #ABC7CA; }
.swatch div:nth-child(858){ background: #94B7BB; }
.swatch div:nth-child(859){ background: #7FA9AE; }
.swatch div:nth-child(860){ background: #4F868E; }
.swatch div:nth-child(861){ background: #07272D; }
.swatch div:nth-child(862){ background: #00968F; }
.swatch div:nth-child(863){ background: #00857D; }
.swatch div:nth-child(864){ background: #7672; }
.swatch div:nth-child(865){ background: #006D68; }
.swatch div:nth-child(866){ background: #00635B; }
.swatch div:nth-child(867){ background: #005E5D; }
.swatch div:nth-child(868){ background: #5151; }
.swatch div:nth-child(869){ background: #9CDBD9; }
.swatch div:nth-child(870){ background: #64CCC9; }
.swatch div:nth-child(871){ background: #00B2A9; }
.swatch div:nth-child(872){ background: #8675; }
.swatch div:nth-child(873){ background: #7367; }
.swatch div:nth-child(874){ background: #00685E; }
.swatch div:nth-child(875){ background: #00534C; }
.swatch div:nth-child(876){ background: #71DBD4; }
.swatch div:nth-child(877){ background: #2AD2C9; }
.swatch div:nth-child(878){ background: #00BFB3; }
.swatch div:nth-child(879){ background: #00A499; }
.swatch div:nth-child(880){ background: #8578; }
.swatch div:nth-child(881){ background: #00594F; }
.swatch div:nth-child(882){ background: #004C45; }
.swatch div:nth-child(883){ background: #7CE0D3; }
.swatch div:nth-child(884){ background: #2CD5C4; }
.swatch div:nth-child(885){ background: #00C7B1; }
.swatch div:nth-child(886){ background: #00B398; }
.swatch div:nth-child(887){ background: #9681; }
.swatch div:nth-child(888){ background: #7864; }
.swatch div:nth-child(889){ background: #473E42; }
.swatch div:nth-child(890){ background: #6DCDB8; }
.swatch div:nth-child(891){ background: #49C5B1; }
.swatch div:nth-child(892){ background: #00AB8E; }
.swatch div:nth-child(893){ background: #009B77; }
.swatch div:nth-child(894){ background: #8264; }
.swatch div:nth-child(895){ background: #006A52; }
.swatch div:nth-child(896){ background: magenta; }
.swatch div:nth-child(897){ background: #B9DCD2; }
.swatch div:nth-child(898){ background: #A1D6CA; }
.swatch div:nth-child(899){ background: #86C8BC; }
.swatch div:nth-child(900){ background: #6BBBAE; }
.swatch div:nth-child(901){ background: #006F62; }
.swatch div:nth-child(902){ background: #00594C; }
.swatch div:nth-child(903){ background: #1D3C34; }
.swatch div:nth-child(904){ background: #B5E3D8; }
.swatch div:nth-child(905){ background: #A5DFD3; }
.swatch div:nth-child(906){ background: #98DBCE; }
.swatch div:nth-child(907){ background: #6BCABA; }
.swatch div:nth-child(908){ background: #00816D; }
.swatch div:nth-child(909){ background: #006C5B; }
.swatch div:nth-child(910){ background: #173F35; }
.swatch div:nth-child(911){ background: #ADCAB8; }
.swatch div:nth-child(912){ background: #9ABEAA; }
.swatch div:nth-child(913){ background: #85B09A; }
.swatch div:nth-child(914){ background: #6FA287; }
.swatch div:nth-child(915){ background: #28724F; }
.swatch div:nth-child(916){ background: #205C40; }
.swatch div:nth-child(917){ background: #284734; }
.swatch div:nth-child(918){ background: #BFCEC2; }
.swatch div:nth-child(919){ background: #A7BDB1; }
.swatch div:nth-child(920){ background: #92ACA0; }
.swatch div:nth-child(921){ background: #7F9C90; }
.swatch div:nth-child(922){ background: #5C7F71; }
.swatch div:nth-child(923){ background: #43695B; }
.swatch div:nth-child(924){ background: #183028; }
.swatch div:nth-child(925){ background: #BAC5B9; }
.swatch div:nth-child(926){ background: #B0BDB0; }
.swatch div:nth-child(927){ background: #A3B2A4; }
.swatch div:nth-child(928){ background: #94A596; }
.swatch div:nth-child(929){ background: #708573; }
.swatch div:nth-child(930){ background: #5E7461; }
.swatch div:nth-child(931){ background: #22372B; }
.swatch div:nth-child(932){ background: #BCC9C5; }
.swatch div:nth-child(933){ background: #B1C0BC; }
.swatch div:nth-child(934){ background: #9DB0AC; }
.swatch div:nth-child(935){ background: #829995; }
.swatch div:nth-child(936){ background: #5D7975; }
.swatch div:nth-child(937){ background: #3E5D58; }
.swatch div:nth-child(938){ background: #18332F; }
.swatch div:nth-child(939){ background: #D1E0D7; }
.swatch div:nth-child(940){ background: #B7CDC2; }
.swatch div:nth-child(941){ background: #9AB9AD; }
.swatch div:nth-child(942){ background: #789F90; }
.swatch div:nth-child(943){ background: #507F70; }
.swatch div:nth-child(944){ background: #285C4D; }
.swatch div:nth-child(945){ background: #13322B; }
.swatch div:nth-child(946){ background: #A7E6D7; }
.swatch div:nth-child(947){ background: #8CE2D0; }
.swatch div:nth-child(948){ background: #3CDBC0; }
.swatch div:nth-child(949){ background: #9775; }
.swatch div:nth-child(950){ background: #007B5F; }
.swatch div:nth-child(951){ background: #00664F; }
.swatch div:nth-child(952){ background: #8FD6BD; }
.swatch div:nth-child(953){ background: #6ECEB2; }
.swatch div:nth-child(954){ background: #00B388; }
.swatch div:nth-child(955){ background: #00965E; }
.swatch div:nth-child(956){ background: #007A53; }
.swatch div:nth-child(957){ background: #6747; }
.swatch div:nth-child(958){ background: #115740; }
.swatch div:nth-child(959){ background: #50A684; }
.swatch div:nth-child(960){ background: #00966C; }
.swatch div:nth-child(961){ background: #8755; }
.swatch div:nth-child(962){ background: #007B4B; }
.swatch div:nth-child(963){ background: #006F44; }
.swatch div:nth-child(964){ background: #6845; }
.swatch div:nth-child(965){ background: #5844; }
.swatch div:nth-child(966){ background: #7AE1BF; }
.swatch div:nth-child(967){ background: #47D7AC; }
.swatch div:nth-child(968){ background: #00C389; }
.swatch div:nth-child(969){ background: #00AF66; }
.swatch div:nth-child(970){ background: #7749; }
.swatch div:nth-child(971){ background: #6341; }
.swatch div:nth-child(972){ background: #154734; }
.swatch div:nth-child(973){ background: #A0DAB3; }
.swatch div:nth-child(974){ background: #91D6AC; }
.swatch div:nth-child(975){ background: #71CC98; }
.swatch div:nth-child(976){ background: #009A44; }
.swatch div:nth-child(977){ background: #00843D; }
.swatch div:nth-child(978){ background: #046A38; }
.swatch div:nth-child(979){ background: #2C5234; }
.swatch div:nth-child(980){ background: #A2E4B8; }
.swatch div:nth-child(981){ background: #8FE2B0; }
.swatch div:nth-child(982){ background: #80E0A7; }
.swatch div:nth-child(983){ background: #00B140; }
.swatch div:nth-child(984){ background: #9639; }
.swatch div:nth-child(985){ background: #007A33; }
.swatch div:nth-child(986){ background: #215732; }
.swatch div:nth-child(987){ background: #9BE3BF; }
.swatch div:nth-child(988){ background: #26D07C; }
.swatch div:nth-child(989){ background: #00BF6F; }
.swatch div:nth-child(990){ background: #00B74F; }
.swatch div:nth-child(991){ background: #009F4D; }
.swatch div:nth-child(992){ background: #275D38; }
.swatch div:nth-child(993){ background: #00573F; }
.swatch div:nth-child(994){ background: #4B9560; }
.swatch div:nth-child(995){ background: #228848; }
.swatch div:nth-child(996){ background: #007A3E; }
.swatch div:nth-child(997){ background: #7041; }
.swatch div:nth-child(998){ background: #286140; }
.swatch div:nth-child(999){ background: #36573B; }
.swatch div:nth-child(1000){ background: #395542; }
.swatch div:nth-child(1001){ background: #6BA539; }
.swatch div:nth-child(1002){ background: #48A23F; }
.swatch div:nth-child(1003){ background: #319B42; }
.swatch div:nth-child(1004){ background: #3A913F; }
.swatch div:nth-child(1005){ background: #44883E; }
.swatch div:nth-child(1006){ background: #4A773C; }
.swatch div:nth-child(1007){ background: #44693D; }
.swatch div:nth-child(1008){ background: #ADDC91; }
.swatch div:nth-child(1009){ background: #A1D884; }
.swatch div:nth-child(1010){ background: #6CC24A; }
.swatch div:nth-child(1011){ background: #43B02A; }
.swatch div:nth-child(1012){ background: #509E2F; }
.swatch div:nth-child(1013){ background: #4C8C2B; }
.swatch div:nth-child(1014){ background: #4A7729; }
.swatch div:nth-child(1015){ background: #D0DEBB; }
.swatch div:nth-child(1016){ background: #BCE194; }
.swatch div:nth-child(1017){ background: #8EDD65; }
.swatch div:nth-child(1018){ background: #78D64B; }
.swatch div:nth-child(1019){ background: #74AA50; }
.swatch div:nth-child(1020){ background: #719949; }
.swatch div:nth-child(1021){ background: #79863C; }
.swatch div:nth-child(1022){ background: #C2E189; }
.swatch div:nth-child(1023){ background: #B7DD79; }
.swatch div:nth-child(1024){ background: #A4D65E; }
.swatch div:nth-child(1025){ background: #78BE20; }
.swatch div:nth-child(1026){ background: #64A70B; }
.swatch div:nth-child(1027){ background: #658D1B; }
.swatch div:nth-child(1028){ background: #546223; }
.swatch div:nth-child(1029){ background: #D4EB8E; }
.swatch div:nth-child(1030){ background: #CDEA80; }
.swatch div:nth-child(1031){ background: #C5E86C; }
.swatch div:nth-child(1032){ background: #97D700; }
.swatch div:nth-child(1033){ background: #84BD00; }
.swatch div:nth-child(1034){ background: #7A9A01; }
.swatch div:nth-child(1035){ background: #59621D; }
.swatch div:nth-child(1036){ background: #C4D6A4; }
.swatch div:nth-child(1037){ background: #BCD19B; }
.swatch div:nth-child(1038){ background: #B7CE95; }
.swatch div:nth-child(1039){ background: #A9C47F; }
.swatch div:nth-child(1040){ background: #789D4A; }
.swatch div:nth-child(1041){ background: #67823A; }
.swatch div:nth-child(1042){ background: #4E5B31; }
.swatch div:nth-child(1043){ background: #D0D1AB; }
.swatch div:nth-child(1044){ background: #C6C89B; }
.swatch div:nth-child(1045){ background: #BABD8B; }
.swatch div:nth-child(1046){ background: #A2A569; }
.swatch div:nth-child(1047){ background: #8A8D4A; }
.swatch div:nth-child(1048){ background: #6D712E; }
.swatch div:nth-child(1049){ background: #3D441E; }
.swatch div:nth-child(1050){ background: #D2CE9E; }
.swatch div:nth-child(1051){ background: #CBC793; }
.swatch div:nth-child(1052){ background: #C0BB87; }
.swatch div:nth-child(1053){ background: #AFA96E; }
.swatch div:nth-child(1054){ background: #A09958; }
.swatch div:nth-child(1055){ background: #89813D; }
.swatch div:nth-child(1056){ background: #555025; }
.swatch div:nth-child(1057){ background: #C3C6A8; }
.swatch div:nth-child(1058){ background: #B3B995; }
.swatch div:nth-child(1059){ background: #A3AA83; }
.swatch div:nth-child(1060){ background: #899064; }
.swatch div:nth-child(1061){ background: #737B4C; }
.swatch div:nth-child(1062){ background: #5E6738; }
.swatch div:nth-child(1063){ background: #3E4827; }
.swatch div:nth-child(1064){ background: #BFCC80; }
.swatch div:nth-child(1065){ background: #BBC592; }
.swatch div:nth-child(1066){ background: #9CAF88; }
.swatch div:nth-child(1067){ background: #8F993E; }
.swatch div:nth-child(1068){ background: #76881D; }
.swatch div:nth-child(1069){ background: #7A7256; }
.swatch div:nth-child(1070){ background: #5B6236; }
.swatch div:nth-child(1071){ background: #BABC16; }
.swatch div:nth-child(1072){ background: #ABAD23; }
.swatch div:nth-child(1073){ background: #999B30; }
.swatch div:nth-child(1074){ background: #888D30; }
.swatch div:nth-child(1075){ background: #7C8034; }
.swatch div:nth-child(1076){ background: #727337; }
.swatch div:nth-child(1077){ background: #656635; }
.swatch div:nth-child(1078){ background: #E2E868; }
.swatch div:nth-child(1079){ background: #DBE442; }
.swatch div:nth-child(1080){ background: #CEDC00; }
.swatch div:nth-child(1081){ background: #C4D600; }
.swatch div:nth-child(1082){ background: #A8AD00; }
.swatch div:nth-child(1083){ background: #949300; }
.swatch div:nth-child(1084){ background: #787121; }
.swatch div:nth-child(1085){ background: #E9EC6B; }
.swatch div:nth-child(1086){ background: #E3E935; }
.swatch div:nth-child(1087){ background: #E0E721; }
.swatch div:nth-child(1088){ background: #D0DF00; }
.swatch div:nth-child(1089){ background: #B5BD00; }
.swatch div:nth-child(1090){ background: #9A9500; }
.swatch div:nth-child(1091){ background: #827A04; }
.swatch div:nth-child(1092){ background: #E3E48D; }
.swatch div:nth-child(1093){ background: #E0E27C; }
.swatch div:nth-child(1094){ background: #DBDE70; }
.swatch div:nth-child(1095){ background: #D2D755; }
.swatch div:nth-child(1096){ background: #B7BF10; }
.swatch div:nth-child(1097){ background: #8E8C13; }
.swatch div:nth-child(1098){ background: #625D20; }
.swatch div:nth-child(1099){ background: #F0EC74; }
.swatch div:nth-child(1100){ background: #EDE939; }
.swatch div:nth-child(1101){ background: #ECE81A; }
.swatch div:nth-child(1102){ background: #E1E000; }
.swatch div:nth-child(1103){ background: #BFB800; }
.swatch div:nth-child(1104){ background: #ADA400; }
.swatch div:nth-child(1105){ background: #A09200; }
.swatch div:nth-child(1106){ background: #F3EA5D; }
.swatch div:nth-child(1107){ background: #F3E500; }
.swatch div:nth-child(1108){ background: #EFDF00; }
.swatch div:nth-child(1109){ background: #EEDC00; }
.swatch div:nth-child(1110){ background: #BBA600; }
.swatch div:nth-child(1111){ background: #9A8700; }
.swatch div:nth-child(1112){ background: #685C20; }
.swatch div:nth-child(1113){ background: #F1EB9C; }
.swatch div:nth-child(1114){ background: #F0E991; }
.swatch div:nth-child(1115){ background: #F0E87B; }
.swatch div:nth-child(1116){ background: #EDE04B; }
.swatch div:nth-child(1117){ background: #EADA24; }
.swatch div:nth-child(1118){ background: #E1CD00; }
.swatch div:nth-child(1119){ background: #CFB500; }
.swatch div:nth-child(1120){ background: #EBE49A; }
.swatch div:nth-child(1121){ background: #E9E186; }
.swatch div:nth-child(1122){ background: #E6DE77; }
.swatch div:nth-child(1123){ background: #E1D555; }
.swatch div:nth-child(1124){ background: #D7C826; }
.swatch div:nth-child(1125){ background: #C4B000; }
.swatch div:nth-child(1126){ background: #B39B00; }
.swatch div:nth-child(1127){ background: #E9DF97; }
.swatch div:nth-child(1128){ background: #E4D77E; }
.swatch div:nth-child(1129){ background: #DECD63; }
.swatch div:nth-child(1130){ background: #D9C756; }
.swatch div:nth-child(1131){ background: #B89D18; }
.swatch div:nth-child(1132){ background: #A28E2A; }
.swatch div:nth-child(1133){ background: #695B24; }
.swatch div:nth-child(1134){ background: #DCD59A; }
.swatch div:nth-child(1135){ background: #D6CF8D; }
.swatch div:nth-child(1136){ background: #D0C883; }
.swatch div:nth-child(1137){ background: #C0B561; }
.swatch div:nth-child(1138){ background: #AC9F3C; }
.swatch div:nth-child(1139){ background: #9F912A; }
.swatch div:nth-child(1140){ background: #8A7B19; }
.swatch div:nth-child(1141){ background: #CAB64B; }
.swatch div:nth-child(1142){ background: #CFB023; }
.swatch div:nth-child(1143){ background: #C1A01E; }
.swatch div:nth-child(1144){ background: #A08629; }
.swatch div:nth-child(1145){ background: #897630; }
.swatch div:nth-child(1146){ background: #736635; }
.swatch div:nth-child(1147){ background: cyan; }
.swatch div:nth-child(1148){ background: #D4C304; }
.swatch div:nth-child(1149){ background: #C4B200; }
.swatch div:nth-child(1150){ background: #91852C; }
.swatch div:nth-child(1151){ background: #747136; }
.swatch div:nth-child(1152){ background: #5D6439; }
.swatch div:nth-child(1153){ background: #585C3B; }
.swatch div:nth-child(1154){ background: #535435; }
.swatch div:nth-child(1155){ background: #BBB323; }
.swatch div:nth-child(1156){ background: #B4A91F; }
.swatch div:nth-child(1157){ background: #AA9D2E; }
.swatch div:nth-child(1158){ background: #8F7E35; }
.swatch div:nth-child(1159){ background: #716135; }
.swatch div:nth-child(1160){ background: #635939; }
.swatch div:nth-child(1161){ background: #4E4934; }
.swatch div:nth-child(1162){ background: #D5CB9F; }
.swatch div:nth-child(1163){ background: #CFC493; }
.swatch div:nth-child(1164){ background: #C5B783; }
.swatch div:nth-child(1165){ background: #B3A369; }
.swatch div:nth-child(1166){ background: #998542; }
.swatch div:nth-child(1167){ background: #8C7732; }
.swatch div:nth-child(1168){ background: #614F25; }
.swatch div:nth-child(1169){ background: #CAC7A7; }
.swatch div:nth-child(1170){ background: #BFBB98; }
.swatch div:nth-child(1171){ background: #B0AA7E; }
.swatch div:nth-child(1172){ background: #9B945F; }
.swatch div:nth-child(1173){ background: #594A25; }
.swatch div:nth-child(1174){ background: #524727; }
.swatch div:nth-child(1175){ background: #4A412A; }
.swatch div:nth-child(1176){ background: #F1E6B2; }
.swatch div:nth-child(1177){ background: #DFD1A7; }
.swatch div:nth-child(1178){ background: #D9C89E; }
.swatch div:nth-child(1179){ background: #CEB888; }
.swatch div:nth-child(1180){ background: #A89968; }
.swatch div:nth-child(1181){ background: #94795D; }
.swatch div:nth-child(1182){ background: #816040; }
.swatch div:nth-child(1183){ background: #DDCBA4; }
.swatch div:nth-child(1184){ background: #D3BC8D; }
.swatch div:nth-child(1185){ background: #C6AA76; }
.swatch div:nth-child(1186){ background: #B9975B; }
.swatch div:nth-child(1187){ background: #8B5B29; }
.swatch div:nth-child(1188){ background: #744F28; }
.swatch div:nth-child(1189){ background: #5C462B; }
.swatch div:nth-child(1190){ background: #EFDBB2; }
.swatch div:nth-child(1191){ background: #FCD299; }
.swatch div:nth-child(1192){ background: #E1B87F; }
.swatch div:nth-child(1193){ background: #D6A461; }
.swatch div:nth-child(1194){ background: #C6893F; }
.swatch div:nth-child(1195){ background: #B77729; }
.swatch div:nth-child(1196){ background: #A6631B; }
.swatch div:nth-child(1197){ background: #EDC8A3; }
.swatch div:nth-child(1198){ background: #E7B78A; }
.swatch div:nth-child(1199){ background: #DDA46F; }
.swatch div:nth-child(1200){ background: #C88242; }
.swatch div:nth-child(1201){ background: #B36924; }
.swatch div:nth-child(1202){ background: #934D11; }
.swatch div:nth-child(1203){ background: #7D3F16; }
.swatch div:nth-child(1204){ background: #F3CFB3; }
.swatch div:nth-child(1205){ background: #F1C6A7; }
.swatch div:nth-child(1206){ background: #F0BF9B; }
.swatch div:nth-child(1207){ background: #E59E6D; }
.swatch div:nth-child(1208){ background: #B86125; }
.swatch div:nth-child(1209){ background: #A45A2A; }
.swatch div:nth-child(1210){ background: #693F23; }
.swatch div:nth-child(1211){ background: #E0C09F; }
.swatch div:nth-child(1212){ background: #D9B48F; }
.swatch div:nth-child(1213){ background: #CDA077; }
.swatch div:nth-child(1214){ background: #B58150; }
.swatch div:nth-child(1215){ background: #9E652E; }
.swatch div:nth-child(1216){ background: #774212; }
.swatch div:nth-child(1217){ background: #623412; }
.swatch div:nth-child(1218){ background: #E0C6AD; }
.swatch div:nth-child(1219){ background: #DCBFA6; }
.swatch div:nth-child(1220){ background: #CDA788; }
.swatch div:nth-child(1221){ background: #BF9474; }
.swatch div:nth-child(1222){ background: #AD7C59; }
.swatch div:nth-child(1223){ background: #946037; }
.swatch div:nth-child(1224){ background: #4F2C1D; }
.swatch div:nth-child(1225){ background: #E1B7A7; }
.swatch div:nth-child(1226){ background: #D5A286; }
.swatch div:nth-child(1227){ background: #C58B68; }
.swatch div:nth-child(1228){ background: #99552B; }
.swatch div:nth-child(1229){ background: #85431E; }
.swatch div:nth-child(1230){ background: #6D4F47; }
.swatch div:nth-child(1231){ background: #5E4B3C; }
.swatch div:nth-child(1232){ background: #D7C4B7; }
.swatch div:nth-child(1233){ background: #CDB5A7; }
.swatch div:nth-child(1234){ background: #C0A392; }
.swatch div:nth-child(1235){ background: #AE8A79; }
.swatch div:nth-child(1236){ background: #956C58; }
.swatch div:nth-child(1237){ background: #7C4D3A; }
.swatch div:nth-child(1238){ background: #5B3427; }
.swatch div:nth-child(1239){ background: #DBC8B6; }
.swatch div:nth-child(1240){ background: #D3BBA8; }
.swatch div:nth-child(1241){ background: #C6A992; }
.swatch div:nth-child(1242){ background: #AA8066; }
.swatch div:nth-child(1243){ background: #703F2A; }
.swatch div:nth-child(1244){ background: #623B2A; }
.swatch div:nth-child(1245){ background: #4E3629; }
.swatch div:nth-child(1246){ background: #D6D2C4; }
.swatch div:nth-child(1247){ background: #C5B9AC; }
.swatch div:nth-child(1248){ background: #B7A99A; }
.swatch div:nth-child(1249){ background: #A39382; }
.swatch div:nth-child(1250){ background: #7A6855; }
.swatch div:nth-child(1251){ background: #63513D; }
.swatch div:nth-child(1252){ background: #473729; }
.swatch div:nth-child(1253){ background: #D1CCBD; }
.swatch div:nth-child(1254){ background: #B7B09C; }
.swatch div:nth-child(1255){ background: #A69F88; }
.swatch div:nth-child(1256){ background: #A7ACA2; }
.swatch div:nth-child(1257){ background: #949A90; }
.swatch div:nth-child(1258){ background: #8E9089; }
.swatch div:nth-child(1259){ background: #4B4F54; }
.swatch div:nth-child(1260){ background: #D0D3D4; }
.swatch div:nth-child(1261){ background: #C1C6C8; }
.swatch div:nth-child(1262){ background: #A2AAAD; }
.swatch div:nth-child(1263){ background: #7C878E; }
.swatch div:nth-child(1264){ background: #5B6770; }
.swatch div:nth-child(1265){ background: #333F48; }
.swatch div:nth-child(1266){ background: #1D252D; }
.swatch div:nth-child(1267){ background: #C7C9C7; }
.swatch div:nth-child(1268){ background: #B2B4B2; }
.swatch div:nth-child(1269){ background: #9EA2A2; }
.swatch div:nth-child(1270){ background: #898D8D; }
.swatch div:nth-child(1271){ background: #707372; }
.swatch div:nth-child(1272){ background: #54585A; }
.swatch div:nth-child(1273){ background: #25282A; }
.swatch div:nth-child(1274){ background: #BEC6C4; }
.swatch div:nth-child(1275){ background: #A2ACAB; }
.swatch div:nth-child(1276){ background: #919D9D; }
.swatch div:nth-child(1277){ background: #717C7D; }
.swatch div:nth-child(1278){ background: #505759; }
.swatch div:nth-child(1279){ background: #3F4444; }
.swatch div:nth-child(1280){ background: #373A36; }
.swatch div:nth-child(1281){ background: #BABBB1; }
.swatch div:nth-child(1282){ background: #A8A99E; }
.swatch div:nth-child(1283){ background: #919388; }
.swatch div:nth-child(1284){ background: #7E7F74; }
.swatch div:nth-child(1285){ background: #65665C; }
.swatch div:nth-child(1286){ background: #51534A; }
.swatch div:nth-child(1287){ background: #212322; }
.swatch div:nth-child(1288){ background: #C4BFB6; }
.swatch div:nth-child(1289){ background: #AFA9A0; }
.swatch div:nth-child(1290){ background: #9D968D; }
.swatch div:nth-child(1291){ background: #8C857B; }
.swatch div:nth-child(1292){ background: #696158; }
.swatch div:nth-child(1293){ background: #C4BCB7; }
.swatch div:nth-child(1294){ background: #B2A8A2; }
.swatch div:nth-child(1295){ background: #978C87; }
.swatch div:nth-child(1296){ background: #857874; }
.swatch div:nth-child(1297){ background: #746661; }
.swatch div:nth-child(1298){ background: #5E514D; }
.swatch div:nth-child(1299){ background: #382F2D; }
.swatch div:nth-child(1300){ background: #D0C4C5; }
.swatch div:nth-child(1301){ background: #C1B2B6; }
.swatch div:nth-child(1302){ background: #AB989D; }
.swatch div:nth-child(1303){ background: #7B6469; }
.swatch div:nth-child(1304){ background: #584446; }
.swatch div:nth-child(1305){ background: #453536; }
.swatch div:nth-child(1306){ background: #382E2C; }
.swatch div:nth-child(1307){ background: #D7D2CB; }
.swatch div:nth-child(1308){ background: #CBC4BC; }
.swatch div:nth-child(1309){ background: #BFB8AF; }
.swatch div:nth-child(1310){ background: #B6ADA5; }
.swatch div:nth-child(1311){ background: #ACA39A; }
.swatch div:nth-child(1312){ background: #A59C94; }
.swatch div:nth-child(1313){ background: #968C83; }
.swatch div:nth-child(1314){ background: #8C8279; }
.swatch div:nth-child(1315){ background: #83786F; }
.swatch div:nth-child(1316){ background: #6E6259; }
.swatch div:nth-child(1317){ background: #D9D9D6; }
.swatch div:nth-child(1318){ background: #D0D0CE; }
.swatch div:nth-child(1319){ background: #C8C9C7; }
.swatch div:nth-child(1320){ background: #BBBCBC; }
.swatch div:nth-child(1321){ background: #B1B3B3; }
.swatch div:nth-child(1322){ background: #A7A8AA; }
.swatch div:nth-child(1323){ background: #97999B; }
.swatch div:nth-child(1324){ background: #888B8D; }
.swatch div:nth-child(1325){ background: #75787B; }
.swatch div:nth-child(1326){ background: #63666A; }
.swatch div:nth-child(1327){ background: #53565A; }
.swatch div:nth-child(1328){ background: #332F21; }
.swatch div:nth-child(1329){ background: #212721; }
.swatch div:nth-child(1330){ background: #31261D; }
.swatch div:nth-child(1331){ background: #3E2B2E; }
.swatch div:nth-child(1332){ background: #101820; }

.normani {
/*display: grid;
grid-gap: 5px;
grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
display: flex;
flex-wrap: wrap;
width: 100%;
height: 80px;

}
.normani div:nth-child(1) { background: #F2E205;}
.normani div:nth-child(2) { background: #D9CB04;}
.normani div:nth-child(3) { background: #A69B03;}
.normani div:nth-child(4) { background: #595302;}
.normani div:nth-child(5) { background: #262401;}

.normani div {

flex: 0 1 200px;
flex: 1 1 200px;
padding: 0px;

}
.normani {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  height: 80px;
}
.normani div:nth-child(1) {
  background: #f2e205;
}
.normani div:nth-child(2) {
  background: #d9cb04;
}
.normani div:nth-child(3) {
  background: #a69b03;
      animation: 2s ease-out 0s 1 slideInFromLeft;
}
.normani div:nth-child(4) {
  background: #595302;
}
.normani div:nth-child(5) {
  background: #262401;
}

.normani div {
  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;
}

.gullies {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  height: 2em;
  
}
.gullies div:nth-child(1) {
  background: #3029f2;
    animation: .2s ease-out 0s 1 slideInFromLeft;
  animation: .5s ease-in .5s 1 blur;
  
}
.gullies div:nth-child(2) {
  background: #446ff2;
  animation: .2s ease-in .2s 1 blur;
}
.gullies div:nth-child(3) {
  background: #3098f2;
  animation: .8s ease-out 0s 1 slideInFromLeft;
  
}
.gullies div:nth-child(4) {
  background: #0dd9c4;
  animation: .9s ease-out 0s 1 slideInFromLeft;
  
}
.gullies div:nth-child(5) {
  background: #3df28b;
  
  
}

.gullies div {
  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;

  
}

.oncall {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  height: 5%;
}
.oncall div:nth-child(1) {
  background: #f2a922;
}
.oncall div:nth-child(2) {
  background: #f28b0c;
   
}
.oncall div:nth-child(3) {
  background: #f27405;
}
.oncall div:nth-child(4) {
  background: #732e07;
  
}
.oncall div:nth-child(5) {
  background: #bf3706;
}

.oncall div {
  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;
    /* animation: 1s ease-out 0s 1 slideInFromLeft;*/
  
}



.megan {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  height: 3em;

}

.megan div:nth-child(1) { background: #F2059F;}
.megan div:nth-child(2) { background: #F279D2;}
.megan div:nth-child(3) { background: #F2E205;}
.megan div:nth-child(4) { background: #F2CB05;}
.megan div:nth-child(5) { background: #594302;}

.megan div {

  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;

}



.viking {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */

  display: flex;
  flex-wrap: wrap;
  width: 100%;
  height: 3em;

}
.viking div:nth-child(1) { background: #F2F2F2; }
.viking div:nth-child(2) { background: #73463C;}
.viking div:nth-child(3) { background: #8C564A;;}
.viking div:nth-child(4) { background: #260101;}
.viking div:nth-child(5) { background: #0D0000;}

.viking div {

  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;
  

}


.vikingbright {
  /*display: grid;
  grid-gap: 5px;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
  display: flex;
  flex-wrap: nowrap;
  width: 100%;
  height: 30px;

}
.vikingbright div:nth-child(1) { background: #F2F2F2;animation: 1s ease-out 0s 1 flip}
.vikingbright div:nth-child(2) { background: #D9AA71;}
.vikingbright div:nth-child(3) { background: #A65F46;}
.vikingbright div:nth-child(4) { background: #73463C;}
.vikingbright div:nth-child(5) { background: #0D0000;/* animation: 1s ease-out 0s 1 flip ;*/}

.vikingbright div {
/* transform: rotateY(3.142rad);*/
  flex: 0 1 200px;
  flex: 1 1 200px;
  padding: 0px;

}
#a-title {
text-decoration: none;
}


.glass-content {
width: 100%;
margin: 0;
padding: 0;
display: flex;
flex-flow: column nowrap;


}
.glass-item {
 scrollbar-color: #595959 #262626;
scrollbar-width: thin;
flex: 1 0 80vw;
  padding: 1em;

min-height: 50px;
max-height: 40vh;
background-color: rgba(255, 255, 255, 0.7);
text-align: left;
margin: 2vmin;
padding: 2vmin;
background-color: #fce4ec; /* for testing*/
  max-width: 60vw;
background: hsla(0,0%,100%,.25) border-box;
overflow: auto;

box-shadow: 0 0 0 1px hsla(0,0%,100%,.3) inset,
    0 .5em 1em rgba(0, 0, 0, 0.6);
text-shadow: 0 1px 1px hsla(0,0%,100%,.3);
}


.strawberry {
/*display: grid;
grid-gap: 5px;
grid-template-columns: 1fr 1fr 1fr 1fr 1fr; */
display: flex;
flex-wrap: wrap;
width: 100%;
height: 5%;
}
.strawberry div:nth-child(1) {
background: #485922;
}
.strawberry div:nth-child(2) {
background: #A0A676;
}
.strawberry div:nth-child(3) {
background: #A69F7C;
}
.strawberry div:nth-child(4) {
background: #8C8881;
}
.strawberry div:nth-child(5) {
background: #402E24;
}

.strawberry div {
flex: 0 1 200px;
flex: 1 1 200px;
padding: 0px;
}

