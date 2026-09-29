# Retrato socioeconômico do Distrito Federal

Este projeto nasceu da ideia de pegar os dados da **PDAD 2024** e transformá-los em algo mais fácil de explorar. A pesquisa tem uma quantidade enorme de informações sobre o Distrito Federal, mas trabalhar diretamente com os microdados não é tão simples: antes de chegar ao mapa foi preciso entender o dicionário de variáveis, explorar as bases, selecionar o que seria útil e tratar os dados para que regiões e indicadores pudessem ser comparados.

Ao longo desse processo, os dados foram separados e reorganizados em conjuntos menores, voltados para temas como **renda, domicílios, infraestrutura urbana e mobilidade**. A partir deles, foram calculados indicadores para cada Região Administrativa e essas informações foram então associadas aos limites geográficos das RAs.

O resultado desse trabalho é o mapa que você encontra nesta página. A ideia é permitir que os dados sejam explorados diretamente pelo território do DF, tornando mais fácil visualizar diferenças entre as Regiões Administrativas e comparar os vários indicadores construídos a partir da PDAD.

O repositório tá em [Projeto GeoPandas](https://github.com/PedroHenrique31/ProjetoGeoPandas) usei isso como subtefúrgio para aprender a processar dados geográficos e acho que seria um serviço público interessante.

## Entendendo os indicadores de renda

Eu comecei todo esse projeto **Exclusivamente** com a ideia de renda na cabeça, porque queria provar um ponto específico, mas a medida que o trabalho de provar meu ponto se mostrou maior do que parecia, e fui obrigado a procurar dados no site do _Instituto de Pesquisa Estatística_ do DF (IPES-DF) eu resolvi aumentar o escopo e abarcar outras informações legais que achei, porque não né? Já tava fácil mesmo...

Embora isso prove meu ponto, o maior problema é que todo o objetivo do meu trabalho era voltado para a renda, então hoje eu confesso que fico meio perdido em como visualizar e o que fazer com esses outros dados que processei, aceito ajuda da intepretação de colegas que estiverem disponíveis.

Por hora vou me ater a **Renda** e não pretendo disicutir o penso aqui, quero apresentar friamente os dados e deixar vagamente uma interpretação de sua signficância estatística, a interpretação creio que seja mais rica se feita por cada um, e confesso que adoraria que compartilhassem sua opinião comigo.

Os indicadores de renda não mostram exatamente a mesma coisa e elemento principal a se notar nesse trabalho é que simplesmente caracterizar a **renda média** como classificador de uma região, é vazio de significado, e uma análise muito pobre. Por isso resolvi trazer toda sorte de indicadores para tentar evidenciar **como a renda está distribuída dentro de cada Região Administrativa**.

### Renda média

É a média das rendas observadas para aquela Região Administrativa. Ela oferece uma visão geral do nível de renda da região, mas pode ser bastante enganosa pois ela é influenciada por rendas muito altas ou muito baixas.

Por exemplo, se nove pessoas recebem R$ 2.000 e uma recebe R$ 30.000, essa última pessoa aumenta consideravelmente a média. Por isso, é interessante observar a renda média junto com algumas medidas de dispersão para ver o quanto os resultados se afastam dela.

Para o estudo da renda eu decidi abordar a divisão do valores em algo que na estatística chamamos de **quantis**.

Quantis são uma técnica de análise descritiva de dados, ao invés de usarmos fórmulas para calcular valores aproximados (a exemplo da média), nós ordenamos nossos dados em ordem crescente e então dividimos os dados em uma certa quantidade de grupos (chamados quantis, quando divimos em 4 são chamados quartis, em 5 quintis, até centis quando dividimos em 100 partes) e pegamos o valor que ocupa a posição Q desse grupo

### P10 — 10º percentil

O **P10** representa o valor abaixo do qual estão aproximadamente **10% das observações** de renda daquela região.

Ele ajuda a observar a parte de menor renda da distribuição. Se uma RA possui P10 de R$ 1.000, isso significa que aproximadamente 10% das observações consideradas possuem renda de até esse valor, enquanto cerca de 90% estão acima dele.


### P50 — mediana

O **P50** é a **mediana da renda** e divide as observações da região ao meio: aproximadamente **50% estão abaixo desse valor e 50% estão acima**.

A mediana é especialmente útil para comparar renda porque sofre menos influência de valores extremos do que a média. Uma RA pode, por exemplo, apresentar uma renda média elevada por causa de um grupo relativamente pequeno de rendas muito altas, enquanto sua mediana permanece consideravelmente menor.

### P90 — 90º percentil

O **P90** representa o valor abaixo do qual estão aproximadamente **90% das observações**. Apenas cerca de 10% estão acima desse valor.

Ele oferece uma referência para a parte de maior renda da distribuição sem depender diretamente dos valores mais extremos existentes na base.

## Como interpretar esses valores em conjunto

Os percentis podem ser imaginados como **pontos ao longo de uma fila de rendas ordenadas da menor para a maior**:

**menores rendas → P10 → P25 → P50 → P75 → P90 → maiores rendas**

Para se ter uma ideia de como uma região é desigual, é interessante muitas vezes analisar a diferença (em valores monetários) entre o P75 e o P25, isso é chamado _diferença interquartil_ e mostra bem o quanto uma região pode ser um abismo de valor entre os 25% mais ricos (que ganham pelo o valor de P75) e os 25% mais pobres (que ganham até o valor de P25).

Por isso, não é necessário escolher apenas um deles. A **média** oferece uma medida geral da renda da região; a **mediana (P50)** mostra melhor o centro da distribuição; P10 e P25 ajudam a observar sua parte inferior; e P75 e P90 mostram o comportamento da parte superior.

Ao clicar esses indicadores no mapa, é possível observar não apenas quais Regiões Administrativas apresentam rendas maiores ou menores, mas também perceber diferenças na **distribuição da renda dentro de cada região**.



## Como usar o mapa

O mapa reúne os indicadores calculados a partir dos dados da **PDAD 2024** e os apresenta por Região Administrativa do Distrito Federal. Os dados da pesquisa foram tratados e agrupados por RA e, posteriormente, associados aos limites geográficos de cada região para permitir sua visualização no mapa.

As **cores** representam o valor do indicador selecionado: regiões com valores semelhantes aparecem com tonalidades próximas, enquanto a escala apresentada na legenda ajuda a interpretar as diferenças entre elas. Você pode navegar normalmente pelo mapa, aproximando ou afastando a visualização, e passar o cursor sobre uma Região Administrativa para consultar seus dados.

Quando houver mais de uma camada disponível, o **controle de camadas** permite escolher qual indicador será representado pelas cores do mapa. Assim, o mesmo mapa pode ser utilizado para observar diferentes aspectos do Distrito Federal sem precisar abrir uma página diferente para cada indicador.

<iframe
    src="mapa_renda_df.html"
    width="100%"
    height="900"
    style="border: none;">
</iframe>
