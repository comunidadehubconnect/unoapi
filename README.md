<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2023/08/logo-github-cwmkt.svg" alt="DispZap Whats Marketing" width="240" />
<p align="center">Seja bem-vindo ao Guia do Chatwoot+UnoAPI 🚀</p>
</p>
  
<p align="center">
<img src="https://whatsapp.com/favicon.ico" alt="WhatsAPP-logo" width="32" />
<span>Grupo WhatsaAPP: </span>
<a href="https://link.cwmkt.com.br/grupo-whats" target="_blank">Grupo</a>
</p>

<hr />
<hr />

<details>
<summary>Manual de Instalação Chatwoot</summary>

### Atualize sua máquina com os últimos pacotes

```bash
sudo apt update && apt upgrade -y
```

### Baixe o instalador automático do Chatwoot

```bash
wget https://get.chatwoot.app/linux/install.sh
```

### Execute a permisão no arquivo install.sh

```bash
chmod +x install.sh
```

### Inicie a instalação, digite "yes" para SSL, em seguida digite seu dominio e prossiga confimando com yes.
### Esse processo vai levar média ~ 15

  ```bash
./install.sh --install
  ```

Use as opções abaixo

yes

app.dominio.com.br

contato@dominio.com.br

yes para todos

### Alterando Idioma e ativando sua tela de cadastro

```bash
nano /home/chatwoot/chatwoot/.env
```

Altere a linha:

`DEFAULT_LOCALE=pt_BR` para `ENABLE_ACCOUNT_SIGNUP=true`

```bash
systemctl daemon-reload && systemctl restart chatwoot.target
```

Acesse: app.seudominio.com.br

Faça seu cadastro

### Habilitando configurações ocultas do Chatwoot no banco de dados PostgreSQL

```bash
sudo -i -u postgres psql
\c chatwoot_production
```

```bash
update installation_configs set locked = false;
```

```bash
\q
```

</details>

<details>
  
<summary>Manual de Instalação UNOAPI</summary>


## Instalando API UNO

```bash
sudo apt update && apt upgrade -y
```

```bash
sudo apt-get install -y libgbm-dev wget unzip fontconfig locales gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils
```

```bash
git clone https://github.com/clairton/unoapi-cloud
```

```bash
cd unoapi-cloud
```

```bash
chmod 777 data
```

```bash
npm install pm2 -g
```

```bash
yarn install
```

Cole codigo abaixo

```bash
nano .env
```

```bash
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

```bash
yarn build
```

```bash
pm2 start dist/index.js --name UNOAPI
```

## EXECUTE COMANDO ABAIXO PARA NÃO CAIR QUANDO REINICIAR A VPS

```bash
sudo pm2 startup ubuntu -u root && sudo pm2 startup ubuntu -u root --hp /root && sudo pm2 save
```


</details>

<details>

<summary>Rebuild Chatwoot</summary>

## Recompilando seu Chatwoot

```bash
sudo -i -u chatwoot
```

```bash
cd chatwoot
```

```bash
git checkout master && git pull
```

```bash
bundle
```

```bash
yarn
```

```bash
rake assets:precompile RAILS_ENV=production
```

```bash
RAILS_ENV=production bundle exec rake db:migrate
```

```bash
exit
```

```bash
systemctl daemon-reload
```

```bash
systemctl restart chatwoot.target
```

</details>


## Acesse ChatWoot

Caixas de Entrada

Adicionar Caixas de Entrada

Canal do whatsapp

Nome da Caixa de Entrada (Adicione o que desejar)

Número de telefone (+Número de telefone)

ID do número de telefone (+Número de telefone )

ID da Conta de Negócios (Número de telefone )

Chave da API (any)

Print abaixo

<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/copy_token.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/create_channel.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/create_contact.png" alt="Quepasa-logo" width="1000" />
<img src="https://github.com/clairton/unoapi-cloud/blob/main/examples/chatwoot/prints/read_qrcode.png" alt="Quepasa-logo" width="1000" />
