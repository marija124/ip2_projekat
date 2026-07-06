# NBA Database - Klasterovanje

Seminarski rad iz predmeta **Istraživanje podataka 2** na Matematičkom fakultetu Univerziteta u Beogradu.

**Autori:** Marija Grekulović (264/2019), Stepan Ignjatović (128/2021)

## Opis projekta

Analiza NBA baze podataka primenom šest algoritama klasterovanja na dva nivoa:
- **Tim-sezone**: Klasterovanje tim-sezona na osnovu statistike utakmica
- **Igrači**: Klasterovanje igrača na osnovu fizičkih i atletskih merenja (NBA Draft Combine)

##  Algoritmi klasterovanja

1. **K-Means** - particionisanje
2. **Aglomerativno (hijerarhijsko) klasterovanje** - hijerarhijski pristup
3. **Bisecting K-Means** - divizivni pristup
4. **DBSCAN** - klasterovanje bazano na gustini
5. **Gaussian Mixture Model (GMM)** - statistički model sa mekim klasterovanjem
6. **Spectral Clustering** - klasterovanje preko grafa sličnosti

##  Skup podataka

Korišćena je **NBA Database** sa Kaggle platforme:
- **65.698 utakmica** (1946-2022)
- **4.815 igrača**
- **30 timova**

### Tim-sezone (1.519 sloga)
- 38 atributa: prosečne statistike po utakmici (napad i odbrana)
- Pokazatelji: poeni, asistencije, skokovi, blokade, ukradene lopte, greške, šutevi...

### Igrači (1.016 sloga)
- 9 atributa fizičkih i atletskih merenja:
  - Visina, težina, raspon ruku, dohvat
  - Procenat telesne masti
  - Vertikalni skokovi (iz mesta i iz zaleta)
  - Lane agility test, sprint



##  Pokretanje

### Prerequisiti
```bash
pip install pandas scikit-learn numpy matplotlib seaborn kagglehub jupyter
```

### Automatski preuzimanje podataka
```python
import kagglehub

# Preuzimanje NBA baze
path = kagglehub.dataset_download("wyattowalsh/basketball")
```

### Pokretanje analize
```bash
jupyter notebook NBA_Clustering_Analysis.ipynb
```






##  Sačuvani modeli

Svi modeli su sačuvani u **joblib formatu** za ponovljivost:



##  Dokumentacija

Detaljno objašnjenje svih koraka, rezultata i tumačenja dostupno je u PDF seminarskom radu.

---

**Datum:** Jul 2026  
Matematički fakultet, Univerzitet u Beogradu
