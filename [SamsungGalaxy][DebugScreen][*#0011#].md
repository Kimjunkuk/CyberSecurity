# mmWave Test Debug screen = B66 + n260<br>
## Debug info: 0 0 9 168 66786<br>
## HPLMN(310-260) sim_state(1)<br>
## Serving PLMN(310-260) - LTE<br>
## NW sel mode: Auto<br>
## EMM(registered-0) TAC(31894)<br>
## GUTI: 310-260-280-d6-8f9a41ca<br>
## LTE RRC: Conn Band66 BW: 20<br>
## Earfcn: 66786, PCI: 224<br>
PCI(Physical Cell ID)<br>
5G NR(New Radio) has 1008(PCI) each numbers<br>
LTE(Long term evolution) has 504(PCI) each numbers<br>
refer from: https://www.techplayon.com/5g-nr-physical-cell-id-pci-planning/<br>
What is this?<br>
Each 5G NR cell corresponds to a Physical cell ID(PCI) and it is used to distinguish cell on the Radio side.<br>
why using this?<br>
The purpose of PCI optimiztion is to ensure to a great extent that neighboring cells should have different primary sequences allocated.<br>
what knowlege do i need about this?<br><br>
## RSRP:-80 RSRQ:-12 SNR:-0.6<br>
RSRP and RSRQ are key measures of signal level and quality for modern LTE networks.<br>
In cellular networks, when a mobile moves from cell to cell and performs cell selection/reselection and handover, it has to measure the signal strength/quality of the neighbor cells.<br>
## PCC MIMO Configured: 4<br>
## Tx Pwr: -3 dBm<br>
## UpperLayer_Ind_R15: Support<br>
## Dcnr_Restriction: False<br>
## NR5G_RSRP:-84<br>
## NR5G_SINR: 22.0<br>
## NR5G RSRQ: -11<br>
## NR_SSB_Index: 21<br>
## NR_EARFCN: 2256859<br>
## NR_PCI: 224<br>
## NR_RLF Count<br>
## SCGF Type:<br>
## NR_Band: n260<br>
## NR_CDRX: Active<br>
## NR_Num_CC: 1<br>
## NR_DL Scheduling: 0.07<br>
## NR_BLER: 0.00<br>
## NR_BW: 100<br>
## NR_SB Status: LTE+NR<br>
## NR_ANT MAX RSPR: -81<br>
## NR_ANT MIN RSRP: 84<br>
## NR_Tx Pwr: 10dBm<br>
## ENDC Total Tx Pwr: 10dBm<br>
## NR_SCS: 240kHz<br>
## paging_cycle: 1280ms<br>
## CA-Not Config 0 0<br>
## PA State: 0(ET, HDET: 0<br>
## Network: unblock<br>
## Final IMEI certi: Pass<br>
## Unknown 0 <br>
## AJB Init_bug: 0 ms<br>
## AsDiv: Not supported<br>
## TM: ALL TM Lvl is 0 <br>
## Wakeup_info: 0 <br>



 
In LTE network, a UE measures two parameters on reference signal: RSRP (Reference Signal Received Power) and RSRQ (Reference Signal Received Quality).

In LTE network, a UE measures two parameters on reference signal:

RSSI – Received Signal Strength Indicator:The carrier RSSI (Receive Strength Signal Indicator) measures the average total received power observed only in OFDM symbols containing reference symbols for antenna port 0 (i.e., OFDM symbol 0 & 4 in a slot) in the measurement bandwidth over N resource blocks.

The total received power of the carrier RSSI includes the power from co-channel serving & non-serving cells, adjacent channel interference, thermal noise, etc. Total measured over 12-subcarriers including RS from Serving Cell, Traffic in the Serving Cell

RSRP – Reference Signal Received Power: RSRP is a RSSI type of measurement, as follows there are some definition of it and some details as well.
It is the power of the LTE Reference Signals spread over the full bandwidth and narrowband.
A minimum of -20 dB SINR (of the S-Synch channel) is needed to detect RSRP/RSRQ

RSRQ – Reference Signal Received Quality: Quality considering also RSSI and the number of used Resource Blocks (N) RSRQ = (N * RSRP) / RSSI measured over the same bandwidth. RSRQ is a C/I type of measurement and it indicates the quality of the received reference signal. The RSRQ measurement provides additional information when RSRP is not sufficient to make a reliable handover or cell reselection decision. 

In the procedure of handover, the LTE specification provides the flexibility of using RSRP, RSRQ, or both. 

It must to be measured over the same bandwidth:

Narrowband N = 62 Sub Carriers (6 Resource Blocks)
Wideband N = full bandwidth (up to 100 Resource Blocks / 20 MHz)

RSRP
In other words RSRP (Reference Signal Receive Power) is the average power of Resource Elements (RE) that carry cell specific Reference Signals (RS) over the entire bandwidth, so RSRP is only measured in the symbols carrying RS.

RSRP is the average received power of a single RS resource element.
UE measures the power of multiple resource elements used to transfer the reference signal but then takes an average of them rather than summing them.
Reporting range -44…-140 dBm
RSRP does a better job of measuring signal power from a specific sector while potentially excluding noise and interference from other sectors.

RSRP levels for usable signal typically range from about -75 dBm close in to an LTE cell site to -120 dBm at the edge of LTE coverage.

RSRP mapping 3GPP TS 36.133 V8.9.0 (2010-03)
LTE RSRP TableThe reporting range of RSRP is defined from -140 dBm to – 44 dBm with 1 dB resolution.

The mapping of measured quantity is defined in the table.

RSRQ
In formula:

RSRQ = N x RSRP / RSSI
LTE RSRQ reporting rangeN is the number of Physical Resource Blocks (PRBs) over which the RSSI is measured, typically equal to system bandwidth
RSSI is pure wide band power measurement, including intracell power, interference and noise
The reporting range of RSRQ is defined from -3…-19.5dB
Reference Signals recap: OFDMA Channel Estimation
In simple terms the Reference Signal (RS) is mapped to Resource Elements (RE). This mapping follows a specific pattern (see to below).

So at any point in time the UE will measure all the REs that carry the RS and average the measurements to obtain an RSRP reading.

Channel estimation in LTE is based on reference signals (like CPICH functionality in WCDMA)
Reference signals position in time domain is fixed (0 and 4 for Type 1 Frame) whereas in frequency domain it depends on the Cell ID
In case more than one antenna is used (e.g. MIMO) the Resource elements allocated to reference signals on one antenna are DTX on the other antennas
Reference signals are modulated to identify the cell to which they belong.

RSSI (Received Signal Strength Indicator) is a parameter which provides information about total received wide-band power (measure in all symbols) including all interference and thermal noise.

RSSI is not reported to eNodeB by UE. It can simply be computed from RSRQ and RSRP that are, instead, reported by UE.

RSSI = wideband power = noise + serving cell power + interference power
So, without noise and interference, we have that 100% DL PRB activity: RSSI=12*N*RSRP

Where:

RSRP is the received power of 1 RE (3GPP definition) average of power levels received across all Reference Signal symbols within the considered measurement frequency bandwidth
RSSI is measured over the entire bandwidth
N: number of RBs across the RSSI is measured and depends on the BW
Based on the above, under full load and high:

SNR: RSRP (dBm)= RSSI (dBm) -10*log (12*N)
So we have:

RSRQ = RSRP / (RSSI/N)
N = Number of PRBs (Physical Resource Blocks)
RSSI = noise + serving cell power + interference power during RS symbol
So we have that RSRQ depends on serving cell power and the number of Tx antennas
Impact of serving cell power to RSRQ:
Example for noise limited case (no interference): If all resource elements are active and are transmitted with equal power, then

RSRQ = N / 12N = -10.8 dB for 1Tx
RSRQ = N / 20N = -13 dB for 2Tx taking DTX into account
(because RSRP is measured over 1 resource element and RSSI per resource block is measured over 12 resource elements).

Remember that RSSI is only measured at those symbol times during which RS REs are transmitted – We do not have to take into the count DTx!!!

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
</table>

So, when there is no traffic, and assuming only the reference symbols are transmitted (there are 2 of them within the same symbol of a resource block) from a single Tx antenna then the RSSI is generated by only the 2 reference symbols so the result becomes

RSRQ = N / 2N = -3 dB for 1Tx
RSRQ = -6dB for 2Tx
 SINR DefinitionSINR is the reference value used in the system simulation and can be defined:

Wide band SINR
SINR for a specific subcarriers (or for a specific resource elements)
SINR = S/(I+N), all measured over the same bandwidth

