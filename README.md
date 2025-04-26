# projeto_aplicado_iv
Sensoriamento remoto de avanço da seca em São Tomé das Letras

## Aquisição de Dados

[Projeto Aplicado IV Classes](https://github.com/rafavidal1709/projeto_aplicado_iv/blob/main/Projeto_Aplicado_IV_Classes.ipynb)
Esse notebook é uma exploração inicial de funcionalidade que serviram para iniciar a aquisição de dados do GEE.

[Carcara Clean Module](https://github.com/rafavidal1709/projeto_aplicado_iv/blob/main/Carcara_Clean_Module.ipynb)
Depois seguimos para passar a limpo as funções anteriores e modularizá-las para facilitar a importação. Nesse notebook estão as linhas de código que fazem a biblioteca Carcará disponível em carcara.asav.com.br.

[Carcará targz](https://github.com/rafavidal1709/projeto_aplicado_iv/blob/main/Carcara_targz.ipynb)
O mesmo que o Clean Module, mas desta vez já importamos todas as funções do site de um arquivo targz e inciamos como uma biblioteca. Veja como fazê-lo aqui. Tudas as funções usadas no projeto serão refinadas e incluídas neste arquivo para serem portáteis e incluídas de qualquer lugar de forma prática e rápida. A modularidade é uma qualidade essencial para desenvolvimento de grandes projetos.

**Anote**
_!pip install https://carcara.asav.com.br/package/Carcara.tar.gz_

## Limpeza

[Carcara DataCleaner](https://github.com/rafavidal1709/projeto_aplicado_iv/blob/main/Carcara_DataCleaner.ipynb)
Esse algorítimo usa a camada SCL para criar uma classificação de confiança sobre os pixeis e susbtituir os não-confiáveis pela média ponderada do anterior com o posterior na linha do tempo e que ocupa a mesma posição X e Y na iimagem. No caso, levou quatro dias para executar até estorar a cota de acesso do GoogleDrive. O refino da classificação de confiança com uma CNN especializada vai diminuir esse gargalo e reduzir o disperdício pelos pixeis mal classificados que ficam meses esperando um pixel confiável como as pedreiras que se confundem com nuvens.

## Visualização e Predição SARIMA

[PAIV Visualização e Predição com SARIMA](https://github.com/rafavidal1709/projeto_aplicado_iv/blob/main/PAIV_Visualiza%C3%A7%C3%A3o_e_Predi%C3%A7%C3%A3o_com_SARIMA.ipynb)
Após a limpeza visualizamos os dados distribuídos no tempo, para isso transformamos as imagens em dois valores escalares, as médias do canal vermelho e do vapor de água. Após criar o gráfico utilizamos o SARIMA para prever a série temporal com sazonalidade.
