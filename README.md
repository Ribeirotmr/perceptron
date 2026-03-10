## O que é o Perceptron?

O Perceptron é a unidade fundamental das redes neurais. Ele é um classificador linear que aprende a separar duas classes através de um ajuste iterativo de pesos.

###  O Passo a Passo do Algoritmo

O funcionamento do código que desenvolvemos segue estes 4 estágios:

1. **Inicialização**:
   - Definimos os pesos ($w$) e o bias ($b$) inicialmente como zero.
   - Escolhemos um número de iterações (épocas).

2. **Soma Ponderada**:
   Para cada amostra de entrada $x$, calculamos o potencial de ativação $u$:
   $$u = \sum_{i=1}^{n} w_i x_i + b$$

3. **Função de Ativação (Degrau)**:
   O modelo decide a classe baseada no sinal de $u$:
   - Se $u \geq 0$, a previsão é **+1**.
   - Se $u < 0$, a previsão é **-1**.

4. **Regra de Atualização (Aprendizado)**:
   Se o modelo errar a classe ($y_{predito} \neq y_{real}$), ajustamos os pesos para corrigir o erro:
   $$w_{novo} = w_{antigo} + y_{real} \cdot x$$
   $$b_{novo} = b_{antigo} + y_{real}$$

---

###  Por que a acurácia não foi 100%?

No experimento realizado, obtivemos **85.71%** de acurácia. 

Isso ocorre porque o Perceptron clássico possui uma limitação teórica: ele **só converge para 100% se os dados forem Linearmente Separáveis**. Como nossos dados possuem pontos "misturados" no espaço, o algoritmo encontra a melhor linha reta possível, mas não consegue contornar os pontos sobrepostos.

