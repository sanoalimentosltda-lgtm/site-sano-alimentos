# IA Resumo - Site Sano Alimentos

## 📋 Sobre
Site institucional do **Grupo Sano Alimentos** (Patos de Minas - MG). One-page moderna com história, unidades, operacoes, premios e contato.

## 🚀 Deploy
- **URL:** https://site-sano-alimentos.vercel.app
- **Repo:** github.com/sanoalimentosltda-lgtm/site-sano-alimentos
- **Automatico:** Push no main → Vercel deploy automatico

## 📐 Stack
- HTML5 + Tailwind CSS (CDN) + JavaScript
- Google Fonts: Playfair Display (titulos) + Inter (corpo)
- Hospedagem: Vercel (deploy continuo)

## 🎨 Identidade Visual
- **Paleta:** Navy #1a1a3e, Gold #D4A830, Terracota #B84A30, Cream #F5F0E8
- **Logo oficial:** Cores azul marinho, amarelo, vermelho (extraidas da logo real)
- **Logo header:** Oval amarelo com "Sano" + fundo transparente (ajustado p/ header navy)

## 🏗️ Estrutura do Site
1. **Header** - Sempre visivel (bg navy/95), logo + navegacao
2. **Hero** - Tagline "Nossa historia e a nossa conquista"
3. **Stats** - 35+ anos, 80+ empregos, 16 caminhoes, 700+ ha, 3x Agriness, 25.000 animais
4. **Historia** - Texto com fundacao 1989, Agroceres PIC, timeline interativa, foto dos fundadores
5. **Unidades** - Cards: Abelhas (UPL), Patinhas (recria/terminacao), Esperanca, Ribeirao da Mata, Sede, Lavouras
6. **Atuacao** - Cards: Suinocultura, Bovinocultura, Agricultura, Distribuicao
7. **Ciclo Produtivo** - 4 fases da suinocultura
8. **Premios** - Tabela com 3 premios Agriness (9a 2016, 11a 2018, 14a 2021)
9. **Video** - YouTube embed institucional
10. **Missao + Valores + Resp. Social** - Cards e bloco social
11. **CTA + Contato** - Formulario, endereco, mapa, telefone/email
12. **Footer** - Logo, navegacao, copyright

## 📝 Historico de Alteracoes

### Fase 1 - Estrutura Inicial
- Criacao do site one-page com hero, historia, timeline, unidades, atuacao, contato
- Deploy na Vercel com dominio temporario

### Fase 2 - Identidade Visual
- Paleta ajustada para cores reais da logo (navy/gold/terracota/cream)
- Logo oficial tratada: fundo branco removido, glow eliminado
- Fonte: Playfair Display + Inter

### Fase 3 - Conteudo e Dados
- Informacoes atualizadas da transcricao do video institucional
- Historia enriquecida: fundadores ex-funcionarios da Agroceres PIC
- Timeline reorganizada: 1989, 1993, 1997, 2001, 2002, 2009, 2012 (Sede), 2014
- Foto dos fundadores (Saulo e Valder) no evento de 30 anos inserida na historia

### Fase 4 - Remocoes e Correcoes
- Granja Diamante removida (nao existe mais)
- Secao Infraestrutura (Frota + Distrito Industrial) removida (info duplicada)
- Badge premio "2a Melhor Suinocultura" removido do hero e historia
- Repeticoes do premio no Ciclo Produtivo eliminadas
- Cards Atuacao reordenados: Suino > Bovi > Agri > Distrib
- Badges "Desde X" removidos dos cards de unidades
- Icones redes sociais: LinkedIn e WhatsApp (com links reais)

### Fase 5 - Premiacoes
- Tabela de premios Agriness unificada antes do video:
  - 9a Ed. 2016: 2o Lugar Brasil (501-1000 matrizes)
  - 11a Ed. 2018: 1o Lugar Brasil (ate 300 matrizes)
  - 14a Ed. 2021: 2o Lugar Brasil (501-1000 matrizes)
- Stat "3x Premiada Agriness"

### Fase 6 - Formulario e Contato
- Formulario integrado com FormSubmit
- Email: controladoria@sanoalimentos.com.br
- WhatsApp: wa.me/553438219928
- Endereco: Rua Negrinho de Freitas, 151 - Cidade Nova, Patos de Minas - MG

### Fase 7 - Ortografia e Padronizacao
- Correcao de acentos em toda a secao "Nossa Filosofia"
- Padronizacao de classes de texto (text-navy-500/80 leading-relaxed)
- Texto "Patos de Minas e regiao*" padronizado

### Fase 8 - Logo
- Logo recortada para apenas o oval amarelo com "Sano"
- Removido "Produtos" (topo) e "Carnes nobres desde 1989" (base)
- Fundo branco removido, cores originais preservadas
- Header sempre visivel (bg navy desde o carregamento)

## 📦 Fotos no Repositorio
- fotos/abelhas.jpg - Granja Abelhas
- fotos/patinhas.png - Granja Patinhas
- fotos/esperanca.jpg - Granja Esperanca
- fotos/ribeirao.jpg - Faz. Ribeirao da Mata
- fotos/sede.jpg - Sede Administrativa
- fotos/fundadores.jpg - Saulo e Valder (30 anos Sano)
- fotos/logo_sano.png - Logo oficial (apenas oval Sano)

## 🔗 Links Importantes
- **Site:** https://site-sano-alimentos.vercel.app
- **GitHub:** https://github.com/sanoalimentosltda-lgtm/site-sano-alimentos
- **Video:** https://www.youtube.com/watch?v=FzdzpJC8sHA
- **Formulario:** formsubmit.co/controladoria@sanoalimentos.com.br

## 🪟 Lightbox - Histórico e Lições Aprendidas

### Contexto
O lightbox (visualização ampliada das fotos das propriedades) foi implementado no commit `1a0b3a0`.
Ele permite clicar nos cards das propriedades (Granja Abelhas, Patinhas, Esperança, etc.) para ver a foto em tamanho maior com fundo escuro.

### Estrutura do Lightbox
- **CSS:** Classe `.lightbox` com `position: fixed; z-index: 9999` e `.lightbox.active { display: flex; }`
- **HTML:** `<div id="lightbox">` com `<img id="lightbox-img">` e `<div id="lightbox-caption">`
- **JS:** Funções `openLightbox(filename, caption)` e `closeLightbox()`
- **Imagens:** Servidas via `raw.githubusercontent.com` do próprio repositório (pasta `/fotos/`)

### 🐛 BUG CRÍTICO DESCOBERTO (Julho 2026)
O lightbox parou de funcionar corretamente (imagem aparecia minúscula ou tela preta sem imagem) devido a **tags HTML mal fechadas** na seção da timeline ("Marcos da nossa jornada").

**Causa:** Ao reformatar a timeline (commit `b9d04df`), a estrutura de fechamento da seção História foi quebrada:
- Faltaram 4 tags de fechamento (`</div>` x3 + `</section>`)
- Isso fez o DOM inteiro ficar malformado
- O lightbox (posicionado depois no HTML) ficou dentro de uma estrutura quebrada
- O `z-index`, posicionamento `fixed` e layout do lightbox foram afetados

**Solução:** Garantir que TODAS as seções HTML sejam corretamente fechadas com `</section>`, `</div>` etc. Um DOM malformado afeta componentes que usam `position: fixed` e `z-index`.

**Lições:**
1. ⚠️ Sempre verificar se seções HTML têm fechamento correto (`</section>`, `</div>`)
2. 🔍 Se o lightbox (ou qualquer elemento `position: fixed`) parar de funcionar, verificar a estrutura do DOM primeiro
3. ✅ A ordem de fechamento correta é: divs aninhados → div da seção → `</section>` → próxima seção
4. 📐 O `max-width: 90%` na imagem do lightbox funciona apenas em DOM bem formado (standards mode)
5. 🚫 A falta de `<!DOCTYPE html>` também pode causar problemas (quirks mode)

### Commits de referência
- `a3543df` — Último commit ANTES do bug (lightbox funcionando)
- `b9d04df` — Commit onde o bug foi INTRODUZIDO (timeline quebrou o DOM)
- `218e490` — Commit onde o bug foi CORRIGIDO
