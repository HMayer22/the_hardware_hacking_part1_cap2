> O\
> Hardware
>
> Hacker
>
> Aventuras em Criação e
>
> quebrando hardware
>
> Andrew "coelho" Huang

> Parte 1. Capítulo 2.
>
> dentro de três fábricas muito diferentes
>
> Édifícil entendercomo funciona umcomputador sem abri-lo e olharseu
> interior.Da mesma forma, é difícil entendercomoos produtos sãofeitos
> sem entrar em uma fábrica e conheceralinha. Emboramuitas vezes
> pensemos naproduçãocomo uma etapa necessária,mas enfadonha, após a
> inovação, narealidade,as duas estãointimamente ligadas. Um
> inventorpensa umavez num produto; umafábricapensa no mesmo produto
> todos os dias,às vezes durante anosafio.
>
> A importânciadas fábricas comocentrode inovação só estáa crescer na
> economiaglobal conectadade hoje.Arealidade é que não existe uma
> "fábricadaApple" ou "fábricada Nike". Em vezdisso, há uma série de
> instalações que são especialistas em processos (como\
> fabricaçãode PCB ou fabricaçãode zíperes) que são

**Capítulo 2**

com curadoria de marcas conhecidas. Portanto, não é incomum ver produtos
de dois concorrentes operando lado alado em linhas semelhantes em uma
única instalação.Essa concentração de conhecimento específico de um
domínio significaque o melhorlugarparaaprendercomo melhorarum aspecto do
seu produto é muitas vezes o mesmo lugar que fazum aspectosemelhantenos
produtos de todos os outros.

Algunsdos maiores insights que tive sobre como melhorar um produto
vieram da observação de técnicos trabalhando em uma linha edos truques
inteligentes de otimização que eles desenvolveram depois de fazerem a
mesma coisarepetidamente portanto tempo.

Este capítulo leva você a um passeiopor três fábricas que fabricam
coisascotidianas: PCBs (em particular,os usados noArduino),cartões de
memória USB e zíperes. Aoabriracortina,você terá algunsinsights sobre as
compensações dedesign por trás dos produtos e como elas podem ser
melhoradas. Na fábricade PCB,descobriosegredode como eles imprimem um
mapadaItália em alta resolução naparte de trás de cadaArduino; na
fábricade cartõesde memória USB, testemunhei um estranhocasamento entre
técnicasde fabricaçãode alta e baixa\
tecnologia; e na fábricade zíperes,descobri comoaté os produtos mais
humildes podem trazer lições valiosas paradesigners de produtos.

**onde nascem os arduinos**

Era julho de2012ejá se passaram cercade seis meses desde que
minhastartup anterior, a Chumby, encerrou as operações. Decidi tirarum
ano de folga para resolveras coisas e riscaralguns itens da lista de
desejos, um dos quais era uma viagemà Itália. Minha namoradatevea
brilhante ideia de entrarem contato coma equipe do Arduino paraver se eu
poderiavisitarafábrica deles em Scarmagno (isso foianos antes da
divisãoArduino/Genuino) como parte do nosso itinerário.

Os membros da Officine Arduino(particularmente o diretor-gerente Davide
Gomba) gentilmente reservaram um tempo de suas agendas lotadas
paramostrar


> meem torno de suafábrica.Eles esperarampacientemente enquanto eu
> expressava meu fotógrafo interno e meu amor geral por todas as coisas
> de hardware,e eu definitivamente saí commuitas fotos ótimas.
>
> Uma pequenacidade no norte daItália, Scarmagno fica a cerca deuma
> horae meia de carro a oeste de Milão, perto das fábricas da Olivetti,
> nos arredores de Torino. A cidade cuida detoda a fabricação deplacas
> de circuito, preenchimento de placase distribuição de Arduinos de
> marcaoficial. Fiquei muito animado para ver as fábricas,e o destaquedo
> meu passeio foi conheceraSystemElettronica, a fábrica de PCBs que
> fabricava os PCBs do Arduino.
>
> Um aspecto encantador daSystemElettronica é que o proprietário pintou
> a fábrica de verde, branco e vermelho para combinar com as cores da
> bandeira italiana. No chão de fábrica,vi um pouco desseespíritonos
> postes vermelhos e verdes que percorriam toda a extensão dainstalação.
>
> Visão ampla do chão de fábrica da SystemElettronica em agostode2012
>
> Maslogoparei de prestar muitaatençãoàdecoração,pois aquele chãode
> fábrica também eraonde pude acompanhar um novolote de ArduinoLeonardos
> durante todooprocessode fabricação.Vejacomo essas placas foram feitas.

**Capítulo 2**

**começando com uma folha de cobre**

As placas Arduino Leonardo começam como enormes folhas de cobre virgem
FR-4,um materialfeito de fibrade vidro e epóxi que a maioria dos PCBs
usa como substrato, uma camadaisolante e estrutural entre as camadas de
cobre.

As folhas tinham1,6mmde espessura(a espessura mais comum para uma
PCB,que corresponde a1/16polegada), provavelmente um metro de largura e
cercade ummetro e meio de comprimento.


A primeira etapa no processamento de PCBs é perfurar todos os holepads,
vias (os pequenos orifícios que conectamas diferentes camadas do PCB),
orifícios demontagem, slots chapeados e assim por diante. Quandouma PCB
éfabricada, os furos são perfurados antespadronização, o estágioem queum
produto químico de mascaramento é definido fotograficamente na folha em
todos os lugares emque as placas finais precisam tercobre, incluindo
locais de\
vestígios,almofadas de solda e assim por diante. Alguns dos furos são
usados paraalinharas máscaras que modelam os traços posteriormenteno
processo. A perfuração também é um processo sujo e confuso que
podedanificar os padrões do circuito se eles estiverem instalados
antecipadamente.

dentrodetrês fábricas muito diferentes


A cabeçade perfuração CNC usadaparaperfurar asplacas Arduino

> Os painéis de cobre vazios foram empilhados em três alturas, e uma
> furadeira CNC fez uma únicapassagem emtodos os três, permitindo
> perfurar três substratos porvez.

O rack deperfuração usadopela furadeira CNC.

Se você já teve que criararquivos de perfuração NC, este é o "suporte de
perfuração".

> Cadafuro naplacaArduino foi perfurado mecanicamente,incluindo vias.
> Omesmo se aplicaaqualquerPCBcom furos passantes, razão pelaqual
> acontagem de vias é um parâmetro tãoimportante nocálculo docustode
> umaPCB.

**Capítulo 2**

Observe que afuradeira específica que vi na System Elettronica era
relativamente pequena. Já vi enormes plataformas de perfuração na China
que agrupam(conectammecanicamente) quatro ou seis cabeças de\
perfuração em umamáquina do tamanho de um caminhão,processando dezenas
de painéis ao mesmo tempo,em oposição aos três painéisque esta broca
poderia suportar. O raciocínio por trás dessa abordagem éque o conjunto
de posicionamento robótico preciso é a partecara de uma furadeira. A
furadeira em si é barata -- apenas um motor giratórioparaacionara broca.
Portanto, uma maneira deaumentar o rendimento é agrupar várias brocas em
uma grande montagem e movê-las emconjunto. Cadafuradeira individual
ainda passa por sua própria pilha de painéis, mas pelo preço de um\
posicionador XY, você obtém de quatro a seis vezes o rendimento da\
furadeiraque vi emminha viagemàItália. Essas máquinas maiores perfuram
com tantarapidez e força que o solo treme a cada via perfurada, mesmo a
vários metros de distância.

Depoisque os painéis são perfurados, limpos e rebarbados,eles
estãoprontos para a próxima etapa do processo de fabricação.

> Umapilhade painéisperfurados e acabadosde placas Arduino Leonardo


> **aplicando opadrãoPCBao cobre**
>
> Opróximopasso é aplicarumfotorresistente, um produto químico sensível
> à luz, ao painel e expõe um padrão.Na System Elettronica esseprocesso
> utilizouumacaixa de luz e umfilme de alto contraste.Também viimagens
> diretas a laser -- naforma de um laser devarredura raster -- usadas
> para aplicarum padrão auma PCB. Os scanners a laser diretos são
> maiscomuns em casas de protótipos de giro rápido,e a imagem de filmeé
> maiscomum em casas de produçãoem massa.
>
> Antesedepois: o painel direito mostra fotorresiste antesda exposição,
> e o painel esquerdodepois.
>
> Uma PCB sendo montada emumacaixade luzque
> exporáseufilmetraseironãoprocessado

50**Capítulo 2**

Apósa aplicação do padrão, cada painel de placas éenviado para uma
máquina para ser desenvolvido. Neste caso, a mesma máquina
éutilizadapara revelar o fotorresistente e amáscara de solda.


> Amáquina que desenvolve o fotorresiste


> Essa foto de umpainel com fotorresistente reveladoéuma das minhasfotos
> preferidasda fábrica da SystemElettronica.
>
> Além disso, algo sobre"Codice: Leonardo"parecelegal.


dentrodetrês fábricas muito diferentes51

> **gravando os PCBs**
>
> Apóso processamento e revelação das fotos, os painéis passam por
> umasérie de banhos químicos que gravam e chapeiam o cobre.
>
> Os painéis são agitados suavemente para frente e para trás em um banho
> químico paraagilizar o processo de gravação. O movimento também
> circula o ácido usado paralonge dos painéis, garantindouma taxa de
> ataque mais uniforme,independentemente daquantidade de cobre a
> serremovida. A\
> movimentação dos painéis através desses banhos químicos foi totalmente
> automatizada em Scarmagno. A automação é necessária porque os painéis
> devem sertratados com uma série de banhos químicos cáusticos com
> exposição mínimaao oxigênio. O oxigênio pode estragarum painel em
> questão de\
> segundos,portanto atransferência entre os banhos precisa serrápida e a
> quantidade de tempo que umpainel passano banho deve ser consistente.
> Os banhos também contêmprodutos químicos prejudiciais aos seres
> humanos,por isso é muito mais seguro paraum robô fazer esse trabalho.
>
> Uma máquina quemovepainéis em gravador
>
> Umavez que os painéissão processadosnestasérie de soluções, um
>
> revestimentobranco e fosco (queeusuponho ser de níquel ou estanho) se
> desenvolve
>
> emtodasassuperfícies do painelnão tratadas com fotorresistente,
> incluindo asvias e
>
> almofadas doorifício de passagem anteriormente não revestidas .
>
> **Capítulo 2**


> Painéis de placasArduino Leonardo apóspassarempor uma
> sériedebanhosquímicos
>
> Neste ponto, aresistência e o cobre não revestido são removidos,
> deixando apenas o FR-4 bruto e o cobre revestido. A etapa final do
> processamentoproduzumacabamento de cobre brilhante.


> Painéis PCB com cobre brilhanteebrilhante. Esta foto não mostra um
> painelArduino, já queeles não estavam passando pela máquina
> quandoeufotografei.
>
> **aplicação de máscara de solda e serigrafia**
>
> Uma vez polido o cobre, os painéis estão prontos paraomáscara de
> solda( uma camada protetora semelhante alacaque isolaos traços de
> cobre abaixo eevita aformação de pontes de soldaacima) eserigrafia(a
> tintausada para rotular componentes,desenharlogotipos e assim por
> diante). Estes são aplicados em umprocesso muito semelhante ao dos
> padrões de traço,usando umafotomáscara e
> umamáquinareveladora/decapante.
>
> Um painel de placas Arduino commáscara desolda eserigrafia
> desenvolvido

**Capítulo 2**

NocasodosArduinos, a serigrafia é na verdade uma segunda camada da
máscara de solda. Umaformulação muito específica de máscara de solda
branca de filme seco foi adquirida pela equipe do Arduino para criar uma
camadanítida e bonita que resolvesse a intrincadaarte que você vê nas
placas do Arduino -- especialmente o mapada Itáliana parte traseira.
Outras técnicas quevi para a produção de camadas de serigrafia incluem
impressão a jato detinta de alta resolução, que é mais adequada para
casas de\
papelão de giro rápido e,claro, o processohomônimo de serigrafia comrodo
e pintura.

**Testandoefinalizandoas placas**

Depois de todo esse processamentoquímico,os painéis recebem um
revestimento

protetor de solda de uma máquina niveladora de solda a ar quente.

Com o revestimento de soldainstalado, cadaplaca é 100% testada. Cada
traço tem sua continuidade e resistênciamedidas com um par de sondas\
voadoras.O processo que vi é chamadoteste de cabeçavoadora(também
referido comotestede sondavoadora), e nesse tipo de configuração, vários
pares de braços com sondas emformade agulhatestam acontinuidade entre
pares de traços em ummovimento rápido de batidas. Considerando todos os
traços deum Arduino Leonardo,isso é muitainvestigação!Felizmente, os
braços do robô se movem como um borrão, pois ele pode sondar centenas
depontos porminuto.

**observação** Umaalternativa ao testedecabeça voadora éo testeem
concha, onde um conjuntodepinos pogoécolocadoem um acessório que pode
testar toda a placa com uma única operaçãomecânica. Noentanto, os
acessórios em formatodeconcha sãomuitotrabalhosos para montare manter e
exigem religaçãofísica semprequeos arquivos Gerber quedescrevem as
imagens PCB são atualizados. Portanto, em volumes menores, o testede
sonda voadora émais econômicoe flexível do que o teste em concha.

>
> Umapilhade painéisPCB quase acabados,\
> prontoparauma etapa final de roteamentodasplacas individuais
>
> Esta instalação específicaapenas criou os painéis; uma fábrica
> diferente realmente preencheu os componentes.Em situações como essa,
> antes que os painéis possam ser enviados paraapróxima fábrica, os PCBs
> individuais precisam serroteados paraque caibamdentrotecnologia de
> montagem em superfície (SMT)máquinas para colocar os componentes. Os
> painéis são novamenteempilhados e processados emlote por meio de uma
> máquina que utiliza umafresapara cortar e soltaras placas. Depois
> disso, as placas estão finalmente prontas para serem enviadas às
> instalações da SMT.

Vários painéisArduino, empilhados pararoteamento

**Capítulo 2**

>
> Uma verdadeirapilhade cercade 25.000 PCBs Arduino vazios, prontos para
> sairda fábricade PCBs. A partirdaí, eles foram recheados,\
> enviado e vendidoparafabricantesde todoo mundo!

Estou feliz por terfeito umaviagemparalelaparavisitara fábrica de PCB do
Arduino.Visiteivárias fábricas de PCB e cadauma delas tem
características diferentes e seu próprio conjunto de truques para
melhorarorendimento, bem como limitações exclusivas que os designers
precisam compensar.Tambémfoi interessante ver o pequeno truque de usarum

dentrodetrês fábricas muito diferentes57

camada extrade máscarade solda emvezde serigrafia paraobteralta
qualidade

> cosmética.Enquanto aresolução de uma serigrafia é limitada pela malha
> da
>
> barreirade sedapara seguraratinta, a máscara de solda é limitada pela

qualidade da óptica e do desenvolvimento químico, proporcionando
umamelhoria

> de ordemde magnitude naresolução e, em última análise, umaqualidade
>
> percebidamaisalta. Normalmente a qualidade inferiorda serigrafia é
> aceitável
>
> porque os usuários finais não veem as placas de circuito dentro dos
>
> computadores, mas paraoArduino, o produto finaléaplacade circuito.
>
> **onde nascemoscartões de memória USB**
>
> Váriosmeses depois de minha visitaà fábricadoArduino, tive asorte de
> ser opalestrante principal naLinux Conference Australia(LCA)2013.
> Emminhapalestra, "Linux in the Flesh:Adventures EmbeddingLinux in
> Hardware", discuti comooLinux está em todos ostiposde dispositivos que
> vemos todosos dias. Esta história não é sobre Linux, mas conecta amim
> e, tangencialmente,aoLCAa umafábrica.
>
> Umadas bugigangas que recebi dosorganizadores doLCA foi um
> pequenocartãode memória USB com opinguim Tux,o mascote do Linux,do
> ladode fora. Quando vi odispositivo,penseique era umapura
> coincidênciaque, cercade uma semanaantes daconferência, eu estivesse
> em uma fábrica que fabricavacartões de memória USB exatamente iguais.
> Eu vi oprocessode montagem daplacaUSB do inícioao fim e,
> surpreendentemente, envolveu muitomenosautomação doque oprocessode
> fabricaçãodoArduino.
>
> **O iníciodeum stick USB**
>
> Os pendrives USBcomeçam a vida comochips de memória flash simples.
> Antes de
>
> serem montados emPCBs,esses chips são avaliados quanto à capacidadee
>
> funcionalidadeda memória.



**Capítulo 2**


Em uma estação de trabalho nesta fábrica,pilhas dechips flash vazios\
aguardavam testes e armazenamentocom umcartãode sonda, que possui pinos
minúsculos e posicionados commuita precisão, usados para tocar almofadas
apenas um pouco mais largas doque umfiodecabelo humano na superfície de
um wafer de silício. (Adorocomoo trabalhador desta estaçãoem particular
usou elásticos para prender ummedidor decorrente analógico à placa de
sonda.)

A placa desonda, de perto

dentrodetrês fábricas muito diferentes59


> Olhando através do microscópio na estação demicrossondagem. Observe as
> agulhas tocando as almofadasquadradasnabordadasuperfíciedochipflash.
> Cada almofada tem talvez 100 mícronsde lado -- umfiode cabelohumanotem
> cerca de70 mícronsdediâmetro.
>
> Curiosamente,os chips quevi nãoforam testados de forma alguma em um
> ambiente de sala limpa. Os trabalhadores manuseavam os cavacos com
> pinças e tornos de sucçãomanuais emontavammanualmenteos cartões de
> sonda em seus gabaritos.
>
> **Colocando chips manualmenteem um PCB**
>
> Depois que os chips foramavaliados quanto à funcionalidade, eles foram
> colocados à mãonos PCBs do stick USB.Estanão é uma práticaincomum;
> todas as instalações de wire bonding orientadas paraovalor que visitei
> dependem da colocação manualdamatriz nua.

**Capítulo 2**


> UmIC controladorsendocolocado emumpainel de PCBsdependrive USB. As
> minúsculasmatrizes estãoàdireita, emum pacotede waffles.


> Uma visãoampliada da estação de trabalho de colocação dematrizes

A senhora que observei colocando o molde estavausandoumaferramenta
semelhante a umpauzinho feitade bambucortadoà mão. Aindanão descobri
exatamente como funciona o processo, mas meu melhor palpiteé que as
varas de bambu têma energia superficialcerta paraaderir.

dentrodetrês fábricas muito diferentes61

> a matriz de silício,de modo que o silíciogrude napontadahaste de
> bambu. Um ponto de cola épré-aplicadonas placas nuas,de modo que
> quando o operador toca a matriz nacola,atensão superficial da cola
> puxa a matrizda varade bambu.
>
> É estranho pensar que os chips dentro do meu pendrive foram
> manipulados com pauzinhos modificados.
>
> **ligando os chips aoPCB**
>
> Depoisque os chips foramcolocados no PCB,eles foramfio ligado à placa
> com umamáquina de colagemautomatizada, que usa reconhecimento de
> imagemassistido porcomputador para encontrar a localização das placas
> de colagem(essa é parte da razão pela qual as fábricaspodem se safar
> coma colocação manual das matrizes). A ligaçãode fios é o processo que
> conecta um circuito integrado à sua embalagem, e amáquina de ligação\
> automatizada conecta os fios ao IC a uma velocidade insana, girando a
> placade circuito o tempo todo.Enquantoeu observava esse processo, o
> operador teve que retirar esubstituir manualmente umfio mal colado
> e,em seguida, realocar o fio na máquina. Dado que esses fios são mais
> finos que um fio de cabelo eque asalmofadas de colagemna embalagem e
> no CI são microscópicas,issonão foiumatarefafácil de destrezamanual.
>
> **uma olhadamais de perto nas placasUSB**
>
> Assim comoafábrica do Arduino usava painéis contendo múltiplas placas
> Leonardo, afábrica de cartões de memória USB usava painéis deoito
> cartõesUSB cada. Cada stickno painel consistia em um chip de memória
> flash e umIC controlador que fazia a ponteentre o USB e o flash bruto,
> uma tarefanão trivial que inclui o gerenciamento de mapas de blocos
> defeituosos e correção de erros, entre outras coisas.Ocontrolador era
> provavelmente uma CPU da classe 8051 rodando a algumas dezenas de MHz.

**Capítulo 2**


> APCB parcialmente ligada, mas totalmente montada emmatriz, que o o
>
> proprietário dafábrica me deu como lembrança daminha visita.
>
> Algumas das ligações dos fios foram quebradas durante otransporte.

dentrodetrês fábricas muito diferentes63

> 
> Curiosamente, todo o conjunto do stick USB é flexível
> antesdoencapsulamento.
>
>
>
> Amarcação da matrizdo chip flash. Aparentemente, éfabricadopela Intel.

**Capítulo 2**


> Uma foto do chip controlador queestava dentrodospendrives

Depoisde colados e testados os painéis, eles foram moldados com epóxi e
depois cortados em pedaços individuais,prontos para venda.

Masisso é o suficiente sobre a fabricação de eletrônicos;a
seguir,queromostrar um tipodiferente de chãode fábrica.

**um conto de dois zíperes**

Meu amigo Chris "Akiba" Wang temumaformação semelhante à minha,
excetoque em sua juventude ele eramuito mais descolado:ele foidançarino
de artistas como LL Cool J e Run DMC nos anos 90. Depois depassar por
uma fase trabalhando para grandes empresas de semicondutores, ele
finalmente desistiu e seguiu sua paixão de projetar e fabricar
seuspróprios projetos de hardware. Especialista em redes sem fiode curto
alcance e baixo consumo de energia (eleé coautor de
umlivrosobreBluetooth de baixo consumo de energia evende uma
varianteArduino + 802.15.4\
chamada "Freakduino"),ele agora


dentrodetrês fábricas muito diferentes65

> prestaconsultoria para organizações como as Nações Unidas e a\
> Universidade Keio, administra o FreakLabs e colabora com vários
> artistas de dança, como o Wrecking Crew, parafornecer soluções
> deiluminação exclusivase atraentes para espetáculos de palco.
>
> Tive asorte de apresentarAkibaàárea metropolitanade Shenzhen em uma
> viagem comalunos doMIT MediaLab em 2013 -- amesma viagem emque
> visitamos a fábricade cartões de memóriaUSB.Desde então, ele tem
> exploradocadavez mais profundamente aárea.Como seu trabalhoabrange as
> disciplinas de arte performática, wearables e eletrônica, sua rede de
> fábricas é bem diferente da minha, por isso sempre
> aprecioaoportunidade de aprender mais sobre seu mundo.
>
> Emjaneirode 2015, Akiba me levou paravisitara fábricade zíperes de seu
> amigo. Fiquei muitoanimadocom opasseio:por mais humilde que
> sejaoproduto, sempre aprendoalgo novovisitandosuafábrica.
>
> Esta fábrica eramuitodiferente das instalações do Arduino e do stick
> USB. Havia muito menos funcionários e era um fabricante altamente
> automatizado e integradoverticalmente.Parase ter umaideiadoque isso
> significa, essainstalação transformou lingotesde metal, serragem e
> arroz empeças de zíper.
>
> Aproximadamente 1 tonelada de lingotes,\
> composto de 93% de zinco e 7% deliga de alumínio
>
> **Capítulo 2**


> Pelotasdeserragem comprimidas, usadas paraabastecerafundição de
> lingotes


Arroz,usadoparaalimentar os trabalhadores

dentrodetrês fábricas muito diferentes67


> Conjuntos de puxador de zíper e controle deslizante finalizados
>
> Vejamos um ladode como esse processorealmente funciona.
>
> **umprocesso totalmenteautomatizado**
>
> Entre os três materiais de entrada e o produto de saídahaviaumalinha
> de fundição sob pressão totalmente automatizada paracriaros puxadores
> e\
> controles deslizantes de zíper, um conjunto de copos e potes
> vibratórios (ou, como gosto de chamá-los,"vibrapots") paraliberar e
> poliros zíperes e um conjunto demáquinas pararebarbar e unir cada
> puxadorao seucontrole\
> deslizante. Acho que conteimenos de umadúzia de funcionários nas
> instalações e suponho que a capacidade deles excede em muitoum milhão
> de zíperes por mês.
>
> Fiqueihipnotizado pelos vibrapots\* que unem os zíperes. Havia dois
> vibrapots: um com extratores e outro com controles deslizantes.Tanto
> os controles deslizantes quanto os extratores foram depositados em um
> trilho móvel e, enquanto eu observava esses milagres em ação, parecia
> que os controles deslizantes e os extratores estavam se alinhando na
> orientação correta pormágica. Cadaum caiu em seu trilho e, no final da
> linha, foram pressionados juntos emumformato familiar de zíper,tudo em
> uma única máquinatotalmente automatizada.
>
> \* Sinceramente, não sei como eles sãochamados, então sim, vou
> continuar chamando-os assim.


**Capítulo 2**

Quando coloqueiamão napanela,descobrique nãohavianenhum agitador para
provocar o movimento;Eu apenas sentiuma forte vibração.

Relaxei minha mão e percebique ela começou a se moverjuntocom todos os
outros itens da panela.Todo o pote vibravade forma tendenciosa, de modo
que os itens dentro dele tendiama se mover em movimentos circulares.
Isso\
empurrou os puxadores e controles deslizantes parao conjunto
detrilhos,que forammoldados paraaproveitaras assimetrias dos objetos
para permitirque apenas as peças que saltavam no trilhona orientação
correta continuassempara apróxima etapa.

**umprocessosemiautomatizado**

Apesar do alto nível de automação nestafábrica,muitos dos trabalhadores
que vi realizavam uma única operação.Eles alimentaram os extratores de
um tipo diferente dezíper em umdispositivo conectadoaoutrovibrapot
contendo controles deslizantes, enquanto o dispositivojuntavaos
controles deslizantes e os puxadores.

Claro, perguntei:"Porque alguns zíperes têmprocessos de montagem
totalmente automatizados, enquanto outros são semiautomáticos?"\
Aconteceque a resposta é muitosutile seresume à forma.

> Observe a diferença entreessesdoisextratores, indicada pelassetas.


dentrodetrês fábricas muito diferentes69

> Uma pequenaguia,quase invisível, era a diferença entre aautomaçãototal
> e a necessidade de um ser humano paraunir milhões de controles
> deslizantes e extratores. Para entender o porquê, vamos revisaruma
> etapa crítica na operação do vibrapot. Umtrabalhador gentilmente
> pausouo vibrapotresponsávelpor classificar os extratores
> naorientaçãocorreta para o processo totalmente automático paraque eu
> pudesse tiraruma foto daetapa principal.

Extratores passando pelo vibrapot

> Quando os puxadores contornaram o trilho, suaorientação foialeatória:
> alguns voltados paraadireita, outros paraaesquerda. Mas aoperação de
> união só deve inserir o controle deslizante no menor dos dois
> orifícios. Essa pequena aba permitiu que agravidade fizessecom que
> todos os extratores pendurassem namesmadireção ao cair emum trilhoà
> esquerda.
>
> O design de zíper semiautomático não possuiessa aba; como resultado, o
> design é muito simétrico para que um vibrapot alinhe o extrator.
> Perguntei ao proprietário dafábrica se adicionar a pequena aba
> economizaria esse trabalho, e ele disse que sim.
>
> Nesse ponto, parecia extremamente óbvio para mim quetodos os zíperes
> deveriamter essa pequenaaba, mas o designer do zíper não a teria.
> Mesmo que essaaba sejamuito pequena, os consumidores podem sentir os
> solavancos sutis, e alguns percebem isso como um

**Capítulo 2**

defeitono projeto. Como resultado, o designer insistiu em uma aba
perfeitamentelisa, que, portanto, não tinhanenhum recurso que permitisse
a orientação automática de maneirafácile confiável.

**Aironia da escassez e dademanda**

Eu gostariade imaginar que a maioria das pessoas,depois deobservar uma
pessoa

unindo puxadores a controles deslizantes por alguns minutos, ficaria
bastante

contente em sofrer umpequenoimpacto na ponta do zíper para salvar outro
ser

humanododestinode alinhar manualmenteos puxadores em controles
deslizantes

duranteoito horas por dia.Alternativamente, suponho que um engenheiro
poderia

gastar inúmeras horas tentando projetar um métodomais complexopara
alinhar os

extratores econtroles deslizantes, mas há dois problemas com isso:

• Oclientedo zíper provavelmente não pagaria por esseesforço.

• Provavelmente é mais barato pagar mão de obra não qualificadapara
realizar a

> classificaçãomanualmente.

Odono da fábrica de zíperes jáhaviaautomatizado todo o resto nas
instalações, então imagino que eles também pensaram muito sobre esse
problema. Meu palpite é que a construção e a manutenção derobôssão
caras; as pessoas são auto-replicantes eem grande parteauto-\
sustentáveis. Lembra daquele terceiro insumo da fábrica: o arroz? As
peças sobressalentes de qualquerrobô têm que ser mais baratas queoarroz
para que o robô ganhe um lugarnafábrica.

Na realidade,porém, é muito trabalhosoexplicar esse conceitoaos
clientesfinais; na verdade, acontece exatamente ooposto nomercado.

Montar os zíperes lisos envolve mãode obra extra, então oszíperes custam
mais; portanto, eles tendemaacabar em produtosde alta qualidade.
Issoreforçaainda mais a noçãode que zíperes realmente lisos, sem
nenhumapequenaaba,devem sero resultadode controle de qualidade e
atençãoaos detalhes.

Meu mundo está cheiodepequenas frustrações comoessa. Porexemplo, a

maioriados clientes considera os plásticos com acabamentoespelhado de

qualidade superior aos plásticos com acabamento acetinado. Há

dentrodetrês fábricas muito diferentes71

> não há diferençafuncional entre o desempenho estrutural dos dois
> plásticos, masfazeralgo comacabamento espelhado exige muito mais
> esforço. As ferramentas de moldagemporinjeção devem sercuidadosa e
> meticulosamente polidas e, em cada etapada fábrica, os trabalhadores
> devem usar luvas brancas. Montanhas de plástico são descartadas em
> busca de defeitos epelículas extras de plástico são colocadas sobre
> superfícies espelhadas paraprotegê-las durante o transporte.
>
> Apesar de todoesseesforço, apesar de todo esse desperdício, qualé a
> primeiracoisaqueos usuários fazem? Eles colocaram suas impressões
> digitais sujas em todoo acabamentoespelhado. Umminuto depois de um
> produto sairda caixa, todoesseesforçoédesfeito. Ou pior ainda, o
> usuário deixa a película protetora, resultandoem umefeitocosméticopior
> do que um acabamentoacetinado.
>
> Compare isso com o plástico com acabamento acetinado. Osacabamentos
>
> acetinados não requerem películas protetoras,são maisfáceisde manusear
> pelos
>
> trabalhadores e usuários, durammaise têm rendimentos muito melhores.
> Nas mãos
>
> do usuário, escondem pequenos arranhões,impressõesdigitais e pedaçosde
> poeira.
>
> Indiscutivelmente, o acabamento acetinado oferece uma melhor
> experiênciaao cliente
>
> alongo prazodo que o acabamento espelhado.
>
> Mas esse acabamento espelhado certamente fica lindo em fotos e
> exibições de showroom!
