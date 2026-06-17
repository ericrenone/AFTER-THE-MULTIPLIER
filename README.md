# AFTER THE MULTIPLIER

## AI Compute Economics, Energy Constraint, and the Arithmetic Substrate Decision: A Five-Year Strategic Outlook · 2026–2031

*ERI Labs Research · June 17, 2026*

---

> **The bottom line, stated once:** The global AI industry is spending $630 billion this year on computing infrastructure built around arithmetic that wastes between two and ten times the energy it needs to. Two alternative substrates — logarithmic (Tensordyne Napier, shipping 2027) and iterative rotation-based (CORDIC-native, demonstrated at research scale) — have now cleared proof-of-concept. The next five years will determine which one captures the ecosystem. The answer will be decided not by which arithmetic is correct, but by which one reaches three-nanometer silicon first, earns safety certification second, and integrates with quantum hardware third. As of June 17, 2026, the logarithmic approach leads on process node. The rotation approach leads on everything else.

---

## Executive Summary

**Five findings that executives should act on now.**

**1. Inference is the new training.** Enterprise AI inference now represents 85% of total AI compute budgets. Per-token costs are falling — Gartner forecasts a 90% reduction by 2030 — but total AI bills are rising because agentic AI consumes five to thirty times more tokens per task than conventional chatbots. The total inference energy bill doubles by 2030 regardless of unit efficiency gains.

**2. The arithmetic substrate is a strategic variable, not a technical detail.** The IEEE 754 floating-point standard ratified in 1985 carries a measured two-to-ten times energy overhead versus purpose-built alternatives on iterative AI workloads. At $630–700 billion in AI CapEx in 2026 alone and $7.6 trillion projected through the mid-2030s, the choice of arithmetic substrate is a board-level energy and cost variable.

**3. Two credible alternatives now exist, with different risk profiles.** Tensordyne's logarithmic Pareto system taped out at TSMC 3nm in June 2026 and ships systems in Q2 2027 — first-mover advantage, process node leadership, no retraining required, $200 million in forecasted orders. CORDIC-native silicon leads on geometric correctness, per-operation error certification, quantum compatibility, and safety-critical deployability — but has not taped out at an advanced process node.

**4. The energy constraint will force the decision.** IEA projects data center electricity consumption doubling to 945 TWh by 2030, with AI-focused data centers tripling. Five leading technology companies spent more than $400 billion in 2025 CapEx — more than global investment in oil and gas production — increasing by 75% in 2026. The pipeline of conditional nuclear agreements between data center operators and small modular reactor projects has grown from 25 gigawatts at end-2024 to 45 gigawatts today. This is unsustainable without a step-change in arithmetic efficiency. The arithmetic substrate decision is an energy policy decision.

**5. The five-year window is 2026–2031, and it closes fast.** Ecosystem lock-in in semiconductors follows the same mechanism that locked in IEEE 754 in 1985: co-fitness. The substrate that accumulates framework support, safety certifications, customer deployments, and foundry commitments first is extremely difficult to displace regardless of technical merit. The window in which a theoretically superior substrate can still compete is narrow and measurable.

---

## Section I — Market Context: The Scale That Makes the Arithmetic Matter

### The Demand Curve

The AI inference chip market reached approximately $106 billion in 2025. It is projected to reach $255 billion by 2030 at a 19.2% compound annual growth rate. Cloud AI inference chips specifically — the datacenter segment — were valued at $45.6 billion in 2025 and are projected to reach $284.9 billion by 2034.

These figures understate the energy economics because they measure hardware revenue, not operating cost. The operating cost structure of inference at scale is dominated by electricity, which represents 35–50% of total cost of ownership and is the only component the arithmetic substrate directly changes. Hardware amortization, cooling, networking, and labor are largely fixed by system architecture; the electricity variable moves with arithmetic efficiency.

### The Energy Ceiling

The IEA's April 2026 analysis establishes the boundary conditions with precision:

- **2025 baseline:** 485 TWh global data center electricity consumption
- **2030 base case:** 945 TWh — doubling in five years
- **AI-focused data centers:** electricity demand tripling in the same period, growing at 30% annually — four times the rate of total global electricity consumption growth
- **U.S. data centers alone:** 183 TWh in 2024, projected 426 TWh by 2030 — a 133% increase

For context: 945 TWh equals the current annual electricity consumption of Japan. Data centers are adding Japan's electricity demand to the global grid in the next four years.

The bottleneck is not political will or financial capital. It is physics and grid infrastructure. Grid connection timelines in the United States average five to seven years for large facilities. The pipeline of nuclear offtake agreements has doubled in eighteen months. The largest technology companies are funding new power generation because they cannot connect to existing grids fast enough.

This is the context in which the arithmetic substrate decision is being made. The question is not whether efficiency matters. The question is which efficiency pathway arrives at scale first, and whether it gets there before the capital is committed.

---

## Section II — The Three-Substrate Landscape

### What Is Currently Running and What Threatens It

| | IEEE 754 (Incumbent) | Pareto / LNS (Tensordyne Napier) | CORDIC-Native |
|--|--|--|--|
| **Process node** | 3nm–7nm at scale | 3nm (taped out June 2026) | 28nm (CARMEN, measured 2026) |
| **Status** | Production at full scale | Tape-out; ships Q2 2027 | Research / demonstrated silicon |
| **Energy vs. IEEE 754** | Baseline (1×) | ~3–4× per-chip gain (simulated) | 2–10× gain (measured at 28nm) |
| **Geometry** | Flat (Euclidean) | Flat (log-scalar, linear accumulation) | Selectable: flat / circular / hyperbolic |
| **Addition handling** | Native, exact | Approximate (99.9% model accuracy) | Not applicable — no log domain used |
| **Multiplication** | Native (expensive — quadratic silicon area) | Eliminated (log domain → addition) | Eliminated (shift-and-add rotation) |
| **Error model** | Population-level benchmark | Population-level (99.9% on tested models) | Per-operation, hardware-certified (2⁻ⁿ per n steps) |
| **Safety certification** | ASIL-D achieved in automotive | Not yet attempted | Structural path demonstrated |
| **Quantum extension** | None | None | O(n)-depth quantum circuits demonstrated |
| **Ships** | Now | Q2 2027 | Not announced at advanced node |

### The Honest Accounting of the Tensordyne Claim

The announced 13× tokens/second and 17× tokens/watt figures against an Nvidia GB300 rack require decomposition. A 288-chip Tensordyne rack operates at equivalent total power to a 72-chip GB300 rack — meaning four times as many chips at matched power. Decomposing the headline numbers:

- **Chip density advantage:** ~4× (more chips at same power)
- **Real per-chip arithmetic gain:** ~3–4× (log-domain multiplication efficiency)
- **Combined system gain:** ~13–16× — consistent with the claim

The per-chip arithmetic gain of 3–4× is real. It is also, as of June 17, 2026, a simulated result derived from pre-silicon models. It has not been measured on fabricated silicon under production workloads. Systems ship Q2 2027, at which point the genuine comparison target will be Nvidia Rubin — not the GB300 used in the benchmark.

The CORDIC-native equivalent: CARMEN's measured 11.67 TOPS/W at 28nm, projected by process node scaling to 35–60 TOPS/W at 3nm. This comparison has not been made because no CORDIC-native chip has taped out at 3nm. That is the single most important gap in the current landscape.

---

## Section III — Phase Analysis: The Five-Year Arc

The five-year period from 2026 to 2031 divides into four phases, each dominated by a different competitive variable.

```
   2026          2027          2028          2029          2030          2031
    │             │             │             │             │             │
    ▼             ▼             ▼             ▼             ▼             ▼
════════════════════════════════════════════════════════════════════════════
PHASE 1           │ PHASE 2              │ PHASE 3          │ PHASE 4
Node Advantage    │ Geometry Reckoning   │ Safety & Quantum │ Consolidation
════════════════════════════════════════════════════════════════════════════
Pareto leads:     │ Pareto constrained:  │ CORDIC leads:    │ Winner defined
3nm, first-mover, │ flat accumulation    │ ASIL-D cert,     │ by which prior
ecosystem seeding │ vs. hyperbolic models│ quantum overlap  │ phases resolved
════════════════════════════════════════════════════════════════════════════
```

### Phase 1 (2026–2027): The Process Node Window

Tensordyne's Napier is first to market with non-IEEE-754 arithmetic at an advanced process node. The measured results, when they arrive in late 2027, will calibrate the real efficiency gap versus simulation claims and versus the Rubin architecture. First-mover advantage in enterprise inference infrastructure is substantial but not permanent: switching costs for inference infrastructure are lower than for training infrastructure, because inference racks can be replaced on a 2–3 year cycle versus training infrastructure on a 4–5 year cycle.

The critical question for Phase 1: how quickly does Pareto's software ecosystem close around PyTorch, Triton, and the major serving frameworks? Software lock-in is faster and more durable than hardware lock-in.

### Phase 2 (2027–2028): The Geometry Reckoning

Researchers at NeurIPS 2025 demonstrated that a billion-parameter language model running in hyperbolic space outperforms its Euclidean counterpart on standard reasoning benchmarks. Two independent groups confirmed that production language models organize their internal representations in negatively curved (hyperbolic) space. Agentic AI — the dominant inference workload growth driver, consuming 5–30× more tokens per task — is structurally hierarchical and therefore structurally hyperbolic.

Tensordyne's Pareto accumulates in flat Euclidean space. This is architecturally correct for conventional transformer workloads. It is architecturally suboptimal for the workloads that are growing fastest. By 2028, the geometry constraint will be measurable in benchmark results on agentic and multi-step reasoning tasks.

The Phase 2 trigger: a published benchmark showing >15% performance advantage of geometry-native inference (CORDIC m=−1 or Lorentz-equivariant) versus flat-geometry inference on an agentic task suite. This benchmark does not exist yet. It will.

### Phase 3 (2028–2030): The Safety and Quantum Wedge

**Safety:** Automotive AI at ASIL-D safety levels requires hardware-certified convergence — per-inference verification that the computation has reached the required precision under actual operating conditions. This is architecturally different from population-level model accuracy. CORDIC's iterative structure enables this certification; Pareto's fixed-depth approximation does not. The autonomous vehicle market at scale — BYD at 500,000+ monthly production with ASIL-D certified silicon, Tesla with 7 million deployed compute platforms facing replacement cycles — creates a procurement requirement that safety-certifiable iterative arithmetic satisfies and fixed-depth approximation currently does not.

**Quantum:** The Anderon foundry (Albany, New York, $2 billion capitalization, 300mm quantum wafer process, announced May 21, 2026) represents the first dedicated quantum chip foundry in the United States. By 2030, quantum-classical hybrid workloads will exist in production for specific application classes. CORDIC's Walther iteration maps to quantum gate sequences at O(n) depth; logarithmic arithmetic has no quantum analogue. This is the third leg of CORDIC's structural advantage — and the one with the longest lead time.

### Phase 4 (2030–2031): Consolidation

By 2031, the arithmetic substrate landscape consolidates around one or two dominant approaches. The consolidation criteria, in order of market force:

1. Which substrate achieves the lowest total cost of ownership per token at 2030 electricity prices?
2. Which substrate supports safety-certified automotive and edge inference at volume?
3. Which substrate runs next-generation geometry-aware AI models at native performance?
4. Which substrate integrates with quantum-classical hybrid workloads?

No current analysis gives Pareto the structural lead on criteria 2, 3, or 4. Pareto leads on the precondition for criterion 1: being in production. The race is between Pareto capturing ecosystem lock-in before the geometry and safety requirements scale, and CORDIC-native reaching an advanced process node before lock-in is irreversible.

---

## Section IV — The Economics of Arithmetic at $7.6 Trillion Scale

### The Arithmetic Tax

The IEEE 754 energy overhead — two to ten times versus purpose-built alternatives on iterative AI workloads — translates directly to a dollar figure at current AI CapEx levels.

At Goldman Sachs's estimate of $7.6 trillion in cumulative AI CapEx through the mid-2030s, and applying the midpoint four-times overhead estimate from Luo et al. (2019), the implied arithmetic tax embedded in the global AI infrastructure build is approximately **$2.3 trillion** in excess energy and cooling cost over the build cycle. This figure represents the economic incentive for arithmetic substrate transition — the present-value prize available to the substrate that displaces IEEE 754.

Neither Pareto nor CORDIC-native captures this prize fully. Both capture a portion determined by their respective efficiency gains and deployment scale.

### Token Economics and the Efficiency Race

Gartner's 90% forecast reduction in frontier model inference cost per token by 2030 distributes across five levers:

| Lever | Estimated Contribution |
|-------|------------------------|
| Model architecture improvements | 30–40% |
| Hardware generation advances | 20–30% |
| Quantization and precision reduction | 15–20% |
| **Arithmetic substrate improvement** | **10–20%** |
| Utilization and software optimization | 10–15% |

The arithmetic substrate lever is unique: it is the only lever that affects the physics of computation itself. Every other lever organizes, compresses, or schedules computation more efficiently. The arithmetic substrate determines how much energy each individual computation actually requires. Its efficiency gain is therefore multiplicative with every other lever, not additive.

### The EV Range and Carbon Dividend: Currently Unbooked

IBM Research's 2026 finding establishes a conversion rate: a 20% reduction in inference chip power consumption produces a 3–5% increase in EV driving range. Applied to arithmetic substrate improvement:

At NeuEdge trajectory levels (sub-1W edge inference versus current FSD-class chips at 50–100W), the implied power reduction is 80–90%. IBM's conversion rate extended linearly implies 12–20% range increase. At 900,000+ monthly EV production (BYD and Tesla combined), this is a fleet-level energy and carbon variable.

**None of this appears in any published life cycle assessment for electric vehicles. No LCA standard reserves for it. No carbon accounting framework captures it.**

The same gap applies to inference chip replacement cycle embodied carbon: approximately 7 million Tesla HW3 vehicles carry chips now obsolete for autonomous driving capability. Their replacement generates semiconductor fabrication embodied carbon — mining, refining, fabrication, assembly — that is absent from every published EV carbon accounting model.

The regulatory closure of these gaps — expected within three to five years as EU taxonomy updates, California SB standards, and IPCC Working Group III mitigation accounting mature — will create a retroactive carbon liability for the fleet arithmetic choices made in 2026–2028.

---

## Section V — Scenario Analysis: Three Futures for 2031

### Scenario A — Log Lock-In (35% probability)

Tensordyne's Napier delivers measured results within 80% of simulated claims. Hyperscalers adopt Pareto-native inference infrastructure. The software ecosystem consolidates around Pareto number formatting before geometry-native chips reach an advanced node. By 2029, Pareto is the de facto non-IEEE-754 standard for large language model inference.

The geometry problem is deferred: hyperbolic AI models grow in academic influence but lag in production deployment. Next-generation model architectures are designed around Pareto's Euclidean accumulation constraint rather than demanding geometrically correct hardware.

**Energy outcome:** 3–4× improvement over IEEE 754 per chip at 3nm. IEA base case energy trajectory slows but does not reverse. Nuclear and gas generation for data centers proceeds as planned.

**Strategic implication:** Invest in Pareto-native software tooling and inference infrastructure. Treat CORDIC-native as a long-dated option on safety-critical and quantum workloads.

### Scenario B — Substrate Race (45% probability)

Tensordyne ships Napier in 2027 with measured performance somewhat below simulation claims — the historical norm. A CORDIC-native chip tapes out at 3–5nm in late 2026 or 2027, motivated by the Tensordyne announcement demonstrating market appetite for non-IEEE-754 silicon. Two substrates coexist: Pareto captures datacenter LLM inference; CORDIC-native captures automotive, safety-critical edge, and early quantum-classical hybrid workloads. The market bifurcates.

**Energy outcome:** Combined effect — Pareto in datacenter, CORDIC-native in edge and automotive — produces 4–6× overall improvement versus IEEE 754 status quo. This is the scenario in which the IEA base case projections are materially beaten.

**Strategic implication:** Hold positions in both substrates. The bifurcation creates two distinct procurement criteria: density and throughput (Pareto) versus certification and geometry (CORDIC). Enterprises with both datacenter and automotive exposure need both.

### Scenario C — Geometry Wins (20% probability)

Hyperbolic AI models demonstrate dramatically superior performance on agentic and reasoning tasks by 2028–2029, with gaps large enough to override ecosystem inertia. A CORDIC-native chip reaches 3nm with a major hyperscaler or sovereign AI program as anchor customer. The geometry advantage in agentic AI — where multi-step reasoning over hierarchical knowledge structures is the dominant workload — creates demand pull that overcomes Pareto's first-mover advantage.

**Energy outcome:** CORDIC-native at 3nm — projecting 35–60 TOPS/W — is the scenario in which the energy constraint is most decisively addressed and the carbon dividend of arithmetic substrate change becomes quantifiable at civilizational scale.

**Strategic implication:** Invest now in the research supply chain: hyperbolic model architectures, CORDIC-native PDK development, and the mathematical infrastructure (Lorentzian inference, convergence certification) that CORDIC's architectural depth enables and Pareto's does not.

---

## Section VI — Strategic Imperatives by Stakeholder

### Hyperscalers and Cloud Providers

**Now (2026–2027):** Run controlled Pareto pilots on current LLM inference workloads. Do not commit full inference infrastructure before measuring Napier silicon against Rubin. Maintain optionality on CORDIC-native by tracking tape-out announcements. The switching cost between inference chip architectures is lower than widely assumed — inference racks turn over faster than training infrastructure.

**Near-term (2027–2029):** Benchmark both substrates on agentic workloads as they scale. The first measurable performance gap between flat-geometry and geometry-native inference on multi-step reasoning will be the decisive inflection point. The enterprise that identifies this gap two quarters earlier than competitors captures meaningful cost and quality advantage.

**Strategic (2029–2031):** Architect your quantum-classical hybrid compute roadmap before committing arithmetic substrate for the decade. Only one of the two alternatives has a quantum extension. This is not yet a product requirement. It will become one.

### Automotive OEMs and Tier-1 Suppliers

**Now:** The EV inference chip power budget is a carbon accounting variable not captured in any current life cycle assessment. Begin working with LCA standards bodies (ISO, SAE, EU taxonomy technical working groups) to insert chip replacement cycle and arithmetic efficiency into EV carbon accounting frameworks. First movers in this accounting will define the standard rather than comply with it.

**Near-term:** Evaluate CORDIC-native edge inference chips for safety-critical autonomy. The convergence certificate — hardware-level verification that inference has reached required precision before an irrevocable action commits — is a structural requirement for ASIL-D that fixed-depth approximation architectures do not currently satisfy.

**Strategic:** The arithmetic substrate of the autonomy chip is not a silicon team decision. It affects driving range (IBM 2026 conversion rate: 20% efficiency gain = 3–5% range), lifetime carbon footprint (chip replacement cycle embodied carbon), and safety certification (ASIL-D convergence requirement). Escalate the substrate decision to the level of authority appropriate to those stakes.

### AI Chip Investors

**The Pareto position:** First-mover at 3nm, $200M+ in forecasted orders, validated software pipeline, no retraining requirement. Primary risks: simulation-versus-measured-silicon gap (2027 validation event); geometry limitation becoming a product requirement gap (2028 inflection); Rubin as the actual comparison benchmark; safety certification timeline unknown. A 2027 validation-dependent medium-conviction position.

**The CORDIC-native position:** Superior mathematical properties on every dimension that will matter most in 2028–2031. Primary risk: ecosystem timing — Pareto may achieve lock-in before CORDIC reaches an advanced node. Catalysts: 3nm tape-out announcement; ASIL-D certification achievement; major hyperscaler or sovereign AI anchor customer announcement. A long-dated option with asymmetric upside if any of three independent catalysts fires.

**The structural position:** The transition from IEEE 754 — in whichever direction — is the largest architectural efficiency opportunity in semiconductors since the RISC/CISC transition of the 1990s. Companies holding positions in the enabling infrastructure — TSMC advanced packaging, HBM4 memory, Anderon-class quantum foundries — benefit regardless of which arithmetic wins. The substrate race creates demand; the demand benefits the infrastructure layer.

### Energy and Climate Policymakers

**The unbooked items that regulation will close within five years:**

| Item | Current Accounting Status | Regulatory Closure Likely By |
|------|--------------------------|------------------------------|
| AI arithmetic substrate energy overhead vs. CORDIC baseline | Not in any AI emissions framework | 2028–2029 (EU AI Act implementing measures) |
| EV inference chip power vs. battery range tradeoff | Not in any LCA standard | 2028 |
| EV compute chip replacement cycle embodied carbon | Not in any LCA standard | 2029 |
| Climate attribution model geometric error (Euclidean vs. hyperbolic) | Not recognized as a carbon variable | 2030 |

Each item, when captured, creates a retroactive accounting adjustment for infrastructure decisions made between 2026 and 2029. Companies and countries making those decisions now are accruing unbooked liabilities. Policymakers who define the standards will shape the incentive structure of a $7.6 trillion capital deployment.

---

## Section VII — Five Predictions with Measurable Triggers

| # | Prediction | Measurable Trigger | Timeline |
|---|-----------|-------------------|----------|
| **P1** | Measured Napier silicon delivers 8–11× total rack gain versus GB300 (not 13–17×), reflecting simulation-to-silicon gap and density decomposition | First customer benchmark publication | Q3–Q4 2027 |
| **P2** | A CORDIC-native AI inference chip tapes out at 5nm or better before end of 2027, motivated by Tensordyne's market signal | Named tape-out announcement by a fabless designer or research institution | 2027 |
| **P3** | A published benchmark shows >15% performance advantage of geometry-native inference over flat-geometry inference on an agentic task suite, making hyperbolic hardware a procurement criterion | Published result from a top-5 AI research institution or hyperscaler | 2028 |
| **P4** | The first EV life cycle assessment incorporating inference chip arithmetic efficiency is published, creating a new line item in automotive carbon accounting | Publication by an OEM, standards body, or regulatory agency | 2028–2029 |
| **P5** | CORDIC-native or Lorentz-equivariant inference silicon achieves ASIL-D certification before Pareto does, establishing safety-critical inference as CORDIC-native territory | Certified ASIL-D product announcement for an iterative-architecture inference chip | 2029 |

---

## Section VIII — The Decision Map

### Where to Invest Now for 2031 Position

```
              STRATEGIC POSITIONING MATRIX · 2026–2031
              BASED ON GEOMETRY REQUIREMENT × SAFETY REQUIREMENT

                              GEOMETRY REQUIREMENT
                     LOW (flat transformer workloads)  HIGH (agentic / hierarchical)
                ┌─────────────────────────────────────┬──────────────────────────────┐
  SAFETY   LOW  │  PARETO / LNS                       │  GEOMETRY-NATIVE CORDIC      │
  REQUIRE- │    │  Clear winner, 2027–2028             │  Required by 2028–2029       │
  MENT     │    │  Invest: Tensordyne ecosystem,       │  Invest: HELM-class model    │
           │    │  Pareto software compatibility,      │  development + CORDIC        │
  (data-   │    │  inference infrastructure            │  silicon pipeline            │
  center   │    │                                     │                              │
  LLM)     │    │  Risk: geometry ceiling 2028         │  Risk: node timing vs.       │
           │    │                                     │  Pareto lock-in              │
           ├────┼─────────────────────────────────────┼──────────────────────────────┤
  HIGH     │    │  CORDIC-NATIVE REQUIRED             │  CORDIC-NATIVE REQUIRED      │
           │    │  Convergence certificate is          │  Full stack:                 │
  (auto-   │    │  a structural ASIL-D requirement.   │  geometry-correct +          │
  motive,  │    │  Pareto's fixed-depth approx.       │  safety-certifiable +        │
  medical, │    │  currently cannot satisfy it.       │  quantum-extensible.         │
  safety-  │    │  Invest: CORDIC edge silicon,        │  The strongest long position │
  critical)│    │  ASIL-D certification path          │  in the five-year horizon    │
           └────┴─────────────────────────────────────┴──────────────────────────────┘

  NOTE: Quantum extension available only in right-column (CORDIC-native) quadrants.
  NOTE: Process node lead as of June 17, 2026 sits in the Pareto quadrants.
  NOTE: The top-right quadrant is the fastest-growing workload category (agentic AI).
```

---

## The One-Page Summary

The global AI industry has reached the point where the choice of arithmetic is a strategic variable. The IEEE 754 standard — a reasonable choice in 1985 — carries a two-to-ten times energy penalty on the workloads that define 2026 compute. Two alternatives have cleared proof-of-concept.

**Logarithmic arithmetic (Tensordyne Napier)** ships first, at the most advanced process node, with no retraining requirement. Its per-chip arithmetic gain is real at approximately 3–4×. Its limitation is geometric: accumulation in flat Euclidean space is the wrong structure for hierarchical and causal AI models — the models growing fastest. It has no convergence certificate for safety-critical applications and no quantum extension.

**CORDIC-native arithmetic** is geometrically correct, certifiable per-operation, quantum-extensible, and projects to 35–60 TOPS/W at three nanometers by node-scaling. It leads on every technical dimension that will matter most in 2028–2031. It trails on the dimension that matters most today: it has not taped out at an advanced node.

The energy constraint — data center electricity doubling by 2030, AI-focused demand tripling, five technology companies outspending the oil industry on capital expenditure, nuclear power plants being commissioned to serve data centers — will force a decision regardless of technical preference. Either the arithmetic gets more efficient or the lights go off.

The arithmetic will get more efficient. The question is which arithmetic and when. That question has a five-year window, a measurable set of trigger events, and a $7.6 trillion capital structure riding on the answer.

The window opened June 15, 2026, when Tensordyne announced its tape-out.

It will not stay open indefinitely.

---

## Primary Sources

| Source | Date | Key Figure |
|--------|------|-----------|
| IEA, *Key Questions on Energy and AI* | April 2026 | Data center electricity 485 TWh (2025) → 945 TWh (2030); AI-focused tripling |
| IEA, Data Centre Electricity Surge | April 2026 | Tech CapEx exceeded $400B in 2025; rising 75% in 2026; nuclear pipeline 45 GW |
| Gartner | March 2026 | 90% reduction in frontier model inference cost per token by 2030 |
| Goldman Sachs | 2026 | $7.6T cumulative AI CapEx; $630–700B in 2026 |
| MarketsandMarkets | 2026 | AI inference market: $106B (2025) → $255B (2030); 19.2% CAGR |
| Intel Market Research | April 2026 | Inference AI chip market $20.4B (2026) → $85.8B (2034); 27.8% CAGR |
| AnalyticsWeek | 2026 | Inference now 85% of enterprise AI compute budget |
| Brookings Institution | April 2026 | U.S. data centers: 183 TWh (2024) → 426 TWh (2030); +133% |
| Luo et al. | IEEE TVLSI, 2019 | 2–10× energy overhead: IEEE 754 vs. CORDIC-native on iterative workloads |
| Kumar et al. (CARMEN) | arXiv:2605.06878, June 2026 | 4.83 TOPS/mm², 11.67 TOPS/W CORDIC-for-AI at 28nm CMOS |
| SYCore | arXiv:2503.11685, Mar 2025 | Systolic CORDIC: 4.64× throughput, 5.02× power reduction |
| NeuEdge | arXiv:2602.02439, Feb 2026 | Sub-1W edge inference; 4.7× efficiency gain |
| He et al. (HELM) | arXiv:2505.24722, NeurIPS 2025 | Hyperbolic LLM outperforms Euclidean at billion-parameter scale; MMLU, ARC |
| Robinson, Dey & Sweet | arXiv:2410.08993 (2024); arXiv:2504.01002 (2025) | Negative Ricci curvature confirmed in production LLM embeddings |
| ILNN | arXiv:2602.23981, ICLR 2026 | Fully intrinsic Lorentz architecture; eliminates all Euclidean operations |
| Fast Lorentz NNs | arXiv:2601.21529, Jan 2026 | Lorentz distance in two CORDIC operations |
| Burge et al. | arXiv:2411.14434, 2024 | Quantum CORDIC circuits at O(n) depth on quantum hardware |
| Safe-NEureka | arXiv:2602.04803, Feb 2026 | 24-cycle hardware fault recovery; ASIL-D certification structural path |
| IBM Research | 2026 | 20% inference power = 3–5% EV range increase |
| IBM / U.S. DoC (Anderon) | May 21, 2026 | $2B quantum foundry; Albany, NY; 300mm quantum wafer; 45 GW nuclear pipeline |
| BYD Xuanji A3 | May 28, 2026 | 4nm, 2,100 TOPS, ASIL-D; new automotive inference benchmark |
| Tensordyne announcement | June 15, 2026 | Napier tape-out; TSMC 3nm; 300W; 138B transistors; $200M+ forecasted orders |
| Tensordyne / NextPlatform | June 16, 2026 | 48 cores, 128×128 systolic arrays; novel accumulator; cloud access end 2026 |
| Tensordyne / Recogni | August 2024 | Pareto: 99.9% vs. FP16 accuracy on Mixtral, Llama, Falcon, Stable Diffusion |
| Hooker, S. | CACM 2020 | Hardware co-fitness determines research direction survival — the lottery mechanism |
| Bérczi & Kiem | arXiv:2605.29151, May 2026 | CORDIC iterations isomorphic to M̄₀,ₙ forgetting maps — convergence certificate mathematical grounding |
| Volder, J. | IRE Trans. Electronic Computers, 1959 | CORDIC: shift-and-add computes all transcendental functions iteratively |
| Walther, J. | AFIPS SJCC, 1971 | Three-mode CORDIC: circular / flat / hyperbolic |
| Mitchell, J.N. | IRE Trans. Electronic Computers, 1962 | Mitchell approximation: log₂(1+x) ≈ x — the founding idea Pareto corrects |
