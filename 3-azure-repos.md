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



