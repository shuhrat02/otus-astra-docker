# otus-astra-docker (astralinux + vagrant + docker) 
### Создание ВМ Astra Linux Orel с установленным docker:
1. На хостовой машине предварительно должен быть установлен "vagrant" (https://www.vagrantup.com/) & VirtualBox
2. Далее нужно выполнить команду:
```bash
git clone https://github.com/shuhrat02/otus-astra-docker.git
```
3. Перейти в директорию otus-astra-docker и выполнить команду:
```bash
vagrant up
```
4. Теперь можно отойти на 2-3 мин, заварить себе чай и дождаться когда развернется гостевая Astra Linux с docker на борту.
5. В случае возникновения ошибки: 
`"Vagrant attempted to execute the capability 'configure_networks'
on the detect guest OS 'linux', but the guest doesn't                                                                                                        
support that capability. This capability is required for your                                                                                                
configuration of Vagrant. Please either reconfigure Vagrant to                                                                                               
avoid this capability or fix the issue by creating the capability." `
выполните команду: 
```bash
vagrant provision
```
