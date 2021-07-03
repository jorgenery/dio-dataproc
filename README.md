# dio-dataproc
Criando um Ecossistema Hadoop Totalmente Gerenciado com Google Cloud Dataproc

### Criando Cluster
gcloud beta dataproc clusters create cluster-procdados --enable-component-gateway --region southamerica-east1 --zone southamerica-east1-c --master-machine-type n1-standard-4 --master-boot-disk-size 500 --num-workers 2 --worker-machine-type n1-standard-4 --worker-boot-disk-size 500 --image-version 2.0-ubuntu18 --optional-components JUPYTER,ZOOKEEPER --project digitalonecloud
### Pegando Arquivos
git clone https://github.com/jorgenery/dio-dataproc.git
### Identificando gs
gsutil ls
### Criando Job
![image](https://user-images.githubusercontent.com/28833671/124360532-d402dc00-dc00-11eb-8f38-577667f84ebd.png)
### Rodando Job
gcloud dataproc jobs wait job-11c0563f --project digitalonecloud --region southamerica-east1
### Pegando Resultado
gsutil -m cp -r "gs://dataproc-staging-sa-east1-464278246124-uyyjwsi3/dio-dataproc/resultado/"
