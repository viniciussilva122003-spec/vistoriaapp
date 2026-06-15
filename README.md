# ⚡ VistoriaApp

App PWA para vistoria elétrica de sites de telecomunicações, data centers e instalações industriais.

## Funcionalidades

- ✅ Projetos por cliente / site
- ✅ Cadastro de quadros elétricos (QDG, QDCA, QDL, QTA…)
- ✅ Cadastro de consumidores com cálculo automático
- ✅ Cálculos NBR 5410 (monofásico, bifásico, trifásico)
- ✅ Alertas automáticos (>80% DJ, desequilíbrio de fase, neutro sobrecarregado)
- ✅ Gauge de ocupação por quadro
- ✅ Relatório de vistoria com tabela de cargas
- ✅ Exportação CSV (Excel / Google Sheets)
- ✅ Exportação Memorial TXT
- ✅ **100% offline** — dados salvos no dispositivo (IndexedDB)
- ✅ **Instalável como app** no iPhone (via Safari → Adicionar à tela de início)

## Deploy no GitHub Pages (2 minutos)

### Opção 1 — Interface web do GitHub

1. Crie um repositório novo em github.com (ex: `vistoriaapp`)
2. Clique em **Add file → Upload files**
3. Arraste os 3 arquivos: `index.html`, `sw.js`, `manifest.json`
4. Clique em **Commit changes**
5. Vá em **Settings → Pages**
6. Em *Source*, selecione **Deploy from a branch → main → / (root)**
7. Clique em **Save**
8. Em ~1 minuto o app estará em: `https://SEU_USUARIO.github.io/vistoriaapp/`

### Opção 2 — Git no terminal

```bash
git clone https://github.com/SEU_USUARIO/vistoriaapp.git
cp index.html sw.js manifest.json vistoriaapp/
cd vistoriaapp
git add .
git commit -m "VistoriaApp v1"
git push
```

Ative o GitHub Pages em **Settings → Pages → main → Save**.

## Instalar no iPhone como app

1. Abra o link no **Safari** (obrigatório — Chrome no iOS não suporta PWA)
2. Toque no ícone de **Compartilhar** (quadrado com seta para cima)
3. Toque em **Adicionar à tela de início**
4. Toque em **Adicionar**

O ícone ⚡ aparece na tela inicial. O app abre em tela cheia, sem barra do Safari, com dados 100% offline.

## Estrutura de arquivos

```
vistoriaapp/
├── index.html      ← App completo (HTML + CSS + JS)
├── sw.js           ← Service Worker (cache offline)
├── manifest.json   ← Manifest PWA (ícone, nome, cores)
└── README.md
```

## Tecnologias

- HTML5 / CSS3 / JavaScript vanilla
- IndexedDB para persistência local offline
- Service Worker para cache PWA
- Tabler Icons (CDN)
- Sem frameworks, sem build, sem dependências locais

## Próximos passos planejados

- [ ] Sincronização com Google Sheets via API
- [ ] Exportação PDF profissional com logo
- [ ] Fotos dos quadros e equipamentos
- [ ] Diagrama unifilar simplificado
- [ ] App nativo SwiftUI (iOS)
