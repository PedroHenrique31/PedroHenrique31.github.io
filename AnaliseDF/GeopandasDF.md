# Retrato socioeconômico do Distrito Federal

Este projeto nasceu da ideia de pegar os dados da **PDAD 2024** e transformá-los em algo mais fácil de explorar. A pesquisa tem uma quantidade enorme de informações sobre o Distrito Federal, mas trabalhar diretamente com os microdados não é tão simples: antes de chegar ao mapa foi preciso entender o dicionário de variáveis, explorar as bases, selecionar o que seria útil e tratar os dados para que regiões e indicadores pudessem ser comparados.

Ao longo desse processo, os dados foram separados e reorganizados em conjuntos menores, voltados para temas como **renda, domicílios, infraestrutura urbana e mobilidade**. A partir deles, foram calculados indicadores para cada Região Administrativa e essas informações foram então associadas aos limites geográficos das RAs.

O resultado desse trabalho é o mapa que você encontra nesta página. A ideia é permitir que os dados sejam explorados diretamente pelo território do DF, tornando mais fácil visualizar diferenças entre as Regiões Administrativas e comparar os vários indicadores construídos a partir da PDAD.

O repositório tá em [Projeto GeoPandas](https://github.com/PedroHenrique31/ProjetoGeoPandas) usei isso como subtefúrgio para aprender a processar dados geográficos e acho que seria um serviço público interessante.

## Entendendo os indicadores de renda

Os indicadores de renda não mostram exatamente a mesma coisa. Alguns representam valores médios, enquanto outros ajudam a enxergar **como a renda está distribuída dentro de cada Região Administrativa**.

### Renda média

É a média das rendas observadas para aquela Região Administrativa. Ela oferece uma visão geral do nível de renda da região, mas pode ser bastante influenciada por rendas muito altas ou muito baixas.

Por exemplo, se nove pessoas recebem R$ 2.000 e uma recebe R$ 30.000, essa última pessoa aumenta consideravelmente a média. Por isso, é interessante observar a renda média junto com os percentis apresentados abaixo.

### P10 — 10º percentil

O **P10** representa o valor abaixo do qual estão aproximadamente **10% das observações** de renda daquela região.

Ele ajuda a observar a parte de menor renda da distribuição. Se uma RA possui P10 de R$ 1.000, isso significa que aproximadamente 10% das observações consideradas possuem renda de até esse valor, enquanto cerca de 90% estão acima dele.

### P25 / Q1 — primeiro quartil

O **P25**, também chamado de **primeiro quartil (Q1)**, é o valor abaixo do qual estão aproximadamente **25% das observações**.

Ele funciona como outro ponto de referência para a parcela de menor renda da região. Em outras palavras, aproximadamente um quarto das observações está abaixo desse valor e três quartos estão acima.

### P50 — mediana

O **P50** é a **mediana da renda** e divide as observações da região ao meio: aproximadamente **50% estão abaixo desse valor e 50% estão acima**.

A mediana é especialmente útil para comparar renda porque sofre menos influência de valores extremos do que a média. Uma RA pode, por exemplo, apresentar uma renda média elevada por causa de um grupo relativamente pequeno de rendas muito altas, enquanto sua mediana permanece consideravelmente menor.

### P75 / Q3 — terceiro quartil

O **P75**, ou **terceiro quartil (Q3)**, indica o valor abaixo do qual estão aproximadamente **75% das observações**. Consequentemente, cerca de 25% encontram-se acima desse ponto.

Comparar o P75 com a mediana e os percentis inferiores ajuda a perceber como a renda se distribui dentro da própria Região Administrativa.

### P90 — 90º percentil

O **P90** representa o valor abaixo do qual estão aproximadamente **90% das observações**. Apenas cerca de 10% estão acima desse valor.

Ele oferece uma referência para a parte de maior renda da distribuição sem depender diretamente dos valores mais extremos existentes na base.

## Como interpretar esses valores em conjunto

Os percentis podem ser imaginados como **pontos ao longo de uma fila de rendas ordenadas da menor para a maior**:

**menores rendas → P10 → P25 → P50 → P75 → P90 → maiores rendas**

Por isso, não é necessário escolher apenas um deles. A **média** oferece uma medida geral da renda da região; a **mediana (P50)** mostra melhor o centro da distribuição; P10 e P25 ajudam a observar sua parte inferior; e P75 e P90 mostram o comportamento da parte superior.

Ao alternar esses indicadores no mapa, é possível observar não apenas quais Regiões Administrativas apresentam rendas maiores ou menores, mas também perceber diferenças na **distribuição da renda dentro de cada região**.



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
