[README_despeses.md](https://github.com/user-attachments/files/27962028/README_despeses.md)
# 💶 Despeses en Metàl·lic

App per registrar els pagaments en metàl·lic de casa, tant personals com comuns, i exportar-los en format compatible amb l'Excel de control de despeses familiar.

---

## 📱 Instal·lació al mòbil

1. Obre Safari i accedeix a la URL de l'app
2. Prem el botó de compartir (quadrat amb fletxa cap amunt)
3. Selecciona **"Afegir a pantalla d'inici"**
4. Posa-li el nom **"Despeses"** i prem **"Afegir"**

> ⚠️ Cal obrir-la sempre des de Safari (no Chrome ni cap altre navegador) perquè les dades es guardin correctament.

---

## 🗂️ Estructura de l'app

L'app té tres pestanyes:

### Llista
Mostra tots els moviments pendents d'exportar. Es poden filtrar per tipus (Personal / Comuna) o per categoria.

### Resum
Totals del mes agrupats per tipus i per categoria, amb gràfic de barres.

### Ajustos
Gestió de les categories personals i comunes. També permet esborrar totes les dades.

---

## ➕ Afegir un moviment

1. Prem el botó **+** (part inferior dreta)
2. Selecciona el tipus:
   - 🔵 **Personal** — despesa del compte personal
   - 🟢 **Comuna** — despesa del compte familiar compartit
3. Omple la categoria, el concepte, l'import i la data
4. Prem **Guardar**

> Les despeses comunes s'acumulen automàticament al **saldo pendent de regularitzar**.

---

## 🔄 Regularització de despeses comunes

Quan pagues despeses comunes amb diners personals, cal recuperar-los del compte comú al caixer.

**Com funciona:**
1. Cada despesa comuna afegida suma al saldo pendent (banner verd a la part superior)
2. Quan vas al caixer, prem **"Regularitzar"**
3. L'app suggereix automàticament l'import en bitllets de 50€ i 20€ sense superar el total
4. Confirma l'import tret i la data

> El saldo pendent es conserva fins i tot després d'exportar, ja que la regularització és un moviment independent.

---

## 📤 Exportar a Excel

1. Prem el botó **"Exportar CSV"** (part superior dreta de la pestanya Llista)
2. El fitxer es desa automàticament a **iCloud Drive → Descàrregues**
3. Des de l'ordinador, mou el fitxer de iCloud a Dropbox
4. Obre l'Excel de control de despeses
5. Obre el fitxer exportat i copia les files a la pestanya corresponent:
   - Moviments **personals** → pestanya **"Llistat de moviments Albert"**
   - Moviments **comuns** → pestanya **"Llistat de moviments Comú"**

**Format del fitxer exportat:**

| Data | Compte | Categoría | Concepte | Import | Comptabilitzat |
|------|--------|-----------|----------|--------|----------------|
| 45659 | En Metàl·lic | Oci | Cinema | -12.50 | *(fórmula Excel)* |

> La columna **Data** exporta en format numèric d'Excel. Si la columna de l'Excel ja té format de data, es mostrarà correctament en enganxar-la.
> La columna **Comptabilitzat** la gestiona automàticament la fórmula de l'Excel.

> ⚠️ En exportar, els moviments s'esborren de l'app. El saldo pendent de regularització es conserva.

---

## 📂 Categories

### Personals (pestanya "Llistat de moviments Albert")
ACNUR, Associació Espanyola contra el càncer, Escola d'Anglès, Farmàcia, Impostos, Magatzem de Benavent, Metges, Oci, Perruquer, Quota Gimnàs Albert, Quota Gimnàs Maria, Roba i calçat, Seguretat Social, Varies

### Comunes (pestanya "Llistat de moviments Comú")
Abril. Escola de música, Abril. Estudis, Abril. Llibres, Abril. Metges, Casa. Abastament Aigua, Casa. Calefacció, Casa. Hipoteca, Casa. Manteniment, Casa. Neteja, General. Alimentació, General. Assegurances, General. Assessorament fiscal, General. Efectiu, General. Electricitat, General. Oci, General. Regals, General. Telefonía Fixa i internet, General. Telefonía mòbil, Impostos. Clavegueres, Impostos. Escombraries, Impostos. IBI Urbana, Maria. Estudis, Maria. Gimnàs, Maria. Metges, Mercè. Assegurança de vida, Mercè. Metges, Mixu. Veterinari, Vehicles. Opel Astra, Vehicles. Toyota Prius

Les categories es poden afegir, editar o eliminar des de la pestanya **Ajustos**.

---

## 💾 Emmagatzematge de dades

Les dades es guarden al **localStorage del Safari** de l'iPhone. Això vol dir:
- Les dades són locals al dispositiu
- No es sincronitzen automàticament entre dispositius
- La manera de fer còpia de seguretat és exportar el CSV regularment

---

## 🛠️ Actualitzar l'app

Si es publica una nova versió del fitxer `index.html` a GitHub, les dades existents es conserven ja que estan al localStorage del Safari, independent del codi de l'app.
