1. SVC(Switched Virtual Circuit) 
<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr><td>Out Of SVC</td><td>OOS_02</td><td>Power on in In-Service area -> Move to No SVC area -> wait 2 min -> Move to In service</td><td>Check the behavior of the UE whether UE camps on 3G network and lost SVC for 2min. And it should camp on 3G cell again. 
So there should be In SVC -> No SVC -> In SVC activity <br>Validation : Check whether MO voice call  is OK. </td></tr>
<tr><td>Out Of SVC</td><td>OOS_04</td><td>Power on in LTE Service area -> Move to No SVC area -> wait 2 min -> Move to LTE In service area</td><td>Check the behavior of the UE whether UE camps on LTE network and lost SVC for 2min. And it should camp on LTE cell again. 
So there should be In SVC -> No SVC -> In SVC activity<br>Validation : Check whether UE camps on LTE succesfully.</td></tr>
</table>
