<div align="center">

# 🏹 Arcadia Defense

**Jogo de ação e tower defense 2D desenvolvido em Unity**

Defenda Arcádia posicionando torres ao longo do caminho, encare ondas crescentes de inimigos e enfrente o boss final.

<img src="https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white" />
<img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white" />
<img src="https://img.shields.io/badge/Plataforma-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white" />

**[⬇️ Baixar e jogar](../../releases/latest)**

</div>

---

## Sobre o projeto

Primeiro jogo completo que desenvolvi, criado como trabalho avaliativo da faculdade. A proposta era simples — entregar um jogo que atendesse a requisitos básicos — mas acabamos indo bem além do escopo pedido: o resultado tem **3 níveis, cutscene de abertura, sistema de progressão, inventário com equipamentos, loja e um boss com IA própria**.

Foi onde aprendi que a parte difícil de um jogo não é fazer o personagem andar. É fazer dez sistemas independentes conversarem entre si sem quebrar.

<br>

## O que tem dentro

| Sistema | Descrição |
|---|---|
| ⚔️ **Combate** | Player com movimentação, vida e ataque; inimigos corpo a corpo e à distância |
| 🗼 **Torres** | Posicionamento por blueprint, mira automática e projéteis aliados |
| 🌊 **Ondas** | Spawner progressivo com barra de progresso da onda atual |
| 👹 **Boss** | Máquina de estados própria: segue rota → detecta o player → persegue → ataca |
| 🎒 **Inventário** | Itens, consumíveis e equipamentos via `ScriptableObject`, com drop e coleta |
| 🏪 **Loja** | Compra de melhorias com moeda acumulada durante as partidas |
| 📈 **Progressão** | Sistema de vidas, progressão do jogador e loot escalonado por nível |
| 🎬 **Apresentação** | Cutscene inicial, menu principal, menu in-game, tela de opções e game over |

**3 níveis jogáveis** + cutscene + menu principal + tela de game over.

<br>

## Minha contribuição

Este foi um trabalho em grupo, e minha atuação foi ampla — programação, level design e áudio:

**Programação**
- **Mecânica do player** — movimentação, controle e sistema de vida
- **Mecânica dos inimigos** — comportamento de movimento, combate e disparo
- **IA do Boss** ([`BossAi.cs`](Assets/Scripts/Enemys/Boss/BossAi.cs)) — máquina de estados com três fases (seguir rota, perseguir, atacar), detecção do player por raio de alcance, navegação por waypoints e cooldown de ataque
- **Barra de vida** ([`HealthUI.cs`](Assets/Scripts/Managers/HealthUI.cs)) — código e arte, com interpolação `Lerp` para a barra descer suavemente em vez de saltar
- **Menus e navegação** — fluxo entre menu principal, jogo, opções e game over

**Design**
- Level design e composição visual dos 3 mapas, montados a partir de bibliotecas de assets gratuitas
- Arte da barra de vida
- Roteiro e história do jogo

**Áudio**
- Direção musical e integração da trilha — as faixas (*Ascensio Angelorum*, *O Sol se pôs em Arcádia*) foram geradas com ferramenta de IA de composição, e a curadoria, o corte e a implementação no `AudioManager` foram nossos

Desenvolvido em conjunto com [@Zev07](https://github.com/Zev07) e demais colegas.

> **Nota sobre o histórico de commits:** durante a faculdade nosso fluxo era eu enviar o trabalho para um colega, que centralizava os envios ao repositório. Por isso o histórico deste repositório não reflete a divisão real do desenvolvimento.

<br>

## Como jogar

**Opção 1 — jogar direto**
Baixe o `.zip` na página de [Releases](../../releases/latest), extraia e execute `Arcadia Defense.exe`.
> ⚠️ O build disponível é apenas para **Windows**.

**Opção 2 — abrir no Unity**
1. Instale o **Unity Hub** e o **Unity Editor 2022.3 LTS** ou superior
2. Clone este repositório
3. Em *Add project from disk*, aponte para a pasta raiz do projeto
4. Abra a cena `Assets/Scenes/MenuPrincipal.unity`

<br>

## Estrutura do código

```
Assets/Scripts/
├── Player/       Movimentação e vida do jogador
├── Enemys/       Boss, combate, movimentação e spawner
├── Towers/       Torres, blueprints, mira e projéteis
├── Inventory/    ScriptableObjects de itens, drop e coleta
├── Shop/         Loja e compra de melhorias
├── Managers/     Áudio, cenas, UI, progressão e ondas
└── World/        NPCs e vida ambiente
```

<br>

## Créditos

Os sprites de personagens, inimigos e cenário vêm de bibliotecas de assets gratuitas. As músicas da trilha foram geradas com ferramenta de IA de composição musical, e os efeitos sonoros vêm de bibliotecas de áudio livre. O trabalho autoral do projeto está na **programação, no level design e na composição visual** dos mapas.

Projeto com finalidade **exclusivamente acadêmica**, sem qualquer intuito comercial.

<br>

---

<div align="center">

**Jhonatan Brum** · [LinkedIn](https://www.linkedin.com/in/jhonatan-brum/) · [GitHub](https://github.com/jhonysab)

</div>
