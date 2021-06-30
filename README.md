# tratando-dados-regex-python
Breve solução usando Regex com Python + Pandas
## Expressões Regulares com Python

No mês de novembro de 2019, a comunidade Data Hackers fez uma pesquisa sobre o mercado de Data Science no Brasil.

E quero tratar de uma das coluna que me chamou a atenção.

A coluna (P16) retorna esses valores

![image](https://user-images.githubusercontent.com/68204206/123883811-1cc84580-d920-11eb-8257-6e945aaa9b0e.png)

Fui abordado com a seguinte pergunta : Qual a faixa salarial por idade ?

Para responder essa pergunta fui analisar o dataset e separar apenas as colunas de interesse e até adicionei a coluna que da situação de contrato (CLT, Freelancer, Empreendedor, etc).

![image](https://user-images.githubusercontent.com/68204206/123883835-2e115200-d920-11eb-97a9-032511c489c7.png)

Ao bater o olho no dataset, me pergunto: E agora, como tratar os dados da coluna salário para criar um gráfico ? 

Então é nesse momento que lhe apresento o módulo re + a função findall() que já está incluída dentro do Python. Com essa linguagem é possível especificar regras no nosso caso utilizaremos a coluna "salario" para pegar apenas os números e continuar a solução.

Como a função findall() vai criar uma lista com os valores encontrados, pensei em criar uma coluna com o salário médio. Faz sentido para você ?

Documentação disponível em: [https://docs.python.org/pt-br/3.8/howto/regex.html](https://docs.python.org/pt-br/3.8/howto/regex.html)

### Tratando dados

A lógica que pensei para resolver o problema foi a seguinte :

![image](https://user-images.githubusercontent.com/68204206/123884012-92ccac80-d920-11eb-911d-558a5bcb1b3e.png)

Pensando assim, desenvolvi o seguinte código

![image](https://user-images.githubusercontent.com/68204206/123883870-44b7a900-d920-11eb-81dc-42b33a69b874.png)

Repare que no final, adicionei uma outra verificação e o motivo dessa verificação é que os salários entre 2.001 á 3.000, está com um pequeno erro ou simplesmente faltando um ponto ( . ), sendo assim, acabava adicionando outliers indesejadas para o dataset e isso foi percebido ao imprimir um histograma, veja só o resultado antes da solução :


![image](https://user-images.githubusercontent.com/68204206/123883898-5600b580-d920-11eb-868a-1f0ba705d615.png)

Agora veja o resultado, depois da solução :

![image](https://user-images.githubusercontent.com/68204206/123883907-5ac56980-d920-11eb-96bf-3e2fe38e9911.png)
Bem melhor, concorda ou não ? 

Já estamos perto de finalizar, vamos só verificar como ficou o dataset depois do código implementado : 

![image](https://user-images.githubusercontent.com/68204206/123883912-62850e00-d920-11eb-9512-c11ba0f38a28.png)
Agora sim, senti confiança em plotar um gráfico e decidi que fosse um gráfico de barras, o resultado final foi o seguinte :

![image](https://user-images.githubusercontent.com/68204206/123883922-66189500-d920-11eb-9d6e-c93de7c21daf.png)


Finalizamos essa breve solução, com um gráfico bem bonito :) 
Estarei disponibilizando este notebook no meu github, assim como este material.

Fique a vontade para comentar e colocar perguntas, críticas positivas e elogios também são bem vindos, o meu foco é evoluir e poder agregar valor a quem precisa.

Me siga nas redes sociais e saiba que gostaria muito de ter você como conexão no LinkedIn.

Forte abraço!

dataset : [https://www.kaggle.com/datahackers/pesquisa-data-hackers-2019](https://www.kaggle.com/datahackers/pesquisa-data-hackers-2019)

Instagram : [https://www.instagram.com/andrade_rafa93/](https://www.instagram.com/andrade_rafa93/)

LinkedIn : [https://www.linkedin.com/in/andraderafa/](https://www.linkedin.com/in/andraderafa/)
