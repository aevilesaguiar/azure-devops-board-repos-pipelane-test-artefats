## Azure Pipelines - Integração e Entrega Contínua - Editor Clássico

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/360ad6fa-7cb5-4ad4-93e9-aa068d5d12d1)

<img width="591" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/00fe04b9-b171-4c34-937f-f369ebba79aa">

<img width="559" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b799817b-15a5-4798-a7a3-f852d18c821d">


## Build Pipelines

O azure pipeline é dos serviços do azure devops, ele é um serviço de nuvem, você pode usar para criar e  testar automaticamente o seu projeto de código, e ainda disponibilizar ele para os seus usuários.
O build pipeline integra CI e CD;

<img width="590" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6d971600-bb13-4ac8-93d1-9646794b82e5">

Para criar e testar constatemente seu código e enviá-lo para qualquer destino. Resumidamente o ciclo é assim:

- 1 - o código chega no nosso repositório, geralmente o git;

<img width="607" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/4f718250-a4a8-4762-b97c-232e18a40d34">

- 2 - começa a rodar o nosso build, durante o build geramos o noso pacote, que no caso é o artefato que queremos publicar.
<img width="602" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/495f3ac9-621a-4c24-b756-1a8d106cd3e7">
<img width="600" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6e239ed1-77ae-42c7-8483-f9b8ffdb1a75">

- 3 - então entra a parte de release, onde efetuamos a entrega contínua para o nosso servidor.
<img width="607" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/c6b857fe-95fe-4220-98cb-a3d951275f8e">

é macro esse resumo;

## Editor clássico no azure pipeline

Conceitos do pipelines usando editor classico;

Logo após o código ser submetido ao push para o nosso repositório, temos a presença de uma trigger, essa trigger está esperando essa ação, ela funciona como o próprio nome já diz, um gatilho. 

<img width="606" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/3442e001-5c76-424a-8cab-171ef8dc7428">

Esse gatilho quando acionado chama o pipeline

<img width="598" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b85b70d5-2783-4465-81f5-e04ee88891be">

Que deve rodar o nosso Build, ele é automático, mas podemos adicioná-los manualmente

<img width="608" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/1fc26612-0d53-46ad-8e7b-07b191b8eb15">

ou períodicamente:

<img width="605" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ee35b35b-28ac-47e5-8677-2994db3098af">

Assim temos o início do pipeline, propriamente dito. Dentro do pipeline temos stages, ou no bom português estágio, dentro do editor classico temos apenas um pipeline , temos todos esses estagios, conforme mostrado(agent job 1 ou simplesmente agent) e pode ter mais de um agent.


<img width="613" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/816a5fff-a608-46ec-bf6e-0b36aa7146a5">


Os agents são simplismente os servidores que vão processar  e executar as ações que precisamos na integração contínua, e nos agents temos a especificação do recurso que necessitamos para a execução do pipeline:

<img width="589" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/e964c46d-185c-4405-bf05-8a2857f5d72f">


Podemos ter mais de um agent em um stage, e tmos a opção de adicionar dependência entre eles.

Em um estagio temos vários job, um job define a sequencia de execução de um conjunto de step, ou no bom portugês as nossas etapas. 
Uma etapa pode ser uma tarefa ou script, e é o menor componente de um pipeline.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/55bbf4da-2cc9-46c5-88d4-6687e876f0b2)

As tarefas podem ser agrupadas

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/639799d6-10c8-4573-84d4-fa8efe9e094d)

Esse é um atalho para incluir a task group, e você pode criar um grupo de tarefas para executar as rotinas relacionadas aos pacotes .net, podemos criar grupo de tarefas dentro de tarefas;

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/c8a861f2-31b8-4975-8950-70cb0935dd96)

Uma tarefa é um script pré empacotado, que executa uma ação, como rogar um comando shell, rodar os testes unitários, ou ainda publicar um artefato de construção, e geralmente será sua última tarefa;

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/34b26ac5-57dd-4621-8aeb-a4e2fac0ec34)

Um artefato, é uma coleção de arquivos, ou pacotes publicados por uma execução. Esse artefato nada mais é que o produto do seu código, se for uma aplicação com js e framework angular, serão suas páginas contendo todos os arquivos a serem publicados, se for uma aplicação java ´pode ser o seu jar ou war, se for uma aplicação .net pode ser a deliery da sua aplicação por exemplo.

Depois disso podemos acionar a trigger de entrega continua.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/46a5594a-e788-44ed-af6c-682d4a596249)

Vamos fazer uso do azure devops para provisionar os nossos recursos e publicar o nosso site no azure apps services,
