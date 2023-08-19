# Animacao-CSS

### CSS Animation:  

* https://animista.net/ *

A propriedade CSS `transform` é usada para aplicar transformações a elementos HTML, permitindo alterar sua posição, rotação, escala e outros aspectos visuais. O valor `translateX` é uma função de transformação que permite mover um elemento ao longo do eixo horizontal (eixo X) da página.

Aqui está um exemplo de como usar `transform: translateX`:

```css
.elemento {
  transform: translateX(50px); /* Move o elemento 50 pixels para a direita */
}
```

No exemplo acima, o elemento com a classe `.elemento` será movido 50 pixels para a direita ao longo do eixo X. Você pode ajustar o valor numérico positivo ou negativo para controlar a quantidade e direção do movimento.

Essa propriedade é útil para criar animações e efeitos de transição, permitindo que você mova elementos de forma dinâmica em resposta a interações do usuário ou outras ações. Além do `translateX`, existem outras funções de transformação disponíveis, como `translateY` para mover ao longo do eixo Y, `scale` para dimensionar o elemento e `rotate` para girá-lo, entre outras.


`@keyframes` é uma regra do CSS que permite criar animações definindo um conjunto de etapas (keyframes) para controlar as mudanças de estilo de um elemento ao longo do tempo. Com essa regra, é possível criar animações complexas e suaves, especificando diferentes estados intermediários entre o início e o fim da animação.

Aqui está um exemplo de como usar `@keyframes` para criar uma animação que faz um elemento se mover suavemente de um lado para o outro:

```css
@keyframes mover {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(100px);
  }
  100% {
    transform: translateX(0);
  }
}

.elemento {
  animation: mover 2s infinite; /* Aplica a animação "mover" durante 2 segundos em um loop infinito */
}
```

Neste exemplo, a animação `mover` possui três etapas (0%, 50% e 100%) que definem a posição horizontal do elemento usando a propriedade `transform: translateX`. A classe `.elemento` aplica essa animação, fazendo com que o elemento se mova de um lado para o outro repetidamente.

Você pode usar o `@keyframes` para criar uma variedade de animações, definindo diferentes estados em diferentes porcentagens da duração total da animação. A combinação de `@keyframes` com outras propriedades de animação, como `animation-duration`, `animation-timing-function` e `animation-delay`, permite criar efeitos visuais interessantes e interativos em suas páginas web.

A propriedade CSS `animation-fill-mode` é usada para controlar como um elemento deve ser estilizado antes e depois de uma animação ser executada. Ela possui diferentes valores que determinam como o elemento se comportará no início e no final da animação.

Os valores possíveis para `animation-fill-mode` são:

1. `none`: O valor padrão. O elemento não mantém nenhum estado da animação após sua conclusão.
2. `forwards`: O elemento mantém o estado final da animação após sua conclusão.
3. `backwards`: O elemento mantém o estado inicial da animação antes dela ser executada.
4. `both`: O elemento mantém tanto o estado inicial quanto o estado final da animação.

Aqui está um exemplo de uso da propriedade `animation-fill-mode`:

```css
@keyframes move {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(100px);
  }
}

.elemento {
  animation: move 2s forwards;
  animation-fill-mode: forwards;
}
```

A propriedade CSS `animation-direction` é usada para controlar a direção de reprodução de uma animação definida usando a regra `@keyframes`. Ela determina se a animação deve ser reproduzida normalmente, de trás para frente ou em um loop alternado.

Os valores possíveis para `animation-direction` são:

1. `normal`: A animação é reproduzida normalmente, ou seja, do início para o fim.
2. `reverse`: A animação é reproduzida de trás para frente, ou seja, do fim para o início.
3. `alternate`: A animação é reproduzida alternadamente entre normal e reverso em cada ciclo.
4. `alternate-reverse`: A animação é reproduzida alternadamente entre reverso e normal em cada ciclo.

Aqui está um exemplo de uso da propriedade `animation-direction`:

```css
@keyframes slide {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(100px);
  }
}

.elemento {
  animation: slide 2s alternate infinite;
  animation-direction: alternate;
}
```

No exemplo acima, a classe `.elemento` será animada usando a animação `slide`. A propriedade `animation-direction: alternate;` foi definida, o que fará com que a animação alterne entre normal e reverso em cada ciclo, criando um efeito de ida e volta.

A propriedade `animation-direction` é útil para criar animações mais dinâmicas e variadas, permitindo controlar a direção em que os elementos se movem ao longo da animação.

No exemplo acima, a classe `.elemento` será animada usando a animação `move`. Além disso, `animation-fill-mode: forwards;` foi especificado, o que faz com que o elemento mantenha o estado final da animação após sua conclusão.

A propriedade `animation-fill-mode` é útil para controlar como os elementos se comportam antes e depois das animações, permitindo criar efeitos visuais mais interessantes e previsíveis.

A propriedade CSS `animation-iteration-count` é usada para controlar o número de vezes que uma animação definida por `@keyframes` será repetida. Ela determina quantas vezes a animação será executada antes de parar.

Os valores possíveis para `animation-iteration-count` podem ser:

1. Um valor numérico: Especifica quantas vezes a animação deve ser repetida. Por exemplo, `animation-iteration-count: 3;` fará com que a animação seja executada três vezes.
2. `infinite`: Faz com que a animação seja executada infinitamente, ou seja, ela continuará se repetindo indefinidamente.

Aqui está um exemplo de uso da propriedade `animation-iteration-count`:

```css
@keyframes fade {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

.elemento {
  animation: fade 2s infinite;
  animation-iteration-count: 3;
}
```

No exemplo acima, a classe `.elemento` será animada usando a animação `fade`. A animação terá uma duração de 2 segundos e será repetida três vezes, de acordo com `animation-iteration-count: 3;`.

A propriedade `animation-iteration-count` é útil para controlar o número de vezes que uma animação é repetida, permitindo criar efeitos de animação precisos e controlados.

A propriedade CSS `animation-timing-function` também suporta o valor `steps`, que é usado em conjunto com animações baseadas em etapas (steps) para criar transições com comportamento discreto, onde cada etapa da animação é exibida instantaneamente.

O valor `steps` requer dois argumentos: o primeiro é o número de etapas na animação, e o segundo é o tipo de ação que ocorre nas transições entre as etapas. Por exemplo:

```css
@keyframes step-animation {
  0%, 100% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(100px);
  }
}

.elemento {
  animation: step-animation 2s steps(2, start);
  animation-timing-function: steps(2, start);
}
```

No exemplo acima, a classe `.elemento` será animada usando a animação `step-animation`, que possui três etapas definidas. O valor `steps(2, start)` na propriedade `animation-timing-function` faz com que a animação ocorra em duas etapas com transições instantâneas no início de cada etapa.

Essa abordagem é útil para criar animações com comportamento mais discreto, como a exibição de frames individuais de uma animação de sprites ou outros efeitos que requerem transições instantâneas entre estados discretos.

A função `cubic-bezier` é uma das formas de especificar uma curva de velocidade personalizada para animações em CSS. Ela permite criar transições mais complexas, ajustando a aceleração e desaceleração ao longo do tempo.

A função `cubic-bezier` recebe quatro valores como argumentos, cada um representando as coordenadas x e y de dois pontos de controle que definem a curva de velocidade. Esses valores devem estar dentro do intervalo [0, 1], onde (0,0) é o ponto inicial da curva (tempo, progresso) e (1,1) é o ponto final (tempo, progresso).

Aqui está um exemplo de uso da função `cubic-bezier`:

```css
@keyframes custom-animation {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(100px);
  }
}

.elemento {
  animation: custom-animation 2s cubic-bezier(0.25, 0.1, 0.25, 1);
}
```

Neste exemplo, a classe `.elemento` será animada usando a animação `custom-animation` com uma duração de 2 segundos e a curva de velocidade definida pela função `cubic-bezier(0.25, 0.1, 0.25, 1)`. Esses valores personalizados controlam como a velocidade da animação varia ao longo do tempo, resultando em uma sensação de movimento única.

Você pode usar ferramentas online ou gráficos de curvas de Bezier para visualizar e ajustar os valores da função `cubic-bezier` de acordo com as suas necessidades, criando efeitos de animação mais precisos e agradáveis.

A propriedade CSS `animation-play-state` é utilizada para controlar o estado de reprodução de uma animação definida através da regra `@keyframes`. Ela permite pausar ou retomar a execução de uma animação em um determinado elemento.

Os valores possíveis para a propriedade `animation-play-state` são:

- `running`: A animação está em execução (valor padrão).
- `paused`: A animação está pausada.

Aqui está um exemplo de como usar a propriedade `animation-play-state`:

```css
@keyframes slide-animation {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(100px);
  }
}

.elemento {
  animation: slide-animation 2s linear infinite;
}

.paused {
  animation-play-state: paused;
}
```

No exemplo acima, a classe `.elemento` possui uma animação contínua de deslizamento usando a animação `slide-animation`. Ao adicionar a classe `.paused` a esse elemento, a animação será pausada, mantendo o elemento em sua posição atual até que o estado seja alterado novamente.

Isso é especialmente útil quando você deseja controlar a reprodução de animações com base em eventos, interações do usuário ou outras condições dinâmicas.