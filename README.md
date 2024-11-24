bash <(curl -Ls https://raw.githubusercontent.com/FlushT/serv00-sing-box-vmess/main/install_serv00_vmess.sh)

(crontab -l; echo "*/12 * * * * pgrep -x "web" > /dev/null || nohup /home/${USER}/.vmess/web run -c /home/${USER}/.vmess/config.json >/dev/null 2>&1 &") | crontab -

<ARGO_AUTH> = token
(crontab -l; echo "*/12 * * * * pgrep -x "bot" > /dev/null || nohup /home/${USER}/.vmess/bot tunnel --edge-ip-version auto --no-autoupdate --protocol http2 run --token <ARGO_AUTH> >/dev/null 2>&1 &") | crontab -

crontab -l

cat /home/${USER}/.vmess/list.txt

keep_serv00.yml

Settings > Secrets and variables > Actions > Secrets

SSH_ACCOUNTS 
[
  {"ip": "s13.serv00.com", "username": "test", "password": "tzCOu"},
  {"ip": "s13.serv00.com", "username": "abc", "password": "yTev"}
]


CHAT_ID

1282345

TG_TOKEN

803xx8165:AAEOwpSKbxxxpFyuZbbi

keep_serv00_login.yml

Settings -> Secrets and variables -> Actions -> Secrets

SERVERS_JSON

{
    "s13.serv00.com,username1,password1":"s5,10000",
    "s13.serv00.com,username2,password2":"x-ui,30000,;vmess,50000,vmess.abc.xyz,token",
    "s13.serv00.com,username3,password3":"nezha-dashboard,40000;vmess,50000,vmess.abc.xyz,token"
}

