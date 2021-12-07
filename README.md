```
ssh-keygen -t rsa
docker ps
docker cp ~/.ssh/id_rsa.pub id-container:/git-server/keys
docker restart id-container 
ssh git@0.0.0.0 -p 2222 - проверка подключения, пишет ключ подошел и сбрасывает подключение
docker cp ~/test.git c35435d8f294:/git-server/repos
git clone ssh://git@0.0.0.0:2222/git-server/repos/test.git
```

![Server](/proofs/server-hook.png)

![Иллюстрация к проекту](/proofs/pre-commit.png)

![Иллюстрация к проекту](/proofs/client-message.png)