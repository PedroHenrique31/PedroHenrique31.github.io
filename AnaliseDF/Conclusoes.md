## Das conclusões — ou de como este projeto deixou de ser sobre renda

Eu já comecei este projeto com uma pulga atrás da orelha. Há quase dez anos, li sobre uma pesquisa internacional que colocava o Brasil entre os países em que havia maior distância entre a percepção das pessoas e alguns aspectos mensuráveis da própria realidade social ([Fundação Perseu Abramo](https://fpabramo.org.br/brasileiro-e-o-segundo-pior-na-percepcao-da-propria-realidade/) | [Folha de S.Paulo](https://www1.folha.uol.com.br/mundo/2017/12/1941021-brasil-e-2-pais-com-menos-nocao-da-propria-realidade-aponta-pesquisa.shtml)). Essa informação ficou na minha cabeça desde então. De alguma forma, sempre me incomodou a possibilidade de vivermos em um país que conhecemos muito menos do que imaginamos.

Mas este projeto, curiosamente, não começou como uma tentativa de investigar isso. **Eu só queria saber sobre renda.**

A ideia original era relativamente simples: comparar renda e custo de vida entre os estados brasileiros. Queria saber quanto as pessoas ganham, quanto custa viver em cada lugar e, a partir disso, tentar construir alguma comparação sobre onde uma determinada renda proporciona melhores condições de vida. Como fazer isso para o Brasil inteiro logo de cara seria coisa demais, resolvi começar pelo Distrito Federal, entender o processo e depois expandir.

Foi aí que apareceu um problema que eu ingenuamente não esperava ter: **qual renda?**

Pesquisando no Google, eu encontrava de tudo. Renda média, média da renda, renda domiciliar, renda domiciliar per capita, rendimento do trabalho, números de anos diferentes apresentados como se descrevessem a mesma coisa... Às vezes encontrava determinado indicador para um ano, mas não para outro. Em outros casos, jornais e páginas simplesmente reproduziam um número sem deixar suficientemente claro o que exatamente estava sendo medido. Antes mesmo de começar a comparar renda com custo de vida, eu já estava com dificuldade para estabelecer qual número deveria usar para representar a renda das pessoas.

Foi assim que cheguei às pesquisas oficiais do DF. Minha expectativa era bastante razoável: se existe um instituto público responsável por estudar estatisticamente o Distrito Federal, vou parar de depender de números soltos encontrados na internet e buscar a informação diretamente na fonte.

Só que a fonte também não resolveu o problema tão facilmente.

As informações existem, mas nem sempre estão organizadas de maneira consistente para o tipo de análise que eu queria fazer. Os indicadores apresentados mudam entre publicações e anos; uma edição traz renda média, outra trabalha com faixas de renda, outra apresenta valores relacionados ao salário mínimo. Parte das informações está em enormes planilhas, parte aparece em relatórios em PDF ou DOCX e, para piorar, coisas com nomes parecidos nem sempre significam exatamente a mesma coisa.

Então tomei uma decisão que acabou mudando o projeto inteiro: **em vez de procurar os indicadores prontos, fui abrir os microdados e calcular eu mesmo.**

Se eu queria saber a renda típica de uma população, poderia calcular a mediana. Se queria entender melhor sua distribuição e desigualdade, poderia olhar os quartis e outros quantis. Em vez de depender exclusivamente da maneira como os resultados haviam sido resumidos nas publicações, eu poderia voltar aos dados e construir os indicadores de que precisava, sabendo exatamente o que cada um significava.

E foi quando abri os microdados que aconteceu a grande virada deste projeto.

### Eu fui procurar renda e encontrei um retrato do DF

Tinha **MUITA COISA** ali.

Informações sobre domicílios, infraestrutura, transporte, deslocamentos, trabalho, características socioeconômicas e uma quantidade enorme de outras variáveis. Entre elas, descobri algo que particularmente me chamou atenção: existem dados capazes de estimar os fluxos de trabalhadores entre as regiões e até informações relacionadas ao tempo gasto nos deslocamentos entre casa e trabalho.

Isso é uma informação absurdamente importante.

Pense no tanto de discussão que existe no DF sobre ônibus, congestionamentos, rodovias, BRT, metrô e tempo perdido no trânsito. Agora pense no valor de saber não apenas que “o trânsito está ruim”, mas **de onde as pessoas estão saindo, para onde estão indo, quantas estão fazendo determinado trajeto e quanto tempo esses deslocamentos estão levando**.

Eu, pelo menos, nunca tinha ouvido falar dessas bases antes deste projeto. Na verdade, eu sequer conhecia direito o instituto que produzia essas pesquisas. E, se eu não sabia que essas informações existiam, comecei a me perguntar quantas outras pessoas também não sabem.

Foi nesse ponto que percebi que o problema que eu estava encontrando talvez não fosse exatamente uma falta de dados.

**Os dados estavam lá.**

O problema era outro.

### Dados não são informação — e informação ainda não é conhecimento

Existe um modelo bastante conhecido na área de inteligência (que eu tive que estudar quando fiz perícia computacional) chamado pirâmide **DIKW** (*Data, Information, Knowledge, Wisdom* — Dados, Informação, Conhecimento e Sabedoria). Sem entrar demais na discussão teórica sobre o modelo, ele ajuda muito a explicar o problema que encontrei [que você pode ler mais aqui](https://en.wikipedia.org/wiki/DIKW_pyramid#Representations).

Um conjunto enorme de respostas de uma pesquisa é **dado**.

Quando esses dados são organizados, resumidos, contextualizados e transformados em indicadores que conseguimos interpretar, começamos a produzir **informação**.

Quando conseguimos relacionar essas informações, compreender o que elas significam e utilizá-las para entender um problema concreto, começamos a produzir **conhecimento**.

E, idealmente, esse conhecimento deveria ajudar alguém a tomar uma decisão melhor.

Foi aí que comecei a enxergar este projeto de outra maneira. Talvez o grande gargalo não estivesse na produção dos dados, mas justamente no caminho que eles precisam percorrer depois de produzidos.

Não adianta muito saber que milhares de pessoas responderam a uma pesquisa sobre seus deslocamentos se essa informação termina em uma planilha gigantesca que quase ninguém abre. Não basta medir o tempo gasto no trânsito se essa medida não chega de maneira inteligível a quem discute mobilidade. Não basta registrar um problema: é preciso transformar esse registro em algo que possa ser compreendido, comparado e utilizado.

Isso vale para praticamente qualquer área.

Um policial não precisa depender de histórias e boatos sobre onde acontecem crimes: existem registros de ocorrência que podem ajudar a identificar padrões. Atendimentos de saúde produzem registros que podem indicar problemas recorrentes em determinada região. Acidentes de trânsito deixam dados que podem revelar pontos perigosos e ajudar a orientar mudanças na infraestrutura.

O registro é o começo da história, não o final.

E foi justamente aí que comecei a pensar não apenas em quem **produz** esses dados, mas em quem deveria transformá-los em conhecimento utilizável.

### Quem faz essa tradução?

Um cidadão conhece muito bem uma parte da realidade. Ele sabe quanto tempo **ele** demora para chegar ao trabalho. Sabe que o ônibus que **ele** pega está lotado. Conhece os problemas da rua e do bairro onde vive.

Mas ele dificilmente conhece sozinho o sistema inteiro.

Eu posso dizer quanto tempo gasto para chegar ao trabalho, mas não consigo, a partir da minha experiência pessoal, dizer qual região administrativa possui os maiores tempos de deslocamento do DF, quais são os principais fluxos de trabalhadores ou onde determinada intervenção beneficiaria mais pessoas.

É justamente para enxergar além das experiências individuais que produzimos estatísticas.

Mas então vem a outra ponta: **quem está transformando essas estatísticas em subsídio para quem decide?**

Que estrutura técnica existe em uma assessoria parlamentar, em uma campanha ou dentro do próprio governo para pegar essas bases, entender suas limitações, relacioná-las e entregar uma informação realmente útil para um deputado, governador, secretário ou candidato?

Porque o político também não tem como conhecer individualmente a experiência de milhões de pessoas.

É claro que ouvir a população é indispensável. Um governante precisa ouvir reclamações, conversar com comunidades e conhecer as demandas de quem vive os problemas. Dados estatísticos não substituem isso. Mas o Estado precisa decidir simultaneamente sobre problemas que atingem milhares ou milhões de pessoas, e alguma coisa precisa organizar essas experiências individuais em uma visão mais ampla.

Como decidir onde uma nova linha de ônibus é mais necessária? Onde uma intervenção viária teria maior impacto? Qual região deveria receber determinado equipamento público? Onde os tempos de deslocamento são maiores? Onde determinado problema está crescendo?

Não precisamos necessariamente concordar sobre **o que fazer** diante dessas informações. Essa é justamente uma das partes da política.

Mas seria bom, pelo menos, conseguirmos discutir a partir de alguma compreensão compartilhada sobre **o que está acontecendo**.

### E onde entra a IA nessa história?

A IA entrou para mim como uma espécie de experimento paralelo.

Eu tenho o hábito de perguntar para modelos de IA sobre assuntos que estou começando a investigar. Não porque considere suas respostas uma fonte definitiva, mas justamente porque elas são muito boas para produzir uma primeira aproximação: mostrar conceitos, indicar caminhos e resumir aquilo que aparece repetidamente nos textos com os quais tiveram contato.

Gosto de pensar nisso, com todas as ressalvas necessárias, como uma espécie de **eco do *zeitgeist* da internet** [ferrou né, corre aqui](Zeitgeist.md).

Não é uma pesquisa de opinião e uma resposta de IA obviamente não representa estatisticamente o que “a sociedade pensa”. Mas, como esses modelos são construídos a partir de enormes quantidades de produção humana, suas respostas frequentemente carregam ideias, associações e também confusões que aparecem repetidamente nesse material.

E foi depois de abrir os microdados que comecei a olhar com outros olhos para uma coisa que, em outro contexto, eu provavelmente faria sem pensar muito: simplesmente pedir para uma IA encontrar e organizar esses dados para mim.

Conheço gente que provavelmente entregaria a tarefa inteira para uma ferramenta como o Claude Code e esperaria o CSV sair do outro lado.

Só que agora eu ficaria com um pé atrás.

Porque **de onde a IA tiraria a informação?**

Se nem as próprias publicações oficiais apresentam de maneira uniforme os indicadores de renda que eu estava procurando, como um modelo saberia que dois números encontrados em páginas diferentes medem coisas distintas? Como saberia que determinada “renda média” é domiciliar e outra é per capita? Que uma publicação está falando de um ano e outra de outro? Que determinada comparação simplesmente não deveria ser feita?

Talvez acertasse. Talvez encontrasse os microdados, interpretasse corretamente o dicionário de variáveis e produzisse exatamente o resultado que eu queria.

Mas também poderia fazer algo muito mais perigoso: **me entregar uma resposta perfeitamente organizada, coerente e convincente construída a partir de números que não deveriam estar juntos.**

E eu talvez nunca percebesse.

A dificuldade da IA, portanto, acabou revelando para mim um problema muito maior que a própria IA.

### Porque essa confusão não começa nela

Ela já está espalhada pela maneira como nós mesmos tratamos informação.

Isso aparece no cidadão que conhece sua experiência, mas naturalmente não possui uma visão estatística do conjunto. Aparece na comunicação pública quando dados importantes existem, mas dificilmente chegam à população de maneira compreensível. Aparece na política quando propostas são apresentadas sem que fique claro de qual diagnóstico partiram.

E, na minha percepção, aparece com muita frequência também no jornalismo.

É extremamente comum vermos análises sobre economia, tributação, relações internacionais, estatística e políticas públicas sendo feitas por comentaristas cuja formação principal está em áreas completamente diferentes daquilo que estão explicando. Isso acontece em veículos com orientações políticas muito diferentes. Da GloboNews ao Brasil 247, da direita à esquerda, muda a interpretação política, mas permanece muitas vezes uma cultura de tratar assuntos profundamente técnicos como se bastasse ter uma pessoa inteligente e bem informada diante de uma câmera para analisá-los.

E isso ajuda a produzir uma coisa particularmente perigosa: **o erro que se repete até ganhar aparência de senso comum.**

Um exemplo que me incomodou durante este projeto foi justamente a renda. Em distribuições muito assimétricas, como costuma ocorrer com renda, a média pode contar uma história bastante diferente da mediana. Isso não significa que a média seja “errada”; significa que ela responde a uma pergunta diferente. Mesmo assim, conceitos estatísticos relativamente básicos como esse frequentemente desaparecem quando um número sai de uma base de dados, passa por uma publicação, chega ao jornal, circula pela internet e finalmente aparece numa discussão cotidiana.

Quando chega ao fim desse caminho, às vezes ninguém mais sabe exatamente o que aquele número significava no começo.

E aí ele entra novamente na internet.

E uma IA aprende com a internet.

O ciclo fica quase engraçado, se não fosse um pouco assustador.

### Isso acabou mudando também a maneira como eu penso a política

Talvez essa tenha sido a consequência mais inesperada de um projeto que começou simplesmente porque eu queria comparar renda e custo de vida.

Direita e esquerda continuam sendo categorias importantes para entender valores, prioridades e diferentes projetos de sociedade. Mas, para mim, elas perderam bastante força como **critério suficiente** para avaliar alguém.

Passei a sentir falta de uma pergunta anterior.

Antes de perguntar apenas **“o que essa pessoa pretende fazer?”**, comecei a querer perguntar também:

**“Como ela sabe que esse é o problema?”**

E depois:

**“Como chegou à conclusão de que essa é a solução?”**

Que informações sustentam a proposta? De onde vieram? O indicador utilizado mede realmente aquilo que está sendo afirmado? A equipe conseguiu distinguir correlação de causalidade? Média de mediana? Experiência individual de fenômeno coletivo? Duas estatísticas parecidas que, na verdade, foram construídas de maneiras diferentes?

Porque boa intenção não resolve essa etapa.

Pessoas de direita e de esquerda podem partir de valores diferentes e chegar legitimamente a soluções diferentes para o mesmo problema. Isso faz parte da política. O que me preocupa mais depois desta experiência é algo anterior: **e se nem estivermos descrevendo corretamente o problema sobre o qual estamos discordando?**

Uma política pública pode ser perfeitamente coerente com determinada visão de mundo e, ainda assim, fracassar porque partiu de uma descrição equivocada da realidade.

Foi aí que voltei, quase dez anos depois, àquela pesquisa de que falei no começo.

### Afinal, o quanto conhecemos a nossa própria realidade?

Existe um tipo de piada que fazemos muito com os estadounidenses. Aparece uma pesquisa pedindo para alguém apontar a Venezuela num mapa-múndi e surge alguém colocando o dedo em algum lugar perto da China. A graça está no absurdo da distância entre o mundo real e o mapa mental que aquela pessoa construiu dele.

Depois deste projeto, comecei a pensar que talvez tenhamos nosso próprio problema cartográfico.

Talvez saibamos perfeitamente onde ficam Brasília, Goiás, Bahia ou Amazonas no mapa e, ao mesmo tempo, tenhamos enorme dificuldade para nos localizar no **mapa estatístico da sociedade brasileira**.

Quanto ganha uma pessoa típica no lugar onde vivemos? Quanto tempo ela leva para chegar ao trabalho? Como isso muda entre bairros e regiões? Onde estão as maiores desigualdades? Como as pessoas se deslocam pela cidade? Que infraestrutura possuem em casa? Quais problemas são locais e quais aparecem sistematicamente em várias regiões?

E talvez a questão mais importante seja que essa dificuldade não afeta apenas o cidadão comum.

Se a informação não percorre adequadamente o caminho entre os dados e o conhecimento, o jornalista também tem dificuldade para explicá-la, o eleitor tem dificuldade para avaliar propostas, o assessor tem dificuldade para produzir diagnósticos e o governante pode ter dificuldade para decidir.

Voltamos, então, àquela velha inquietação: **como podemos ter uma boa percepção da nossa realidade se temos dificuldade até para transformar os dados que produzimos sobre ela em conhecimento acessível?**

E há uma pergunta ainda mais incômoda, que eu não tenho a pretensão de responder aqui:

**se compreender estatística é tão importante para compreender a sociedade em que vivemos, por que nossa formação para interpretar esses números é tão limitada?**

E, talvez mais provocativamente:

**a quem interessa que continue sendo assim?**

Não sei.

Mas agora quero pelo menos aprender a fazer perguntas melhores.

### E agora?

Foi por isso que este projeto deixou de ser apenas aquela comparação de renda que imaginei no começo.

O Distrito Federal foi uma escolha de escopo. Eu precisava começar por algum lugar pequeno o suficiente para conseguir entender as fontes, cometer meus erros, aprender a trabalhar com os microdados e descobrir que perguntas realmente valia a pena fazer.

E, mesmo assim, ainda há muita coisa para explorar aqui.

Quero voltar às análises do DF, aprofundar principalmente aquilo que encontrei sobre mobilidade e melhorar a maneira como essas informações são apresentadas. Também quero falar melhor sobre o próprio processo de desenvolvimento — inclusive sobre *vibecoding* e sobre como foi usar IA para construir parte das ferramentas deste projeto.

Mas a ideia original ainda está lá.

Eu queria comparar renda e custo de vida entre os estados brasileiros. Depois de tudo isso, talvez eu queira fazer algo um pouco maior: reunir para cada estado informações que ajudem a construir uma descrição minimamente comparável da realidade de quem vive ali — renda, custo de vida e, na medida do possível, outras dimensões que ajudem a contextualizar esses números.

Vai dar trabalho. Depois de conhecer as fontes, provavelmente **MUITO** mais trabalho do que eu imaginava quando tive essa ideia. 😅

Mas espero que esta primeira experiência já tenha contribuído de algum jeito.

Se não para responder onde é melhor viver, qual política pública devemos adotar ou quem está certo em determinada discussão, pelo menos para fazer uma coisa que agora me parece anterior a todas elas:

**tentar entender um pouco melhor o lugar onde vivemos antes de decidir o que queremos fazer com ele.**
