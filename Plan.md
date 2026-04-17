# Game concept

TaylorSwiftSentAHitmanMyWay é um jogo de puzzle/platformer e terror psicologico inspirado em Angry Birds e Celeste, herdando uma mistura de mecânicas e gameplay entre ambos os jogos. Baseia-se numa andorinha chamada Andy, que quer derrotar o criador da linguagem de programação Swift (Chris Lattner) consertando "bugs" que seriam completamente razoaveis em qualquer outra linguagem.
# Gameplay loop

O gameplay loop do jogo é o clássico, modulo de níveis, onde o Andy é disparado do canhão "Try-Throw", e enquanto no ar, consegue apanhar extensões para prolongar o voo enquanto se desvia de obstáculos e atinge os "bugs" presentes no nível. O jogador ganha se conseguir atingir todos os "bugs" na tela.
# Technical approach

- World space: World space is fixed. All objects stay within the same screen position, until being cleared on moving to the next level and new ones are instantiated.
- Collisions: AABB or OBB with SAT collisions, where we use axis to compare (non-rotating and rotating objects respectively).
- Vectorial physics: Simple vector based movement with gravity simulation. Will also use collisions for certain things like kinetic reflection/etc
- Level transitions: After clearing some goal the game transitions to the next scene/level
- Sprites: Uses SpriteKit
# MVP scope

Para garantir que o projeto é realista e executável, vamos nos focar em:
Mecânica base seria o lançamento, como ângulos e forças;
Sistema de detenção de colisão funcional para ressaltos simples em obstáculos (ex: paredes, etc);
Objetos que influenciam a partida, como power ups;
Interface de utilizador (UI) básicas com botões de voltar ao menu, pontuação na tela e quantidade de saltos;

# Future ideas

Como planos de expansão futura, o projeto poderá incluir:
Zonas de efeito, que alteram o projétil.
Diversidade de projéteis, com diferentes comportamentos de ressalto ou tamanhos.
Obstáculos destrutíveis, que desaparecem após um determinado número de impactos.
Boss final, batalha realizada se atingir um quantidade razoável de pontos, utilizando no mapa os pawer ups para derrotar o criador do Swift, Chris Lattner.
