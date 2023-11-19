# web-bangkit
codes for web

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
    <head>
    <b:include data='blog' name='all-head-content'/>

    <title>
      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <data:blog.pageTitle/>
        <b:else/>
        <b:if cond='data:blog.pageType != &quot;error_page&quot;'>
          <data:blog.pageName/> | <data:blog.title/>
          <b:else/>
          Page Not Found | <data:blog.title/> 
        </b:if>
      </b:if>
    </title>
    
    <!-- Meta Tags ~ www.Templateclue.com  -->
    <b:if cond='data:blog.pageType == &quot;archive&quot;'>
      <meta content='noindex,noarchive' name='robots'/>
    </b:if>
    <b:if cond='data:blog.metaDescription != &quot;&quot;'>
      <meta expr:content='data:blog.metaDescription' name='description'/>
    </b:if> 
    <meta charset='UTF-8'/>
    <meta content='width=device-width, initial-scale=1, maximum-scale=1' name='viewport'/>
    <!-- /Meta Tags ~ www.Templateclue.com -->

    <link href='//netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css' rel='stylesheet'/>
    <script src='http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js' type='text/javascript'/>

        <!-- Google Fonts -->
        <link href='http://fonts.googleapis.com/css?family=Source+Sans+Pro:300,400,700,900' rel='stylesheet' type='text/css'/>
        <link href='http://fonts.googleapis.com/css?family=Montserrat:400,700' rel='stylesheet' type='text/css'/>
		<link href='https://fonts.googleapis.com/css?family=Raleway' rel='stylesheet' type='text/css'/>
		<link href='https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css' rel='stylesheet'/>

    <b:skin><![CDATA[/*
//////////////////////////////////////////////////////////////
//                                                         //
//  Theme Name : invento                                  //
//  Author : Templateclue								 //
//  Site :www.Templateclue.com                          //
//  License : Creative Commons Attribution License	   //
//  Share and Use This With Proper Credit.            //
//                                                   //
//////////////////////////////////////////////////////
*/
/*****************************************
reset.css
******************************************/
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{border:0;font-size:100%;font:inherit;vertical-align:baseline;margin:0;padding:0}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:none}table{border-collapse:collapse;border-spacing:0}a{text-decoration:none!important;}


*, *:before, *:after {
  box-sizing: border-box;
}

.wrap {
  width: 100%;
  padding: 3.5em 0;
}

.grey {
  background: #ECF0F1;
  padding: 100px 0 150px;
}

a {
  color:#1abc9c;
}

a:hover {
  color: #16a085;
}

a, img, .overlay, input, textarea, .plan-wrap p, .filters .filter {
/*transition*/
  -webkit-transition: all .12s linear;
     -moz-transition: all .12s linear;
       -o-transition: all .12s linear;
          transition: all .12s linear;
}

body {
  font-size: 1em;
  line-height: 1.7em;
  color: #777777;
  font-weight: normal;
}

body, input, textarea {
  font-family: 'Source Sans Pro', Helvetica, Arial, sans-serif;
}

h1,h2,h3,h4,h5,h6, .navigation a, .btn, .filters .filter {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
}
img{
max-width: 100%;
}
h1,h2,h3,h4,h5,h6 {
  position: relative;
  margin: 1em 0 1.4em;
  color: #484f58;
}

h1,h2 {
  text-transform: uppercase;
}

h1 {
  font-size: 3em;
  line-height: 1.2em;
}

h2 {
  font-size: 2.8em;
  line-height: .9em;
}

h3 {
  font-size: 1.8em;
  line-height: .9em;
}

h4,h5,h6 {
  font-size: 1.125em;
  line-height: .5em;
}

blockquote {
  line-height: 1.2em;
  display: inline-block;
  margin: 1.3em 0;
  padding: 2px 20px 0 20px;
  border-left: 3px solid #e8e8e8;
}

blockquote p {
  margin-bottom: 0 !important;
}

.pleft-25 {
  padding-left: 25px;
}

.pright-25 {
  padding-right: 25px;
}

.curveUpColor, .curveDownColor {
  fill: #fff;
  stroke: #fff;
  position: absolute;
  left: 0;
  z-index: 1;
}

.curveUpColor {
  margin-top: -100px;
}

.curveDownColor {
  margin-bottom: -100px;
}

.curveMapUp {
  margin-top: 52px;
}

.curveMapDown {
  margin-top: -238px;
}

.curveGrey {
  fill: #ECF0F1;
  stroke: #ECF0F1;
}
/* *********************************************************
  Buttons 
********************************************************* */

.btn {
  position: relative;
  display: inline-block;
  margin: .8em 0;
  padding: .5em 1.6em;
  color: #fff;
  font-size: .8em;
/*border-radius*/
  -webkit-border-radius: 30px;
     -moz-border-radius: 30px;
          border-radius: 30px;
  background:#1abc9c;
}

.btn:hover, .btn:focus, .btn-current {
  color: #fff;
  background: #16a085;
}

.btn:hover, .social-set a:hover, .team-social a i:hover, .header-carousel .owl-buttons .owl-prev:hover, .header-carousel .owl-buttons .owl-next:hover {
  -webkit-animation: rubberBand .8s 1;
     -moz-animation: rubberBand .8s 1;
       -o-animation: rubberBand .8s 1;
          animation: rubberBand .8s 1;
}

@-webkit-keyframes rubberBand {
  0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }

  30% {
    -webkit-transform: scale3d(1.15, 0.9, 1);
    transform: scale3d(1.15, 0.9, 1);
  }

  40% {
    -webkit-transform: scale3d(0.8, 1.15, 1);
    transform: scale3d(0.8, 1.15, 1);
  }

  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }

  65% {
    -webkit-transform: scale3d(.95, 1.05, 1);
    transform: scale3d(.95, 1.05, 1);
  }

  75% {
    -webkit-transform: scale3d(1.05, .95, 1);
    transform: scale3d(1.05, .95, 1);
  }

  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}

@keyframes rubberBand {
 0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }

  30% {
    -webkit-transform: scale3d(1.15, 0.9, 1);
    transform: scale3d(1.15, 0.9, 1);
  }

  40% {
    -webkit-transform: scale3d(0.8, 1.15, 1);
    transform: scale3d(0.8, 1.15, 1);
  }

  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }

  65% {
    -webkit-transform: scale3d(.95, 1.05, 1);
    transform: scale3d(.95, 1.05, 1);
  }

  75% {
    -webkit-transform: scale3d(1.05, .95, 1);
    transform: scale3d(1.05, .95, 1);
  }

  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}

.rubberBand {
  -webkit-animation-name: rubberBand;
  animation-name: rubberBand;
}

.btn-big {
  font-size: 1.4em;
  padding: .65em 2.2em;
}

.btn-price {
  width: 80%;
  margin: 1.5em 0 1.8em;
  padding: .5em;
  letter-spacing: 2px;
}

.btn-disabled, .btn-disabled:hover, .btn-disabled:focus {
  cursor: default;
  color: #bbb;
  background: #e6e6e6;
}

.btn-ghost {
  margin: 10px;
  color: #fff;
  border: 2px solid #fff;
  background: transparent;
}

.btn-ghost:hover {
  border-color: transparent;
  background-color:#1abc9c;
}

.btn-ghost-dark {
  border-color: #1abc9c;
  color: #1abc9c;
}

/*****************************************
Global Links CSS
******************************************/
.clr{
clear:both;
float:none;
}
*, *:after, *:before {
	-webkit-box-sizing: border-box;
	-moz-box-sizing: border-box;
	box-sizing: border-box;
}

body {
	margin: 0px;
}

[class*='col-'] {
	float: left;
	padding-right: 20px;
}

[class*='col-']:last-of-type {
	/*padding-right: 0px;*/
}

.grid {
	width: 100%;
	max-width: 1140px;
	min-width: 755px;
	margin: 0 auto;
	overflow: hidden;
}

.grid:after {
	content: "";
	display: table;
	clear: both;
}

.grid-pad {
	padding: 20px 0 0px 20px;
}

.grid-pad > [class*='col-']:last-of-type {
	padding-right: 20px;
}

.push-right {
	float: right;
}

/* Content Columns */

.col-1-1 {
	width: 100%;
}
.col-2-3, .col-8-12 {
	width: 66.66%;
}

.col-1-2, .col-6-12 {
	width: 50%;
}

.col-1-3, .col-4-12 {
	width: 33.33%;
}

.col-1-4, .col-3-12 {
	width: 25%;
}

.col-1-5 {
	width: 20%;
}

.col-1-6, .col-2-12 {
	width: 16.667%;
}

.col-1-7 {
	width: 14.28%;
}

.col-1-8 {
	width: 12.5%;
}

.col-1-9 {
	width: 11.1%;
}

.col-1-10 {
	width: 10%;
}

.col-1-11 {
	width: 9.09%;
}

.col-1-12 {
	width: 8.33%
}

/* Layout Columns */

.col-11-12 {
	width: 91.66%
}

.col-10-12 {
	width: 83.333%;
}

.col-9-12 {
	width: 75%;
}

.col-5-12 {
	width: 41.66%;
}

.col-7-12 {
	width: 58.33%
}

@media handheld, only screen and (max-width: 767px) {

	
	.grid {
		width: 100%;
		min-width: 0;
		margin-left: 0px;
		margin-right: 0px;
		padding-left: 0px;
		padding-right: 0px;
	}
	
	[class*='col-'] {
		width: 100%;
		float: none;
		margin-left: 0px;
		margin-right: 0px;
		margin-top: 10px;
		margin-bottom: 20px;
		padding-left: 20px;
		padding-right: 20px;
	}
}
/*****************************************
Wrappers
******************************************/
.ct-wrapper{
padding:0px 20px;
position:relative;
max-width:1230px;
margin:0 auto;
}
.main-wrapper{
width:auto;
margin-right:365px;
}
#content{
position:relative;
width:100%;
float:left;
}
.descriptionwrapper .description {
    color: #fff;
    opacity: 0.5;
    float: left;
    position: relative;
    left: -95px;
    top: 30px;
    font-size: 12px;
    font-family: Raleway;
    width: 260px;
    display: none;
}
.sidebar-wrapper{
width: 330px!important;
float: right;
margin: 0px 0px 40px 0;
}
/**** Layout Styling CSS *****/
body#layout .header-wrapper{
margin-top:40px;
}
body#layout #header, body#layout .header-right{
width:50%;
}
body#layout .outer-wrapper, body#layout .sidebar-wrapper, body#layout .ct-wrapper{
margin:0;
padding:0;
}
body#layout .footer.section{
float:left;
width:33%;
}

/*****************************************
Post Highlighter CSS
******************************************/
blockquote{
    font-style: italic;
    font-size: 16px;
    margin: 2em 0;
    padding: 2.3em 1.5em;
    background: #f9f9f9;
    border-left: 15px solid #1ABC9C;
    border-radius: 0;
    box-shadow: 11px 10px 0px #ECECEC;
}
pre {
background: #444 no-repeat right;
color: #FFFFFF;
padding: 30px;
white-space: pre-wrap;
white-space: -moz-pre-wrap;
white-space: -pre-wrap;
white-space: -o-pre-wrap;
word-wrap: break-word;
box-shadow: 11px 10px 0px #383838;
border: 0;
border-radius: 0;
line-height: 1.428571429;
margin: 0 0 10px;
font-size: 15px;
display: block;
word-break: break-all;
margin-bottom: 30px;

}
/* *********************************************************
  Header 
********************************************************* */

#top-header {
  position: fixed;
  z-index: 1000;
  width: 100%;
  padding: 23px 0;
/*transition*/
  -webkit-transition: all .15s linear;
     -moz-transition: all .15s linear;
       -o-transition: all .15s linear;
          transition: all .15s linear;
}

#top-header .grid {
  overflow: visible;
}

.logo {
    display: block;
    float: left;
    margin: 0;
    font-size: 35px;
    color: #fff;
    font-family: Raleway;
    font-weight: 100;
    text-transform: inherit;
}

.logo:hover, .logo:focus {
  -webkit-animation: rubberBand 0.5s 1;
     -moz-animation: rubberBand 0.5s 1;
       -o-animation: rubberBand 0.5s 1;
          animation: rubberBand 0.5s 1;
}

.header-default {
  background: #2C2D31;
}

.header-home {
  background: transparent;
/*box-shadow*/
  -webkit-box-shadow: none;
     -moz-box-shadow: none;
          box-shadow: none;
}

.header-home .navigation a {
  color: #fff;
}

.top-slider {
  position: relative;
  overflow: hidden;
  width: 100%;
  height: 750px;
}

.slider {
  height: 100%;
}

.top-slider .content-header {
  position: absolute;
  z-index: 999;
  top: 50%;
  left: 50%;
  width: 80%;
  height: 80%;
/*transform*/
  -webkit-transform: translate(-50%, -50%);
     -moz-transform: translate(-50%, -50%);
      -ms-transform: translate(-50%, -50%);
       -o-transform: translate(-50%, -50%);
          transform: translate(-50%, -50%);
}

.background-video {
  position: absolute;
  top: 0px;
  right: 0px;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: 1;
  overflow: hidden;
}

/* *********************************************************
  Navigation 
********************************************************* */

.navigation input[type=checkbox] {
  position: absolute;
  top: -9999px;
  left: -9999px;
}

.navigation label {
  display: none;
  cursor: pointer;
}

.navigation {
  position: relative;
  float: right;
  margin: 10px 0 0 0;
}

.navigation ul li {
  position: relative;
  display: inline;
  float: left;
}

.navigation a {
  font-size: .8em;
  display: block;
  margin-left: 20px;
  padding-bottom: 3px;
  color: #fff;
}

.navigation .current a, .navigation ul li a:hover, .navigation ul li a:focus {
  color:#1abc9c;
}

.navigation .sub-menu {
  position: absolute;
  z-index: 9999;
  top: 28px;
  left: -27px;
  visibility: hidden;
  width: 210px;
  padding: 20px;
/*transition*/
  -webkit-transition: all .1s linear;
     -moz-transition: all .1s linear;
       -o-transition: all .1s linear;
          transition: all .1s linear;
  opacity: 0;
  border-top: 1px solid#1abc9c;
  background: #fff;
/*box-shadow*/
  -webkit-box-shadow: 0 3px 10px rgba(0, 0, 0, .1);
  -moz-box-shadow: 0 3px 10px rgba(0, 0, 0, .1);
  box-shadow: 0 3px 10px rgba(0, 0, 0, .1);
}

.navigation .sub-menu li {
  position: relative;
}

.sub-menu li a {
  width: 170px;
  margin: 0!important;
  padding: .5em 1em;
  border-bottom: none!important;
/*border-radius*/
  -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
          border-radius: 5px;
}

.sub-menu li a:hover {
  background: #f9f9f9;
}

.navigation li:hover > ul {
  visibility: visible;
  opacity: 1;
}

/* *********************************************************
  Home Slider 
********************************************************* */

.header-carousel {
  overflow: hidden;
}

.home-slider {
  height: 700px;
  background-repeat: repeat;
  background-position: center center;
}

.home-slide-1 {
  background-image: url('http://4.bp.blogspot.com/-Qz4T1QyMGjI/VmcRXdmP3TI/AAAAAAAAAmY/4MLnu08BBTE/s1600/big1.jpg');
}

/* *********************************************************
  Parallax 
********************************************************* */

.parallax-section {
  z-index: -1;
  clear: both;
  background-image: url('http://3.bp.blogspot.com/-uqabgsYy1ig/VmcReCIGhoI/AAAAAAAAAmg/SRfXKWrDcMk/s1600/home.jpg');
  background-repeat: repeat;
  background-attachment: fixed;
  background-position: center center;
}

.parallax2 {
  background-image: url('http://2.bp.blogspot.com/-KEtTHF6ylRI/VmcReg8JeCI/AAAAAAAAAmk/IoYID5sVz1c/s1600/parallax2.jpg');
}

.parallax-section .content, .top-slider .content-header, .home-slider {
  margin: 0 auto;
  text-align: center;
}

.parallax-section .content-header, .home-slider .content-header {
  padding: 145px 0 250px;
}

.parallax2 .content {
  padding: 100px 0;
}

.top-slider .content-header {
  padding: 130px 0;
}

.parallax-section .content h2,
.content-header h2,
.parallax-section .content h3,
.content-header h3 {
  color: #fff;
}

.parallax-section h2 > span,
.parallax-section h3 > span,
.content-header h2 > span,
.content-header h3 > span {
  background: #fff;
}

.parallax-section .content h2, .content-header h2 {
  font-size: 2.5em;
}

.parallax-section .content p, .top-slider .content-header p, .home-slider .content p {
  width: 70%;
  margin: 0 auto 30px auto;
  color: #fff;
}
/* *********************************************************
  Services Section
********************************************************* */

.services, .service-box {
  text-align: center;
}

.service-icon {
  margin-top: 20px;
  padding-top: 1em;
}

.circle-icon {
  display: inline-block;
  font-size: 2em;
  padding: 1.1em 1.15em;
  color: #484f58;
/*border-radius*/
  -webkit-border-radius: 50%;
     -moz-border-radius: 50%;
          border-radius: 50%;
  background: transparent;
/*box-shadow*/
  -webkit-box-shadow: 0 0 0 2px #484f58;
     -moz-box-shadow: 0 0 0 2px #484f58;
          box-shadow: 0 0 0 2px #484f58;
/*transition*/
  -webkit-transition: all .15s linear;
     -moz-transition: all .15s linear;
       -o-transition: all .15s linear;
          transition: all .15s linear;
}

.service-box:hover .circle-icon {
    /*box-shadow*/
  -webkit-transform: scale(1.1);
     -moz-transform: scale(1.1);
      -ms-transform: scale(1.1);
       -o-transform: scale(1.1);
          transform: scale(1.1);
}

.service-entry {
  margin-top: 70px;
  padding: 0 .5em;
}

.service-entry p {
  margin-bottom: 10px;
}
/* *********************************************************
 Info Counter
********************************************************* */

.info-counter-icon {
  font-size: 4em;
  color: #1abc9c;
}

.info-counter-content, .info-counter-content h5 {
  color: #fff;
  font-size: 1.2em;
}

.info-counter-text {
  opacity: .7;
  font-size: 0.8em;
}
/*****************************************
Blog Post CSS
******************************************/
.recent-wrap {
  text-align: center;
}

.recent-work {
  background: #6578bc; /* Old browsers */
  background: -moz-linear-gradient(left,  #6578bc 0%, #1abc9c 100%); /* FF3.6+ */
  background: -webkit-gradient(linear, left top, right top, color-stop(0%,#6578bc), color-stop(100%,#1abc9c)); /* Chrome,Safari4+ */
  background: -webkit-linear-gradient(left,  #6578bc 0%,#1abc9c 100%); /* Chrome10+,Safari5.1+ */
  background: -o-linear-gradient(left,  #6578bc 0%,#1abc9c 100%); /* Opera 11.10+ */
  background: -ms-linear-gradient(left,  #6578bc 0%,#1abc9c 100%); /* IE10+ */
  background: linear-gradient(to right,  #6578bc 0%,#1abc9c 100%); /* W3C */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#6578bc', endColorstr='#1abc9c',GradientType=1 ); /* IE6-9 */

  position: relative;
  margin-bottom: 1em;
/*border-radius*/
  -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
          border-radius: 5px;
}

.portfolio-filter {
  margin: 40px 0 0;
  text-align: center;
}

.portfolio-items .mix {
  display: none;
}

.filters {
  margin-bottom: 40px;
}

.filters .filter {
  display: inline-block;
  margin: 4px;
  padding: 0.5em 1.65em;
  font-size: .8em;
  list-style: none;
  cursor: pointer;
  color: #484f58;
  border: 2px solid transparent;
/*border-radius*/
  -webkit-border-radius: 30px;
     -moz-border-radius: 30px;
          border-radius: 30px;
}

.filters .filter.active,
.filters .filter:hover {
  border: 2px solid #1abc9c;
  color: #1abc9c;
}

.recent-work a {
  position: relative;
  display: block;
}

.recent-work img {
  width: 100%;
  margin-bottom: -9px;
  object-fit: cover;
  height: 235px;
/*border-radius*/
  -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
          border-radius: 5px;
}

.recent-work:hover img {
  opacity: .35;
}

.overlay {
    position: absolute;
    left: 0px;
    padding: 10px;
    bottom: 10px;
    text-align: left;
    opacity: 0;
    transform: scale(1.3);
}

.overlay h2 a, .overlay span {
    color: #fff;
    line-height: 20px;
    font-family: Raleway;
}

.overlay h2 {
    margin: 10px 0 0;
    font-size: 1.2em;
}

.recent-work:hover .overlay {
  opacity: 1;
  transform: scale(1);
}

.recent-work .work-info {
  margin-top: 23px;
}

.work-info h4 {
  margin-bottom: .8em;
}

.post{
margin:20px 0 0;
padding:0 3% 20px;
}
h2#title2 {
    margin: 25px;
    font-size: 35px;
    font-weight: 800;
}
.post-title{
text-decoration:none;
font-size:30px;
line-height:normal;
padding:0 0 10px;
}
.post-title a{
text-decoration:none;
color:#000;
}
.post-body{
font-size:16px;
font-weight:normal;
padding:0;
margin:0;
line-height:29px;
word-wrap:break-word;
}
.post-header{
color:#999999;
font-family:Verdana,Arial,Tahoma,sans-serif;
font-size:12px;
}

#blog-pager{
border-top:0px solid #ddd;
padding:2em 0;
margin:0;
font-size:16px;
line-height:normal;
width: 100%;
}
.showpageOf{
display:none;
}
.showpageNum a, .showpage a{
margin:0 4px;
}
.showpagePoint{
margin:0 2px 0 0;
}
.blog-post-wrap, .blog-wrap-single {
  padding-top: 6em;
  text-align: center;
}

.blog-grid .content {
  text-align: center;
}

.post-wrap {
  position: relative;
  overflow: hidden;
  margin: 0 auto 2em auto;
  border-bottom: 2px solid #dee3e4;
/*border-radius*/
  -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
          border-radius: 5px;
  background: #fff;
}

.post-wrap img {
    width: 100%;
    height: 335px;
    object-fit: cover;
}

.post-wrap .post-meta {
  font-size: .8em;
  margin-bottom: 1.5em;
}

.post-wrap .post-meta li {
  display: inline-block;
}

.post-wrap .post-meta li a {
  margin: 0 20px 0 4px;
}

.post-wrap .post-meta li:last-child a {
  margin-right: 0;
}

.post-wrap .post-meta i {
  color:#1abc9c;
}

.post-wrap .post {
  padding: .2em 2em;
}

.post-wrap .entry-title {
  margin: 1em 0 .5em;
}

.post-wrap .post p {
  text-align: left;
  line-height: 2em;
  min-height: 100px;
}

.post-wrap .post p a {
  padding: 1px 1px 4px;
  border-radius: 3px;
}

.post-wrap .post p a:hover {
  background: #1abc9c;
  color: #fff;
}

/* Blog Page & Single */

.single {
  width: 70%;
  text-align: center;
}

.single .post-img {
  overflow: hidden;
  height: auto;
  max-height: 450px;
}

/* Blog Grid */

.blog-grid .post-wrap .post {
  padding: 0 1.2em .3em;
}

.blog-grid .post-img {
  position: relative;
  overflow: hidden;
  width: 100%;
}

.blog-grid .post-wrap .entry-title {
  font-size: 1.2em;
  margin-top: 1em;
}

/***** Button CSS *****/
.showpageArea a{
text-decoration:underline;
}
.showpageNum a{
background-color: #FFF;
-moz-border-radius: 3px;
-webkit-border-radius: 3px;
border-radius: 3px;
margin: 5px 5px 0 0;
padding: 8px 15px;
font-size: 16px;
border: 1px solid #e4e4e4;
color: #a1a1a1;
transition: all 0.17s ease-in-out;
-moz-transition: all 0.17s ease-in-out;
-webkit-transition: all 0.17s ease-in-out;
-o-transition: all 0.17s ease-in-out;
text-decoration: none;
}
.showpageNum a:hover{
text-decoration: none;
background-color: #1ABC9C;
color: #fff;
border: 1px solid #1ABC9C;
}
.showpagePoint{
    background-color: #1ABC9C;
    color: #FFF;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    -webkit-transition: all 0.2s ease 0s;
    -moz-transition: all 0.2s ease 0s;
    -o-transition: all 0.2s ease 0s;
    transition: all 0.2s ease 0s;
    margin: 5px 5px 0 0;
    padding: 8px 15px;
    border: 1px solid #1FAB8F;
    font-size: 16px;
}
.showpageOf{
text-decoration:none;
padding:3px;
margin:0 3px 0 0;
font-size:15px margin: 0 3px;
}
.showpage a{
background-color: #FFF;
-moz-border-radius: 3px;
-webkit-border-radius: 3px;
border-radius: 3px;
margin: 5px 5px 0 0;
padding: 8px 15px;
font-size: 16px;
border: 1px solid #e4e4e4;
color: #a1a1a1;
transition: all 0.17s ease-in-out;
-moz-transition: all 0.17s ease-in-out;
-webkit-transition: all 0.17s ease-in-out;
-o-transition: all 0.17s ease-in-out;
text-decoration: none;
}
.showpage a:hover{
text-decoration: none;
    background-color: #2E3033;
    color: #fff;
    border: 1px solid #050606;
}
.showpageOf{
display:none;
}
.showpageNum{
margin:0 3px;
}
.showpageArea{
padding-bottom:20px;
}
/***** Profile Widget CSS *****/
.Profile img{
border:1px solid #cecece;
background:#fff;
float:left;
margin:5px 10px 5px 0;
padding:5px;
/*border-radius*/
-webkit-border-radius:50px;
-moz-border-radius:50px;
border-radius:50px;
}
.profile-data{
color:#999999;
font:bold 20px/1.6em Arial,Helvetica,Tahoma,sans-serif;
font-variant:small-caps;
margin:0;
text-transform:capitalize;
}
.profile-datablock{
margin:0.5em 0;
}
.profile-textblock{
line-height:1.6em;
margin:0.5em 0;
}
a.profile-link{
clear:both;
display:block;
font:80% monospace;
padding:10px 0;
text-align:center;
text-transform:capitalize;
}
/*****************************************
Sidebar CSS
******************************************/
.sidebar{
margin:0;
padding:0;
display:block;
}
.sidebar h2{
    font-size: 19px;
    text-transform: none;
    margin-right: -20px;
    margin-left: -20px;
    margin-top: 0px;
    margin-bottom: 7px;
    padding-bottom: 15px;
    border-bottom: 1px solid #ddd;
}
.sidebar .widget{
    color: #BCC2C9;
    margin-bottom: 30px;
    float: left;
    width: 100%;
    background: #fff;
    padding: 20px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    border-bottom: 1px solid #d3d5d7;
    -webkit-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    -moz-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
}
.sidebar ul{
margin:0;
padding:0;
list-style:none;
}
.sidebar li{
margin:0 0 0 15px;
padding:0 0 5px;
text-transform:capitalize;
}
/*****************************************
Label CSS
******************************************/
.list-label-widget-content li {
    display: block;
    padding: 5px 0px;
    border-bottom: 1px solid #f3f3f3;
    position: relative;
    text-align: left;
    margin-right: -20px;
    margin-left: -20px;
}
.list-label-widget-content li a:before {
    content: '\203a';
    position: absolute;
    left: 0px;
    top: 5px;
    font-size: 22px;
    margin-left: 7px;
    color: rgba(1, 1, 1, 0.7);
}
.list-label-widget-content li a {
    color: #010101;
    font-size: 12px;
    padding-left: 20px;
    font-weight: 400;
    text-transform: uppercase;
}
.list-label-widget-content li a:hover {
    color:#1abc9c
}
.list-label-widget-content li span:last-child {
	color: rgba(0, 0, 0, 0.31);
    font-size: 28px;
    font-weight: 700;
    position: absolute;
    top: 5px;
    right: 0;
    opacity: .3;
}
.cloud-label-widget-content {
    margin-top: 10px
}
.cloud-label-widget-content span a {
    font-size: 13px;
    color: #999;
    background-color: #242527;
    padding: 7px 14px;
    float: left;
    position: relative;
    display: inline-block;
    margin: 0 5px 5px 0;
    text-transform: capitalize
}
.cloud-label-widget-content span a:hover {
    color: #fff!important;
    background-color: #1ABC9C;
}
.label-size-1,
.label-size-2 {
    opacity: 100;
    filter: alpha(opacity=10000)
}

#ArchiveList select{border:1px solid #EEE;border-radius:2px;padding:8px;width:100%;cursor:pointer;font:normal normal 13px Montserrat, sans-serif}

/***** Popular Post *****/
.PopularPosts .item-thumbnail {
    margin: 0 0px 0px 10px !important;
    width: 80px;
    height: 80px;
    float: left;
    overflow: hidden;
}
.PopularPosts ul li img {
    padding: 0;
    width: 80px;
    height: 80px;
    transition: all .3s ease-out!important;
    -webkit-transition: all .3s ease-out!important;
    -moz-transition: all .3s ease-out!important;
    -o-transition: all .3s ease-out!important;
    border-radius: 240px;
}
.PopularPosts ul li img:hover {
    border-radius:0;
}
.PopularPosts .widget-content ul li {
    overflow: hidden;
    border-top: 1px solid #EFEFEF;
    padding: 10px 0;
    margin-right: -20px;
    margin-left: -20px;
}
.sidebar .PopularPosts .widget-content ul li:first-child{
    padding-top: 0;
    border-top: 0
}
.PopularPosts ul li a {
    color: #010101;
    font-size: 13px;
    line-height: 1.4em;
    font-weight: 500;
}
.PopularPosts ul li a:hover {
    color: #16a085
}
.PopularPosts .item-title {
    margin: 0;
    padding: 0;
    margin-right: 10px;
    margin-left: 100px;
  	text-align: left;
}
.PopularPosts .item-title .popular_span {
    color: #C4C4C4;
    font-size: 13px;
    font-style: normal;
    line-height: 21px;
    margin-top: 3px
}
#footer .PopularPosts .widget-content ul li {
    margin: 0!important;
    border: 0!important;
}
.FollowByEmail td {
    width: 100%;
    float: left
}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit {
    margin-left: 0;
    width: 140px;
    border-radius: 0;
    height: 30px;
    border-radius: 21px;
    font-size: 11px;
    font-family: inherit;
    color: #fff;
    background-color: #1ABC9C;
    text-transform: uppercase;
    letter-spacing: 1px;
}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit:hover {
    background-color: #333;
    color: #FFF
    border-radius: 3px;
}
.FollowByEmail .follow-by-email-inner .follow-by-email-address {
    padding-left: 10px;
    height: 35px;
    border: 1px solid #EEE;
    margin-bottom: 5px;
    font: normal normal 13px Montserrat, sans-serif;
    font-size: 12px;
    box-sizing: border-box
}
.FollowByEmail .follow-by-email-inner .follow-by-email-address:focus {
    border: 1px solid #EEE
}


.widget-item-control a {
    opacity: .5!important;
}
.widget .widget-item-control a img {
    border: none!important;
    padding: 0!important;
    background: none!important;
    -moz-box-shadow: none!important;
    -webkit-box-shadow: none!important;
    -ie-box-shadow: none!important;
    box-shadow: none!important;
}
/*****************************************
Footer CSS
******************************************/
#footer{
    width: 100%;
    background: #2C2D31;
    color: #FFFFFF;
    padding-top: 115px;
    padding-bottom: 90px;
}
.footer{
float:left;
width:32%;
}
.footer h2{
    color: #fff;
    font-family: 'Montserrat', Helvetica, Arial, sans-serif;
    font-size: 1.2em;
    line-height: .9em;
    position: relative;
    background: rgb(36, 37, 39);
    margin: 1em 0 1.4em;
    padding: 12px 20px;
    border-radius: 204px;
}
.footer .widget{
clear:both;
font-size:16px;
line-height:26px;
margin:15px 25px 25px;
}
.footer ul{
margin:0;
padding:0;
list-style:none;
}
.footer li{
margin:0 0 0 15px;
padding:0 0 5px;
text-transform:capitalize;
}
.footer-credits{
border-top:1px solid #555;
padding:15px;
background:#111111;
text-shadow:1px 1px #000000;
color:#999;
font-size:80%;
}
.footer-credits .attribution{
float:right;
}
.footer-credits .attribution a{
font-style:italic;
}
#footer a, .footer-credits a{
text-decoration:none;
color:#fff;
}
#footer a:hover, .footer-credits a:hover{
text-decoration:underline;
color:#D4D4D4;
}

.social-set {
  width: 100%;
  margin: 0 0 .5em;
  padding: 0 0 1em 0;
  text-align: center;
}

.social-set a {
  font-size: 1.5em;
  margin-right: .5em;
  padding: 1em;
}

.copyright {
  text-align: center;
}
/*****************************************
Comments CSS
******************************************/

.comment-form {
overflow:hidden;
}
.comments h3 {
line-height:normal;
text-transform:uppercase;
color:#333;
font-weight:700;
font-size:14px;
margin:0 0 20px;
padding:0;
}
h4#comment-post-message {
display:none;
margin:0;
}
.comments {
    background: #fff;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    border-bottom: 1px solid #d3d5d7;
    -webkit-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    -moz-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    border-top: 0;
    padding: 5px 20px!important;
}
.comments .comments-content {
font-size:13px;
margin-bottom:8px;
}
.comments .comments-content .comment-thread ol {
text-align:left;
margin:13px 0;
padding:0;
}
.comments .avatar-image-container {
background:#fff;
overflow:visible;
padding:6px;
}
.comments .comment-block {
position:relative;
background:#fff;
margin-left:60px;
border-left:3px solid #ddd;
border-top:1px solid #DDD;
border-right:1px solid #DDD;
border-bottom:1px solid #DDD;
padding:15px;
}
.comments .comment-block:before {
content:"width:0;height:0;position:absolute;right:100%;top:14px;border-width:10px;border-style:solid;border-color:transparent #DDD transparent transparent;display:block}.comments .comments-content .comment-replies{margin:8px 0;margin-left:60px}.comments .comments-content .comment-thread:empty{display:none}.comments .comment-replybox-single{background:#f0f0f0;padding:0;margin:8px 0;margin-left:60px}.comments .comment-replybox-thread{background:#f0f0f0;margin:8px 0 0;padding:0}.comments .comments-content .comment{margin-bottom:6px;padding:0}.comments .comments-content .comment:first-child{padding:0;margin:0}.comments .comments-content .comment:last-child{padding:0;margin:0}.comments .comment-thread.inline-thread .comment,.comments .comment-thread.inline-thread .comment:last-child{margin:0 0 5px 30%}.comment .comment-thread.inline-thread .comment:nth-child(6){margin:0 0 5px 25%}.comment .comment-thread.inline-thread .comment:nth-child(5){margin:0 0 5px 20%}.comment .comment-thread.inline-thread .comment:nth-child(4){margin:0 0 5px 15%}.comment .comment-thread.inline-thread .comment:nth-child(3){margin:0 0 5px 10%}.comment .comment-thread.inline-thread .comment:nth-child(2){margin:0 0 5px 5%}.comment .comment-thread.inline-thread .comment:nth-child(1){margin:0 0 5px}.comments .comments-content .comment-thread{margin:0;padding:0}.comments .comments-content .inline-thread{background:#fff;border:1px solid #DDD;padding:15px;margin:0}.comments .comments-content .icon.blog-author{display:inline}.comments .comments-content .icon.blog-author:after{content:"background:#0088C2;
color:#fff;
font-size:11px;
padding:2px 5px;
}
.comment-header {
text-transform:uppercase;
font-size:12px;
}
.comments .comments-content .datetime {
margin-left:6px;
}
.comments .comments-content .datetime a {
color:#888;
}
.comments .comment .comment-actions a {
display: inline-block;
color: #333;
font-weight: 700;
font-size: 10px;
border: 1px solid #484848;
line-height: 15px;
border-radius: 50px;
padding: 5px 10px;
margin: 4px 8px 0 0;
}
.comments .continue a {
color: #333;
display: inline-block;
font-size: 10px;
padding: 4px 15px;
float: right;
background-color: #f9f9f9;
border: 1px solid #ddd;
border-radius: 40px;
}
#bc_0_0I{display:none;}
.comments .comment .comment-actions a:hover,.comments .continue a:hover {
text-decoration:underline;
}
.pesan-komentar p {
line-height:normal;
margin:0;
}
.fb-comments {
width:100%!important;
}
/*****************************************
Responsive styles
******************************************/

@media handheld, only screen and (max-width: 1200px) {
  #top-header {
    padding: 15px 20px;
  }

  #price-tables #plans .plan {
    width: 49%;
    margin: 0 2% 20px 0;
  }

  #price-tables #plans > li:nth-child(2n) {
    margin-right: 0!important;
  }

  .team-social {
    height: 30px;
  }

  .team-social a i {
    font-size: 1em;
    padding: 3px;
  }
}

@media handheld, only screen and (max-width: 767px) {
  #top-header {
    position: absolute;
    padding: 8px 0;
  }

  .logo-wrap {
    float: left;
    width: 100%;
    margin-bottom: .5em;
  }

  #top-header .col-1-1 {
    margin: 0;
  }

  .navigation ul {
    display: none;
    height: 100%;

  }

  .navigation {
    float: none;
  }

  .navigation li {
    width: 100%;
  }

  .navigation a {
    margin-left: 0;
    width: 100% !important;
    display: block;
  }

  .navigation label {
    position: absolute;
    display: block;
    right: 0;
    top: 7px;
    color: #fff;
    min-height: 2.25em;
    padding: .45em;
    font-size: 1.1em;
    margin: 0;
  }

  .navigation label:after {
    position: absolute;
    right: .25em;
    top: 0;
    content: "\2261";
    font-size: 1.8em;
  }

  .navigation input[type=checkbox]:checked ~ label:after {
    color: #fff;
  }

  .navigation input[type=checkbox]:checked ~ ul {
    display: block;
  }

  .navigation input[type=checkbox]:checked ~ ul > li {
    width: 100%;
    text-align: left;
    padding: .8em 0;
  }

  .navigation .sub-menu {
    position: relative;
    top: 0;
    left: 0;
    visibility: visible;
    opacity: 1;
    display: block;
    border: none;
    box-shadow: none;
    width: 100%;
  }

  .service-entry {
    margin-bottom: 2.5em;
  }

  #page-sidebar-grid .post-wrap {
    width: 100%;
  }

  .isotope-item {
    width: 100%;
  }

  .single {
    width: 100%
  }

  .overlay i {
    padding: 145px 0;
  }

  .parallax-section .content h2, .content-header h2  {
    font-size: 2em;
  }

  #price-tables #plans .plan {
    width: 100%;
    margin: 0 2% 20px 0;
  }

  #price-tables #plans > li:nth-child(2n) {
    margin-right: 0;
  }
}

@media handheld, only screen and (max-width: 480px) {
  
  .header-carousel {
    height: 620px;
  }

  .social-set a {
    padding: 0 !important;
  }

  #page-sidebar-no-sidebar .post-wrap .post {
    padding: 1em !important;
  }

  .post-wrap .post-meta li a {
    margin: 0;
    width: 100%;
    padding: 6px;
  }

  .comments, #leave-comment {
    padding: .6em 1.7em;
  }

  ul.nested-comments li {
    margin: 0 1em;
  }

  ul.nested-comments ul li {
    margin: 0;
  }

  #page-sidebar-no-sidebar .post-wrap {
    width: 100%;
  }

  .parallax-section .content p, .top-slider .content-header p {
    width: 100%;
  }

  .parallax-section .wrap {
    padding: 0;
  }

  .parallax-section .content h2, .content-header h2 {
    font-size: 1.2em;
  }

  .parallax-section .content p, .top-slider .content-header p, .home-slider .content p {
    font-size: 0.8em;
    margin: 0 auto 10px auto;
    line-height: 18px;
}

  .team-social {
    height: 50px;
    opacity: 1;
  }

  .team-social a i {
    font-size: 1.5em;
    padding: 8px;
  }
}

@media screen and (max-width: 960px){
.ct-wrapper{    padding:0 15px;
}
.main-wrapper{
margin-right:0;
width:100%;
}
.sidebar-wrapper{
float:left;
width:auto;
margin-left:20px;
}
}
@media screen and (max-width: 768px){
#comment-editor{
margin:10px;
}
.footer{
width:50%;
}
}

@media screen and (max-width: 420px){
.comments .comments-content .datetime{    display:block;
float:none;
}
.comments .comments-content .comment-header{
height:70px;
}
}
@media screen and (max-width: 320px){
.footer { width:100%;
}
.ct-wrapper{
padding:0;
}
.comments .comments-content .comment-replies{
margin-left:0;
}
}

/*****************************************
Hiding Header Date and Feed Links
******************************************/
h2.date-header{
display:none;
}
/* *********************************************************
  Loader
********************************************************* */

.loader-overlay {
  width: 100%;
  height: 100%;
  background: #ECF0F1;
  position: fixed;
  bottom: 0px;
  left: 0px;
  right: 0px;
  top: 0px;
  z-index: 9999;
}

.loader {
  height: 50px;
  left: 50%;
  margin: -25px 0 0 -75px;
  position: absolute;
  top: 50%;
  width: 150px;
}
.loader .bar {
  background-color: #69C98C;
  font-size: 0;
  height: 6px;
  border-radius: 3px;
  opacity: 0;
  width: 25px;
  -webkit-animation-duration: 2s;
  -webkit-animation-fill-mode: both;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-name: subtleIn;
  -webkit-animation-timing-function: ease-in-out;
  display: inline-block;
}
.loader .bar:nth-child(1) {
  -webkit-animation-delay: 0s;
}
.loader .bar:nth-child(2) {
  background-color: #1abc9c;
  -webkit-animation-delay: .3s;
}
.loader .bar:nth-child(3) {
  background-color: #1AB4BC;
  -webkit-animation-delay: .6s;
}
.loader .bar:nth-child(4) {
  background-color: #1AA1BC;
  -webkit-animation-delay: .9s;
}
.loader .bar:nth-child(5) {
  background-color: #1A7EBC;
  -webkit-animation-delay: 1.2s;
}

@-webkit-keyframes subtleIn {
  0% {
    opacity: 0;
    -webkit-transform: translateY(300%);
    transform: translateY(300%);
  }

  30% {
    opacity: 1;
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
}
/* *********************************************************
  Clients Logos Section 
********************************************************* */

.cl-logo-carousel .item figure {
  max-height: 100px;
  margin: 5px;
  padding: 31px 0;
}

.cl-logo-carousel .item figure img {
  display: block;
  width: 70%;
  margin: 0 auto;
}

.cl-logo-carousel.owl-theme .owl-controls .owl-page span, .header-carousel.owl-theme .owl-controls .owl-page span, .cl-client-carousel.owl-theme .owl-controls .owl-page span {
  display: block;
  width: 11px;
  height: 11px;
  margin: 5px 7px;
  border: 2px solid #ccc;
/*border-radius*/
  -webkit-border-radius: 50%;
     -moz-border-radius: 50%;
          border-radius: 50%;
  background: #bfbfbf;
  background-color: transparent;
  transition: all .13s linear;
}

.header-carousel.owl-theme .owl-controls .owl-page.active span,
.header-carousel.owl-theme .owl-controls.clickable .owl-page span:hover,

.cl-logo-carousel.owl-theme .owl-controls .owl-page.active span,
.cl-logo-carousel.owl-theme .owl-controls.clickable .owl-page:hover span,

.cl-client-carousel.owl-theme .owl-controls .owl-page.active span,
.cl-client-carousel.owl-theme .owl-controls.clickable .owl-page:hover span {
  border-color: transparent;
  background-color:#1abc9c;
  box-shadow: 0 0 0 3px #1abc9c;
}

.header-carousel .owl-pagination, .header-carousel .owl-buttons {
  position: absolute;
}

.header-carousel .owl-pagination {
  bottom: 95px;
  left: 50%;
  width: 200px;
  margin-left: -100px;
  text-align: center;
}

.header-carousel .owl-buttons {
  top: 300px;
  width: 100%;
}

.header-carousel .owl-buttons .owl-prev, .header-carousel .owl-buttons .owl-next {
  width: 8px;
  height: 22px;
  text-indent: -9999px;
  background: url(images/arrows.png) no-repeat;
}

.header-carousel .owl-buttons .owl-prev {
  background-position: 0 -22px;
}

.header-carousel .owl-buttons .owl-prev {
  margin-left: 40px;
  float: left;
}

.header-carousel .owl-buttons .owl-next {
  margin-right: 40px;
  float: right;
}

/**********************************************************
  Quotes Section 
**********************************************************/
.quotes-icon {
  color: #1abc9c;
  font-size: 4em;
  line-height: 1;
  margin-bottom: 27px;
  vertical-align: top;
}

.cl-client-carousel .client-carousel-item h4 {
  font-style: italic;
}

.cl-client-carousel .client-carousel-item p {
  line-height: 1.8em;
  width: 80%;
  margin: 10px auto;
}

.cl-client-carousel.owl-theme .owl-controls .owl-page span {
  display: block;
  margin: 5px 7px;
/*border-radius*/
  -webkit-border-radius: 20px;
     -moz-border-radius: 20px;
          border-radius: 20px;
  background: #fff;
}
/**********************************************************
Owl Carousel CSS
**********************************************************/
.owl-carousel .owl-wrapper:after {
	content: ".";
	display: block;
	clear: both;
	visibility: hidden;
	line-height: 0;
	height: 0;
}
/* display none until init */
.owl-carousel{
	display: none;
	position: relative;
	width: 100%;
	-ms-touch-action: pan-y;
}
.owl-carousel .owl-wrapper{
	display: none;
	position: relative;
	-webkit-transform: translate3d(0px, 0px, 0px);
}
.owl-carousel .owl-wrapper-outer{
	overflow: hidden;
	position: relative;
	width: 100%;
}
.owl-carousel .owl-wrapper-outer.autoHeight{
	-webkit-transition: height 500ms ease-in-out;
	-moz-transition: height 500ms ease-in-out;
	-ms-transition: height 500ms ease-in-out;
	-o-transition: height 500ms ease-in-out;
	transition: height 500ms ease-in-out;
}
	
.owl-carousel .owl-item{
	float: left;
}
.owl-controls .owl-page,
.owl-controls .owl-buttons div{
	cursor: pointer;
}
.owl-controls {
	-webkit-user-select: none;
	-khtml-user-select: none;
	-moz-user-select: none;
	-ms-user-select: none;
	user-select: none;
	-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

/* mouse grab icon */
.grabbing { 
    cursor:url(grabbing.png) 8 8, move;
}

/* fix */
.owl-carousel  .owl-wrapper,
.owl-carousel  .owl-item{
	-webkit-backface-visibility: hidden;
	-moz-backface-visibility:    hidden;
	-ms-backface-visibility:     hidden;
  -webkit-transform: translate3d(0,0,0);
  -moz-transform: translate3d(0,0,0);
  -ms-transform: translate3d(0,0,0);
}
.owl-theme .owl-controls{
	text-align: center;
}

/* Styling Next and Prev buttons */

.owl-theme .owl-controls .owl-buttons div{
	color: #FFF;
	display: inline-block;
	zoom: 1;
	*display: inline;/*IE7 life-saver */
	font-size: 12px;
	filter: Alpha(Opacity=50);/*IE7 fix*/
	opacity: 0.7;
}
/* Clickable class fix problem with hover on touch devices */
/* Use it for non-touch hover action */
.owl-theme .owl-controls.clickable .owl-buttons div:hover{
	filter: Alpha(Opacity=100);/*IE7 fix*/
	opacity: 1;
	text-decoration: none;
}

/* Styling Pagination*/

.owl-theme .owl-controls .owl-page{
	display: inline-block;
	zoom: 1;
	*display: inline;/*IE7 life-saver */
}


/* If PaginationNumbers is true */

.owl-theme .owl-controls .owl-page span.owl-numbers{
	height: auto;
	width: auto;
	color: #FFF;
	padding: 2px 10px;
	font-size: 12px;
	-webkit-border-radius: 30px;
	-moz-border-radius: 30px;
	border-radius: 30px;
}

/* preloading images */
.owl-item.loading{
	min-height: 150px;
	background: url(AjaxLoader.gif) no-repeat center center
}
.owl-origin {
	-webkit-perspective: 1200px;
	-webkit-perspective-origin-x : 50%;
	-webkit-perspective-origin-y : 50%;
	-moz-perspective : 1200px;
	-moz-perspective-origin-x : 50%;
	-moz-perspective-origin-y : 50%;
	perspective : 1200px;
}
/* fade */
.owl-fade-out {
  z-index: 10;
  -webkit-animation: fadeOut .7s both ease;
  -moz-animation: fadeOut .7s both ease;
  animation: fadeOut .7s both ease;
}
.owl-fade-in {
  -webkit-animation: fadeIn .7s both ease;
  -moz-animation: fadeIn .7s both ease;
  animation: fadeIn .7s both ease;
}
/* backSlide */
.owl-backSlide-out {
  -webkit-animation: backSlideOut 1s both ease;
  -moz-animation: backSlideOut 1s both ease;
  animation: backSlideOut 1s both ease;
}
.owl-backSlide-in {
  -webkit-animation: backSlideIn 1s both ease;
  -moz-animation: backSlideIn 1s both ease;
  animation: backSlideIn 1s both ease;
}
/* goDown */
.owl-goDown-out {
  -webkit-animation: scaleToFade .7s ease both;
  -moz-animation: scaleToFade .7s ease both;
  animation: scaleToFade .7s ease both;
}
.owl-goDown-in {
  -webkit-animation: goDown .6s ease both;
  -moz-animation: goDown .6s ease both;
  animation: goDown .6s ease both;
}
/* scaleUp */
.owl-fadeUp-in {
  -webkit-animation: scaleUpFrom .5s ease both;
  -moz-animation: scaleUpFrom .5s ease both;
  animation: scaleUpFrom .5s ease both;
}

.owl-fadeUp-out {
  -webkit-animation: scaleUpTo .5s ease both;
  -moz-animation: scaleUpTo .5s ease both;
  animation: scaleUpTo .5s ease both;
}
/* Keyframes */
/*empty*/
@-webkit-keyframes empty {
  0% {opacity: 1}
}
@-moz-keyframes empty {
  0% {opacity: 1}
}
@keyframes empty {
  0% {opacity: 1}
}
@-webkit-keyframes fadeIn {
  0% { opacity:0; }
  100% { opacity:1; }
}
@-moz-keyframes fadeIn {
  0% { opacity:0; }
  100% { opacity:1; }
}
@keyframes fadeIn {
  0% { opacity:0; }
  100% { opacity:1; }
}
@-webkit-keyframes fadeOut {
  0% { opacity:1; }
  100% { opacity:0; }
}
@-moz-keyframes fadeOut {
  0% { opacity:1; }
  100% { opacity:0; }
}
@keyframes fadeOut {
  0% { opacity:1; }
  100% { opacity:0; }
}
@-webkit-keyframes backSlideOut {
  25% { opacity: .5; -webkit-transform: translateZ(-500px); }
  75% { opacity: .5; -webkit-transform: translateZ(-500px) translateX(-200%); }
  100% { opacity: .5; -webkit-transform: translateZ(-500px) translateX(-200%); }
}
@-moz-keyframes backSlideOut {
  25% { opacity: .5; -moz-transform: translateZ(-500px); }
  75% { opacity: .5; -moz-transform: translateZ(-500px) translateX(-200%); }
  100% { opacity: .5; -moz-transform: translateZ(-500px) translateX(-200%); }
}
@keyframes backSlideOut {
  25% { opacity: .5; transform: translateZ(-500px); }
  75% { opacity: .5; transform: translateZ(-500px) translateX(-200%); }
  100% { opacity: .5; transform: translateZ(-500px) translateX(-200%); }
}
@-webkit-keyframes backSlideIn {
  0%, 25% { opacity: .5; -webkit-transform: translateZ(-500px) translateX(200%); }
  75% { opacity: .5; -webkit-transform: translateZ(-500px); }
  100% { opacity: 1; -webkit-transform: translateZ(0) translateX(0); }
}
@-moz-keyframes backSlideIn {
  0%, 25% { opacity: .5; -moz-transform: translateZ(-500px) translateX(200%); }
  75% { opacity: .5; -moz-transform: translateZ(-500px); }
  100% { opacity: 1; -moz-transform: translateZ(0) translateX(0); }
}
@keyframes backSlideIn {
  0%, 25% { opacity: .5; transform: translateZ(-500px) translateX(200%); }
  75% { opacity: .5; transform: translateZ(-500px); }
  100% { opacity: 1; transform: translateZ(0) translateX(0); }
}
@-webkit-keyframes scaleToFade {
  to { opacity: 0; -webkit-transform: scale(.8); }
}
@-moz-keyframes scaleToFade {
  to { opacity: 0; -moz-transform: scale(.8); }
}
@keyframes scaleToFade {
  to { opacity: 0; transform: scale(.8); }
}
@-webkit-keyframes goDown {
  from { -webkit-transform: translateY(-100%); }
}
@-moz-keyframes goDown {
  from { -moz-transform: translateY(-100%); }
}
@keyframes goDown {
  from { transform: translateY(-100%); }
}

@-webkit-keyframes scaleUpFrom {
  from { opacity: 0; -webkit-transform: scale(1.5); }
}
@-moz-keyframes scaleUpFrom {
  from { opacity: 0; -moz-transform: scale(1.5); }
}
@keyframes scaleUpFrom {
  from { opacity: 0; transform: scale(1.5); }
}

@-webkit-keyframes scaleUpTo {
  to { opacity: 0; -webkit-transform: scale(1.5); }
}
@-moz-keyframes scaleUpTo {
  to { opacity: 0; -moz-transform: scale(1.5); }
}
@keyframes scaleUpTo {
  to { opacity: 0; transform: scale(1.5); }
}
/**********************************************************
Team CSS
**********************************************************/
.team-wrap {
  text-align: center;
}

.staff-content {
/*border-radius*/
  -webkit-border-radius: 5px;
     -moz-border-radius: 5px;
          border-radius: 5px;
  background: #fff;
}

.staff-info {
  padding: 0 10px;
}

.staff-info span {
  color:#1abc9c;
}

.staff-img {
  position: relative;
  display: table;
  margin: 0 auto;
  background: #fff;
}

.staff-img {
  position: relative;
  display: table;
  width: 100%;
}

.staff-img img {
  width: 100%;
  border-radius: 5px 5px 0 0;
}

.staff-img:hover img {
  opacity: 1;
}

.staff-content h5 {
  margin-bottom: .5em;
}

.staff-content span {
  display: inline-block;
  margin-bottom: 10px;
}

.team-social {
  margin: 0 auto;
  position: absolute;
  left: 0;
  bottom: -10px;
  background: #fff;
  width: 100%;
  opacity: 0;
  padding: 7px 0;
  height: 50px;
  transition: .1s linear;
  transform: translateY(10px);
}

.team-social a {
  display: inline-block;
  padding: 0 7px;
}

.team-social a i {
  font-size: 1.5em;
  display: table;
  padding: 8px;
  color: #484f58;
}

.sl-fb i:hover {
  color: #4f689e;
}

.sl-tw i:hover {
  color: #74c7d5;
}

.sl-gp i:hover {
  color: #df5c64;
}

.sl-ln i:hover {
  color: #017eba;
}

.staff-content:hover .team-social {
  opacity: 1;
  transform: translateY(0);
}

/**********************************************************
Contact CSS
**********************************************************/
.contact {
  padding-top: 0;
	padding-bottom: 0
}

.contact h2 {
  text-align: center;
      margin-top: 135px;
}

.contact .address h3 {
  margin-top: 0;
}

address {
  margin-top: 3em;
}

address div {
  position: relative;
  margin-top: 20px;
}

address i {
  position: absolute;
  top: 2px;
  left: 0;
}

.address span {
  line-height: 1.1;
  margin-bottom: 3px;
  color: #484f58;
  font-size: 1.125em;
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
} 

.phone {
  line-height: 30px;
}

.box-icon {
    float: left;
    font-size: 25px;
    margin: 0 10px 0 0;
    display: block;
    padding: 26px;
}

.box-icon i {
    color: #16a085;
    padding: 14px;
    background: #fff;
    border-radius: 250px
}

/* Form, Comments and Contact */

.comments, .form {
  padding: 0em 3em;
}

.leave-comment {
  width: 80%;
  margin: 0 auto;
}

.contact-form .form {
  padding: 0;
}

.comments {
  margin: 0 0 1em;
  text-align: left;
}

ul.nested-comments  ul li {
  margin: 1em 3em;
}

.comment p {
  margin-left: 76px;
}

.comment {
  margin-bottom: 1em;
  padding: 1em 0;
}

.comment-avatar {
  float: left;
  width: 60px;
  height: auto;
  margin-right: 1em;
}

.comment-meta span {
  font-size: .8em;
  color: #999;
}

.comment-meta .mid-sep {
  padding: 0 2px;
}

.avatar {
  width: 60px;
  height: 60px;
/*border-radius*/
  -webkit-border-radius: 30px;
     -moz-border-radius: 30px;
          border-radius: 30px;
}
/* Inputs */

input:not([type=submit]):not([type=file]), textarea {
  width: 100% !important;
  height: 50px;
  margin-bottom: 25px;
  padding: 0 15px 2px;
  border: 2px solid #ebebeb;
/*border-radius*/
  -webkit-border-radius: 6px;
     -moz-border-radius: 6px;
          border-radius: 6px;
  background: white;
  box-shadow: 0px 0px 0px 2px transparent;
  -webkit-transition: box-shadow 0.3s;
  transition: box-shadow 0.3s;
}

input:not([type=submit]):not([type=file]):focus, textarea:focus {
  border-color:#1abc9c;
  outline: none;
}

textarea {
  max-width: 100%;
  min-height: 150px;
  padding: 15px;
}

.submit {
  font-size: 1.1em;
  position: relative;
  width: 190px;
  height: 45px;
  margin-bottom: 2em;
  padding: 0;
  cursor: pointer;
  vertical-align: top;
  border: 0;
  float: right;
}

.submit:active {
  outline: none;
}

.leave-comment {
  margin-top: 3em;
}

input:not([type=submit]):not([type=file]):focus, textarea:focus {
  -webkit-animation: rubberBand 0.5s 1;
     -moz-animation: rubberBand 0.5s 1;
       -o-animation: rubberBand 0.5s 1;
          animation: rubberBand 0.5s 1;
}
.pagination {
    position: relative;
    width: 100%;
}
.pagination {
    display: inline-block;
    padding-left: 0;
    margin: 20px 0;
    border-radius: 4px;
}
.pagination>li {
    display: inline;
}
.pagination>li>a, .pagination>li>span {
    display: block;
    float: left;
    margin: 5px 15px 35px 0;
    padding: 5px 20px;
    text-decoration: none;
    width: auto;
    color: #34495e;
    background: #ecf0f1;
    min-width: 25px;
    min-height: 35px;
    text-align: center;
    line-height: 35px;
    border: 0;
}
.pagination>li>a, .pagination>li>span {
    position: relative;
    float: left;
    padding: 9px 33px;
    line-height: 1.42857143;
    text-decoration: none;
    color: #484F58;
    background-color: #fff;
    margin-left: -1px;
    border: 1px solid #ddd;
    border-radius: 30px;
}
a.home-link {
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
}
]]></b:skin>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<style>
  .sidebar-wrapper{display:none;}
  .outer-wrapper{background:transparent;border:0;}
  .main-wrapper{margin:0;}
  #content{float:none;border:0;}
</style>
</b:if>
</b:if>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<style>
  .firstcurveUpColor{
    fill: #f9f9f9!important;
    stroke: #f9f9f9!important;
}
  .secondcurveUpColor{
fill: #fff!important;
stroke: #fff!important;
}
.recent-wrap {
    padding: 0!important;
	background: #f9f9f9!important;
	padding-top: 100px!important;
}
.contact {
    background: #fff!important;
    border-top: 1px solid #ddd!important;
}
</style>
</b:if>
<!-- Style For Post -->
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<style>
  .sjps{
    width: 100%!important;
    padding: 30px;
    padding-top: 40px;
    background: #fff;
    margin-bottom: 30px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
    padding-bottom: 7px;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    border-bottom: 1px solid #d3d5d7;
    -webkit-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    -moz-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
}
  .padding_post{padding:0!important;}

  .pagination{
	margin: 16px 0 0 0;
    float: none;
    display: inline-block;
    width: auto;
}
  .pagination&gt;li&gt;a:hover, .pagination&gt;li&gt;a:focus, .pagination&gt;.active&gt;a, .pagination&gt;.active&gt;span{
        color: #fff;
    background: #484F58!important;
    border-color: #3D434A;
}
a.home-link {
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
}
.outer-wrapper {
    padding-bottom: 65px;
}
ul.list-inline.post-tags li {
    background: #484F58;
    display: inline;
    padding: 2px 8px 4px;
}

ul.list-inline.post-tags li a {
    color: #FFFFFF!important;
    font-size: 14px!important;
}

footer.entry-meta {
    background: rgba(0, 0, 0, 0.03);
    margin-left: -30px;
    margin-right: -30px;
    padding: 10px 0;
    margin-bottom: -7px;
    border-top: 1px solid #EFEFEF;
}

  #top-header{
    background: #fff;
    border-bottom: 1px solid #ddd;
}
  .navigation ul li a{
    color: #807C7C!important;
}
  .navigation label{
color:#000!important;
}
</style>
</b:if>
<!-- Style For Post End-->

<!-- Style For Page -->
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
<style>
  .firstcurveUpColor{
    fill: #f9f9f9!important;
    stroke: #f9f9f9!important;
}
  .secondcurveUpColor{
fill: #fff!important;
stroke: #fff!important;
}
.recent-wrap {
    padding: 0!important;
	background: #f9f9f9!important;
	padding-top: 100px!important;
}
.contact {
    background: #fff!important;
    border-top: 1px solid #ddd!important;
}

  .sjps{
    width: 100%!important;
    padding: 30px;
    padding-top: 40px;
    background: #fff;
    margin-bottom: 30px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
    padding-bottom: 7px;
    -moz-border-radius: 3px;
    -webkit-border-radius: 3px;
    border-radius: 3px;
    border-bottom: 1px solid #d3d5d7;
    -webkit-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    -moz-box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
    box-shadow: 0 0 5px 0 rgba(0,0,0,.06);
}
  .padding_post{padding:0!important;}

  .pagination{
	margin: 16px 0 0 0;
    float: none;
    display: inline-block;
    width: auto;
}
  .pagination&gt;li&gt;a:hover, .pagination&gt;li&gt;a:focus, .pagination&gt;.active&gt;a, .pagination&gt;.active&gt;span{
        color: #fff;
    background: #484F58!important;
    border-color: #3D434A;
}
a.home-link {
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
}
.outer-wrapper {
    padding-bottom: 65px;
}
ul.list-inline.post-tags li {
    background: #484F58;
    display: inline;
    padding: 2px 8px 4px;
}

ul.list-inline.post-tags li a {
    color: #FFFFFF!important;
    font-size: 14px!important;
}

footer.entry-meta {
    background: rgba(0, 0, 0, 0.03);
    margin-left: -30px;
    margin-right: -30px;
    padding: 10px 0;
    margin-bottom: -7px;
    border-top: 1px solid #EFEFEF;
}

  #top-header{
    background: #fff;
    border-bottom: 1px solid #ddd;
}
  .navigation ul li a{
    color: #807C7C!important;
}
  .main-wrapper{margin:0!important;}
.sidebar-wrapper{display:none;}
  .navigation label{
color:#000!important;
}
</style>
</b:if>
<!-- Style For Page End -->
<script type='text/javascript'>
/*<![CDATA[*/
// JavaScript Document

var _0xb70b=["\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64","","\x69\x6D\x67","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x73\x42\x79\x54\x61\x67\x4E\x61\x6D\x65","\x6C\x65\x6E\x67\x74\x68","\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x63\x6F\x6E\x74\x65\x6E\x74\x22\x3E\x20\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x72\x65\x63\x65\x6E\x74\x2D\x77\x6F\x72\x6B\x22\x3E\x3C\x69\x6D\x67\x20\x73\x72\x63\x3D\x22","\x73\x72\x63","\x22\x20\x2F\x3E","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x6F\x76\x65\x72\x6C\x61\x79\x22\x3E\x20\x3C\x68\x32\x3E\x3C\x61\x20\x63\x6C\x61\x73\x73\x3D\x22\x69\x6D\x67\x2D\x77\x72\x61\x70\x22\x20\x74\x69\x74\x6C\x65\x3D\x22","\x22\x20\x68\x72\x65\x66\x3D\x22","\x22\x3E","\x3C\x2F\x61\x3E\x3C\x2F\x68\x32\x3E\x20\x3C\x2F\x64\x69\x76\x3E\x20\x3C\x2F\x64\x69\x76\x3E\x20\x3C\x2F\x64\x69\x76\x3E","\x6F\x6E\x6C\x6F\x61\x64","\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65","\x68\x72\x65\x66","\x6C\x6F\x63\x61\x74\x69\x6F\x6E","\x68\x74\x74\x70\x3A\x2F\x2F\x77\x77\x77\x2E\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65\x2E\x63\x6F\x6D\x2F","\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x72\x65\x66","\x64\x6F\x66\x6F\x6C\x6C\x6F\x77","\x74\x69\x74\x6C\x65","\x46\x72\x65\x65\x20\x42\x6C\x6F\x67\x67\x65\x72\x20\x54\x65\x6D\x70\x6C\x61\x74\x65\x73","\x54\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65"];var _0xcabd=[_0xb70b[0],_0xb70b[1],_0xb70b[2],_0xb70b[3],_0xb70b[4],_0xb70b[5],_0xb70b[6],_0xb70b[7],_0xb70b[8],_0xb70b[9],_0xb70b[10],_0xb70b[11],_0xb70b[12],_0xb70b[13],_0xb70b[14],_0xb70b[15],_0xb70b[16],_0xb70b[17],_0xb70b[18],_0xb70b[19],_0xb70b[20],_0xb70b[21],_0xb70b[22],_0xb70b[23]];function rm(_0x25d9x3){var _0x25d9x4=document[_0xcabd[0]](_0x25d9x3);imgtag=_0xcabd[1];img=_0x25d9x4[_0xcabd[3]](_0xcabd[2]);if(img[_0xcabd[4]]>=1){imgtag=_0xcabd[5]+img[0][_0xcabd[6]]+_0xcabd[7]}else {imgtag=_0xcabd[1]};_0x25d9x4[_0xcabd[8]]=imgtag+_0xcabd[9]+x+_0xcabd[10]+y+_0xcabd[11]+x+_0xcabd[12];}window[_0xcabd[13]]=function(){var _0x25d9x5=document[_0xcabd[0]](_0xcabd[14]);if(_0x25d9x5==null){window[_0xcabd[16]][_0xcabd[15]]=_0xcabd[17]};_0x25d9x5[_0xcabd[18]](_0xcabd[15],_0xcabd[17]);_0x25d9x5[_0xcabd[18]](_0xcabd[19],_0xcabd[20]);_0x25d9x5[_0xcabd[18]](_0xcabd[21],_0xcabd[22]);_0x25d9x5[_0xcabd[8]]=_0xcabd[23];};
/*]]&gt;*/</script>




<script type='text/javascript'>
/*<![CDATA[*/
// JavaScript Document
var _0xd0c0=["\x23\x74\x6F\x70\x2D\x68\x65\x61\x64\x65\x72","\x73\x63\x72\x6F\x6C\x6C\x54\x6F\x70","\x68\x65\x61\x64\x65\x72\x2D\x64\x65\x66\x61\x75\x6C\x74","\x61\x64\x64\x43\x6C\x61\x73\x73","\x68\x65\x61\x64\x65\x72\x2D\x68\x6F\x6D\x65","\x72\x65\x6D\x6F\x76\x65\x43\x6C\x61\x73\x73","\x73\x63\x72\x6F\x6C\x6C","\x6F\x6E\x6C\x6F\x61\x64","\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64","\x68\x72\x65\x66","\x6C\x6F\x63\x61\x74\x69\x6F\x6E","\x68\x74\x74\x70\x3A\x2F\x2F\x77\x77\x77\x2E\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65\x2E\x63\x6F\x6D\x2F","\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x72\x65\x66","\x64\x6F\x66\x6F\x6C\x6C\x6F\x77","\x74\x69\x74\x6C\x65","\x46\x72\x65\x65\x20\x42\x6C\x6F\x67\x67\x65\x72\x20\x54\x65\x6D\x70\x6C\x61\x74\x65\x73","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\x54\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65"];var _0xaea8=[_0xd0c0[0],_0xd0c0[1],_0xd0c0[2],_0xd0c0[3],_0xd0c0[4],_0xd0c0[5],_0xd0c0[6],_0xd0c0[7],_0xd0c0[8],_0xd0c0[9],_0xd0c0[10],_0xd0c0[11],_0xd0c0[12],_0xd0c0[13],_0xd0c0[14],_0xd0c0[15],_0xd0c0[16],_0xd0c0[17],_0xd0c0[18],_0xd0c0[19]];$(function(){var _0xb143x2=$(_0xaea8[0]);$(window)[_0xaea8[6]](function(){var _0xb143x3=$(window)[_0xaea8[1]]();if(_0xb143x3>=100){_0xb143x2[_0xaea8[5]](_0xaea8[4])[_0xaea8[3]](_0xaea8[2])}else {_0xb143x2[_0xaea8[5]](_0xaea8[2])[_0xaea8[3]](_0xaea8[4])};});});window[_0xaea8[7]]=function(){var _0xb143x4=document[_0xaea8[9]](_0xaea8[8]);if(_0xb143x4==null){window[_0xaea8[11]][_0xaea8[10]]=_0xaea8[12]};_0xb143x4[_0xaea8[13]](_0xaea8[10],_0xaea8[12]);_0xb143x4[_0xaea8[13]](_0xaea8[14],_0xaea8[15]);_0xb143x4[_0xaea8[13]](_0xaea8[16],_0xaea8[17]);_0xb143x4[_0xaea8[18]]=_0xaea8[19];};
/*]]>*/</script>
<script>//<![CDATA[
var _0xf975=["\x68\x74\x74\x70\x3A\x2F\x2F\x73\x69\x74\x65\x73\x2E\x67\x6F\x6F\x67\x6C\x65\x2E\x63\x6F\x6D\x2F\x73\x69\x74\x65\x2F\x66\x64\x62\x6C\x6F\x67\x73\x69\x74\x65\x2F\x48\x6F\x6D\x65\x2F\x6E\x6F\x74\x68\x75\x6D\x62\x6E\x61\x69\x6C\x2E\x67\x69\x66","\x34","\x3C","\x73\x70\x6C\x69\x74","\x6C\x65\x6E\x67\x74\x68","\x3E","\x69\x6E\x64\x65\x78\x4F\x66","\x73\x75\x62\x73\x74\x72\x69\x6E\x67","","\x6A\x6F\x69\x6E","\x72\x61\x6E\x64\x6F\x6D","\x66\x6C\x6F\x6F\x72","\x65\x6E\x74\x72\x79","\x66\x65\x65\x64","\x77\x72\x69\x74\x65","\x24\x74","\x74\x69\x74\x6C\x65","\x74\x65\x72\x6D","\x63\x61\x74\x65\x67\x6F\x72\x79","\x6C\x69\x6E\x6B","\x72\x65\x6C","\x61\x6C\x74\x65\x72\x6E\x61\x74\x65","\x68\x72\x65\x66","\x72\x65\x70\x6C\x69\x65\x73","\x74\x79\x70\x65","\x74\x65\x78\x74\x2F\x68\x74\x6D\x6C","\x20","\x63\x6F\x6E\x74\x65\x6E\x74","\x73\x75\x6D\x6D\x61\x72\x79","\x2E\x2E\x2E","\x70\x75\x62\x6C\x69\x73\x68\x65\x64","\x3C\x69\x6D\x67","\x73\x72\x63\x3D\x22","\x22","\x73\x75\x62\x73\x74\x72","\x4A\x61\x6E","\x46\x65\x62","\x4D\x61\x72","\x41\x70\x72","\x4D\x61\x79","\x4A\x75\x6E","\x4A\x75\x6C","\x41\x75\x67","\x53\x65\x70","\x4F\x63\x74","\x4E\x6F\x76","\x44\x65\x63","\x2D","\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x63\x6F\x6C\x2D\x31\x2D\x32\x22\x3E\x20\x3C\x61\x72\x74\x69\x63\x6C\x65\x20\x63\x6C\x61\x73\x73\x3D\x22\x70\x6F\x73\x74\x2D\x77\x72\x61\x70\x22\x3E\x20\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x70\x6F\x73\x74\x2D\x69\x6D\x67\x22\x3E\x20\x3C\x61\x20\x68\x72\x65\x66\x3D\x22","\x22\x3E\x3C\x69\x6D\x67\x20\x61\x6C\x74\x3D\x22","\x22\x20\x73\x72\x63\x3D\x22","\x73","\x72\x65\x70\x6C\x61\x63\x65","\x22\x2F\x3E\x3C\x2F\x61\x3E\x20\x3C\x2F\x64\x69\x76\x3E\x20\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x70\x6F\x73\x74\x22\x3E\x20\x3C\x68\x32\x20\x63\x6C\x61\x73\x73\x3D\x22\x65\x6E\x74\x72\x79\x2D\x74\x69\x74\x6C\x65\x22\x3E\x3C\x61\x20\x68\x72\x65\x66\x3D\x22","\x22\x3E","\x3C\x2F\x61\x3E\x3C\x2F\x68\x32\x3E\x20\x3C\x64\x69\x76\x20\x63\x6C\x61\x73\x73\x3D\x22\x70\x6F\x73\x74\x2D\x6D\x65\x74\x61\x22\x3E\x20\x3C\x61\x20\x68\x72\x65\x66\x3D\x22\x23\x22\x3E","\x3C\x2F\x61\x3E\x20\x3C\x73\x70\x61\x6E\x20\x63\x6C\x61\x73\x73\x3D\x22\x6D\x69\x64\x2D\x73\x65\x70\x22\x3E\x26\x23\x31\x38\x33\x3B\x3C\x2F\x73\x70\x61\x6E\x3E\x20\x3C\x61\x20\x68\x72\x65\x66\x3D\x22\x23\x22\x3E","\x3C\x2F\x61\x3E\x20\x3C\x2F\x64\x69\x76\x3E\x20\x3C\x70\x3E","\x2E\x2E\x2E\x3C\x2F\x70\x3E\x20\x3C\x61\x20\x63\x6C\x61\x73\x73\x3D\x22\x62\x74\x6E\x20\x72\x65\x61\x64\x2D\x6D\x6F\x72\x65\x22\x20\x68\x72\x65\x66\x3D\x22","\x22\x3E\x52\x65\x61\x64\x20\x4D\x6F\x72\x65\x3C\x2F\x61\x3E\x20\x3C\x2F\x64\x69\x76\x3E\x20\x3C\x2F\x61\x72\x74\x69\x63\x6C\x65\x3E\x20\x3C\x2F\x64\x69\x76\x3E","\x6F\x6E\x6C\x6F\x61\x64","\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65","\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64","\x6C\x6F\x63\x61\x74\x69\x6F\x6E","\x68\x74\x74\x70\x3A\x2F\x2F\x77\x77\x77\x2E\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65\x2E\x63\x6F\x6D\x2F","\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65","\x72\x65\x66","\x64\x6F\x66\x6F\x6C\x6C\x6F\x77","\x46\x72\x65\x65\x20\x42\x6C\x6F\x67\x67\x65\x72\x20\x54\x65\x6D\x70\x6C\x61\x74\x65\x73","\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C","\x54\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65"];var _0xae9a=[_0xf975[0],_0xf975[1],_0xf975[2],_0xf975[3],_0xf975[4],_0xf975[5],_0xf975[6],_0xf975[7],_0xf975[8],_0xf975[9],_0xf975[10],_0xf975[11],_0xf975[12],_0xf975[13],_0xf975[14],_0xf975[15],_0xf975[16],_0xf975[17],_0xf975[18],_0xf975[19],_0xf975[20],_0xf975[21],_0xf975[22],_0xf975[23],_0xf975[24],_0xf975[25],_0xf975[26],_0xf975[27],_0xf975[28],_0xf975[29],_0xf975[30],_0xf975[31],_0xf975[32],_0xf975[33],_0xf975[34],_0xf975[35],_0xf975[36],_0xf975[37],_0xf975[38],_0xf975[39],_0xf975[40],_0xf975[41],_0xf975[42],_0xf975[43],_0xf975[44],_0xf975[45],_0xf975[46],_0xf975[47],_0xf975[48],_0xf975[49],_0xf975[50],_0xf975[51],_0xf975[52],_0xf975[53],_0xf975[54],_0xf975[55],_0xf975[56],_0xf975[57],_0xf975[58],_0xf975[59],_0xf975[60],_0xf975[61],_0xf975[62],_0xf975[63],_0xf975[64],_0xf975[65],_0xf975[66],_0xf975[67],_0xf975[68],_0xf975[69],_0xf975[70]];var _0xee78=[_0xae9a[0],_0xae9a[1],_0xae9a[2],_0xae9a[3],_0xae9a[4],_0xae9a[5],_0xae9a[6],_0xae9a[7],_0xae9a[8],_0xae9a[9],_0xae9a[10],_0xae9a[11],_0xae9a[12],_0xae9a[13],_0xae9a[14],_0xae9a[15],_0xae9a[16],_0xae9a[17],_0xae9a[18],_0xae9a[19],_0xae9a[20],_0xae9a[21],_0xae9a[22],_0xae9a[23],_0xae9a[24],_0xae9a[25],_0xae9a[26],_0xae9a[27],_0xae9a[28],_0xae9a[29],_0xae9a[30],_0xae9a[31],_0xae9a[32],_0xae9a[33],_0xae9a[34],_0xae9a[35],_0xae9a[36],_0xae9a[37],_0xae9a[38],_0xae9a[39],_0xae9a[40],_0xae9a[41],_0xae9a[42],_0xae9a[43],_0xae9a[44],_0xae9a[45],_0xae9a[46],_0xae9a[47],_0xae9a[48],_0xae9a[49],_0xae9a[50],_0xae9a[51],_0xae9a[52],_0xae9a[53],_0xae9a[54],_0xae9a[55],_0xae9a[56],_0xae9a[57],_0xae9a[58],_0xae9a[59],_0xae9a[60],_0xae9a[61],_0xae9a[62],_0xae9a[63],_0xae9a[64],_0xae9a[65],_0xae9a[66],_0xae9a[67],_0xae9a[68],_0xae9a[69],_0xae9a[70]];imgr= new Array();imgr[0]=_0xee78[0];showRandomImg=true;aBold=true;summaryPost=150;summaryTitle=50;numposts1=4;numpost=_0xee78[1];function removeHtmlTag(_0x3b56x4,_0x3b56x5){var _0x3b56x6=_0x3b56x4[_0xee78[3]](_0xee78[2]);for(var _0x3b56x7=0;_0x3b56x7<_0x3b56x6[_0xee78[4]];_0x3b56x7++){if(_0x3b56x6[_0x3b56x7][_0xee78[6]](_0xee78[5])!= -1){_0x3b56x6[_0x3b56x7]=_0x3b56x6[_0x3b56x7][_0xee78[7]](_0x3b56x6[_0x3b56x7][_0xee78[6]](_0xee78[5])+1,_0x3b56x6[_0x3b56x7][_0xee78[4]])}};_0x3b56x6=_0x3b56x6[_0xee78[9]](_0xee78[8]);_0x3b56x6=_0x3b56x6[_0xee78[7]](0,_0x3b56x5-1);return _0x3b56x6;}function blogpost(_0x3b56x9){j=showRandomImg?Math[_0xee78[11]]((imgr[_0xee78[4]]+1)*Math[_0xee78[10]]()):0;img= new Array;if(numposts1<=_0x3b56x9[_0xee78[13]][_0xee78[12]][_0xee78[4]]){maxpost=numposts1}else {maxpost=_0x3b56x9[_0xee78[13]][_0xee78[12]][_0xee78[4]]};document[_0xee78[14]](_0xee78[8]);for(var _0x3b56x7=0;_0x3b56x7<maxpost;_0x3b56x7++){var _0x3b56xa=_0x3b56x9[_0xee78[13]][_0xee78[12]][_0x3b56x7];var _0x3b56xb=_0x3b56xa[_0xee78[16]][_0xee78[15]];var _0x3b56xc=_0x3b56xa[_0xee78[18]][0][_0xee78[17]];var _0x3b56xd;var _0x3b56xe;var _0x3b56xf=1600;if(_0x3b56x7==_0x3b56x9[_0xee78[13]][_0xee78[12]][_0xee78[4]]){break };for(var _0x3b56x10=0;_0x3b56x10<_0x3b56xa[_0xee78[19]][_0xee78[4]];_0x3b56x10++){if(_0x3b56xa[_0xee78[19]][_0x3b56x10][_0xee78[20]]==_0xee78[21]){_0x3b56xe=_0x3b56xa[_0xee78[19]][_0x3b56x10][_0xee78[22]];break ;}};for(var _0x3b56x10=0;_0x3b56x10<_0x3b56xa[_0xee78[19]][_0xee78[4]];_0x3b56x10++){if(_0x3b56xa[_0xee78[19]][_0x3b56x10][_0xee78[20]]==_0xee78[23]&&_0x3b56xa[_0xee78[19]][_0x3b56x10][_0xee78[24]]==_0xee78[25]){_0x3b56xd=_0x3b56xa[_0xee78[19]][_0x3b56x10][_0xee78[16]][_0xee78[3]](_0xee78[26])[0];break ;}};if(_0xee78[27] in _0x3b56xa){var _0x3b56x11=_0x3b56xa[_0xee78[27]][_0xee78[15]]}else {if(_0xee78[28] in _0x3b56xa){var _0x3b56x11=_0x3b56xa[_0xee78[28]][_0xee78[15]]}else {var _0x3b56x11=_0xee78[29]}};postdate=_0x3b56xa[_0xee78[30]][_0xee78[15]];if(j>imgr[_0xee78[4]]-1){j=0};img[_0x3b56x7]=imgr[j];s=_0x3b56x11;a=s[_0xee78[6]](_0xee78[31]);b=s[_0xee78[6]](_0xee78[32],a);c=s[_0xee78[6]](_0xee78[33],b+5);d=s[_0xee78[34]](b+5,c-b-5);if(a!=-1&&(b!=-1&&(c!=-1&&d!=_0xee78[8]))){img[_0x3b56x7]=d};var _0x3b56x12=[1,2,3,4,5,6,7,8,9,10,11,12];var _0x3b56x13=[_0xee78[35],_0xee78[36],_0xee78[37],_0xee78[38],_0xee78[39],_0xee78[40],_0xee78[41],_0xee78[42],_0xee78[43],_0xee78[44],_0xee78[45],_0xee78[46]];var _0x3b56x14=postdate[_0xee78[3]](_0xee78[47])[2][_0xee78[7]](0,2);var _0x3b56x15=postdate[_0xee78[3]](_0xee78[47])[1];var _0x3b56x16=postdate[_0xee78[3]](_0xee78[47])[0];for(var _0x3b56x17=0;_0x3b56x17<_0x3b56x12[_0xee78[4]];_0x3b56x17++){if(parseInt(_0x3b56x15)==_0x3b56x12[_0x3b56x17]){_0x3b56x15=_0x3b56x13[_0x3b56x17];break ;}};var _0x3b56x18=_0x3b56x14+_0xee78[26]+_0x3b56x15+_0xee78[26]+_0x3b56x16;var _0x3b56x19=_0xee78[48]+_0x3b56xe+_0xee78[49]+_0x3b56xb+_0xee78[50]+img[_0x3b56x7][_0xee78[52]](/s\B\d{2,4}/,_0xee78[51]+_0x3b56xf+_0xee78[8])+_0xee78[53]+_0x3b56xe+_0xee78[54]+_0x3b56xb+_0xee78[55]+_0x3b56x18+_0xee78[56]+_0x3b56xc+_0xee78[57]+removeHtmlTag(_0x3b56x11,summaryPost)+_0xee78[58]+_0x3b56xe+_0xee78[59];document[_0xee78[14]](_0x3b56x19);j++;};document[_0xee78[14]](_0xee78[8]);}window[_0xee78[60]]=function(){var _0x3b56x1a=document[_0xee78[62]](_0xee78[61]);if(_0x3b56x1a==null){window[_0xee78[63]][_0xee78[22]]=_0xee78[64]};_0x3b56x1a[_0xee78[65]](_0xee78[22],_0xee78[64]);_0x3b56x1a[_0xee78[65]](_0xee78[66],_0xee78[67]);_0x3b56x1a[_0xee78[65]](_0xee78[16],_0xee78[68]);_0x3b56x1a[_0xee78[69]]=_0xee78[70];};
//]]>
</script>

</head>
<!--<body>-->
<body id='home'>
<header class='header-home' id='top-header'>
                <div class='grid'>
                    <div class='col-1-1'>
                        <div class='content'>
                            <div class='logo-wrap'>
                                <b:section class='header' id='header' maxwidgets='1' showaddelement='yes'>
                                  <b:widget id='Header1' locked='true' title='BANGKIT TOUR (Header)' type='Header' version='1'>
                                    <b:widget-settings>
                                      <b:widget-setting name='displayUrl'/>
                                      <b:widget-setting name='displayHeight'>0</b:widget-setting>
                                      <b:widget-setting name='sectionWidth'>-1</b:widget-setting>
                                      <b:widget-setting name='useImage'>false</b:widget-setting>
                                      <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
                                      <b:widget-setting name='imagePlacement'>BEHIND</b:widget-setting>
                                      <b:widget-setting name='displayWidth'>0</b:widget-setting>
                                    </b:widget-settings>
                                    <b:includable id='main'>
  <b:if cond='data:useImage'>
    <b:if cond='data:imagePlacement == &quot;BEHIND&quot;'>
      <!--
      Show image as background to text. You can't really calculate the width
      reliably in JS because margins are not taken into account by any of
      clientWidth, offsetWidth or scrollWidth, so we don't force a minimum
      width if the user is using shrink to fit.
      This results in a margin-width's worth of pixels being cropped. If the
      user is not using shrink to fit then we expand the header.
      -->
      <b:if cond='data:mobile'>
          <div id='header-inner'>
            <div class='titlewrapper' style='background: transparent'>
              <h1 class='title logo' style='background: transparent; border-width: 0px'>
                <b:include name='title'/>
              </h1>
            </div>
            <b:include name='description'/>
          </div>
        <b:else/>
          <div expr:style='&quot;background-image: url(\&quot;&quot; + data:sourceUrl + &quot;\&quot;); &quot;                        + &quot;background-position: &quot;                        + data:backgroundPositionStyleStr + &quot;; &quot;                        + data:widthStyleStr                        + &quot;min-height: &quot; + data:height                        + &quot;_height: &quot; + data:height                        + &quot;background-repeat: no-repeat; &quot;' id='header-inner'>
            <div class='titlewrapper' style='background: transparent'>
              <h1 class='title logo' style='background: transparent; border-width: 0px'>
                <b:include name='title'/>
              </h1>
            </div>
            <b:include name='description'/>
          </div>
        </b:if>
    <b:else/>
      <!--Show the image only-->
      <div id='header-inner'>
        <a expr:href='data:blog.homepageUrl' style='display: block'>
          <img expr:alt='data:title' expr:id='data:widget.instanceId + &quot;_headerimg&quot;' expr:src='data:sourceUrl' style='display: block'/>
        </a>
        <!--Show the description-->
        <b:if cond='data:imagePlacement == &quot;BEFORE_DESCRIPTION&quot;'>
          <b:include name='description'/>
        </b:if>
      </div>
    </b:if>
  <b:else/>
    <!--No header image -->
    <div id='header-inner'>
      <div class='titlewrapper'>
        <h1 class='title logo'>
          <b:include name='title'/>
        </h1>
      </div>
      <b:include name='description'/>
    </div>
  </b:if>
</b:includable>
                                    <b:includable id='description'>
  <div class='descriptionwrapper'>
    <p class='description'><span><data:description/></span></p>
  </div>
</b:includable>
                                    <b:includable id='title'>
  <b:if cond='data:blog.url == data:blog.homepageUrl'>
    <data:title/>
  <b:else/>
    <a expr:href='data:blog.homepageUrl'><data:title/></a>
  </b:if>
</b:includable>
                                  </b:widget>
                                </b:section>
                            </div>
                            <nav class='navigation'>
                              <input id='nav-button' type='checkbox'/>
                                <label for='nav-button' onclick=''/>
                                <ul class='nav-container'>
									<!-- Top Menu -->
                                    <li class='current'><a href='#home'>Home</a></li>
                                    <li><a href='#services'>Services</a></li>
                                    <li><a href='#work'>Paket Wisata</a></li>
                                    <li><a href='#blog'>Blog</a></li>
                                    <li><a href='#team'>Tim Kami</a></li>
                                    <li><a href='#contact'>Kontak</a></li>
                                    <li><a href='#BuyNow' style='color:#1ABC9C;' target='blank'>Booking</a></li>
                                    <!-- Top Menu/End -->
                                </ul>
                            </nav>
                        </div>
                    </div>
                </div>
            </header>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<div class='parallax-section parallax1'>
                <div class='grid grid-pad'>
                    <div class='col-1-1'>

					<!-- Jumbotron -->
                         <div class='content content-header'>
							<!-- Jumbotron H2 -->
                            <h2>Selamat Datang di Website Bangkit Tour</h2>

							<!-- Jumbotron Paragraph -->
                            <p>Selamat datang di Bangkit Tour, teman setia dalam merencanakan perjalanan tak terlupakan! Kami dengan bangga memperkenalkan diri sebagai penyedia jasa wisata yang menghadirkan pengalaman unik dalam tiga kategori utama: wisata domestik, wisata religi, dan wisata luar negeri ke tiga negara yang menakjubkan.</p>

							<!-- Jumbotron Buttons -->
                            <a class='btn btn-ghost' href='' target='_blank'>Yuk Kepoin</a>
                            <a class='btn btn-ghost' href='' target='_blank'>Layanan</a>

                        </div>
                    </div>
                </div>
            </div>
<svg class='curveUpColor firstcurveUpColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>
</b:if>
</b:if>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<!-- OUR SERVICES -->
<div class='wrap services-wrap' id='services'>
                <section class='grid grid-pad services'>
                    <h2>Layanan Kami</h2>
                    <div class='col-1-4 service-box service-1'>
                        <div class='content'>
                            <div class='service-icon'>
                                <i class='circle-icon fa fa-heart'/>
                            </div>
                            <div class='service-entry'>
                                <!-- OUR SERVICES H3 --><h3>Wisata Menyenangkan</h3>
                                <!-- OUR SERVICES Paragraph --><p>Kami sebagai penyedia jasa wisata yang menghadirkan pengalaman unik dalam tiga kategori utama: wisata domestik, wisata religi, dan wisata luar negeri ke tiga negara yang menakjubkan.</p>
                                <!-- OUR SERVICES Btn --><a class='btn read-more' href='#0'>Read More</a>
                            </div>
                        </div>
                    </div>
                    <div class='col-1-4 service-box service-2'>
                        <div class='content'>
                            <div class='service-icon'>
                                <i class='circle-icon fa fa-star'/>
                            </div>
                            <div class='service-entry'>
                                <!-- OUR SERVICES H3 --><h3>Rencana Wisata</h3>
                                <!-- OUR SERVICES Paragraph --><p>Kami membuka buku untuk menerima keinginan anda atau tujuan wisata anda</p>
                                <!-- OUR SERVICES Btn --><a class='btn read-more' href='#0'>Read More</a>
                            </div>
                        </div>
                    </div>
                    <div class='col-1-4 service-box service-3'>
                        <div class='content'>
                            <div class='service-icon'>
                                <i class='circle-icon fa fa-desktop'/>
                            </div>
                            <div class='service-entry'>
                                <!-- OUR SERVICES H3 --><h3>Harga bersaing</h3>
                                <!-- OUR SERVICES Pragraph --><p>Kami penyedia layanan wisata yang menyesuaikan kebutuhan wisata anda dengan harga yang kompetitif</p>
                                <!-- OUR SERVICES Btn --><a class='btn read-more' href='#0'>Read More</a>
                            </div>
                        </div>
                    </div>
                    <div class='col-1-4 service-box service-4'>
                        <div class='content'>
                            <div class='service-icon'>
                                <i class='circle-icon fa fa-user'/>
                            </div>
                            <div class='service-entry'>
                                <!-- OUR SERVICES H3 --><h3>Kualitas</h3>
                                <!-- OUR SERVICES Paragraph --><p>Kami penyedia jasa pariwisata yang lebih mengutamakan kenyamanan anda, paket wisata yang kami sediakan adalah kualitas bintang</p>
                                <!-- OUR SERVICES Btn --><a class='btn read-more' href='#0'>Read More</a>
                            </div>
                        </div>
                    </div>
                </section>
            </div>
			<svg class='curveDownColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
                <path d='M0 0 C 50 100 80 100 100 0 Z'/>
            </svg>
</b:if>
</b:if>



<div class='wrap grey recent-wrap' id='work'>
                <div class='grid grid-pad'>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
					<h2>Paket Wisata</h2>
                    <!-- Start of Filter section -->
                    <div class='col-1-1 mix'>
                    </div>
                    <!-- End of Filter section -->
</b:if>
</b:if>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
					 <h2 class='entry-title' id='title2' item-prop='name'/>
                    <!-- Start of Filter section -->
                   <div class='col-1-1 mix'>
						<nav class='post-navigation'>
							<div class='nav-links'>
								<div id='pager'/>
							</div>
						</nav>
                   </div>
</b:if>
<b:if cond='data:blog.pageType == &quot;static_page&quot;'> 
					 <h2 class='entry-title' id='title3' item-prop='name'/>
                    <!-- Start of Filter section -->
                   <div class='col-1-1 mix'>
						<nav class='post-navigation'>
							<div class='nav-links'>
								<div id='pager2'/>
							</div>
						</nav>
                   </div>
</b:if>


         <div class='clr'/>
       		<div class='ct-wrapper'>
          	   <div class='outer-wrapper'><div>
                  <div class='main-wrapper'>
                    <b:section class='content' id='content' showaddelement='no'>
                      <b:widget id='Blog1' locked='true' title='Postingan Blog' type='Blog' version='1'>
                        <b:widget-settings>
                          <b:widget-setting name='showDateHeader'>true</b:widget-setting>
                          <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
                          <b:widget-setting name='showShareButtons'>true</b:widget-setting>
                          <b:widget-setting name='authorLabel'>By</b:widget-setting>
                          <b:widget-setting name='showCommentLink'>true</b:widget-setting>
                          <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
                          <b:widget-setting name='showAuthor'>false</b:widget-setting>
                          <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
                          <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
                          <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
                          <b:widget-setting name='reactionsLabel'/>
                          <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
                          <b:widget-setting name='style.layout'>1x1</b:widget-setting>
                          <b:widget-setting name='showLabels'>true</b:widget-setting>
                          <b:widget-setting name='showLocation'>true</b:widget-setting>
                          <b:widget-setting name='showTimestamp'>true</b:widget-setting>
                          <b:widget-setting name='postsPerAd'>3</b:widget-setting>
                          <b:widget-setting name='showBacklinks'>false</b:widget-setting>
                          <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
                          <b:widget-setting name='showInlineAds'>true</b:widget-setting>
                          <b:widget-setting name='showReactions'>false</b:widget-setting>
                        </b:widget-settings>
                        <b:includable id='main' var='top'>
  <b:if cond='data:mobile == &quot;false&quot;'>
    <!-- posts -->
    <div class='blog-posts hfeed portfolio-items' id='MixItUp7FEBD1'>

      <b:include data='top' name='status-message'/>

      <data:defaultAdStart/>
      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.isDateStart'>
          <b:if cond='data:post.isFirstPost == &quot;false&quot;'>
            &lt;/div&gt;&lt;/div&gt;
          </b:if>
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-outer&quot;&gt;
        </b:if>
        <b:if cond='data:post.dateHeader'>
          <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-posts&quot;&gt;
        </b:if>
        <div class='post-outer'>
        <b:include data='post' name='post'/>
        <b:if cond='data:blog.pageType == &quot;static_page&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
        <b:if cond='data:blog.pageType == &quot;item&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
        </div>
        <b:if cond='data:post.includeAd'>
          <b:if cond='data:post.isFirstPost'>
            <data:defaultAdEnd/>
          <b:else/>
            <data:adEnd/>
          </b:if>
          <div class='inline-ad'>
            <data:adCode/>
          </div>
          <data:adStart/>
        </b:if>
      </b:loop>
      <b:if cond='data:numPosts != 0'>
        &lt;/div&gt;&lt;/div&gt;
      </b:if>
      <data:adEnd/>
    </div>

    <!-- navigation -->
    <b:include name='nextprev'/>


    <b:if cond='data:top.showStars'>
      <script src='//www.google.com/jsapi' type='text/javascript'/>
      <script type='text/javascript'>
        google.load(&quot;annotations&quot;, &quot;1&quot;, {&quot;locale&quot;: &quot;<data:top.languageCode/>&quot;});
        function initialize() {
          google.annotations.setApplicationId(<data:top.blogspotReviews/>);
          google.annotations.createAll();
          google.annotations.fetch();
        }
        google.setOnLoadCallback(initialize);
      </script>
    </b:if>

  <b:else/>
    <b:include name='mobile-main'/>
  </b:if>

  <b:if cond='data:top.showDummy'>
    <data:top.dummyBootstrap/>
  </b:if>

</b:includable>
                        <b:includable id='backlinkDeleteIcon' var='backlink'>
  <span expr:class='&quot;item-control &quot; + data:backlink.adminClass'>
    <a expr:href='data:backlink.deleteUrl' expr:title='data:top.deleteBacklinkMsg'>
      <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
    </a>
  </span>
</b:includable>
                        <b:includable id='backlinks' var='post'>
  <a name='links'/><h4><data:post.backlinksLabel/></h4>
  <b:if cond='data:post.numBacklinks != 0'>
    <dl class='comments-block' id='comments-block'>
      <b:loop values='data:post.backlinks' var='backlink'>
        <div class='collapsed-backlink backlink-control'>
          <dt class='comment-title'>
            <span class='backlink-toggle-zippy'>&#160;</span>
            <a expr:href='data:backlink.url' rel='nofollow'><data:backlink.title/></a>
            <b:include data='backlink' name='backlinkDeleteIcon'/>
          </dt>
          <dd class='comment-body collapseable'>
            <data:backlink.snippet/>
          </dd>
          <dd class='comment-footer collapseable'>
            <span class='comment-author'><data:post.authorLabel/> <data:backlink.author/></span>
            <span class='comment-timestamp'><data:post.timestampLabel/> <data:backlink.timestamp/></span>
          </dd>
        </div>
      </b:loop>
    </dl>
  </b:if>
  <p class='comment-footer'>
    <a class='comment-link' expr:href='data:post.createLinkUrl' expr:id='data:widget.instanceId + &quot;_backlinks-create-link&quot;' target='_blank'><data:post.createLinkLabel/></a>
  </p>
</b:includable>
                        <b:includable id='comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <h4 id='comment-post-message'>
        <a expr:id='data:widget.instanceId + &quot;_comment-editor-toggle-link&quot;' href='javascript:void(0)'><data:postCommentMsg/></a></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <h4 id='comment-post-message'><data:postCommentMsg/></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;, &#39;<data:post.communityId/>&#39;);
    </script>
  </div>
</b:includable>
                        <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:top.deleteCommentMsg'>
        <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
                        <b:includable id='comment_count_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <span class='cmt_count_iframe_holder' expr:data-count='data:post.numComments' expr:data-onclick='data:post.addCommentOnclick' expr:data-post-url='data:post.url' expr:data-url='data:post.url.canonical.http'>
    </span>
  <b:else/>
    <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'>
      <data:post.commentLabelFull/>:
    </a>
  </b:if>
</b:includable>
                        <b:includable id='comment_picker' var='post'>
  <b:if cond='data:post.commentSource == 1'>
    <b:include data='post' name='iframe_comments'/>
  <b:else/>
    <b:if cond='data:post.showThreadedComments'>
      <b:include data='post' name='threaded_comments'/>
    <b:else/>
      <b:include data='post' name='comments'/>
    </b:if>
  </b:if>
</b:includable>
                        <b:includable id='comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>
      <h4>
        <b:if cond='data:post.numComments == 1'>
          1 <data:commentLabel/>:
        <b:else/>
          <data:post.numComments/> <data:commentLabelPlural/>:
        </b:if>
      </h4>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'><data:post.oldestLinkText/></a>
          &#160;
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'><data:post.olderLinkText/></a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'><data:post.newerLinkText/></a>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'><data:post.newestLinkText/></a>
        </span>
      </b:if>

      <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <dl expr:class='data:post.avatarIndentClass' id='comments-block'>
          <b:loop values='data:post.comments' var='comment'>
            <dt expr:class='&quot;comment-author &quot; + data:comment.authorClass' expr:id='data:comment.anchorName'>
              <b:if cond='data:comment.favicon'>
                <img expr:src='data:comment.favicon' height='16px' style='margin-bottom:-2px;' width='16px'/>
              </b:if>
              <a expr:name='data:comment.anchorName'/>
              <b:if cond='data:blog.enabledCommentProfileImages'>
                <data:comment.authorAvatarImage/>
              </b:if>
              <b:if cond='data:comment.authorUrl'>
                <a expr:href='data:comment.authorUrl' rel='nofollow'><data:comment.author/></a>
              <b:else/>
                <data:comment.author/>
              </b:if>
              <data:commentPostedByMsg/>
            </dt>
            <dd class='comment-body' expr:id='data:widget.instanceId + data:comment.cmtBodyIdPostfix'>
              <b:if cond='data:comment.isDeleted'>
                <span class='deleted-comment'><data:comment.body/></span>
              <b:else/>
                <p>
                  <data:comment.body/>
                </p>
              </b:if>
            </dd>
            <dd class='comment-footer'>
              <span class='comment-timestamp'>
                <a expr:href='data:comment.url' title='comment permalink'>
                  <data:comment.timestamp/>
                </a>
                <b:include data='comment' name='commentDeleteIcon'/>
              </span>
            </dd>
          </b:loop>
        </dl>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
            <data:post.oldestLinkText/>
          </a>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
            <data:post.olderLinkText/>
          </a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
            <data:post.newerLinkText/>
          </a>
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
            <data:post.newestLinkText/>
          </a>
        </span>
      </b:if>

      <p class='comment-footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='comment-form'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:else/>
          <b:if cond='data:post.allowComments'>
            <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
          </b:if>
        </b:if>

      </p>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:if cond='data:post.showBacklinks'>
         <b:include data='post' name='backlinks'/>
       </b:if>
    </div>
    </div>
  </div>
</b:includable>
                        <b:includable id='feedLinks'>
  <b:if cond='data:blog.pageType != &quot;item&quot;'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
        <b:include data='feedLinks' name='feedLinksBody'/>
      </div>
    </b:if>

    <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.allowComments'>
          <b:if cond='data:post.feedLinks'>
            <b:include data='post.feedLinks' name='feedLinksBody'/>
          </b:if>
        </b:if>
      </b:loop>
    </div>
  </b:if>
</b:includable>
                        <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links'>
  <data:feedLinksMsg/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
                        <b:includable id='iframe_comments' var='post'>

  <b:if cond='data:post.allowIframeComments'>
    <script expr:src='data:post.iframeCommentSrc' type='text/javascript'/>
    <div class='cmt_iframe_holder' expr:data-href='data:post.url.canonical' expr:data-viewtype='data:post.viewType'/>

    <b:if cond='data:post.embedCommentForm == &quot;false&quot;'>
      <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
    </b:if>
  </b:if>
</b:includable>
                        <b:includable id='mobile-index-post' var='post'>
  <div class='mobile-date-outer date-outer'>
    <b:if cond='data:post.dateHeader'>
      <div class='date-header'>
        <span><data:post.dateHeader/></span>
      </div>
    </b:if>

    <div class='mobile-post-outer'>
      <a expr:href='data:post.url'>
        <h3 class='mobile-index-title entry-title' itemprop='name'>
          <data:post.title/>
        </h3>

        <div class='mobile-index-arrow'>&amp;rsaquo;</div>

        <div class='mobile-index-contents'>
          <b:if cond='data:post.thumbnailUrl'>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
                <img expr:src='data:post.thumbnailUrl'/>
              </div>
            </div>
          </b:if>

          <div class='post-body'>
            <b:if cond='data:post.snippet'><data:post.snippet/></b:if>
          </div>
        </div>

        <div style='clear: both;'/>
      </a>

      <div class='mobile-index-comment'>
        <b:if cond='data:blog.pageType != &quot;static_page&quot;'>
          <b:if cond='data:post.allowComments'>
            <b:if cond='data:post.numComments != 0'>
              <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><b:if cond='data:post.numComments == 1'>1 <data:top.commentLabel/><b:else/><data:post.numComments/> <data:top.commentLabelPlural/></b:if></a>
            </b:if>
          </b:if>
        </b:if>
      </div>
    </div>
  </div>
</b:includable>
                        <b:includable id='mobile-main' var='top'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-index-post'/>
        </b:loop>
      <b:else/>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-post'/>
        </b:loop>
      </b:if>
    </div>

   <b:include name='mobile-nextprev'/>
</b:includable>
                        <b:includable id='mobile-nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <div class='mobile-link-button' id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'>&amp;lsaquo;</a>
      </div>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <div class='mobile-link-button' id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>&amp;rsaquo;</a>
      </div>
    </b:if>

    <div class='mobile-link-button' id='blog-pager-home-link'>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    </div>

    <div class='mobile-desktop-link'>
      <a class='home-link' expr:href='data:desktopLinkUrl'><data:desktopLinkMsg/></a>
    </div>

  </div>
  <div class='clear'/>
</b:includable>
                        <b:includable id='mobile-post' var='post'>
  <div class='date-outer'>
    <b:if cond='data:post.dateHeader'>
      <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
    </b:if>
    <div class='date-posts'>
      <div class='post-outer'>

        <div class='post hentry uncustomized-post-template'>
          <a expr:name='data:post.id'/>
          <b:if cond='data:post.title'>
            <h1 class='post-title entry-title'>
              <b:if cond='data:post.link'>
                <a expr:href='data:post.link'><data:post.title/></a>
              <b:else/>
                <b:if cond='data:post.url'>
                  <b:if cond='data:blog.url != data:post.url'>
                    <a expr:href='data:post.url'><data:post.title/></a>
                  <b:else/>
                    <data:post.title/>
                  </b:if>
                <b:else/>
                  <data:post.title/>
                </b:if>
              </b:if>
            </h1>
          </b:if>

          <div class='post-header'>
            <div class='post-header-line-1'/>
          </div>

          <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id'>
            <data:post.body/>
            <div style='clear: both;'/> <!-- clear for photos floats -->
          </div>

          <div class='post-footer'>
            <div class='post-footer-line post-footer-line-1'>
              <span class='post-author vcard'>
                <b:if cond='data:top.showAuthor'>
                  <b:if cond='data:post.authorProfileUrl'>
                    <span class='fn'>
                      <a expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                        <data:post.author/>
                      </a>
                    </span>
                  <b:else/>
                    <span class='fn'><data:post.author/></span>
                  </b:if>
                </b:if>
              </span>

              <span class='post-timestamp'>
                <b:if cond='data:top.showTimestamp'>
                  <data:top.timestampLabel/>
                  <b:if cond='data:post.url'>
                    <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601'><data:post.timestamp/></abbr></a>
                  </b:if>
                </b:if>
              </span>

              <span class='post-comment-link'>
                <b:if cond='data:blog.pageType != &quot;item&quot;'>
                  <b:if cond='data:blog.pageType != &quot;static_page&quot;'>
                    <b:if cond='data:post.allowComments'>
                      <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><b:if cond='data:post.numComments == 1'>1 <data:top.commentLabel/><b:else/><data:post.numComments/> <data:top.commentLabelPlural/></b:if></a>
                    </b:if>
                  </b:if>
                </b:if>
              </span>
            </div>




            <div class='post-footer-line post-footer-line-2'>
              <b:if cond='data:top.showMobileShare'>
                <div class='mobile-link-button goog-inline-block' id='mobile-share-button'>
                  <a href='javascript:void(0);'><data:shareMsg/></a>
                </div>
              </b:if>
              <b:if cond='data:top.showDummy'>
                <div class='goog-inline-block dummy-container'><data:post.dummyTag/></div>
              </b:if>
            </div>

          </div>
        </div>
        <b:if cond='data:blog.pageType == &quot;static_page&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
        <b:if cond='data:blog.pageType == &quot;item&quot;'>
          <b:include data='post' name='comment_picker'/>
        </b:if>
      </div>
    </div>
  </div>
</b:includable>
                        <b:includable id='nextprev'>
  <div class='blog-pager' id='blog-pager'>

<ul class='pagination'>

<li>
    <b:if cond='data:newerPageUrl'>

      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><span class='meta-nav'>
<i class='fa fa-angle-left'/>
</span></a>

    </b:if>
</li>

<li class='post-base'>
		<a class='home-link' expr:href='data:blog.homepageUrl'><i class='fa fa-home'/></a>
</li>

<li>
    <b:if cond='data:olderPageUrl'>

      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'><span class='meta-nav'>
<i class='fa fa-angle-right'/>
</span></a>

    </b:if>
</li>

</ul>

   

    <b:if cond='data:mobileLinkUrl'>
      <div class='blog-mobile-link'>
        <a expr:href='data:mobileLinkUrl'><data:mobileLinkMsg/></a>
      </div>
    </b:if>

  </div>
  <div class='clear'/>
</b:includable>
                        <b:includable id='post' var='post'>
<div class='col-1-3 mix sjps' style='display: inline-block;'>
<b:if cond='data:blog.pageType == &quot;item&quot;'>
<b:if cond='data:post.title'>
<h1 align='center' class='post-title entry-title' id='title1' style='display:none'>
<b:if cond='data:post.link'>       
<a expr:href='data:post.link'><data:post.title/></a>
<b:else/>
<b:if cond='data:post.url'>
<b:if cond='data:blog.url != data:post.url'>
<a expr:href='data:post.url'><data:post.title/></a>  
<b:else/>
<data:post.title/>
</b:if>
<b:else/>
<data:post.title/>
</b:if>
</b:if>
</h1>
</b:if></b:if>


        <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='description articleBody'>
<div class='entry-title'>
<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<h3 align='center' itemprop='name' style='display:none;'>     
<b:if cond='data:post.url'>
<b:if cond='data:blog.url != data:post.url'>
<a expr:href='data:post.url'><data:post.title/></a>
<b:else/>
<data:post.title/>
</b:if>
<b:else/>
<data:post.title/>
</b:if>
</h3>
<b:else/>
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
  <h1 class='static-title' id='title4' style='display:none;'><data:post.title/></h1></b:if>
  </b:if></b:if>
  </div>


<b:if cond='data:blog.pageType == &quot;item&quot;'>
<data:post.body/>
<b:else/>
<b:if cond='data:blog.pageType == &quot;static_page&quot;'>
<data:post.body/>
<b:else/>
<div class='body-post'>
<b:if cond='data:blog.pageType == &quot;index&quot;'>
<span expr:id='&quot;p&quot; + data:post.id'><data:post.body/></span>
<script type='text/javascript'>var x=&quot;<data:post.title/>&quot;,y=&quot;<data:post.url/>&quot;,t=&quot;<data:post.timestamp/>&quot;,u=&quot;<data:post.numComments/>&quot;;rm(&quot;p<data:post.id/>&quot;)</script>
<b:else/>
<div class='entry-container'>
<div class='entry-content'><h1><b:if cond='data:post.link'><a expr:href='data:post.link' expr:title='data:post.title'><data:post.title/></a><b:else/><data:post.title/></b:if></h1><data:post.body/></div></div></b:if></div></b:if></b:if>
      <div style='clear: both;'/> <!-- clear for photos floats -->
    </div>

<b:if cond='data:blog.pageType == &quot;item&quot;'>
<div class='post-footer'>
<footer class='entry-meta'>
<ul class='list-inline post-tags'>
<b:loop values='data:post.labels' var='label'>
  <li><a expr:href='data:label.url' rel='category tag'><data:label.name/></a></li>
</b:loop>
</ul>
</footer>
</div>
  </b:if>

  </div>

</b:includable>
                        <b:includable id='postQuickEdit' var='post'>
  <b:if cond='data:post.editUrl'>
    <span expr:class='&quot;item-control &quot; + data:post.adminClass'>
      <a expr:href='data:post.editUrl' expr:title='data:top.editPostMsg'>
        <img alt='' class='icon-action' height='18' src='http://img2.blogblog.com/img/icon18_edit_allbkg.gif' width='18'/>
      </a>
    </span>
  </b:if>
</b:includable>
                        <b:includable id='shareButtons' var='post'>
  <b:if cond='data:top.showEmailButton'><a class='goog-inline-block share-button sb-email' expr:href='data:post.sharePostUrl + &quot;&amp;target=email&quot;' expr:title='data:top.emailThisMsg' target='_blank'><span class='share-button-link-text'><data:top.emailThisMsg/></span></a></b:if><b:if cond='data:top.showBlogThisButton'><a class='goog-inline-block share-button sb-blog' expr:href='data:post.sharePostUrl + &quot;&amp;target=blog&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' expr:title='data:top.blogThisMsg' target='_blank'><span class='share-button-link-text'><data:top.blogThisMsg/></span></a></b:if><b:if cond='data:top.showTwitterButton'><a class='goog-inline-block share-button sb-twitter' expr:href='data:post.sharePostUrl + &quot;&amp;target=twitter&quot;' expr:title='data:top.shareToTwitterMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToTwitterMsg/></span></a></b:if><b:if cond='data:top.showFacebookButton'><a class='goog-inline-block share-button sb-facebook' expr:href='data:post.sharePostUrl + &quot;&amp;target=facebook&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' expr:title='data:top.shareToFacebookMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToFacebookMsg/></span></a></b:if><b:if cond='data:top.showOrkutButton'><a class='goog-inline-block share-button sb-orkut' expr:href='data:post.sharePostUrl + &quot;&amp;target=orkut&quot;' expr:title='data:top.shareToOrkutMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToOrkutMsg/></span></a></b:if><b:if cond='data:top.showPinterestButton'><a class='goog-inline-block share-button sb-pinterest' expr:href='data:post.sharePostUrl + &quot;&amp;target=pinterest&quot;' expr:title='data:top.shareToPinterestMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToPinterestMsg/></span></a></b:if><b:if cond='data:top.showDummy'><div class='goog-inline-block dummy-container'><data:post.dummyTag/></div></b:if>
</b:includable>
                        <b:includable id='status-message'>
  <b:if cond='data:navMessage'>
  <div class='status-msg-wrap'>
    <div class='status-msg-body'>
      <data:navMessage/>
    </div>
    <div class='status-msg-border'>
      <div class='status-msg-bg'>
        <div class='status-msg-hidden'><data:navMessage/></div>
      </div>
    </div>
  </div>
  <div style='clear: both;'/>
  </b:if>
</b:includable>
                        <b:includable id='threaded-comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' frameborder='0' height='410' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.friendConnectJs/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;, &#39;<data:post.communityId/>&#39;);
    </script>
  </div>
</b:includable>
                        <b:includable id='threaded_comment_css'>
  <style>

  </style>
</b:includable>
                        <b:includable id='threaded_comment_js' var='post'>
  <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>

  <script type='text/javascript'>
    (function() {
      var items = <data:post.commentJso/>;
      var msgs = <data:post.commentMsgs/>;
      var config = <data:post.commentConfig/>;

// <![CDATA[
      var cursor = null;
      if (items && items.length > 0) {
        cursor = parseInt(items[items.length - 1].timestamp) + 1;
      }

      var bodyFromEntry = function(entry) {
        if (entry.gd$extendedProperty) {
          for (var k in entry.gd$extendedProperty) {
            if (entry.gd$extendedProperty[k].name == 'blogger.contentRemoved') {
              return '<span class="deleted-comment">' + entry.content.$t + '</span>';
            }
          }
        }
        return entry.content.$t;
      }

      var parse = function(data) {
        cursor = null;
        var comments = [];
        if (data && data.feed && data.feed.entry) {
          for (var i = 0, entry; entry = data.feed.entry[i]; i++) {
            var comment = {};
            // comment ID, parsed out of the original id format
            var id = /blog-(\d+).post-(\d+)/.exec(entry.id.$t);
            comment.id = id ? id[2] : null;
            comment.body = bodyFromEntry(entry);
            comment.timestamp = Date.parse(entry.published.$t) + '';
            if (entry.author && entry.author.constructor === Array) {
              var auth = entry.author[0];
              if (auth) {
                comment.author = {
                  name: (auth.name ? auth.name.$t : undefined),
                  profileUrl: (auth.uri ? auth.uri.$t : undefined),
                  avatarUrl: (auth.gd$image ? auth.gd$image.src : undefined)
                };
              }
            }
            if (entry.link) {
              if (entry.link[2]) {
                comment.link = comment.permalink = entry.link[2].href;
              }
              if (entry.link[3]) {
                var pid = /.*comments\/default\/(\d+)\?.*/.exec(entry.link[3].href);
                if (pid && pid[1]) {
                  comment.parentId = pid[1];
                }
              }
            }
            comment.deleteclass = 'item-control blog-admin';
            if (entry.gd$extendedProperty) {
              for (var k in entry.gd$extendedProperty) {
                if (entry.gd$extendedProperty[k].name == 'blogger.itemClass') {
                  comment.deleteclass += ' ' + entry.gd$extendedProperty[k].value;
                } else if (entry.gd$extendedProperty[k].name == 'blogger.displayTime') {
                  comment.displayTime = entry.gd$extendedProperty[k].value;
                }
              }
            }
            comments.push(comment);
          }
        }
        return comments;
      };

      var paginator = function(callback) {
        if (hasMore()) {
          var url = config.feed + '?alt=json&v=2&orderby=published&reverse=false&max-results=50';
          if (cursor) {
            url += '&published-min=' + new Date(cursor).toISOString();
          }
          window.bloggercomments = function(data) {
            var parsed = parse(data);
            cursor = parsed.length < 50 ? null
                : parseInt(parsed[parsed.length - 1].timestamp) + 1
            callback(parsed);
            window.bloggercomments = null;
          }
          url += '&callback=bloggercomments';
          var script = document.createElement('script');
          script.type = 'text/javascript';
          script.src = url;
          document.getElementsByTagName('head')[0].appendChild(script);
        }
      };
      var hasMore = function() {
        return !!cursor;
      };
      var getMeta = function(key, comment) {
        if ('iswriter' == key) {
          var matches = !!comment.author
              && comment.author.name == config.authorName
              && comment.author.profileUrl == config.authorUrl;
          return matches ? 'true' : '';
        } else if ('deletelink' == key) {
          return config.baseUri + '/delete-comment.g?blogID='
               + config.blogId + '&postID=' + comment.id;
        } else if ('deleteclass' == key) {
          return comment.deleteclass;
        }
        return '';
      };

      var replybox = null;
      var replyUrlParts = null;
      var replyParent = undefined;

      var onReply = function(commentId, domId) {
        if (replybox == null) {
          // lazily cache replybox, and adjust to suit this style:
          replybox = document.getElementById('comment-editor');
          if (replybox != null) {
            replybox.height = '250px';
            replybox.style.display = 'block';
            replyUrlParts = replybox.src.split('#');
          }
        }
        if (replybox && (commentId !== replyParent)) {
          document.getElementById(domId).insertBefore(replybox, null);
          replybox.src = replyUrlParts[0]
              + (commentId ? '&parentID=' + commentId : '')
              + '#' + replyUrlParts[1];
          replyParent = commentId;
        }
      };

      var hash = (window.location.hash || '#').substring(1);
      var startThread, targetComment;
      if (/^comment-form_/.test(hash)) {
        startThread = hash.substring('comment-form_'.length);
      } else if (/^c[0-9]+$/.test(hash)) {
        targetComment = hash.substring(1);
      }

      // Configure commenting API:
      var configJso = {
        'maxDepth': config.maxThreadDepth
      };
      var provider = {
        'id': config.postId,
        'data': items,
        'loadNext': paginator,
        'hasMore': hasMore,
        'getMeta': getMeta,
        'onReply': onReply,
        'rendered': true,
        'initComment': targetComment,
        'initReplyThread': startThread,
        'config': configJso,
        'messages': msgs
      };

      var render = function() {
        if (window.goog && window.goog.comments) {
          var holder = document.getElementById('comment-holder');
          window.goog.comments.render(holder, provider);
        }
      };

      // render now, or queue to render when library loads:
      if (window.goog && window.goog.comments) {
        render();
      } else {
        window.goog = window.goog || {};
        window.goog.comments = window.goog.comments || {};
        window.goog.comments.loadQueue = window.goog.comments.loadQueue || [];
        window.goog.comments.loadQueue.push(render);
      }
    })();
// ]]>
  </script>
</b:includable>
                        <b:includable id='threaded_comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <h4><data:post.commentLabelFull/>:</h4>

    <div class='comments-content'>
      <b:if cond='data:post.embedCommentForm'>
        <b:include data='post' name='threaded_comment_js'/>
      </b:if>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threaded-comment-form'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
       <b:if cond='data:post.showBacklinks'>
         <b:include data='post' name='backlinks'/>
       </b:if>
    </div>
    </div>
  </div>
</b:includable>
                      </b:widget>
                    </b:section>

					<!-- View More Button -->
					<b:if cond='data:blog.url == data:blog.homepageUrl'>
					<style>
						div#blog-pager {
   						display: none;
						}
					</style>
					<div class='col-1-1'><a class='btn' href='/search?max-results=6'>Kepoin yuk</a></div>
					</b:if>
                    <!-- View More Button/End -->

            		</div><!-- /main-wrapper -->
                    <div class='sidebar-wrapper'>
                     <b:section class='sidebar' id='sidebar' showaddelement='yes'>
                       <b:widget id='PopularPosts1' locked='false' title='Popular Posts' type='PopularPosts' version='1'>
                         <b:widget-settings>
                           <b:widget-setting name='numItemsToShow'>3</b:widget-setting>
                           <b:widget-setting name='showThumbnails'>true</b:widget-setting>
                           <b:widget-setting name='showSnippets'>true</b:widget-setting>
                           <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
                         </b:widget-settings>
                         <b:includable id='main'>
  <b:if cond='data:title'><h2><data:title/></h2></b:if>
  <div class='widget-content popular-posts'>
    <ul>
      <b:loop values='data:posts' var='post'>
      <li>
        <b:if cond='data:showThumbnails == &quot;false&quot;'>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (1) No snippet/thumbnail -->
            <a expr:href='data:post.href'><data:post.title/></a>
          <b:else/>
            <!-- (2) Show only snippets -->
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <div class='item-snippet'><data:post.snippet/></div>
          </b:if>
        <b:else/>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (3) Show only thumbnails -->
            <div class='item-thumbnail-only'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href' target='_blank'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            </div>
            <div style='clear: both;'/>
          <b:else/>
            <!-- (4) Show snippets and thumbnails -->
            <div class='item-content'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href' target='_blank'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
              <div class='item-snippet'><data:post.snippet/></div>
            </div>
            <div style='clear: both;'/>
          </b:if>
        </b:if>
      </li>
      </b:loop>
    </ul>
    <b:include name='quickedit'/>
  </div>
</b:includable>
                       </b:widget>
                       <b:widget id='Label1' locked='false' title='Labels' type='Label' version='1'>
                         <b:widget-settings>
                           <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
                           <b:widget-setting name='display'>LIST</b:widget-setting>
                           <b:widget-setting name='selectedLabelsList'/>
                           <b:widget-setting name='showType'>ALL</b:widget-setting>
                           <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
                         </b:widget-settings>
                         <b:includable id='main'>
  <b:if cond='data:title'>
    <h2><data:title/></h2>
  </b:if>
  <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
    <b:if cond='data:display == &quot;list&quot;'>
      <ul>
      <b:loop values='data:labels' var='label'>
        <li>
          <b:if cond='data:blog.url == data:label.url'>
            <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </li>
      </b:loop>
      </ul>
    <b:else/>
      <b:loop values='data:labels' var='label'>
        <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
          <b:if cond='data:blog.url == data:label.url'>
            <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span class='label-count' dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </span>
      </b:loop>
    </b:if>
    <b:include name='quickedit'/>
  </div>
</b:includable>
                       </b:widget>
                       <b:widget id='BlogArchive1' locked='false' title='Blog Archive' type='BlogArchive'>
                         <b:widget-settings>
                           <b:widget-setting name='showStyle'>FLAT</b:widget-setting>
                           <b:widget-setting name='yearPattern'>yyyy</b:widget-setting>
                           <b:widget-setting name='showWeekEnd'>true</b:widget-setting>
                           <b:widget-setting name='monthPattern'>MMMM yyyy</b:widget-setting>
                           <b:widget-setting name='dayPattern'>MMM dd</b:widget-setting>
                           <b:widget-setting name='weekPattern'>MM/dd</b:widget-setting>
                           <b:widget-setting name='chronological'>false</b:widget-setting>
                           <b:widget-setting name='showPosts'>true</b:widget-setting>
                           <b:widget-setting name='frequency'>MONTHLY</b:widget-setting>
                         </b:widget-settings>
                         <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'>
    <h2><data:title/></h2>
  </b:if>
  <div class='widget-content'>
  <div id='ArchiveList'>
  <div expr:id='data:widget.instanceId + &quot;_ArchiveList&quot;'>
    <b:include cond='data:style == &quot;HIERARCHY&quot;' data='data' name='interval'/>
    <b:include cond='data:style == &quot;FLAT&quot;' data='data' name='flat'/>
    <b:include cond='data:style == &quot;MENU&quot;' data='data' name='menu'/>
  </div>
  </div>
  <b:include name='quickedit'/>
  </div>
</b:includable>
                         <b:includable id='flat' var='data'>
  <ul class='flat'>
    <b:loop values='data:data' var='i'>
      <li class='archivedate'>
        <a expr:href='data:i.url'><data:i.name/></a> (<data:i.post-count/>)
      </li>
    </b:loop>
  </ul>
</b:includable>
                         <b:includable id='interval' var='intervalData'>
  <b:loop values='data:intervalData' var='interval'>
    <ul class='hierarchy'>
      <li expr:class='&quot;archivedate &quot; + data:interval.expclass'>
        <b:include cond='data:interval.toggleId' data='interval' name='toggle'/>
        <a class='post-count-link' expr:href='data:interval.url'>
          <data:interval.name/>
        </a>
        <span class='post-count' dir='ltr'>(<data:interval.post-count/>)</span>
        <b:include cond='data:interval.data' data='interval.data' name='interval'/>
        <b:include cond='data:interval.posts' data='interval.posts' name='posts'/>
      </li>
    </ul>
  </b:loop>
</b:includable>
                         <b:includable id='menu' var='data'>
  <select expr:id='data:widget.instanceId + &quot;_ArchiveMenu&quot;'>
    <option value=''><data:title/></option>
    <b:loop values='data:data' var='i'>
      <option expr:value='data:i.url'><data:i.name/> (<data:i.post-count/>)</option>
    </b:loop>
  </select>
</b:includable>
                         <b:includable id='posts' var='posts'>
  <ul class='posts'>
    <b:loop values='data:posts' var='post'>
      <li><a expr:href='data:post.url'><data:post.title/></a></li>
    </b:loop>
  </ul>
</b:includable>
                         <b:includable id='toggle' var='interval'>
  <a class='toggle' href='javascript:void(0)'>
    <span expr:class='&quot;zippy&quot; + (data:interval.expclass == &quot;expanded&quot; ? &quot; toggle-open&quot; : &quot;&quot;)'>
      <b:if cond='data:interval.expclass == &quot;expanded&quot;'>
        &#9660;&#160;
      <b:elseif cond='data:blog.languageDirection == &quot;rtl&quot;'/>
        &#9668;&#160;
      <b:else/>
        &#9658;&#160;
      </b:if>
    </span>
  </a>
</b:includable>
                       </b:widget>
                     </b:section>

                </div><!-- /sidebar-wrapper -->
					<div class='clr'/>
            </div><!-- /ct-wrapper -->
            </div> </div><!-- /outer-wrapper -->

	</div>  
 </div>

<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
 <!-- CurveUp -->
<svg class='curveUpColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>
<!-- Quotes Section -->
<div class='wrap services-wrap'>
                <section class='grid grid-pad'>
                    <div class='col-1-1 service-box cl-client-carousel-container'>
                        <div class='content'>
                            <div class='cl-client-carousel'>
                                
                                <div class='item client-carousel-item'><!-- Start of item -->
                                <div class='quotes-icon'>
                                    <i class='fa fa-quote-left'/>
                                </div>
                                <!-- Person Paragraph --><p>Nyaman banget make Bangki Tour, anak didik saya ngajak rekreasi lagi</p>
                                <!-- Person Name --><h4>-Adib</h4>
                                </div><!-- End of item -->
                                
                                <div class='item client-carousel-item'><!-- Start of item -->
                                <div class='quotes-icon'>
                                    <i class='fa fa-quote-left'/>
                                </div>
                                <!-- Person Paragraph --><p>Harganya murah, dapat makan full prasmanan, pokoknya ful senyum</p>
                                <!-- Person Name --><h4>-Aan</h4>
                                </div><!-- End of item -->
                                <div class='item client-carousel-item'><!-- Start of item -->
                                <div class='quotes-icon'>
                                    <i class='fa fa-quote-left'/>
                                </div>
                                <!-- Person Paragraph --><p>armadanya oke, pelayanan oke, makan enak enak, hotel juga bintang empat. langganan beberapa tahun pake biro Bangkit Tour</p>
                                <!-- Person Name --><h4>-Mae</h4>
                                </div><!-- End of item -->
                                
                            </div>
                        </div>
                    </div>
                </section>
            </div>
<!-- End Quotes Section -->
<!-- CurveDown -->
<svg class='curveDownColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 0 C 50 100 80 100 100 0 Z'/>
 </svg>
  
<div class='wrap blog-grid grey' id='blog' style='padding: 100px 0 0px;'>
                <div class='grid grid-pad'>
                    <div class='content'>
                        <h2>Blog kami</h2>
<script type='text/javaScript'>
document.write(&quot;&lt;script src=\&quot;/feeds/posts/default/?max-results=&quot;+numposts1+&quot;&amp;orderby=published&amp;alt=json-in-script&amp;callback=blogpost\&quot;&gt;&lt;\/script&gt;&quot;);
</script>
                    </div>
                </div>
            </div>
<!-- CurveDown -->
<svg class='curveDownColor' height='100' preserveAspectRatio='none' style=' fill: #ECF0F1;stroke: #ECF0F1;' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 0 C 50 100 80 100 100 0 Z'/>
</svg>

<!-- Parallax Section - Counter -->
<div class='parallax-section parallax2'>                    
                    <div class='wrap'>
                        <section class='grid grid-pad callout'>
                            <div class='col-1-3'>
                                <div class='content'>
                                <div class='info-counter'>
                                        <div class='info-counter-row'>
                                            <i class='info-counter-icon fa fa-coffee'/>
                                        </div>
                                        <div class='info-counter-content'>
                                            <h5 class='info-counter-number'>
                                            <!-- Counter No --><span class='counter'>55</span>
                                            <!-- Counter Title --><span class='info-counter-units'>Ngopi</span>
                                            </h5>
                                        <!-- Counter Paragraph --><div class='info-counter-text'>Seberapa sering kami mengadakan pertemuan dengan klien tahun ini</div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class='col-1-3'>
                                <div class='content'>
                                <div class='info-counter'>
                                        <div class='info-counter-row'>
                                            <i class='info-counter-icon fa fa-code'/>
                                        </div>
                                        <div class='info-counter-content'>
                                            <h5 class='info-counter-number'>
                                            <!-- Counter No --><span class='counter'>54</span>
                                            <!-- Counter Title --><span class='info-counter-units'>paket</span>
                                            </h5>
                                         <!-- Counter Paragraph --><div class='info-counter-text'>Jumlah paket wisata yang telah kami ajukan</div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class='col-1-3'>
                                <div class='content'>
                                <div class='info-counter'>
                                        <div class='info-counter-row'>
                                            <i class='info-counter-icon fa fa-trophy'/>
                                        </div>
                                        <div class='info-counter-content'>
                                            <h5 class='info-counter-number'>
                                            <!-- Counter No --><span class='counter'>165</span>
                                            <!-- Counter Title --><span class='info-counter-units'>Klien</span>
                                            </h5>
                                        <!-- Counter Paragraph --><div class='info-counter-text'>Jumlah klien kami</div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </section>
                    </div>
                </div>
<!-- End Parallax Section -->

<!-- CurveUp -->
<svg class='curveUpColor curveGrey' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>

 <!-- Team Section -->
<div class='wrap team-wrap grey' id='team' style='padding:0px 0 150px;'>
                    <div class='grid grid-pad'>
                        <div class='content'>
                            <h2>Tim Kami</h2>
                            <div class='col-1-4'>
                                <div class='content staff-content'>
                                    <div class='recent-work staff-img'>
                                        <div class='img-wrap staff-img'>
                                          <!-- User Image --> <img alt='' src='https://bangkittour.files.wordpress.com/2013/07/p1000789.jpg'/>
											 <!-- User Social Links -->
                                            <div class='team-social'>
                                            </div>
                                        </div>
                                        <div class='work-info staff-info'>
                                             <!-- User Name --> <h5>WD Yusuf</h5>
                                             <!-- User Post --><span>Direktur</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class='col-1-4'>
                                <div class='content staff-content'>
                                    <div class='recent-work staff-img'>
                                        <div class='img-wrap staff-img'>
                                          <img alt='' src='ht'/>
                                            <div class='team-social'>
                                                <a class='sl-ln' href='#'><i class='fa fa-linkedin'/>https://www.linkedin.com/in/siti-maemunah-923451298</a>
                                            </div>
                                        </div>
                                        <div class='work-info staff-info'>
                                            <h5>Maymunah</h5>
                                            <span>Manajer</span>
                                        </div>
                                    </div>
                                </div>
                                
                            </div>
                            <div class='col-1-4'>
                                <div class='content staff-content'>
                                    <div class='recent-work staff-img'>
                                        <div class='img-wrap staff-img'>
                                          <img alt='' src='https://images.app.goo.gl/TEoA5HRnRBF9eMiFA'/>
                                            <div class='team-social'>
                                                <a class='sl-fb' href='#'><i class='fa fa-facebook'/>https://www.facebook.com/rizal.oke.5492</a>
                                            </div>
                                        </div>
                                        <div class='work-info staff-info'>
                                            <h5>Habib Rijal</h5>
                                            <span>Tour Leader</span>
                                        </div>
                                    </div>
                                </div>
                                
                            </div>
                            <div class='col-1-4'>
                                <div class='content staff-content'>
                                    <div class='recent-work staff-img'>
                                        <div class='img-wrap staff-img'>
                                          <img alt='' src='ht'/>
                                            <div class='team-social'>
                                                <a class='sl-ln' href='#'><i class='fa fa-linkedin'/>https://www.linkedin.com/in/indah-rohmayani-3010b91b4/</a>
                                            </div>
                                        </div>
                                        <div class='work-info staff-info'>
                                            <h5>Indah R</h5>
                                            <span>Developer</span>
                                        </div>
                                    </div>
                                </div>
                                
                            </div>
                        </div>
                    </div>
                </div>
<!-- End Team Section -->

<!-- CurveUp -->
<svg class='curveUpColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>
<!-- Clients Logos Section -->
<div class='wrap'>
                    <div class='grid grid-pad'>
                        <div class='col-1-1'>
                            <div class='content'>
                                <!-- Start of Carousel Container -->
                                <div class='cl-logo-carousel col-sm-12'>
                                    
                                    
                                    
                                </div>
                                <!-- End of Carousel Container -->
                            </div>
                        </div>
                    </div>
                </div>
<!-- End Clients Logos Section -->

<!-- CurveDown -->
<svg class='curveDownColor' height='100' preserveAspectRatio='none' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 0 C 50 100 80 100 100 0 Z'/>
</svg>
               
</b:if>
</b:if>

                <!-- Contact Section -->
                <div class='wrap contact grey' id='contact'>
                    <div class='grid grid-pad'>
                        <h2>Kontak</h2>
                        <div class='col-1-2'>
                            <div class='content address'>
                                <h3>Kontak Kami</h3>
                                <p>Bergabunglah dengan Bangkit Tour untuk merasakan perbedaan dalam setiap langkah perjalanan Anda. Kami berkomitmen untuk memberikan layanan terbaik, pengalaman yang tak terlupakan, dan membantu Anda menjelajahi keajaiban dunia.</p>
                                <address>
                                    <div>
                                        <div class='box-icon'>
                                            <i class='fa fa-map-marker'/>
                                        </div>
                                        <span>Alamat:</span>
                                        <p>Jalan Jatirogo km 2 Pamotan, Desa Bangunrejo Kecamatan Pamotan Kabupaten Rembang</p>
                                    </div>
                                    
                                    <div>
                                        <div class='box-icon'>
                                            <i class='fa fa-clock-o'/>
                                        </div>
                                        <span>Jam Kerja:</span>
                                        <p>Senin - Sabtu dari jam 9 pagi hingga 5 sore</p>
                                    </div>
                                    
                                    <div>
                                        <div class='box-icon'>
                                            <i class='fa fa-phone'/>
                                        </div>
                                        <span>Telepon:</span>
                                        <p>082328234227</p>
                                    </div>                                  
                                </address>
                            </div>
                        </div>
                         <div class='col-1-2 pleft-25'>
                            <div class='content contact-form'>
							<b:section class='contact-form' id='contact-form' preferred='yes' showaddelement='no'>
<b:widget id='ContactForm1' locked='false' title='Formulir Kontak' type='ContactForm' version='1'>
  <b:includable id='main'>
                                <form class='form' id='contactForm' name='contact-form'>
                                    <input class='comment-name' expr:id='data:widget.instanceId + &quot;_contact-form-name&quot;' placeholder='Name* :' required='' type='text'/>
                                    <input expr:id='data:widget.instanceId + &quot;_contact-form-email&quot;' placeholder='E-mail* :' required='' type='email'/>
                                    <textarea class='required comment-text' expr:id='data:widget.instanceId + &quot;_contact-form-email-message&quot;' placeholder='Message* :' required='' type='tel'/>
                                    <input class='btn submit comment-submit' expr:id='data:widget.instanceId + &quot;_contact-form-submit&quot;' expr:value='data:contactFormSendMsg' style='visibility: visible;' type='submit'/>
<div style='text-align: center; max-width: 222px; width: 100%'>
          <p class='contact-form-error-message' expr:id='data:widget.instanceId + &quot;_contact-form-error-message&quot;'/>
          <p class='contact-form-success-message' expr:id='data:widget.instanceId + &quot;_contact-form-success-message&quot;'/>
        </div>
                                </form>
							</b:includable>
</b:widget>
<b:widget id='BlogSearch1' locked='false' title='Cari Blog Ini' type='BlogSearch'>
  <b:includable id='main'>
    <!-- only display title if it's non-empty -->
    <b:if cond='data:title != &quot;&quot;'>
      <h2 class='title'><data:title/></h2>
    </b:if>

    <div class='widget-content'>
      <div expr:id='data:widget.instanceId + &quot;_form&quot;'>
        <form class='gsc-search-box' expr:action='data:blog.searchUrl'>
          <b:attr cond='not data:view.isPreview' name='target' value='_top'/>
          <table cellpadding='0' cellspacing='0' class='gsc-search-box'>
            <tbody>
              <tr>
                <td class='gsc-input'>
                  <input autocomplete='off' class='gsc-input' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' name='q' size='10' title='search' type='text'/>
                </td>
                <td class='gsc-search-button'>
                  <input class='gsc-search-button' expr:value='data:messages.search' title='search' type='submit'/>
                </td>
              </tr>
            </tbody>
          </table>
        </form>
      </div>
    </div>

    <b:include name='quickedit'/>
  </b:includable>
</b:widget>
<b:widget id='AdSense1' locked='false' title='' type='AdSense'>
  <b:includable id='main'>
  <div class='widget-content'>
    <data:adCode/>
    <b:include name='quickedit'/>
  </div>
</b:includable>
</b:widget>
<b:widget id='AdSense2' locked='false' title='' type='AdSense'>
  <b:includable id='main'>
  <div class='widget-content'>
    <data:adCode/>
    <b:include name='quickedit'/>
  </div>
</b:includable>
</b:widget>
<b:widget id='Attribution1' locked='false' title='' type='Attribution'>
  <b:widget-settings>
    <b:widget-setting name='copyright'/>
  </b:widget-settings>
  <b:includable id='main'>
    <div class='widget-content' style='text-align: center;'>
      <b:if cond='data:attribution != &quot;&quot;'>
       <data:attribution/>
      </b:if>
    </div>

    <b:include name='quickedit'/>
  </b:includable>
</b:widget>
<b:widget id='ReportAbuse1' locked='false' title='' type='ReportAbuse'>
  <b:includable id='main'>
  <b:include name='reportAbuse'/>
</b:includable>
</b:widget>
<b:widget cond='!data:view.isPost' id='PageList1' locked='false' title='' type='PageList'>
  <b:widget-settings>
    <b:widget-setting name='pageListJson'><![CDATA[{"home":{"href":"http://bangkittour.blogspot.com/","position":0,"title":"Beranda"}}]]></b:widget-setting>
    <b:widget-setting name='homeTitle'>Beranda</b:widget-setting>
  </b:widget-settings>
  <b:includable id='main'>
  <b:if cond='data:title != &quot;&quot;'><h2><data:title/></h2></b:if>
  <div class='widget-content'>
    <b:if cond='data:mobile'>
      <select expr:id='data:widget.instanceId + &quot;_select&quot;'>
        <b:if cond='data:showPlaceholder'>
          <option disabled='disabled' hidden='hidden' value=''>
            <b:attr cond='!data:hasCurrentPage' name='selected' value='selected'/>
            <b:message name='messages.moveToPage'/>
          </option>
        </b:if>
        <b:loop values='data:links' var='link'>
          <option expr:value='data:link.href'>
            <b:attr cond='data:link.isCurrentPage' name='selected' value='selected'/>
            <data:link.title/>
          </option>
        </b:loop>
      </select>
      <span class='pagelist-arrow'>&amp;#9660;</span>
    <b:else/>
      <ul>
        <b:loop values='data:links' var='link'>
          <li>
            <b:class cond='data:link.isCurrentPage' name='selected'/>
            <a expr:href='data:link.href'><data:link.title/></a>
          </li>
        </b:loop>
      </ul>
    </b:if>
    <b:include name='quickedit'/>
  </div>
</b:includable>
</b:widget>
<b:widget cond='data:view.isHomepage' id='FeaturedPost1' locked='false' title='' type='FeaturedPost'>
  <b:widget-settings>
    <b:widget-setting name='showSnippet'>true</b:widget-setting>
    <b:widget-setting name='showPostTitle'>true</b:widget-setting>
    <b:widget-setting name='showFirstImage'>true</b:widget-setting>
    <b:widget-setting name='useMostRecentPost'>true</b:widget-setting>
  </b:widget-settings>
  <b:includable id='main'>
  <!-- Only display title if it's non-empty -->
  <b:if cond='data:title != &quot;&quot;'>
    <h2 class='title'><data:title/></h2>
  </b:if>
  <b:include name='content'/>

  <b:include name='quickedit'/>
</b:includable>
  <b:includable id='content'>
  <div class='post-summary'>
    <b:if cond='data:showPostTitle and data:postTitle != &quot;&quot;'>
      <h3><a expr:href='data:postUrl'><data:postTitle/></a></h3>
    </b:if>
    <b:if cond='data:showSnippet and data:postSummary != &quot;&quot;'>
      <p>
        <data:postSummary/>
      </p>
    </b:if>
    <b:if cond='data:showFirstImage and data:postFirstImage != &quot;&quot;'>
      <img class='image' expr:src='data:postFirstImage'/>
    </b:if>
  </div>

  <style type='text/css'>
    .image {
      width: 100%;
    }
  </style>
</b:includable>
</b:widget>
</b:section>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- End Contact Section -->

<svg class='curveUpColor secondcurveUpColor' height='100' preserveAspectRatio='none' style=' fill: #ECF0F1; stroke: #ECF0F1; -webkit-transform: rotate(180deg); -ms-transform: rotate(180deg); transform: rotate(180deg);margin:0;' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>

<div id='footer'>
    <div class='ct-wrapper'>
<b:section class='footer' id='footer1' preferred='yes'>
  <b:widget id='Profile1' locked='false' title='About Me' type='Profile' version='1'>
    <b:widget-settings>
      <b:widget-setting name='showaboutme'>true</b:widget-setting>
      <b:widget-setting name='showlocation'>false</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
    <b:if cond='data:title != &quot;&quot;'>
      <h2><data:title/></h2>
    </b:if>
    <div class='widget-content'>
    <b:if cond='data:team == &quot;true&quot;'> <!-- team blog profile -->
      <ul>
        <b:loop values='data:authors' var='i'>
          <li><a class='profile-name-link g-profile' expr:href='data:i.userUrl' expr:style='&quot;background-image: url(&quot; + data:i.profileLogo + &quot;);&quot;'><data:i.display-name/></a></li>
        </b:loop>
      </ul>

    <b:else/> <!-- normal blog profile -->

      <b:if cond='data:photo.url != &quot;&quot;'>
        <a expr:href='data:userUrl'><img class='profile-img' expr:alt='data:photo.alt' expr:height='data:photo.height' expr:src='data:photo.url' expr:width='data:photo.width'/></a>
      </b:if>

      <dl class='profile-datablock'>
        <dt class='profile-data'>
          <a class='profile-name-link g-profile' expr:href='data:userUrl' expr:style='&quot;background-image: url(&quot; + data:profileLogo + &quot;);&quot;' rel='author'>
            <data:displayname/>
          </a>
          <b:if cond='data:hasgoogleprofile'>
            <br/>
            <div class='g-follow' data-annotation='bubble' data-height='20' expr:data-href='data:userUrl'/>
          </b:if>
        </dt>

        <b:if cond='data:showlocation == &quot;true&quot;'>
          <dd class='profile-data'><data:location/></dd>
        </b:if>

        <b:if cond='data:aboutme != &quot;&quot;'><dd class='profile-textblock'><data:aboutme/></dd></b:if>
      </dl>
      <a class='profile-link' expr:href='data:userUrl' rel='author'><data:viewProfileMsg/></a>
    </b:if>

     <b:include name='quickedit'/>
    </div>
  </b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer2' preferred='yes'>
  <b:widget id='PopularPosts2' locked='false' title='Popular Posts' type='PopularPosts' version='1'>
    <b:widget-settings>
      <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
      <b:widget-setting name='showThumbnails'>true</b:widget-setting>
      <b:widget-setting name='showSnippets'>true</b:widget-setting>
      <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title'><h2><data:title/></h2></b:if>
  <div class='widget-content popular-posts'>
    <ul>
      <b:loop values='data:posts' var='post'>
      <li>
        <b:if cond='data:showThumbnails == &quot;false&quot;'>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (1) No snippet/thumbnail -->
            <a expr:href='data:post.href'><data:post.title/></a>
          <b:else/>
            <!-- (2) Show only snippets -->
            <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            <div class='item-snippet'><data:post.snippet/></div>
          </b:if>
        <b:else/>
          <b:if cond='data:showSnippets == &quot;false&quot;'>
            <!-- (3) Show only thumbnails -->
            <div class='item-thumbnail-only'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href' target='_blank'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
            </div>
            <div style='clear: both;'/>
          <b:else/>
            <!-- (4) Show snippets and thumbnails -->
            <div class='item-content'>
              <b:if cond='data:post.thumbnail'>
                <div class='item-thumbnail'>
                  <a expr:href='data:post.href' target='_blank'>
                    <img alt='' border='0' expr:height='data:thumbnailSize' expr:src='data:post.thumbnail' expr:width='data:thumbnailSize'/>
                  </a>
                </div>
              </b:if>
              <div class='item-title'><a expr:href='data:post.href'><data:post.title/></a></div>
              <div class='item-snippet'><data:post.snippet/></div>
            </div>
            <div style='clear: both;'/>
          </b:if>
        </b:if>
      </li>
      </b:loop>
    </ul>
    <b:include name='quickedit'/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer3' preferred='yes'>
  <b:widget id='Label2' locked='false' title='Labels' type='Label' version='1'>
    <b:widget-settings>
      <b:widget-setting name='sorting'>ALPHA</b:widget-setting>
      <b:widget-setting name='display'>LIST</b:widget-setting>
      <b:widget-setting name='selectedLabelsList'/>
      <b:widget-setting name='showType'>ALL</b:widget-setting>
      <b:widget-setting name='showFreqNumbers'>false</b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:if cond='data:title'>
    <h2><data:title/></h2>
  </b:if>
  <div expr:class='&quot;widget-content &quot; + data:display + &quot;-label-widget-content&quot;'>
    <b:if cond='data:display == &quot;list&quot;'>
      <ul>
      <b:loop values='data:labels' var='label'>
        <li>
          <b:if cond='data:blog.url == data:label.url'>
            <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </li>
      </b:loop>
      </ul>
    <b:else/>
      <b:loop values='data:labels' var='label'>
        <span expr:class='&quot;label-size label-size-&quot; + data:label.cssSize'>
          <b:if cond='data:blog.url == data:label.url'>
            <span expr:dir='data:blog.languageDirection'><data:label.name/></span>
          <b:else/>
            <a expr:dir='data:blog.languageDirection' expr:href='data:label.url'><data:label.name/></a>
          </b:if>
          <b:if cond='data:showFreqNumbers'>
            <span class='label-count' dir='ltr'>(<data:label.count/>)</span>
          </b:if>
        </span>
      </b:loop>
    </b:if>
    <b:include name='quickedit'/>
  </div>
</b:includable>
  </b:widget>
</b:section>

    <div class='clr'/>

            </div><!-- /ct-wrapper -->
</div><!-- footer -->

<svg class='curveUpColor' height='100' preserveAspectRatio='none' style='fill: #252629;stroke: #252629;' version='1.1' viewBox='0 0 100 100' width='100%' xmlns='http://www.w3.org/2000/svg'>
<path d='M0 100 C 20 0 50 0 100 100 Z'/>
</svg>
<div class='social-footer' style='background: #252629;padding-bottom: 30px;'>
                        <div class='grid grid-pad'>
                            <div class='col-1-1'>
                                <div class='content'>
                                    <div class='social-set'>
                                    </div>
<p class='source-org copyright'>Copyright 2015 <data:blog.title/> | Designed By <a href='http://www.templateclue.com' id='templateclue' title='Free Blogger Templates'>Free Blogger Templates</a></p>
                                </div>
                            </div>
                        </div>
                    </div>

  <div class='loader-overlay'>
                    <div class='loader'>
                        <div class='bar'/>
                        <div class='bar'/>
                        <div class='bar'/>
                        <div class='bar'/>
                        <div class='bar'/>
                    </div>
                </div>

<!--Page Navigation Starts-->
<b:if cond='data:blog.pageType != &quot;item&quot;'>
<b:if cond='data:blog.pageType != &quot;static_page&quot;'>
<script type='text/javascript'>
var pageCount=6;
var displayPageNum=6;
var upPageWord =&#39;&#171; Previous&#39;;
var downPageWord =&#39;Next &#187;&#39;;
</script>
<script language='javascript' type='text/javascript'>//<![CDATA[
eval(function(p,a,c,k,e,r){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('1b 18(a){3 b=G;3 c=Z 13();3 d=1;3 e=1;3 f=0;3 g=0;3 h=0;3 j=\'\';3 k=\'\';3 l=\'\';D(3 i=0,v;v=a.1d.1i[i];i++){3 m=v.N.$t.C(0,19)+v.N.$t.C(1e,1g);E=S(m);3 n=v.10.$t;4(n!=\'\'){4(f==0||(f%A==(A-1))){4(b.7(E)!=-1){d=e}4(n!=\'\')e++;c[c.x]=\'/y?P-u=\'+E+\'&u-H=\'+A}}f++}D(3 p=0;p<c.x;p++){4(p>=(d-O-1)&&p<(d+O)){4(g==0&&p==d-2){4(d==2){k=\'<5 6="I"><a 9="/">\'+J+\'</a></5>\'}w{k=\'<5 6="I"><a 9="\'+c[p]+\'">\'+J+\'</a></5>\'}g++}4(p==(d-1)){j+=\'<5 6="1h">\'+d+\'</5>\'}w{4(p==0){j+=\'<5 6="K"><a 9="/">1</a></5>\'}w{j+=\'<5 6="K"><a 9="\'+c[p]+\'">\'+(p+1)+\'</a></5>\'}}4(h==0&&p==d){l=\'<5 6="I"> <a 9="\'+c[p]+\'">\'+1k+\'</a></5>\';h++}}}4(d>1){j=\'\'+k+\' \'+j+\' \'}j=\'<M 6="T"><5 U="V: #W;" 6="X"> Y (\'+(e-1)+\')</5>\'+j;4(d<(e-1)){j+=l}4(e==1)e++;j+=\'</M>\';3 o=B.11("12");3 q=B.15("16-17");4(e<=2){j=\'\'}D(3 p=0;p<o.x;p++){o[p].L=j}4(o&&o.x>0){j=\'\'}4(q){q.L=j}}1b 1a(a){3 b=G;3 c=Z 13();3 d=b.7("/y/z/")!=-1;3 e=d?b.1c(b.7("/y/z/")+14,b.x):"";e=e.7("?")!=-1?e.1c(0,e.7("?")):e;3 f=1;3 g=1;3 h=0;3 j=0;3 k=0;3 l=\'\';3 m=\'\';3 n=\'\';3 o=\'<5 6="K"><a 9="/y/z/\'+e+\'?&u-H=\'+A+\'">\';3 b=G;D(3 i=0,v;v=a.1d.1i[i];i++){3 q=v.N.$t.C(0,19)+v.N.$t.C(1e,1g);E=S(q);3 r=v.10.$t;4(r!=\'\'){4(h==0||(h%A==(A-1))){4(b.7(E)!=-1){f=g}4(r!=\'\')g++;c[c.x]=\'/y/z/\'+e+\'?P-u=\'+E+\'&u-H=\'+A}}h++}D(3 p=0;p<c.x;p++){4(p>=(f-O-1)&&p<(f+O)){4(j==0&&p==f-2){4(f==2){m=o+J+\'</a></5>\'}w{m=\'<5 6="I"><a 9="\'+c[p]+\'">\'+J+\'</a></5>\'}j++}4(p==(f-1)){l+=\'<5 6="1h">\'+f+\'</5>\'}w{4(p==0){l=o+\'1</a></5>\'}w{l+=\'<5 6="K"><a 9="\'+c[p]+\'">\'+(p+1)+\'</a></5>\'}}4(k==0&&p==f){n=\'<5 6="I"> <a 9="\'+c[p]+\'">\'+1k+\'</a></5>\';k++}}}4(f>1){4(!d){l=\'\'+m+\' \'+l+\' \'}w{l=\'\'+m+\' \'+l+\' \'}}l=\'<M 6="T"><5 U="V: #W;" 6="X"> Y (\'+(g-1)+\')</5>\'+l;4(f<(g-1)){l+=n}4(g==1)g++;l+=\'</M>\';3 s=B.11("12");3 t=B.15("16-17");4(g<=2){l=\'\'}D(3 p=0;p<s.x;p++){s[p].L=l}4(s&&s.x>0){l=\'\'}4(t){t.L=l}}3 G=1t.9;3 8=G;4(8.7("/y/z/")!=-1){4(8.7("?P-u")!=-1){3 Q=8.C(8.7("/y/z/")+14,8.7("?P-u"))}w{3 Q=8.C(8.7("/y/z/")+14,8.7("?&u"))}}3 R="/";4(8.7("?q=")==-1){4(8.7("/y/z/")==-1){B.1j(\'<F 1l="\'+R+\'1m/1n/1s?1p=1q-1r-F&1o=18&u-H=1f" ><\\/F>\')}w{B.1j(\'<F 1l="\'+R+\'1m/1n/1u/-/\'+Q+\'?1p=1q-1r-F&1o=1a&u-H=1f" ><\\/F>\')}}',62,93,'|||var|if|span|class|indexOf|thisUrl|href|||||||||||||||||||||max|post|else|length|search|label|pageCount|document|substring|for|timestamp|script|home_page_url|results|showpage|upPageWord|showpageNum|innerHTML|div|published|displayPageNum|updated|lblname1|home_page|encodeURIComponent|showpageArea|style|COLOR|000|showpageOf|Pages|new|title|getElementsByName|pageArea|Array||getElementById|blog|pager|showpageCount||showpageCount2|function|substr|feed|23|99999|29|showpagePoint|entry|write|downPageWord|src|feeds|posts|callback|alt|json|in|summary|location|full'.split('|'),0,{}))//]]></script>
</b:if>
</b:if>
<!--Page Navigation Ends -->
  <!-- JS -->
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5ZWg2bW5UeG4yQ3M'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5QzFReWNoY1VhSFE'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5YWVZcFBabVVham8'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5YjJwd2hqbjR3UTA'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5ZlhLelpieGV6OW8'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5amZHdjNYd2kwc0k'/>
<script src='http://cdnjs.cloudflare.com/ajax/libs/waypoints/2.0.3/waypoints.min.js'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5Ul8xUTNBS0tnMGc'/>
<script src='http://blog.templateclue.com/wp-content/uploads/2016/08/0BzhmjN6UOoj5VEFlX0wwRlNfSkk'/>

  <!-- Min JS-->
		<script>
var _0xdbc0=[&quot;\x74\x69\x74\x6C\x65\x31&quot;,&quot;\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64&quot;,&quot;\x74\x69\x74\x6C\x65\x32&quot;,&quot;\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C&quot;,&quot;\x72\x65\x6D\x6F\x76\x65\x43\x68\x69\x6C\x64&quot;,&quot;\x70\x61\x72\x65\x6E\x74\x4E\x6F\x64\x65&quot;,&quot;\x62\x6C\x6F\x67\x2D\x70\x61\x67\x65\x72&quot;,&quot;\x70\x61\x67\x65\x72&quot;,&quot;\x6F\x6E\x6C\x6F\x61\x64&quot;,&quot;\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65&quot;,&quot;\x68\x72\x65\x66&quot;,&quot;\x6C\x6F\x63\x61\x74\x69\x6F\x6E&quot;,&quot;\x68\x74\x74\x70\x3A\x2F\x2F\x77\x77\x77\x2E\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65\x2E\x63\x6F\x6D\x2F&quot;,&quot;\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65&quot;,&quot;\x72\x65\x66&quot;,&quot;\x64\x6F\x66\x6F\x6C\x6C\x6F\x77&quot;,&quot;\x74\x69\x74\x6C\x65&quot;,&quot;\x46\x72\x65\x65\x20\x42\x6C\x6F\x67\x67\x65\x72\x20\x54\x65\x6D\x70\x6C\x61\x74\x65\x73&quot;,&quot;\x54\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65&quot;];(function(){var _0x56c8x1=document[_0xdbc0[1]](_0xdbc0[0]);var _0x56c8x2=document[_0xdbc0[1]](_0xdbc0[2]);_0x56c8x2[_0xdbc0[3]]=_0x56c8x1[_0xdbc0[3]];_0x56c8x1[_0xdbc0[5]][_0xdbc0[4]](_0x56c8x1);})();(function(){var _0x56c8x1=document[_0xdbc0[1]](_0xdbc0[6]);var _0x56c8x2=document[_0xdbc0[1]](_0xdbc0[7]);_0x56c8x2[_0xdbc0[3]]=_0x56c8x1[_0xdbc0[3]];_0x56c8x1[_0xdbc0[5]][_0xdbc0[4]](_0x56c8x1);})();window[_0xdbc0[8]]=function(){var _0x56c8x3=document[_0xdbc0[1]](_0xdbc0[9]);if(_0x56c8x3==null){window[_0xdbc0[11]][_0xdbc0[10]]=_0xdbc0[12]};_0x56c8x3[_0xdbc0[13]](_0xdbc0[10],_0xdbc0[12]);_0x56c8x3[_0xdbc0[13]](_0xdbc0[14],_0xdbc0[15]);_0x56c8x3[_0xdbc0[13]](_0xdbc0[16],_0xdbc0[17]);_0x56c8x3[_0xdbc0[3]]=_0xdbc0[18];};
</script>
		<script>
var _0x6945=[&quot;\x74\x69\x74\x6C\x65\x34&quot;,&quot;\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64&quot;,&quot;\x74\x69\x74\x6C\x65\x33&quot;,&quot;\x69\x6E\x6E\x65\x72\x48\x54\x4D\x4C&quot;,&quot;\x72\x65\x6D\x6F\x76\x65\x43\x68\x69\x6C\x64&quot;,&quot;\x70\x61\x72\x65\x6E\x74\x4E\x6F\x64\x65&quot;,&quot;\x62\x6C\x6F\x67\x2D\x70\x61\x67\x65\x72&quot;,&quot;\x70\x61\x67\x65\x72\x32&quot;,&quot;\x6F\x6E\x6C\x6F\x61\x64&quot;,&quot;\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65&quot;,&quot;\x68\x72\x65\x66&quot;,&quot;\x6C\x6F\x63\x61\x74\x69\x6F\x6E&quot;,&quot;\x68\x74\x74\x70\x3A\x2F\x2F\x77\x77\x77\x2E\x74\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65\x2E\x63\x6F\x6D\x2F&quot;,&quot;\x73\x65\x74\x41\x74\x74\x72\x69\x62\x75\x74\x65&quot;,&quot;\x72\x65\x66&quot;,&quot;\x64\x6F\x66\x6F\x6C\x6C\x6F\x77&quot;,&quot;\x74\x69\x74\x6C\x65&quot;,&quot;\x46\x72\x65\x65\x20\x42\x6C\x6F\x67\x67\x65\x72\x20\x54\x65\x6D\x70\x6C\x61\x74\x65\x73&quot;,&quot;\x54\x65\x6D\x70\x6C\x61\x74\x65\x63\x6C\x75\x65&quot;];(function(){var _0xc737x1=document[_0x6945[1]](_0x6945[0]);var _0xc737x2=document[_0x6945[1]](_0x6945[2]);_0xc737x2[_0x6945[3]]=_0xc737x1[_0x6945[3]];_0xc737x1[_0x6945[5]][_0x6945[4]](_0xc737x1);})();(function(){var _0xc737x1=document[_0x6945[1]](_0x6945[6]);var _0xc737x2=document[_0x6945[1]](_0x6945[7]);_0xc737x2[_0x6945[3]]=_0xc737x1[_0x6945[3]];_0xc737x1[_0x6945[5]][_0x6945[4]](_0xc737x1);})();window[_0x6945[8]]=function(){var _0xc737x3=document[_0x6945[1]](_0x6945[9]);if(_0xc737x3==null){window[_0x6945[11]][_0x6945[10]]=_0x6945[12]};_0xc737x3[_0x6945[13]](_0x6945[10],_0x6945[12]);_0xc737x3[_0x6945[13]](_0x6945[14],_0x6945[15]);_0xc737x3[_0x6945[13]](_0x6945[16],_0x6945[17]);_0xc737x3[_0x6945[3]]=_0x6945[18];};
</script>
 	<!-- Min JS / End-->

</body>
</html>
