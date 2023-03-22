<p align="center">
	<img src="https://github.com/EngajamentoFlow/unoapi/blob/main/unoapi.png" alt="Quepasa-logo" width="100" />	
	<p align="center">UNOAPI é um software de código aberto, totalmente gratuito, para troca de mensagens com a plataforma Whatsapp</p>
</p>
<hr />
<p align="left">
	<img src="https://telegram.org/favicon.ico" alt="Telegram-logo" width="32" />
	<span>Grupo Telegram: </span>
	<a href="https://t.me/unoapii" target="_blank">Grupo</a>
</p>
<hr />
<p align="left">
	<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
	<span>Grupo WhatsaAPP: </span>
	<a href="https://chat.whatsapp.com/KOc9il7AdQVCG06fTmG3Uh" target="_blank">Grupo</a>
</p>
----------------------------------------------------------------------------
</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>

**Manual de Instalação Chatwoot+UNOAPI**

----------------------------------------------------------------------------
**Manual ChatWoot+UNOAPI**

Vamos precisar de 1 subdomínios

1º Chatwoot
chatwoot.dominio.com.br

app.mdatatelecom.com.br

----------------------------------------------------------------------------

**Manual de Instalação ChatWoot**

sudo apt update && sudo apt upgrade
wget https://get.chatwoot.app/linux/install.sh
chmod +x install.sh
./install.sh --install

Use as opções abaixo.

yes
chatwoot.dominio.com.br
contato@dominio.com.br
yes
yes

nano /home/chatwoot/chatwoot/.env 

#adicione a Linha
WHATSAPP_CLOUD_BASE_URL=http://localhost:9876 

----------------------------------------------------------------------------

**Recompilando seu Chatwoot**

sudo -i -u chatwoot
cd chatwoot
git checkout develop && git pull
bundle
yarn
rake assets:precompile RAILS_ENV=production
RAILS_ENV=production bundle exec rake db:migrate
exit
systemctl daemon-reload
systemctl restart chatwoot.target

----------------------------------------------------------------------------

**Manual de Instalação UNOAPI**

sudo apt update && sudo apt upgrade
git clone https://github.com/clairton/unoapi-cloud
cd unoapi-cloud
chmod 777 data
npm install pm2 -g
yarn install

Cole codigo abaixo

nano .env

WEBHOOK_URL=http://localhost:3000/webhooks/whatsapp
WEBHOOK_TOKEN=(Token Plataforna Superadmin)
WEBHOOK_HEADER=api_access_token
IGNORE_GROUP_MESSAGES=false
IGNORE_BROADCAST_STATUSES=false

yarn build

pm2 start dist/index.js --name UNOAPI
pm2 startup ubuntu -u root
sudo env PATH=$PATH:/usr/bin pm2 startup ubuntu -u root --hp
pm2 save

----------------------------------------------------------------------------

**Acesse ChatWoot**

Caixas de Entrada
Adicionar Caixas de Entrada
Canal do whatsapp

Nome da Caixa de Entrada (Adicione o que desejar)
Número de telefone (+Número de telefone)
ID do número de telefone (+Número de telefone )
ID da Conta de Negócios (Número de telefone )
Chave da API (any)

Print no material Google Drive

https://drive.google.com/drive/folders/1iqnDNIUou-Ly_9-WCI8_8J1Fqe9mrCH-?usp=share_link

----------------------------------------------------------------------------

**Pronto tudo Funcionando**

----------------------------------------------------------------------------
</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>
----------------------------------------------------------------------------
