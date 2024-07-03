![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0b7b09e2-f6c2-420e-b168-dcd69ae66e3d)# AZURE PIPELINES - Integracao-e-entrega-continua-YAML

Criar pipeline através de código com yaml

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/03d0b779-ab46-464b-b90c-659fe83aed75)


YAML é um formato de serialização de dados legíveis para humanos é um acrônimo para Ain't Markup Language .YAML não é linguagem de marcação , ele é um substituto ao xml como 
linguagem de marcação, seu propósito é ser uma linguagem mais rápida e mais fácil a leitura por nós seres humanos e nossa máquina. 

O nosso time pode alterar a confuguração do pipeline sem nem mesmo entrar no azure devops.

Características e sintaxe:

Usamos ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/81820f8d-3faf-4444-be86-97b7cf99a339)

Na sua estrutura utilizamos ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/01b5d808-fae8-442e-8ab9-9cc8964dfc06)

Podemos ter listas: ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8ee63494-d15f-4c41-8ce2-686ab25c1753)

Podemos ter vetores associados: <img width="589" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/64fca748-2e7d-4d62-831e-42cbedcdd365">

## Conceitos do Pipeline usando YAML

Vamos falar sobre os conceitos presentes no pipelines, no processo de integração contínua. Vimos eles aplicados ao editor clássico, e agora vão mostrar quanto ao  YAML.
Muda um pouco, o YAML nos dá mais liberdade e possibilidades do que o modelo com interface visual.

Quando trabalhamos com yaml precisamos do arquivo.yml

<img width="298" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/4e925f34-3a55-4c7c-ab76-c19fae82e671">

E toda a nossa configuração de pipeline ficará nesse arquivo, estando o arquivo lá configurado logo após o código ser submetido ao push para o nosso repositório. Teremos a presença de uma trigger.

Essa trigger é opcional e se ela tiver habilitada estará esperando essa ação.Ela funciona, como o próprio nome já diz, um gatilho, e esse gatilho, quando acionado, diz ao pipeline o que ele deve começar a rodar.
E ele é automático, mas podemos também acioná-lo manualmente, ou ainda periodicamente.Por exemplo, todos os dias às 11:50 e 21h00 e tudo isso configurado dentro do arquivo.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6ae6cc3a-a6d0-4c0f-8f33-550aa514a86f)


Bom assim temos o início do pipeline e nesse ponto iniciamos o que chamamos de pipeline propriamente dito.

E dentro do pipeline temos os estages ou no bom português, os estágios.E um estágio no YAML Também é um limite lógico no pipeline, ele pode ser usado para marcar a separação de preocupações.
Por exemplo, a compilação Controle de qualidade produção.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a79d94ea-8630-487f-90b7-501b7cdf2ea8)

E dentro desse estágio temos os nossos Agent Jobs ou simplesmente agentes e podemos ter mais de um. Os agentes são simplesmente os servidores que vão processar e executar as 
ações que precisamos na nossa integração contínua.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/cdebe82b-14bc-43bd-bb07-b9f32e392641)

Nos agentes temos a especificação dos recursos que necessitamos para a execução do pipeline, e nos agentes com o yaml também temos a opção de adicionar dependência entre eles.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/f5d77572-b42e-4758-8937-6adb38b2bbeb)

No yaml temos a visão do job. Um job define a sequência de execução de um conjunto de steps(etapas).


![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/04249eeb-7d2d-41ea-8dcb-218608978d0c)

Uma etapa pode ser uma tarefa ou script e é o menor componente de um pipeline. No Yaml não usamos tasks groupas, mas podemos usar templates

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/42cee61a-d7d9-4235-8e56-5a0636e5535c)

E templates Nada mais é do que uma parte da nossa configuração que queremos replicar em outras configurações e évuma forma de facilitar a nossa vida, eliminando repetição de configurações.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/af0c362b-83be-4b45-b01e-e7b1e606393f)

Uma tarefa no YAML é igual no editor clássico. Ele é um script pré empacotado que executa uma ação como chamar um comando shell ou dar os testes unitários,  ou ainda publicar um artefato que geralmente será sua última tarefa.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/11c6ef44-d42c-4558-819e-a0da1dfde30f)

o artefato no YAML também é uma coleção de arquivos ou pacotes publicados por uma execução. E esse artefato nada mais é do que o produto do seu código.
E depois disso podemos acionar a trigger de entrega contínua.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/cd194374-588a-4f77-80af-5d297dffbb88)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/73240cb4-3352-4ac1-a24f-2579d0cd416d)

