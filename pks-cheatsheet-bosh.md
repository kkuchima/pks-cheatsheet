# PKS Cheat Sheet（BOSH操作）

### BOSH Env設定
bosh alias-env \<ENV-NAME\> -e \<BOSHDIRECTOR-IP\> --ca-cert /var/tempest/workspaces/default/root_ca_certificate  

### BOSH Login
bosh -e \<ENV-NAME\> login  
※認証情報はOps ManagerのCredentialページに記載あり

### BOSH task一覧
bosh -e \<ENV-NAME\> tasks  

### BOSH Taskキャンセル
bosh -e \<ENV-NAME\> cancel-task \<TASK-ID\>

### BOSH Recreate
bosh recreate -d \<DEPLOYMENT-ID\>

### BOSH VM停止
bosh -e \<ENV-NAME\> -d \<DEPLOYMENT-ID\> stop \<VM-ID\>

### BOSH SSH
bosh -e \<ENV-NAME\> -d \<DEPLOYMENT-ID\> ssh \<VM-ID\>
