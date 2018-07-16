# LINUX
Devido a falta de memória e algum grau de preguiça, ficam aqui alguns arquivos e dicas sobre o sistema operacional do pinguim que esqueço com certa frequência.


## Comandos terminal

### Exibir configurações do sistema
inxi -Fxz

### Verificar serviços iniciados no boot
rcconf

### Listando arquivos e pastas por tamanho
du -h --max-depth=1 | sort -h

### Alterar o usuário para o user root
su - root

### Comando para atualização total do sistema
aptitude full-upgrade
aptitude safe-upgrade

### Compactação
tar -cf <Nome>.tar <Nome do arquivo ou Diretório>
tar -pczf <Nome do arquivo>.tar.gz <Arquivo ou diretório>
gzip -9 <Nome do arquivo>.tar

### Descompactação
gzip -d <Nome do arquivo>.tar.gz
tar -zxvf <Nome do arquivo>.tar.gz
tar -xvf <Nome do arquivo>.tar
7z x -y <Nome do arquivo>.7z
  
### Permissões
http://www.vivaolinux.com.br/artigo/Entendendo-as-permissoes-no-Linux
chown -R usuário.grupo

### Verificações de sistema
LOG: logwatch
Memória: free
CPU info: cat /proc/cpuinfo 
Informações do sistema: screenfetch


## MySQL

### Acessar via terminal o MySQL
mysql -u <user> -p

### Reiniciar MySQL
./mysql start/stop/restart

### Dump de base de dados
mysqldump nome-do-banco > nome-do-arquivo.sql -h nome-do-servidor-de-banco -u usuario-do-banco -p
