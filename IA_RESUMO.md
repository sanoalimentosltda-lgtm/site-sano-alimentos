# 🏢 IA_Resumo — Projeto Site Sano Alimentos

> **Documento técnico e funcional do projeto**
> Atualizado em: 03/07/2026

---

## 📋 Índice

1. [Sobre o Projeto](#1-sobre-o-projeto)
2. [Identidade Visual](#2-identidade-visual)
3. [Estrutura do Site](#3-estrutura-do-site)
4. [Funcionamento do Workflow](#4-funcionamento-do-workflow)
5. [Tecnologias Utilizadas](#5-tecnologias-utilizadas)
6. [Dados da Empresa (Consolidado)](#6-dados-da-empresa-consolidado)
7. [Manutenção e Evolução](#7-manutenção-e-evolução)
8. [URLs Importantes](#8-uris-importantes)
9. [Instruções para o Assistente](#9-instrucoes-para-o-assistente)

---

## 1. Sobre o Projeto

### 1.1 O que é

Site institucional de página única (One Page) do **Grupo Sano Alimentos**, empresa de suinocultura, bovinocultura, agricultura e distribuição de carnes com sede em **Patos de Minas - MG**, fundada em **1989**.

### 1.2 Propósito

Apresentar a história, as unidades produtivas, as operações e os valores da empresa de forma moderna, profissional e acolhedora.

### 1.3 Tagline Oficial

> **"Nossa história é a nossa conquista"**

---

## 2. Identidade Visual

### 2.1 Paleta de Cores

| Cor        | Hex       | Uso                                              |
|------------|-----------|--------------------------------------------------|
| **Navy**   | `#1a1a3e` | Fundos principais, header, footer, títulos       |
| **Gold**   | `#D4A830` | Detalhes, botões, destaques, ícones, stats       |
| **Terracota** | `#B84A30` | Tags de seção, acentos secundários              |
| **Cream**  | `#F5F0E8` | Fundos de seções alternadas, cards               |

### 2.2 Tipografia

| Função      | Fonte            | Estilos                                    |
|-------------|------------------|--------------------------------------------|
| **Títulos** | Playfair Display | 400, 600, 700 (regular + itálico)          |
| **Corpo**   | Inter            | 300, 400, 500, 600, 700, 800, 900          |

### 2.3 Logo

- **Origem:** Logo oficial da empresa (imagem PNG do Blogger)
- **Ajuste no header:** `filter: drop-shadow(0 0 8px rgba(255,255,255,0.2))`
- **Cores da logo:** Azul marinho, amarelo/dourado, vermelho

---

## 3. Estrutura do Site

```
HEADER → HERO → STATS → HISTÓRIA + TIMELINE → UNIDADES →
ATUAÇÃO → FROTA → VÍDEO → CTA → CONTATO → FOOTER
```

### Seções

| Seção    | ID          | Conteúdo                                    |
|----------|-------------|---------------------------------------------|
| Header   | `#header`   | Logo + navegação + menu mobile              |
| Hero     | `#hero`     | Tagline, CTAs                               |
| Stats    | (sem ID)    | 6 métricas da empresa                       |
| História | `#historia` | Texto + imagem + timeline                   |
| Unidades | `#unidades` | Cards com zoom hover                        |
| Atuação  | `#atuacao`  | Agricultura, Suínos, Bovinos, Frota         |
| Contato  | `#contato`  | Formulário + endereço + mapa Google         |

---

## 4. Workflow

### LobeHub → GitHub → Vercel

1. Pedido no chat do LobeHub
2. Assistente edita o `index.html`
3. Push para o GitHub
4. Vercel faz deploy automático
5. Site atualizado na internet

---

## 5. Tecnologias

HTML5 + Tailwind CSS + JavaScript + Google Fonts + GitHub + Vercel

Arquitetura: estático, único arquivo `index.html` (~46KB).

---

## 6. Dados da Empresa

### Geral

- **Razão Social:** Sano Alimentos LTDA
- **Fundação:** 1989
- **Fundadores:** Saulo de Deus Vieira e Valder Caixeta dos Santos
- **Sede:** Rua Negrinho de Freitas, 151, Patos de Minas - MG
- **Prêmio:** 2ª melhor Suinocultura do Brasil — Agriness

### Números

- 100 empregos diretos | 16 caminhões | 1.600 matrizes suínas
- 25.000 animais em crescimento | 1.000 reses bovinas
- 700+ ha lavouras | 8.000 m² no Distrito Industrial III

### Timeline

1989 → 1997 → 2001 → 2002 → 2009 → 2014 → 2015

---

## 7. URLs

| Recurso          | URL                                                       |
|------------------|-----------------------------------------------------------|
| **Site ao vivo** | https://site-sano-alimentos.vercel.app                    |
| **Repositório**  | https://github.com/sanoalimentosltda-lgtm/site-sano-alimentos |

---

## 8. ⚠️ Instruções para o Assistente

### 8.1 Conta e Acesso

- **Repositório:** `sanoalimentosltda-lgtm/site-sano-alimentos`
- **Autenticação:** Token salvo no LobeHub (credencial `github-sano-alimentos`, chave `GITHUB_TOKEN_SANO`)

### 8.2 ⛔ Regra Crítica

**NUNCA** usar a conta `juliamendesbeauty` para este projeto. A conta `juliamendesbeauty` é de outro projeto e não tem permissão neste repositório.

**Sempre usar** a credencial `github-sano-alimentos` do LobeHub.

### 8.3 Push

```bash
export GH_TOKEN="<recuperar da credencial github-sano-alimentos>"
cd /tmp/repo_sano
git pull origin main
# editar arquivos...
git add .
git -c user.email="sano@sanoalimentos.com" -c user.name="Sano Alimentos" commit -m "msg"
git push origin main
```

### 8.4 Segurança

O token NUNCA deve aparecer em arquivos, mensagens ou commits. Apenas recuperado da credencial segura do LobeHub em tempo de execução.

---

> **Sano Alimentos — Nossa história é a nossa conquista**
