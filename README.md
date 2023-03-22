<p align="center">
	<img src="https://github.com/EngajamentoFlow/unoapi/blob/main/unoapi.jpg" alt="Quepasa-logo" width="100" />	
	<p align="center">Quepasa é um software de código aberto, totalmente gratuito, para troca de mensagens com a plataforma Whatsapp</p>
</p>
<hr />
<p align="left">
	<img src="https://telegram.org/favicon.ico" alt="Telegram-logo" width="32" />
	<span>Grupo e Canal Telegram: </span>
	<a href="https://t.me/quepasa_api" target="_blank">Grupo</a>
	<span> || </span>
	<a href="https://t.me/quepasa_channel" target="_blank">Canal</a>
</p>
<hr />
<p align="left">
	<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
	<span>Grupo WhatsaAPP: </span>
	<a href="https://chat.whatsapp.com/Cv5WfmujRzE09yQ6hagYim" target="_blank">Grupo</a>
</p>
----------------------------------------------------------------------------
</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>

**Manual de Instalação Chatwoot+N8N+Quepasa**

----------------------------------------------------------------------------
</p>
Vamos precisar de 3 subdomínios
</p>
1º Chatwoot
</p>
chatwoot.dominio.com.br
</p>
2º N8N
</p>
n8n.dominio.com.br
</p>
3º Quepasa
</p>
quepa.dominio.com.br
</p>
----------------------------------------------------------------------------

**Manual de Instalação ChatWoot**

sudo apt update && sudo apt upgrade
</p>
wget https://get.chatwoot.app/linux/install.sh
</p>
chmod +x install.sh
</p>
./install.sh --install
</p>
Use as opções abaixo
</p>
yes
</p>
chatwoot.dominio.com.br
</p>
contato@dominio.com.br
</p>
yes
</p>
yes
</p>
nano /home/chatwoot/chatwoot/.env 
</p>
Adicione
</p>
----------------------------------------------------------------------------

**Manual de Instalação N8N**

sudo apt update && sudo apt upgrade
</p>
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
</p>
sudo apt-get install -y nodejs
</p>
sudo npm install n8n -g
</p>
npm update -g n8n
</p>
npm install pm2 -g
</p>
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
</p>
sudo apt install ./google-chrome-stable_current_amd64.deb
</p>
sudo nano /etc/nginx/sites-available/n8n
</p>
server {
</p>
  server_name n8n.dominio.com.br;
</p>
  location / {
</p>
    proxy_pass http://127.0.0.1:5678;
</p>
    proxy_http_version 1.1;
</p>
    proxy_set_header Upgrade $http_upgrade;
</p>
    proxy_set_header Connection 'upgrade';
</p>
    proxy_set_header Host $host;
</p>
    proxy_set_header X-Real-IP $remote_addr;
</p>
    proxy_set_header X-Forwarded-Proto $scheme;
</p>
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
</p>
    proxy_cache_bypass $http_upgrade;
</p>
    proxy_buffering off;
</p>
    proxy_cache off;
</p>
  }
</p>
  }
</p>
sudo ln -s /etc/nginx/sites-available/n8n /etc/nginx/sites-enabled
</p>
sudo certbot --nginx
</p>
sudo service nginx restart
</p>
pm2 start n8n --cron-restart="0 0 * * *" -- start
</p>
----------------------------------------------------------------------------

**Manual de Instalação API Quepasa**

git clone https://github.com/sufficit/sufficit-quepasa /opt/quepasa-source
</p>
bash /opt/quepasa-source/helpers/install.sh
</p>
sudo nano /etc/nginx/sites-available/quepasa
</p>
server {
</p>
  server_name quepasa.dominio.com.br;
</p>
  location / {
</p>
    proxy_pass http://127.0.0.1:31000;
</p>
    proxy_http_version 1.1;
</p>
    proxy_set_header Upgrade $http_upgrade;
</p>
    proxy_set_header Connection 'upgrade';
</p>
    proxy_set_header Host $host;
</p>
    proxy_set_header X-Real-IP $remote_addr;
</p>
    proxy_set_header X-Forwarded-Proto $scheme;
</p>
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
</p>
    proxy_cache_bypass $http_upgrade;
</p>
  }
</p>
  }

sudo ln -s /etc/nginx/sites-available/quepasa /etc/nginx/sites-enabled
</p>
sudo certbot --nginx
</p>
sudo service nginx restart
</p>
nano /opt/quepasa-source/src/.env
</p>
Alterar linha 1
</p>
WEBSOCKETSSL=false
</p>
para
</p>
WEBSOCKETSSL=true
</p>
systemctl restart quepasa
</p>
----------------------------------------------------------------------------

**Primeira parte da Instalação Finalizadas**

Acesse:
</p>
chatwoot.dominio.com.br
</p>
n8n.dominio.com.br
</p>
quepa.dominio.com.br/setup
</p>
Faça os cadastros em todos eles
</p>
----------------------------------------------------------------------------
</p>
----------------------------------------------------------------------------

**Instalar NO no N8N**

n8n-nodes-chatwoot
</p>
n8n-nodes-quepasa
</p>
Baixar Workflow
</p>
Disponiveis nesse Github
</p>
----------------------------------------------------------------------------
</p>

**Configue os Worflows no N8N**

**Worflow QuepasaQrcode**

</p>
Acesse seuchatwoot/super_admin e crie um token na opção Platform Apps
</p>
Segundo NO “COLOCANDO DADOS" URL N8N, URL DO QUEPASA, URL CHATWOOT, TOKEN TOKEN PLATFORM APPS
</p>
Coloque suas credenciais NOS PostgreSQL, elas estarão em seu .env na pasta /home/chatwoot/chatwoot
</p>
Ligue seu Workflow e divirta-se 

</p>
----------------------------------------------------------------------------
</p>

**Worflows ChatwootToQuepasa QuepasaToChatwoot**

</p>
Adicione numeros NOS Trigger com numeros correspondente a Workflow
</p>
----------------------------------------------------------------------------

**Criando Seu Bot Agente**

Acesse: chatwoot.dominio.com.br/superadmin
</p>
Crie seu Token Platform Apps
</p>
----------------------------------------------------------------------------

**Crie uma Automação conforme a imagem abaixo**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Automa%C3%A7%C3%A3o.png" alt="Automação" width="1000" />
</p>
----------------------------------------------------------------------------

**Criando sua Caixa de Entrada**

Criar um contato no Chatwoot
</p>
Quepasa Control
</p>
control@quepasa.io
</p>
Envia uma mensagem para Contato Criado
</p>
Quepasa Control
</p>
/qrcode
</p>
Leia QRCODE
</p>
----------------------------------------------------------------------------

**Pronto tudo Funcionando**

----------------------------------------------------------------------------
</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>
----------------------------------------------------------------------------
