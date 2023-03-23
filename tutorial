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

</p>
Vamos precisar de 1 subdomínios
</p>
1º Chatwoot
</p>
chatwoot.dominio.com.br
</p></p>
app.mdatatelecom.com.br
</p>
----------------------------------------------------------------------------
</p>

**Manual de Instalação ChatWoot**

</p>
sudo apt update && sudo apt upgrade
</p>
wget https://get.chatwoot.app/linux/install.sh
</p>
chmod +x install.sh
</p>
./install.sh --install
</p>
Use as opções abaixo.
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
#adicione a Linha
</p>
WHATSAPP_CLOUD_BASE_URL=http://localhost:9876 
</p>

----------------------------------------------------------------------------
</p>

**Recompilando seu Chatwoot**

</p>
sudo -i -u chatwoot
</p>
cd chatwoot
</p>
git checkout develop && git pull
</p>
bundle
</p>
yarn
</p>
rake assets:precompile RAILS_ENV=production
</p>
RAILS_ENV=production bundle exec rake db:migrate
</p>
exit
</p>
systemctl daemon-reload
</p>
systemctl restart chatwoot.target
</p>

----------------------------------------------------------------------------
</p>

**Manual de Instalação UNOAPI**

</p>
sudo apt update && sudo apt upgrade
</p>
</p>
git clone https://github.com/clairton/unoapi-cloud
</p>
cd unoapi-cloud
</p>
chmod 777 data
</p>
npm install pm2 -g
</p>
yarn install
</p>
Cole codigo abaixo
</p>
nano .env
</p>
WEBHOOK_URL=http://localhost:3000/webhooks/whatsapp
</p>
WEBHOOK_TOKEN=(Token Plataforna Superadmin)
</p>
WEBHOOK_HEADER=api_access_token
</p>
IGNORE_GROUP_MESSAGES=false
</p>
IGNORE_BROADCAST_STATUSES=false
</p>
SEND_CONNECTION_STATUS=false
</p>
IGNORE_CALLS=aqui sua mensagem
</p>
yarn build
</p>
pm2 start dist/index.js --name UNOAPI
</p>
pm2 startup ubuntu -u root
</p>
sudo env PATH=$PATH:/usr/bin pm2 startup ubuntu -u root --hp
</p>
pm2 save
</p>

----------------------------------------------------------------------------
</p>

**Acesse ChatWoot**

</p>
Caixas de Entrada
</p>
Adicionar Caixas de Entrada
</p>
Canal do whatsapp
</p>
Nome da Caixa de Entrada (Adicione o que desejar)
</p>
Número de telefone (+Número de telefone)
</p>
ID do número de telefone (+Número de telefone )
</p>
ID da Conta de Negócios (Número de telefone )
</p>
Chave da API (any)
</p>
Print abaixo

<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/copy_token.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/create_channel.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/create_contact.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/read_qrcode.png" alt="Quepasa-logo" width="1000" />

----------------------------------------------------------------------------
</p>

**Pronto tudo Funcionando**

</p>
----------------------------------------------------------------------------
</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>
----------------------------------------------------------------------------
