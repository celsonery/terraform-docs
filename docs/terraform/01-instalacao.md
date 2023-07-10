# Instalação

###### Sistemas Suportados
- MacOS
- Windows
- Linux
- FreeBSD
- OpenBSD
- Solaris

###### Instalação em distribuições linux OpenSUSE

```bash
$ sudo zypper in terraform
```

###### Instalação via repositório

> https://developer.hashicorp.com/terraform/downloads

Em Debian/Ubuntu
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
```

CentOS/RHEL
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
sudo yum -y install terraform
```

Fedora
```bash
sudo dnf install -y dnf-plugins-core
sudo dnf config-manager --add-repo https://rpm.releases.hashicorp.com/fedora/hashicorp.repo
sudo dnf -y install terraform
```

Amazon Linux
```bash
sudo yum install -y yum-utils shadow-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo
sudo yum -y install terraform
```

###### Caso sua distro não suporte via gerenciador de pacotes, faça o download o binário e descompacte.

!['Download Terraform Binário'](../imgs/download-terraform-binario.png)

Irá descompactar um arquivo executável com nome **terraform**, copie-o para um local de fácil execução incluído no seu **PATH**

```bash
$ sudo cp terraform /usr/local/bin
```