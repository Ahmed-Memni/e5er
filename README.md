# e5er ProjetPSR/
├── src/ ← tous les fichiers sources et en-tête en
C
│ ├── vol.h – modèle de données des vols
│ ├── file_io.c – chargement/enregistrement de
data/vols.txt
│ ├── test_chargement.c – test autonome du chargeur de vols
│ ├── histo.h – modèle de données de l’historique
│ ├── histo_io.c – chargement/enregistrement de
data/histo.txt
│ ├── facture.h – modèle de données des factures
│ ├── facture_io.c – chargement/enregistrement de
data/facture.txt
│ ├── server.c – serveur TCP **multi-thread**
│ │ (AFF_VOL, TRANSACTION, AFF_HISTO,
AFF_FACTURE + pénalité 10 %)
│ └── client.c – client TCP flexible (toute commande)
│
├── data/ ← fichiers de stockage persistants
│ ├── vols.txt – liste initiale des vols
│ ├── histo.txt – historique des transactions
│ │ (vide au démarrage, avec en-tête)
│ └── facture.txt – factures des agences
│ (vide au démarrage, avec en-tête)
│
├── Makefile ← règles de compilation pour :
│ • test_chargement
│ • server
│ • client
│
└── bin/ ← exécutables générés
├── test_chargement
├── server
└── client
