# Trabalho Prático 01 - Técnicas de Desenvolvimento de Videojogos
# Análise do jogo Platformer2D

## Grupo
- **Nome:** Hugo Rodrigues (31480)
- **Curso:** Engenharia de Desenvolvimento de Jogos Digitais (IPCA)
## Descrição do Jogo
O Platformer2D é um jogo de plataformas onde o jogador controla uma personagem que pode andar e saltar através de níveis, evitando obstáculos.

## Implementação
O jogo foi desenvolvido em C# utilizando o framework MonoGame. 
A estrutura principal baseia-se na classe PlatformerGame, com os métodos Update e Draw.
O movimento do jogador é tratado através de input do teclado, enquanto a física (gravidade e saltos) é implementada manualmente.
A gravidade é aplicada continuamente ao jogador, simulando um comportamento realista de queda. As colisões são tratadas para impedir que a personagem atravesse o chão.

## Decisões de Implementação
- Uso de sprites 2D para representar personagens
- Separação entre lógica de jogo e rendering
- Uso de tilemap para o nível

 ## Teclas
- Setas / A-D: mover personagem
- Espaço/ W / Seta para cima: saltar
- **Objetivo:** chegar ao fim do nível
  
## Estrutura do Projeto
- Platformer2D.Core → Contém toda a lógica e classes principais (.cs).
- Content → Pasta de assets (sprites, fontes e efeitos sonoros).
- Platformer2D.WindowsDX → Projeto de inicialização para ambiente Windows.
  
## Análise do Código
1. **Gestão de Input:** O código utiliza "Keyboard.GetState()" para detetar comandos em tempo real.
2. **Sistema de Colisões:** Implementado na classe "Level.cs", verificando a interseção entre o retângulo do jogador e os tiles adjacentes.
3. **Animação:** A classe "AnimationPlayer.cs" gere a troca de frames dos sprites baseada no tempo decorrido ("gameTime").

## Créditos e Referências
Este trabalho baseia-se no projeto original **Platformer2D** desenvolvido pela equipa oficial do **MonoGame**.
- **Fonte Original:** [MonoGame Samples Repository](https://github.com/MonoGame/MonoGame.Samples)
