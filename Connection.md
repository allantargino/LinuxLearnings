Ao utilizar muitas VMs em uma nuvem pública, é um problema gerenciar o acesso via SSH de várias máquinas. Uma maneira interessante que descobri para facilitar o acesso (essencialmente se usar par de chaves assimétricas), é ter um arquivo de configuração para fazer a conexão mais automática.

```shell
## Criar arquivo:
vi $HOME/.ssh/config
```

Arquivo de configuração

Host masterKub<br>
  HostName maquinaallan.eastus.cloudapp.azure.com<br>
  User userlinux<br>
  Port 22<br>
  IdentityFile ~/.ssh/key<br>
    
    
```shell
## Para se conectar:
ssh masterKub
```

