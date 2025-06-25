<p align="center">
  <a href="">
    <img alt="Hero" src="https://github.com/user-attachments/assets/bc3f63fc-32e5-40dd-a54f-daaee4328263" width="75%" />
  </a>
</p>

## Ön Bilgi
- Nexus hesaplama gücünü demokratikleştirmek için merkeziyetsiz/süper bilgisayar ağları üzerine çalışmalar yapan bir proje olarak biliniyor
- $20M+ yatırım topladılar bu kesinlikle dikkat çekici bir ayrıntı.
- Testnet 3 ödüllü ve büyük ihtimalle son testnet.
- Sınırısz node kurulabiliyor. Hangi yöntemle olduğu fark etmez, önemli olan panele kaydetmek.

## Tavsiye Edilen Sistem Gereksinimleri
- CPU: 4+ Cores
- RAM: 4+ GB
- SSD: 50+ GB
- İşletim Sistemi: UBUNTU 24.04LTS

## Yükleme Adımları
- Öncelikle güncellemeleri yapalım ve tmux ekranı açalım.
```
sudo apt update && sudo apt upgrade -y && sudo apt install pkg-config libssl-dev build-essential tmux && cd $HOME && tmux new-session -t nexus
```

- Daha sonra Rust yükleyelim
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source $HOME/.cargo/env
```

- Son olarak Nexus yükleyelim ve platform üzerinden aldığımız ID ile node başlatalım. SS'de göründüğü gibi ilk önce 1 numaraya tıklıyoruz sonra 2 numaraya tıklayıp Node ID alıyoruz. Çalıştırmaya başladıktan bir süre sonra aynı ekranın alt tarafında görünmeye başlar. Sol tarafında yeşil yanması çalışltığını gösteriyor.
```
curl https://cli.nexus.xyz/ | sh
source ~/.bashrc
nexus-network start --node-id <your-node-id>
```

<p align="center">
  <a href="">
    <img alt="Hero" src="https://github.com/user-attachments/assets/0e07c5b6-5261-4a98-ace7-1f659bffa427" width="75%" />
  </a>
</p>

## Ek Kodlar
- İsim vererek tmux ekranı açmak: ````tmux new-session -t boundless````
- Tmux ekranında çıkmak: Önce ````ctrl+b```` sonra ````d```` bas
- Tmux ekranına tekrar giriş yapmak: ````tmux attach -t boundless````
- Tmux ekranlarını listelemek: ````tmux ls````


