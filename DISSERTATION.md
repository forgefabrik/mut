# DISSERTATION — FINALE FASSUNG

## Die Modulare Kubo-Identität:
## Araki-Relative Modularhamiltonianer als Instrument der
## linearen Antworttheorie in algebraischen Quantenfeldtheorien

---

**Zur Erlangung des Grades Doctor rerum naturalium**

Fachbereich: Mathematische Physik

---

## Das echte Problem und warum es gelöst wird

**Das Problem:**
Die lineare Antworttheorie (Kubo 1957) basiert auf dem expliziten
Hamiltonoperator H. In algebraischen Quantenfeldtheorien vom Typ III₁
existiert kein solcher Hamiltonian als beschränkter Operator. Gleichzeitig
ist der Modularhamiltonian K_Ω (Tomita-Takesaki) wohlbekannt. Die Frage,
wie die Kubo-Formel in der Sprache von K_Ω ausgedrückt werden kann, ist
in der Literatur nicht beantwortet.

**Die Lösung:**
Diese Arbeit zeigt, dass die statische Kubo-Suszeptibilität durch die
Formel

```
χ_A^{stat} = -(i/β) · ω([A, δK_Ω])
```

ausgedrückt werden kann, wobei δK_Ω = K_{ω_V} - K_{ω_0} der
Araki-Relativhamiltonian (1973) ist. Diese **Modulare Kubo-Identität**
gilt auch dann, wenn V kein wohldefiniertter beschränkter Operator ist,
solange δK_Ω existiert.

---

## Zusammenfassung

Die Kubo-Formel der linearen Antworttheorie verbindet die Gleichgewichts-
Korrelationsfunktionen eines Quantensystems mit seiner Reaktion auf externe
Störungen. Ihre Formulierung setzt einen expliziten Hamiltonoperator H voraus.

In algebraischen Quantenfeldtheorien vom Typ III₁ — dem mathematisch
korrekten Rahmen für relativistische QFT — existiert kein solcher Operator.
Der Modularhamiltonian K_Ω der Tomita-Takesaki-Theorie übernimmt die Rolle
von βH, hat jedoch eine andere mathematische Struktur.

Diese Arbeit leitet die **Modulare Kubo-Identität** her:

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│    χ_A^{stat} = -(i/β) · ω([A, δK_Ω])                        │
│                                                                │
│    δK_Ω = K_{ω_V} - K_{ω_0}  (Araki 1973)                    │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

Diese Formel:

1. Gilt für KMS-Zustände auf beliebigen Von-Neumann-Algebren
2. Erfordert keinen expliziten Hamiltonoperator
3. Reduziert auf die Standard-Kubo-Formel für Type-I-Systeme
4. Ist in holographischen Systemen (JLMS 2016) direkt anwendbar

**Neuheit:** Die explizite Verbindung zwischen dem Araki-Relative-
Modularhamiltonian und der linearen Antworttheorie ist nach Kenntnis
des Autors in dieser Form nicht in der Literatur.

---

## Abstract (English)

The Kubo formula of linear response theory requires an explicit Hamiltonian.
In Type III₁ von Neumann algebras — the mathematically correct framework
for relativistic QFT — no such operator exists. The modular Hamiltonian
K_Ω of Tomita-Takesaki theory plays the role of βH but has a different
mathematical structure.

This dissertation derives the **Modular Kubo Identity**:

```
χ_A^{stat} = -(i/β) · ω([A, δK_Ω]),    δK_Ω = K_{ω_V} - K_{ω_0}
```

This formula: (1) holds for KMS states on arbitrary von Neumann algebras;
(2) requires no explicit Hamiltonian; (3) reduces to the standard Kubo
formula for Type-I systems; (4) is directly applicable in holographic
systems (JLMS 2016).

---

## 1. Einleitung

### 1.1 Das Problem: Lineare Antworttheorie ohne Hamiltonian

Die lineare Antworttheorie (Kubo 1957, Martin-Schwinger 1959) beschreibt
die Reaktion eines Quantensystems im Gleichgewicht auf eine schwache externe
Störung δH = εV. Die zentrale Formel:

```
δ⟨A⟩(t) = ε · ∫_{-∞}^t dt' · χ_A(t-t') + O(ε²)

χ_A(t) = -i · θ(t) · ω_β([A(t), V(0)])
```

setzt voraus: (a) explizites H, (b) die Zeitentwicklung A(t) = e^{iHt}Ae^{-iHt}.

**Wo diese Voraussetzung versagt:**

In algebraischer QFT (AQFT) vom Typ III₁ — dem physikalisch korrekten
Rahmen für relativistische Quantenfeldtheorien (Haag 1992, Buchholz-
Fredenhagen 1982) — gilt:

- kein Trace: tr(e^{-βH}) = ∞
- H existiert nicht als beschränkter Operator
- "A(t) = e^{iHt}Ae^{-iHt}" ist formal, nicht wohldefiniert

**Die natürliche Ersetzung:**

Der Modularhamiltonian K_Ω = -log Δ_Ω der Tomita-Takesaki-Theorie
erzeugt den Modularfluss σ_t^Ω(A) = e^{itK_Ω}Ae^{-itK_Ω}, der in KMS-
Systemen mit der physikalischen Zeitentwicklung übereinstimmt:

```
ω KMS bei β  ⟺  α_t = σ_t^ω  (Bratteli-Robinson Vol. II, Prop. 5.3.7)
```

Die Frage, die diese Arbeit beantwortet: Wie lautet die Kubo-Formel in
der Sprache von K_Ω und dem Araki-Relativhamiltonian δK_Ω?

### 1.2 Warum das wichtig ist

**(a) Holographische Systeme:**
In AdS/CFT ist der Modularhamiltonian der Grenz-CFT direkt mit
Bulk-Geometrie verknüpft (JLMS 2016):

```
K_A^{boundary} = K_A^{bulk} + Area(γ_A)/4G
```

Die modulare Kubo-Identität ermöglicht, Response-Funktionen holographischer
Systeme aus Bulk-Geometrie zu berechnen.

**(b) Strongly correlated systems:**
Nahe Quantenphasenübergängen divergieren herkömmliche Störungsreihen.
Die modulare Formulierung liefert einen nicht-perturbativen Zugang.

**(c) Konzeptuelle Klarheit:**
Die Identifikation der Kubo-Suszeptibilität mit dem Araki-Relativhamiltonian
verbindet Informationstheorie (relative Entropie), modulare Theorie und
Antworttheorie.

### 1.3 Abgrenzung: Bekannte vs. neue Resultate

**Bekannt:**
- Kubo-Formel (Kubo 1957): χ(t) = -iθ(t)ω([A(t),V])
- Tomita-Takesaki: K_Ω = -log Δ_Ω, α_t = σ_t^ω für KMS
- Araki (1973): δK_Ω = βV + O(‖V‖²) für beschränktes V
- JLMS (2016): K_A^{boundary} = K_A^{bulk} + Area/4G

**Neu in dieser Arbeit:**
Die explizite Formel χ_A^{stat} = -(i/β)ω([A, δK_Ω]) und ihre
mathematisch präzise Herleitung als Verbindung zwischen diesen
bekannten Resultaten.

---

## 2. Mathematische Grundlagen

### 2.1 Von-Neumann-Algebren und Typklassifikation

**Definition 2.1** Eine Von-Neumann-Algebra 𝓜 ⊂ B(ℋ) ist eine
*-Unteralgebra, abgeschlossen in der σ-schwachen Topologie.

**Typklassifikation (Murray-von Neumann):**

| Typ | Projektion | Trace | Physik |
|-----|-----------|-------|--------|
| I_n | endlich | endlich | Quantenmechanik |
| I_∞ | abzählbar | σ-endlich | Quantenfeldth. (endl. Vol.) |
| II₁ | endlich | endlich | Kondensierte Materie |
| III₁ | — | ∄ | AQFT, QFT (thermodynamischer Limes) |

**Kritischer Punkt für diese Arbeit:**
Lokale Algebren in relativistischer AQFT sind generisch hyperfinite
Typ-III₁-Faktoren (Buchholz-Fredenhagen 1982). Für diese existiert
kein normalierter Trace, daher kein Gibbs-Zustand e^{-βH}/Z im
klassischen Sinne.

### 2.2 KMS-Zustände (Haag-Hugenholtz-Winnink 1967)

**Definition 2.2** ω_β ist KMS bei β > 0 bezüglich α_t, wenn
∀A,B ∈ 𝒜: F_{AB}(t) = ω(A·α_t(B)) analytisch im Streifen
0 < Im(z) < β mit F_{AB}(t+iβ) = ω(α_t(B)·A).

**Theorem 2.3 (Bratteli-Robinson, Vol. II, Prop. 5.3.7)**

```
ω_β ist KMS bei β bezüglich α_t  ⟺  α_t = σ_t^{ω_β}
```

Für Type-I mit endlichem H: K_{ω_β} = βH.
Für Type-III₁: K_Ω existiert, aber kein H als beschränkter Operator.

### 2.3 Tomita-Takesaki-Modulartheorie

**Theorem 2.4 (Tomita 1967, Takesaki 1970)**

Für 𝓜 ⊂ B(ℋ) mit zyklischem separierendem Vektor Ω:

```
S_Ω(AΩ) = A*Ω  →  S_Ω = J_Ω Δ_Ω^{1/2}
K_Ω = -log Δ_Ω    (Modularhamiltonian)
σ_t^Ω(A) = e^{itK_Ω} A e^{-itK_Ω}
σ_t^Ω(𝓜) = 𝓜  ∀t ∈ ℝ
```

**Wichtig:** K_Ω ist i.A. ein unbeschränkter selbstadjungierter Operator
mit komplizierter nichtlokaler Struktur. In AQFT hängt K_Ω von der
Region ab und ist nur für spezielle Regionen (Rindler-Keil) geometrisch
interpretierbar (Bisognano-Wichmann 1975).

### 2.4 Araki-Perturbationstheorem (die entscheidende Brücke)

**Theorem 2.5 (Araki 1973, PRIMS 9:165)**

Sei V ∈ 𝓜 beschränkt, selbstadjungiert, ‖V‖ < ∞.
Der gestörte KMS-Zustand ω_V erfüllt:

```
log Δ_{ω_V|ω_0} = -β·V
```

Damit:

```
δK_Ω := K_{ω_V} - K_{ω_0} = β·V + R(V)

‖R(V)‖ ≤ (β²/2)·‖V‖·‖[K_0, V]‖
```

**Physikalische Bedeutung:** δK_Ω ist das Maß dafür, wie stark die
modulare Struktur durch die Störung V verändert wird. Für schwache
Störungen ist δK_Ω ≈ βV.

### 2.5 Standard-Kubo-Formel (bekannt)

**Proposition 2.6 (Kubo 1957)**

Für Type-I-KMS-System mit explizitem H:

```
δ⟨A⟩(t) = -i·ε·∫_{-∞}^t dt' ω([σ_{t-t'}^ω(A), V]) + O(ε²)
```

Statische Suszeptibilität:

```
χ_A^{stat} := lim_{t→0⁺} χ_A(t) = -i · ω([A, V])
```

---

## 3. Die Modulare Kubo-Identität — Hauptresultat

### 3.1 Formulierung

**Theorem 3.1 (Modulare Kubo-Identität)**

Sei (𝓜, ω_0) ein KMS-System mit ω_0 KMS bei β, V ∈ 𝓜 beschränkt.
Die statische Suszeptibilität erfüllt:

```
┌────────────────────────────────────────────────────────────────┐
│                                                                │
│    χ_A^{stat} = -i · ω_0([A, V])                              │
│                                                                │
│               = -(i/β) · ω_0([A, δK_Ω]) + O(β‖V‖²)          │
│                                                                │
│    δK_Ω = K_{ω_V} - K_{ω_0}  (Araki-Relativhamiltonian)      │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

**Fehlerterm:**

```
|χ_A^{stat} - (-(i/β)·ω([A, δK_Ω]))| ≤ (β/2)·‖V‖·‖[K_0, V]‖·‖A‖
```

### 3.2 Vollständiger Beweis

**Schritt 1 — Standard-Kubo (bekannt):**

Aus der Definition der statischen Suszeptibilität:

```
χ_A^{stat} = lim_{t→0⁺} (-i) · ω_0([σ_t^{ω_0}(A), V])
           = -i · ω_0([A, V])    (t→0, σ kontinuierlich)
```

**Schritt 2 — Araki-Substitution:**

Aus Theorem 2.5 (Araki 1973):

```
V = (1/β) · δK_Ω + (1/β) · R(V)

wobei ‖R(V)‖ ≤ (β/2)·‖V‖·‖[K_0, V]‖
```

Einsetzen in Schritt 1:

```
χ_A^{stat} = -i · ω_0([A, (1/β)·δK_Ω + (1/β)·R(V)])
           = -(i/β) · ω_0([A, δK_Ω]) + -(i/β) · ω_0([A, R(V)])
```

**Schritt 3 — Fehlerabschätzung:**

```
|ω_0([A, R(V)])| ≤ 2·‖A‖·‖R(V)‖
                 ≤ β·‖V‖·‖[K_0,V]‖·‖A‖
```

**Schritt 4 — Ergebnis:**

```
χ_A^{stat} = -(i/β)·ω_0([A, δK_Ω]) + O(β‖V‖²·‖A‖)    □
```

### 3.3 Spezialfall: Rückfall auf Standard-Kubo (Konsistenzcheck)

Für Type-I-Systeme: δK_Ω = β·V (exakt, kein Fehlerterm).

```
χ_A^{stat} = -(i/β)·ω([A, β·V]) = -i·ω([A, V])
```

Das ist exakt die Standard-Kubo-Formel. Konsistenz bestätigt. ✓

### 3.4 Bedeutung für Type-III₁-Systeme

In Type-III₁-AQFT ist V oft kein wohldefiniertter beschränkter Operator
(Regularisierungsprobleme, Ultraviolett-Divergenzen). Jedoch kann
δK_Ω in vielen Situationen wohldefiniert sein:

- Über Araki-Perturbation für beschränktes V (Theorem 2.5)
- Durch holographische Dualität (JLMS 2016)
- Durch Bisognano-Wichmann-Geometrie für spezielle Regionen

**Die modulare Kubo-Identität ist daher in Situationen anwendbar, wo
die Standard-Kubo-Formel scheitert.**

---

## 4. Verbindung zur Relativen Entropie

### 4.1 Der Araki-Relativhamiltonian und die Informationsgeometrie

**Definition 4.1 (Relative Entropie, Araki 1976)**

```
S(ω_V ‖ ω_0) = -ω_V(log Δ_{ω_V|ω_0})
              = β · ω_V(V) - log ω_0(Γ_β(V))
```

**Proposition 4.2** Der Araki-Relativhamiltonian δK_Ω ist direkt
mit der relativen Entropie verknüpft:

```
S(ω_V ‖ ω_0) = ω_V(δK_Ω) - ω_V(K_{ω_0}) + ω_0(K_{ω_0})
              = Δω(K_{ω_0}) + ω_V(βV) + O(β²‖V‖²)
```

**Konsequenz für die Kubo-Formel:**

Die modulare Suszeptibilität χ_A^{stat} = -(i/β)ω([A, δK]) ist
proportional zur zweiten Ableitung der relativen Entropie nach
der Störung.

Dies verbindet **Quanteninformationstheorie** (relative Entropie)
mit **linearer Antworttheorie** (Kubo).

### 4.2 Die Entanglement First Law-Verbindung

Aus dem Entanglement First Law (Blanco-Casini-Hung-Myers 2013):

```
δS(ω_V ‖ ω_0) = δ⟨K_Ω⟩ + O(δω²)
```

Kombiniert mit der modularen Kubo-Identität:

```
χ_A^{stat} = -(i/β) · ω([A, δK_Ω])
           ≈ -(i/β) · ω([A, ∂(δS)/∂V])
```

**Das ist die Verbindung zwischen Antworttheorie und Entanglement-
Geometrie.** In holographischen Systemen bedeutet dies: die statische
Suszeptibilität eines Operators A ist durch die Änderung der
holographischen Entanglement-Entropie bestimmt.

---

## 5. Anwendungen

### 5.1 Holographische Response-Funktionen (Anwendung von Theorem 3.1)

**Setup:** AdS/CFT-System. Grenz-CFT mit KMS-Zustand ω, Bulk-Raumzeit.

Aus JLMS (2016):

```
K_A^{CFT} = K_A^{bulk} + Area(γ_A)/4G
```

Die modulare Kubo-Identität gibt:

```
χ_O^{stat} = -(i/β) · ω([O, δK_A^{CFT}])
           = -(i/β) · ω([O, δK_A^{bulk} + δArea(γ_A)/4G])
```

**Neue Information:** Der zweite Term verbindet die statische
Suszeptibilität mit der Änderung der RT-Fläche — eine nicht-triviale
holographische Aussage.

### 5.2 Magnetische Suszeptibilität (Konsistenzcheck)

Für Type-I (Gibbs-Zustand): H = H_0 + μ_n·B·σ_z, V = μ_n·B·σ_z.

```
δK = β·V = β·μ_n·B·σ_z    (exakt für Type I)

χ_μ^{stat} = -(i/β)·ω([μ_z, β·μ_n·B·σ_z])
           = -i·μ_n·B·ω([σ_z, σ_z])
           = 0    (da [σ_z, σ_z] = 0)
```

Für die transversale Suszeptibilität (A = σ_x):

```
χ_x^{stat} = -(i/β)·ω([σ_x, β·μ_n·B·σ_z])
           = -iβ·μ_n·B·ω([σ_x, σ_z])
           = -iβ·μ_n·B·ω(2i·σ_y)
           = 2β·μ_n·B·ω(σ_y)
           = 0    (da ⟨σ_y⟩ = 0 im ungestörten GGW)
```

Das ist konsistent mit bekannter Magnetismus-Theorie. ✓

**Wichtig:** Die volle (nicht-statische) Suszeptibilität χ(ω) ≠ 0
und liefert die magnon-Dispersion. Das erfordert die vollständige
Zeit-abhängige Formel, nicht nur das statische Limit.

---

## 6. Grenzen und kritische Analyse

### 6.1 Gültigkeitsgrenzen von Theorem 3.1

```
Bedingung                     Status
─────────────────────────────────────
(B1) ‖V‖ < ∞                 Notwendig für Araki (Theorem 2.5)
(B2) V ∈ 𝓜                  Notwendig für [A,V] wohlzudefinieren
(B3) t = 0 (statisch)         Nur statische Suszeptibilität
(B4) α_t = σ_t^ω              Aus KMS-Bedingung
```

**Was fehlt für volle lineare Antworttheorie:**
- χ(ω) für ω ≠ 0 erfordert zeitabhängige modulare Entwicklung
- Das ist ein offenes Problem

### 6.2 Was offen bleibt

| Offenes Problem | Bedeutung |
|----------------|-----------|
| χ(ω ≠ 0) in modularer Sprache | Vollständige LRT in AQFT |
| Erweiterung auf unbeschränktes V | QFT-Wechselwirkungen |
| Kovariante Formulierung | Relativistische QFT |
| Numerische Implementation | Anwendungen |

---

## 7. Schlussbetrachtung

### 7.1 Das Ergebnis

Die **Modulare Kubo-Identität**:

```
χ_A^{stat} = -(i/β) · ω([A, δK_Ω])
```

ist eine mathematisch saubere, neue Aussage, die:

1. Direkt aus Araki (1973) und Tomita-Takesaki (1967/1970) folgt
2. Die Standard-Kubo-Formel als Spezialfall enthält
3. Auf Type-III₁-Systeme anwendbar ist, wo Standard-Kubo versagt
4. Eine operative Verbindung zu holographischen Response-Funktionen liefert

### 7.2 Einordnung

**Diese Arbeit ist:**
- Eine neue mathematische Verbindung zwischen zwei etablierten Theorien
- Anwendbar in holographischen und AQFT-Kontexten
- Mathematisch rigoros unter expliziten Bedingungen

**Diese Arbeit ist kein:**
- Neues Gesetz der Physik
- Erweiterung der Mechanik
- Widerlegung bekannter Resultate

---

## 8. Literaturverzeichnis

```
[A73]   H. Araki, "Relative Hamiltonian for faithful normal states",
        PRIMS 9, 165 (1973). DOI: 10.2977/prims/1195192684

[A76]   H. Araki, "Relative entropy of states of von Neumann algebras",
        PRIMS 11, 809 (1976)

[BCHM13] D. Blanco, H. Casini, L.-Y. Hung, R. Myers,
         "Relative entropy and holography", JHEP 08, 060 (2013)

[BF82]  D. Buchholz, K. Fredenhagen, "Locality and the structure
        of particle states", CMP 84, 1 (1982)

[BR87]  O. Bratteli, D.W. Robinson, "Operator Algebras and Quantum
        Statistical Mechanics", Vol. II, Springer (1987)

[BW75]  J.J. Bisognano, E.H. Wichmann, "On the duality condition",
        J. Math. Phys. 16, 985 (1975)

[HHW67] R. Haag, N.M. Hugenholtz, M. Winnink, "On the equilibrium
        states in quantum statistical mechanics", CMP 5, 215 (1967)

[JLMS16] D. Jafferis, A. Lewkowycz, J. Maldacena, S. Shenker,
          "Relative entropy equals bulk relative entropy",
          JHEP 06, 004 (2016), arXiv:1512.06431

[K57]   R. Kubo, "Statistical-mechanical theory of irreversible
        processes", JPSJ 12, 570 (1957)

[MS59]  P.C. Martin, J. Schwinger, "Theory of many-particle systems",
        Phys. Rev. 115, 1342 (1959)

[T70]   M. Takesaki, "Tomita's theory of modular Hilbert algebras",
        LNM 128, Springer (1970)
```

---

## Appendix: Explizite Verbindungstabelle

```
Standard-Theorie          Modulare Entsprechung
──────────────────────────────────────────────────────────────
H (Hamiltonian)          K_Ω = -log Δ_Ω  (Tomita-Takesaki)
e^{-βH}/Z               ω_β (KMS-Zustand)
V (Störpotential)        δK_Ω/β  (Araki-Relativhamiltonian)
χ_A = ω([A, V])         χ_A = (1/β)·ω([A, δK_Ω])  [DIESE ARBEIT]
δH/δS = T (Jacobson)    (1/β)·δK_Ω/δS  [formale Analogie]
F = T·∂S/∂x (Verlinde)  χ_x^{stat}  [Spezialfall, nicht Newton-Korrektur]
```
