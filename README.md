<p align="center">
	<img src="https://github.com/EngajamentoFlow/unoapi/blob/main/unoapi.png" alt="Quepasa-logo" width="100" />	
	<p align="center">UNOAPI é um software de código aberto, totalmente gratuito, para troca de mensagens com a plataforma Whatsapp</p>
</p>
<hr />
<p align="left">
	<img src="https://telegram.org/favicon.ico" alt="Telegram-logo" width="32" />
	<span>Grupo Telegram: </span>
	<a href="https://t.me/unoapi" target="_blank">Grupo</a>
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

**PIX CNPJ**

```
45959142000119	
```

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
WEBHOOK_TOKEN=Coloque Token Agente aqui
WEBHOOK_HEADER=api_access_token
BASE_URL=current base url to download medias
PORT=the http port
IGNORE_GROUP_MESSAGES=false
IGNORE_BROADCAST_STATUSES=false
IGNORE_BROADCAST_MESSAGES=false
IGNORE_HISTORY_MESSAGES=true
IGNORE_OWN_MESSAGES=false
IGNORE_YOURSELF_MESSAGES=true
COMPOSING_MESSAGE=true
REJECT_CALLS=Olá! Sinto muito, mas não consigo responder chamadas neste momento. Por favor, deixe uma mensagem com seu nome e número de telefone, e eu retornarei assim que possível. Obrigado!
REJECT_CALLS_WEBHOOK=Olá! Recebi sua chamada, mas não consigo atendê-la pessoalmente no momento. No entanto, sua mensagem é importante para mim. Por favor, deixe seu nome, número de telefone e motivo da ligação, e entrarei em contato o mais breve possível. Agradeço sua compreensão!
SEND_CONNECTION_STATUS=true
UNOAPI_BASE_STORE=./data
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
</p>

----------------------------------------------------------------------------
----------------------------------------------------------------------------


</p>

**Pronto tudo Funcionando**

</p>


----------------------------------------------------------------------------

----------------------------------------------------------------------------


</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>

**PIX CNPJ**

```
45959142000119	
```
----------------------------------------------------------------------------
