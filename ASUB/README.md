# Detekcija intracerebralnog krvarenja na CT slikama mozga

Timski projekt s FER-a usmjeren na razvoj sustava za automatsku detekciju intracerebralnog krvarenja na CT slikama mozga primjenom digitalne obrade slike i klasičnih metoda strojnog učenja.

## Opis projekta

Cilj projekta bio je klasificirati CT slike mozga u dvije kategorije: **krvarenje** i **bez krvarenja**. Razvijen je postupak koji obuhvaća predobradu slika, izdvajanje regije interesa (ROI), ekstrakciju vizualnih značajki i usporedbu modela.

## Korištene tehnologije

- **Python**
- **OpenCV** – obrada i segmentacija slika
- **NumPy i Pandas** – numerička obrada i manipulacija podacima
- **Scikit-learn** – implementacija i evaluacija modela strojnog učenja
- **XGBoost** – klasifikacija
- **Matplotlib i Seaborn** – vizualizacija rezultata

## Metodologija

1. **Predobrada slika** – promjena rezolucije na 224 × 224 piksela, uklanjanje šuma Gaussovim filtrom i poboljšanje kontrasta metodom CLAHE.
2. **Segmentacija regije interesa (ROI)** – izdvajanje intrakranijalne regije primjenom Otsuova pragiranja, morfoloških operacija i najveće povezane komponente.
3. **Ekstrakcija značajki** – izračun intenzitetskih, rubnih i teksturalnih značajki pomoću statističkih mjera, Sobelova gradijenta, Cannyjeve detekcije rubova, GLCM-a i LBP-a.
4. **Klasifikacija** – implementacija i usporedba pet modela: logističke regresije, SVM-a, Random Foresta, XGBoosta i višeslojnog perceptrona (MLP).
5. **Evaluacija** – usporedba točnosti i odziva (recall), analiza matrice zabune i procjena važnosti značajki.

## Rezultati

Najbolje rezultate na testnom skupu ostvario je model **višeslojnog perceptrona (MLP)**, s točnošću od **80 %** i odzivom od **0,85**. Dodatna analiza važnosti značajki pokazala je značajnu ulogu udjela svijetlih piksela, gustoće rubova i teksturalnih značajki.

## Autori

Karla Budimir, Anja Obuljen, Marko Sršić i Nela Štubelj

*Napomena: Projekt je izrađen u akademske svrhe i nije namijenjen samostalnom postavljanju medicinskih dijagnoza.*
