# PKS Cheat Sheet（ログイン編）

### Opsmanへのログイン
ssh ubuntu@\<OPSMAN-FQDN\> -i ./\<KEYPATH\>  

### UAACの接続先設定
uaac target https://\<PKS-FQDN\>:8443 --ca-cert /var/tempest/workspaces/default/root_ca_certificate  

### Admin Tokenの取得
uaac token client get admin -s \<SECRET\>  

### PKS User作成
uaac user add \<USERID\> --emails \<EMAILADDRESS\> -p \<PASSWORD\>  

### UAA Scopeのアサイン
uaac member add \<UAASCOPE\> \<USERID\>  
※PKSで利用可能なUAA SCOPEは3種類(pks.clusters.manage, pks.clusters.admin, pks.clusters.admin.read) 2020/02現在  

### PKSへのログイン
pks login -a \<PKS-API\> -u \<USERNAME\> -k  
