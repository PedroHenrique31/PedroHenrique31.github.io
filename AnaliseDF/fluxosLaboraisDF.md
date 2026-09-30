# Fluxos laborais do Distrito Federal

Durante a exploração dos microdados da PDAD-A 2024, encontrei uma possibilidade que me chamou bastante a atenção: relacionar o lugar onde as pessoas moram com o lugar onde trabalham. Eu estava construindo outros indicadores do Distrito Federal, mas essa descoberta me deu vontade de abrir uma frente própria de trabalho. Afinal, além de conhecer as características de cada região, podemos observar como elas se conectam pela atividade laboral.

Foi daí que surgiu o grafo interativo de fluxos de trabalho: uma visualização das relações entre as regiões de residência e os destinos de trabalho, construída a partir de um dataset de fluxos origem-destino.

**Espero mesmo trazer algo de interessante, pois essa questão do transporte no DF acho que é a nossa pauta mais complexa.**

## Um dataset maior do que parece

O conjunto de dados não se limita às ligações entre as Regiões Administrativas (RAs) do DF. Ele também registra destinos em municípios de Goiás, incluindo cidades do entorno e lugares mais distantes, como Anápolis e Goiânia. O CSV de origem-destino utilizado nesta etapa contém 940 combinações, com 36 categorias de origem e 53 categorias de destino. Essas categorias incluem locais de trabalho como “No domicílio” e “Vários locais”, portanto nem todas correspondem a cidades ou RAs.

Quando todas essas relações aparecem juntas, o grafo fica grande e bastante carregado. Para tornar a leitura mais confortável, fizemos adaptações no recorte da visualização, inclusive retirando destinos de Goiás na etapa de desenho. O dataset completo permanece como base para outras análises: o que aparece na tela é um recorte dele.

## Para que serve o grafo?

O grafo permite explorar de onde saem os trabalhadores, para onde vão e qual é o volume estimado de cada ligação. Ele ajuda a formular perguntas sobre a concentração dos destinos de trabalho, as conexões entre regiões e a participação do trabalho realizado na própria RA de residência.

Com esse mesmo dataset, podemos construir uma **matriz origem-destino**: as linhas representam os locais de residência, as colunas representam os locais de trabalho e cada célula contém o número estimado de trabalhadores daquela combinação. O grafo apresenta essas relações visualmente, enquanto a matriz facilita comparações e cálculos.

Isso permite estudar a mobilidade laboral e os deslocamentos pendulares associados ao DF, dentro da cobertura da pesquisa. Embora seja comum falar em “fluxo migratório”, aqui estamos observando relações entre residência e trabalho, que não significam necessariamente mudança de residência nem viagem diária. Para analisar migração residencial, seriam necessárias outras informações.

## Como ler a visualização

| Elemento | Significado |
| --- | --- |
| **Bolinhas, ou nós** | Representam as localidades incluídas no recorte do grafo. |
| **Tamanho das bolinhas** | Indica o volume total estimado de trabalhadores recebidos pela localidade no recorte representado. Quanto maior a bolinha, maior esse volume. |
| **Linhas, ou arestas** | Representam os fluxos entre um local de residência e um local de trabalho. |
| **Setas** | Indicam o sentido da relação: da origem, onde a pessoa mora, para o destino, onde trabalha. |
| **Espessura das linhas** | Expressa a magnitude do fluxo estimado de trabalhadores entre aquela origem e aquele destino. |
| **Ligação de uma localidade com ela mesma** | Representa pessoas que moram e trabalham na mesma localidade. Inclui o trabalho no domicílio após a adaptação descrita abaixo. |
| **Informações ao passar o mouse (tooltip)** | Apresentam detalhes do nó ou do fluxo, permitindo consultar os valores que sustentam a visualização. |

O tamanho de uma bolinha, portanto, não é a população total daquela região: é uma representação do fluxo de trabalhadores que ela recebe. Já a espessura de uma aresta se refere a uma ligação específica. As escalas visuais ajudam a comparar os volumes, e os valores dos tooltips permitem consultar as estimativas numéricas.

A posição das bolinhas na tela é definida pelo arranjo do grafo. Ela não corresponde à localização geográfica das regiões, e a distância entre dois nós não representa quilômetros ou tempo de deslocamento.

### E quem trabalha em casa?

O dataset possui a categoria **“No domicílio”**, que faz sentido para descrever o local de trabalho, mas não é uma RA. Na preparação do grafo, esses trabalhadores são somados ao fluxo da própria região de residência, evitando criar uma bolinha chamada “No domicílio” como se fosse uma localidade.

Para preservar essa informação, o tooltip da ligação destaca separadamente **“pessoas que trabalham no domicílio”**. Assim, podemos representar o trabalho realizado na própria RA e ainda distinguir a parcela correspondente ao trabalho em casa.

_Seria uma informação interessante para algumas análises, mas não sei bem o que fazer com isso agora, porém note que home office no DF é algo bem raro_

## Uma curiosidade que me fez conferir os dados

Uma das pequenas surpresas foi encontrar **aproximadamente 41 trabalhadores estimados que moram no Lago Sul e trabalham em Alexânia**. Eu não acreditei de cara e quis conferir: uma ligação pequena, mas inesperada, que chamou minha atenção no meio de tantas outras.

Na lembrança inicial, associei esse exemplo a Abadiânia. Conferindo o CSV utilizado nesta etapa, o registro é de **Alexânia**, com estimativa de 41,49 trabalhadores. Fica aqui a curiosidade com o nome corrigido.

Esses números são **estimativas obtidas com os pesos amostrais da pesquisa**, não uma contagem direta de pessoas entrevistadas. Por isso aparecem valores decimais: os registros da amostra representam um contingente estimado de trabalhadores. O exemplo é um convite para explorar os dados, sem tirar agora conclusões sobre essa ligação.

## Próximo passo: um mapa de fluxos

No futuro, quero acrescentar um **mapa de fluxos**, colocando as relações origem-destino sobre uma base geográfica. Ele permitirá observar essas conexões junto da localização real das regiões e dos municípios, complementando a leitura do grafo.

## Conclusões sobre os fluxos

<!-- Espaço reservado para acrescentar as conclusões após a análise dos fluxos laborais. -->

<!--
<iframe
    src="grafo_fluxos_trabalho.html"
    width="100%"
    height="900"
    style="border: none;">
</iframe> 

-->
