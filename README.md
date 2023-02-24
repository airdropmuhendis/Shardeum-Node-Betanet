<h1 align="center">Shardeum Betanet Node Kurulumu

## Shardeum için sunucuyu nerden nasıl alacağınızı bilmiyorsanız node eğitim serimizi izleyebilirsiniz. [Node Eğitim Serisi](https://www.youtube.com/playlist?list=PLKxGUfdcj7MVXls2OvTpwx6CnpVJN685w)


### Sistem Gereksinimleri
 - Ubuntu 20.04
 - 2-4 CPU
 - 8GB RAM
 - 200- 250 GB SSD

## Metamaska sphin1x ağı ekleme
- Ağ : Shardeum Sphinx 1.X
- New RPC URL : ``` https://sphinx.shardeum.org/ ```
- Chain ID : 8082
- Symbol : SHM
- Block Explorer URL : ``` https://explorer-sphinx.shardeum.org/ ```


 ## Root yetkisi almak için aşağğıdaki kodu giriyoruz bazı sunucularda bunu sürekli girmemiz gerekiyor. eğer bunu girmezseniz yazdığınız kodun başına sudo komutunu yazarkata devam edebilirsiniz ancak karışıklık olmaması için aşğıdaki komutu yazmanızı tavsiye ederim. ( root: Windows cihazlarda olduğu gibi yönetici olarak çalıştırmamıza, yani bize yetki veren bir komuttur.)
  ```
  sudo su
  cd
  ```

## Aşağıdaki komutlarla sunucumuzdaki güncellemeleri, yükseltmeleri kontrol ediyoruz, ve gerekli olan bağımlılıkları kütüphaneleri indiriyoruz. sondaki -y işareti gelen onay işlemlerini otamatik olarak onaylanmasını sağlayacaktır.

  ```
 sudo apt update && sudo apt upgrade -y

  ```
  ```
sudo apt-get install curl
  ```
## Docker kurulumu
```
sudo apt install docker.io
```
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
```
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```
## Tarayıcınıza ip adresi kısmını değiştirerek aratıyoruz ve güvenli değil ilerle diyip ilerliyoruz ve satake yapıyoruz.
```
https://ıpadresi:8080
```

```
cd .shardeum
./shell.sh
operator-cli gui start
```
Görüntüleme için 
```
pm2 list
```

## Faucet

[Discord](https://discord.gg/shardeum)

# 1.1 Güncellemesi

## Tarayıcınıza ip adresi kısmını değiştirerek aratıyoruz ve güvenli değil ilerle diyip ilerliyoruz. ve Stop node dedikten sonra remove stake diyip stake yaptığımız tokenleri geri çekiyoruz ve aşağıdaki adımları tekrar uyguluyoruz
```
https://ıpadresi:8080
```
gelen sorulara y diyip diğer işlemlerde sadece enter tuşuna basıyoruz.
```
curl -O https://gitlab.com/shardeum/validator/dashboard/-/raw/main/installer.sh && chmod +x installer.sh && ./installer.sh
```
diğer işlemler aynı olacak

## Tarayıcınıza ip adresi kısmını değiştirerek aratıyoruz ve güvenli değil ilerle diyip ilerliyoruz ve cüzdanımızı bağlayıp tekardan stake  satake yapıyoruz ve satart node diyoruz.
```
https://ıpadresi:8080
```

```
cd .shardeum
./shell.sh
operator-cli gui start
```
Görüntüleme için 
```
pm2 list
```


