# 1. Check for Binary UPdate on Knox Chat
## 1-1. BL: Bootloader
## 1-2. AP: Application
## 1-3. CP: Modem
## 1-4. CSC: Carrier
# 2. Device Set up
## 2-1. Flash (Software AP/CP write and IMEI and calabration tile write to device)
### 2-1-1. Check new release
### 2-1-2. Locate path in FileZilla and download to desktop
### 2-1-3. Unzip and load to Odin
### 2-1-4. Put Devices download mode and connect
### 2-1-5. Click start and eject when finished
## 2-2. Verify Software (Send Key string *#12580*369*)
## 2-3. Check if there is existing Google Account to remove FRP lock
## 2-4. Factory RESET - after flashing software (CP or CP+AP)
## 2-5. Silent Log ON (for All)
## 2-5-1. *#9900#
## 2-5-2. Enable slient logging from boot
## 2-6. IMS Log on (T/ATT/Verizon)
### 2-6-1. *#9900#
### 2-6-2. IMS logger
### 2-6-3. Application options > select both, change count to 20
## 2-7. Reboot after step 5 and 6
## 2-8. Sanity Test (Call, SMS, MMS, Data)
## 2-9. For Automation Test
### 2-9-1. FTAT Download / Install
### 2-9-2. ACT Download/ Install
# 3. Testing
## 3-1. Follow Regression Test sheet to run Test
## 3-2. Follow below test for Drive test
### 3-2-1. YouTube
### 3-2-2. Google Map
### 3-2-3. ATT Refresher Loop
### 3-2-4. FTAT SMS/ MMS, Manual SMS/ MMS
### 3-2-5. Call: 877-340-9024
### 3-2-6. Speed Test Minimum 3 sets for 3F and 5 set for LTE
### 3-2-7. MO/MT calls
## 3-4. Run Automation Test script using FTAT

Aging
