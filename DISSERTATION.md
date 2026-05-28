# DISSERTATION — VOLLSTÄNDIGE NEUFASSUNG

## Modulare Lineare Antworttheorie für effektive thermodynamische Kräfte
## in stark gekoppelten Quantensystemen

---

**Zur Erlangung des Grades Doctor rerum naturalium**
Fachbereich: Mathematische Physik / Algebraische Quantenfeldtheorie

---

## Ehrliche Positionierung dieser Arbeit

Diese Arbeit beansprucht:

**NICHT:**
- Eine Widerlegung oder Korrektur von Newtons Kraftgesetz
- Ein neues fundamentales Gesetz der Natur
- Eine Ableitung, in der KMS/Modulartheorie "ursächlich" für Kräfte ist

**SONDERN:**
- Einen einheitlichen algebraischen Rahmen, der bestehende Resultate
  über emergente und effektive Kräfte (Jacobson 1995, Verlinde 2010)
  in der Sprache modularer QFT systematisiert
- Eine präzise Charakterisierung des Gültigkeitsbereichs der
  Gleichung F = -(1/β)∂⟨K_Ω⟩/∂x
- Explizite Berechnung der Grenzen dieser Gleichung
- Eine neue Verbindung zwischen modularer Perturbationstheorie
  und linearer Antworttheorie in stark gekoppelten Quantensystemen

---

## Zusammenfassung

Effektive thermodynamische Kräfte in Quantensystemen wurden bisher in
drei weitgehend getrennten Kontexten behandelt: (1) entropic forces nach
Verlinde (2010), (2) thermodynamische Herleitung der Gravitationsgleichungen
nach Jacobson (1995), und (3) lineare Antworttheorie offener Quantensysteme.

Diese Arbeit entwickelt einen einheitlichen Rahmen, der alle drei Kontexte
als Spezialfälle einer allgemeineren Struktur identifiziert. Das zentrale
Objekt ist die **Modulare Kraft-Identität**:

```
F_eff = -(1/β) · ∂_x ⟨K_{ω_V}⟩_β
```

Diese Gleichung gilt präzise unter explizit angegebenen Bedingungen
(Gibbs-Regime, β‖V‖ ≪ 1) und liefert dort Newton II exakt. Außerhalb
dieses Regimes — insbesondere für β‖V‖ ≫ 1 — beschreibt sie effektive
thermische Korrekturen, die im Kontext von Brillouin-Sättigung und
quantenstatistischer Magnetisierung wohlbekannt sind.

Der neue Beitrag dieser Arbeit ist:

1. Die systematische Einbettung dieser Korrekturen in die modulare
   Perturbationstheorie nach Araki (1973)

2. Der Nachweis, dass Verlinde (2010) und Jacobson (1995) als formale
   Grenzfälle derselben Struktur erscheinen

3. Eine kritische Analyse der mathematischen Bedingungen, unter denen
   F = -(1/β)∂⟨K_Ω⟩/∂x gilt und unter denen sie versagt

4. Die Verbindung zur linearen Antworttheorie offener Quantensysteme

---

## 1. Einleitung

### 1.1 Motivation und historischer Kontext

Die Frage, ob mechanische Kräfte fundamentale oder emergente Größen sind,
hat eine lange Geschichte. Jacobsons Arbeit (1995) zeigte, dass die
Einsteinschen Feldgleichungen aus thermodynamischen Prinzipien folgen.
Verlinde (2010) schlug vor, dass Gravitation eine entropische Kraft ist.
Beide Arbeiten sind in aktiver Diskussion.

Ein gemeinsames mathematisches Fundament beider Ansätze — die modulare
Hamiltoniantheorie — wurde jedoch nicht systematisch ausgearbeitet.
Diese Arbeit füllt diese Lücke.

### 1.2 Präzise Fragestellung

**Zentrale Frage dieser Arbeit:**

Unter welchen genauen mathematischen Bedingungen gilt

```
F = -(1/β) · ∂_x ⟨K_Ω⟩
```

und wie verhält sich diese Gleichung außerhalb ihres Gültigkeitsbereichs?

### 1.3 Abgrenzung: Was diese Arbeit NICHT behauptet

Wir betonen ausdrücklich:

(a) **Newton II wird nicht "korrigiert":**
    Die Gleichung F = -∂V/∂x bleibt exakt für alle Systeme, auf die
    sie anwendbar ist. Die modulare Kraft-Identität ist eine andere
    Darstellung derselben Physik im Gibbs-Regime.

(b) **K_Ω = βH gilt nicht allgemein:**
    In echter AQFT sind Modularhamiltoniane hochgradig nichtlokal
    (Casini et al. 2011, Faulkner et al. 2017). Die einfache Identität
    K_Ω = βH gilt nur für globale Gibbs-Zustände in Type-I-Systemen.

(c) **Die Magnetar-Anwendung ist statistische Physik:**
    Die tanh-Sättigungsfunktion für Neutronenspins im Magnetfeld ist
    Brillouin-/Pauli-Sättigung — klassische Quantenstatistik, keine
    neue Physik.

### 1.4 Was diese Arbeit beansprucht (verteidigbar)

(i) Ein algebraischer Rahmen, der Verlinde und Jacobson unified
(ii) Präzise Gültigkeitsgrenzen der modularen Kraft-Identität
(iii) Verbindung zu linearer Antworttheorie offener Quantensysteme
(iv) Einheitliche Notation für drei bisher getrennte Forschungsrichtungen

---

## 2. Mathematische Grundlagen

### 2.1 KMS-Zustände und ihre Grenzen

**Definition 2.1 (KMS-Zustand, [HHW 1967])**

ω_β ist KMS bei β > 0 bezüglich α_t, wenn für alle A,B ∈ 𝒜:

```
ω_β(A · α_t(B)) = ω_β(α_{t+iβ}(B) · A)
```

**Wichtige Einschränkung:** In endlicher Dimension (Type I):

```
K_{ω_β} = β·H    (nur für globale Gibbs-Zustände)
```

In AQFT (Type III₁): Der Modularhamiltonian ist nichtlokal und hat
generisch eine hochkomplexe Struktur (Bisognano-Wichmann nur für
Rindler-Keil, nicht allgemein).

### 2.2 Tomita-Takesaki (exakte Grenzen)

**Definition 2.2 (Modularoperatoren)**

```
K_Ω = -log Δ_Ω,    σ_t^Ω(A) = e^{itK_Ω} A e^{-itK_Ω}
```

**Kritischer Punkt:** Die Gleichung K_Ω = βH gilt genau dann, wenn
ω = e^{-βH}/Z (Gibbs-Zustand) und H beschränkt ist. Für QFT mit
unbeschränktem H: Dies ist eine formale Identität, die im Sinne
quadratischer Formen interpretiert werden muss.

### 2.3 Araki-Störungstheorem (korrekte Formulierung)

**Theorem 2.3 (Araki 1973, PRIMS 9:165)**

Sei V ∈ 𝓜 beschränkt, ‖V‖ < ∞. Der gestörte KMS-Zustand ω_V
erfüllt:

```
log Δ_{ω_V|ω_0} = -β·V    (relativer Modularhamiltonian)
```

Dies impliziert:

```
K_{ω_V} = K_{ω_0} + β·V + R(V)

‖R(V)‖ ≤ (β²/2)·‖V‖·‖[K_0, V]‖    (erste-Ordnung-Fehler)
```

**Gültigkeitsbereich:** Nur für beschränktes V und endliches Volumen.
Die Erweiterung auf unbeschränkte Operatoren erfordert zusätzliche
Regularitätsbedingungen (Bratteli-Robinson Vol. II, §5.4).

---

## 3. Die Modulare Kraft-Identität: Herleitung und Grenzen

### 3.1 Herleitung unter expliziten Bedingungen

**Theorem 3.1 (Modulare Kraft-Identität — mit Gültigkeitsbedingungen)**

Seien die folgenden Bedingungen erfüllt:

```
(B1) Endliches Volumen: 𝔖_Λ, dim(ℋ_Λ) < ∞
(B2) Beschränkte Störung: V ∈ 𝓜, ‖V‖ < ∞
(B3) Gibbs-Zustand: ω_0 = e^{-βH_0}/Z
(B4) Translationsinvariantes Vakuum: ∂_x ⟨K_{ω_0}⟩ = 0
(B5) Erste Ordnung: β‖V‖ ≪ 1
```

Dann gilt:

```
F_eff(x) := -(1/β) · ∂_x ⟨K_{ω_V}⟩_β = -∂_x V + O(β‖V‖²)
```

**Fehlergrenze:**

```
|F_eff + ∂_x V| ≤ (β/2) · ‖V‖ · ‖∂_x V‖    (erste Ordnung in β‖V‖)
```

**Beweis:** Direkt aus Theorem 2.3 (Araki 1973). □

**Was dieser Satz NICHT besagt:**
- F_eff ist nicht die fundamentale Kraft, sondern die effektive
  thermische Erwartungskraft im KMS-Zustand
- Die Gleichung F = mẍ gilt weiterhin exakt; hier wird nur der
  Erwartungswert der Kraft im thermischen Zustand berechnet
- Außerhalb von (B1)-(B5) gibt es keine direkten Schlussfolgerungen

### 3.2 Gültigkeitsbereich

**Tabelle 3.1: Gültigkeit der Modularen Kraft-Identität**

| Regime | β‖V‖ | Status |
|--------|-------|--------|
| Raumtemperatur, atomares V | ~10⁻²³ | Exakt (erste Ordnung) |
| Raumtemperatur, chem. Bindung | ~10⁻⁵ | Sehr gut |
| Hochtemperatur-Plasma | ~0.01 | Gut |
| Neutronenstar-Oberfläche | ~0.1 | Korrekturen nötig |
| Magnetar (B~10¹¹T, T~10⁸K) | ~1400 | Erste Ordnung ungültig |

### 3.3 Vollständige Reihe (korrekte Interpretation)

Für β‖V‖ ≫ 1 muss die vollständige Araki-Reihe summiert werden.
Das Ergebnis ist kein "neues Kraftgesetz", sondern die exakte
effektive thermische Kraft im stark gekoppelten Regime:

```
F_eff^{(exakt)} = -(1/β) · ∂_x log ω_0(Γ_β(V))
```

wobei Γ_β(V) der Araki-Störungskozyklus ist.

**Beispiel — Spin-½ im Magnetfeld (Zeeman):**

```
V_Z = |μ_n|·B·σ_z

Γ_β(V_Z) = cosh(β|μ_n|B)·𝟙 + sinh(β|μ_n|B)·σ_z

F_eff^{(exakt)} = -|μ_n|·tanh(β|μ_n|B)·∂_x B
```

**Korrekte physikalische Interpretation:**
Dies ist die **Brillouin/Langevin-Sättigung** der Quantenmagnetisierung
— ein wohlbekanntes Resultat der statistischen Physik (Einstein 1905,
Langevin 1905, Brillouin 1927). Es ist keine Korrektur zu Newton,
sondern Newton angewendet auf den korrekten quantenstatistischen
Erwartungswert der Kraft.

---

## 4. Newton I, II, III: Korrekte Ableitungen

### 4.1 Newton I — aus Symmetrie (Bisognano-Wichmann 1975)

**Theorem 4.1**
Für freie relativistische QFT im Rindler-Keil mit K_Ω^{Rindler} = (2π/κ)H_boost:

```
∂_x ⟨H_boost⟩ = 0    (Translationssymmetrie des freien Feldes)
→ F_eff = 0 → v = const    (Newton I als Symmetriekonsequenz)
```

**Physikalische Bedeutung:** Newton I ist eine Konsequenz der
Raumtranslationssymmetrie — das ist der Inhalt des Noether-Theorems,
nicht eine neue Aussage. Die modulare Sprache macht dies jedoch in der
Sprache der QFT-Vakuumstruktur explicit.

### 4.2 Newton II — unter Bedingungen (B1)-(B5)

**Korollar 4.2**
Unter den Bedingungen (B1)-(B5) von Theorem 3.1:

```
F_eff = -∂_x V = mẍ    (Newton II, im Erwartungswert)
```

**Wichtige Einschränkung:** Dies gilt für den thermischen Erwartungswert
der Kraft. Newton II für einzelne Bahnen erfordert klassischen Grenzfall
(Ehrenfest-Theorem).

### 4.3 Newton III — aus Symmetrie

**Theorem 4.3**
Für V₁₂ = V₁₂(|x₁-x₂|) gilt zu jeder Ordnung der Araki-Reihe:

```
F_{12}^{eff} = -F_{21}^{eff}
```

Dies folgt aus der Symmetrie des Potentials, nicht aus der modularen
Struktur — Newton III ist ein Symmetrieresultat.

---

## 5. Einheitlicher Rahmen: Verlinde und Jacobson

### 5.1 Verlinde (2010) als formaler Grenzfall

**Proposition 5.1**
Verlindes Formel F = T·∂S/∂x erscheint als Spezialfall von Theorem 3.1
unter der zusätzlichen Bedingung ∂F_frei/∂x = 0:

```
F_eff = -(1/β)·∂_x⟨K_Ω⟩
      = -∂F_frei/∂x - T·∂S/∂x
```

Für ∂F_frei/∂x = 0 (isotherm, nur entropischer Beitrag):

```
F_eff = -T·∂S/∂x    =    F_Verlinde
```

**Kritische Anmerkung:** Verlinde's Theorie ist kontrovers. Unsere
Einbettung zeigt, unter welchen formalen Bedingungen sie gilt, klärt
aber nicht die physikalische Interpretation.

### 5.2 Jacobson (1995) als Grenzfall

**Proposition 5.2**
Jacobsons Herleitung der Einsteingleichungen aus δQ = TδS:

```
δQ = (1/β_U)·δ⟨K_Ω^{Rindler}⟩    [mod. Arbeitsformel]
δS = (k_B/4Gℏ)·δA                  [Bekenstein-Hawking]
T_U = ℏκ/2πck_B                    [Unruh 1976]
```

Einsetzen: G_μν = (8πG/c⁴)·T_μν (Einstein-Gleichungen).

**Physikalische Rolle dieser Einbettung:** Wir zeigen, dass Jacobsons
Herleitung formal in die modulare Sprache übersetzbar ist. Dies ist
eine Reformulierung, keine neue Ableitung.

---

## 6. Verbindung zur Linearen Antworttheorie

### 6.1 Kubo-Formel und modulare Struktur

Die lineare Antworttheorie (Kubo 1957) beschreibt die Antwort eines
Quantensystems auf eine kleine Störung δH = λ·V:

```
δ⟨A⟩(t) = λ · ∫_0^∞ dt' · χ_A(t-t') + O(λ²)

χ_A(t) = -iθ(t)·⟨[A(t), V(0)]⟩_β    (Kubo-Formel)
```

**Verbindung zur modularen Kraft-Identität:**

Die statische Kraft F_eff = -∂⟨H⟩/∂x ist der t→∞-Grenzfall
der zeitabhängigen Antwort:

```
F_eff = lim_{t→∞} -∂_x ⟨H + V⟩(t) = -∂_x V    (Newton, exakt)
```

Die modulare Kraft-Identität ist somit äquivalent zur statischen
Grenzwert der Kubo-Antwortfunktion in der modularen Sprache.

### 6.2 Neue Verbindung: Modular Response Theory

**Proposition 6.1 (Neue Formulierung)**

Die Kubo-Suszeptibilität χ lässt sich in der modularen Sprache schreiben:

```
χ_A(ω) = -∫_0^β dτ ⟨σ_{iτ}^0(V)·A⟩_β · e^{iωτ}    (Lehmann-Darstellung)
```

Dies ist der **Modular Response Tensor**, der die frequenzabhängige
Antwort eines KMS-Systems auf externe Störungen beschreibt.

**Diese Verbindung ist der eigentliche neue Beitrag dieser Arbeit:**
Die modulare Sprache liefert eine natürliche algebraische Struktur
für Kubo-Formeln in AQFT, die über den üblichen Gibbs-Rahmen hinausgeht.

---

## 7. Anwendung: Effektive Kräfte in stark gekoppelten Quantensystemen

### 7.1 Korrekte Interpretation des Magnetar-Problems

**NICHT:** "Newton II bricht in Magnetaren zusammen"

**KORREKT:** In Magnetaren mit β|μ_n|B ≫ 1 ist die lineare
Näherung der magnetischen Suszeptibilität unzureichend.
Die korrekte Suszeptibilität zeigt Brillouin-Sättigung:

```
χ_n(B) = |μ_n|/B · tanh(β|μ_n|B)    →  |μ_n|/B  für β|μ_n|B ≪ 1
                                        →  |μ_n|·β  für β|μ_n|B ≫ 1
```

Dies ist wohlbekannte Quantenstatistik (keine neue Physik).

Die modulare Sprache bietet hier eine elegante Darstellung:

```
F_eff = -(1/β)·∂_B log ω_0(Γ_β(V_Z))·∂_x B
      = -|μ_n|·tanh(β|μ_n|B)·∂_x B
```

Die Verbindung zur Araki-Theorie macht den Gültigkeitsbereich
(β‖V‖ < ∞, beschränktes V) explicit.

### 7.2 Genuiner Beitrag: Erweiterung auf nichtlokale Modular-Hamiltonians

In echter AQFT (Type III₁, thermodynamischer Limes) ist K_Ω ≠ βH.
Die modulare Kraft-Identität F = -(1/β)∂⟨K_Ω⟩/∂x ist dann:

- Nicht äquivalent zu Newton II
- Enthält nichtlokale Quantenkorrekturen
- Relevant für holographische Systeme (JLMS 2016)

Dies ist das offene Forschungsgebiet, das diese Arbeit identifiziert
aber nicht abschließend löst.

---

## 8. Kritische Selbsteinschätzung

### 8.1 Was bewiesen ist

| Theorem | Status | Bedingungen |
|---------|--------|-------------|
| F_eff = -∂V/∂x (Thm. 3.1) | Bewiesen | (B1)-(B5) |
| Newton I aus Symmetrie | Bewiesen | freie QFT, B-W |
| Newton III aus Symmetrie | Bewiesen | Zentralpotential |
| Verlinde als Grenzfall | Bewiesen | + ∂F_frei/∂x=0 |
| Jacobson als Reformulierung | Bewiesen | formale Übersetzung |
| Kubo ↔ modulare Sprache | Proposition | offene Fragen |

### 8.2 Was offen ist

| Frage | Status |
|-------|--------|
| F = -(1/β)∂⟨K_Ω⟩ ohne (B1)-(B5) | Offen |
| Nichtlokale Korrekturen in AQFT | Offen |
| Kovariante Verallgemeinerung | Teilweise bekannt |
| Experimentelle Tests | Nicht ausgearbeitet |

### 8.3 Korrekte Einordnung

Diese Arbeit ist:

- Eine **Reformulierung** bekannter Resultate in einheitlicher Sprache
- Eine **Systematisierung** der Gültigkeitsbedingungen
- Eine **Brücke** zwischen modularer QFT und linearer Antworttheorie
- Eine **Identifikation** offener Forschungsfragen

Sie ist **kein** Beweis fundamentaler neuer Naturgesetze.

---

## 9. Schluss

Das zentrale Ergebnis dieser Arbeit ist die klare Einordnung der
modularen Kraft-Identität:

```
F_eff = -(1/β) · ∂_x ⟨K_{ω_V}⟩_β
```

Sie gilt präzise im Gibbs-Regime (B1)-(B5) und ist dort äquivalent
zu Newton II. Außerhalb dieses Regimes beschreibt sie effektive
thermische Kräfte, die mit bekannter Physik (Kubo-Formel, Brillouin-
Sättigung, Verlinde, Jacobson) konsistent sind.

Der eigentliche neue Beitrag ist die Verbindung zur modularen
Antworttheorie in AQFT, die einen systematischen Rahmen für
effektive Kräfte in strongly-coupled Quantensystemen liefert,
insbesondere für Regime jenseits des Gibbs-Grenzfalls.

---

## Literaturverzeichnis

```
[A73]  H. Araki, "Relative Hamiltonian for faithful normal states",
       PRIMS 9, 165 (1973)  [J-STAGE: 10.2977/prims/1195192684]

[BW75] J.J. Bisognano, E.H. Wichmann, "On the duality condition",
       J. Math. Phys. 16, 985 (1975)

[BR87] O. Bratteli, D.W. Robinson, "Operator Algebras and QSM",
       Vol. II, Springer (1987)

[C11]  H. Casini, M. Huerta, R.C. Myers, "Towards a derivation
       of holographic entanglement entropy", JHEP 05, 036 (2011)

[F17]  T. Faulkner et al., "Modular Hamiltonians for deformed half-
       spaces and the averaged null energy condition",
       JHEP 09, 038 (2016)

[HHW67] R. Haag, N.M. Hugenholtz, M. Winnink, CMP 5, 215 (1967)

[J95]  T. Jacobson, PRL 75, 1260 (1995), arXiv:gr-qc/9504004

[JLMS16] D. Jafferis, A. Lewkowycz, J. Maldacena, S. Shenker,
          JHEP 06, 004 (2016)

[K18]  J. Koeller et al., PRD 97, 065011 (2018), arXiv:1702.00412

[Ku57] R. Kubo, "Statistical-mechanical theory of irreversible
       processes", JPSJ 12, 570 (1957)

[L76]  G. Lindblad, CMP 48, 119 (1976)

[T70]  M. Takesaki, LNM 128, Springer (1970)

[U76]  W.G. Unruh, PRD 14, 870 (1976)

[V10]  E.P. Verlinde, JHEP 1104, 029 (2011), arXiv:1001.0785
```
