# TesteAtlantico
A DevOps test for Istituto Atlantico.

A arquitetura apresentada na imagem example.png para a tarefa 1 é a descrição de um monitoramento open source que é uma alternativa
para o ansible tower da oracle chamado de AWX, com uma adaptação facil a arqquitetura da AWS, pois exitem imagens docker para este
tipo de serviço e que facilitam muito que o serviço entre no ar o mais rapido possivel.

Nesse modelo de projeto, temos a aplicação do playbook com todos os passos de automação nescessarios para que o pipeline de entrega
esteja operacional e host inventory que é a listagem dos servidores ou containers, a depender da arquitetura, a serem utilizados na
resolução do problema estabelecido para ser resolvido.

Obedecendo a ilustração em questão temos que aplicar os 4 passos de entrega do codigo com a listagem dos steps de desenvolvimento e 
o acesso via SSH na porta 22 que foi especificada na tarefa 2 e que tbm contem a as portas 80 e 443 para uso na internet, além da 
conexão com o banco via uma estancia MySQL instalada no RDS da AWS para manter um projeto seguro e com alta disponibilidade que se 
faz nescessario a um time de desenvolvimento remoto.

Com os dados escritos no host inventory e no playbook, o servidor Ansible irá criar de forma automatica todos os steps nescessarios
com o ambiente virtualizado como se pretende ter, isso implicará no uso de outro script de configuração que será criado no terraform
de maneira a facilitar e aumentar a produtividade do ambiente, onde o numero de maquinas e os paramentros de acesso podem serão 
rapidamente implementados.




-DEV 
-QA
-UAT
-PROD

Esses passo são utilizados para organizar o processo de entrega e integração continuas que foi projetado para essa tarefa
com especial atenção a segurança de acesso visto que a ação para o acionamento do passo de desenvolvimento é feito por SSH
atraves do servidor Ansible que está sendo usado para esse fim.

Neste mesmo servidor temos a preocupação com os passos de desenvolvimento em especial com a aceitação do código pelo usuário
e analise de qualidade que considero especialmente importante na etapa de entrega continua.
