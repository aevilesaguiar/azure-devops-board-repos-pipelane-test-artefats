# Azure repos

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/2c604690-a3c9-4f3e-b5bd-35230d5976f6)

O Azure repos serve para hospedar os nossos repositórios e eles podem ser tanto git quanto tfvc.Git é o controlador de versão mais usado hoje em dia já o tfvc é o repositório proprietário da microsoft usado cada vez menos.
Com i azure repos podemos hospedar nosso código fonte e criar repositórios publicos ou privados, podemos criar branchs e gerenciar os commits, temos a opção de adicionar tags e trabalhar com git flow, podemos ainda fazer toda a parte de pull requests
usando a sua ferramenta visual, e o  azure repos é facilmente lincado ao visual studio e ao visual studio code ou qualquer outra ferramenta que se integre


![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/7eb30738-04b4-46c5-b73a-5818246f9a40)


Também podemos integrar facilmente ao azure pipeline:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/2a4a225a-ab04-4f7a-beac-adba02d2f040)

## Fundamentos do controle de versão

Temos dois tipos de controle de versão:

- Centralizado: esse já foi o tipo de versionamento mais utilizado, mas hoje perde muita força, cada vez mais está em desuso, ele segue a topologia em estrela, onde temos um único repositório central, e uma cópia de trabalho para cada desenvolvedor. E a comunicação entre uma área de trabalho e outrsa sempre ocorre através de um repositório central, e ele funciona como um modelo cliente servidor. O servidor contém todos os arquivos versionados, os clientes podem gravar ou resgatar todo o histórico da versão, e essa ação chamaos de checkout. O principal problema desse modelo é a dependência do servidor, caso o servidor fique inoperante ninguém pode fazer nada até ela voltar ao ar. Os sistemas que usam esse tipo de controle são: svn, sub version e até tfvc.
![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8af00708-368c-4319-9df4-8f5d8495423a)

- Distribuído:o outro controle de versão que temos é o distribuído, ele é amplamente popular e usado pela maioria das empresas de desenvolvimento de software. Se no modelo centralizado temos o servidor no centro de tudo, no distribuído temos ao contrário, temos vários repositórios autonomos independentes, um para cada desenvolvedor, onde cada repositório possui uma área de trabalho incorporada, com isso cada desenvolvedor tem uma cópia de todas as versões dos arquivos, eliminando o problema do sistema centralizado, onde o servidor precisa estar 100% online, no caso do distribuído ele pode cair e contianuamos trabalhando nos arquivos, e quando ele voltar fazemos o push. Os sistemas que usam esse modelo são Mercurion e o amplamente difundido git.
![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/e37bf0a0-70fe-440f-aba2-beb01a8911c6)


O git pull e o git push são comandos complementares, utilizados em conjunto para compartilhar código em um fluxo de trabalho colaborativo. Enquanto o git pull atualiza o repositório local com as alterações do remoto, o git push envia seus commits locais para o repositório remoto, mantendo-o atualizado com seu trabalho.

## Conceitos do GIT

Git é um sistema de controle de versão, é o mais popular sistema de controle de versão, ele nos possibilita rastrear alterações, adicionar novos arquivos, modificar arquivos e caso a alteração esteja incorreta voltar ao estado inicial.
Nós subimos nosso código ao servidor, alteramos nosso código e podemos fazer rollback( ou seja, voltar a situação anterior). Mas o gir é muito mais que isso, é uma ferramenta que manté todo o nosso histórico de alterações, além disso ele é distribuido.

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/d5404796-64df-4578-a745-7fd79b0944ed)

o Git como mencionamos acima usa o modelo de versionador distribuído, quando o desenvolvedor deseja usar o projeto, ele não vai usar o código diretamente no servidor, ele vai fazer um clone de todo o repositório e todas as alterações para a sua máquina, assim eliminamos pontos de falha, pois todos tem uma cópia na sua máquina e claro no servidor.

Conceitos do git:

- Repositório: no git sempre precisamos de um repositório, um repositório nada mais é que uma pasta onde estão todos os arquivos do nosso projeto incluindo o nosso versionamento. Podemos criar um repositório, ou baixar ele de algum servidor de repositório git. E o azure repos será o nosso servidor que fornecerá os nossos repositórios, poderia ser também o github ou gitlab e ainda o bitbucket.Todos eles trabalham com git, além disso podemos trabalhar localmente ou ainda ter o nosso próprio servidor git na nossa empresa, mas o ideal é sempre usar os serviços disponibilizados na nuvem e assim tornam-se acessíveis de qualquer local, como o azure repos. 

<img width="575" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ac287920-9359-4a71-916e-24af0bb95f44">

Também temos as branchs são as ramificações do nosso código, podemos criar ramificações a partir de outras ramificações. Podemos também fazer merge, ou seja mesclar ramificações, por exemplo da sua branch onde você está trabalhando para a branch principal. 

<img width="302" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/de1c7fd9-4a83-405a-9998-8d32233896a5">

Também temos os commits, um commit é tudo que subimos para a branch, é o nosso pacote de atualização do código, podendo conter inclusões, exclusões e edições do código.



<img width="287" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/b0d72192-1161-4391-9914-dae4a3f721aa">


## Pull Requests e Code review

- Code review: é uma prática de revisão de código, ele consiste em quando um ou mais colaboradores revisam o código do seu colega, o code review ajuda na qualidade do software. Com o code review temos o scompartilhamento de conhecimento, criar soluções alternativas para o problema(criar melhores soluções) e compartilhar a responsabilidade(quando outra pessoa verifica o seu código ele se torna indiretamente responsável por essa implementação).
- Pull requests(PR):  a prática de pull request facilita a colaboração dos desenvolvedores com uma interface fácil de usar para discutir alterações antes de integrá-la a um projeto. Pull request geralmente é aberto quando queremos subir um novo código para a branch develop, e só podemos subir ela assim que seus colegas aprovem ela. No azure repos podemos delimitar um numero de aprovadores.

<img width="584" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/3a7c1c0e-6369-4f01-a3a1-1fe91affd38a">

<img width="741" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0c861a48-841b-4ba6-9beb-3016ac6aa407">

<img width="784" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/bb5cd386-5098-4ebb-bcfb-3fabd59c4d46">

<img width="811" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/4a5558ee-2436-4c23-a085-3d28ca7b488e">

AGORA PRECISAMOS MERGEAR

<img width="814" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/f429473e-2bc0-43da-b60c-25fba3817c3c">

## Branch Policy - Obrigar PR

Exemplo: aplicar uma política que obrigada que obriga que todo commit na branch main deve vir de uma pull request, então obrigamos que tudo que entre na nossa branch default seja revisada por aprovadores;

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/146f2b60-5f2b-4567-8c75-68dd054b2891)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/8b5d04e9-4605-43f3-b08a-c905a96bbcc3)

a mensagem diz que não foi possivel executar o commit diretamente na branch main:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/9466980a-284f-4830-a9ae-4a7c75c41bc5)

## Branch Policy - obrigar vincular work itens

obrigar vincular work itens

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/346e814b-e075-4471-b529-0c829ccc08bf)

precisamos fazer um commit incluindo o work item:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/7b996f19-4632-4fc2-910b-e090b0c8fbf6)

e depois executamos o pull request

<img width="632" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/17b9b661-ce80-46cf-b9a5-2f4da755fdfa">

Passou o merge, sem conflito, agora podemos aprovar e completar, subimos para a branch main:

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ff44c6cb-ea2f-4b81-b1c8-73ad4af6da37)


<img width="935" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/948b504a-29aa-480c-91d0-d93f9fe1add0">

## Comandos git

O git trabalha através de linhas de comando. 

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/54c01efe-862e-4bb8-83e7-0b457a86960c)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5c51faee-53fd-401a-b317-46dc763423f5)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/284070af-7093-43a6-88a9-1a7fa95851c4)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/bc44d7e1-b055-4f92-995f-dda4ce089433)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/d2b2f0a1-20fd-40a5-9440-6f058d80d2b9)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/42c6de8c-bbcc-484a-89d3-f55d302782dc)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/25870082-53fc-4ffc-8dd9-fe3b53739ba5)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/12b8aa39-90be-4199-9034-8ce873a4bf42)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/7bd60d6a-71c7-42e2-bbc2-7522ee8c92f5)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/131da81b-1764-4ba8-9a3d-794a0de8c5d0)

<img width="560" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/303311e3-4fbb-47b5-b4f0-8345b2f70b1f">

<img width="559" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/4665e3dd-36cc-45ef-862d-ea8da49bc8b3">

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a60919b1-1736-4e03-95cc-4af42c6cdc8a)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5de6236b-8c00-406e-a5c9-bbdf269d42c7)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/ed83e5ec-9cb0-4c3c-983c-832c647fec5f)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/cbfa49b4-e135-4c66-8185-a61739405c2a)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/6beb4f07-6f05-46a5-99f5-a96f639ba50a)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/d320fc9e-e95f-499f-87a8-08dd7c513745)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/73922bf7-446e-4ed7-8248-96d41bab3a3e)

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/5f6b2b3b-0e9b-4c85-927b-8596c3ae89bc)

Com push você atualiza o repositório remoto,  com pull vc atualiza o repositorio local
