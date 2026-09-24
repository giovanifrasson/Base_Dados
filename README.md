# Base_Dados

Repositório de dados base para Skills do Claude Code.

## Estrutura

```
Base_Dados/
└── SKILL/
    └── ICMS_SC/
        ├── icms-sc-skill.md      ← Arquivo da Skill (instalar em ~/.claude/agents/)
        └── Legislacao/
            ├── RICMS_SC_Regulamento.md
            ├── RICMS_SC_Anexo_01.md
            └── ...               ← Todos os 12 Anexos do RICMS/SC-01
```

## Como usar a Skill ICMS-SC

1. Baixe SKILL/ICMS_SC/icms-sc-skill.md
2. Copie para ~/.claude/agents/icms-sc.md
3. Reinicie o Claude Code
4. Use /icms-sc em qualquer conversa

A Skill busca os arquivos de legislação neste repositório via WebFetch.
