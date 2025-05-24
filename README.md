# 🐕 Excel Daily Tracker

Jupyter Notebook do analizy spacerów z moim psem — Excelkiem.  
Śledzenie dystansu, czasu, pogody i nastroju.

**Cele projektu:**
- obliczanie czasu trwania spacerów
- sumowanie dystansu i czasu na dzień
- w przyszłości: wykresy, interaktywne dopisywanie spacerów

**Technologie:**  
Python, Pandas, Jupyter


## 📦 Nowa funkcja: archiwizacja danych spacerów

W wersji 2.0 dodałam funkcję archiwizacji danych spacerów zapisanych w pliku `excel_walks.csv`.

### 📝 Co robi ten kod:
- Dopisuje nowe dane spaceru do istniejącego pliku `excel_walks.csv`.
- Zmienia folder roboczy za pomocą `os.chdir()`.
- Tworzy archiwum ZIP z kompresją (`compress_type=zipfile.ZIP_DEFLATED`) zawierające plik `excel_walks.csv`.

### 🔍 Przykładowe komendy:
```python
import os
import zipfile

# Zmiana folderu roboczego
os.chdir('C:/Users/User/Desktop/IT/PYTHON/Mentoring/inne ćwiczenia')

# Pakowanie pliku do ZIP
with zipfile.ZipFile('comp_excel_walks.zip', 'w') as comp_excel_walks:
    comp_excel_walks.write('excel_walks.csv', compress_type=zipfile.ZIP_DEFLATED)