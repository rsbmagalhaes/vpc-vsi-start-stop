# vpc-vsi-start-stop
Este script foi extraido do blog https://www.ibm.com/cloud/blog/using-ibm-cloud-code-engine-to-turn-virtual-server-instances-on/off-in-an-automated/scheduled-manner que ensina como efetuar start e stop de vsis no VPC utilizando o COde Engine como Job Runner e permitindo inclusive que o mesmo faça schedule do start e stop dos servidores.

Pontos importantes:

- O Dockerfile foi criado de forma leve e para executar o python somente.

- Lembre-se que o Code Engine pode compilar esse repositorio e criar o image e ja subir o container pra voce

- Não se esqueça de criar o secrets com sua API KEY ou com a API Key do service ID que executará o script ( valide as permissoes deste usuário na VSI )

- Crie os configmaps de vsi-id com o id das VSIs que serao desligadas, de action-start e action-stop, conforme descrito na documentação do Blog

- Lembre-se de criar os Jobs de start e Stop.

- Voce tambem tem a opção de criar Subscriptions para agendar a execucao dos Jobs. Basta seguir os passos de criação do event subscriptions.
