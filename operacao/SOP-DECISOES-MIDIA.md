# SOP — Decisões de Mídia (Confere)

> DEFINIÇÃO DE VENCEDOR = Oferta com ROI positivo escalada dando lucro.
> Regra de ouro: **SEMPRE 1 variável por ciclo**. Ciclo = 48–72h OU ~R$ 60–80 de gasto, o que ocorrer primeiro.

---

## 1. Fundamento: a matemática da vitória

| Indicador | Valor | Como calcular |
|---|---|---|
| Preço na página | R$ 50,89 | tabelado |
| Receita líquida pós-Cakto | ~R$ 44–47 | preço − (taxa Cakto + taxa fixa) |
| **CPA break-even** | **~R$ 40–45** | acima disso = perde dinheiro |
| **CPA alvo (com lucro)** | **≤ R$ 25** | ~50% de margem |

**Matemática reversa (com seu CPM atual de R$ 7):**
R$ 50 de gasto ≈ 7.300 impressões → com CTR de 1% ≈ 73 cliques reais → se 5% chegam ao checkout e 3% compram → **CPA ≈ R$ 23 → DÁ LUCRO** ✓

**Conclusão:** a oferta é matematicamente lucrativa SE o funil se comporta. Cada etapa tem um gatilho numérico abaixo — quando ela quebra, você sabe ONDE agir.

---

## 2. Ordem de leitura do gargalo (SLEP)

`S`pend → `L`anding → Etapas → `P`urchase. Antes de tocar em qualquer alavanca:

1. **O clique é humano?** CTR > 3% + CPC < R$ 0,15 = suspeita de bot → desligar Pangle/Audience Network
2. **GA4 mostra sessões ≈ cliques?** Se menos de 60% dos cliques aparecem como sessões → tráfego lixo → o problema é PLACEMENT, não criativo

---

## 3. Tabela de decisão por etapa (gatilhos numéricos)

| # | Alavanca | Métrica | Saudável | GATILHO DE AÇÃO | Ação |
|---|---|---|---|---|---|
| 1 | **Criativo** | CTR real * | ≥ 1,0% | < 0,6% | Novo hook nos 2 primeiros segundos; criar 2 variantes novas |
| 1b | Criativo | Retenção de 3s | ≥ 30% | < 20% | Cortar a introdução do vídeo |
| 2 | **Funil — entrada** | `ck_landing → ck_start` | 15–30% | < 10% | Encurtar intro / reforçar a promessa |
| 3 | Funil — vídeo | `ck_start → ck_stage (após revelar)` | 60–80% | < 45% | Vídeo pesado? encurtar a contagem do reveal |
| 4 | Funil — resposta | `ck_stage → ck_result` | 80–95% | < 65% | encurtar perguntas (cansaço) |
| 5 | **Oferta** | `ck_result → ck_discount_open` | 45–65% | < 35% | A oferta não conecta com a dor → reescrever oferta/posição |
| 6 | Mecânica | `ck_discount_open → ck_checkout_click` | 60–85% | < 50% | Urgência/escassez fraca → reforçar "só hoje" |
| 7 | **Preço/checkout** | `ck_checkout_click → compra` | 1,5–4% | < 1% (com ≥ 50 cliques) | Fricção no Cakto ou preço — preço é o ÚLTIMO de tudo |

*CTR medido SEM Audience Network, somente placements TikTok.

**Amostra mínima por decisão:** etapas 1–4 → ≥ 30–50 visitas na etapa. Etapa 7 → ≥ 50 `ck_checkout_click` antes de julgar o preço.

---

## 4. Calendário de checkpoints (começa hoje)

| Dia | Momento | O que vale decidir |
|---|---|---|
| **D0–D3** | Fase de aprendizado | ❌ NADA estrutural. Duas únicas exceções: (a) tráfego bot evidente (desligar Pangle), (b) evento de otimização errado (mudar para InitiateCheckout). Todo o resto = COLETAR DADOS. |
| **D3** | Checkpoint 1 | Com ~R$ 50–80 gastos: ler SLEP → diagnosticar gargalo → escolher 1 alavanca da seção 3. Hipótese ANOTADA antes de mexer. |
| **D5** | Checkpoint 2 | A variável mexida reverteu a etapa-alvo? SIM = mantém. NÃO = volta atrás e sobe para a alavanca `n+1` da ordem. |
| **D7** | Sentença | 3 cenários: (A) ≥ 1 venda com CPA ≤ R$ 30 → **ESCALAR** (+20–50% por dia no anúncio vencedor, não na campanha toda); (B) funil até checkout saudável e compra fraca → pixel de compra ausente → conectar pixel no Cakto ANTES de julgar; (C) funil inteiro saudável e zero inits → problema de OFERTA/criativo → novo vértice. |
| **D10+** | Iteração | Máximo 1 mudança por ciclo por nível. Nunca mexer em 2 alavancas no mesmo ciclo. |

---

## 5. Kills e escala (regras duras)

- **PAUSAR criativo:** R$ 15–20 gastos no anúncio sem 1 único `ck_start` → pausa, sem dó.
- **PAUSAR campanha:** R$ 100 gastos (≈ 2× o CPA break-even) sem 1 `ck_checkout_click` real → pausa e reconstrói com outro vértice/ângulo.
- **ESCALAR:** a 1ª venda com CPA ≤ R$ 25 → duplicar o anúncio vencedor em NOVO conjunto de anúncios (não mexer no original) e aumentar orçamento 20% a cada 24h conforme o CPA se mantém.
- **Nunca escalar** com base em 1 dia de sorte: exigir 3 dias consecutivos lucrativos.

---

## 6. Log de decisão (colunas da planilha)

`data | gasto do ciclo | impressões | cliques reais | sessões GA4 | ck_start | ck_result | ck_discount | ck_checkout | compras | CPA | ROAS | VARIÁVEL MEXIDA | hipótese | resultado esperado | veredicto (D+3)`

---

## 7. Ações de hoje (checklist D0)

- [ ] Desligar Pangle/Audience Network na campanha (tráfego bot = CTR 12,8%)
- [ ] Evento de otimização → **InitiateCheckout** (o evento já dispara no site)
- [ ] Pixel TikTok `DBHDHNJC77U4J2JQL880` colado no painel do Cakto (fecha o buraco da `compra`)
- [ ] Nomes dos anúncios → slugs sem espaço (`thirsty-par-v1`) + UTMs aplicadas
- [ ] Planilha do log criada (seção 6) e preenchida com os dados do D0
