# SpringThymeLeaf
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml" xmlns:th="http://www.thymeleaf.org">
<head>
<meta charset="utf-8"/>
<title>Aurora</title>
<style type="text/css">
textarea{
	font:15px verdana, serif; /* font inside textbox */

}
-
-\-\\
input[type=text] {
	width: 250px;
	padding: 8px 2px;
	margin: 8px 0;
	display: inline-block;
	border: 1px solid #ccc;
	border-radius: 4px;
	box-sizing: border-box;
	font:15px verdana, serif; /* font inside textbox */
}

select{
	font: 12px verdana, serif; /*form font size */

}

fieldset {
	padding: 1em;
	font: 80%/1 sans-serif;
	border: 1px solid green
}

legend {
	color: #0000FF;
	font-weight: bold;
	font: bold 18px/30px Georgia, serif; /*form font size */
}

#title{
	
	color: white;
	font-weight: bold;
	background-color: forestgreen;
	font: bold 15px Georgia, serif; /*form font size */
	text-align:center;
}


.tabletitle{
	
	color: green;
	font-weight: bold;
	/*background-color: forestgreen;*/
	font: bold 16px Georgia, serif; /*form font size */
	text-align:left;
}

.tableHead{
	
	color: green;
	font-weight: bold;
	/*background-color: forestgreen;*/
	font: bold 15px Georgia, serif; /*form font size */
	text-align:center;
	border:1px red solid;
}

#divnetwork{
display:inline;
}

.tableValue{
	
	color: black;
	font-weight: bold;
	/*background-color: forestgreen;*/
	font:16px verdana, serif; /*form font size */
	text-align:left;
	padding-left:10px;
}

.tableresult{
	border:1px green solid;
}


input[type=submit] {
	width: 30%;
	background-color: #4CAF50;
	color: white;
	padding: 10px 20px;
	margin: 8px 0;
	border: none;
	border-radius: 4px;
	cursor: pointer;
	font: bold 12px Georgia, serif;
}

textarea {
	width: 270px;
	height: 100px;
	overflow: hidden resize: none;
}

label {
	color: #0000FF;
	font-weight: bold;
	font: bold 14px Georgia, serif;  /*font size*/
	//display: block;
	width: 150px;
	float: left;
}

#tableHeadBorder tr{
	border:1px green solid;
}

.auto-style2 {
	border-collapse: collapse;
	text-align: left;
}
form {
	border:1px solid green;
	width:75%;	
	margin:auto;
	padding-left:10px;
}
.auto-style6 {
	text-align: left;
}
.auto-style7 {
	border-collapse: collapse;
	border: 1px solid #008000;
}
</style>

<script>
		function formSubmit() {
			alert();
			document.getElementById("logoutForm").submit();
			alert();
		}
	</script>

<script type="text/javascript">
function initiate(){
//alert("after mvc");
//if start then hide forms
//document.getElementById('divnetwork').style.display = "none";
//alert();
hideForms();
persistForm();

//to persist the selection form
		
var btn=hiddenForm.getElementsByTagName("p")["hiddenParagraphStat"].innerHTML;
if(btn=="setConfig" || btn=="getConfig"){
		//alert("set config licked");
		//alert(hiddenForm.getElementsByTagName("p")["hiddenParagraphParam"].innerHTML);
		
		frmwebpa.enteredUri.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML;
		//for default selection of data type
		var dataType=hiddenForm.getElementsByTagName("p")["hiddenParagraphDataType"].innerHTML;
			var dt=$('#dataType').val();
			$('#dataType').val(dataType);
		
		frmdevicetype.parameterName.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphParam"].innerHTML;	
		//alert("end of setconfig");
		
		var selectxb3xi3=hiddenForm.getElementsByTagName("P")["selectxb3xi3"].innerHTML;
		//alert("xix5"+selectxb3xi3);
			var objtr=$('#selectxb3xi3').val();
			$('#selectxb3xi3').val(selectxb3xi3);
		
      //end for default data type selection
	   var trObject=hiddenForm.getElementsByTagName("P")["trObject"].innerHTML;
	     //alert("selcteed device"+trObject);
		var objtr=$('#trObject').val();
		$('#trObject').val(trObject);
		
		var objparam=hiddenForm.getElementsByTagName("P")["hiddenParagraphParam"].innerHTML;
		var objpar=$('#parameterName').val();
		$('#parameterName').val(objparam);
	
	}
	
}

function persistForm(){
	//alert("final persistance");
	frmoperationtype.trObject.value=hiddenForm.getElementsByTagName("p")["trObject"].innerHTML;
	frmoperationtype.selectxb3xi3.value=hiddenForm.getElementsByTagName("p")["selectxb3xi3"].innerHTML;
	if(hiddenForm.getElementsByTagName("p")["hiddenParagraphDevice"].innerHTML!=""){
		frmwebpa.deviceId.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphDevice"].innerHTML;
	}
	frmwebpa.enteredUri.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML;
	//set181Object();
	selectTrObjects();
}

function hideForms(){
		frmoperationtype.style.display="none";
}
	
function populatefrmauth(){
	if(hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML!=""){
	frmwebpa.enteredUri.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML;
	}
	
	frmdevicetype.parameterName.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphParam"].innerHTML; //selected device
	
}

//to persist device selection and hidden fields
function populatefrmdevicetype(){
//alert(hiddenForm.getElementsByTagName("p")["hiddenParagraphAuthValue"].innerHTML);
frmdevicetype.auth.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphAuthValue"].innerHTML;
frmwebpa.enteredUri.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML;

if(hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML!=""){
	frmwebpa.enteredUri.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphWebpaConnectedTo"].innerHTML;
	}
//alert(frmdevicetype.auth.value);
frmdevicetype.deviceId.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphDevice"].innerHTML;
console.log("device id after get form is clicked  " + frmdevicetype.deviceId.value);
}

function populatefrmoperationtype(){
	populatefrmdevicetype();
	frmoperationtype.auth.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphAuthValue"].innerHTML;
	//frmoperationtype.deviceId.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphDevice"].innerHTML;
	frmoperationtype.parameterName.value=hiddenForm.getElementsByTagName("p")["hiddenParagraphParam"].innerHTML;
	console.log("set is done for set button");
		//selectTrObjects();
	//alert("hai " + hiddenForm.getElementsByTagName("P")["selectxb3xi3"].innerHTML);
}


function selectTrObjects1(){
	//$(document)
	//alert("loaded trobects");
	var value = document.getElementById("selectxb3xi3").value;
	$select = $('#trObject');
	//request the JSON data and parse into the select element
	
	$.ajax({
	  type:'get',
	  url: '/hello/device/json/'+value,
	  dataType:'json',
	  cache:false,
	  success:function(data){
	    //clear the current content of the select
	    console.log(" sucess value is " + value);
	    $select.html('');
	    //iterate over the data and append a select option
	    console.log(data);	    
	    $.each(data, function(index, element){	 
	    	
	      var trobj=hiddenForm.getElementsByTagName("p")["trObject"].innerHTML;
	      if(element==trobj)
	    	  {
	      		$select.append('<option id="' + element + '" selected="selected">' + element + '</option>');
	    	 }
	      else{
	    	  $select.append('<option id="' + element + '">' + element + '</option>');
	      }
	      
	    })
	    
	    var selectedValue = document.getElementById("trObject").value;
		//$("input[name='parameterName']").val("" + selectedValue);
	    //$("input[name='parameterName']").val("Please select Object");
	  },
	  error:function(){
	    //if there is an error append a 'none available' option
	    $select.html('<option id="-1">none available</option>');
	  }
	});  
	
	//alert();
	}

// 
function set181Object(){

	
	var trobj=document.getElementById("trObject").value;
	var no=trobj.indexOf("WiFi");
	if(no>=1){
		//alert("wifi");
		$('#divnetwork').show();
		//var netval=$('input[name="network"]:checked').val();
		//frmdevicetype.parameterName.value=trobj+netval;
	}else{
		frmdevicetype.parameterName.value=trobj;
		$('#divnetwork').hide();
		
	}
	
	
	$(document).ready(function(){
		$("input[name=network]:radio").change(function(){
			//alert('did it');
			var netval=$('input[name="network"]:checked').val();
			frmdevicetype.parameterName.value=trobj+netval;
		});
	});
	
}
</script>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.2/jquery.min.js"></script>
</head>
<body bgcolor="#f2f2f2" onload="initiate()">
<div class="auto-style6">
<table style="width:1600px;margin:auto">
					<div id="title">
					<h1>AURORA</h1>
					</div>
					<h1></h1>
	<tr>
		<td style="height: 23px">
			<!--frmauth end-->
			 
				<br />
		</td>
	</tr>
	<tr>
		<td>
			<c:url value="/device/login_spring?logout" var="logoutUrl" />
			<!-- <form name="frmlogout" method="post" action="${logoutUrl}"> -->
			<form action="${logoutUrl}" method="get" id="logoutForm">
		<input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}" />
				<table style="width: 100%">
					<tr>
						<td style="width: 1198px">&nbsp;</td>
						<td style="width: 146px" class="auto-style2"></td> 								
						<span th:text="${session.username}">[...]</span>| <a href="/hello">Logout</a>
					</tr>
				
			</table>
			 	</form>
				</td>
	</tr>
	
	<tr>
		<td style="height: 23px">
			<form name="frm" id="frmwebpa" action="getWebpa.html" method="post" style="height:250px">
			<input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}" />
			
			<table style="width: 100%">
						<tr>
							<td style="width: 336px">
							<br />
							<fieldset name="Group1">
							<legend>WebPa</legend>
							<form name="frmwebpa" method="post">
							<table style="width: 100%">
								<tr>
									<td style="width: 234px">
					<label for="Device ID:" style="width: 98px">Device ID:</label></td>
									<td>
					<input type="text" id="deviceId" name="deviceId" placeholder="mac:" style="width:233px" th:value="${deviceID}"/></td>
								</tr>
								<tr>
									<td style="width: 234px"><label for="WEBPA SERVER">Webpa Server:</label></td>
									<td>
									<input type="text" id="enteredUri" name="enteredUri" style="width: 233px" disabled="true"/></td>
								</tr>
								<tr>
									<td style="width: 234px">&nbsp;</td>
									<td> 
					<input type="hidden" name="auth"/>
					<input type="submit" value="Find Webpa Server"
				onclick="populatefrmauth()" style="width: 167px; height: 36px;"/>
				
									</td>
								</tr>
								</table>
								</form>
							
							</fieldset>					
			</td>
							
							
							
							<td style="width: 15px">&nbsp;</td>
							<td style="width: 538px"><fieldset name="Group1">
							<legend>TR181</legend>
							<form name="frmdevicetype" method="post" action="getdeviceConfig.html">
							<input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}" />
							
							<table style="width: 100%">
								<tr>
									<td style="height: 17px">
									&nbsp;</td>
									<td style="height: 17px">
						<select id="selectxb3xi3" name="selectxb3xi3" size="1" style="width:99px; height: 30px;" hidden="true">
						  <option id="optionXB3" value="xb3">XB3</option>
						 </select></td>
								</tr>
								<tr>
									<td style="height: 17px">
						<label for="WEBPA SERVER" style="width: 121px">
						TR 181 Obj:</label></td>
									<td style="height: 17px">
					<select id="trObject" name="trObject" onchange="set181Object()" style="width:311px; height: 30px;">
					 <option value="0" selected="selected">..Select..</option>
					 <option value="Device.DeviceInfo.MemoryStatus.">Memory Status</option>
					 <option value="Device.DeviceInfo.NetworkProperties.">Network Properties</option>
					 <option value="Device.ManagementServer.">Management Server</option>
					 <option value="Device.GatewayInfo.">Gateway Info</option>
					 <option value="Device.UserInterface.">User Interface</option>
					 <option value="Device.WiFi.SSID.">WiFi SSID Level</option>
					 <option value="Device.WiFi.AccessPoint.">WiFi AccessPoint Level</option>
					 <option value="Device.IP.Diagnostics.">IP Diagnostics</option>
					 <option value="Device.Routing.">Routing Info</option>
					 <option value="Device.Hosts.">Device Hosts</option>
					</select></td>
								</tr>
								<tr>
									<td style="height: 17px">&nbsp;</td>
									<td>
									<div id="divnetwork" name="divnetwork" style="display:none">	
									2.4 GHz <input name="network" type="radio" value="10001."/>&nbsp;&nbsp;&nbsp; 
									5GHz<input name="network" type="radio" value="10101." />&nbsp;&nbsp;&nbsp; 
									XHS<input name="network" type="radio" value="10002." />
									</div>
									</td>
										</tr>
								<tr>
									<td style="height: 17px"></td>
									<td style="height: 17px">
					<input type="text" name="parameterName" id="parameterName" placeholder="select tr object" style="width: 293px" readonly="readonly"/></td>
								</tr>
								<tr>
									<td style="height: 17px">&nbsp;</td>
									<td style="height: 17px">
				        <input name="Submit1" style="width:75px; height: 36px;" type="submit" value="Get" onclick="populatefrmdevicetype()"/></td>
						<input type="hidden" name="auth" />
					  <input type="hidden" name="deviceId" />
					 <input type="hidden" name="parameterValue" value=""/>
		     		 <input type="hidden" name="dataType" value = "1"/>
		             <input type="hidden" name="type" value="Get Config"/>
										

						</tr>
							</table>
							</form>
							</fieldset></td>
						</tr>
				</table>
			
				</form> </td>
	</tr>
	
	<tr>
		<td>&nbsp;</td>
	</tr>
	<tr>
		<td style="height: 23px"></td>
	</tr>
	
	<tr>
		<td style="height: 23px">
		<form name="frmoperationtype" action="${contextPath}/device/deviceConfig" style="height:200px" method="post" onsubmit="persistForm()">
		<input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}" />
								<table style="width:100%; margin-bottom:45px;margin-top:45px; margin-right: auto;" align="left">
				<tr>
					<td style="height: 53px; width: 1059px">
					<label for="Device ID:" style="width: 101px">Data Type:</label></td>
					<td style="height: 53px; width: 1711px;">
						<select id = "dataType"  name="dataType" style="color:black;width:300px; height: 30px;">
               <option value="0">String</option>
               <option value="1">Integer</option>
               <option value="2">Unsigned Integer</option>
               <option value="3">Boolean</option>
               <option value="4">DateTime</option>
               <option value="5">Base64</option>
               <option value="6">Long</option>
               <option value="7">Unsigned Long</option>
               <option value="8">Float</option>
               <option value="9">Double</option>
               <option value="10">Byte</option>
           </select>
					</td>
					<td style="height: 53px;">
					<label for="WEBPA SERVER" style="width: 119px">Value:</label></td>
					<td style="width: 786px; height: 53px;">
						<input type="text" name="parameterValue" style="width: 300px" value="${parameterValue}" size="20"/></td>
				</tr>
							<tr>
					<td style="width: 1059px; height: 54px;" class="auto-style2">
					&nbsp;
				</td>
					<td style="width: 1711px; height: 54px;"> 
				
				<input name="Submit3" style="width: 110px; height: 34px;" type="submit" value="Set" onclick="populatefrmoperationtype()"/></td>
				    <input type="hidden" name="auth" />
					<input type="hidden" name="deviceId" />
					<input type="hidden" name="parameterName" />
					<input type="hidden" name="type" value="Set Config"/>
					<input type="hidden" name="trObject"/>
					<input type="hidden" name="selectxb3xi3"/>

					<td style="height: 54px;"> 
				
								</td>
					<td style="width: 786px; height: 54px;"> 
				
					&nbsp;</td>
				</tr>
			
					</table>
		</form><!--frmoperationtype-->
		</td>
	</tr>
	<tr>
		<td style="height: 23px">
		<form name="frmtable" id="frmtable">
		<input type="hidden" name="${_csrf.parameterName}" value="${_csrf.token}" />
		
		
		<table  style="width:94%; margin-bottom:30px; margin-left: auto; margin-right: auto;">
			
			<div id="tableHeadBorder">
			<tr class="tableHead">
				<td style="height: 25px;" colspan="3" class="tabletitle"><br />
				Results for the TR 181 object 
				:: ${parameter} </td>
			</tr>
			<tr class="tableHead">
				<td style="width: 2232px; height: 25px;"></td>
				<td style="width: 506px; height: 25px;"></td>
				<td style="width: 657px; height: 25px;"></td>
			</tr>
			</div>
					<div id="tableValue">
					</div>
			       <tr class="tableHead">
				<td style="height: 25px;" colspan="3">
				<table style="width:100%" name="tblresult" class="auto-style7">
					<tr>
				<td style="width: 2232px; height: 25px;" class="tableresult">Device Name</td>
				<td style="width: 506px; height: 25px;" class="tableresult">Value</td>
				<td style="width: 657px; height: 25px;" class="tableresult">Type</td>
					</tr>
					<!-- <c:forEach var="list" items="${parvalue}"> -->
					<tr th:each="list:${parvalue}" class="tableValue" style="padding:10px">
							<td th:text="${list.name}" style="height: 45px; width: 2232px; padding-left:5px" class="tableresult" >name</td>
							<td th:text="${list.value}" style="height: 45px; width: 506px; padding-left:5px" class="tableresult">value</td>
							<td th:text="${list.datatype}" style="height: 45px; width: 657px; padding-left:5px" class="tableresult">datatype</td>
						</tr>
					<!-- </c:forEach> -->
				</table>
				</td>
			</tr>
		</table>
		</form>
		</td>
	</tr>
</table>

<form name="hiddenForm" hidden="true">
		<p th:inline="text" id="hiddenParagraphAuthValue">[[${value}]]</p>
		<p th:inline="text" id="hiddenParagraphStat">[[${call}]]</p>
		<p th:inline="text" id="hiddenParagraphGetWebPa">[[${message}]]</p>
		<p th:inline="text" id="hiddenParagraphDevice">[[${deviceId}]]</p>
		<p th:inline="text" id="hiddenParagraphParam">[[${parameter}]]</p>
		<p th:inline="text" id="hiddenParagraphParamValue">[[${parameterValue}]]</p>
		<p th:inline="text" id="hiddenParagraphWebpaConnectedTo">[[${WebpaConnectedTo}]]</p>
		<p th:inline="text" id="hiddenParagraphDataType">[[${dataType}]]</p>
		<p th:inline="text" id="hiddenParagraphresponseString">[[${responseString}]]</p>
		<p th:inline="text" id="isMultiple">[[${isMultiple}]]</p>
		<p th:inline="text" id="Message">[[${message}]]</p>
		<p th:inline="text" id="trObject">[[${trObject}]]</p>
		<p th:inline="text" id="selectxb3xi3">[[${selectxb3xi3}]]</p>
		<p th:inline="text" id="selectxb3xi3">[[${username}]]</p>
	</form>
</div>
</body>
</html>
