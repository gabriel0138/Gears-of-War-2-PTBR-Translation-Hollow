# Tradução e Otimização PT-BR - Gears of War 2 (GoW2Hollow)

Este pacote contém a tradução completa em Português do Brasil e otimizações de performance de última geração para a versão PC do port **Gears of War 2 - Hollow**.

---

## 🌟 Conteúdo do Pacote

- **Tradução 100% PT-BR**:
  - Legendas de vídeos, cinematics e falas de rádio de 100% dos personagens (Marcus, Dom, Baird, Cole, Anya, Hoffman, Carmine, etc.).
  - 41 parágrafos e documentos de colecionáveis traduzidos.
  - 50 conquistas e Diário de Guerra sincronizados em PT-BR.
  - Mensagens de interface, avisos de sistema e menus 100% em Português do Brasil.
  - Refinamento terminológico oficial do universo Gears (*Vermes*, *Imulsion*, *COG*, *Lancer*, *Bomba de Imulsion*, *Arco de Torques*, *Amigão!*, *caos total*).

- **Otimização Extrema de Desempenho (Unreal Engine 3)**:
  - **PoolSize=6144**: Reserva 6GB de VRAM para eliminação total de pop-in de textura e stutters em GPUs dedicadas.
  - **OneFrameThreadLag=False**: Redução drástica de input lag e resposta instantânea aos comandos.
  - **SmoothFrameRate=False**: Desbloqueio de FPS para monitores de alta frequência (144Hz, 165Hz, 240Hz+).
  - **TimeBetweenPurgingPendingKillObjects=120**: Garbage Collector otimizado a cada 2 minutos, zerando engasgos em tiroteios.
  - Sombras em alta resolução (4096px) e filtragem anisotrópica 16x.

---

## 🚧 Status Atual & Itens Pendentes (Work in Progress)

Trabalhamos continuamente para entregar a melhor experiência possível. Abaixo estão os pontos que ainda estão em desenvolvimento:

1. **Página de Conquistas do Diário de Guerra (War Journal)**:
   - A aba interna de visualização do Diário de Guerra in-game ainda possui partes do layout da interface pendentes de tradução visual.

2. **Escala / Tamanho das Legendas em Altas Resoluções (1080p, 1440p, 4K, 16:10)**:
   - **O Problema**: A interface original do jogo roda sobre caixas do Autodesk Scaleform (GFx) ancoradas em 720p.
   - **O que já tentamos**:
     - Alteração dos parâmetros `SubtitleFontScale`, `UIScaleMultiplier` e `bScaleSubtitles` em todos os `.ini` (`GearEngine.ini`, `DefaultEngine.ini`, `BaseEngine.ini`).
     - Aplicado o bloqueio de atributo 'Apenas Leitura' (`IsReadOnly`) para impedir resets pelo launcher.
     - Redirecionamento de vetores de fontes em `GearGameUI.int` para fontes de alta resolução (`WarfareFonts_Euro24` / `Chrom24`).
     - Injeção direta de argumentos de linha de comando (`-SubtitleFontScale=2.5`, `-UIScaleMultiplier=1.8`) no processo `GoW2Hollow.exe`.
   - **Status**: O motor da UE3 ignora a redimensionação dinâmica do texto sem a modificação direta nos pacotes `.upk`/`.gfx` de interface. Continuaremos investigando soluções e patches para contornar essa limitação técnica.

---

## 📢 Como Ajudar / Reportar Bugs

Este projeto é feito para a comunidade! Se você encontrar qualquer erro de digitação, fala não traduzida, bug visual ou falha de formatação:

1. Acesse a aba **[Issues](../../issues)** no repositório.
2. Clique em **New Issue** e descreva o problema (se possível, anexe uma captura de tela e o capítulo em que o erro ocorreu).
3. Atualizações e novas correções serão lançadas periodicamente nesta página.

---

## 🚀 Instruções de Instalação

1. Baixe o arquivo **`GearsOfWar2_PTBR_Traducao_Completa.zip`** no repositório ou na aba **Releases**.
2. Extraia o conteúdo do `.zip`.
3. Copie as pastas extraídas (`GearGame`, `Engine`, `Binaries`) para a pasta raiz do seu **Gears of War 2 - Hollow**.
4. Substitua os arquivos se o Windows perguntar.
5. Inicie o jogo normalmente!

---

## 🔒 Proteção Contra Resets do Launcher

Os arquivos `.ini` de configuração da tradução e otimização já vêm pré-configurados com a propriedade **Somente Leitura (Read-Only)** ativada para evitar que o launcher altere ou resete as preferências ao iniciar o jogo.

---

### 💻 Compatibilidade
- Desenvolvido e homologado especificamente para a versão PC **Gears of War 2 - Hollow**.
- Compatível com monitores 16:9 e 16:10 (1080p, 1440p, 4K).