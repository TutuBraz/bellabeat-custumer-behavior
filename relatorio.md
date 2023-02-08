# RELATÓRIO

## Definição do problema:
O projeto tem como objetivo identificar o comportamento de cliente que utilizam dispositivos inteligentes que não são Bellabeat, e posteriormente selecionar um dos produtos da empresa par aplicar os insights.

**Peguntas norte:**

1. Quais são algumas da tendêndias no uso de dispositivos inteligentes.
2. Como essas tendências podem se aplicar aos clientes da Bellabeat.
3. Como essas tendências podem ajudar a influenciar a estratégia de marketing da Bellabeat?
4. Quais são os horários de maior intensidade de exercicios, existe uma rotina?
5. Como os usuários dormem?


**Tarefa de negócios:** Comos usuários utilizam dispositivos inteligentes?.



## Preparar.

O conjunto de dados foi obtido através do Kaggle e contém um rastreador de condicionamento físico pessoal de trinta usuários do Fitbit, uma empresa estadunidense de eletrônicos e fitness. Trinta usuários elegíveis do Fitbit consentiram com o envio de dados pessoais do rastreador, incluindo os resultados a cada minuto de atividade física, frequência cardíaca e monitoramento do sono. São abrangidas informações sobre atividades diárias, passos e frequência cardíaca que podem ser usadas para explorar os hábitos dos usuários.

Os data frames utilizados são:
* daily_activity
* daily_intensities
* sleep_day
* minute_narrow_METs

As únicas tabelas que estão no formato longo são:
* daily_intensities
* daily_activity

**Integridade:** Verificar se os dados estão completos, duplicados e faltando. Para verificação criei uma função que verifica a quantidade de usúario, a quantidade de dados duplicados e a quantidade de dados faltantes. Quaisquer alterações serão feitas manualmente. 
 	A tabela sleep_day possui 24 usúarios, como ela é vital para análise e possui uma quantidade relativamente próximado total não irei descarta-la.

## Processar.

 Existem valores duplicados na tabela sleep_day, estes valores serão excluidos. Também irei criar uma coluna 'day', nos datasets daily_intensities e daily_acivity, para informar nominalmente qual dia da semana as informações foram registrada registadas. Já nos datasets sleep_day e minute_narrow_METs irei criar três colunas, data, dia_semana e horas, E contrapartida irei retirar a coluna que marca essas informações no data frames. Em todos os datasets serão retiradas as colunas Id.

## Analisar:

**Sobre a rotina de sono:** 
	
A Fundação Nacionla do Sono dos Estados Unidos, indica que o sono médio da na faixa etária de 18 a 64 ano deve estar entre 420  minutos a 540 minutos. Os usuários analisados apresentaram uma média de 419,17 minutos dormidos e uma mediana de 432,5 minutos dormidos, o que signica que em média e mediana os usuários estão preenchendo o minimo necessário de horas de sono por dia. Domingo e sábado são respectivamente os dias em que os participantes mais dormem.
	
Percebe-se uma redução drástica de minutos de sono de domingo para segunda, essa redução vai até terça. Na quarta acontece um aumento relativamente pequeno de minutos dormidos em comparação ao dia anterior, porém continua reduzindo até sexta-feria quando no sábado existe um aumento repentino de minutos dormidos. 
	
Vale ressaltar que os participantes ficam em mediana 25,5 minutos por dia acordados na cama (foi utilizada a mediana, pois existem muito outliers nesta feature), sendo que, domingo é o dia em que os participantes mais ficam na cama.  