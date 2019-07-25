# protcoin MN Script

***
## Installation:
```
git clone https://github.com/pineplatform/PROT_MasterNode_install
cd PROT_MasterNode_install
bash PROT_MasterNode_install.sh

```
***
## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the protcoin Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **5000** **PROT** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Tools -> "Open Masternode Configuration File"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
12. Open **Debug Console** and type:
```
startmasternode "alias" "0" "MN1"
```
***

## Usage:
```
protcoin-cli getinfo
protcoin-cli mnsync status
protcoin-cli masternode status
```
Also, if you want to check/start/stop **protcoin** , run one of the following commands as **root**:

**Ubuntu 16.04**:
```
systemctl status protcoin #To check the service is running.
systemctl start protcoin #To start protcoin service.
systemctl stop protcoin #To stop protcoin service.
systemctl is-enabled protcoin #To check whether protcoin service is enabled on boot or not.
```
**Ubuntu 14.04**:  
```
/etc/init.d/protcoin start #To start protcoin service
/etc/init.d/protcoin stop #To stop protcoin service
/etc/init.d/protcoin restart #To restart protcoin service
```
***
