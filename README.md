## Gitlab Runner With Ansible
### Vagrant oluşturulan bir sanal makinede docker ile bir gitlab runner oluşturur ve tüm bu süreci Ansible ile yürütür.

```
vagrant up
```
komutu ile bir sanal makine oluşturulurile ayağa kaldırılır ve sanal makine oluşmuş olur. Vagrantfile dosyasında belirtildiği üzere *192.168.56.10* adresinden SSH ile bağlantı yapılabilir.

```
ansible-playbook -i inventory.yml provision.yml
```
komutu çalıştırılarak sanal makinede Docker kurulumu yapılıp Gitlab Runner imajı indirilerek çalıştırılır.

Yeni bir Gitlab runner register etmek için
```
./register-runner.sh
``` 
komutu çalıştırılır. Dosya, gitlab runner için gereken 'regisration token'i isteyecektir. Token girildikten sonra Gitlab Runner çalışacaktır.
