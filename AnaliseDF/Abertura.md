# Projeto de análise socioeconômica do DF

Comecei esse projeto com uma ideia: agrupar as regiões administrativas do DF de acordo com suas características socioeconômicas. Com isso, queria encontrar problemas comuns e ajudar o público a definir metas e prioridades políticas para suas regiões. Mas esse esforço se mostrou mais difícil do que parecia.

Primeiro fui atrás de dados que permitissem fazer esse agrupamento e encontrei as pesquisas do IPE-DF (instituto de pesquisas estatísticas do DF uma espécie de IBGE só do DF todo Estado tem um e eu queria começar calculando o custo de vida de cada estado do Brasil para organizar eles). Só que, na hora de trabalhar com os resultados, esbarrei em um problema: eu não encontrava um padrão muito claro na disponibilização dos dados. Às vezes encontrava uma informação, mas não outra, e reunir tudo do jeito que eu precisava estava longe de ser simples.

Descobri que, para fazer o projeto da maneira que queria, teria que eu mesmo ir fuçar nas fontes e organizar os dados. E isso foi bem trabalhoso. Mas aqui está.

O resultado, por enquanto, é um trabalho mais descritivo das regiões do DF. A ideia é apresentar suas características e facilitar a leitura dessas informações. Ainda restam muitas análises e conclusões a serem tiradas daqui. Acreditem: o que está publicado aqui não tem nem 40% do que foi produzido.

Também confesso que me falta um feedback. Preciso saber o que interessa mais ao público, quais perguntas as pessoas gostariam de responder e que informações ajudariam a tomar uma boa decisão. Então, se você olhar os dados e pensar “queria entender melhor isso aqui”, já temos um caminho para continuar.

## Links para clicar

Tenho até vergonha, porque ainda preciso melhorar os textos e as explicações para deixar tudo mais amigável para quem lê. Mas, como tô fazendo tudo sozinho, ando meio confuso: tenho que olhar os dados, analisar, processar, gerar os gráficos e pensar em como colocar tudo na página. Depois ainda preciso escrever as explicações e tirar alguma conclusão — essa última parte é a mais difícil, e até agora não entreguei nenhuma 😅

Mas você já pode dar uma zoiada aí, clicar, arrastar e ver umas coisinhas com cores. 🌈⃤

- Nesse projeto você pode ver um mapa das RAs do DF organizados pelas informações de renda, preparei ele como um resumo de tudo que que temos, então tem também informações de caracterização dos domicílios, de meios de transporte e afins: [Aqui pra ver o mapa geral 👀](GeopandasDF.md)

- Nessa outra página, você pode explorar só o tópico de transportes, eu fiz um mapa de fluxos de como as pessoas se deslocam no DF, o sentido casa-trabalho, foi uma descoberta interessantissima saber que tem gente compilando esses dados, eles são MUITO úteis e servem para planejar muitas coisa do transporte do DF, mas infelizmente no pouco tempo de tive eu só reuni as descrições dele e fiz esse negocinho... tem muitíssimo mais informações a saber nesse topico aqui e pretendo aumentar depois: [Aqui pra ver a análise dos tranportes 👀](fluxosLaboraisDF.md)

Mas no geral os dois grandes objetivos que eu tinha eu diria que cumpri, que era criar os gráficos de análise mais facilitada, cheio de bolinha e frufru, corzinha essas bobajada que os analistas de dados amam pq evitar de ler números.

No mínimo vc vai pode se sentir no matriz vendo os bytes passando.


<iframe
    src="Keanu Reeves 90S GIF.gif"
    width="250"
    height="200"
    style="border: none;">
</iframe>

Ainda tem muito mais melhoria que dá pra fazer, mas confesso que aí começo a entrar no terreno do front end, e preciso organizar os dados que insights que queria mostrar, isso não dá tempo de ser feito até a eleição (que já é nesse domingo), mas quem sabe eu faça com calma depois e fique tudo pronto para uma próxima análise.

## Das conclusões

Ao longo desse projeto, passei por várias experiências e tirei conclusões sobre muita coisa. Vocês podem me lembrar e cobrar depois para falar de *vibecoding*, por exemplo: como foi o processo de usar IA para desenvolver os códigos. Também quero voltar às análises do DF (e nessa parte adoraria uma ajudinha de mais alguém).

Mas já posso adiantar uma reflexão que acabou virando o grande mobilizador do projeto inteiro. Depois de toda essa saga, fiquei com a sensação de que, nessa questão, direita e esquerda não fazem a menor diferença: se obter uma simples descrição socioeconômica das RAs do DF foi **TÃO TRABALHOSO** assim, como esperar que alguém consiga planejar um serviço público muito bom?

Por mais boa intenção que um político de qualquer matiz tenha, fica difícil acreditar que ele vá saber onde investir e como aplicar bem o dinheiro público se a informação que deveria ajudar nessa decisão, embora exista, é tão difícil de reunir e usar.

Como esperar que um político planeje melhor as linhas de ônibus ou as rodovias? Ou que saiba onde construir uma linha de BRT ou metrô? Você sabe onde fazer isso? Porque eu não. E, mesmo encontrando pesquisas que reúnem **TODAS ESSAS INFORMAÇÕES**, não encontrei uma apresentação que juntasse o que eu precisava para descrever e comparar as regiões sem ter que fazer todo esse trabalho antes.

Veja bem: não estou dizendo que somente as informações oficiais e os dados estatísticos são válidos na tomada de decisão. O político tem como um de seus principais papéis ouvir a população e suas reclamações para agir em cima disso. Mas também é óbvio que precisa haver uma forma mais inteligente de organizar e tratar essas informações, principalmente porque o Estado tem que lidar com vários problemas de várias pessoas ao mesmo tempo.

É importante formalizar os problemas para que eles sejam objetivos e tratáveis. Isso é algo básico que qualquer programador aprende no segundo semestre, quando vai implementar seu primeiro app, e creio que qualquer profissional lida com isso em algum momento. É justamente aí que, pela experiência que tive com esse projeto, vejo uma grande falha do GDF: transformar a informação disponível em algo que ajude a planejar.

Imagine se o policial tivesse que trabalhar de forma artesanal, colecionando histórias e boatarias sobre crimes para decidir onde agir. A segurança pública teria dificuldade para prender até um ladrão de bolsa na feira. É por isso que existem sistemas e registros de ocorrências. Na saúde, os atendimentos também geram registros. Todas essas informações podem formar bases de conhecimento para auxiliar nas decisões seguintes.

Então, mesmo que um problema não seja resolvido na hora, a informação continua lá e pode ajudar depois. Os registros de crimes podem orientar o policiamento de uma região. Os dados de saúde podem ajudar a identificar problemas recorrentes em um bairro e planejar atendimento e conscientização. Os registros de acidentes podem orientar mudanças na infraestrutura para melhorar a fluidez e a segurança do trânsito.

A questão é fazer esses registros virarem planejamento. Minha impressão, ao tentar reunir os dados para este projeto, é que ainda falta enxergar os problemas em conjunto. Quando cada órgão trabalha por si, fica difícil entender como transporte, infraestrutura, renda e condições de vida se relacionam.

No caso do trânsito, por exemplo, minha crítica é que multas, controle de velocidade e burocracia podem acabar ocupando mais espaço do que a discussão sobre como melhorar os deslocamentos. Esse é um assunto que eu queria abordar futuramente, mas faltavam justamente as informações que comecei a organizar aqui para conseguir discutir isso direito.

Foi daí que esse projeto ganhou outro sentido para mim. Além de agrupar regiões parecidas, quero facilitar o acesso a uma descrição do DF que ajude a fazer perguntas melhores. As conclusões não estão todas prontas, mas pelo menos agora temos um ponto de partida para conversar sobre os problemas com alguma informação na mesa.

_De qualquer forma as informações estão aqui, espero que gostem, gostaria que servicem para ajudá-los em suas escolhas políticas no domingo... mas não sei se dá, pelo menos para brincar deu_

