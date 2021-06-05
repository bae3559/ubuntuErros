## DPKG LOCK ERRORS
'''
E: Could not get lock /var/lib/dpkg/lock-frontend - open (11: Resource temporarily unavailable)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), is another process using it?
'''

## 1. sudo killall apt apt-get

'''
apt: no process found
apt-get: no process found
'''
로 process가 없다고하면, 

### 2. 직접 디렉토리 다 삭제

'''
sudo rm /var/lib/apt/lists/lock

sudo rm /var/cache/apt/archives/lock

sudo rm /var/lib/dpkg/lock*

sudo dpkg --configure -a 

sudo apt update

'''
