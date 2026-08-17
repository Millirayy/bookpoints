<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Book Points 📚</title>

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Georgia, serif;
        }

        body {
            background: #fff7fb;
            color: #5b4050;
            min-height: 100vh;
        }

        /* CABEÇALHO */

        header {
            background: #f3d6e5;
            padding: 25px;
            text-align: center;
            box-shadow: 0 3px 12px rgba(120, 70, 100, 0.12);
        }

        header h1 {
            color: #8b5270;
            font-size: 36px;
        }

        header p {
            margin-top: 7px;
            color: #765568;
            font-size: 16px;
        }

        /* CONTAINER */

        .container {
            max-width: 1100px;
            margin: 30px auto;
            padding: 20px;
        }

        .tela {
            display: none;
            animation: aparecer 0.5s ease;
        }

        .ativa {
            display: block;
        }

        @keyframes aparecer {

            from {
                opacity: 0;
                transform: translateY(15px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }

        }

        /* INÍCIO */

        .inicio {
            text-align: center;
            padding: 30px 10px;
        }

        .simbolo {
            font-size: 55px;
            color: #c982a5;
            margin-bottom: 10px;
        }

        .inicio h2 {
            color: #8b5270;
            font-size: 31px;
            margin-bottom: 15px;
        }

        .descricao {
            max-width: 750px;
            margin: auto;
            font-size: 18px;
            line-height: 1.7;
        }

        .escolha {
            margin-top: 35px;
            color: #765568;
            font-size: 21px;
        }

        /* LIVROS */

        .livros {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-top: 25px;
        }

        .livro {
            background: white;
            border: 2px solid #efd0df;
            border-radius: 25px;
            padding: 20px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 5px 18px rgba(130, 80, 110, 0.09);
        }

        .livro:hover {
            transform: translateY(-8px);
            border-color: #d99ab8;
            box-shadow: 0 10px 25px rgba(130, 80, 110, 0.16);
        }

        .capa {
            width: 170px;
            height: 250px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 18px;
            box-shadow: 0 5px 12px rgba(0,0,0,0.15);
        }

        .livro h3 {
            color: #8b5270;
            font-size: 20px;
            line-height: 1.3;
            margin-bottom: 8px;
        }

        .autor {
            color: #a06c86;
            font-size: 14px;
            margin-bottom: 10px;
        }

        .livro p {
            color: #876b79;
            font-size: 14px;
            line-height: 1.5;
        }

        /* LEITURA */

        .leitura {
            background: white;
            border-radius: 25px;
            padding: 35px;
            box-shadow: 0 5px 20px rgba(130, 80, 110, 0.1);
        }

        .topo-leitura {
            text-align: center;
        }

        .topo-leitura .capa {
            width: 150px;
            height: 220px;
        }

        .titulo-livro {
            color: #8b5270;
            font-size: 30px;
            line-height: 1.3;
            margin-bottom: 5px;
        }

        .autor-leitura {
            color: #a06c86;
            margin-bottom: 20px;
        }

        /* CRONÔMETRO */

        .cronometro {
            position: sticky;
            top: 10px;
            z-index: 10;

            width: fit-content;
            margin: 15px auto 30px;

            background: #f5dce8;
            color: #8b5270;

            padding: 13px 30px;
            border-radius: 40px;

            font-size: 29px;
            font-weight: bold;

            box-shadow: 0 4px 12px rgba(130, 80, 110, 0.12);
        }

        /* RESUMO */

        .resumo {
            background: #fffafd;
            border-left: 6px solid #d99ab8;
            border-radius: 12px;

            padding: 30px;

            font-size: 17px;
            line-height: 1.9;

            text-align: justify;
        }

        .resumo h3 {
            color: #8b5270;
            margin-bottom: 15px;
            text-align: center;
            font-size: 24px;
        }

        .resumo p {
            margin-bottom: 18px;
        }

        /* BOTÕES */

        .botao {
            display: block;

            margin: 30px auto 0;

            background: #c982a5;
            color: white;

            border: none;
            border-radius: 30px;

            padding: 14px 30px;

            font-size: 16px;

            cursor: pointer;

            transition: 0.3s;
        }

        .botao:hover {
            background: #a96586;
            transform: scale(1.04);
        }

        /* FINAL */

        .final {
            background: white;
            border-radius: 25px;

            padding: 55px 25px;

            text-align: center;

            box-shadow: 0 5px 20px rgba(130, 80, 110, 0.1);
        }

        .bombom {
            font-size: 75px;
            margin-bottom: 15px;
        }

        .final h2 {
            color: #8b5270;
            font-size: 29px;
            margin-bottom: 18px;
        }

        .final p {
            font-size: 18px;
            line-height: 1.7;
            max-width: 650px;
            margin: auto;
        }

        .destaque {
            color: #c982a5;
            font-weight: bold;
        }

        /* CELULAR */

        @media (max-width: 750px) {

            .livros {
                grid-template-columns: 1fr;
            }

            .livro {
                max-width: 350px;
                margin: auto;
            }

            .inicio h2 {
                font-size: 27px;
            }

            .descricao {
                font-size: 16px;
            }

            .leitura {
                padding: 20px;
            }

            .resumo {
                padding: 20px;
                font-size: 16px;
                line-height: 1.8;
            }

            .titulo-livro {
                font-size: 25px;
            }

        }

    </style>

</head>


<body>

<header>

    <h1>📚 Book Points</h1>

    <p>
        Leia por 10 minutos, descubra novas histórias e conquiste seu prêmio! 🍫
    </p>

</header>


<div class="container">


    <!-- ========================= -->
    <!-- TELA INICIAL -->
    <!-- ========================= -->

    <section id="inicio" class="tela ativa">

        <div class="inicio">

            <div class="simbolo">
                ♡
            </div>

            <h2>
                Bem-vindo ao Book Points!
            </h2>

            <p class="descricao">

                Aqui, cada minuto de leitura vale a pena! 📖

                <br><br>

                Escolha um dos livros abaixo e você terá
                <strong>10 minutos</strong> para ler o resumo
                da história.

                <br><br>

                Leia com atenção, pois depois da leitura
                serão feitas perguntas <strong>na sala de aula</strong>.

                <br><br>

                Quem responder corretamente poderá ganhar
                um delicioso <strong>bombom! 🍫</strong>

            </p>


            <h3 class="escolha">
                Escolha sua leitura:
            </h3>


            <div class="livros">


                <!-- LIVRO 1 -->

                <div class="livro"
                     onclick="iniciarLeitura('lua')">

                    <img
                        class="capa"
                        src="https://m.media-amazon.com/images/I/81luFS7PasL._SL1500_.jpg"
                        alt="Capa de O Despertar da Lua Caída"
                    >

                    <h3>
                        O Despertar da Lua Caída
                    </h3>

                    <div class="autor">
                        Sarah A. Parker
                    </div>

                    <p>
                        Fantasia, mistério, romance e
                        acontecimentos sobrenaturais.
                    </p>

                </div>


                <!-- LIVRO 2 -->

                <div class="livro"
                     onclick="iniciarLeitura('marques')">

                    <img
                        class="capa"
                        src="https://tse3.mm.bing.net/th/id/OIP.8LB14n6luRe4lst5HtdTZwHaKp?r=0&rs=1&pid=ImgDetMain&o=7&rm=3"
                        alt="Capa de Como Se Casar com um Marquês"
                    >

                    <h3>
                        Como Se Casar com um Marquês
                    </h3>

                    <div class="autor">
                        Julia Quinn
                    </div>

                    <p>
                        Romance histórico, humor,
                        segredos e encontros inesperados.
                    </p>

                </div>


                <!-- LIVRO 3 -->

                <div class="livro"
                     onclick="iniciarLeitura('hope')">

                    <img
                        class="capa"
                        src="https://cdn.kobo.com/book-images/8b99911e-9cc5-40ec-944e-7a0fa0e104fb/1200/1200/False/o-massacre-da-familia-hope.jpg"
                        alt="Capa de O Massacre da Família Hope"
                    >

                    <h3>
                        O Massacre da Família Hope
                    </h3>

                    <div class="autor">
                        Riley Sager
                    </div>

                    <p>
                        Suspense, mistério, investigação
                        e segredos de família.
                    </p>

                </div>


            </div>

        </div>

    </section>


    <!-- ========================= -->
    <!-- TELA DE LEITURA -->
    <!-- ========================= -->

    <section id="leitura" class="tela">

        <div class="leitura">


            <div class="topo-leitura">

                <img
                    id="capaLeitura"
                    class="capa"
                    src=""
                    alt="Capa do livro"
                >

                <h2
                    id="tituloLivro"
                    class="titulo-livro">
                </h2>

                <p
                    id="autorLivro"
                    class="autor-leitura">
                </p>

            </div>


            <!-- CRONÔMETRO -->

            <div class="cronometro">

                ⏱️

                <span id="tempo">
                    10:00
                </span>

            </div>


            <!-- RESUMO -->

            <div
                id="resumo"
                class="resumo">
            </div>


            <button
                class="botao"
                onclick="finalizarLeitura()">

                Finalizar leitura

            </button>


        </div>

    </section>


    <!-- ========================= -->
    <!-- TELA FINAL -->
    <!-- ========================= -->

    <section id="final" class="tela">

        <div class="final">

            <div class="bombom">
                🍫
            </div>

            <h2>
                Tempo de leitura encerrado! 💗
            </h2>

            <p>

                Muito bem! Você concluiu seus
                <span class="destaque">
                    10 minutos de leitura
                </span>.

            </p>

            <br>

            <p>

                Agora é hora de guardar o que você aprendeu,
                porque as perguntas serão feitas
                <strong>na sala de aula</strong>.

            </p>

            <br>

            <p>

                Responda corretamente e conquiste
                seu <strong>bombom! 🍫✨</strong>

            </p>


            <button
                class="botao"
                onclick="voltarInicio()">

                Escolher outro livro 📚

            </button>

        </div>

    </section>


</div>


<script>


    /* ========================= */
    /* CONFIGURAÇÃO DOS LIVROS */
    /* ========================= */


    const livros = {


        lua: {

            titulo: "O Despertar da Lua Caída",

            autor: "Sarah A. Parker",

            capa:
            "https://m.media-amazon.com/images/I/81Y5qfJqEHL._SL1500_.jpg",

            resumo: `

                <h3>O Despertar da Lua Caída</h3>

                <p>
                Em um mundo de fantasia marcado por magia,
                criaturas poderosas e um passado cheio de conflitos,
                Raeve aprendeu a sobreviver seguindo uma regra simples:
                cumprir suas missões e não deixar que ninguém descubra
                quem ela realmente é.
                </p>

                <p>
                Ela trabalha como assassina para um grupo que se opõe
                ao governo do Grado e está acostumada a agir sozinha.
                Raeve não procura reconhecimento, glória ou amizade.
                Seu objetivo é completar o que lhe foi ordenado e
                desaparecer antes que alguém consiga encontrá-la.
                </p>

                <p>
                A vida de Raeve muda quando uma de suas missões coloca
                seu caminho diante de um caçador de recompensas
                particularmente perigoso.
                </p>

                <p>
                Depois de um confronto, Raeve acaba capturada pela
                Guilda dos Nobres, uma organização formada por
                feéricos extremamente poderosos.
                </p>

                <p>
                Para eles, Raeve não é apenas uma prisioneira.
                Ela pode ser transformada em um exemplo para todos
                aqueles que desafiam o poder estabelecido.
                </p>

                <p>
                Enquanto Raeve está presa, outra história começa
                a se aproximar da dela.
                </p>

                <p>
                Kaan Vaegor passou por uma tragédia que mudou
                completamente sua vida. Consumido pela perda de
                seu grande amor, ele tomou decisões extremas e
                passou a procurar respostas para acontecimentos
                relacionados às luas daquele mundo.
                </p>

                <p>
                Kaan procura fragmentos lunares e acaba chegando
                à prisão onde Raeve está mantida.
                </p>

                <p>
                O encontro entre os dois é cercado de desconfiança.
                Raeve não confia facilmente em ninguém, enquanto
                Kaan percebe que existe algo nela que lhe parece
                estranhamente familiar.
                </p>

                <p>
                Aos poucos, acontecimentos do presente começam
                a se conectar com acontecimentos de muitos anos
                antes.
                </p>

                <p>
                As luas possuem uma importância muito maior do que
                Raeve imaginava. Elas estão ligadas às memórias,
                às perdas e aos poderes daquele universo.
                </p>

                <p>
                A fuga da prisão acaba sendo apenas o começo.
                Raeve e Kaan precisam descobrir por que suas
                histórias parecem estar conectadas e por que
                determinados poderes estão interessados neles.
                </p>

                <p>
                Ao longo da jornada, Raeve precisa enfrentar
                seu próprio passado e aprender a confiar novamente.
                Kaan também precisa lidar com a perda que marcou
                sua vida.
                </p>

                <p>
                Quanto mais segredos são revelados, mais fica claro
                que o conflito é maior do que uma simples disputa.
                O equilíbrio daquele mundo está ameaçado.
                </p>

                <p>
                A história mistura fantasia, romance, aventura
                e mistério, enquanto Raeve e Kaan tentam compreender
                as conexões entre seus passados.
                </p>

                <p>
                No final, fica evidente que a história dos dois
                está ligada a acontecimentos muito maiores do que
                eles imaginavam, e que o despertar da lua pode
                representar o início de uma grande transformação.
                </p>

            `
        },


        marques: {

            titulo: "Como Se Casar com um Marquês",

            autor: "Julia Quinn",

            capa:
            "https://m.media-amazon.com/images/I/81JZJvKq0DL._SL1500_.jpg",

            resumo: `

                <h3>Como Se Casar com um Marquês</h3>

                <p>
                Elizabeth Hotchkiss vive uma situação muito diferente
                da vida confortável que se poderia imaginar para uma
                jovem da sociedade inglesa.
                </p>

                <p>
                Depois da morte dos pais, ela precisa cuidar dos
                três irmãos mais novos e garantir que a família
                tenha um futuro seguro.
                </p>

                <p>
                Elizabeth percebe que não possui dinheiro suficiente
                para resolver todos os problemas da família.
                Por isso, começa a considerar a possibilidade
                de se casar com um homem rico.
                </p>

                <p>
                Elizabeth trabalha como dama de companhia de
                Lady Danbury. Certo dia, encontra na biblioteca
                um livro chamado “Como se Casar com um Marquês”.
                </p>

                <p>
                O livro apresenta estratégias para conquistar
                um marido adequado. Elizabeth decide utilizá-lo
                como um guia para conseguir encontrar alguém
                que possa ajudá-la a proteger sua família.
                </p>

                <p>
                É nesse momento que surge James Sidwell.
                James é o marquês de Riverdale, mas Elizabeth
                não sabe disso.
                </p>

                <p>
                James está investigando um problema envolvendo
                sua tia, Lady Danbury, e decide assumir uma
                identidade diferente para descobrir quem está
                por trás de uma chantagem.
                </p>

                <p>
                Elizabeth acaba chamando sua atenção.
                Ela é uma das pessoas próximas de Lady Danbury
                e poderia saber mais sobre o caso.
                </p>

                <p>
                James também descobre que Elizabeth está usando
                o livro sobre como conquistar um marquês.
                Ele decide ajudá-la a colocar as estratégias
                em prática.
                </p>

                <p>
                O problema é que, enquanto James tenta investigar
                a situação, Elizabeth começa a seguir cada vez mais
                as orientações do livro.
                </p>

                <p>
                Os dois passam muito tempo juntos e começam
                a desenvolver uma atração inesperada.
                </p>

                <p>
                Elizabeth continua acreditando que precisa fazer
                um casamento vantajoso para garantir o futuro
                dos irmãos.
                </p>

                <p>
                James, porém, começa a perceber que Elizabeth
                não está simplesmente procurando dinheiro.
                Ela é determinada, inteligente e extremamente
                dedicada à família.
                </p>

                <p>
                Ao mesmo tempo, James precisa continuar sua
                investigação sem revelar sua verdadeira identidade.
                </p>

                <p>
                A convivência entre os dois provoca situações
                divertidas e também faz com que Elizabeth perceba
                que seus sentimentos estão mudando.
                </p>

                <p>
                Aos poucos, o relacionamento que deveria ser
                apenas uma espécie de treinamento se transforma
                em algo muito mais verdadeiro.
                </p>

                <p>
                Quando Elizabeth descobre a verdadeira identidade
                de James, sente-se enganada e precisa decidir
                se ainda pode confiar nele.
                </p>

                <p>
                James também percebe que não consegue mais separar
                sua investigação dos sentimentos que desenvolveu
                por Elizabeth.
                </p>

                <p>
                Enquanto o mistério da chantagem continua,
                os dois precisam lidar com segredos, desconfianças
                e mal-entendidos.
                </p>

                <p>
                Elizabeth começa a entender que talvez não precise
                escolher um marido apenas pela riqueza.
                </p>

                <p>
                James pode oferecer segurança, mas também oferece
                algo que ela não esperava encontrar: amor,
                respeito e companheirismo.
                </p>

                <p>
                A história mistura romance, humor, investigação
                e situações da sociedade inglesa.
                </p>

                <p>
                No fim, Elizabeth percebe que o casamento que
                realmente deseja não é aquele baseado apenas
                em dinheiro.
                </p>

                <p>
                James também percebe que seu verdadeiro objetivo
                não é apenas investigar o problema de sua tia.
                Ele quer construir uma vida ao lado de Elizabeth.
                </p>

                <p>
                Assim, o manual que Elizabeth encontrou acaba
                tendo um resultado muito diferente do esperado:
                ela começa procurando aprender como conquistar
                um marquês e termina descobrindo que já havia
                conquistado o coração do próprio marquês.
                </p>

            `
        },


        hope: {

            titulo: "O Massacre da Família Hope",

            autor: "Riley Sager",

            capa:
            "https://m.media-amazon.com/images/I/81sJq9ZKpUL._SL1500_.jpg",

            resumo: `

                <h3>O Massacre da Família Hope</h3>

                <p>
                A história acompanha Kit McDeere, uma jovem que
                está passando por um momento difícil de sua vida.
                </p>

                <p>
                Ela recebe uma oportunidade de trabalho como
                cuidadora de uma família que vive em uma grande
                casa isolada chamada Hope's End.
                </p>

                <p>
                A propriedade possui uma história assustadora.
                Décadas antes, ocorreu um crime que ficou conhecido
                como o massacre da família Hope.
                </p>

                <p>
                Naquela noite, praticamente todos os membros da
                família foram encontrados mortos.
                </p>

                <p>
                A única sobrevivente foi Lenora Hope.
                </p>

                <p>
                Lenora era apenas uma criança quando o massacre
                aconteceu. Depois da tragédia, permaneceu vivendo
                em Hope's End.
                </p>

                <p>
                Anos mais tarde, ela está completamente dependente
                de cuidados. Não consegue andar e também não consegue
                falar.
                </p>

                <p>
                Ela se comunica escrevendo em uma máquina de escrever.
                </p>

                <p>
                Durante muitos anos, as pessoas acreditaram que
                Lenora havia sido responsável pela morte de sua
                própria família.
                </p>

                <p>
                Kit conhece essa história antes de começar a trabalhar
                na casa, mas logo percebe que existem muitas coisas
                que não fazem sentido.
                </p>

                <p>
                Lenora começa a escrever mensagens para Kit e afirma
                que deseja contar sua história.
                </p>

                <p>
                A partir desse momento, Kit começa a questionar
                a versão oficial do massacre.
                </p>

                <p>
                Lenora conta detalhes sobre a família e sobre os
                acontecimentos que aconteceram antes da tragédia.
                </p>

                <p>
                Kit descobre que os Hope eram uma família rica e
                respeitada por fora, mas escondiam muitos conflitos
                dentro de casa.
                </p>

                <p>
                Existiam segredos, ressentimentos e problemas
                familiares que poucas pessoas conheciam.
                </p>

                <p>
                Quanto mais Lenora conta, mais Kit percebe que
                talvez a história conhecida pelo público esteja
                incompleta.
                </p>

                <p>
                Kit começa então a investigar o passado.
                Ela procura informações sobre o massacre e tenta
                descobrir o que realmente aconteceu naquela noite.
                </p>

                <p>
                Porém, ela também começa a perceber que não pode
                confiar completamente em ninguém.
                </p>

                <p>
                A própria Lenora poderia estar contando a verdade,
                mas também poderia estar escondendo alguma coisa.
                </p>

                <p>
                A investigação fica ainda mais perigosa quando
                acontecimentos estranhos começam a acontecer
                dentro de Hope's End.
                </p>

                <p>
                Kit percebe que algumas pessoas não querem que
                o passado seja descoberto.
                </p>

                <p>
                Aos poucos, ela entende que descobrir quem matou
                a família Hope não é suficiente.
                É necessário entender tudo o que aconteceu
                antes do massacre.
                </p>

                <p>
                A história se transforma em um grande quebra-cabeça.
                Cada descoberta parece responder uma pergunta,
                mas também cria novos mistérios.
                </p>

                <p>
                Kit começa a questionar por que Lenora sobreviveu,
                por que foi considerada culpada e quais pessoas
                poderiam ter motivos para esconder a verdade.
                </p>

                <p>
                A relação entre Kit e Lenora também muda.
                No começo, Kit é apenas sua cuidadora.
                Depois, as duas passam a trabalhar juntas
                para tentar descobrir o passado.
                </p>

                <p>
                Kit percebe que Lenora passou décadas sendo julgada
                sem conseguir contar sua própria versão dos fatos.
                </p>

                <p>
                Ao mesmo tempo, Kit precisa enfrentar seus próprios
                problemas e perceber que sua chegada à casa não
                aconteceu por acaso.
                </p>

                <p>
                Conforme a investigação avança, diferentes versões
                dos acontecimentos começam a aparecer.
                </p>

                <p>
                Kit precisa separar fatos de histórias e descobrir
                quais pessoas estão dizendo a verdade.
                </p>

                <p>
                A narrativa mostra como uma tragédia pode continuar
                afetando a vida das pessoas mesmo décadas depois.
                </p>

                <p>
                Hope's End permanece marcada pelo massacre e
                Lenora continua sendo vista por muitos como uma
                assassina.
                </p>

                <p>
                Kit começa a entender que a verdade pode ser muito
                mais complicada do que a história contada durante
                todos aqueles anos.
                </p>

                <p>
                Quando finalmente consegue juntar as principais
                peças do quebra-cabeça, Kit percebe que o massacre
                estava ligado aos segredos da própria família Hope.
                </p>

                <p>
                As revelações mudam a maneira como ela enxergava
                Lenora e também mostram que várias pessoas tinham
                motivos para esconder determinadas informações.
                </p>

                <p>
                No fim, Kit consegue reconstruir acontecimentos
                importantes daquela noite e compreender melhor
                o que realmente aconteceu.
                </p>

                <p>
                O livro mostra que uma pessoa pode ser considerada
                culpada durante anos simplesmente porque a versão
                mais conhecida parece ser a mais fácil de acreditar.
                </p>

                <p>
                O Massacre da Família Hope mistura suspense,
                mistério e investigação, fazendo o leitor desconfiar
                constantemente dos personagens.
                </p>

                <p>
                Kit começa sua história como cuidadora, mas acaba
                se transformando em investigadora.
                </p>

                <p>
                Ao lado de Lenora, ela tenta descobrir a verdade
                sobre um crime que aconteceu muitos anos antes.
                </p>

                <p>
                A principal mensagem da história é que a verdade
                pode ser muito mais complicada do que aquilo que
                as pessoas escolheram acreditar.
                </p>

            `
        }

    };


    /* ========================= */
    /* CRONÔMETRO */
    /* ========================= */

    let tempoRestante = 600;

    let cronometro;


    function iniciarLeitura(livro) {

        document
            .getElementById("inicio")
            .classList
            .remove("ativa");

        document
            .getElementById("final")
            .classList
            .remove("ativa");

        document
            .getElementById("leitura")
            .classList
            .add("ativa");


        document
            .getElementById("tituloLivro")
            .innerText =
            livros[livro].titulo;


        document
            .getElementById("autorLivro")
            .innerText =
            livros[livro].autor;


        document
            .getElementById("capaLeitura")
            .src =
            livros[livro].capa;


        document
            .getElementById("resumo")
            .innerHTML =
            livros[livro].resumo;


        iniciarCronometro();

        window.scrollTo(0, 0);

    }


    function iniciarCronometro() {

        clearInterval(cronometro);

        tempoRestante = 600;

        atualizarTempo();


        cronometro = setInterval(function() {

            tempoRestante--;

            atualizarTempo();


            if (tempoRestante <= 0) {

                clearInterval(cronometro);

                finalizarLeitura();

            }

        }, 1000);

    }


    function atualizarTempo() {

        let minutos =
            Math.floor(tempoRestante / 60);

        let segundos =
            tempoRestante % 60;


        minutos =
            minutos
            .toString()
            .padStart(2, "0");


        segundos =
            segundos
            .toString()
            .padStart(2, "0");


        document
            .getElementById("tempo")
            .innerText =
            minutos + ":" + segundos;

    }


    /* ========================= */
    /* FINAL DA LEITURA */
    /* ========================= */

    function finalizarLeitura() {

        clearInterval(cronometro);


        document
            .getElementById("leitura")
            .classList
            .remove("ativa");


        document
            .getElementById("final")
            .classList
            .add("ativa");


        window.scrollTo(0, 0);

    }


    /* ========================= */
    /* VOLTAR AO INÍCIO */
    /* ========================= */

    function voltarInicio() {

        document
            .getElementById("final")
            .classList
            .remove("ativa");


        document
            .getElementById("inicio")
            .classList
            .add("ativa");


        window.scrollTo(0, 0);

    }

</script>

</body>
</html>
