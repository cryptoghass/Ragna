# Ragnarok
Shell script to install a [Ragnarok Masternode](https://ragnaproject.io/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
wget -q https://raw.githubusercontent.com/zoldur/Ragna/master/ragna_install.sh
bash ragna_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Ragna Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **10000** RAGNA to **MN1**. You need to send all 10000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
11. Close and open the wallet again.
12. Go to **Masternodes** -> **My Master Nodes** tab
13. If you don't see your masternode, click **Update**
14. Unlock your wallet if it is encrypted
15. Select your masternode and click on **Start**
16. Login to your VPS and check your masternode status by running the following command. If you get **Status 9**, it means your masternode is active.
```
ragnarok-cli masternode status
```
***

## Usage:
```
ragnarok-cli masternode status  
ragnarok-cli getinfo
```
Also, if you want to check/start/stop **Ragna**, run one of the following commands as **root**:

```
systemctl status Ragna #To check if Ragna service is running  
systemctl start Ragna #To start Ragna service  
systemctl stop Ragna #To stop Ragna service  
systemctl is-enabled Ragna #To check if Ragna service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated

**RAGNA**: RRqx1y2j3ErhPZwZQTrpufCe7iV6w99Mwb  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB  
