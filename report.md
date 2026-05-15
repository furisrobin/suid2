V této úloze byla využita zranitelnost v tom, že skript init.sh používá uživatelskou proměnnou STUDENT_NAME při generování flagu.

Útočník může tuto hodnotu ovlivnit a tím si předem spočítat výsledný flag bez nutnosti získání root práv.

UID je skutečné ID uživatele, který proces spustil, zatímco EUID je efektivní ID používané během běhu programu pro oprávnění.

Jako administrátor by bylo vhodné nepoužívat uživatelské vstupy v privilegovaných skriptech a oddělit generování citlivých dat od environment proměnných.

Další ochrana by byla odstranění SUID bitu u nepotřebných binárek a minimalizace privilegovaných operací.
