# DATE-
date for java
public class DateHeure {
    private int jour;
    private int mois;
    private int annee;
    private int heure;
    private int minute;

    // Constructeur avec vérification
    public DateHeure(int jour, int mois, int annee, int heure, int minute) {
        if (jour >= 1 && jour <= 31) {
            this.jour = jour;
        } else {
            System.out.println("Jour invalide !");
        }

        if (mois >= 1 && mois <= 12) {
            this.mois = mois;
        } else {
            System.out.println("Mois invalide !");
        }

        this.annee = annee; // Pas de restriction ici

        if (heure >= 0 && heure < 24) {
            this.heure = heure;
        } else {
            System.out.println("Heure invalide !");
        }

        if (minute >= 0 && minute < 60) {
            this.minute = minute;
        } else {
            System.out.println("Minute invalide !");
        }
    }

    public void afficher() {
        System.out.printf("Date et heure saisies : %02d/%02d/%d %02d:%02d\n",
                this.jour, this.mois, this.annee, this.heure, this.minute);
    }
}
