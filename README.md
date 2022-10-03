# Informações a respeito das eleições no dia (02/10/2022)

### <> Objetivo do repositório:
- O Jupyter Notebook `infos_eleicoes_2022.ipynb` conterá análises feitas enquanto os votos estavam sendo apurados no respectivo dia;
- Conterá análises para: 
  - Presidente da República
  - Governador
  - Deputado Federal
  - Deputado Estadual
  - Senador 
- Importante constar que mantenho-me imparcial quanto ao meu partido político, apenas apresentei algumas análises feitas ao vivo;

### <> Metodologia:
- Para garantir a confiabilidade dos dados obtidos para cada tipo de eleição, usufuí de API's oficiais do Tribunal Superior Eleitoral (TSE), em seu respectivo [site](https://resultados.tse.jus.br/oficial/app/index.html#/eleicao;e=e544/resultados) que fora atualizado à medida que os resultados saíam para cada cidade.
- Importante mencionar que quando trata-se de cargos distintos de presidente, utilizei filtros por estados, bastando apenas editar uma parte na requisição feito ao site oficial do TSE.
  - Exemplo para obter informações das eleições para Governador de MG: 
     `https://resultados.tse.jus.br/oficial/ele2022/546/dados-simplificados/mg/mg-c0003-e000546-r.json`
- Como uma boa prática do paradigma da POO, cada tipo de eleição está atrelado a uma classe específica, que, por sua vez, herda métodos gerais de uma classe mãe que denominei de `EleicaoBase`.
