# PKS Cheat Sheet（Opearation編）

### Planの一覧
pks plans  

### Cluster作成
pks create-cluster <CLUSTER-NAME> --external-hostname <CLUSTER-FQDN> --plan <PLAN-NAME>  
pks create-cluster <CLUSTER-NAME> --external-hostname <CLUSTER-FQDN> --plan <PLAN-NAME> --network-profile <NETWORKPROFILE>  
※External hostnameは後から変更不可なので注意  

### Clusterの一覧
pks clusters  

### Cluster情報の取得
pks cluster <CLUSTER-NAME>  

### kubeconfig取得
pks get-credentials <CLUSTER-NAME>  

### Cluster削除
pks delete-cluster <CLUSTER-NAME>  

### ClusterのResize（Worker Nodeを増やす）
pks resize <CLUSTER-NAME> --num-nodes <NUM-OF-NODES>  
※スケールアップをする場合は利用しているPlanの内容を変更する必要あり