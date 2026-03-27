# 🌱 Sisteminha Embrapa — Semiárido Pernambucano

> Ferramenta de planejamento agrícola para agricultura familiar no semiárido de Pernambuco.
> Calendário de plantio escalonado, banco de sementes pessoal e visualizações 3D interativas de todos os módulos do sisteminha.

---

## 🎬 Preview em Vídeo

[![Preview do Sítio](https://img.youtube.com/vi/VIDEO_ID_AQUI/maxresdefault.jpg)](https://www.youtube.com/watch?v=VIDEO_ID_AQUI)

> **Como atualizar:** Suba o `docs/preview_sitio_2x.mov` no YouTube como **Não listado** e substitua `VIDEO_ID_AQUI` nas duas URLs acima pelo ID gerado (ex: `dQw4w9WgXcQ`).

---

## 🖥 Demo

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/psvictor-dev/urban-system)

---

## 📦 O que está neste repositório

| Arquivo | Descrição |
|--------|-----------|
| `index.html` | App principal — Calendário, Canteiros e Banco de Sementes |
| `sitio_3d.html` | Visualização 3D do sítio completo com todos os módulos |
| `galinheiro_3d.html` | Visualização 3D interativa do galinheiro low cost |
| `horta_3d.html` | Visualização 3D da horta — 4 canteiros + sementeira |
| `tanque_tilapias_3d.html` | Visualização 3D do tanque de tilápias |
| `composteira_minhocario_3d.html` | Visualização 3D da composteira e minhocário |
| `planejamento_canteiros_maio2027.html` | Planejamento detalhado dos canteiros |
| `docs/PlanoSisteminhaEmbrapa_6meses.pdf` | Plano de implantação mês a mês (PDF) |
| `docs/Galinheiro_LowCost_Embrapa.pdf` | Estrutura e montagem do galinheiro (PDF) |
| `README.md` | Este arquivo |

---

## ✨ Funcionalidades

### 📅 Calendário de Plantio
- Tabela mensal com **26 culturas** adaptadas ao semiárido pernambucano
- Código visual: **P** plantar · **S** sementeira · **C** colheita · **⚠** atenção
- Barra climática indicando período chuvoso (mar–jul) e seco (ago–fev)
- Notas técnicas por cultura com variedades recomendadas pela Embrapa

### 🔄 Escalonamento dos Canteiros
- 4 canteiros de **5m × 1,4m** organizados por função
- Régua quinzenal: o que fazer a cada 15 dias para colheita contínua
- Ciclos de plantio anuais por canteiro com períodos de descanso

### 🫙 Banco de Sementes Pessoal
- Cadastro completo: nome, variedade, tipo, estoque em gramas, origem e notas
- Filtros por categoria: Hortaliças · Ervas · Grãos · Frutas · Milpa · Flores
- Barra de estoque visual com alerta de baixo estoque
- **Dados salvos localmente no navegador** (localStorage) — sem necessidade de servidor
- Merge inteligente: novas sementes adicionadas em atualizações não sobrescrevem dados existentes

### 🐔 Galinheiro 3D
- Visualização 3D interativa com **Three.js**
- Rotação livre com mouse/touch · Zoom · Rotação automática
- Vistas pré-definidas: Isométrico · Frente · Lateral · Topo
- Opções de ocultar telhado e paredes para ver o interior
- Galinhas animadas, ninhos, poleiros, bebedouro e comedouro

---

## 🌵 Plantas incluídas

### Hortaliças e Legumes
Rúcula · Couve · Brócolis · Tomate · Pimentão · Quiabo · Abobrinha · Cenoura · Alface · Batata-doce

### Ervas e Temperos
Coentro · Cebolinha · Salsinha · Manjericão · Capim-limão

### Grãos e Leguminosas
Feijão-caupi (BRS Pujante) · Feijão-fava · Feijão-de-metro · Lentilha · Alho · Cebola

### Milpa (Consórcio)
Milho (BRS Caatingueiro) · Feijão-caupi · Abóbora

### Frutas
Banana Pacovan · Abacaxi Pérola · Maracujá (BRS Sol do Cerrado) · Girassol

### Flores Companheiras
Cravo-de-defunto · Cosmos · Outras flores de bordadura

---

## 🏗 Estrutura do Sisteminha Embrapa

O projeto é baseado na tecnologia **Sisteminha Embrapa/UFU/Fapemig**, desenvolvida pelo zootecnista **Luiz Carlos Guilherme** em 2011, adaptada para o contexto do semiárido pernambucano com:

```
Cisterna 16.000L (parte baixa do terreno)
    ↓
Galinheiro 4×6m — 20 galinhas Embrapa 051
    ↓ esterco
Compostagem (45 dias) → Minhocário → Húmus
    ↓ húmus
Horta — 4 canteiros 5×1,4m
    ↑ água nutrida
Tanque Tilápias 10.000L — 150 peixes
    ↑ reposição
Captação de chuva / cisterna
```

---

## 🗓 Calendário Climático — Semiárido PE

| Período | Meses | Regime |
|---------|-------|--------|
| Chuvoso | Mar · Abr · Mai · Jun · Jul | 💧 Chuvas concentradas |
| Seco | Ago · Set · Out · Nov · Dez · Jan · Fev | ☀ Irrigação essencial |

> Com a cisterna de 16.000L e o tanque do sisteminha, é possível manter produção o ano todo.

---

## 🚀 Como usar localmente

Não há dependências nem build necessário. Basta abrir o arquivo:

```bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/sisteminha-embrapa.git
cd sisteminha-embrapa

# Abrir no navegador (qualquer um desses)
open index.html           # Mac
start index.html          # Windows
xdg-open index.html       # Linux
```

Ou acesse diretamente pelo link do Vercel após o deploy.

---

## ▲ Deploy no Vercel

1. Acesse [vercel.com](https://vercel.com) e faça login com GitHub
2. Clique em **Add New Project**
3. Selecione o repositório `sisteminha-embrapa`
4. Deixar todas as configurações padrão (sem framework, sem build)
5. Clique em **Deploy**

Qualquer `git push` atualiza o site automaticamente.

```bash
# Fluxo de atualização
git add .
git commit -m "feat: adicionar novas sementes ao banco"
git push origin main
# → Vercel redeploy automático em ~30 segundos
```

---

## 📁 Adicionar novos arquivos ao repositório

```bash
# Após baixar novos PDFs ou HTMLs gerados
cp ~/Downloads/novo_arquivo.html .
git add novo_arquivo.html
git commit -m "docs: adicionar plano de irrigação"
git push origin main
```

---

## 🌾 Fontes e Referências

- **Sisteminha Embrapa oficial:** [sisteminhaembrapa.org](https://www.sisteminhaembrapa.org)
- **Embrapa Semiárido (Petrolina-PE):** [embrapa.br/semiarido](https://www.embrapa.br/semiarido)
- **Embrapa Hortaliças:** [embrapa.br/hortalicas](https://www.embrapa.br/hortalicas)
- **Emater/IPA Pernambuco:** assistência técnica gratuita para agricultores familiares
- **Tese original:** Luiz Carlos Guilherme, Embrapa/UFU/Fapemig (2011)
- **Aviários para Galinhas Caipiras NE:** Embrapa Meio-Norte (2018)
- **Calendário agrícola Nordeste:** MAPA / Embrapa / CONAB

---

## 📋 Roadmap

- [ ] Adicionar módulo de controle de irrigação (consumo da cisterna)
- [ ] Integrar calendário lunar ao escalonamento
- [ ] Módulo de registro de colheitas (diário da horta)
- [ ] Exportar banco de sementes em CSV/PDF
- [ ] Adicionar módulo do tanque de tilápias com controle de ração
- [ ] Versão mobile otimizada (PWA)
- [ ] Mapa interativo do layout do sítio com posicionamento dos módulos

---

## 🤝 Contribuindo

Sugestões, correções e adaptações regionais são bem-vindas!

1. Fork este repositório
2. Crie uma branch: `git checkout -b feat/minha-melhoria`
3. Commit: `git commit -m 'feat: descrição da melhoria'`
4. Push: `git push origin feat/minha-melhoria`
5. Abra um Pull Request

---

## 📄 Licença

Este projeto é de uso livre para agricultores familiares e fins educativos.  
Tecnologia base: © Embrapa — todos os créditos técnicos aos pesquisadores da Embrapa.

---

<p align="center">
  Feito com 🌱 para o semiárido pernambucano<br>
  <em>"A seca não é o problema. A falta de planejamento é."</em>
</p>
