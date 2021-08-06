
Understanding Half & Full Duplex

<table style="width:100%">
  <tr>
    <th>Half & Full Duplex</th>
  </tr>
  <tr>
    <td><img src="https://user-images.githubusercontent.com/54308434/128448765-987d203c-a676-4bce-ae67-3c3568131a56.PNG" alt="Error"><p><b>Differences Between Full and Half Duplex Systems</b><br>
There are distinct differences between full and half-duplex systems. With half-duplex mode, each transmitted character is immediately displayed on a monitor. If a device is operating in full-duplex mode, transmitted data does not appear on-screen until it is received and returned. Full-duplex Ethernet does save time when compared to half-duplex because it alleviates collisions and frame retransmissions. Sending and receiving are separate functions, creating a system where there is full data capacity in each direction. In contrast, half-duplex can be used to conserve bandwidth.</p></td>
  </tr>
</table>

Understanding FDD/TDD carrier aggregation

Explain LTE Frame Structure both for FDD and TDD


<table style="width:100%;">
  <tr>
    <td>Time duration for one frame (One radio frame, One system frame) is 10 ms. Thia mean that we have 100 radio frame per second.</td>
  </tr>
  <tr>
    <td><p>frame structure</p><img src="https://user-images.githubusercontent.com/54308434/128444868-ab18d4cd-f81f-448f-a528-41fb430e8269.PNG" alt="Error">
      <p>Some of high level description you can get from this figure would be<br>
Number of subframe in one frame is 10<br>
Number of slots in one subframe is 2. This means that we have 20 slots within one frame.<br>
And one slot is made up of 7 small blocks called ‘symbol’<br></p></td>
  </tr>
  <tr>
    <td><h4>Type1: FDD Frame Structure</h4><p>As LTE FDD is full duplex system, means both the downlink and uplink transmission happens at the same time at different requencies.</p><img src="https://user-images.githubusercontent.com/54308434/128444963-64d90984-9497-44a2-999f-db0b560e2cfd.PNG" alt="Error"></td>
  </tr>
  <tr>
    <td><h4>Type2: TDD Frame Structure</h4><p>In TDD, the transmission is deivided into time domain, means at one moment of time either downlink subframe is transmitted or uplink.</p><img src="https://user-images.githubusercontent.com/54308434/128445028-4382d909-a3c8-4b67-a47f-66303aca02cd.PNG" alt="Error"><p>As one can see in above image, one frame is divided into 10 subframes (1ms each), and that subframe can be either downlink, uplink or special subframe.</p></td>
  </tr>
  <tr>
    <td><p>Who decides the sequence of these subframes. that has been defined by 3GPP with the name TDD Frame Configurations. There are fixed patterns of these configurations and network perator has to choose out of these defined patters. There are total 7 TDD configurations as shown below</p><br><img src="https://user-images.githubusercontent.com/54308434/128447714-fca997b2-8574-47a6-a5f4-6653cfa7ea0c.PNG" alt="Error"><br><br><p>And there comes a Special subframe which comes when there is transition from downlink subframe to uplink subframe. It has three parts –  DwPTS(Downlink Pilot Time Slot),GP (Guard Period) and UpPTS (Uplink Pilot Time Slot) and all of these have configurable lengths, which depends upon Special subframe configuration.</p><br><br><p>Special subframe configuration as shown below:</p><img src="https://user-images.githubusercontent.com/54308434/128447822-b734449d-5fdf-4052-8dbd-97277bc5d99b.PNG" alt="Error"><p>DwPTSis considered as a “normal” DL subframe and carries reference signals and control information as well as data for those cases when sufficient duration is configured. It also carries PSS.<br><br>
GPis used to control the switching between the UL and DL transmission. Switching between transmission directions has a small hardware delay for both UE and eNodeB and needs to be compensated by GP. GP has to be large enough to cover the propagation delay of DL interferes. Its length determines the maximum supportable cell size.<br><br>
UpPTSis primarily intended for sounding reference signals (SRS) transmission from UE. Mainly used for RACH transmission.<br><br></p></td>
  </tr>
</table>

