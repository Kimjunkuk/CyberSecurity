1. SVC(Switched Virtual Circuit) 
<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr><td>Out Of SVC</td><td>OOS_02</td><td>Power on in In-Service area -> Move to No SVC area -> wait 2 min -> Move to In service</td><td>Check the behavior of the UE whether UE camps on 3G network and lost SVC for 2min. And it should camp on 3G cell again. 
So there should be In SVC -> No SVC -> In SVC activity <br>Validation : Check whether MO voice call  is OK. </td></tr>
<tr><td>Out Of SVC</td><td>OOS_04</td><td>Power on in LTE Service area -> Move to No SVC area -> wait 2 min -> Move to LTE In service area</td><td>Check the behavior of the UE whether UE camps on LTE network and lost SVC for 2min. And it should camp on LTE cell again. 
So there should be In SVC -> No SVC -> In SVC activity<br>Validation : Check whether UE camps on LTE succesfully.</td></tr>
</table>


2.
<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr><td>3G Data Call</td><td>MRAB_03</td><td>Multi Rab  CS Voice  + PS  ( Wedge or Hedge )
- WEB(WAP) or PC Browsing</td><td>Validation : Successful MRAB call in HEDGE or WEDGE Mode</td></tr>
<tr><td>3G Data Call</td><td>MRAB_04</td><td>Multi Rab  PS  +  CS Voice  ( Wedge or Hedge )
- WEB(WAP) or PC Browsing</td><td>Validation : Successful MRAB call in HEDGE or WEDGE Mode</td></tr>
</table>


3.

<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr><td>4G CSFB</td><td>LTE_CSFB_01</td><td>MO Voice call in LTE IDLE mode with REF UE.<br>
- Two time trial for 'P1'<br>
- Ten times trial for 'P1+P2'.</td><td>Established successful MO voice call, UE will try CSFB to GSM or WCDMA according to RedirectionMessage.

Validation : 
 1) Check the CSFB notification (ex. RAT Icon)
 2) Check the MO voice call notification and call time in the screen.
 3) Check the voice mute. 
 4) Check reselection time to LTE after releasing CS call.
     It should be less than 15sec.
 5) Try 10 times with REF UE and mark AVG time
     AVG CSFB time should be same or within 2sec
 1) Check successful voice call in 3G or 2G</td></tr>
<tr><td>4G CSFB</td><td>LTE_CSFB_02</td><td>MT Voice call in LTE IDLE mode with REF UE.<br>
- Two time trial for 'P1'<br>
- Ten times trial for 'P1+P2'.</td><td>Established successful MO voice call, UE will try CSFB to GSM or WCDMA according to RedirectionMessage.

Validation : 
 1) Check the CSFB notification (ex. RAT Icon)
 2) Check the MO voice call notification and call time in the screen.
 3) Check the voice mute.
 4) Check reselection time to LTE after releasing CS call.
     It should be less than 15sec.
 5) Try 10 times with REF UE and mark AVG time
     AVG CSFB time should be same or within 2sec
 1) Check successful voice call in 3G or 2G</td></tr>
</table>


4.
<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr><td>SMS/MMS/SS</td><td>LTE_SMS_1</td><td>Receiving SMS While Idle (E-UTRAN Only)</td><td></td><td>MT SMS while DUT camps on an E-UTRAN cell in the idle mode. 

Validation: 
verify that the DUT can correctly receive one or two page SMS from a second DUT camped on an E-UTRAN cell.  Verify that the destination device receives the entire message as one inbox item.</td></tr>
<tr><td>SMS/MMS/SS</td><td>LTE_SMS_3</td><td></td><td>Sending SMS During Idle (E-UTRAN Only)</td><td>MO SMS while DUT camps on an E-UTRAN cell in the idle mode. 

Validation: 
verify that the DUT can correctly send one or two page SMS from a second DUT camped on an E-UTRAN cell.  Verify that the destination device receives the entire message as one </td></tr>
</table>

5.

<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr>
<td>4G VoLTE</td><td>VLT_01</td><td>Make MO VOLTE Call</td><td>Successful VOLTE Call Establishment.

Validation :
 1) VOLTE Icon is shown properly
 2) make VOLTE MO call whether Call Fail or not.
 3) check VOLTE MO call establishment.</td>
</tr>
<tr>
<td>4G VoLTE</td><td>VLT_03</td><td>Receive MT VOLTE Call</td><td>Successful VOLTE Call Reception

Validation :
 1) VOLTE Icon is shown properly
 2) make VOLTE MO call on another device.
 3) Check whether UE is ringing or not.
 4) on ringing state, receive Call and check call works properly.</td>
</tr>
<tr>
<td>4G VoLTE</td><td>VLT_09</td><td>MO/MT SMS whille VoLTE is Active</td><td>
Validation : Successful sending/receiving  SMS while Voice Call is Active</td>
</tr>
</table>


6.

<table>
<tr><td>Category</td><td>TC No</td><td>Test Case/Scenario Description</td><td>Expected Behavior/Validation Criteria</td></tr>
<tr>
<td>Basic Mobility</td><td>Call_Driving-01</td><td>Make a call in Automatic mode and try driving test for 30min. 
And check Call Drop, No Service and any abnormality.</td><td>[Procedure]
'- Make a call in LTE or WCDMA and try long duration call while driving for 30min.
- 2 devices can be used together with 2 REF device.

[PASS/FAIL Criteria]
This TC is PASS if belcow criterias are met. 
1. there's no abnormality such as calldrop / crash / No Service.</td>
</tr>
<tr>
<td>Basic Mobility</td><td>Tput_Driving-01</td><td>Make a data call such as YouTube in Automatic mode and try driving test for 30min. 
And check Data stall, No Service and any abnormality.</td><td>[Procedure]
'- Make a call in LTE or WCDMA and try long duration data call while driving for 30min.
- 2 devices can be used together with 2 REF device.

[PASS/FAIL Criteria]
This TC is PASS if belcow criterias are met. 
1. there's no abnormality such as data stall for 10sec / crash / No Service.</td>
</tr>
</table>
