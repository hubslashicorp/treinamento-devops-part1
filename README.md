![UML](img/LogotipoSlashicorp.png)

# Treinamento DevOps - Part I

Sinta-se à vontade para rodar `Vagrant` ou `Docker` onde quiser!

Em nosso `lab`, para estudar `Linux` e `Docker`, provisionaremos uma VM `Ubuntu-server` no `VirtualBox` com o `Vagrant`.
 
Caso você rode `Windows`, não se preocupe! Também é possivel rodar o terminal `Linux` nele com o `wsl`:

```
How-To: https://docs.microsoft.com/pt-br/windows/wsl/install-win10
```

No nosso, caso utilizaremos o `VirtualBox` sendo assim, de qualquer maneira você pode participar pois,
`VirtualBox`, `Vagrant` e o `Docker` rodam no `Windão`.
 
## RECs:

Git:
``` 
How-To: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
```

VirtualBox:
```
Download: https://www.virtualbox.org/wiki/Downloads
Documentacão: https://www.virtualbox.org/wiki/Documentation
```

Vagrant
```
Download: https://www.vagrantup.com/downloads.html
Documentacão: https://www.vagrantup.com/docs
Boxes: https://app.vagrantup.com/boxes/search
```

Ubuntu 18.04 LTS (ISO)
```
Download: https://ubuntu.com/download/server
Documentacão: https://help.ubuntu.com/
```

Docker
``` 
Download: https://docs.docker.com/engine/install/ubuntu/
Docker Hub: https://hub.docker.com/
```

## Step by Step:

| Item  | Descrição                                |
|-------|------------------------------------------|
|  1.0  |   [lab] Instalando VirtualBox            |
|  2.0  |   [lab] Instalando Vagrant               |
|  3.0  |   Inspecionando Vagranfile               |
|  4.0  |   [lab] Provisionando VM com Vagrant     |
|  5.0  |   Entendendo o GNU/Linux                 |
|  5.1  |   [lab] Principais comandos GNU/Linux    |
|  6.0  |   Entendendo o Docker                    |
|  6.1  |   [lab] Principais comandos Docker       |
|  6.2  |   Entendendo Dockerfile                  |
|  6.3  |   [lab] Construindo primeira imagem      |
|  6.4  |   [lab] Commitando imagem no docker hub  |


## Observação importante:

Em alguns casos o download da `box` Vagrant demora uma eternidade para baixar sendo assim,
caso queira provisionar o ambiente com antecedencia, apos instalar o Git, Virtualbox e o Vagrant, navegue ate o 
repositorio clonado localmente em sua maquina e execute os passos:

1.0 - Realize o clone do repositorio:
```
$ git clone https://github.com/hubslashicorp/treinamento-devops-part1.git
```

2.0 - Acesse o diretório local `treinamento-devops-part1`:
``` 
$ cd treinamento-devops-part1
```

3.0 - Provisionando VM com Vagrant:
``` 
$ vagrant up
```

4.0 - Validando se VM esta Online:
``` 
$ vagrant status
```

5.0 - Desligando VM (`opcional`):
```
$ vagrant halt
```

Mais uma vez, sinta-se à vontade para esclarecer duvidas com relação a instalação e tudo o mais
com seu instrutor.

att;

![UML](img/SlashiCorpSig.png)