# Retrato socioeconômico do Distrito Federal

Este projeto nasceu da ideia de pegar os dados da **PDAD 2024** e transformá-los em algo mais fácil de explorar. A pesquisa tem uma quantidade enorme de informações sobre o Distrito Federal, mas trabalhar diretamente com os microdados não é tão simples: antes de chegar ao mapa foi preciso entender o dicionário de variáveis, explorar as bases, selecionar o que seria útil e tratar os dados para que regiões e indicadores pudessem ser comparados.

Ao longo desse processo, os dados foram separados e reorganizados em conjuntos menores, voltados para temas como **renda, domicílios, infraestrutura urbana e mobilidade**. A partir deles, foram calculados indicadores para cada Região Administrativa e essas informações foram então associadas aos limites geográficos das RAs.

O resultado desse trabalho é o mapa que você encontra nesta página. A ideia é permitir que os dados sejam explorados diretamente pelo território do DF, tornando mais fácil visualizar diferenças entre as Regiões Administrativas e comparar os vários indicadores construídos a partir da PDAD.

O repositório tá em [Projeto GeoPandas](https://github.com/PedroHenrique31/ProjetoGeoPandas) usei isso como subtefúrgio para aprender a processar dados geográficos e acho que seria um serviço público interessante.

## Entendendo os indicadores de renda

Eu comecei todo esse projeto **exclusivamente** com a ideia de renda na cabeça, porque queria investigar um ponto específico. Só que, à medida que o trabalho de demonstrar esse ponto se mostrou bem maior do que parecia e eu fui obrigado a procurar dados no site do _Instituto de Pesquisa Estatística_ do DF (IPES-DF), resolvi aumentar um pouco o escopo e aproveitar outras informações interessantes que encontrei pelo caminho.

Porque não, né? Já estava fácil mesmo... 🫠

Embora isso tenha aumentado bastante o escopo do projeto, o objetivo original sempre esteve relacionado à **renda**. Por isso, confesso que ainda fico meio perdido sobre como visualizar e o que fazer com alguns dos outros dados que processei. Inclusive, aceito de bom grado a ajuda e a interpretação de colegas que estiverem dispostos a explorar essas informações comigo.

Por enquanto, vou me ater à **renda**. Também não pretendo discutir muito o que os resultados *significam* social ou economicamente. Minha intenção aqui é apresentar os dados da maneira mais direta possível e explicar o que cada indicador consegue — e o que não consegue — nos mostrar. A interpretação desses resultados, acredito, fica mais rica quando cada pessoa olha para os dados e tira suas próprias conclusões. E, claro, adoraria que compartilhassem essas interpretações comigo.

O principal ponto que quero destacar é que os indicadores de renda **não mostram exatamente a mesma coisa**. Simplesmente caracterizar uma Região Administrativa pela sua **renda média** pode esconder muita informação sobre quem realmente vive ali.

Por isso, em vez de olhar apenas para uma média, resolvi trazer alguns indicadores que nos ajudam a enxergar **como a renda está distribuída dentro de cada Região Administrativa**.

### Renda média

A renda média é provavelmente o indicador mais intuitivo de todos: somamos as rendas observadas em uma Região Administrativa e dividimos esse valor pela quantidade de observações.

Ela oferece uma visão geral da renda da região, mas pode ser bastante enganosa quando existem pessoas com rendas muito diferentes das demais.

Imagine, por exemplo, um grupo de dez pessoas. Nove delas recebem R$ 2.000 e uma recebe R$ 30.000. Essa única renda de R$ 30.000 é suficiente para puxar a média do grupo bastante para cima, mesmo que ela não represente a realidade das outras nove pessoas.

É justamente por isso que não quero depender somente da média. Precisamos de algumas outras maneiras de olhar para a distribuição dessas rendas.

E é aqui que entram os **quantis**.

### Mas o que são quantis?

O nome parece mais complicado do que a ideia realmente é.

Imagine que pegamos todas as rendas de uma Região Administrativa e colocamos as pessoas em uma grande fila, começando por quem possui a menor renda e terminando em quem possui a maior:

**😢 menores rendas → → → → → → → → → maiores rendas 💸🤑**

Depois disso, podemos marcar alguns pontos ao longo dessa fila.

Esses pontos são os **quantis**.

Quando dividimos os dados ordenados em quatro partes, falamos em **quartis**. Quando dividimos em cinco, temos **quintis**. Quando usamos cem divisões, temos os **percentis**.

Neste trabalho, os percentis são particularmente úteis porque permitem fazer perguntas bastante intuitivas. Em vez de perguntar apenas "qual é a renda média dessa região?", podemos perguntar coisas como:

**"Quanto ganha uma pessoa que está perto dos 10% de menor renda?"**

ou:

**"A partir de qual renda alguém entra aproximadamente nos 10% de maior renda?"**

Para isso, escolhi três pontos especialmente fáceis de interpretar: **P10, P50 e P90**.

**😢 menores rendas → P10 → → → P50 → → → P90 → maiores rendas 💸🤑**

Assim conseguimos observar um ponto próximo da parte mais pobre da distribuição, o centro dela e um ponto próximo da parte mais rica, sem depender somente dos casos mais extremos.

### P10 — olhando para a parte de menor renda

O **P10** é o ponto da distribuição abaixo do qual estão aproximadamente **10% das observações**.

Suponha, por exemplo, que uma Região Administrativa tenha um P10 de **R$ 1.000**. Isso significa que aproximadamente 10% das rendas observadas naquela região são de até R$ 1.000, enquanto os outros 90% estão acima desse valor.

Escolhi o P10 justamente porque ele permite olhar para a **parte de menor renda da população sem depender do caso mais extremo**.

Usar simplesmente a menor renda encontrada seria pouco representativo. Uma única pessoa com renda excepcionalmente baixa, uma observação incomum ou mesmo alguma situação particular poderia distorcer completamente nossa percepção.

O P10 é mais interessante porque nos leva para perto da parte inferior da distribuição, mas ainda representa um grupo relevante das observações.

### P50 — a mediana, é... ela mermo!

E finalmente chegamos a ela: **a mediana**.

Talvez você já tenha encontrado esse nome alguma vez nas aulas de estatística e depois nunca mais tenha dado muita atenção a ele. Pois bem: neste trabalho ela vai aparecer bastante. Pode ir se acostumando com ela. 🙂

A mediana é o **P50**, o ponto exatamente no meio daquela nossa grande fila de rendas.

Se colocarmos todas as pessoas em ordem, da menor renda para a maior, e caminharmos até o meio dessa fila, é ali que encontramos a mediana:

**50% das rendas estão abaixo dela e 50% estão acima.**

Parece uma informação simples — e é justamente essa simplicidade que a torna tão interessante.

Ao contrário da média, a mediana não se impressiona muito com aquela pessoa absurdamente rica que apareceu no final da fila. Ela quer saber onde está **o meio**.

Voltando ao exemplo anterior, em que nove pessoas ganham R$ 2.000 e uma ganha R$ 30.000, aquela renda de R$ 30.000 consegue puxar a média bastante para cima. A mediana, por outro lado, permanece ali perto dos R$ 2.000 recebidos pela maioria.

Ela é, portanto, uma medida muito mais resistente aos valores extremos.

E é justamente por estar no centro da distribuição e ser relativamente robusta a esses extremos que a mediana pode ser interpretada como uma boa representação estatística da ideia de **"valor típico"** de um conjunto de dados.

Se estivéssemos analisando alturas, por exemplo, poderíamos pensar na mediana como uma espécie de **"altura típica"** de uma pessoa daquele grupo. Aqui estamos fazendo a mesma coisa com a renda: a mediana nos dá uma referência bastante útil da **"renda típica" de uma pessoa daquela região**.

Por isso, daqui para frente, quando eu utilizar neste trabalho a expressão **renda típica**, estarei me referindo justamente à **renda mediana (P50)**. Essa nossa velha amiga ainda vai aparecer bastante por aqui.

### P90 — olhando para a parte de maior renda

Na outra ponta temos o **P90**.

Ele é o ponto abaixo do qual estão aproximadamente **90% das observações**. Consequentemente, apenas cerca de **10% estão acima dele**.

Se o P90 de uma região for R$ 15.000, por exemplo, isso significa que aproximadamente 90% das rendas observadas estão em até R$ 15.000, enquanto os 10% restantes estão acima desse valor.

A lógica para escolher o P90 é basicamente a mesma usada no P10, só que olhando para o outro lado da distribuição.

Eu quero observar a população de renda mais alta, mas não quero que toda a análise dependa simplesmente da pessoa mais rica encontrada na base.

Assim, **P10 e P90 funcionam como duas referências das pontas da distribuição**, sem ficarmos presos aos valores mínimos e máximos, que podem ser muito extremos.

### Intervalo Interquartil (IIQ)

Além desses pontos, existe outra informação interessante: **o quanto as rendas estão espalhadas**.

Para isso podemos utilizar o **Intervalo Interquartil (IIQ)**.

Aqui entram dois percentis que não precisamos analisar separadamente: o P25 e o P75. O P25 marca o ponto abaixo do qual estão aproximadamente 25% das observações, enquanto o P75 marca o ponto abaixo do qual estão aproximadamente 75%.

O IIQ é simplesmente a distância entre esses dois valores:

**IIQ = P75 − P25**

Na prática, ele mostra o tamanho do intervalo ocupado pela **metade central das rendas observadas**.

Quanto menor esse intervalo, mais próximas estão entre si as rendas dessa parte central da população. Quanto maior ele for, mais espalhadas estão essas rendas.

Isso nos dá uma medida de **dispersão** que complementa os outros indicadores. Duas regiões podem, por exemplo, possuir medianas parecidas e ainda assim apresentar distribuições bastante diferentes: em uma delas, boa parte das rendas pode estar concentrada em valores próximos; na outra, elas podem estar muito mais espalhadas.

É importante fazer essa distinção porque o IIQ, sozinho, não é uma medida completa de desigualdade social. Ele simplesmente nos ajuda a enxergar **quanto varia a metade central da distribuição**.

**Por enquanto, eu ainda não calculei o IIQ para todas as Regiões Administrativas.** A ideia está aqui porque é uma medida que considero interessante para complementar a análise, mas preferi não aumentar ainda mais o escopo do processamento neste momento. Se houver interesse — ou se alguém pedir 😅 — depois eu calculo e acrescento ao conjunto de indicadores.

### Então, como interpretar tudo isso junto?

No fim das contas, podemos imaginar nossos indicadores novamente naquela grande fila de rendas:

**😢 menores rendas → P10 → → → P50 → → → P90 → maiores rendas 💸🤑**

Cada indicador responde a uma pergunta um pouco diferente.

A **renda média** nos dá uma referência geral, mas pode ser puxada pelos extremos.

A **mediana (P50)** — ou, como passaremos a chamá-la, nossa **renda típica** — mostra onde está o centro da distribuição sem sofrer tanto com esses extremos.

O **P10** nos dá uma referência para a população de menor renda.

O **P90** faz o mesmo para a população de maior renda.

E, quando o incorporarmos à análise, o **IIQ** poderá ajudar a perceber se a metade central das rendas está relativamente concentrada ou muito espalhada.

Nenhum desses números conta a história inteira sozinho. É justamente **a diferença entre eles** que começa a tornar a análise interessante.

Ao clicar nesses indicadores no mapa, portanto, a ideia não é simplesmente descobrir quais Regiões Administrativas são "mais ricas" ou "mais pobres". É possível observar também **como essa renda está distribuída dentro de cada região** e perceber situações que uma simples média poderia esconder.


## Como usar o mapa

O mapa reúne os indicadores calculados a partir dos dados da **PDAD 2024** e os apresenta por Região Administrativa do Distrito Federal. Os dados da pesquisa foram tratados e agrupados por RA e, posteriormente, associados aos limites geográficos de cada região para permitir sua visualização no mapa.

As **cores** representam o valor do indicador selecionado: regiões com valores semelhantes aparecem com tonalidades próximas, enquanto a escala apresentada na legenda ajuda a interpretar as diferenças entre elas. Você pode navegar normalmente pelo mapa, aproximando ou afastando a visualização, e passar o cursor sobre uma Região Administrativa para consultar seus dados.

Quando houver mais de uma camada disponível, o **controle de camadas** permite escolher qual indicador será representado pelas cores do mapa. Assim, o mesmo mapa pode ser utilizado para observar diferentes aspectos do Distrito Federal sem precisar abrir uma página diferente para cada indicador.

<span style="color: #e74c3c;">Ah e tem de brinde uma pagina nova onde eu quis falar APENAS da parte de transporte do DF: </span> [Aqui](fluxosLaborais.md)

<iframe
    src="mapa_renda_df.html"
    width="100%"
    height="900"
    style="border: none;">
</iframe>
