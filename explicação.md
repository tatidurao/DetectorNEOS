Explicação do Cálculo para a Palestra (Roteiro)
Você pode conduzir sua explicação ao vivo dividindo aquele bloco de código em 4 passos lógicos. Como vamos focar em uma linguagem acessível e atraente, aqui está como você pode explicar cada linha:

1. O "Catadão" de Dados (Juntando os objetos)

O que o código faz: let meteor_arr = Object.keys... e concat.apply...
Como explicar: "Quando a NASA nos envia os dados, ela manda os asteroides (NEOs) organizados em 'caixinhas' separadas por dias da semana. Mas para descobrir qual é o mais perigoso no geral, nós não podemos olhar uma caixa por vez. O que essas duas primeiras linhas fazem é virar todas as caixinhas no chão e criar uma única grande lista com todos os asteroides que estão passeando perto da Terra neste momento."

2. Descobrindo o Tamanho (A Média)

O que o código faz: let diameter = (min + max) / 2
Como explicar: "No espaço, é muito difícil medir um objeto com precisão milimétrica. Por isso, a NASA nos dá uma estimativa: 'Esse asteroide tem entre 100 e 200 metros'. O que nós fazemos aqui é matemática básica: somamos o mínimo e o máximo e dividimos por dois para encontrar o tamanho médio. É o nosso melhor palpite para o tamanho real do objeto."

3. O Nível de Alerta (O "Threat Score")

O que o código faz: let threatScore = (diameter / miss_distance) * 1000000000
Como explicar: "Aqui está a mágica do nosso radar! Como saber se um asteroide é perigoso? Pense assim: um caminhão a 10 km de distância assusta menos do que uma bicicleta vindo na sua direção a 1 metro de distância. O perigo depende do tamanho e da distância.
Nós dividimos o tamanho do asteroide pela distância que ele está da Terra. Quanto maior o asteroide e menor a distância, maior o resultado. Como essas distâncias espaciais são gigantescas, a divisão gera um número minúsculo (como 0.000005). Para não mostrar isso na tela, nós multiplicamos por 1 bilhão! É como colocar uma lupa matemática para que o 'Nível de Alerta' vire um número fácil da gente ler (tipo 20, 50, 80)."

4. O Top 5 dos NEOs (O Pódio)

O que o código faz: meteors.sort(...) e meteors.slice(0,5)
Como explicar: "Por fim, pegamos essa nota de alerta que criamos e pedimos para o computador organizar a lista do maior perigo para o menor (sort). Como não queremos poluir a tela com milhares de pedregulhos espaciais inofensivos, passamos uma faca na lista (slice) e pegamos apenas os 5 primeiros. São esses os 5 NEOs que merecem a nossa atenção hoje!"