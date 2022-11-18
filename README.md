# Script de Firewall para Desktop Linux

1 - Copiar o script para /etc/init.d/

2 - Conceder Permissão de Execução: chmod +x firewall

3 - Criar Soft Link dentro de /etc/rc5.d/: 
	ln -s ../init.d/firewall S21firewall (se estiver dentro do diretório /etc/rc5.d)
  
4 - Iniciar Firewall: /etc/init.d/firewall start

5 - Verificar Funcionamemto: iptables -L

Funcionamento Esperado:

Bloqueia todas as entradas, exceto as que são respostas a uma saída anterior.
   OUTPUT < INPUT

Permite entradas loopback.

OBS: comandos com SUDO.
