# Wiki — Iluminação da Cena

## Visão geral

A cena utiliza diferentes tipos de iluminação do Unity para criar efeitos distintos no ambiente nevado, nas casas, nas árvores, no boneco de neve e na área interna da caverna.

Foram utilizadas cinco configurações principais:

1. **Directional Light**
2. **Spot Light vermelha**
3. **Point Light azul**
4. **Spot Light amarela/quente**
5. **Directional Light com temperatura de cor e sombras suaves**

---

## 1. `01 - directional light.png`

### Tipo: Directional Light

![Configurações da Directional Light](imagens/01_configuracoes.png)

A **Directional Light** funciona como uma fonte de luz muito distante, semelhante ao Sol. Sua posição não determina a direção dos raios; a **rotação** é o principal fator que define como a luz incide na cena.

### Configurações

- **Posição:** X = 0, Y = 3, Z = 0
- **Rotação:** X = -20,6°, Y = -30°, Z = 0°
- **Escala:** X = 1, Y = 1, Z = 1

![Resultado da Directional Light](imagens/01_directional_light.png)

### Alteração na cena

Essa luz fornece uma **iluminação geral do ambiente externo**, atingindo uma grande parte da cena de forma uniforme.

A rotação determina a direção da iluminação e, consequentemente, a direção das sombras projetadas pelos objetos.

---

## 2. `2- spot light.png`

### Tipo: Spot Light

![Configurações da Spot Light vermelha](imagens/02_configuracoes.png)

A **Spot Light** emite luz em uma direção específica, formando um cone de iluminação, semelhante a um holofote.

### Configurações

- **Modo:** Realtime
- **Cor:** Vermelha
- **Intensidade:** 1140,3
- **Indirect Multiplier:** 47,1
- **Range:** 21,56
- **Inner Spot Angle:** 30°
- **Shadow Type:** No Shadows

![Resultado da Spot Light vermelha](imagens/02_spot_light.png)

### Alteração na cena

Essa configuração adiciona uma **iluminação vermelha direcionada** à região para a qual a Spot Light está apontada.

O efeito vermelho é percebido principalmente no **boneco de neve e nas árvores próximas**, criando um destaque visual.

Como o **Shadow Type** está configurado como **No Shadows**, a luz não produz sombras próprias, sendo utilizada principalmente para adicionar o efeito de cor e iluminação localizada.

---

## 3. `3 - point light_.png`

### Tipo: Point Light

![Configurações da Point Light azul](imagens/03_configuracoes.png)

A **Point Light** funciona como uma fonte de luz localizada em um único ponto. Diferentemente da Spot Light, ela emite luz **em todas as direções**.

### Configurações

- **Modo:** Realtime
- **Cor:** Azul
- **Intensidade:** 121,19
- **Range:** aproximadamente 2,73
- **Shadow Type:** No Shadows

![Resultado da Point Light azul](imagens/03_point_light.png)

### Alteração na cena

Essa luz adiciona uma **iluminação azul localizada**.

Como o **Range** é pequeno, sua influência fica concentrada nas proximidades da fonte. O efeito é utilizado principalmente na área da **caverna**, contribuindo para a atmosfera fria e azulada.

A ausência de sombras faz com que a Point Light funcione principalmente como uma fonte de iluminação colorida.

---

## 4. `04 - spot light 2.png`

### Tipo: Spot Light

![Configurações da Spot Light amarela](imagens/04_configuracoes.png)

Essa segunda Spot Light possui uma função diferente da iluminação vermelha. Ela foi utilizada para criar uma iluminação **quente e localizada**, principalmente na área interna da construção.

### Configurações

- **Modo:** Baked
- **Cor:** Amarela/quente
- **Intensidade:** 1039
- **Indirect Multiplier:** 17
- **Range:** 30,3
- **Inner Spot Angle:** aproximadamente 21,8°
- **Outer Spot Angle:** 30°
- **Shadow Type:** Soft Shadows
- **Shape Radius:** 0,025

![Resultado da Spot Light amarela](imagens/04_spot_light.png)

### Alteração na cena

Essa iluminação cria o efeito de **luz quente proveniente da janela/interior da construção**.

A tonalidade amarelada contrasta com a iluminação fria do ambiente externo, deixando o interior visualmente mais aconchegante.

Diferentemente da Spot Light vermelha, esta utiliza **Soft Shadows**, produzindo sombras com bordas mais suaves.

O modo **Baked** permite que a contribuição dessa iluminação seja pré-calculada pelo sistema de iluminação do Unity.

---

## 5. `05 - directional light 2.png`

### Tipo: Directional Light

![Configurações da segunda Directional Light](imagens/05_configuracoes.png)

Essa segunda Directional Light foi configurada para fornecer uma iluminação geral diferente da primeira, utilizando **temperatura de cor** e **sombras suaves**.

### Configurações

- **Modo:** Realtime
- **Rotação:** X = 30°, Y = -30°, Z = 0°
- **Temperatura:** 5000 K
- **Intensidade:** 2
- **Indirect Multiplier:** 1
- **Shadow Type:** Soft Shadows
- **Shadow Strength:** 1
- **Soft Shadow Quality:** Low

![Resultado da segunda Directional Light](imagens/05_directional_light.png)

### Alteração na cena

A mudança na **rotação** altera a direção dos raios luminosos e, portanto, a posição das sombras.

A temperatura de **5000 K** produz uma iluminação próxima do branco, com aparência relativamente neutra/fria.

A utilização de **Soft Shadows** faz com que as bordas das sombras sejam mais suaves, contribuindo para uma aparência mais natural na iluminação das casas, árvores e demais objetos.

---

# Comparação

| Arquivo | Tipo | Cor | Modo | Sombras | Função principal |
|---|---|---|---|---|---|
| `01 - directional light.png` | Directional | Branca | — | — | Iluminação geral externa |
| `2- spot light.png` | Spot | Vermelha | Realtime | Sem sombras | Efeito vermelho localizado |
| `3 - point light_.png` | Point | Azul | Realtime | Sem sombras | Iluminação azul localizada |
| `04 - spot light 2.png` | Spot | Amarela/quente | Baked | Soft Shadows | Iluminação quente interna |
| `05 - directional light 2.png` | Directional | 5000 K | Realtime | Soft Shadows | Iluminação geral com sombras suaves |

---

# Diferenças entre os tipos de luz

## Directional Light

Representa uma fonte de luz muito distante, como o Sol.

- Ilumina a cena de maneira ampla.
- A posição da luz não influencia a direção dos raios.
- A rotação determina a direção da iluminação.
- É adequada para iluminação geral.

## Spot Light

Produz um feixe de luz direcionado.

- Possui formato de cone.
- A direção depende da rotação.
- **Inner Spot Angle** e **Outer Spot Angle** controlam a abertura.
- **Range** determina a distância máxima da iluminação.
- É adequada para holofotes, lanternas e efeitos localizados.

## Point Light

Emite luz a partir de um ponto em todas as direções.

- Iluminação radial.
- A intensidade diminui com a distância.
- **Range** limita a área afetada.
- É adequada para lâmpadas e fontes luminosas pequenas.

---

# Conclusão

As diferentes configurações foram utilizadas para criar **contraste de cor, profundidade e atmosfera** na cena.

A **Directional Light** fornece a iluminação geral, enquanto as **Spot Lights** permitem destacar regiões específicas. A **Point Light** cria uma fonte localizada que ilumina em todas as direções.

As cores também possuem funções diferentes: a iluminação **azul** reforça a sensação de frio, a iluminação **vermelha** cria um destaque visual e a iluminação **amarela** produz uma sensação de calor e aconchego no interior.

Por fim, o uso de **Soft Shadows** e de iluminação **Baked** em determinadas configurações permite controlar melhor a aparência das sombras e o custo de processamento da cena.
