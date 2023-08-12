# DocG6Graph
Documentation of how to utilize the G6 Graph for the PEED Project

Para a trilha génerica com visualização em grafos foi inicialmente feito um estudo premilinar de diferentes APIs para visualização em grafo. A API G6 Graph foi escolhida para ser usada no desenvolvimento do trilha génerica para esse tipo especifico de visualização. A API G6 Graph é um mecanismo de visualização de grafos. Ele fornece os recursos básicos de visualização de grafos, como desenho, layout, análise, interação e animação. Projetado para tornar as relações transparentes e simples. Permite que os usuários obtenham informações sobre dados relacionais. Para acessar a documentação dessa API e obter mais informações para uso acessar o site http://g6-v3-2.antv.vision/zh ou github https://github.com/antvis/g6 .

Instalação:
```
sudo apt-get install npm
sudo npm install --save @antv/g6 ou npm install @antv/g6
```
## Como utilizar:
Após feita a instalação é necessário realizar a importação por CDN. Logo, basta inserir a tag <script></script> com o source do G6 Graph. Há algumas versões diferentes que podem ser utilizadas, sendo algumas delas: 
  - https://gw.alipayobjects.com/os/antv/pkg/_antv.g6-3.7.1/dist/g6.min.js
  - https://gw.alipayobjects.com/os/lib/antv/g6/4.3.11/dist/g6.min.js (4.X and later versions)

Obs: É também possivel visualizar a versão do G6 utilizando o console.log a seguir: 
```
console.log(G6.Global.version)
```
Dados:
Os dados do G6 são compostos de 2 componentes, nodes e edges. Cada um é composto de duas propriedades, sendo elas:
  - Propriedades de estilo, corresponde à propriedades de estilo
  - Outras propriedades, como id e type, as quais são propriedades que não irão mudar independente de alterações no styles dos dado.
  - 
A variável data, a qual irá conter os dados dos nodes e edges que compõem o grafo seguem o padrão visto no exemplo abaixo.
```javascript
const data = {
  nodes: [
    {
      id: "node1",
      label: "Source",
      x: 150,
      y: 150
    },
    {
      id: "node2",
      label: "Target",
      x: 400,
      y: 150
    }
  ],
  edges: [
    {
      source: "node1",
      target: "node2",
      label: "I'm the edge"
    }
  ]
};
```

*Nodes* possuem as seguintes configurações no que diz repeito a suas prorpriedades:

Propriedades comuns:             
| Propriedade | Tipo | Descrição |
| --- | --- | --- |
| `id` | String |ID do node/vértice, deve ser único. |
| `x` | Number | Coordenada x. |
| `y` | Number | Coordenada y. |
| `type` | String | O tipo de formato do node. Pode ser algum dos tipo já existentes ou customizado. O Default é `circle`. |
| `size` | Number/Array | O tamanho da node. |
| `anchorPoints` | anchorPoints | As interações do nó e arestas relacionadas. Pode ser nulo. [0, 0] representa a âncora no canto superior esquerdo; [1, 1]representa a âncora na parte inferior direita. |
| `style` | Object | O style, aparência da node. |
| `label` | String | O texto que é visivel dentro da node. |
| `labelCfg` | Object | As configurações da label. |

A data pode ser preenchida de forma manual, ou através da leitura de um .json






