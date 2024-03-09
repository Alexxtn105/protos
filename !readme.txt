Для генерации go-файлов из .proto-файлов выполнить команду. Должен быть установлен task, см.: https://taskfile.dev/installation/  :

task generate


При обновлении нужно изменить тег (установить нужную версию):
 git tag -a v1.0 -m "my version 1.0"

 помотреть текущий тег:
 git tag


 После обновления обновить версию в SSO^
 Затем нужно обновить версию в SSO:

 go get github.com/Alexxtn105/protos