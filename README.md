### Projekt-programowanie2
Celem jest klasyfikacja binarna studentów pod kątem szans na uzyskanie stażu na podstawie ich profilu akademickiego i technicznego.
 * **Cel:** Zbudowanie modelu przewidującego zmienną binarną (otrzyma staż / nie otrzyma stażu). Główny problem: optymalizacja modelu pod kątem niesymetrycznych klas.
 * **Dane:** Zbiór liczy 10 000 wierszy i 21 kolumn (podział 80% trening, 20% test). Dane są syntetyczne.
 * **Cechy:** Większość danych jest numeryczna (wyniki testów, CGPA, ocena CV itp.), uzupełnione o 3 dodatkowe cechy stworzone pod ten projekt (total_performance_score, practical_experience_score, education_score).
   
### Ostateczne wyniki na zbiorze testowym
Użyto trzech modeli: Logistic Regression, Decision Tree i Random Forest.
Najlepszy,wybrany przez Grid Search został sprawdzony na odizolowanej próbie testowej.
```text
              precision    recall  f1-score   support
           0       0.32      0.53      0.40       525
           1       0.78      0.60      0.68      1475

    accuracy                           0.58      2000

```
 * Model poprawnie identyfikuje **53%** studentów, którzy faktycznie nie uzyskają stażu.
 * Wskaźnik F1-score dla problematycznej klasy ⁠0⁠ wzrósł z 0.01 do 0.40. Model zyskał realną zdolność predykcyjną dla obu klas.
 * Wyniki na zbiorze testowym są spójne z wynikami z walidacji krzyżowej, co potwierdza brak przeuczenia i prawidłową generalizację modelu.
