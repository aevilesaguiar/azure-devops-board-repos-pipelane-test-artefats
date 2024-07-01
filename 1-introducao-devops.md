# Introdução Devops

## Devops Básico

<img width="605" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/44e5703b-a076-4a72-9462-f7e8c7c358d6">

DevOps é um buzzWord do momento;

- Dev: refere-se a desenvolvedores
- OPS: a operação

 <img width="352" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/77cf4d1f-bbe5-4f19-b5d0-2bd338878be1">

Conceito devops enfatiza comunicação, colaboração e a integração entre desenvolvedores de software e o pessoal de operações de tecnologia da informação.

Vamos ver como o DEV funciona: mudança continua e adicionar novos recursos ao produto ou serviço;
OPS: a operação quer estabilidade continua, ou seja que o serviço não saia do ar.;
Negócios: e no centro de tudo isso temos negócios o Business da nossa empresa ou cliente;

<img width="304" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ea77131f-ceaa-470c-83bd-eee33c3bc199">

O business da sua empresa ou cliente é o foco principal, e o uso do DevOps entra nesse jogo como uma ferramenta para ajudar na adoção da cultura DevOps.

## Azure Devops Serviços e Recursos

Azure DevOps plataforma de implantação da cultura devops.

O azure devops tinha outros nomes:

<img width="378" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a9bd2ee5-3fa5-466d-87be-5dcdd99a49fc">

Novos nomes:

<img width="351" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/47023c4c-1a49-44d3-9b3f-df1e21e77e79">

Basicamente, os dois produtos possuem as mesmas funcionalidades.A plataforma do Azure DevOps integra cinco serviços principais que ajuda a nossa equipe no gerenciamento do ciclo de vida do software.Com ele, planejamos e gerenciamos o nosso projeto.Temos a nosso dispor repositório de código, também temos build e deploy contínuo, temos também um serviço dedicado a testes e a qualidade, e também podemos centralizar os nossos artefatos.

<img width="410" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ed8fbda0-0261-4c71-bceb-69ab0b7d7f70">

Os 5 Principais serviços:

- 1. Azure Boards: esse serviço é responsável pela parte de gerenciamento e planejamento do projeto. Nele podemos adotar 4 modelos de processos de processos **Basic**, o **scrum, o ágil e o CMMI** .Criamos nossas histórias de usuários, tarefas e bugs. Também fazemos o planejamento de horas por atividade. Temos os gráficos como burndow, burnup, conseguimos medir a velovidade do time e esforço aplicado ás tarefas, enfim toda a parte de planejamento do projeto.

<img width="615" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/26b5d72b-a577-4063-a965-ada1f729b76c">

  2. Azure Pipelines: e ele é o tema do nosso treinamento , é aqui que podemos adicionar a integração continua, ou s.eja quando eu fizer um commit ou um push dispara uma rotina para fazer o build da aplicação, fazendo também os testes unitários, avaliando a qualidade com sonar, e muitas outras ações. Etambém onde teremos os releases, onde faremos a entrega continua, mantendo a aplicação atualizada de forma automática, podendo adicionar aprovações para subir para os mais distintos ambientes. Fazemos a integração e entrega continua (CI/CD) do nosso código e também da nossa infraestrutura.
    
<img width="604" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5749c1df-efd2-4707-ab3f-f3ca600016f4">

  3. Temos também no azure Repos o serviço para hospedar o código, chamado de azure repos. Nele temos repositórios do GIT e também, do ainda não extinto TFVC, repositório proprietário da Microsoft, que está cada dia mais perdendo espaço para o git.Podemos criar inúmeros repositórios privados e também públicos. E ultimamente com a aquisição do GitHub pela Microsoft, podemos também unir facilmente com o repositório do GitHub, além, claro, de qualquer outro repositório como Git Lab ou serviços de Git on primers. Podemos adicionar pool request ao git facilmente.

<img width="614" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5152af56-6af0-4771-b2a5-1ccd7d0884df">

     
  4. Outro serviço que temos no azure devops é o Azure test Plans. Nele podemos adicionar testes funcionais, testes automatizados, testes de carga e muito mais.Temos ferramentas excelentes para toda essa parte de validação de qualidade da nossa aplicação. Focado em qualidade, podemos rodar testes exploratórios, manuais e automatizados
     
<img width="595" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/dc36f1e9-de14-4b98-95f5-b0ab11303303">

5. Azure Artifacts: Com ele podemos compartilhar pacotes na MAVEN e NPM de fontes públicas e privadas com toda a nossa equipe. Podemos criar, hospedar e compartilhar código empacotado com o nosso time, e também podemos facilmente adicioná-lo a nossa integração e entregação continua.

<img width="619" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/73a46db5-7f7d-474b-9f1e-2e5b2f10fd65">
   
6. Extensões disponíveis do market place, temos mais de mil extensões

 <img width="612" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/95d2c36d-5aea-4325-bd21-9b8027f0e66e">


Bom, além disso, podemos pensar no Azure DevOps como um orquestrador, onde podemos adicionar mais ferramentas e fortalecer ainda mais a plataforma de DevOps da empresa.

- timetracker: gerenciar as horas do time
- integração a docker
- slack e github

<img width="632" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/f64720bc-ae78-4fdf-8af0-d2da4a840464">

  

## Precificação do Azure devops

Azure devops é gratuito, mas não é bem assim, ele tem diversas limitações. Até 5 pessoas o custo é zero


## CI/CD

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/23669bde-15b7-4c2f-89ce-f9c4bf79f494)

O que significa CI e CD?
CI/CD, ou Integração Contínua e Entrega Contínua, são abordagens ágeis de desenvolvimento de software que visam automatizar o processo de construção, teste e entrega de software. Nesse sentido, elas visam automatizar e acelerar o processo de entrega de novas funcionalidades e atualizações aos usuários.


- Introdução
  
Imagine você trabalhando em um time com várias pessoas, trabalhando nos mesmos códigos, mudando tudo ao mesmo tempo. Tudo bem, cada um pode garantir que o código em que está trabalhando esteja integrado ao código no repositório, execute os testes, etc, mas em sua máquina, manualmente. Além disso, ainda temos que fazer o deploy já integrado e testado para o ambiente de produção. Mas vamos pensar! Se você automatizasse esse processo não seria muito melhor? Fora a economia de tempo, fazendo isso você estaria totalmente garantido de que as validações e processos necessários seriam verificados, concorda?

A Integração Contínua (CI) e a Entrega Contínua (CD) são práticas essenciais na área de desenvolvimento de software que ajudam a melhorar a qualidade do código, a eficiência do processo de desenvolvimento e a capacidade de implantação de software. Neste artigo, exploraremos o que é a CI/CD, por que é importante e como você pode implementar essas práticas em seu projeto.

Afinal, o que é essa tal CI/CD?
Vamos desmembrar. Quando falamos de integração, estamos nos referindo a uma solução para mesclar as alterações feitas pelos desenvolvedores. Ao utilizar uma ferramenta de controle de versão, asseguramos a integração do código-fonte de uma solução. Quando mencionamos entrega, estamos nos referindo à implantação dessa solução. Até aqui, não trouxe nada de novo para aqueles que atuam na área de DevOps. No entanto, quando adicionamos o termo “contínuo”, estamos falando da automação dessas atividades, incluindo a parte de teste.

Afinal, o que é essa tal CI/CD?
Vamos desmembrar. Quando falamos de integração, estamos nos referindo a uma solução para mesclar as alterações feitas pelos desenvolvedores. Ao utilizar uma ferramenta de controle de versão, asseguramos a integração do código-fonte de uma solução. Quando mencionamos entrega, estamos nos referindo à implantação dessa solução. Até aqui, não trouxe nada de novo para aqueles que atuam na área de DevOps. No entanto, quando adicionamos o termo “contínuo”, estamos falando da automação dessas atividades, incluindo a parte de teste.

Integração Contínua (CI)
Integração Contínua é a prática de integrar o código produzido por diferentes membros de uma equipe em um repositório compartilhado com frequência, várias vezes ao dia de modo automatizado. Cada integração é verificada automaticamente por meio da execução de testes automatizados. O objetivo da CI é detectar erros de integração o mais cedo possível, antes que eles causem problemas.


Entrega Contínua (CD)
A Entrega Contínua é uma extensão da CI que se concentra em automatizar a construção, o teste e a implantação de uma solução para um ambiente de produção. A entrega contínua garante que o código esteja sempre em um estado pronto para implantação em produção, tornando a implantação um processo simples e repetível.

Bem, a Integração Contínua é uma prática primária se você quiser disseminar a cultura DevOps em sua equipe. É o começo e o primeiro passo para depois alcançar a Entrega Contínua.

O processo como um todo
Aqui está um exemplo simplificado de um fluxo de CI/CD para um projeto:

Um desenvolvedor envia código para um repositório Git.
Um servidor de integração (CI) monitora o repositório e detecta a alteração.
O servidor CI realiza a construção do código e executa testes automatizados.
Se os testes forem bem-sucedidos, o código é implantado automaticamente em um ambiente de homologação.
Testes adicionais, como testes de aceitação, são executados no ambiente de homologação.
Se todos os testes forem aprovados, o código é implantado em produção.
O aplicativo é monitorado em produção, e quaisquer problemas são detectados e tratados imediatamente.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/c74566dd-98d9-41a8-a254-dfe4c258886b)

Implementando CI/CD em Seu Projeto
A implementação de CI/CD pode variar de acordo com a tecnologia, as necessidades do projeto e a infraestrutura da equipe. No entanto, aqui estão os passos gerais para configurar um fluxo de CI/CD:

1. Versionamento de Código:
Certifique-se de que seu código seja versionado usando um sistema de controle de versão, como Git.

2. Ambiente de Integração:
Configure um ambiente de integração (CI) que automatize a verificação contínua do código. Existem muitas ferramentas disponíveis, como Jenkins, Travis CI, CircleCI e GitLab CI/CD.

3. Testes Automatizados:
Escreva testes automatizados que verifiquem a funcionalidade e a integridade do código. Os testes devem ser executados automaticamente no ambiente de integração.

4. Pipelines de Integração:
Crie um pipeline de integração que inclua a construção do código, a execução dos testes e a verificação de qualidade de código.

4. Pipelines de Entrega:
Crie um pipeline de Entrega que inclua build e o deploy do código nos ambientes de homologação e produção.

5. Ambiente de Entrega:
Configure um ambiente de entrega contínua (CD) que automatize a construção, teste e implantação em um ambiente de produção. Isso pode incluir a implantação em servidores ou em contêineres na nuvem.

6. Monitoramento:
Implemente ferramentas de monitoramento e registro para acompanhar a saúde do aplicativo após a implantação.

7. Feedback e Melhoria Contínua:
Use o feedback dos testes e do monitoramento para melhorar continuamente o código e o processo de CI/CD.


Elaborar um Fluxo de CI/CD levando em consideração as ferramentas que estamos utilizando (bitbucket e o dataproc), avaliando soluções de testes para os notebooks e principalmente, avaliando soluções de automatização dos processos de testes, integração e entrega.

Custos
Explicamos a diferença entre integração contínua e entrega contínua, mas ainda não exploramos as razões pelas quais você deveria adotá-las. Embora haja um custo evidente para a implementação de cada prática, esses custos são amplamente compensados pelos benefícios que elas oferecem.

Integração Contínua

O que você precisa (custo)

Sua equipe precisará escrever testes automatizados para cada novo recurso, melhoria ou atualização de segurança.
É necessário ter um servidor de integração contínua que possa monitorar o repositório principal e executar testes automaticamente para cada novo commit enviado por push.
Os desenvolvedores devem mesclar suas alterações com a maior frequência possível, pelo menos uma vez por dia.


O que você ganha

Menos bugs são enviados para a produção, uma vez que as regressões são capturadas antecipadamente por meio de testes automatizados.
A compilação de versões torna-se fácil, uma vez que problemas de integração são resolvidos precocemente.
Menos mudança de contexto, uma vez que os desenvolvedores são alertados imediatamente caso causem uma falha no build e podem trabalhar na correção antes de passar para outra tarefa.
Custos de teste são drasticamente reduzidos, pois seu servidor de integração contínua pode executar centenas de testes em questão de segundos.
Sua equipe de controle de qualidade gasta menos tempo em testes e pode se concentrar em melhorar significativamente a cultura de qualidade.

Entrega Contínua

O que você precisa (custo)

É necessário ter uma base sólida na integração contínua e um conjunto de testes que cubra adequadamente a base de código.
As implementações precisam ser automatizadas. O acionador ainda é manual, mas uma vez que uma implementação é iniciada, não deve haver necessidade de intervenção humana.
A equipe provavelmente precisará adotar marcações de recursos para que recursos inacabados não afetem os clientes em produção.

O que você ganha

A complexidade na implementação de software é eliminada. Sua equipe não precisa mais passar dias se preparando para um lançamento.
Você pode lançar com mais frequência, acelerando o ciclo de feedback com seus clientes.
Há muito menos pressão sobre as decisões para pequenas mudanças, o que incentiva a iteração mais rápida.

Implantação Contínua

O que você precisa (custo)

Sua cultura de testes precisa estar no seu melhor. A qualidade do seu conjunto de testes determinará a qualidade de suas versões.
Seu processo de documentação deve acompanhar o ritmo das implementações.
As marcações de recursos se tornam uma parte inerente do processo de lançamento de mudanças significativas para garantir a coordenação com outros departamentos (Suporte, Marketing, RP…).
O que você ganha

Você pode se desenvolver mais rapidamente, pois não há necessidade de interromper o desenvolvimento para lançamentos. Os pipelines de implementação são acionados automaticamente para cada alteração.
Os lançamentos são menos arriscados e mais fáceis de corrigir em caso de problemas, à medida que você implementa pequenos lotes de alterações.
Os clientes veem um fluxo contínuo de melhorias e aumentos de qualidade todos os dias, em vez de apenas uma vez por mês, trimestre ou ano.


Benefícios
A CI/CD oferece uma série de benefícios significativos:

Detecção Precoce de Erros: A CI verifica constantemente o código, identificando erros e problemas de integração no estágio mais inicial do desenvolvimento.
Maior Qualidade de Software: A execução de testes automatizados e a revisão contínua do código ajudam a garantir que o software seja mais confiável e livre de bugs.
Automatização de Tarefas: A CD automatiza a construção, teste e implantação, economizando tempo e reduzindo a possibilidade de erros humanos.
Implantações mais Rápidas: Com a CD, as implantações em produção podem ser feitas com mais frequência e mais facilidade, resultando em ciclos de desenvolvimento mais curtos.
Colaboração Eficiente: A CI promove a colaboração contínua entre membros da equipe, garantindo que o código seja sempre integrado e testado.
Maior Confiança e Transparência: Com a CI/CD, a equipe tem mais confiança na estabilidade do código e pode rastrear as alterações com mais facilidade.


Conclusão
Desvendando CI/CD, ou Integração Contínua e Entrega Contínua, revela-se um conjunto de práticas essenciais no mundo do desenvolvimento de software. No cerne dessas práticas está a automação, que simplifica processos, economiza tempo e garante a qualidade do código e do software entregue. A Integração Contínua começa como o primeiro passo, garantindo que as alterações sejam integradas e testadas continuamente, capturando problemas logo no início. A Entrega Contínua leva a automação um passo adiante, permitindo a implantação simplificada e repetível do código. Finalmente, a Implantação Contínua garante uma entrega contínua de melhorias de qualidade aos clientes.

Embora a adoção de CI/CD envolva um investimento inicial em termos de escrita de testes e automação, os benefícios são claros. A detecção precoce de erros, a maior qualidade do software, a automação de tarefas, as implantações mais rápidas e uma colaboração eficiente são apenas algumas das vantagens que as práticas de CI/CD oferecem. Além disso, a equipe ganha mais confiança na estabilidade do código e uma visão transparente do processo.

Em resumo, CI/CD não é apenas uma abordagem moderna para o desenvolvimento de software, mas também uma maneira eficaz de melhorar a qualidade, a eficiência e a colaboração no desenvolvimento de software. É um investimento que vale a pena para equipes que buscam otimizar seus processos de entrega de software e melhorar a experiência do cliente.

À medida que as organizações adotam a cultura DevOps, a CI/CD se torna um componente crítico para entregar software de alta qualidade de maneira eficiente e confiável.

TEXTO CI/CD: Hugo Habbema  -> https://medium.com/@habbema/desvendando-ci-cd-b56f515ddd20

## Documentação Azure devops

https://learn.microsoft.com/en-us/azure/devops/?view=azure-devops

##
