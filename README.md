# Discount Coiun
Shell script to install a [Discount Coin Masternode]() on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
wget -q https://raw.githubusercontent.com/zoldur/DiscountCoin/master/discount_install.sh 
bash discount_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Discount Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **500** DSC to **MN1**.  
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
9. Click **OK** to add the Masternode  
10. Click **Start All**  
11. Check the node has started by running the following command on VPS and get **status 9**
```
DiscountCoind masternode status
```
***

## Usage:
```
DiscountCoind masternode status  
DiscountCoind getinfo
```
Also, if you want to check/start/stop **Discount**, run one of the following commands as **root**:

```
systemctl status Discount #To check if Discount service is running  
systemctl start Discount #To start Discount service  
systemctl stop Discount #To stop Discount service  
systemctl is-enabled Discount #To check whether Discount service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated  

**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB
