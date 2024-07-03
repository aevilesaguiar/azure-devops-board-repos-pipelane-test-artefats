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



## Criando Projeto e Repositorio no Azure Repos GIT para nosso Codigo

Vamos fazer uso do azure devops para provisionar os nossos recursos e publicar o nosso site no azure apps service:

- Criar o projeto
![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b67d8433-2665-4657-aea5-c6ac85355f99)

- projeto criado
<img width="939" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/06580ee2-490a-4bb4-b325-b57c26175bfe">

- 
[Importante] Habilitar "Classic Editor" no Azure Pipelines
Para contas novas do Azure DevOps, o Classic Editor está sendo criado desativado por padrão.



Para ativá-lo, siga as instruções abaixo:


Em Configurações do projeto, em Pipelines > Settings > General. Certifique-se de que 'Disable creation of classic release pipelines' e 'Disable creation of classic release pipelines' estejam desativados para que o editor clássico seja exibido após a criação de um projeto.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/05827dc5-8692-470f-8e29-83b5020e63f4)

Se essas opções estiverem desativadas, vá para o nível organizacional e faça o mesmo em ‘Organization Settings’.


## Build Pipeline

já iniciou a esteira:

<img width="935" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/bfa5f7b8-004f-4ce2-9ffc-0083d6cf35d7">

<img width="938" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0a2a0ca0-d89f-4a05-9ec9-cdf0d4590bca">

<img width="949" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/7279abcd-f34b-4512-ad71-aa64c37d347f">

<img width="953" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/272e9e18-2232-46c9-ab44-3f13c254ce74">

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/07c7b718-e26f-41a1-a0aa-d98ee99316d8)

Podemos conferir o artefato:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/4f0677c8-1227-4d07-bb10-e04f9a3f3092)


## Release pipeline no azure pipelines

Vamos usar o azure devops para entrega e implantação dos nossos serviços e produtos. Para acessar a parte de entrega do azure devops, precisamos acessar pipelines e depois releases:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8d542331-fc78-4200-b2c7-1637c1c80ca1)

e temos a opção de criar o fluxo de implantação do nosso software:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8f62aa7c-5027-42d7-b667-7cf16b0792fd)

Podemos criar estágios no fluxo macro:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5c41b8ab-1297-4782-b796-b091358151d2)

## Princípios da entrega continua

Dois termos que usamos com frequencia: 

- continuos delivery: continuos delivery é um termo mais amplo, não é apenas implantar em produção o nosso serviço, mas sim precisamos envolver 8 principios de entrega continua e muitos deles são compartilhados pela cultura ágil;
![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0fed164e-ccf5-427a-b16d-f6221d80bcfa)
  1. Processo confiável repetível: precisamos repetir o processo de implantação e principalmente confiar nele;
  2. Automatize tudo:precisamos automatizar tudo que está relacionado a implantação, testes de qualidade e segurança, após automatizar um processo é necessário menos esforço para executar ele e também para monitorar o seu progresso, e isso garantirá resultados consistentes;
  3. Repositório em tudo: precisamos versionar além da nossa aplicação, configurações, infraestrutura, banco de dados e até a documentação, quanto mais versionado melhor;
  4. Mais complicado, primeiro: lide com coisas difíceis primeiro, tarefas demoradas ou propensas a erros o mais rapidamente possível;
  5. qualidade interna: precisamos criar loops de feedback curtos para lidar com bugs, assim que eles forem criados , assim como fazemos com sprints do ágil
  6. Concluído=liberado:concluido significa liberado, é o definition of done, ou definição de pronto no mundo ágil, mas aplicado apenas quando está em produção, ter uma definição clara de pronto desde o início ajudará a todos a se comunicarem melhor, e a perceber valor em cada recurso;
  7. Todos são responsáveis: funciona na minha máquina nunca é uma desculpa válida, a responsabilidade deve ser de todos em todos os ambientes, principalmente em produção;
  8. Melhoria contínua: o processo precisa ser revisado e melhorado constantemente e para isso precisamos monitorar e criar métricas, além disso sempre aprender e ensinar mais, evoluir o time e o processo de entrega contínua;
devem ser tratadas

- continuos deployment(implantação continua): nada mais é que implantar todas as alterações do código em produção

## Etapas para Entrega do Software no Azure DevOps

Os passos para implantação do software usando release pipeline. O primeiro passo é selecionar o artefato.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/e67e3578-5597-4e7b-8737-322fb3f62b39)

O artefato é gerado a partir do build:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/00e55469-93cd-4bfb-aedd-290e8b4a57bf)


Mas podemos iniciá-lo após push do repositório do git do azure repos

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/9c7821b1-73cf-4d25-bfc7-53e6c9de85e0)

do TFVC:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/bb35d4ca-9f4f-4f49-9332-e3e3c60e3738)

Ou até do github:

<img width="484" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b3830a0f-5f8a-4555-9444-8bed8304e710">

Podemos incluir o release após inclusão de artefato no azure artfects

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/2f03bfe7-8fda-4155-93fb-ff403f44ab70)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/487dfa42-6e8a-4cd9-a53f-d42b83b8a465)

ou github release:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/601ad7b2-fadb-4b1a-bb68-f78d43ad1633)

e ainda utilizando containers:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/1d7ad799-e7cf-4b8b-acd0-0ff8dff1cf66)

e ainda podemos integrar o start do release do pipeline com a integração continua do jenkis:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/221efb96-488d-443d-b453-21085c3ac1b8)

Podemos ter uma ou mais artefatos:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b7457859-0728-4638-895c-8d889623c300)

podemos agendar o início do release, e assim realizar implantações só a noite

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6c377748-cc57-4ce5-a69c-2eaeb58a0591)

Por exemplo nos artefatos podemos adicionar aprovações via trigger de pull request:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/86f114b7-7bfa-413e-a500-9c7e2ba2f7db)


E filtrar o início da release em apenas determinadas branchs.

Depois de selecionar os nossos artefatos a serem implantados damos início a parte chamada de stages ou estagios, e aqui podemos ter quantos stages forem necessários.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/3fce8d1c-4ab9-409a-9fc4-0ae7b163bdd9)

Podendo adicionar aprovação antes:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/aea3563c-e544-493f-b8c1-b7cdbde25d8e)

e depois da realização de um estagio:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6f39e0c9-d19e-40a4-86a3-c88b15cd4df3)

Podemos também adicionar gates.

Dentro de cada estagio temos as nossas tarefas, e temos centenas delas, e com elas podemos publicar automaticamente nossos artefatos em serviços do azure por exemplo

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/56d3785c-e209-4025-b360-25c73be0b463)

Também podemos publicar em servidores com us ou rodar em containers. Basicamente são essas as etapas do processo de implantação usando release do azure pipelines

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8368d376-1643-4512-bdf5-6db2a4a3402b)


## Nuvem e azure Cloud

Por volta de 2010 os usuários casuais da internet foram apresentados ideia de que o mundo digital poderia ser entendido como cloud. Nossos dados estão em algum lugar acima, o que chamamos de nuvem. Mudamos o jeito que assistimos filmes, armazenamento de foto e etc

Notícia antiga
<img width="599" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/2c498edc-658a-4308-bc1a-1bfc8e0c5ffd">

O que é a computação em nuvem?

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a5412fac-bca8-4715-a8a6-975bf6823bad)

Segundo a wikipedia: a nuvem cloud é um nome genérico dado a computação em servidores disponíveis na internet a partir de diferentes provedores. O conceito de computação em nuvem refere-se a utilização de memória e da capacidade de armazenamento e cálculo de computadores e servidores hospedados em datacenters, interligados por um meio da internet, seguindo o princípio da computação em grade.

Azure é a nuvem da microsoft;

## criar conta azure

é necessário criar uma conta na microsoft, podemos criar uma conta gratuita.

## Regiões e Grupo de Recursos no Azure

Regiões no Azure: essass regiões são o conjunto de data centers implantados dentro de um perímetro, de latencia definida e conectado por meio de uma rede regional dedicada de baixa latencia.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/354f8a16-b15c-448d-bed9-63fd6e86f215)

os circulos em azul, são as regiões disponíveis
os circulos tracejados em branco são regiões já anunciadas e logo disponíveis.
e nos circulos mais expessos as zonas de disponibilidade, elas são locais separados dentro de uma regiao do azure;
Cada zona de disponibilidade é formado por 1 ou mais data centers. As zonas de disponibilidade permitem que clientes executem aplicativos críticos com alta disponibilidade e também replicação com baixa latencia;

- Resource group: grupos de recursos, precisamos entender para poder fazer deploy com terraform. Recurso no azure são os serviços, por exemplo uma VM é um recurso, web service é um recurso, ou seja com resource group podemos agrupar esses serviços de maneira rápida e simples, com outras palavras os recursos do azure permite organizar os recursos da sua conta. Mas por que agrupá-lo no resource group? uma vez que eles estiverem agrupados e isolados, você terá muito mais controle.

  ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0a18687f-ea34-4a91-ae7d-f4126308ae12)


Os Resources groups(RG) possuem algumas regras:

 - 1 Os Recursos ou um grupo de Recursos(RG) devem compartilhar o mesmo ciclo de vida. ou seja se excluirmos um Resource Group excluíremos todos os recursos. Um recurso fará parte apenas de um grupo de recursos;
 - 2 Os recursos podem ser transferidos entre grupos de recursos a qualquer momento;
 - RG pode ter recursos de diferentes regiões;
 - Recursos podem interagir com diferentes Recursos

Temos 4 controles para nos ajudar:

- tags: funcionam para taguear, pode usar livremente e marcar aquele grupo de recursos, funcionando como uma categoria
 ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/24246793-ad86-4baf-b320-6ea5879b5fb3)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/28a6277b-71bb-468a-a55f-3e054ee62766)

- locks: ele funciona como um bloqueio , por exemplo você pode criar um block que impessa a exclusão acidental, muito útil caso tenha mais de um usuário operando no mesmo grupo de diretório do azure
![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/c3499490-fd15-45fa-93bd-139c1e6e18b2)

- IAM: IAM(Gerenciamento de identidade de acesso) , e podemos chamar ele de sistema de controle de acesso baseado em funções na assinatura do azure, basicamente ele permite que você ofereça aos usuários determinadas funções de assinaturas, grupos de recursos e recursos individuais; e também protege credenciais com controle de acessos baseada em risco, ferramentas de autenticação forte sem interromper  a produtividade
  ![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/2119dd33-5b6b-4569-a173-b37594e9b9a5)

- Policies: policy(politicas) entidade do azure que controla um determinado tipo de comportamento ou efeito nesse grupo de recursos

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/466d3eb9-b6bc-4be8-b124-b38cbeb6a3f5)

     
  Com esses 4 mecanismos de controle você pode controlar, gerenciar e proteger os recursos da sua solução de resposta colocando todos esses elementos em um grupo de recursos


**TERRAFORM**: Terraform é uma ferramenta criada para construir, alterar e criar versões de infraestrutura. Portanto, ela não é uma linguagem nem um framework, mas sim um recurso usado no DevOps para garantir mais agilidade e segurança nas entregas. 
Como ela foi construída com base em GoLang, ela é muito simples, e as suas dependências estão contidas no próprio binário.

Gerir uma infraestrutura em nuvem dá muito trabalho, principalmente com o crescimento do cloud público, como é o caso do AWS. Mas ao fazer isso com código, essa tarefa fica mais fácil. 

Para entender melhor o Terraform, é interessante saber o conceito de IaC, ou seja, Infrastructure as Code ou Infraestrutura como Código. Ele é, como o nome sugere, o gerenciamento e o provisionamento da infraestrutura através de códigos. Essa ação substitui os processos manuais. 

O terraform foi criado em julho de 2014 pela empresa HashiCorp, que já é conhecida por outras ferramentas criadas no mundo DevOps. Apesar de ser lembrada pelo uso no AWS, a ferramenta também suporta IBM Cloud, Linode, OpenStack, Google Cloud Platform, Microsoft Azure, entre outros.

Vantagens
Com o terraform, o DevOps fica mais eficiente, principalmente usando boas práticas dessa ferramenta. Aliás, ela deve estar na lista de skills de todo desenvolvedor que atua nesta área. Saiba, a seguir, algumas vantagens desse recurso: 

Configuração de ambiente para testes de forma mais rápida e econômica;
Possibilidade de escolher o melhor provedor, como AWS, Google Cloud, Azure, entre outros;
Reprodução do ambiente de forma contínua e fácil; 
Redução de custos;
Maior eficiência e segurança.


## Azure app Service

O azure App Service(Serviço de aplicativo do azure) é um serviço para hospedar splicativos da web, API's REST, back end móveis e até web jobs, ou seja funciona como uma hospedagem tradicional. Onde você não é responsável pelo o servidor, utilizando o modelo PaaS(Plataforma As a Service), você pode desenvolver em sua linguagem favorita, e ainda hospedar aplicações front end

<img width="577" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/7bb42d7a-8bb9-42ca-b471-4a93ad389347">

E por ter um modelo baseado no PaaS, os aplicativos são executados e dimensionados com facilidade em ambientes baseados em windows e linux.E também é possivel usar containers dockers. Além disso usando o App Service você adiciona segurança, balanceamento de carga, escalonamento automático e gerenciamento automático.  
<img width="593" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/dadea39e-b85f-4282-8625-f262180a4530">

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5e7a9eaf-41aa-41e9-8c98-78abfed5a6e2)


## Azure CLI

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a470c8b2-4e2b-4630-9bdd-0ded7bf887ef)

CLI: Comand line interface, é a interfce de linha de comando do azure.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/25c7ef14-ee76-4661-a7d7-426abf874f81)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/c3d8efbe-8d6a-4e7b-8f1c-f62029abab2e)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8eff0a65-d8f8-4eae-bd5a-79fd56cb65cc)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/878e5353-2aa3-4cf5-bdf2-3d30b3fd7d34)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/394b64a1-8681-4e68-a0d8-003d5e669c90)

<img width="508" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b6f1e251-e3dc-401a-bd5a-b9594e729bb6">

<img width="443" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a8f9b5e0-fe29-4772-bd92-0205cd606b43">

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/fe721001-009c-40e9-bca3-5fcb0ce22d24)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/bec69028-2e1e-4cbb-94d3-483394ba43d2)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/3e52e4f0-a90d-471f-8015-92f48932ae5f)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/f33fe284-9b88-433c-bfcc-2b57d6ca20ae)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0c27ae99-bfb7-4085-bdfa-5a97363c13ea)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/dc1c79e7-2069-4f90-8931-2ead187ef270)


Se for criar um banco de dados pode usar o azure CLI, WEB Service pode usar o azure CLI.


O que em batch?VA programação em batch é uma forma de escrita de scripts ou sequência de comandos que possibilita a execução automatizada de tarefas em sistemas operacionais.
