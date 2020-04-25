Kurulum
============

Sırasıyla aşağıdaki yazılımlar kurulmalı ve github token üretilmelidir.

1. [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. [Vagrant](https://www.vagrantup.com/downloads.html)
3. [Git](https://www.git-scm.com)
4. [GitHub API token](https://github.com/settings/tokens) Generate new token'a tıklayarak yeni bir token oluşturulmalıdır. 
5. Yönetici yetkileriyle terminal (komut satırı) açılarak aşağıdaki direktifler uygulanmalıdır.
   
```bash
vagrant plugin install vagrant-hostmanager
git clone https://github.com/kouosl/portalium-kickstarter.git portalium
git clone https://github.com/kouosl/vagrant-portalium.git vagrant-portalium
```

6. Aşağıdaki dizinde bulunan vagrant-local.example.yml dosyasının vagrant-local.yml adıyla kopyası oluşturulmalıdır. 
```
@vagrant-portal/config 
```

7. GitHub api tokenı `vagrant-local.yml` dosyasında aşağıdaki şekilde tanımlanmalıdır.
```
....
github_token: qy6uuqııq8ııqooqwuw78qııqowksjjeoow9oowlw
....
```

8. Vagrant makina çalıştırılarak kurulum başlatlır. Komut vagrant-portal dizininin içinde çalıştırılmalıdır.
```bash
vagrant up
```
   
Vagrant makina kurulumu tamamlandıktan sonra aşağıdaki bağlantılardan uygulamaya erişilebilir.
* frontend: http://portalium/
* backend: http://portalium/admin
* api: http://portalium/api

Terminal'den (komut satırı) sanal makinaya SSH erişimi için;
```bash
vagrant ssh
```
   
Hariçi bir programla (putty vb.) ssh bağlantısı için bilgiler;
* ip : 192.168.83.137
* user : vagrant
* password : vagrant

Private key ile bağlatı için;
```bash
ssh -i .vagrant/machines/portalium/virtualbox/private_key vagrant@portalium
```
