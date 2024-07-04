# Azure artifacts-gerenciamento-de-pacotes-e-bibliotecas-para-o-seu-projeto

Azure artifacts serviço do azure devops para gerenciar packages. O azure artefacts talvez seja o serviço do azure menos usado , mas ele pode ajudar muito na sua aplicação.
Utilizando  artifacts do azure podemos publicar pacotes em um feed privado ou até mesmo publico.

Os benefícios quanto ao uso do azure artfects, é que os desenvolvedores possam copartilhar seu código com eficiência, e gerencie todos os seus pacotes em um só lugar além disso podemos compartilhar seu código na mesma equipe, entre organizações
e até publicamente através da internet. Os desenvolvedores também podem consumir pacotes de diferentes feeds, e registros publicos como o npm js. 

<img width="575" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/a53fdcc6-77e5-4e18-b5d0-e52277eeda86">

No azure artfects um feed é uma construção organizacional para hospear pacotes. Os artefatos do azure dão suporte a vários tipos de pacote, como maven, pyton, mvn, pacotes universais e outros..
Podemos ter feeds para artfacts para modo privado e publico

<img width="605" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/9da0425c-53dd-45a4-be2c-922b321e68b9">

Com o feed privado podemos compartilhar os pacotes com a nossa equipe e usuários específicos e no modelo publico podemos compartilhar com qualquer pessoa na internet.

<img width="587" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/e4ba3922-8cf7-4d28-b4b7-0a12d9a264b0">

E para trabalhar com o azure artifacts temos algumas práticas para seguir. Cada repositório deve referenciar apenas 1 feed. 
Podemos ter vários feeds para um projeto, mas um projeto específico deve fazer referencia a apenas um feed. Se quisermos usar pacotes de vários feeds precisamos usar fontes
upstream para acessar pacotes de vários feeds por meio de  um upstream.
Outra boa prática é publicar pacotes recentes no feed.
Devemos também habilitar as políticas de retenção, para limpar versões antigas do pacote, com isso melhoramos o desempenho e aumentamos espaço de armazenamento.

<img width="605" alt="image" src="https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/0d5088ca-6d0b-4bcf-8989-642b9cac55ee">

Devemos também promover os pacotes no modo de exibição correta, para isso podemos usar release e pre-release

![image](https://github.com/aevilesaguiar/azure-devops-board-repos-pipelane-test-artefats/assets/52088444/80560743-bc6c-4198-b42f-57efb80484e5)

