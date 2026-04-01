# Changes to Apply to Your Local Code

Based on the Kiwi.com flight research (weighted average: 6 PHX + 2 SLC couples).

---

## 1. NIGHTS Constant (line ~50)

```js
// Change from:
const NIGHTS = 9;
// To:
const NIGHTS = 7;
```

Routes 7 and 8 already have their own `nights: 6` property and use `route.nights||NIGHTS`, so they're unaffected.

---

## 2. Flight Costs — Budget Tiers

### Route 1: London, Paris & Rome

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1900 | **1080** |
| mid | fall | 2300 | **1430** |
| premium | fall | 2700 | **1780** |
| value | spring | 1700 | **1300** |
| mid | spring | 2050 | **1650** |
| premium | spring | 2400 | **2000** |

### Route 2: Italian Lakes & Alps

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1600 | **950** |
| mid | fall | 2000 | **1300** |
| premium | fall | 2350 | **1650** |
| value | spring | 1400 | **1140** |
| mid | spring | 1750 | **1490** |
| premium | spring | 2100 | **1840** |

### Route 3: Alpine-Adriatic

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1650 | **950** |
| mid | fall | 2050 | **1300** |
| premium | fall | 2400 | **1650** |
| value | spring | 1450 | **1140** |
| mid | spring | 1800 | **1490** |
| premium | spring | 2100 | **1840** |

### Route 4: Germany, Austria & Prague

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1800 | **950** |
| mid | fall | 2200 | **1300** |
| premium | fall | 2600 | **1650** |
| value | spring | 1650 | **1140** |
| mid | spring | 2000 | **1490** |
| premium | spring | 2350 | **1840** |

### Route 5: Portugal & Spain

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1600 | **990** |
| mid | fall | 1950 | **1340** |
| premium | fall | 2300 | **1690** |
| value | spring | 1500 | **1190** |
| mid | spring | 1800 | **1540** |
| premium | spring | 2100 | **1890** |

### Route 6: Salzburg, Dubrovnik & Rome

| Tier | Season | Old | New |
|------|--------|-----|-----|
| value | fall | 1850 | **950** |
| mid | fall | 2250 | **1300** |
| premium | fall | 2650 | **1650** |
| value | spring | 1700 | **1140** |
| mid | spring | 2050 | **1490** |
| premium | spring | 2400 | **1840** |

### Routes 7 & 8: No changes (deal routes have their own pricing)

---

## 3. Flight Cost Source Data

| Route | Gateway | PHX/pp | SLC/pp | Weighted Avg |
|-------|---------|--------|--------|-------------|
| Route 1 | LHR | $1,061 | $1,241 | **$1,080** |
| Route 2 | MUC | $941 | $977 | **$948** |
| Route 3 | MUC | $941 | $977 | **$948** |
| Route 4 | MUC | $941 | $977 | **$948** |
| Route 5 | LIS | $931 | $1,168 | **$990** |
| Route 6 | MUC | $941 | $977 | **$948** |

- **Tier scaling**: mid = value + $350, premium = value + $700
- **Spring scaling**: fall value x 1.20
- **Source**: Kiwi.com, economy class, Oct 1-10 2026 +/- 3 day flex, checked bag included
- Spring 2027 runs ~15-25% higher. Book 4-6 months in advance.

---

## 4. Itinerary Changes (9 nights → 7 nights) for Routes 1-6

### Date ranges
- **Fall**: "Sep 26 – Oct 6, 2026" → **"Sep 26 – Oct 4, 2026"**
- **Spring**: "Apr 24 – May 4, 2027" → **"Apr 24 – May 2, 2027"**

### Route 1: London, Paris & Rome
**Remove**: Day 3 (3rd Cotswolds: Blenheim Palace) and Day 9 (2nd Rome: Vatican)
**Merge**: Blenheim Palace into Day 2 desc. Vatican/Sistine Chapel into the remaining Rome day.

New itinerary (fall dates shown, spring follows same pattern Apr 24 – May 2):
| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → London | (travel, nights:0) |
| 1 | Sep 27 | Cotswolds | Arrive, Bibury, Arlington Row (nights:1) |
| 2 | Sep 28 | Cotswolds | Bourton-on-the-Water, **Blenheim Palace visit**. Cream tea. Broadway Tower sunset. (nights:1) |
| 3 | Sep 29 | London | Train to London. Churchill War Rooms. Borough Market. Tower Bridge. (nights:1) |
| 4 | Sep 30 | London → Paris | Neal's Yard. Eurostar. Eiffel Tower sunset. (nights:1) |
| 5 | Oct 1 | Paris | Louvre. Tuileries. Sainte-Chapelle. Le Marais. (nights:1) |
| 6 | Oct 2 | Paris → Rome | Montmartre. Sacré-Cœur. Flight to Rome. Trastevere dinner. (nights:1) |
| 7 | Oct 3 | Rome | Colosseum & Forum. Rome Temple. **Vatican Museums & Sistine Chapel. Trevi Fountain.** Farewell dinner Trastevere. (nights:1) |
| 8 | Oct 4 | Rome → Home | (travel, nights:0) |

**Highlights**: Change "3 days in the English countryside" → "2 days in the English countryside"
**Accom**: Cotswolds n:3→**n:2**, Rome n:3→**n:2**

### Route 2: Italian Lakes & Alps
**Remove**: Day 2 (Neuschwanstein day trip) and Day 9 (2nd Lake Como)
**Merge**: Neuschwanstein as "optional day trip" in Munich desc. Bellagio ferry into single Como day.

| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → Munich | (travel, nights:0) |
| 1 | Sep 27 | Munich | Arrive. Marienplatz, Viktualienmarkt, English Garden. Beer hall. **Optional Neuschwanstein day trip.** (nights:1) |
| 2 | Sep 28 | Salzburg | Scenic train 1.5h. Old Town, Getreidegasse, Mozart. Concert. (nights:1) |
| 3 | Sep 29 | Sound of Music Day | Mirabell, Mondsee, Hohensalzburg. (nights:1) |
| 4 | Sep 30 | Innsbruck | Scenic train 2h. Golden Roof, Nordkette cable car. (nights:1) |
| 5 | Oct 1 | Bolzano / Dolomites | Brenner Pass train. Wine country. Ötzi Museum. (nights:1) |
| 6 | Oct 2 | Dolomites Day | Seceda cable car. Mountain hut lunch. Val di Funes. (nights:1) |
| 7 | Oct 3 | Lake Como | Train to Varenna. Villa Monastero. **Ferry to Bellagio, Villa Melzi.** Farewell dinner. (nights:1) |
| 8 | Oct 4 | Milan → Home | (travel, nights:0) |

**Accom**: Munich/Bavaria n:2→**n:1**, Lake Como n:2→**n:1**

### Route 3: Alpine-Adriatic
**Remove**: Day 2 (Neuschwanstein) and Day 7 (Split full day)
**Merge**: Split content (Diocletian's, Riva) into the travel-to-Split day.

| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → Munich | (travel, nights:0) |
| 1 | Sep 27 | Munich | Arrive. LDS church. Marienplatz. Beer hall. (nights:1) |
| 2 | Sep 28 | Salzburg | Scenic train. Old Town. Mozart. Concert. (nights:1) |
| 3 | Sep 29 | Sound of Music Day | Mirabell, Mondsee, Hohensalzburg. (nights:1) |
| 4 | Sep 30 | Lake Bled | Train via Ljubljana. Pletna boat. Cream cake. Alps sunset. (nights:1) |
| 5 | Oct 1 | → Split | Bled Castle morning. Train to Split. **Diocletian's Palace, Riva promenade.** Seafood dinner. (nights:1) |
| 6 | Oct 2 | Dubrovnik | Scenic Adriatic transfer. Stradun. Sunset from walls. (nights:1) |
| 7 | Oct 3 | Dubrovnik | City walls. Kayaking. Cobblestone exploring. Farewell dinner. (nights:1) |
| 8 | Oct 4 | Dubrovnik → Home | (travel, nights:0) |

**Accom**: Munich/Bavaria n:2→**n:1**, Split/Dalmatia n:2→**n:1**

### Route 4: Germany, Austria & Prague
**Remove**: Day 8 (3rd Prague: Jewish Quarter) and Day 9 (Nuremberg)
**Merge**: Jewish Quarter/Lennon Wall into Prague day 7. Fly home from Prague instead of Nuremberg.

| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → Munich | (travel, nights:0) |
| 1 | Sep 27 | Munich | Same as before. (nights:1) |
| 2 | Sep 28 | Neuschwanstein & Salzburg | Same as before. (nights:1) |
| 3 | Sep 29 | Salzburg | Same as before. (nights:1) |
| 4 | Sep 30 | Salzburg → Vienna | Same as before. (nights:1) |
| 5 | Oct 1 | Vienna | Same as before. (nights:1) |
| 6 | Oct 2 | Vienna → Prague | Same as before. (nights:1) |
| 7 | Oct 3 | Prague | Castle, St. Vitus, Petřín Hill. **Jewish Quarter. Lennon Wall & Kampa Island.** Astronomical Clock. Farewell dinner. (nights:1) |
| 8 | Oct 4 | Prague → Home | Morning walk. **Fly home from Prague.** (travel, nights:0) |

**Cities**: Remove "Nuremberg" → `["Munich","Salzburg","Vienna","Prague"]`
**CityFlags**: Remove last → `["🇩🇪","🇦🇹","🇦🇹","🇨🇿"]`
**Accom**: Prague n:3→**n:2**, **remove Nuremberg entry entirely**
**Weather**: Remove Nuremberg entry
**Inspiration**: Remove Nuremberg entry
**TrainLegs**: Remove Prague→Nuremberg leg

### Route 5: Portugal & Spain
**Remove**: Day 3 (3rd Lisbon: Belém/LX Factory) and Day 9 (3rd San Sebastián: day trip)
**Merge**: Belém/Jerónimos into Sintra day. Farewell content into remaining San Sebastián day.

| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → Lisbon | (travel, nights:0) |
| 1 | Sep 27 | Lisbon | Arrive. Alfama, Tram 28, Pastéis de Belém, Fado dinner. (nights:1) |
| 2 | Sep 28 | Lisbon & Sintra | Sintra (Pena Palace). **Belém Tower & Jerónimos Monastery.** Time Out Market. (nights:1) |
| 3 | Sep 29 | Lisbon → Porto | Train 2.5h. São Bento. Ribeira. Port wine. Dom Luís I Bridge. (nights:1) |
| 4 | Sep 30 | Porto | Livraria Lello. Clérigos. Bolhão Market. Serralves. Francesinha. (nights:1) |
| 5 | Oct 1 | Porto → Santiago | Train 3h. Cathedral. Old town. Galician seafood. (nights:1) |
| 6 | Oct 2 | Santiago → San Sebastián | Flight to Bilbao. Bus to San Sebastián. La Concha. Pintxos. (nights:1) |
| 7 | Oct 3 | San Sebastián | Monte Urgull. La Bretxa. Pintxos masterclass. La Concha. **Basque cider house. Farewell dinner.** (nights:1) |
| 8 | Oct 4 | San Sebastián → Home | (travel, nights:0) |

**Accom**: Lisbon n:3→**n:2**, San Sebastián n:3→**n:2**

### Route 6: Salzburg, Dubrovnik & Rome
**Remove**: Day 6 (3rd Dubrovnik: cable car/kayak) and Day 9 (2nd Rome: Vatican)
**Merge**: Cable car/kayak into Dubrovnik day 5. Vatican into Rome day 7.

| Day | Date | Location | Description |
|-----|------|----------|-------------|
| 0 | Sep 26 | U.S. → Salzburg | (travel, nights:0) |
| 1 | Sep 27 | Salzburg | Same as before. (nights:1) |
| 2 | Sep 28 | Salzburg | Same as before. (nights:1) |
| 3 | Sep 29 | Salzburg → Ljubljana | Same as before. (nights:1) |
| 4 | Sep 30 | Ljubljana → Dubrovnik | Same as before. (nights:1) |
| 5 | Oct 1 | Dubrovnik | City Walls. Lokrum Island. **Cable car to Mt Srđ. Kayak.** Old Town dinner. (nights:1) |
| 6 | Oct 2 | Dubrovnik → Rome | Morning farmers market. Flight to Rome. Trastevere dinner. (nights:1) |
| 7 | Oct 3 | Rome | Rome Temple. Colosseum & Forum. **Vatican Museums & Sistine Chapel. Trevi Fountain.** Farewell dinner Trastevere. (nights:1) |
| 8 | Oct 4 | Rome → Home | (travel, nights:0) |

**Accom**: Dubrovnik n:3→**n:2**, Rome n:3→**n:2**

---

## 5. Overview Screen Text

Change "6 curated routes" to "8 curated routes" in the overview description.

---

## 6. UI Code — Pass `nights` Parameter

Everywhere `calcPP` or `calcCouple` is called, pass `route.nights||NIGHTS` as the second argument so Routes 7-8 (with `nights:6`) calculate correctly.

Search for these patterns and update:
- `calcCouple(route.budgetTiers.spring.mid)` → `calcCouple(route.budgetTiers.spring.mid, route.nights||NIGHTS)`
- `calcCouple(route.budgetTiers.fall.mid)` → `calcCouple(route.budgetTiers.fall.mid, route.nights||NIGHTS)`
- In OverviewTab: `const pp = calcPP(t);` → `const rn = route.nights||NIGHTS; const pp = calcPP(t, rn);`
- In OverviewTab: `calcCouple(t)` → `calcCouple(t, rn)`
- In OverviewTab pie chart: `tiers.mid.accommodation*NIGHTS` → `tiers.mid.accommodation*rn` (and same for food, misc)
- In CompareTab: `calcCouple(route.budgetTiers.fall.mid)` → add `const rn = route.nights||NIGHTS;` then pass `rn`
