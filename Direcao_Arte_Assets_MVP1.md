# 🎨 Direção de Arte & Assets — MVP1
### Guia visual + lista de assets + prompts prontos pra IA
*Companheiro do GDD_MVP1 · versão 1.0*

---

## 1. Pilares visuais (as 4 regras de ouro)

1. **2D estilizado, NÃO realista.** Shapes limpos, cores chapadas, contornos definidos. Nada de reflexo/sombra em tempo real. Bonito por *design*, não por poder gráfico.
2. **Leitura acima de tudo.** Num celular, o jogador precisa ler pista, curva, rampa e ghost em milissegundos. Alto contraste entre "pista" e "fora da pista".
3. **Leve = roda em qualquer celular.** Sprites/vetor, sem 3D. Essa é a premissa inegociável do MVP.
4. **Identidade synthwave + arcade retrô-indie.** Neon por cima de um bioma estilizado. Atitude sem custo.

## 2. Perspectiva e câmera

- **Top-down com inclinação de ~35-40°** (não é vista de cima 100% chapada, não é lateral).
- A estrada "foge" levemente pro fundo → sensação de velocidade.
- Todos os sprites (carro, peças de pista) devem ser desenhados **nesse mesmo ângulo** pra encaixar.

## 3. Paleta de cores (neon oasis)

| Uso | Cor | Referência |
|---|---|---|
| Base/fundo (noite) | Azul-marinho profundo → roxo | `#0d0b2b` → `#2a1a4a` |
| Neon primário | Ciano | `#1fd6ff` |
| Neon secundário | Magenta/rosa | `#ff2fb9` |
| Neon acento | Roxo | `#8b3dff` |
| Pista (asfalto) | Cinza-escuro azulado | `#3a3550` |
| Faixa central | Amarelo/laranja | `#ffae2b` |
| Nitro/chama | Laranja → amarelo | `#ff7a1a` → `#ffd23f` |
| Vegetação | Verde estilizado | `#2fbf71` |

## 4. Estilo do carro

- **Formato "chunky" arcade** — carro robusto, rodas grandes, cara de brinquedo caprichado.
- **Carro base ("carro-lata"):** visual **simples e cru**, cores neutras (cinza/bege desbotado), sem enfeites. Deve dar vontade de evoluir.
- **Chassis compráveis (MVP2):** mais estilo, cores vivas.
- **Ghost:** mesmo sprite, **semitransparente** com contorno neon ciano.

## 5. Lista de assets do MVP1

1. Carro base — sprite PNG transparente, vista top-down inclinada.
2. Carro ghost — derivado do carro, ~40% opacidade, contorno ciano.
3. Chama de nitro — sprite laranja-amarelo.
4. Peça: reta — asfalto com faixa central e bordas neon.
5. Peça: curva — curva suave + fechada.
6. Peça: rampa/pulo — rampa com seta ciano.
7. Peça: barreira — mureta neon.
8. Cenário do bioma — fundo neon oasis: palmeiras, rochas, cachoeira, placas neon.
9. UI: galões de nitro — 3 galões, estados cheio/vazio.
10. UI: botões de controle — esquerda, direita e NITRO.
11. UI: moldura de minimapa — círculo/traçado simples.

## 6. Brief visual

O norte visual do MVP é **2D estilizado, flat/vetor, synthwave + arcade retrô-indie**, com pista legível, cenário neon oasis e câmera top-down inclinada em ~35°.

## 7. Brief do jogo

Crie um jogo de corrida arcade 2D top-down para navegador/mobile.

**CÂMERA:** top-down com leve inclinação (~35°), seguindo o carro, com leve zoom ao acelerar para dar sensação de velocidade.

**CONTROLE:** o carro acelera sozinho em velocidade constante. Toque na metade esquerda da tela = vira à esquerda; metade direita = vira à direita. Virar faz o carro derrapar levemente e isso já desacelera (não há freio). Um botão NITRO no canto inferior direito: segurar descarrega o nitro progressivamente.

**NITRO:** 3 galões. Cada um recarrega com o tempo. Há um teto de potência.

**PISTA:** 1 circuito fechado em formato de "8" com uma sobreposição onde a pista cruza por cima dela mesma via uma RAMPA. Ao passar na rampa o carro pula automaticamente; se chegar sem velocidade suficiente, cai fora e faz respawn num ponto anterior com espaço para readquirir velocidade. A pista tem uma reta longa, uma curva suave e uma curva fechada. Barreiras delimitam a pista.

**CORRIDA:** 3 voltas, cronômetro, guarda o melhor tempo do jogador. Um carro GHOST semitransparente corre reproduzindo um tempo-alvo (gerado a partir do melhor tempo do jogador +/- 2%). Mostrar uma seta/indicador de distância para o ghost.

**ESTILO:** 2D estilizado, flat/vetor, cores chapadas, NÃO realista, leve. Bioma "neon oasis" à noite, estética synthwave (ciano, magenta, roxo, laranja no nitro). HUD enxuto: voltas, melhor tempo, seu tempo, 3 galões de nitro, minimapa.

**OBJETIVO:** sensação de dirigir divertida e "pega e joga". Foco no game feel.
