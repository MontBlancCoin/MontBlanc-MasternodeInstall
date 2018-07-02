# MontBlanc
Script to install an [MontBlanc Masternode](https://mblc.me/) on a Linux server running **Ubuntu 16.04**. Use it on your own risk.  
***


## Generate Masternode Private Key on desktop wallet
```
- Open the the desktop wallet
- Click Help
- Click Debug Window
- Click Console Tab
- Type: masternode genkey
- Then save the output
```
***


## Scrypt installation on VPS
```
wget -N https://raw.githubusercontent.com/MontBlancCoin/MontBlanc-MasternodeInstall/master/MontBlanc_install.sh
bash MontBlanc_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet. Here are the steps:
1. Open the MontBlanc Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **3000** **6000** **15000** or **25000** **MBLC** to **MN1**.  
4. Wait for 10 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:11145**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  
***

## Usage:
```
MontBlancd masternode status
MontBlancd getinfo
```
Also, if you want to start/stop **MontBlanc**, run one of the following commands as **root**:

```
systemctl start MontBlanc #To start MontBlanc MN service
systemctl stop MontBlanc #To stop MontBlanc MN service
systemctl status MontBlanc #To check whether MontBlanc MN service is running or not
```  
***

