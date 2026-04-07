# DevEx Marketplace

Afya DevEx Marketplace — uma coleção de skills, plugins, workflows e ferramentas de produtividade para desenvolvedores de software que utilizam Claude Code, Cursor e GitHub Copilot.

Desenvolvido pelo time de Developer Experience (DevEx) da Afya.

## Instalação

### Claude Code

Adicione este marketplace ao Claude Code:

```bash
/plugin marketplace add iclinic/devex-marketplace
```

### Cursor

1. Acesse o [Painel de Plugins do Cursor](https://cursor.com/dashboard/plugins)
2. Importe `iclinic/devex-marketplace` como um marketplace de equipe

Para instalar um plugin, clique nele no painel e depois clique em **Add to Cursor** para instalá-lo diretamente pela IDE desktop do Cursor.

### GitHub Copilot

Adicione este marketplace ao GitHub Copilot:

```bash
copilot plugin marketplace add iclinic/devex-marketplace
```

## Plugins Disponíveis

### Afyapowers (Core)

Um plugin de workflow de desenvolvimento determinístico e com fases controladas, derivado do superpowers. Impõe desenvolvimento estruturado de funcionalidades com estado persistente, continuidade de sessão e rastreabilidade completa.

**O que você obtém:**
- Workflow de desenvolvimento estruturado e com fases controladas
- Estado persistente e continuidade de sessão
- Rastreabilidade completa para desenvolvimento de funcionalidades

**Repositório:** https://github.com/iclinic/devex-marketplace

---

## Estrutura do Projeto

```
devex-marketplace/
├── .claude-plugin/
│   └── marketplace.json       # Catálogo de plugins do Claude Code
├── .cursor-plugin/
│   └── marketplace.json       # Catálogo de plugins do Cursor
├── .github/
│   └── plugin/
│       └── marketplace.json   # Catálogo de plugins do GitHub Copilot
└── README.md
```

## Contribuindo

Para adicionar um novo plugin ao marketplace, adicione a definição do plugin nos três arquivos de marketplace:

- `.claude-plugin/marketplace.json`
- `.cursor-plugin/marketplace.json`
- `.github/plugin/marketplace.json`

Cada plataforma possui um formato de source ligeiramente diferente. Consulte as entradas existentes como referência.

## Licença

Uso interno — Afya.
