# SOP — Decisões de Mídia (Confere)

> DEFINITION OF WINNER = Oferta com ROI positivo escalada dando lucro.
> Regra de ouro: **SEMPRE 1 variável por ciclo**. Ciclo = 48–72h OU ~R$ 60–80 de spend, o que ocorrer primeiro.

---

## 1. Fundamento: a matemática da vitória

| Indicador | Valor | Como calcular |
|---|---|---|
| Preço na página | R$ 50,89 | tabelado |
| Receita líquida pós-Cakto | ~R$ 44–47 | preço − (fee Cakto + taxa fixa) |
| **CPA break-even** | **~R$ 40–45** | acima disso = perde dinheiro |
| **CPA alvo (lucro)** | **≤ R$ 25** | ~50% de margem |
| Conversão necessária (matemática reversa) | Com CPM R$ 7 → R$ 50 = ~7.300 impr. Com CTR 1% → ~73 clicks. Se → checkout 5% e purchase 3% → CPA ≈ **R$ 23** | dá lucro |
| Implicações | Se CPA ≤ R$ 25 o funil matemático fecha | cheque aderência etapa por etapa |

**Hit de compra:** R$ 50 ≈ 7.000 impressões com esse CPM.

---

## 2. Ordem de leitura do gargalo (SLEP)

`S`pend → `L`anding → Etapas → `P`urchase. Antes de tocar em qualquer alavanca:
1. **O clique é humano?** (CTR > 3% + CPC < R$ 0,15 = suspeita → desligar Pangle/Audience Network)
2. **GA4 mostra sessões ≈ clicks?** (se < 60% → tráfego junk → placements, não criativo)

---

## 3. Tabela de decisão por etapa (gatilhos numéricos)

| # | Alavanca | Métrica | Saudável | GATILHO DE AÇÃO | Ação |
|---|---|---|---|---|---|
| 1 | **Criativo** | CTR real * | ≥ 1,0% | < 0,6% | Novo hook nos 2s iniciais; 2 variantes novas |
| 1b | Criativo | Retenção 3s | ≥ 30% | < 20% | Cortar intro do vídeo |
| 2 | **Funil — entrada** | `ck_landing → ck_start` | 15–30% | < 10% | Encurtar intro / reforçar promessa |
| 3 | Funil — vídeo | `ck_start → ck_handle_submit` | 60–80% | < 45% | Pergunta difícil cedo demais? mover @ para depois |
| 4 | Funil — weight | `ck_handle_submit → ck_result` | 80–95% | < 65% | Enxugar perguntas (fatigue) |
| 5 | **Oferta** | `ck_result → ck_discount_open` | 45–65% | < 35% | Oferta não conecta com a dor → reescrever oferta/exposição |
| 6 | Mecânica | `ck_discount_open → ck_checkout_click` | 60–85% | < 50% | Urgência/escassez fraca → reforçar "só hoje" |
| 7 | **Preço/checkout** | `ck_checkout_click → purchase` | 1,5–4% | < 1% (com ≥ 50 clks) | Fricção no Cakto ou preço → testar offer bump/Pix; preço é o ÚLTIMO a alterar |

*CTR medido sem Audience Network / somente placements TikTok.

**Amostra mínima por decisão:** etapa 1–4 → ≥ 30–50 visitas na etapa. Etapa 7 → ≥ 50 `ck_checkout_click` antes de julgar preço.

---

## 4. Calendário de checkpoints (comecet hoje)

| Dia | Gate | O que vale decidir |
|---|---|---|
| **D0–D3** | Fase de aprendizado | ❌ NADA estrutural. Só 2 exceções permitidas: (a) tráfego bot/junk evidente (desligar Pangle), (b) evento de otimização errado (mudar p/ InitiateCheckout). Tudo mais = COLETAR. |
| **D3** | Checkpoint 1 | Com ~R$ 50–80 investidos: leia SLEP → diag. gargalo → escolha 1 alavanca (seção 3). Hipótese ANOTADA antes de mexer. |
| **D5** | Checkpoint 2 | Comprar: a variável mexida reverteu a etapa-alvo? SIM = mantém. NÃO = volta atrás e sobe para alavanca `n+1` na lista. |
| **D7** | Sentença | 3 cenários: (A) ≥ 1 venda com CPA ≤ R$ 30 → **escalada** (+20–50%/dia na ad vencedora, não na campanha toda); (B) dados de até `ck_checkout_click` bons, purchase fraco → trava = evento de compra ausente → conecta pixel no Cakto ANTES de julgar; (C) funnel inteiramente padrão saudável e zero inits → problema é OFERTA/creative match → novo vértice. |
| **D10+** | Iteração | Máx. 1 ciclo viral/dia por nível. Never toça 2 levers naquele mesmo ciclo. |

---

## 5. Kills & escala (regras duras)

- **KILL criativo:** R$ 15–20 investidos no ad sem 1 `ck_start` → pausa sem dó.
- **KILL campanha:** R$ 100 investidos (≈ 2× CPA break-even) sem 1 `ck_checkout_click` real → pausa całownia e reconstrói com outro vértice.
- **ESCALA:** a 1ª venda com CPA ≤ R$ 25 → duplica o anúncio vencedor em novo ad set (não mexe no original) e aumenta 20% a cada 24h-based no CPA.
- **Nunca escale** em CPAs flicos/dia único: exige 3 dias consecutivos lucrativos.

---

## 6. Log de decisão (colunas do controle)

`data | spend do ciclo | impressões | clicks reais | sessões GA4 | ck_start | ck_result | ck_discount | chk_click | purchases | CPA | ROAS | VARIAVEL MEXIDA | hipótese | resultado esperado | veredicto (D+3)`

---

## 7. Hoje (lista de koniecz działania imediata)

- [ ] Desligar Pangle/Audience Network na campanha (tráfego bot = CTR 12,8%)
- [ ] Evento de otimização → **InitiateCheckout** (o evento já dispará no site)
- [ ] Pixel TikTok `DBHDHNJC77U4J2JQL880` colado no painel do Cakto (fecha o buraco `purchase`)
- [ ] Nomes dos anúncios → slugs sem espaço (`thirsty-par-v1`) + UTMs aplicadas
- [ ] Aba do log criada (seção 6) -a preenchida com os dados de D0.
