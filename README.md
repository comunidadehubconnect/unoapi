<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2023/08/logo-github-cwmkt.svg" alt="DispZap Whats Marketing" width="240" />
<p align="center">Seja bem-vindo ao Guia de atualização do n8n, nodejs e quepasa 🚀</p>
</p>
  
<p align="center">
<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
<span>Grupo WhatsaAPP: </span>
<a href="https://link.cwmkt.com.br/grupo-whats" target="_blank">Grupo</a>
</p>

<hr />
<hr />

</p>

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>

**PIX CNPJ**

```
45959142000119	
```

</p>

<hr />
<hr />


**Manual de Instalação ChatWoot**

sudo apt update && apt upgrade -y
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
yes para todos
</p>
<hr />

**Alterando Idioma e ativando sua tela de cadastro**

</p>
cd /home/chatwoot/chatwoot
</p>
nano .env
</p>
Altere a linha
</p>
DEFAULT_LOCALE=pt_BR
</p>
ENABLE_ACCOUNT_SIGNUP=true
</p>
sudo systemctl restart chatwoot.target
</p>
Acesse: seudominio.com.br
</p>
Faça seu cadastro
</p>

<hr />

**Habilitando configurações ocultas do Chatwoot**

</p>
No banco de dados PostgreSQL
</p>
sudo -u postgres psql
</p>
\c chatwoot_production
</p>
update installation_configs set locked = false;
</p>
\q
</p>

<hr />

**NOMES CHATWOOT TERMOS E POLITICA DE PRIVACIDADE**

**Acesse super Admin**
</p>
https://seudominio.com.br/super_admin
</p>
Opção>installation_configs
</p>
LOGO
</p>
LOGO_THUMBNAIL
</p>
NOMES CHATWOOT:
</p>
Alterando nomes na plataforma
</p>
INSTALLATION_NAME
</p>
BRAND_NAME
</p>
TERMOS E POLITICA DE PRIVACIDADE
</p>
TERMS_URL
</p>
PRIVACY_URL
</p>
BRAND_URL
</p>
WIDGET_BRAND_URL
</p>

<hr />
<hr />

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
WEBHOOK_URL=https://urldosite/webhooks/whatsapp
WEBHOOK_TOKEN=Coloque Token Agente aqui
WEBHOOK_HEADER=api_access_token
BASE_URL=http://localhost:9876
IGNORE_GROUP_MESSAGES=false
IGNORE_BROADCAST_STATUSES=true
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
</p>

**EXECUTE COMANDO ABAIXO PARA NÃO CAIR QUANDO REINICIAR A VPS**

</p>
sudo pm2 startup ubuntu -u root && sudo pm2 startup ubuntu -u root --hp /root && sudo pm2 save
</p>
</p>

<hr />
<hr />

**Recompilando seu Chatwoot**

</p>
sudo -i -u chatwoot
</p>
cd chatwoot
</p>
git checkout master && git pull
</p>
rvm reinstall ruby-3.1.3
</p>
rvm use 3.1.3 --default
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

<hr />
<hr />

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

<hr />
<hr />

**Pronto tudo Funcionando**

<hr />
<hr />

**Gostou do Tutorial? Faça sua Contribuição**

<img src="https://github.com/EngajamentoFlow/quepasa/blob/main/Contribui%C3%A7%C3%A3o.png" alt="Quepasa-logo" width="200" />
</p>

**PIX CNPJ**

```
45959142000119	
```
<hr />
