<!-- Sync impact: scaffold -> 1.0.0; princípios derivados de AGENTS.md;
nenhuma regra existente removida; sem pendências. -->
# GateFall Constitution

## Core Principles

### I. Comparabilidade experimental
A, B0, B1, C0 e C1 devem compartilhar grade temporal, partições, sementes,
TCN, número de épocas e política de seleção nas novas comparações. Ablações
alteram um fator declarado por vez. Referências históricas são somente leitura.

### II. Causalidade e separação dos dados
Dividir por vídeo, preferencialmente por sujeito; nunca dividir janelas do
mesmo vídeo entre partições. Features temporais usam apenas passado e presente.
Estatísticas são estimadas exclusivamente no treino. Teste não seleciona parâmetros.

### III. RGB e backbones congelados
Nenhum sensor de profundidade ou descritor derivado de profundidade entra no
sistema. YOLO-Pose, DINOv3 e SAM 3 permanecem congelados, com extração offline.
Features persistidas são agrupadas por vídeo, nunca por quadro.

### IV. Evidência verificável
Distinguir provas matemáticas, testes sintéticos e experimentos reais. Provas
Lean devem explicitar hipóteses, sem sorry/admit. Testes numéricos não provam
melhoria de métricas. Alterações Python exigem uv run pyright.

### V. Escopo e rastreabilidade
Cada adição deve declarar o que substitui. Esta rodada substitui exploração
de novos backbones por controles de confiabilidade. Configurações, fontes,
sementes, versões de features e checkpoints devem ser rastreáveis.

## Restrições adicionais
Documentação e comentários em português brasileiro; identificadores, commits
e títulos de PR em inglês. AGENTS.md continua sendo a fonte das convenções
existentes. Não promover resultados locais automaticamente.

## Fluxo de desenvolvimento
Especificar, planejar, decompor tarefas, implementar e verificar. Testes
sintéticos são necessários quando demonstram contratos numéricos ou causais;
não introduzir framework apenas para mudanças de baixo impacto.

## Governance
Mudanças de princípios exigem justificativa e versionamento semântico.
Revisões devem verificar as invariantes e registrar limitações experimentais.
Instruções explícitas do usuário têm precedência sobre este documento.

**Version**: 1.0.0 | **Ratified**: 2026-10-09 | **Last Amended**: 2026-10-09
