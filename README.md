# ccminer V3.8.3 for ARM (cortex-a53)

Based on https://github.com/monkins1010/ccminer/tree/ARM

Git and Build Process:
```
apt update
apt upgrade
apt install software-properties-common
apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential -y
apt install git
git clone https://github.com/WahyuDwi25/ccminer.git
cd ccminer
chmod +x ccminer
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
./build.sh

Uji Miner dengan perintah dibawah "Jangan Lupa ubah Wallet Addressnya"
./ccminer -a verus -o stratum+tcp://cn.vipor.net:5040 -u WALLET_ADDRESS.NAMA WORKER -p x -t 4

Jalankan perintah Autorun Miner dengan Ketik perintah-perintah dibawah :
nano autorun.sh
/root/ccminer/ccminer -a verus -o stratum+tcp://cn.vipor.net:5040 -u Walet Verus anda.Nama Worker -p x -t 4

Membuat autorun setelah restart atau shutdown
crontab -e
@reboot bash /root/ccminer/autorun.sh > /root/ccminer/miner.log 2>&1

cek mining progress
cd ccminer --enter
tail -f miner.log

cara ganti wallet/pool
cd ccminer --enter
nano autorun.sh

cara cek version ccminer
cd ccminer
./ccminer --version
```

For specific details on installing clang-16 on your current OS, check: https://apt.llvm.org/
