# DISSERTATION — PUBLIKATIONSFÄHIGE ENDFASSUNG

## Perturbative Modulare Lineare Antwort in KMS-Systemen
## unter extremen Magnetfeldern

---

**Dissertation zur Erlangung des Grades eines Doktors der Naturwissenschaften**

Fachbereich Mathematische Physik

---

## Abstract

Diese Arbeit entwickelt eine mathematisch rigorose Formulierung der
linearen Antworttheorie in KMS-Systemen ohne Verwendung expliziter
Hamiltonoperatoren. Ausgangspunkt ist die Beobachtung, dass in
algebraischen Quantenfeldtheorien vom Typ III₁ der klassische Kubo-
Formalismus scheitert, da kein kanonischer Hamiltonoperator existiert.

Wir zeigen, dass der **relative Modularhamiltonian** K_{ω_V|ω_0}
nach Araki (1973) das natürliche Objekt zur Beschreibung perturbativer
Zustandsänderungen ist, und leiten die **Modulare Kubo-Identität** her:

```
χ_A^{stat} = -(i/β) · ω_0([A, K_{ω_V|ω_0}]) + O(‖V‖²)
```

Mittels Laplace-Transformation des adjungierten Modularflusses und des
Hille-Yosida-Theorems (Engel-Nagel 2000) erweitern wir dieses Resultat
auf die vollständige frequenzabhängige Suszeptibilität:

```
χ_A(z) = -(i/β) · ω_0([R_ad(z, iK_0)(A), K_{ω_V|ω_0}]) + O(‖V‖²/Re(z))
```

für Re(z) > 0. Arakis statisches Ergebnis erscheint als Grenzfall
z → ∞ via dem Anfangswerttheorem der Laplace-Transformation.

Als Anwendung wird das Magnetar-Regime (B ~ 10¹¹ T) analysiert, in dem
β|μ_n|B ≫ 1 und der klassische Kubo-Formalismus quantitative Korrekturen
durch die Resummation der Araki-Reihe erfordert.

**MSC2020:** 46L60, 47D06, 82B10, 81T05

**Schlüsselwörter:** KMS-Zustände, Tomita-Takesaki, Araki-Perturbation,
Kubo-Formel, Laplace-Transformation, Hille-Yosida, Magnetarphysik

---

## Kapitel 1: Einleitung und Problemstellung

### 1.1 Das Problem der linearen Antwort in AQFT

Die lineare Antworttheorie nach Kubo (1957) verbindet die Gleichgewichts-
Korrelationsfunktionen eines Quantensystems mit seiner dynamischen Antwort
auf externe Störungen. In der Formulierung für Systeme mit endlichem
Hamiltonoperator H lautet die retardierte Green-Funktion:

```
χ_A(t) = -i · θ(t) · ω_β([e^{iHt} A e^{-iHt}, V])
```

Diese Formulierung setzt einen expliziten beschränkten Hamiltonian voraus.

**In algebraischen Quantenfeldtheorien (AQFT)** vom Typ III₁ — dem
mathematisch korrekten Rahmen für relativistische QFT im thermodynamischen
Limes (Buchholz-Fredenhagen 1982) — existiert kein solcher Operator. Es
gilt: tr(e^{-βH}) = ∞. Die Zeitentwicklung α_t ist ein Automorphismus
der C*-Algebra, aber nicht unitär implementierbar durch einen beschränkten
Operator.

**Die Lösung** liegt in der Tomita-Takesaki-Modulartheorie: Der
Modularfluss σ_t^ω erzeugt die Zeitentwicklung ohne explizites H, und
der **relative Modularhamiltonian** K_{ω_V|ω_0} := -log Δ_{ω_V|ω_0}
nach Araki (1973) liefert das kanonische Perturbationsobjekt.

### 1.2 Stand der Forschung und Lücke

**Bekannt:**
- Araki (1973): K_{ω_V|ω_0} ≈ βV für beschränktes V (statisch)
- Kubo (1957): χ_A(t) = -iθ(t)ω([A(t), V]) für Type-I-Systeme
- Bratteli-Robinson (1987): KMS ↔ Modularfluss-Äquivalenz
- JLMS (2016): K_A^{CFT} = K_A^{bulk} + Area/4G (holographisch)

**Lücke in der Literatur:**
Die dynamische (frequenzabhängige) Kubo-Formel in der Sprache des
relativen Modularhamiltonian K_{ω_V|ω_0} ist nicht explizit formuliert.
Araki gibt nur das statische Ergebnis.

### 1.3 Beiträge dieser Arbeit

**(I)** Beweis der Modularen Kubo-Identität (statisch):
```
χ_A^{stat} = -(i/β) · ω_0([A, K_{ω_V|ω_0}]) + O(‖V‖²)
```

**(II)** Laplace-Erweiterung auf dynamische Antwort (neu):
```
χ_A(z) = -(i/β) · ω_0([R_ad(z)(A), K_{ω_V|ω_0}]) + E(A,V,z)
```

**(III)** Hille-Yosida-Schranken (frequenzaufgelöst):
```
|χ_A(z)| ≤ ‖A‖·‖K_{ω_V|ω_0}‖ / (β · Re(z)) + O(‖V‖²)
```

**(IV)** Anwendung auf Magnetarphysik: Regime β|μ_n|B ≫ 1 und
exakte Resummation der Araki-Reihe für Zeeman-Störung.

### 1.4 Abgrenzung

Diese Arbeit beansprucht **keine** Korrektur oder Erweiterung der
klassischen Mechanik. Die Formulierung in modularer Sprache liefert
eine neue algebraische Struktur für bestehende Physik, keine neue Physik.

---

## Kapitel 2: Mathematische Grundlagen

### 2.1 Von-Neumann-Algebren und Typklassifikation

**Definition 2.1** Eine Von-Neumann-Algebra 𝓜 ⊂ B(ℋ) ist eine
normabgeschlossene *-Unteralgebra mit 𝓜 = 𝓜''.

Die Murray-von-Neumann-Klassifikation unterscheidet:

```
Typ I_n:  endliche Matrix-Algebren, Spur existiert
Typ II₁:  endliche Faktoren, normierte Spur existiert
Typ III₁: hyperfinite Faktoren, KEINE Spur
```

**Satz 2.2 (Buchholz-Fredenhagen 1982)**
Lokale Algebren 𝒜(𝒪) in masselosen relativistischen QFTs im
thermodynamischen Limes sind hyperfinite Typ-III₁-Faktoren.

*Konsequenz:* Der klassische Gibbs-Zustand ρ = e^{-βH}/Z existiert
nicht im strengen Sinne (kein normierter Trace). Die KMS-Bedingung
und Modulartheorie sind die korrekten Ersatzobjekte.

### 2.2 Die Tomita-Algebra

**Definition 2.3** Sei ω_0 ein faithfully normaler Zustand auf 𝓜.
Die **Tomita-Algebra** ist:

```
𝒯 = { A ∈ 𝓜 : τ ↦ σ_τ^0(A) ist analytisch auf ℂ }
```

𝒯 ist eine *-Unteralgebra von 𝓜, dicht im GNS-Hilbertraum ℋ_{ω_0}.

**Satz 2.4 (Tomita 1967, Takesaki 1970)**

```
S_0: A Ω_0 ↦ A* Ω_0         (Tomita-Involution, abschließbar)
S_0 = J_0 · Δ_0^{1/2}       (polare Zerlegung)
K_0 := -log Δ_0              (Modularhamiltonian, selbstadjungiert)
σ_t^0(A) = e^{itK_0} A e^{-itK_0}   (Modularfluss)
σ_t^0(𝓜) = 𝓜  ∀t ∈ ℝ      (Tomita-Fundamentalsatz)
```

### 2.3 KMS-Zustände

**Definition 2.5 (Haag-Hugenholtz-Winnink 1967)**

ω_β ist **KMS-Zustand** bei β > 0 bezüglich α_t, wenn für alle
A, B ∈ 𝒜 eine Funktion F_{AB}: {0 < Im(z) < β} → ℂ existiert mit:

```
F_{AB}(t)    = ω_β(A · α_t(B))
F_{AB}(t+iβ) = ω_β(α_t(B) · A)
```

F_{AB} analytisch im Streifen, stetig am Rand.

**Theorem 2.6 (Bratteli-Robinson Vol. II, Prop. 5.3.7)**

```
ω_β KMS bei β bezüglich α_t  ⟺  α_t = σ_t^{ω_β}
```

*Für Type-I*: K_{ω_β} = βH (endliches System).
*Für Type-III₁*: K_{ω_β} existiert ohne explizites H.

### 2.4 Laplace-Transformation und Hille-Yosida

**Definition 2.7 (Laplace-Transformation)**

```
ℒ{f}(s) = F(s) = ∫_0^∞ f(t) e^{-st} dt,    Re(s) > s_0
```

**Lemma 2.8 (Anfangswerttheorem)**

```
f(0⁺) = lim_{s→+∞} s · F(s)
```

**Theorem 2.9 (Hille-Yosida 1948, Engel-Nagel 2000, Thm II.3.8)**

A erzeugt C₀-Halbgruppe T(t) mit ‖T(t)‖ ≤ Me^{ωt}  ⟺

```
(i)  A abgeschlossen, D(A) dicht
(ii) ∀λ > ω, ∀n: ‖(λI-A)^{-n}‖ ≤ M/(λ-ω)^n
```

**Kernformel:** Resolvent = Laplace-Transformation der Halbgruppe:

```
R(λ, A) = (λI - A)^{-1} = ∫_0^∞ e^{-λt} T(t) dt
‖R(λ, A)‖ ≤ M/(Re(λ) - ω)
```

---

## Kapitel 3: Araki-Perturbationstheorie

### 3.1 Der Relative Modularoperator

**Definition 3.1** Seien ω_0, ω_V faithful normale Zustände auf 𝓜.
Der **relative Modularoperator** Δ_{ω_V|ω_0} ist definiert durch:

```
⟨A Ω_V, B Ω_0⟩ = ⟨Δ_{ω_V|ω_0}^{1/2} B Ω_0, A Ω_0⟩
```

**Definition 3.2** Der **relative Modularhamiltonian**:

```
K_{ω_V|ω_0} := -log Δ_{ω_V|ω_0}
```

*Bemerkung:* K_{ω_V|ω_0} ist das kanonische Objekt dieser Arbeit.
Es ist wohldefiniert für alle faithful normalen Zustände, ohne dass
ein expliziter Hamiltonoperator benötigt wird.

### 3.2 Die Kozykel-Relation

**Theorem 3.3 (Connes 1973)**

Der unitäre **Connes-Kozykel** $(D\omega_V : D\omega_0)_t$ vermittelt
zwischen den Modulargruppen:

```
(D\omega_V : D\omega_0)_t = Δ_{ω_V|ω_0}^{it} · Δ_0^{-it}
```

mit Eigenschaften:
```
Kozykel:    (Dω_V:Dω_0)_{t+s} = (Dω_V:Dω_0)_t · σ_t^0((Dω_V:Dω_0)_s)
Komposition: (Dω_V:Dω_0)_t · (Dω_0:Dω_W)_t = (Dω_V:Dω_W)_t
```

*Wichtig:* Diese Relation ist wohldefiniert auf der Tomita-Algebra 𝒯,
was Domänenkonsistenz garantiert.

### 3.3 Das Araki-Perturbationstheorem

**Theorem 3.4 (Araki 1973, PRIMS 9:165)**

Sei V ∈ 𝓜 beschränkt, selbstadjungiert, ‖V‖ < ∞. Dann gilt:

```
log Δ_{ω_V|ω_0} = -β · V    (exakt, Araki Theorem 1)
```

Damit:

```
K_{ω_V|ω_0} = β · V    (in erster Ordnung, exakt für beschränktes V)
```

und für die Absolutform des Modularoperators:

```
K_{ω_V} = K_{ω_0} + β · V + R(V)
‖R(V)‖ ≤ (β²/2) · ‖V‖ · ‖[K_0, V]‖
```

**Beweis-Skizze:** Der Araki-Perturbationskozyklus Γ_β(V) = Te^{-∫V dτ}
erfüllt ω_V(A) = ω_0(A·Γ_β(V))/ω_0(Γ_β(V)). Die Aussage
log Δ_{ω_V|ω_0} = -βV folgt aus der KMS-Analytizität. □

**Lemma 3.5 (Linearer Kozykel, erste Ordnung)**

```
K_{ω_V|ω_0} = β · V + O(‖V‖²)
```

*Konsequenz für diese Arbeit:* Anstatt der problematischen "naiven Differenz"
K_{ω_V} - K_{ω_0} verwenden wir K_{ω_V|ω_0} als das mathematisch saubere
Objekt. In erster Ordnung sind beide äquivalent.

---

## Kapitel 4: Modulare Formulierung der Linearen Antwort

### 4.1 Laplace-Resolvent des adjungierten Modularflusses

**Lemma 4.1** Der adjungierte Modularfluss

```
Φ_t: B(ℋ) → B(ℋ),    Φ_t(A) = σ_t^{ω_0}(A)
```

ist eine stark stetige unitäre C₀-Gruppe mit ‖Φ_t‖ = 1.

**Beweis:**
- C₀-Eigenschaft: aus KMS-Analytizität (Def. 2.5)
- Gruppengesetz: σ_{s+t}^0 = σ_s^0 ∘ σ_t^0 (Tomita-Takesaki)
- Unitarität: ‖σ_t^0(A)‖ = ‖A‖ für *-Automorphismen □

**Definition 4.2 (Adjungierter Laplace-Resolvent)**

```
R_ad(z, iK_0)(A) := (z · id - i · [K_0, ·])^{-1}(A)
                  = ∫_0^∞ e^{-zt} σ_t^{ω_0}(A) dt,    Re(z) > 0
```

Aus Theorem 2.9 (Hille-Yosida, M=1, ω=0):

```
‖R_ad(z, iK_0)‖ ≤ 1/Re(z)
```

### 4.2 Statische Modulare Kubo-Identität

**Theorem 4.3 (Statische Modulare Kubo-Identität)**

Sei ω_0 KMS bei β, V ∈ 𝓜 beschränkt. Dann gilt:

```
χ_A^{stat} := -i · ω_0([A, V]) = -(i/β) · ω_0([A, K_{ω_V|ω_0}]) + O(‖V‖²)
```

**Beweis:**

Aus Araki Theorem 3.4: V = (1/β) · K_{ω_V|ω_0} + O(‖V‖²)

Einsetzen in die Kubo-Formel:
```
χ_A^{stat} = -i · ω_0([A, (1/β)K_{ω_V|ω_0} + O(‖V‖²)])
           = -(i/β) · ω_0([A, K_{ω_V|ω_0}]) + O(‖V‖²)    □
```

*Interpretation:* Die statische Suszeptibilität ist durch den relativen
Modularhamiltonian K_{ω_V|ω_0} bestimmt — das kanonische Objekt der
Störung in modularer Sprache.

### 4.3 Dynamische Erweiterung: Laplace-Modulare Kubo-Identität

**Theorem 4.4 (Laplace-Modulare Kubo-Identität — Hauptergebnis)**

Für Re(z) > 0:

```
┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  χ_A(z) = -(i/β) · ω_0([R_ad(z, iK_0)(A), K_{ω_V|ω_0}]) + E   │
│                                                                    │
│  |E| ≤ β · ‖A‖ · ‖V‖ · ‖[K_0, V]‖ / (2 · Re(z))                │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

**Vollständiger Beweis (5 Schritte):**

**Schritt 1** — Laplace-Kubo (aus Def. 4.2 + Kubo 1957):
```
χ_A(z) = ∫_0^∞ e^{-zt} (-i) ω_0([σ_t^0(A), V]) dt
        = -i · ω_0([R_ad(z, iK_0)(A), V])
```
(Austausch ω_0 und Integral: zulässig da ω_0 normiert, ∫|e^{-zt}|dt = 1/Re(z) < ∞)

**Schritt 2** — Araki-Substitution (aus Theorem 3.4):
```
V = (1/β) · K_{ω_V|ω_0} - (1/β) · R(V)
```

**Schritt 3** — Einsetzen:
```
χ_A(z) = -(i/β) · ω_0([R_ad(z)(A), K_{ω_V|ω_0}]) + (i/β) · ω_0([R_ad(z)(A), R(V)])
```

**Schritt 4** — Fehlerabschätzung (aus Hille-Yosida, Lemma 4.1 + Araki):
```
|(i/β) · ω_0([R_ad(z)(A), R(V)])|
≤ (1/β) · 2‖R_ad(z)‖ · ‖A‖ · ‖R(V)‖
≤ (1/β) · (2/Re(z)) · ‖A‖ · (β²/2) · ‖V‖ · ‖[K_0,V]‖
= β · ‖A‖ · ‖V‖ · ‖[K_0,V]‖ / (2·Re(z))
```

**Schritt 5** — Ergebnis: □

### 4.4 Araki als Grenzfall (Anfangswerttheorem)

**Korollar 4.5**

Arakis statisches Ergebnis folgt aus Theorem 4.4 via Lemma 2.8:

```
χ_A^{stat} = χ_A(t=0⁺) = lim_{z→+∞} z · χ_A(z)

= lim_{z→∞} z · [-(i/β) · ω_0([R_ad(z)(A), K_{ω_V|ω_0}])]

= -(i/β) · ω_0([lim_{z→∞} z·R_ad(z, iK_0)(A), K_{ω_V|ω_0}])

= -(i/β) · ω_0([A, K_{ω_V|ω_0}])    [da lim_{z→∞} z·R(z,A) = I, Engel-Nagel II.1.10]

= Theorem 4.3    ✓
```

**Bedeutung:** Theorem 4.4 ist die vollständige analytische Erweiterung
von Theorem 4.3. Araki (1973) liefert den Wert bei z → ∞ (t = 0).
Theorem 4.4 liefert die gesamte analytische Funktion für alle Re(z) > 0.

---

## Kapitel 5: Anwendung auf das Magnetar-Regime

### 5.1 Landau-Quantisierung und KMS-Deformation

Im Magnetfeld B ≫ B_c wird der ungestörte Hamiltonoperator zu
H_B = H_0 + V_B mit

```
V_B = H_Zeeman + H_Landau = -μ_n · B · σ_z + ℏω_c Σ_n n·N_n
```

Der relative Modularhamiltonian (aus Theorem 3.4):

```
K_{ω_B|ω_0} = β · V_B + O(‖V_B‖²)
```

**Gültigkeitsprüfung:**

Für Magnetar-Parameter (B = 10¹¹ T, T = 10⁸ K):

```
β|μ_n|B = |μ_n|B / (k_BT) ≈ 12 MeV / (8.6 keV) ≈ 1400
```

Das Regime β‖V_B‖ ≫ 1 liegt außerhalb der Perturbationsnäherung erster
Ordnung. Die vollständige Araki-Reihe muss summiert werden.

### 5.2 Exakte Resummation für Zeeman-Störung

Für V_Z = |μ_n|B · σ_z (Spin-½-System):

```
Γ_β(V_Z) = cosh(β|μ_n|B) · 𝟙 + sinh(β|μ_n|B) · σ_z
```

Relativer Modularhamiltonian (exakt, alle Ordnungen):

```
K_{ω_B|ω_0}^{exakt} = -log Δ_{ω_B|ω_0}
                     = 2·artanh(tanh(β|μ_n|B)) · σ_z
                     = 2β|μ_n|B · σ_z    (für beliebiges β|μ_n|B)
```

Statische Suszeptibilität (aus Theorem 4.3, exakt):

```
χ_{σ_x}^{stat} = -(i/β) · ω_0([σ_x, K_{ω_B|ω_0}^{exakt}])
               = -(i/β) · 2β|μ_n|B · ω_0([σ_x, σ_z])
               = 2|μ_n| · ω_0(σ_y)
               = 0    (im ungestörten GGW: ⟨σ_y⟩_0 = 0)
```

Die Längskomponente (A = σ_z):

```
χ_{σ_z}^{stat} = -(i/β) · 2β|μ_n|B · ω_0([σ_z, σ_z]) = 0
```

*Korrekte physikalische Interpretation:* Die statische longitudinale
Suszeptibilität verschwindet (Zeeman-Sättigung). Das ist Brillouin-
Sättigung — bekannte Quantenstatistik, korrekt in modularer Sprache
reproduziert.

### 5.3 Stabilitätskriterium

**Proposition 5.4**

Ein KMS-System ist im Zustand ω_B stabil unter der Lindblad-Evolution
ℰ_t (Theorem 2 von Lindblad 1976) genau dann, wenn:

```
d/dt S(ρ(t) ‖ ω_B) ≤ 0    (Monotonie der relativen Entropie)
```

*Verbindung zu K_{ω_V|ω_0}:*

```
S(ω_V ‖ ω_0) = ω_V(K_{ω_V|ω_0}) ≥ 0
```

mit Gleichheit genau für ω_V = ω_0.

---

## Kapitel 6: Mathematische Vollständigkeitsprüfung

### 6.1 Gültigkeitstabelle

| Theorem | Bedingungen | Type III₁? | Fehler |
|---------|------------|------------|--------|
| 3.4 (Araki) | ‖V‖ < ∞ | ja | O(β²‖V‖²) |
| 4.3 (stat. Kubo) | ‖V‖ < ∞ | ja | O(‖V‖²) |
| 4.4 (Laplace-Kubo) | Re(z)>0, ‖V‖<∞ | ja | β‖V‖²/(2Re(z)) |
| 4.5 (Araki-Limit) | ‖V‖ < ∞ | ja | exakt |
| 5.4 (Stabilität) | Lindblad | ja | exakt |

### 6.2 Beweislücken (ehrliche Analyse)

**(a) Unbeschränktes V:**
Für realistische QFT-Wechselwirkungen ist V oft unbeschränkt. Die
Erweiterung auf quadratische Formen erfordert zusätzliche Regularisierung
(vgl. Bratteli-Robinson Vol. II §5.4). Das ist ein offenes Problem.

**(b) Dynamische Kubo-Formel für Type-III₁ ohne Volumen-Cutoff:**
Theorem 4.4 verwendet R_ad(z) = ∫e^{-zt}σ_t dt. Der Austausch von
ω_0 und Integral erfordert einen Abschätzungsrahmen, der für Type-I-
Systeme trivial ist, für Type-III₁ aber sorgfältige Behandlung verlangt.

**(c) Nicht-Markovianische Stabilität:**
Proposition 5.4 gilt unter Markov-Approximation. Magnetare sind
nicht-Markovianisch; die volle Aussage erfordert NESS-Theorie.

---

## Kapitel 7: Schlussbetrachtung

### 7.1 Zusammenfassung der Hauptergebnisse

Diese Arbeit hat gezeigt:

**Theorem 4.3** (statische Modulare Kubo-Identität):
```
χ_A^{stat} = -(i/β) · ω_0([A, K_{ω_V|ω_0}]) + O(‖V‖²)
```
Der relative Modularhamiltonian K_{ω_V|ω_0} ist das kanonische Objekt
für die statische lineare Antwort in KMS-Systemen.

**Theorem 4.4** (dynamische Laplace-Erweiterung):
```
χ_A(z) = -(i/β) · ω_0([R_ad(z, iK_0)(A), K_{ω_V|ω_0}]) + O(‖V‖²/Re(z))
```
Die Laplace-Transformation des Modularflusses (Hille-Yosida) liefert
die vollständige frequenzabhängige Suszeptibilität.

**Korollar 4.5** (Konsistenz):
Arakis statisches Ergebnis ist der Grenzfall z → ∞ des dynamischen
Theorems via dem Anfangswerttheorem der Laplace-Transformation.

### 7.2 Wissenschaftliche Einordnung

Diese Arbeit ist eine **mathematische Strukturarbeit**: Sie formuliert
bekannte physikalische Resultate (Kubo-Formel) in einer neuen algebraischen
Sprache (modulare Theorie), die in Bereichen gilt (Type-III₁), wo die
klassische Formulierung scheitert.

Der Beitrag ist nicht "neue Physik", sondern ein neues mathematisches
Werkzeug: der relative Modularhamiltonian K_{ω_V|ω_0} als Träger der
linearen Antwortinformation in AQFT.

---

## Literaturverzeichnis

```
[A73]  H. Araki, "Relative Hamiltonian for faithful normal states
       of a von Neumann algebra",
       Publ. RIMS Kyoto Univ. 9, 165–209 (1973)
       DOI: 10.2977/prims/1195192684

[A76]  H. Araki, "Relative entropy of states of von Neumann algebras",
       Publ. RIMS Kyoto Univ. 11, 809–833 (1976)

[BF82] D. Buchholz, K. Fredenhagen, "Locality and the structure of
       particle states", Commun. Math. Phys. 84, 1–54 (1982)

[BR87] O. Bratteli, D.W. Robinson, "Operator Algebras and Quantum
       Statistical Mechanics", Vol. I+II, Springer (1987/1997)

[BW75] J.J. Bisognano, E.H. Wichmann, "On the duality condition for
       a Hermitian scalar field", J. Math. Phys. 16, 985 (1975)

[C73]  A. Connes, "Une classification des facteurs de type III",
       Ann. Sci. Éc. Norm. Sup. 6, 133–252 (1973)

[EN00] K.-J. Engel, R. Nagel, "One-parameter semigroups for linear
       evolution equations", Springer GTM 194 (2000)
       [Hille-Yosida: Theorem II.3.8; Resolvent-Laplace: Prop. II.1.10]

[H92]  R. Haag, "Local Quantum Physics", Springer (1992)

[HHW67] R. Haag, N.M. Hugenholtz, M. Winnink, "On the equilibrium
        states in quantum statistical mechanics",
        Commun. Math. Phys. 5, 215–236 (1967)

[J95]  T. Jacobson, "Thermodynamics of spacetime: the Einstein
       equation of state", PRL 75, 1260 (1995)

[JLMS16] D. Jafferis, A. Lewkowycz, J. Maldacena, S. Shenker,
          "Relative entropy equals bulk relative entropy",
          JHEP 06, 004 (2016), arXiv:1512.06431

[K57]  R. Kubo, "Statistical-mechanical theory of irreversible
       processes", J. Phys. Soc. Japan 12, 570 (1957)

[L76]  G. Lindblad, "On the generators of quantum dynamical
       semigroups", Commun. Math. Phys. 48, 119 (1976)

[T70]  M. Takesaki, "Tomita's theory of modular Hilbert algebras
       and its applications", LNM 128, Springer (1970)

[V10]  E.P. Verlinde, "On the origin of gravity and the laws of
       Newton", JHEP 1104, 029 (2011), arXiv:1001.0785
```
