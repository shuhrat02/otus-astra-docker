# otus-astra-docker (astralinux + vagrant + docker) 
### Создание ВМ Astra Linux Orel с установленным docker:
1. На хостовой машине предварительно должен быть установлен "vagrant" (https://www.vagrantup.com/) & VirtualBox
1. Далее нужно выполнить команду:
`git clone https://github.com/shuhrat02/otus-astra-docker.git`
1. Перейти в директорию otus-astra-docker и выполнить команду:
`vagrant up`
1. Теперь можно отойти на 2-3 мин, заварить себе чай и дождаться когда развернется гостевая Astra Linux с docker на борту.
2. В случае возникновения ошибок выполните команду: `vagrant provision`
