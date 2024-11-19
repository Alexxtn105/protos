Для генерации go-файлов из .proto-файлов:
1. Устанвовить protoc:
https://github.com/protocolbuffers/protobuf/releases

2. Прописать путь к папке bin в переменной окружения PATH;

3. Проверить работоспособность командой:
protoc --version 

4. Для кодогенерации (с помощью task) выполнить команду: 

task generate

ПРИМЕЧАНИЕ: утилита task по адресу: https://taskfile.dev/installation/


При каждом обновлении proto-файла нужно изменять тег (установить нужную версию), 
иначе в проекте обновления не появятся:

git tag -a v1.0 -m "my version 1.0"

Чтобы помотреть текущий тег:
git tag


После обновления proto, обновить версию в SSO:

 go get github.com/Alexxtn105/protos
