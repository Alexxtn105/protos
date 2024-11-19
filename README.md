# Проект для генерации кода go-файлов из .proto-файлов (для gRPC)
Для генерации go-файлов из .proto-файлов:
1. Установить [protoc](https://github.com/protocolbuffers/protobuf/releases)

2. Прописать путь к папке `bin` в переменной окружения `PATH`;

3. Проверить работоспособность командой:
```bash
protoc --version 
```

4. Для кодогенерации выполнить команду с помощью [task](https://taskfile.dev/installation/): 

```bash
task generate
```

## При каждом обновлении proto-файла нужно изменять тег (установить нужную версию), 
иначе в проекте обновления не появятся:
```bash
git tag -a v1.0 -m "my version 1.0"
```
## Чтобы помотреть текущий тег:
```bash
git tag
```

## После обновления proto, обновить версию в SSO:
```bash
go get github.com/Alexxtn105/protos
```
