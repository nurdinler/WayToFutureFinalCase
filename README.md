# 💻 Final Case 💻
## Eczacıbaşı Way To Future Bootcamp Bitirme Projesi

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of Contents

- [Adım1](#Adım1)
- [Adım2](#Adım2)
- [Adım3](#Adım3)
- [Adım4](#Adım4)
- [Adım5](#Adım5)
- [Adım6](#Adım6)
- [Adım7](#Adım7)
- [Adım8](#Adım8)
- [Adım9](#Adım9)
- [Adım10](#Adım10)
- [Adım11](#Adım11)
- [Adım12](#Adım12)
- [Adım13](#Adım13)
- [Adım14](#Adım14)
- [Adım15](#Adım15)
- [Adım16](#Adım16)
- [Adım17](#Adım17)
- [Adım18](#Adım18)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Adım1
  <i>Bu adımda KONYA routerda kullanılmak üzere kurum tarafından 172.16.42.0/24 IP adres aralığı verilmiştir. Bu routera bağlı  SW2 ağı için 100 kullanıcı, SW3 ağı için de 60 kullanıcı olacağı bilinmektedir. Buna göre ilk IP’ler Gateway olacak  şekilde ağları bölümleyip, PC’lere 2. IP adreslerini veriniz.</i> <br>
  <p align="center">
    <img src="https://github.com/nurdinler/WayToFutureFinalCase/blob/main/images/244513617-72600317-b8f3-488d-9198-3edb95f8a7ca.png">
    <p> Öncelikle KONYA ağı oluşturuldu, IP bölümlemesi yapılacak olan ağlar belirlendi.
  </p>
  Daha sonra IP bölümlemesi için büyük olan ağdan başlanıldı. IP 32 bitlik bir sayı olduğundan 2'nin kuvvetleri şeklinde bölünebilir, 100 IP ihtiyacı olan bir IP için 128 IP bulunan bir aralık belirlenebilir.<i> Böylece ilk ağın network adresi  172.16.42.0 subneti ise /25 olmuştur </i> Bu ağda 172.16.41.1 gateway olarak ayarlandı, PC-1 bilgisayarına ise 172.16.42.2 ip adresi verildi.
  <h3> Router Ayarları <h3>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/078d85b5-ef8b-498e-966a-559acafe35df">
    <p> Konya routerının interfacelerine ip bilgileri girildi.
  </p>

## Adım2
  <i>ANKARA-KONYA ve IZMIR routerları birbirleri ile EIGRP 100 routing protocolü ile haberleşecek şekilde  yapılandırın.</i>
 Her bir routerda yapılan konfigurasyonlar aşağıda verilmiştir.
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/6cda2393-4039-47b5-9734-1b0080e635bf">
    <p> Konya routerında eigrp protokolü kurulumu yapıldı,network ve komşuluklar tanımlandı
  </p>
   <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/35a2993f-5ff4-4189-9568-50f5c8e20c94">
    <p> İzmir routerında eigrp protokolü kurulumu yapıldı,network ve komşuluklar tanımlandı
  </p>
  <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/10b6241b-dd05-4ab2-a72c-cb1115402c79">
    <p> Ankara routerında eigrp protokolü kurulumu yapıldı,network ve komşuluklar tanımlandı
  </p>


## Adım3
  <i>IZMIRe bağlı switche ağ dışından da erişilebilecek şekilde telnet ile erişim yapılmasını sağlayınız.</i>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/0825f1fa-ed27-45e4-9e5c-6784485f76ae">
    <p> İzmir switchine hostname verildi ve bağlantı aynı anda 5 kişinin bağlanabileceği şekilde sınırlandırıldı.
  </p>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/49362bec-8bf3-47c6-ba86-7611263f5dd2">
    <p> Telnet bağlantısına açıldı ve şifre istenmemesi için ayarlandı.
  </p>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/935a9e92-5346-4ca6-84e5-304764d21c49">
    <p> Konya ağındaki bilgisayarın switch telnet arayüzüne bağlanabildiği görülmektedir.
  </p>

  ## Adım4
   <i>VAN Routera bağlı switchlerin yeterli gelmediği görülmüş ve buna göre yeni bir switch (SW4) alınmıştır. Bu yeni  switchi hem SW6’ya hem de SW5’e bağlayınız. <i>
      <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/e6530002-8096-4ea6-a343-37392b7e1c0d">
    <p> SW4 şekilde görüldüğü biçimde bağlanmıştır ve aşağıdaki trunk konfigurasyonu switchlere uygulanmıştır.
  </p>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/a7408e58-cb19-4f14-90e3-778c50d2a33d">
  </p>
     
  ## Adım5
  <i>SW4-SW5 ve SW6 arasında SW6’yı VTP server olacak şekilde yapılandırın ve aşağıdaki VLANları oluşturunuz.</i>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/ec3821d5-95b7-42c7-8cfa-9ed1a50c11af">      
  </p>
   <b> VTP (VLAN Trunking Protocol), Cisco switch'ler arasında VLAN bilgilerini otomatik olarak paylaşmak için kullanılan bir protokoldür. VTP, VLAN oluşturma, düzenleme ve silme gibi VLAN yönetim işlemlerini kolaylaştırır. <br>
       VTP Server (VTP sunucusu), VTP yönetimi için sorumluluk taşıyan bir Cisco switch'dir. </b>
     <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/40ebeebd-846e-4179-bcff-53b0e4755611"> 
       <p>VTP Server tanımlandı
  </p>
     <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/6443e7f6-bd4c-4b52-b0c9-7e7f8fc63213"> 
       <p>Vlanlar tanımlandı
  </p>
        <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/aa9a4f8e-1e58-4ae7-9679-16f53007d2ff"> 
       <p>Vlanlaın ip adresleri tanımlandı
  </p>
         
  ## Adım6
  <i> SW5’in tüm portlarının VLAN 20 üyesi olmasını, 
      SW4’in 1-10 portlarını VLAN 10 üyesi
      SW4’ün 11-20 portlarını VLAN 30 üyesi yapınız. 
      PC1’i VLAN 10’a ; Misafir PC’yi de VLAN 30’a ait porta bağlayınız. <i>
    <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/c15443e6-ccdc-4596-a50a-c33e3b53466a"> 
       <p>Vlanların interfaceler üzerinden bağlantıları sağlandı
  </p>
     <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/f95b8426-78b3-4239-a3b2-339eba1e7cf2"> 
       <p>Vlanların interfaceler üzerinden bağlantıları sağlandı
  </p>
    
  ## Adım7
<i> SW4-5 ve 6 arasında STP çalışacak ve portun biri tamamen bloklanacaktır. Bu switchler arasında RSTP  etkinleştirin SW4’ün VLAN 10 için; SW5 ‘in VLAN 20 için; SW6’nın VLAN 30 için RootBridge olmasını sağlayın.  </i>
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/7d7d83bd-4da7-44a5-95d1-c37261ba093b"> 
<p>SW4 için
<p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/84a92e69-e159-4bc9-b40c-15dace557083"> 
<p>SW5 için
<p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/f4a59451-9c2d-4a2d-84f5-ad6dc2d6fc54"> 
<p>SW6 için
    
## Adım8
  <i> SW4’te son kullanıcıya giden portların hızlı olarak açılmasını sağlayıp. Ayrıca bu switchte max 1 MAC adres  bağlanacak şekilde yapılandırma yapın. Kural ihlali durumunda sadece sonradan bağlanan kişinin bağlantısına  izin vermeyecek şekilde güvenlik uygulayın.  </i>
          <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/3b24931f-de4a-4de0-ae3e-31269de0a261"> 
       <p>SW4 için
         
         
## Adım9
<i> VAN routeri VLAN10 ve VLAN30 için DHCP server olacak şekilde yapılandırın. DNS olarak 192.168.165.8 adresini  ayarlayın.  </i>
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/d4291f61-6ead-422b-9afb-4f029c170aeb"> 
<p>SW4 için
         
## Adım10
<i> VAN ve KAYSERI cihazları birbirleri ile PPP konuşacaklardır. Güvenlik açısından CHAP yapılandırmasını uygulayın </i>
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/9f305029-a5f2-454a-b93e-48ec24fb50f5"> 
<p>PPP ve CHAP yapılandırması
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/7aa53285-b900-407d-a36c-226c32047ae2"> 
<p>Kullanıcı adı ve şifre yapılandırması
        
 ## Adım11
<i> VAN-KAYSERI ve ERZURUM cihazlarının OSPF ile haberleşmesini sağlayın. OSPF için kimlik denetimini  etkinleştiriniz. Ayrıca gereksiz arayüzlere yayın yapılmasını engelleyiniz. </i>
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/137c0b2e-298e-4dd4-a351-11396fc53512"> 
<p>OSPF kurulumu
<p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/f337fe30-356c-4155-b174-a7eb80c4c289"> 
<p>Şifre kurulumu
<br>Bu konfigurasyonlar iki router için de yapıldı.
 <p align="center">
    <img src="https://github.com/nurdinler/finalCase/assets/73022659/ac34a543-c543-4186-8a0e-d91c827e3034"> 
<p>KAyseri routerında OSPF'in çalıştığı görülmekte
  </p>
         
         
## Adım12
<i>ANKARA-ERZURUM arasında Frame-Relay bağlanıtısını kurunuz. </i>
<p align="center">
  <img src="https://github.com/nurdinler/finalCase/assets/73022659/e33be2fe-bb58-41fc-a2e8-544343a3f08e"> 
<p>Ankara için
  </p>
<p align="center">
 <img src="https://github.com/nurdinler/finalCase/assets/73022659/68623870-37cc-44a4-bc8a-ec7fbbc08076"> 
<p>Erzurum için
    </p>
         
## Adım13
<i>Erzurum router’dan internete bağlanmaktayız. Servis sağlayıcı tarafından bize 88.1.1.1 ile 88.1.1.13 IPleri  verilmiştir. Buna göre Dinamik nat yapılandırmasını tamamlayınız. Kurumumuza atanan IP adreslerinden 88.1.1.2  ile 88.1.1.10 aralığını dış havuz olarak kullanınız. </i>
 <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/f311ef98-7c45-4888-a49e-92bce905372f"> 
  <p>
    </p>
  
    
## Adım14
<i>Kurumumuzda IP adresi 192.168.165.100 olan bir web server bulunmaktadır. Bu servere kurum dışından  88.1.1.13 IP’si ile erişilebilmesini sağlayacak şekilde static NAT yapılandırın. Buna göre kurum dışındaki DNS’e  www.erdal.com adresini kayıt ettiriniz.  </i>
     <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/aa86c065-8131-4e09-813c-824ddc463f31"> 
  <p>
    </p>
    
## Adım15
<i> Van router üzerinde bulunan Misafir VLAN için aşağıdaki kısıtlamalara göre bir ACL tanımlayıp filtreleme  sağlayınız.</i>
       <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/31697dbd-1408-4739-9083-c68d9fc8f77b"> 
  <p>
    </p>


## Adım16
<i> Kayseri Routera bağlı Linksys cihazının 192.168.138.0/24 aralığından kablosuz IP dağıtmasını sağlayınız. Ancak  kablosuz ağı mümkün olduğunca güvenlikli hale getiriniz. </i>
     <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/97733845-b4e9-4691-a3d3-f0c56eed6d65"> 
  <p> Öncelikle lapropa wifi adaptörü modülü eklendi
    </p>
      <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/87a92e3f-474b-4436-8a43-443537f882c7"> 
  <p> Laptopın wireless routera bağlandığı görülmektedir.
    </p>
   
       <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/cfeba803-2162-4404-86d1-f064ae8c7883"> 
  <p> Wireless router ayarları
    </p>
     <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/64c8e43b-efee-45f5-a624-0e8a9b38d185"> 
  <p> Wireless router güvenlik ayarları
    </p>

## Adım17
<i>IZMIR’e bağlı PC3’ün, VAN’a bağlı PC1’in internete erişim sorunu vardır. Lütfen bu sorunu çözün. </i>
 <br>
<p>Bu sorunun kaynağı FR Switchte doğru konfigurasyonun yapılmamış olmasıdır.
   <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/ba90dd41-5c14-4766-be02-adf3c643caca"> 
  <p> Frame Relay Ayarı
    </p>
<p> Aynı zamanda Ankara routerında bilinmeyen iplerde Erzurum routerına yönlendirme ayarı da yapılmıştır.
    <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/7457e84e-a050-4829-8022-abeeda03c6b8"> 
  <p> Routing Ayarı
    </p>

## Adım 18
    <i> IZMIR routerda telnet erişimini açıp sadece lokal ağının buna bağlanmasına izin veriniz.</i>
 <p align="center">
   <img src="https://github.com/nurdinler/finalCase/assets/73022659/d9e9785b-f763-450a-99eb-315996d68b95"> 
  <p> İzmir routerında telnetin açılması
    </p>
    




    
    
    
