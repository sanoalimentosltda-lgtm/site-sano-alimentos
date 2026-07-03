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

---

## 1. Sobre o Projeto

### 1.1 O que é

Site institucional de página única (One Page) do **Grupo Sano Alimentos**, empresa de suinocultura, bovinocultura, agricultura e distribuição de carnes com sede em **Patos de Minas - MG**, fundada em **1989** por **Saulo de Deus Vieira** e **Valder Caixeta dos Santos**.

### 1.2 Propósito

Apresentar a história, as unidades produtivas, as operações e os valores da empresa de forma moderna, profissional e acolhedora, servindo como vitrine digital para clientes, parceiros e colaboradores.

### 1.3 Tagline Oficial

> **"Nossa história é a nossa conquista"**

---

## 2. Identidade Visual

### 2.1 Paleta de Cores

A paleta foi extraída da **logo oficial da empresa** (após análise do logo real enviado pelo cliente), substituindo a paleta verde original do briefing inicial.

| Cor        | Hex       | Uso                                              |
|------------|-----------|--------------------------------------------------|
| **Navy**   | `#1a1a3e` | Fundos principais, header, footer, títulos       |
| **Gold**   | `#D4A830` | Detalhes, botões, destaques, ícones, stats       |
| **Terracota** | `#B84A30` | Tags de seção, acentos secundários              |
| **Cream**  | `#F5F0E8` | Fundos de seções alternadas, cards               |

### 2.2 Tipografia

| Função          | Fonte              | Estilos                                              |
|-----------------|--------------------|------------------------------------------------------|
| **Títulos**     | Playfair Display   | 400, 600, 700 (regular + itálico)                    |
| **Corpo**       | Inter              | 300, 400, 500, 600, 700, 800, 900                    |

### 2.3 Logo

- **Origem:** Logo oficial da empresa (imagem PNG do Blogger)
- **Ajuste no header:** `filter: drop-shadow(0 0 8px rgba(255,255,255,0.2))`
- **Cores da logo:** Azul marinho, amarelo/dourado, vermelho (base da paleta)

---

## 3. Estrutura do Site

```
HEADER TRANSPARENTE → HERO FULL-SCREEN → STATS BAR (6 métricas) →
HISTÓRIA (texto + img + timeline) → UNIDADES (6 cards imersivos) →
ATUAÇÃO (4 cards) → FROTA → VÍDEO YouTube → CTA →
CONTATO (form + endereço + mapa) → FOOTER
```

| Seção       | ID              | Conteúdo                                              |
|-------------|-----------------|-------------------------------------------------------|
| Header      | `#header`       | Logo + navegação + menu mobile                        |
| Hero        | `#hero`         | Tagline, stats resumo, CTAs                           |
| Stats       | (sem ID)        | 6 métricas: 35+ anos, 100 empregos, etc.              |
| História    | `#historia`     | Texto fundação + imagem + timeline                    |
| Unidades    | `#unidades`     | Granjas + Lavouras com hover zoom                     |
| Atuação     | `#atuacao`      | Cards Agricultura, Suínos, Bovinos, Frota             |
| Frota       | (embutido)      | Detalhamento dos 16 caminhões                         |
| Vídeo       | (embutido)      | YouTube embed institucional                           |
| CTA         | (embutido)      | "Vamos conversar?"                                    |
| Contato     | `#contato`      | Formulário + endereço + mapa Google                   |
| Footer      | (embutido)      | Logo, direitos reservados                             |

---

## 4. Funcionamento do Workflow

### LobeHub → GitHub → Vercel

1. **Você faz um pedido** no chat do LobeHub em português natural
2. **O assistente processa** e edita o arquivo `index.html`
3. **O assistente faz push** para o GitHub
4. **O Vercel detecta** a mudança e faz deploy automático (~30s)
5. **O site fica disponível** na internet

### Vantagens

- Deploy automático: toda alteração → site atualizado
- Histórico no GitHub: possibilidade de reverter mudanças
- Hospedagem gratuita na Vercel com SSL e CDN
- Não precisa saber programar

---

## 5. Tecnologias

| Tecnologia       | Função                                    |
|------------------|-------------------------------------------|
| **HTML5**        | Estrutura do site                         |
| **Tailwind CSS** | Framework CSS via CDN                     |
| **JavaScript**   | Scroll reveal, menu mobile, interações    |
| **Google Fonts** | Playfair Display + Inter                  |
| **YouTube**      | Embed do vídeo institucional              |
| **Google Maps**  | Embed do mapa                             |
| **GitHub**       | Versionamento e repositório               |
| **Vercel**       | Hospedagem e deploy contínuo              |

Arquitetura: **totalmente estático** — um único `index.html` (~46KB).

---

## 6. Dados da Empresa (Consolidado)

### Informações Gerais

| Item                  | Dado                                             |
|-----------------------|--------------------------------------------------|
| **Razão Social**      | Sano Alimentos LTDA                              |
| **Fundação**          | 1989                                             |
| **Fundadores**        | Saulo de Deus Vieira e Valder Caixeta dos Santos |
| **Sede**              | Rua Negrinho de Freitas, 151, Patos de Minas - MG |
| **Segmento**          | Suinocultura, Bovinocultura, Agricultura, Distribuição |
| **Tagline**           | "Nossa história é a nossa conquista"             |
| **Prêmio**            | 2ª melhor Suinocultura do Brasil — Agriness      |

### Números da Operação

| Indicador                        | Quantidade           |
|----------------------------------|----------------------|
| Empregos diretos                 | 100                  |
| Caminhões na frota               | 16                   |
| Matrizes suínas                  | 1.600                |
| Animais em crescimento           | 25.000               |
| Reses bovinas                    | 1.000                |
| Pastagens para bovinos           | 600 ha               |
| Capacidade bovina anual          | 5.000 animais/ano    |
| Hectares lavouras                | 700+ ha              |
| Imóvel Distrito Industrial III   | 8.000 m²             |

### Unidades

| Unidade              | Atividade                             | Capacidade                        |
|----------------------|---------------------------------------|-----------------------------------|
| Granja Abelhas       | UPL                                   | ~620 matrizes, 3.000 animais     |
| Granja Patinhas      | Recria/terminação + Fábrica rações    | 4.300 animais, 2 silos           |
| Granja Esperança     | Terminação + Café                     | 650 matrizes, 10.000 animais     |
| Faz. Ribeirão da Mata| Confinamento bovino                   | 40 ha                            |
| Granja Diamante      | Terminação                            | 330 matrizes, 3.500 animais      |
| Lavouras             | Agricultura de precisão               | 700+ ha                          |

### Timeline

| Ano  | Evento                                                  |
|------|---------------------------------------------------------|
| 1989 | Fundação com Granja Abelhas                             |
| 1997 | Criação da Sano Alimentos LTDA                          |
| 2001 | Início da distribuição de carcaças                      |
| 2002 | Aquisição da Granja Esperança (34 ha)                   |
| 2009 | Aquisição da Fazenda Ribeirão da Mata (40 ha)           |
| 2014 | Aquisição de 8.000 m² no Distrito Industrial III        |
| 2015 | Arrendamento da Granja Diamante                         |

---

## 7. Manutenção

### Como Pedir Alterações

Basta falar no chat do LobeHub em português natural. Exemplos:

- "Remove a caixa de descrição do vídeo"
- "Corrige a timeline, o item 2015 está desalinhado"
- "A logo está sumindo no fundo escuro"
- "Atualiza o texto do hero com os dados da transcrição do vídeo"

### O que Pode Ser Alterado

| Tipo              | Exemplo                                           |
|-------------------|---------------------------------------------------|
| Texto             | Corrigir informações, atualizar dados             |
| Cores             | Ajustar paleta, mudar cor de botões               |
| Layout            | Reordenar seções, adicionar/remover elementos     |
| Imagens           | Trocar imagens de fundo, logos, fotos             |
| Seções            | Adicionar novas seções                            |
| Responsividade    | Ajustar para tablets, celulares                   |
| SEO               | Meta tags, descrições, Open Graph                 |

### Evoluções Futuras Possíveis

- Integrar formulário de contato com serviço de email
- Registrar domínio próprio (ex: sanoalimentos.com.br)
- Galeria de fotos reais das unidades
- Blog ou seção de notícias
- E-commerce

---

## 8. URLs Importantes

| Recurso          | URL                                                       |
|------------------|-----------------------------------------------------------|
| **Site ao vivo** | https://site-sano-alimentos.vercel.app                    |
| **Repositório**  | https://github.com/sanoalimentosltda-lgtm/site-sano-alimentos |

---

> **Sano Alimentos — Nossa história é a nossa conquista**
