# TT-Miner

### Latest Download Links
Download link - windows version:
https://TradeProject.de/download/Miner/TT-Miner.zip

Download link - linux version:
https://TradeProject.de/download/Miner/TT-Miner.tar.xz

You might need latest c++ runtime for beta 6 if you see a missing VCRUNTIME140_1.dll
https://support.microsoft.com/ms-my/help/2977003/the-latest-supported-visual-c-downloads

## Configure TT-Miner

Supported algorithms:
   - PROGPOW (Zano, Sero & EPIC, Veil)
   - KAWPOW (Raven, Zelantus)
   - ETHASH (ETH, Music, Callisto, etc)
   - ETCHASH (ETC)
   - UBQHASH (UBIQ)
   - MTP (Zcoin, Tecra)

### Parameters
|      `-a, -A, -algo `         |`ALGONAME   `                         |`'select the algorithm to use for mining'`                         |
|----------------|-------------------------------|-----------------------------|
||`ETHASH  `         |`Ethash (ETH, ETC, Music, Callisto, etc)`            |"Isn't this fun?"            |
|         |`UBQHASH`|`Ubiq version of Dagger-Hashimoto (UBIQ)`|
|         |`PROGPOW`|`ProgPoW (Zano, Sero, Raven, Epic, Ethercore)`|
|         |`MTP`|`MTP (Zcoin algo)`|


#### Parameter without argument:
|               |               |    
| ------------- |:-------------:| 
| `-RH, -rate `      | Reports the current hashrate every 90 seconds to the pool | 
| `-n, -list, -ndevs`   | List the detected CUDA devices and exit |      
| `-logpool` | Enable logging of the pool communication. TT-Miner creates the pool-logfile in the folder 'Logs'  |
| `-log`   | Enable logging of screen output and additional information, the file is created in the folder 'Logs' |      
| `-luck`   | Show a second information line that shows you how long it should take to find a new solution (share) |      
| `-U`   |  --nvidia      Mining using CUDA devices (just for combability - can be omitted) |   
| `-X`   | Mining with OpenCL (just for combability - NOT supported) |   
| `-G, --amd`   | Mining using AMD devices (just for combability - NOT supported) |     
| `-h, --help`   | Show this help and exit |     
| `-v, --version`   | Show TT-Miner version and exit |     
| `-nocolor`   | Disables color output |  

#### POOL RELATED


- `-P` - Pool definition - defines all values that are required for a connection to a mining -          -  pool. 
-        [scheme://]user/wallet[.workername/username][:password]@hostname:port
-        
     The minimal definition to connect to a pool is:
-        -P YOUR_WALLET@YOUR_SERVER_IP:YOUR_SERVER_PORT
     With all options it look like this
-        -P stratum+tcp://YOUR_WALLET.YOUR_WORKER:YOUR_PASSWORD@YOUR_SERVER_IP:YOUR_SERVER_PORT
**Note -> The first -P will define your primary pool, all following -P definition will work as
            backup/failover pool.**
|               |               |    
| ------------- |:-------------:| 
| `-o, -url, -pool`      | YOUR_SERVER_IP:YOUR_SERVER_POOL | 
|`-u, -user, -wal       `| YOUR_WALLET[.YOUR_WORKER] or YOUR_USER|
| `-p, -pass`      | YOUR_PASSWORD | 
| `-w, worker`      | YOUR_WORKER | 
|`-pool2`         |YOUR_BACKUP_SERVER_IP:YOUR_BACKUP_SERVER_POOL|
| `-o, -url, -pool`      | YOUR_SERVER_IP:YOUR_SERVER_POOL | 
| `-wal2`      | YOUR_BACKUP_WALLET[.YOUR_BACKUP_WORKER] or YOUR_BACKUP_USER | 
| `-pass2 `      | YOUR_BACKUP_PASSWORD | 
| `-worker2`      | YOUR_BACKUP_WORKER | 

- `-coin` -  defines the coin you want to mine.
-     That helps for connection to some pools and avoids unnecessary DAG creation
      SERO
      EPIC
      ZANO
      ETC
      ETH
      CLO
      PIRL
      etc.... please read readme.txt for more coins
#### Performance and Process Priority

- `-PP INT` -  Process-Priority
-     This option set the process priority for TT-Miner to a different level: 
      1. low
      2. below normal
      3. normal
      4. above normal
      5. high
      Default: -PP 3

