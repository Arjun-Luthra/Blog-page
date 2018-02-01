<!DOCTYPE html> 
<html> 
<!-- The following code has been developed by students and/or researchers of the Freshman Research Initiative DIY Diagnostics Stream at The University of Texas at Austin.  This code is shared for demonstration purposes and should not be considered a product -- it is for entertainment purposes only.  Any user of this code does so at their own risk. Members of the DIY Stream, FRI, and The University of Texas system are not liable for anything related to this code.
 
THIS CODE SHOULD NOT BE USED TO DIAGNOSE ANY KIND OF MEDICAL CONDITION.
 
 
Authors in chronological order of contribution:
Tim Riedel
Arjun Luthra
 
Further Information:
http://cns.utexas.edu/fri
 
Research Educator:
Timothy Riedel
triedel@utexas.edu
 
Brief Description of Goal of Code:
Goal of the code is allow students to learn how to create a web app using HTML and Javascript language
 
Known Issues:Initially struggled with outputting results, but identified need of semicolon in Javascript portion
-->

   <head> 
      <title>Cold or Allergy</title>  
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <meta name="apple-mobile-web-app-capable" content="yes">
      <link rel="stylesheet" href="https://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.css" />
      <script src="https://code.jquery.com/jquery-1.11.1.min.js"></script>
      <script src="https://code.jquery.com/mobile/1.4.5/jquery.mobile-1.4.5.min.js"></script>
	<script>
		//Add variables allergy_count and cold_count//
		var	allergy_count	=	0;
		var	cold_count	=	0;
		//Create function allergyAdd()//
		//Created function coldAdd()//
		function allergyAdd()
			{allergy_count= allergy_count+1;
		}
		function coldAdd()
			{cold_count=cold_count+1;
		}
		//Created function results()//
		//Developed var resultText so it outputs results from question reponse//
		//Created function mathematical calculations to help determine percentage of allergy and percentage of cold based off question responses//
		function results(){
			  var	resultText= document.getElementById("results");
			  var allergyPercent = (allergy_count)/(allergy_count +cold_count)*100;
			  var coldPercent =(cold_count)/(allergy_count + cold_count)*100;
			 resultText.innerHTML="Probability it is allergies="+allergyPercent+"<br>Probability it	is a cold="+coldPercent;
		}
					    
	</script>
	   
	
   </head> 
   
   
	<!--Created mobile page one-->
     <div data-role="pageone">
	<div data-role="header">
		<!-- Changed header from "Hello World" to "Cold or Allergy" -->
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<!--Added content-->
	<div data-role="content">	
		<!--Changed content to "This App is design to help you figure out whether you have a cold or allergy"-->
		<p>This App is design to help you figure out whether you have a cold or allergy.</p>
		<!--Added button "Go to Page Two"-->
		<a href="#pagetwo"data-role="button">Start Diagnostic</a>
	</div><!-- /content -->
	<div data-role="footer" data-position="fixed">
		<p>This is the footer!</p>
		<!--Kept "This is footer"-->	
	</div><!-- /footer -->
     </div>
	  
   
  

<!--Created mobile page two-->
<div data-role="page"id="pagetwo">
	<!--Added header to Page Two-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<!--Added content-->
	<div data-role="content">
		<!--Added content "Are your eyes watery or itchy?" to Page Two-->
		<!--Added style color blue to question-->
		<p style="color:blue">Are your eyes watery or itchy?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to page three-->
		<!--Added onlick="allergyAdd()" to signify the yes response button correlates to allergy-->
		<!--Added onclick="coldAdd()" to signify the no response button correlates to cold-->
		<a href="#pagethree"onclick="allergyAdd();"data-role="button">Yes</a>
		<a href="#pagethree"onclick="coldAdd();"data-role="button">No</a>
	</div><!--content-->
	</div>

<!--Created mobile page three-->
<div data-role="page"id="pagethree">
	<!--Added header to Page Three-->
		<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->

	<div	data-role="content">
		<!--Added content "Do you have a fever?" to Page Three-->
		<!--Added style color blue to question-->
		<p style="color:blue">Do you have a fever?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to shoot page four-->
		<!--Added onlick="allergyAdd()" to signify the no response button correlates to allergy-->
		<!--Added onclick="coldAdd()" to signify the yes response button correlates to cold-->
		<a	href="#pagefour"onclick="coldAdd();"data-role="button">Yes</a>
		<a	href="#pagefour"onclick="allergyAdd();"	data-role="button">No</a>
	</div><!-- /content	-->
</div>
	
<!--Created mobile page four-->
<div data-role="page"id="pagefour">
	<!--Added header to Page Four-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<div	data-role="content">
		<!--Added content "Do you have a sore throat?" to Page Four-->
		<!--Added style color blue to question-->
		<p style="color:blue">Do you have a sore throat?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to shoot page five-->	
		<!--Added onclick="coldAdd()" to signify the yes response button correlates to cold-->
		<!--Added onlick="allergyAdd()" to signify the no response button correlates to allergy-->
		<a	href="#pagefive"onclick="coldAdd();"data-role="button">Yes</a>
		<a	href="#pagefive"onclick="allergyAdd();"	data-role="button">No</a>
	</div><!-- /content	-->
</div>
	
<!--Created mobile page five-->
<div data-role="page"id="pagefive">
	<!--Added header to Page Five-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<div	data-role="content">
		<!--Added content "Are your symptoms seasonal or chronic?" to page five-->
		<!--Added style color blue to question-->
		<p style="color:blue">Are your symptoms seasonal or chronic?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to shoot page six-->
		<!--Added onlick="allergyAdd()" to signify the yes response button correlates to allergy-->
		<!--Added onclick="coldAdd()" to signify the no response button correlates to cold-->		
		<a href="#pagesix"onclick="allergyAdd();"data-role="button">Yes</a>
		<a href="#pagesix"onclick="coldAdd();"data-role="button">No</a>
	</div><!-- /content	-->
</div>

<!--Created mobile page six-->
<div data-role="page"id="pagesix">
	<!--Added header to Page Six-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<div	data-role="content">
		<!--Added content "Do you have any rashes?" to page six-->
		<!--Added style color blue to question-->
		<p style="color:blue">Do you have any rashes?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to shoot page seven-->
		<!--Added onlick="allergyAdd()" to signify the yes response button correlates to allergy-->
		<!--Added onclick="coldAdd()" to signify the no response button correlates to cold-->		
		<a href="#pageseven"onclick="allergyAdd();"data-role="button">Yes</a>
		<a href="#pageseven"onclick="coldAdd();"data-role="button">No</a>
	</div><!-- /content	-->
</div>

<!--Created mobile page seven-->	
<div data-role="page"id="pageseven">
	<!--Added header to Page Seven-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
		
	</div><!-- /header -->
	<div	data-role="content">
		<!--Added content "Are you experiencing any body aches?" to page seven-->
		<!--Added style color blue to question-->
		<p style="color:blue">Are you experiencing any body aches?</p>
		<!--Added"button" Yes-->
		<!--Added "button" No-->
		<!--Set "button" Yes and "button" No to shoot page eight-->
		<!--Added onclick="coldAdd()" to signify the yes response button correlates to cold-->
		<!--Added onlick="allergyAdd()" to signify the no response button correlates to allergy-->		
		<a href="#pageeight"onclick="coldAdd();"data-role="button">Yes</a>
		<a href="#pageeight"onclick="allergyAdd();"data-role="button">No</a>
	</div><!-- /content	-->
</div>
<!--Created mobile page eight-->
<div data-role="page"id="pageeight">
	<!--Added header to page eight-->
	<div data-role="header">
		<h1>Cold or Allergy</h1>
	</div><!-- /header -->
	<!--Added content and button Results to page eight-->
	<div	data-role="content">
		<a onclick="results()" data-role="button">Results</a>
		<p id="results"></p>
	</div><!-- /content	-->
</div>

