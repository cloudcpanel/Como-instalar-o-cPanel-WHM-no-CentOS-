# Como-instalar-o-cPanel-WHM-no-CentOS-

Como instalar o cPanel em um servidor dedicado ou servidor cloud é bastante simples. O cPanel é o painel de controle para hospedagem de sites mais utilizado da atualidade.

O cPanel é composto, basicamente, por duas partes:

WHM , que é o módulo da revenda de hospedagem , aonde pode-se configurar todo o servidor, criar contas de hospedagem e fazer todo o gerenciamento

cPanel , que é o módulo do cliente , aonde se pode criar bancos de dados, contas de e-mail, gerenciar arquivos, etc.
A licença do cPanel tem um custo mensal. Isto varia de acordo com cada empresa. Licenças para servidores cloud (ou servidores VPS) são mais baratas do que as licenças para servidores dedicados. Primeiramente, precisaremos ter um servidor com acesso root (administrador), rodando Linux CentOS. Usaremos o Putty para realizar a conexão SSH ao servidor. Veja aqui como usar o Putty para se conectar ao servidor linux.

## yum install -y gcc gcc-c++ gettext strace automake strace64 ;
## yum install -y gdb bison libtool tar zip perl screen tcp_wrappers-devel wget ;

Em seguida, realize os seguintes passos:
# screen -S cpanel-install # Abre um novo terminal
# mkdir /home/cpins
# cd /home/cpins
# wget http://layer1.cpanel.net/latest
# sh latest

Explicando:
Como a instalação do cPanel demora um pouco, é recomendado que seja instalado em background ou em screen. Com o comando screen é possível rodar vários terminais em um só.

Para sair do terminal que foi aberto pressione Ctrl+a e Ctrl+d.

Para visualizar os terminais aberto com o comando screen:
# screen -ls # Lista os terminais

Para acessar o terminal novamente, execute:
# screen -r cpanel-install

Ou pelo PID do processo: 
# screen -r 8302

Sobre mais detalhes do comando screen, consulte o manual:
man screenAo terminar a instalação, basta acessar o painel WHM pelo browser:
http://IP-DO-SERVIDOR:2086/

Caso ainda não possua uma licença do cPanel, você pode conseguir uma licença trial (por 15 dias) no site https://www.cpanel.net/store 
