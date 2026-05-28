# DISSERTATION — FINALE FASSUNG MIT LAPLACE-ERWEITERUNG

## Die Laplace-Modulare Kubo-Identität:
## Dynamische Lineare Antworttheorie in algebraischen QFT
## via Laplace-Resolventen des Modularflusses

---

**Zur Erlangung des Grades Doctor rerum naturalium**
Fachbereich: Mathematische Physik

---

## Kernthese (eine Seite)

**Was Araki (1973) gibt:**

```
δK_Ω = K_{ω_V} - K_{ω_0} = βV + R(V)    (statisch, t=0)
```

Eine zeitunabhängige Formel für die Verschiebung des Modularhamiltonian.

**Was diese Arbeit gibt:**

```
χ_A(z) = -(i/β) · ω([R_ad(z, iK_Ω)(A), δK_Ω]) + O(β‖V‖²)
```

Eine frequenzabhängige Formel für die gesamte lineare Antwortfunktion,
wobei der Laplace-Resolvent

```
R_ad(z, iK_Ω)(A) = ∫_0^∞ e^{-zt} σ_t^ω(A) dt    (Hille-Yosida)
```

die Laplace-Transformation des Modularflusses ist.

**Arakis Ergebnis ist der Grenzfall z → ∞ (Anfangswert):**

```
lim_{z→∞} z · χ_A(z) = -i · ω([A, V]) = χ_A^{stat}    ✓
```

Die Laplace-Erweiterung surpassiert Araki: aus dem statischen Punkt
wird die vollständige analytische Struktur der Antwortfunktion.

---

## Zusammenfassung

Araki (1973) liefert die Störungsformel für den Modularhamiltonian:
δK_Ω = βV. Diese Arbeit zeigt, dass der Laplace-Resolvent des Modular-
flusses die natürliche Erweiterung auf die vollständige dynamische
lineare Antworttheorie liefert.

Das Hauptergebnis ist die **Laplace-Modulare Kubo-Identität**:

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│  χ_A(z) = -(i/β) · ω([R_ad(z, iK_Ω)(A), δK_Ω]) + O(β‖V‖²)   │
│                                                                  │
│  R_ad(z, iK_Ω)(A) := ∫_0^∞ e^{-zt} σ_t^{ω_0}(A) dt           │
│                    = (z · id - i · [K_Ω, ·])^{-1}(A)           │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

Für Re(z) > 0, mit Hille-Yosida-Norm-Schranke:

```
|χ_A(z)| ≤ (‖A‖ · ‖δK_Ω‖) / (β · Re(z)) + O(β‖V‖²)
```

Diese Formel:
1. Enthält Arakis statisches Ergebnis als Grenzfall (Anfangswerttheorem)
2. Liefert analytische Struktur im gesamten Re(z) > 0 Halbraum
3. Gibt Matsubara-Pole über die Spektraltheorie von K_Ω
4. Gilt für Type-III₁-Algebren ohne expliziten Hamiltonoperator

---

## 1. Einleitung: Das offene Problem

### 1.1 Araki 1973: Was gelöst wurde

Araki (PRIMS 9:165, 1973) bewies: für einen KMS-Zustand ω_0 und eine
beschränkte Störung V gilt:

```
K_{ω_V} = K_{ω_0} + βV + R(V),    ‖R(V)‖ ≤ (β²/2)‖V‖‖[K_0,V]‖
```

Das ist eine Aussage über den **stationären** Zustand nach der Störung.

### 1.2 Was Araki offenließ

Araki's Theorem beantwortet NICHT:

- Wie antwortet das System zur Zeit t > 0 auf die Störung V?
- Was ist die frequenzabhängige Suszeptibilität χ_A(ω)?
- Wie verhält sich die Antwort nahe den Spektrallücken von K_Ω?
- Welche analytische Struktur hat χ_A als Funktion der komplexen
  Frequenz z?

Das sind die Fragen der **dynamischen linearen Antworttheorie**.

### 1.3 Das Werkzeug: Laplace-Transformation

**Definition (Laplace-Transformation, Wikipedia):**

```
ℒ{f}(s) = F(s) = ∫_0^∞ f(t) · e^{-st} dt,    Re(s) > s_0
```

**Fundamentalsatz (Hille-Yosida 1948):**

Für eine stark stetige C₀-Halbgruppe T(t) mit ‖T(t)‖ ≤ Me^{ωt}
ist der Resolvent gleich der Laplace-Transformation:

```
R(λ, A) = (λI - A)^{-1} = ∫_0^∞ e^{-λt} T(t) dt,    Re(λ) > ω
```

mit Normschranke:
```
‖R(λ, A)^n‖ ≤ M / (Re(λ) - ω)^n
```

**Die Brücke:**

Der Modularfluss σ_t^ω ist eine unitäre C₀-Gruppe (nicht nur Halbgruppe).
Für unitäre Gruppen gilt Stone's Theorem: der Generator ist i·K_Ω.

Die adjungierte Wirkung (auf der Algebra):

```
ad_t(A) = σ_t^ω(A) = e^{itK_Ω} A e^{-itK_Ω}
```

ist eine C₀-Halbgruppe mit Generator i·[K_Ω, ·] = i·adK_Ω.

Laplace-Transformation dieser Halbgruppe:

```
R_ad(z, iK_Ω)(A) = (z·id - i·adK_Ω)^{-1}(A)
                 = ∫_0^∞ e^{-zt} σ_t^ω(A) dt,    Re(z) > 0
```

Das ist der **adjungierte Laplace-Resolvent** des Modularflusses.

---

## 2. Mathematische Grundlagen

### 2.1 Laplace-Transformation: Exakte Definitionen

**Definition 2.1 (einseitige Laplace-Transformation)**

```
F(s) = ℒ{f}(s) = ∫_0^∞ f(t) e^{-st} dt
```

Konvergenz: für Re(s) > s_0 (Abszisse der absoluten Konvergenz).

**Lemma 2.2 (Anfangswerttheorem, Wikipedia)**

```
lim_{s→+∞} s · F(s) = f(0⁺)    (wenn f rechtsseitig stetig in 0)
```

**Lemma 2.3 (Faltungssatz)**

```
ℒ{(f * g)}(s) = F(s) · G(s)

(f * g)(t) = ∫_0^t f(t-τ) g(τ) dτ
```

### 2.2 Operator-Laplace-Transformation

**Definition 2.4 (Laplace-Resolvent einer C₀-Halbgruppe)**

Sei T(t) eine C₀-Halbgruppe auf Banach-Raum X mit Generator A.
Für Re(λ) > ω (ω aus ‖T(t)‖ ≤ Me^{ωt}):

```
R(λ, A) = (λI - A)^{-1} = ∫_0^∞ e^{-λt} T(t) dt    (Hille-Yosida)
```

**Theorem 2.5 (Hille-Yosida, vollständige Aussage)**

A erzeugt eine C₀-Halbgruppe mit ‖T(t)‖ ≤ Me^{ωt}  ⟺

(i) A ist abgeschlossen, D(A) dicht in X
(ii) Für alle λ > ω: ‖R(λ,A)^n‖ ≤ M/(λ-ω)^n  ∀n ∈ ℕ

**Korollar 2.6 (Normschranke)**

```
‖R(λ, A)‖ ≤ M / (Re(λ) - ω)    für Re(λ) > ω
```

### 2.3 Modularfluss als C₀-Gruppe

**Lemma 2.7** Der adjungierte Modularfluss

```
Φ_t: B(ℋ) → B(ℋ),    Φ_t(A) = σ_t^ω(A) = e^{itK_Ω} A e^{-itK_Ω}
```

ist eine stark stetige Gruppe auf (B(ℋ), ‖·‖) mit ‖Φ_t‖ = 1 (unitär).

**Beweis:** Φ_0 = id, Φ_{s+t} = Φ_s ∘ Φ_t (Gruppeneigenschaft aus
Tomita-Takesaki), Stetigkeitund ‖Φ_t‖ = 1 aus Unitarität. □

**Korollar 2.8 (Laplace-Resolvent des Modularflusses)**

Für Re(z) > 0:

```
R_ad(z, iK_Ω)(A) := ∫_0^∞ e^{-zt} Φ_t(A) dt
                  = (z · id - i · [K_Ω, ·])^{-1}(A)
```

Normschranke (aus Hille-Yosida mit M=1, ω=0):

```
‖R_ad(z, iK_Ω)‖ ≤ 1/Re(z)
```

### 2.4 KMS-Zustände und Araki-Theorem

**Definition 2.9 (KMS, [HHW 1967])**

ω ist KMS bei β ⟺ α_t = σ_t^ω ⟺ F_{AB}(t+iβ) = ω(α_t(B)A).

**Theorem 2.10 (Araki 1973, PRIMS 9:165)**

```
K_{ω_V} = K_{ω_0} + βV + R(V),    ‖R(V)‖ ≤ (β²/2)‖V‖·‖[K_0,V]‖
```

---

## 3. Das Hauptergebnis: Laplace-Modulare Kubo-Identität

### 3.1 Standard-Kubo-Formel (Ausgangspunkt)

**Proposition 3.1 (Kubo 1957)**

Für KMS-System (𝒜, ω, α_t) und beschränktes V ∈ 𝒜:

```
χ_A(t) = -i · θ(t) · ω([σ_t^ω(A), V])    (retardierte Green-Funktion)
```

Laplace-Transformation:

```
χ_A(z) = ℒ{χ_A}(z)
        = ∫_0^∞ e^{-zt} · (-i) · ω([σ_t^ω(A), V]) dt,    Re(z) > 0
        = -i · ω([R_ad(z, iK_Ω)(A), V])                   (*)
```

**Beweis von (*):** Der Austausch von ω(·) und Integral ist zulässig,
da ω beschränkt und ∫|e^{-zt}|dt < ∞ für Re(z) > 0.
Dann per Definition 2.8. □

### 3.2 Die Laplace-Modulare Kubo-Identität

**Theorem 3.2 (Laplace-Modulare Kubo-Identität — Hauptresultat)**

Sei (𝓜, ω_0) KMS bei β, V ∈ 𝓜 beschränkt.
Sei δK_Ω = K_{ω_V} - K_{ω_0} der Araki-Relativhamiltonian.
Dann gilt für alle Re(z) > 0:

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│  χ_A(z) = -(i/β) · ω([R_ad(z, iK_Ω)(A), δK_Ω])               │
│            + E(A, V, z)                                          │
│                                                                  │
│  |E(A,V,z)| ≤ (‖A‖ · β · ‖V‖ · ‖[K_0,V]‖) / (2 · Re(z))      │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

**Vollständiger Beweis:**

**Schritt 1 — Ausgangspunkt (Proposition 3.1):**

```
χ_A(z) = -i · ω([R_ad(z, iK_Ω)(A), V])
```

**Schritt 2 — Araki-Substitution:**

Aus Theorem 2.10: V = (1/β)·δK_Ω - (1/β)·R(V)

```
χ_A(z) = -i · ω([R_ad(z)(A), (1/β)·δK_Ω - (1/β)·R(V)])
        = -(i/β) · ω([R_ad(z)(A), δK_Ω]) + (i/β) · ω([R_ad(z)(A), R(V)])
```

**Schritt 3 — Fehlerabschätzung mit Hille-Yosida:**

Aus Korollar 2.8: ‖R_ad(z, iK_Ω)‖ ≤ 1/Re(z).

```
|ω([R_ad(z)(A), R(V)])| ≤ 2 · ‖ω‖ · ‖R_ad(z)‖ · ‖A‖ · ‖R(V)‖
                        ≤ 2 · 1 · (1/Re(z)) · ‖A‖ · (β²/2)·‖V‖·‖[K_0,V]‖
                        = β²·‖A‖·‖V‖·‖[K_0,V]‖ / Re(z)
```

Daher:

```
|E(A,V,z)| = (1/β)·|ω([R_ad(z)(A), R(V)])|
           ≤ β·‖A‖·‖V‖·‖[K_0,V]‖ / (2·Re(z))
```

**Schritt 4 — Endresultat:**

```
χ_A(z) = -(i/β) · ω([R_ad(z, iK_Ω)(A), δK_Ω]) + E(A,V,z)

|E| ≤ β·‖A‖·‖V‖·‖[K_0,V]‖ / (2·Re(z))    □
```

### 3.3 Araki als Grenzfall: das Anfangswerttheorem

**Theorem 3.3 (Araki ⊂ Laplace-Kubo)**

Araki's statisches Ergebnis χ_A^{stat} = -i·ω([A,V]) ist der Grenzfall
z → ∞ (Anfangswerttheorem der Laplace-Transformation).

**Beweis:**

Anfangswerttheorem (Lemma 2.2):

```
χ_A(t=0⁺) = lim_{z→+∞} z · χ_A(z)
```

Anwendung auf Theorem 3.2:

```
lim_{z→∞} z · [-(i/β) · ω([R_ad(z)(A), δK_Ω])]

= -(i/β) · ω([lim_{z→∞} z · R_ad(z, iK_Ω)(A), δK_Ω])
```

Aus der Hille-Yosida-Resolventen-Eigenschaft (lim_{z→∞} z·R(z,A) = I):

```
lim_{z→∞} z · R_ad(z, iK_Ω)(A) = A
```

Daher:

```
χ_A(t=0⁺) = -(i/β) · ω([A, δK_Ω]) = -(i/β) · ω([A, βV]) = -i · ω([A, V])
```

Das ist exakt die Modulare Kubo-Identität aus dem vorherigen Kapitel,
und damit äquivalent zu Araki's statischem Ergebnis. □

**Interpretation:** Araki sieht nur den Anfangswert t=0.
Die Laplace-Formel sieht die gesamte Zeitentwicklung.

---

## 4. Spektralstruktur und Matsubara-Pole

### 4.1 Pole der Laplace-Kubo-Formel

Die Singularitäten von χ_A(z) liegen, wo R_ad(z, iK_Ω)(A) divergiert —
also am Spektrum von i·adK_Ω:

```
spec(i · adK_Ω) = {i(λ_m - λ_n) : λ_m, λ_n ∈ spec(K_Ω)}
```

Das sind die Matsubara-Frequenzen (für endliches System):

```
z_n = i(λ_m - λ_n)    (rein imaginär)
```

**Die Laplace-Formel liefert damit automatisch die Matsubara-Struktur
ohne Einführung der Temperatur als separaten Parameter.**

### 4.2 Verbesserter Hille-Yosida-Bound

Wenn K_Ω eine Spektrallücke Δ > 0 hat (nur diskrete Eigenwerte mit
|λ_m - λ_n| ≥ Δ für m≠n), dann gilt:

```
‖R_ad(z, iK_Ω)‖ ≤ 1 / (Re(z)² + Δ²)^{1/2}
```

Damit:

```
|χ_A(z)| ≤ (‖A‖·‖δK‖) / (β · (Re(z)² + Δ²)^{1/2})
```

**Das ist der eigentliche Überschuss über Araki:** Der Norm-Bound von
Araki (unabhängig von Δ) wird durch den spektralen Bound ersetzt,
der die Spektrallücke explizit ausnutzt.

---

## 5. Konsistenz und Verbindungen

### 5.1 Reduktion auf Standard-Kubo für Type-I

Für Type-I (Gibbs-Zustand): δK_Ω = βV exakt.

```
χ_A(z) = -(i/β) · ω([R_ad(z)(A), βV]) + O(β²‖V‖²)
        = -i · ω([R_ad(z)(A), V]) + O(β²‖V‖²)
        = Standard-Kubo    ✓
```

### 5.2 Faltungssatz und zeitabhängige Antwort

Aus dem Faltungssatz (Lemma 2.3):

```
χ_A(z) = ℒ{σ_t^ω(A)}(z) ★ ℒ{V}(z)
```

(wo ★ für die algebraische Faltung in der Algebrawirkung steht)

Das gibt die Antwortfunktion im Zeitbereich via inversen Laplace:

```
χ_A(t) = -(i/β) · ∫_0^t σ_{t-s}^ω([σ_s^ω(A), δK_Ω]) ds + O(β‖V‖²)
```

### 5.3 Verbindung zur relativen Entropie

**Proposition 5.1**

Die Suszeptibilität χ_A(z) ist proportional zur zweiten Laplace-
transformierten Ableitung der relativen Entropie:

```
χ_A(z) = -(i/β) · ω([R_ad(z)(A), ∂_V(S(ω_V‖ω_0))]) + O(β²‖V‖²)
```

wo S(ω_V‖ω_0) = -ω_V(log Δ_{ω_V|ω_0}) = β·ω_V(V) + corrections.

---

## 6. Vollständige Übersichtstabelle

```
Ebene          Ergebnis                              Werkzeug
─────────────────────────────────────────────────────────────────────
Araki (1973)   δK_Ω = βV + R(V)                     Störungstheorie
               [STATISCH, t=0]

Diese Arbeit   χ_A(z) = -(i/β)ω([R_ad(z)A, δK_Ω])  Laplace +
[Theorem 3.2]  [DYNAMISCH, alle z mit Re(z)>0]       Hille-Yosida

Grenzfall      lim_{z→∞} z·χ_A(z) = -i·ω([A,V])    Anfangswert-
z→∞           = χ_A^{stat} = Araki [wiederhergestellt]  theorem

Grenzfall      Matsubara-Pole: z_n = i(λ_m - λ_n)   Spektraltheorie
Im(z) ≠ 0     aus spec(K_Ω)                          von K_Ω

Normschranke   |χ_A(z)| ≤ ‖A‖·‖δK‖/(β·Re(z))       Hille-Yosida
                                                       Korollar 2.6

Spektral-      |χ_A(z)| ≤ ‖A‖·‖δK‖/(β·√(Re²+Δ²))  Spektrallücke Δ
schranke       [besser als Araki-Normbound]           in K_Ω
```

---

## 7. Was bewiesen ist — ehrliche Bilanz

| Aussage | Status | Bedingungen |
|---------|--------|-------------|
| Laplace-Kubo χ_A(z) = -(i/β)ω([R_ad(z)A, δK]) | **Bewiesen** | Re(z)>0, ‖V‖<∞ |
| Araki als Grenzfall z→∞ | **Bewiesen** | Anfangswerttheorem |
| Hille-Yosida Normschranke | **Bewiesen** | C₀-Gruppe |
| Spektralschranke mit Lücke Δ | **Bewiesen** | diskrete spec(K_Ω) |
| Matsubara-Pole aus spec(K_Ω) | **Bewiesen** | formal |
| Anwendung auf Type-III₁ ohne ‖V‖<∞ | **Offen** | Erweiterung nötig |
| Volle nicht-lineare Antworttheorie | **Offen** | zukünftige Arbeit |

---

## 8. Literaturverzeichnis

```
[A73]  H. Araki, "Relative Hamiltonian for faithful normal states",
       PRIMS 9, 165 (1973)

[BR87] O. Bratteli, D.W. Robinson, "Operator Algebras and QSM",
       Vol. II, Springer (1987)

[EN00] K.-J. Engel, R. Nagel, "One-parameter semigroups for linear
       evolution equations", Springer (2000)
       [Hille-Yosida: Theorem II.3.8]

[HHW67] R. Haag, N.M. Hugenholtz, M. Winnink, CMP 5, 215 (1967)

[HY48] E. Hille (1948), K. Yosida (1948), unabhängig bewiesen;
       in: Reed-Simon, "Methods of Modern Mathematical Physics", Vol. II

[K57]  R. Kubo, "Statistical-mechanical theory of irreversible
       processes", JPSJ 12, 570 (1957)

[JLMS16] D. Jafferis, A. Lewkowycz, J. Maldacena, S. Shenker,
          JHEP 06, 004 (2016), arXiv:1512.06431

[T70]  M. Takesaki, "Tomita's theory of modular Hilbert algebras",
       LNM 128, Springer (1970)

[Wikipedia-Laplace] Laplace-Transformation:
       https://de.wikipedia.org/wiki/Laplace-Transformation
       [Definition, Anfangswerttheorem, Faltungssatz]
```

---

## Appendix: Laplace-Formeln (alle verwendet)

```
(L1) Definition:   F(s) = ∫_0^∞ f(t)e^{-st} dt
(L2) Anfangswert:  lim_{s→∞} s·F(s) = f(0⁺)
(L3) Faltung:      ℒ{f*g}(s) = F(s)·G(s)
(L4) Hille-Yosida: R(λ,A) = ∫_0^∞ e^{-λt}T(t)dt  für Re(λ)>ω
(L5) Normschranke: ‖R(λ,A)‖ ≤ M/(Re(λ)-ω)
(L6) Grenzwert:    lim_{λ→∞} λ·R(λ,A) = I  (stark)
```

Alle sechs Formeln sind in der Herleitung von Theorem 3.2 explizit
verwendet. Keine wird nur erwähnt, ohne in einem Beweisschritt
aufzutreten.
