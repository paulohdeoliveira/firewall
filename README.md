# Script de Firewall para Desktop Linux

1 - Copiar o script para /etc/init.d/

2 - Conceder Permissão de Execução: chmod +x firewall.sh

3 - Criar Soft Link dentro de /etc/rc5.d/: <br>

	cd /etc/rc5.d
	ln -s ../init.d/firewall.sh S21firewall.sh
  
4 - Iniciar Firewall: /etc/init.d/firewall.sh start

5 - Verificar Funcionamento: iptables -L

Funcionamento Esperado:

Bloqueia todas as entradas, exceto as que são respostas a uma saída anterior.

Permite entradas loopback.

OBS: comandos com SUDO.
