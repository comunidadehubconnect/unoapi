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

----------------------------------------------------------------------------

**Manual de Instalação UNOAPI**

</p>
sudo apt update && apt upgrade -y
</p>
sudo apt-get install -y libgbm-dev wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils
</p>
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

```
WEBHOOK_URL=http://localhost:3000/webhooks/whatsapp
WEBHOOK_TOKEN=(Token Plataforna Superadmin)
WEBHOOK_HEADER=api_access_token
IGNORE_GROUP_MESSAGES=false
IGNORE_BROADCAST_STATUSES=false
SEND_CONNECTION_STATUS=false
REJECT_CALLS=mensagem que vai para o cliente
REJECT_CALLS_WEBHOOK=mensagem que vai para o webhook
```
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
```

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

**Atualização UNOAPI**

</p>

cd unoapi-cloud
</p>
git pull
</p>
rm -r node_modules
</p>
rm -r dist
</p>
Confira sempre .env
</p>
</p>

```
WEBHOOK_URL: https://seudominio/webhooks/whatsapp
WEBHOOK_TOKEN: tokenagente
WEBHOOK_HEADER: webhook header name
BASE_URL: current base url to download medias
IGNORE_GROUP_MESSAGE: false to send group messages received in socket to webhook, default true
IGNORE_BROADCAST_STATUSE: false to send stories in socket to webhook, default true
IGNORE_BROADCAST_MESSAGE: false to send broadcast messages in socket to webhook, default false
IGNORE_OWN_MESSAGES: false to send own messages in socket to webhook, default true
IGNORE_CALLS: message to send when receiva a call, default is empty and not reject
WEBHOOK_CALLS_MESSAGE: message to send webook when receive a call, default is empty and not send
SEND_CONNECTION_STATUS: true to send all connection status to webhook, false to send only important messages, default is true
```

</p>
yarn install
</p>
yarn build
</p>
pm2 restart all
</p>

----------------------------------------------------------------------------

**Quer ser experimentar novas features no Unoapi? Utilize o branch develop**

</p>
Antes do git pull, faça o seguinte:
</p>
git checkout develop
</p>
Para voltar para produção 
</p>
git checkout main
</p>

----------------------------------------------------------------------------

----------------------------------------------------------------------------

**Versão Docker**

**Manual de Instalação UNOAPI via Docker**

</p>
mkdir unoapi
</p>
Verifique se codigo copiado está extamente alinhado igual abaixo
</p>

<img src="https://github.com/EngajamentoFlow/unoapi/blob/main/modelo.png" alt="Quepasa-logo" width="1000" />

</p>

nano docker-compose.yml
</p>

```
version: '3'
services:
  app:
    image: clairton/unoapi-cloud:latest
    volumes:
      - ./data:/home/u/app/data
    deploy:
      restart_policy:
        condition: on-failure
    environment:
      BASE_URL: http://ip:9876
      WEBHOOK_URL: https://seudominio/webhooks/whatsapp
      WEBHOOK_TOKEN: tokenagente
      WEBHOOK_HEADER: webhook header name
      BASE_URL: current base url to download medias
      IGNORE_GROUP_MESSAGE: false to send group messages received in socket to webhook, default true
      IGNORE_BROADCAST_STATUSE: false to send stories in socket to webhook, default true
      IGNORE_BROADCAST_MESSAGE: false to send broadcast messages in socket to webhook, default false
      IGNORE_OWN_MESSAGES: false to send own messages in socket to webhook, default true
      IGNORE_CALLS: message to send when receiva a call, default is empty and not reject
      WEBHOOK_CALLS_MESSAGE: message to send webook when receive a call, default is empty and not send
      SEND_CONNECTION_STATUS: true to send all connection status to webhook, false to send only important messages, default is true
```

----------------------------------------------------------------------------

 **Colocando para roda**
 
 docker compose up -d

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
