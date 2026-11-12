Nouveautes de la version 2026.11.12.1 :

Connexion SQL Server : la nouvelle connexion est TESTEE avant d'etre enregistree. En cas d'echec, rien n'est enregistre et la base actuelle reste active (aucun risque de rendre l'application inutilisable).
Changement de base IMMEDIAT : la chaine de connexion n'est plus figee au demarrage. Changer de serveur ou de base dans Parametres > General bascule l'application sur la nouvelle base sans redemarrage du service (le panneau « Base SQL Server » et l'application interrogent desormais la meme base).
Parametres > General : nouveau panneau « Base SQL Server » affichant les donnees reelles de la base configuree (serveur, base, utilisateur, version et edition SQL Server, nombre de tables, volume, nombre de clients / fournisseurs / articles / documents / reglements, dernier document, derniere sauvegarde) avec un bouton « Actualiser ».
Session : la session est renouvellee apres un changement de base ; les comptes et mots de passe sont ceux de la base cible (une reconnexion peut etre necessaire).
Cache-busting : 2026.11.12.1
Nouveautes de la version 2026.11.11.3 :

Etat du systeme : le controle de NetBird ne s'applique que si le reseau est REQUIS par le poste (role Hub ou Client, avec NetBird active et une cle de jonction). Desactiver le role Hub ne declenche plus a tort l'alarme « NetBird est installe mais hors reseau » ni le badge rouge « Reseau NetBird hors ligne » : un poste autonome reste en « Systeme operationnel ».
Impayes, compteurs et alarmes : les statuts ecrits « Valide » (documents) et « Paye » (reglements) - recus par synchronisation depuis les postes clients - sont desormais reconnus comme valides. Avant, ces documents etaient ignores par « Factures a encaisser », les alarmes et le module Impayes.
Cache-busting : 2026.11.11.3
Nouveautes de la version 2026.11.11.2 :

Factures clients : le bouton « Modifier » est desormais disponible sur chaque ligne de la liste (plus besoin de selectionner la ligne puis de cliquer dans la barre d'outils). Pour une facture deja validee ou une facture d'acompte, un message clair explique pourquoi la modification est refusee (auparavant le clic etait sans effet et sans explication).
Session : la mise a jour ne deconnecte plus l'utilisateur. Seules les cles techniques obsoletees sont purgees du stockage local ; la session et les preferences d'apparence sont conservees.
BL client : avant de facturer, une fenetre impose la date d'echeance de la facture a creer (obligatoire). La date est reprise sur la facture generee, qui devient ainsi visible dans le suivi des impayes et les relances.
Impayes : nouveau module « Impayes » dans le menu Reglement (clients et fournisseurs) : reste a encaisser / a payer, echeance, retard, montant exigible, filtres par type, retard minimum et recherche, badge de menu et alarme dans la barre du haut.
Impayes : un compteur de numerotation « Impayes » (prefixe IMP) est disponible dans Parametres > Numerotation.
Impayes : mise en page du tableau corrigee (colonnes dimensionnees, montants alignes a droite, defilement horizontal).
Installation : le schema SQL embarque est desormais la version a jour (la copie figee installait un schema incomplet sur les postes locaux).
Cache-busting : 2026.11.11.2
Nouveautes de la version 2026.11.11.1 :

Ecran d'accueil : fond « vagues bleues » (meme dessin que la maquette, degrade bleu ocean et trois vagues fixes, sans animation) ; la carte KI-GEST, le slogan « La gestion maitrisee, de bout en bout » et le badge « Systeme operationnel » flottent dessus.
Espace de travail : le fond « vagues » reste visible derriere les modules ouverts (pages embarquees transparentes).
Licence : le poste ne redemande plus une activation apres chaque mise a jour (les installeurs preservent appsettings.json, la licence est relue avec tous les secrets connus, l'etat illisible est reconstruit, et la notification n'apparait que sur les postes ayant IIS ET SQL Server).
Raccourci « KI-GEST » du Bureau et du Menu Demarrer : cible http://localhost:81 et « Demarrer dans » = C:\inetpub\wwwroot\KI-GEST.
Mise a jour : les fichiers compresses (.br / .gz) sont desormais integres au delta de fichiers, et la session ouverte n'est plus fermee pendant l'installation.
Design : favicon KI dans la barre laterale (1,7 Ko au lieu de 913 Ko), contrastes AA, focus clavier visible.
Cache-busting : 2026.11.11.1
Nouveautes de la version 2026.11.13 :

Ecran d'accueil : le fond de page est l'aurore pastel de la maquette (degrade bleu, lilas, rose et cyan, grille fine, halos flous et etoiles blanches), en version fixe, sans animation. La carte KI-GEST, le slogan « La gestion maitrisee, de bout en bout » et le badge « Systeme operationnel » flottent dessus.
Raccourci « KI-GEST » du Bureau et du Menu Demarrer : la cible pointe sur le site local du poste (http://localhost:81) et « Demarrer dans » indique le dossier de l'application (C:\inetpub\wwwroot\KI-GEST).
Mise a jour : les fichiers compresses (.br / .gz) sont desormais integres au delta de fichiers ; sans cela IIS continuait de servir aux navigateurs les anciennes versions compressees du CSS et du JavaScript.
Le numero de version change : il sert de cle de cache aux fichiers CSS et JavaScript, les navigateurs reprennent donc la nouvelle maquette sans manipulation.
Cache-busting : 2026.11.13
Nouveautes de la version 2026.11.11.3 :

Etat du systeme : le controle de NetBird ne s'applique que si le reseau est REQUIS par le poste (role Hub ou Client, avec NetBird active et une cle de jonction). Desactiver le role Hub ne declenche plus a tort l'alarme « NetBird est installe mais hors reseau » ni le badge rouge « Reseau NetBird hors ligne » : un poste autonome reste en « Systeme operationnel ».
Impayes, compteurs et alarmes : les statuts ecrits « Valide » (documents) et « Paye » (reglements) - recus par synchronisation depuis les postes clients - sont desormais reconnus comme valides. Avant, ces documents etaient ignores par « Factures a encaisser », les alarmes et le module Impayes.
Cache-busting : 2026.11.11.3
Nouveautes de la version 2026.11.11.2 :

Mise a jour : les fichiers compresses (.br / .gz) sont desormais integres au delta de fichiers. Auparavant, IIS continuait de servir aux navigateurs les anciennes versions compressees du CSS et du JavaScript, meme apres une mise a jour : le nouveau design (fond de l'ecran d'accueil, favicon dans la barre laterale, contrastes, focus clavier) n'apparaitrait pas sur les postes clients.
Ecran d'accueil : le fond de page est desormais l'aurore pastel de la maquette (degrade bleu, lilas, rose et cyan, grille fine, halos flous et etoiles), en version fixe ; la carte KI-GEST, le slogan « La gestion maitrisee, de bout en bout » et le badge « Systeme operationnel » flottent dessus.
Raccourci « KI-GEST » du Bureau et du Menu Demarrer : la cible pointe desormais sur le site local du poste (http://localhost:81) et « Demarrer dans » indique le dossier de l'application (C:\inetpub\wwwroot\KI-GEST).
Cette version fait suite a la 2026.11.11 (meme contenu applicatif) : elle permet a tous les postes de recevoir le correctif et d'afficher de nouveau la notification de mise a jour.
Cache-busting : 2026.11.11.2
Nouveautes de la version 2026.11.11 :

Design : le favicon KI remplace l'ancien logo de 913 Ko dans la barre laterale de toutes les pages (nouveau fichier ki-logo.webp de 1,7 Ko ; le package gagne pres de 1 Mo).
Design : ecran d'accueil sur fond « vagues ocean » statique, identique a la page de connexion mais sans animation ; variante sombre incluse.
Design : contrastes des textes secondaires corriges (niveau AA : 6,5:1 et 5,1:1 au lieu de 4,2:1 et 2,3:1).
Design : focus clavier visible sur tous les elements (anneau bleu de 2 px), y compris dans le menu lateral sombre ; les animations sont desactivees si le systeme le demande.
Mise a jour : la notification de mise a jour (bandeau dans l'application et toast Windows) n'est plus affichee que sur les postes qui ont IIS ET SQL Server. Sur un poste de developpement ou une base SQL Server absente, aucune notification n'apparait. Echappatoire disponible : Update:AllowNotificationsWithoutIis dans appsettings.json.
Cache-busting : 2026.11.11
Nouveautes de la version 2026.11.10.15 :

Licence : le poste ne redemande plus une activation apres chaque mise a jour. Les installeurs n'ecrasent plus la configuration du poste (appsettings.json : identifiant client et secret de licence, source des mises a jour, options de securite) : elle est sauvegardee avant l'installation puis restauree juste apres.
Licence : une licence deja importee reste exploitable meme si la configuration du poste change (ajout ou retrait d'un identifiant client) : le secret de chiffrement et la signature sont verifies avec l'ensemble des secrets connus de la machine.
Licence : si le fichier d'etat de licence est illisible (copie abimee, ancien secret), il est reconstruit automatiquement a partir de la licence installee, sans changer l'identifiant d'installation du poste.
Licence : la mise a jour restaure les fichiers de licence du poste depuis le dossier persistant C:\ProgramData\KI-GEST\License s'ils ont disparu.
Licence : message explicite quand un fichier licence est present mais illisible (configuration a corriger : License:CustomerId / License:Secret dans appsettings.json) au lieu d'une simple demande d'activation.
Cache-busting : 2026.11.10.15
Nouveautes de la version 2026.11.10.14 :

Page de connexion : nouveau design « Ocean Blue Flow » (fond a vagues bleues animees, panneau de connexion et panneau d'information KI-GEST, champs avec icones, bouton d'affichage du mot de passe, indicateur de licence et version en pied de page). Le favicon KI remplace les blocs « KI » du formulaire et du panneau d'information. Toutes les fonctions restent disponibles : connexion, « se souvenir de moi », mot de passe oublie, reinitialisation et configuration de la base SQL.
Installeur « Poste local » : nouvelle page de choix du type d'installation AVANT le parametrage - « Poste autonome » (base SQL locale, aucun raccordement NetBird) ou « Poste du hub » (base SQL locale + raccordement NetBird pour que les autres postes se connectent a cette base). Les informations SQL sont demandees dans les deux cas ; les champs NetBird sont masques en mode autonome et ne sont alors pas installes.
Correction : une facture client validee, non encaissée et sans date d'échéance (paiement non différé) n'apparaissait dans aucune alerte de la cloche de la barre du haut. Elle est desormais signalée, comme le compteur « Factures à encaisser » du tableau de bord.
Correction : « Valider et facturer » (et les autres actions de toolbar confirmees) ne declenchaient plus l'action qu'une seule fois. L'action etant jouee deux fois, deux appels API partaient en meme temps et la facturation echouait sur « violation de cle unique » (erreur 500 « Operation refusee ») alors meme que la facture etait bien creee.
Correction : le serveur detecte un bon de livraison deja facture et renvoie un message clair (« Ce bon de livraison est deja facture (Facture client n° ...) ») au lieu d'une erreur 500.
Cache-busting : 2026.11.10.14
Nouveautes de la version 2026.11.10.12 :

Interface : bandeau .hero (tableau de bord) repeint en bleu (radial + linear-gradient #056ea9 / #102b43) et menu lateral en bleu nuit (#0f2e47), dans tous les themes.
Navigation : les liens du menu lateral n'ouvrent plus jamais un nouvel onglet du navigateur ; ils s'ouvrent uniquement dans la barre d'onglets interne (ki-tabbar).
Cheques et traites (traite) : les 4 groupes du RIB (code banque, code guichet, numero de compte, cle RIB) sont desormais deplacables separement, dans chacune des deux rangees de cases ; on peut ainsi ajuster chaque groupe dans sa case.
Cheques et traites (traite) : les dates ne sont plus tronquees dans les cases (echeance, date de creation, lieu) : largeur des zones et chasse ajustees.
Cache-busting : 2026.11.10.12
Nouveautes de la version 2026.11.10.11 :

Cheques et traites (traite) : le RIB est ecrit dans les cases reelles de la lettre (rangee du haut sous l'entete et rangee du bas « Code itab. / Code Agence / N° de Compte / Cle ») ; chaque groupe de chiffres est calibre pour remplir sa case et ne deborde plus.
Cheques et traites (traite) : chiffres du RIB en chasse normale (non gras), taille ajustee a chaque case.
Cache-busting : 2026.11.10.11
Nouveautes de la version 2026.11.10.10 :

Cheques et traites (traite) : nouveau fond imprime (lettre de change "Bill of echange" / "Lettre de Change"), tous les champs sont recales sur les cases de la nouvelle forme.
Cheques et traites (traite) : echeance et date d'emission en tete de lettre, lieu, signature du tire, RIB (rangee du haut et rangee du bas, 20 chiffres en 4 groupes : code banque, code guichet, numero de compte, cle), tireur, ordre de paiement, montant (x2), montant en lettres, lieu et date de creation, nom du cedant, domiciliation, nom et adresse du tire, bon pour aval, signature du tireur.
Cheques et traites (traite) : le RIB ecrit les 20 chiffres dans les cases imprimees de la lettre (Code itab. / Code Agence / N° de Compte / Cle en bas, rangee de cases en tete) ; chaque groupe est calibre pour remplir sa case.
Cheques et traites : les positions memorisees sur l'ancien fond sont ignorees (la mise en page est versionnee avec le modele imprime).
Cache-busting : 2026.11.10.10
Nouveautes de la version 2026.11.10.9 :

Cheques et traites (traite) : le RIB est ecrit dans les cases « Compte cheques » (la rangee de 3 cases situee juste sous la case « Date d'echeance »), comme sur la lettre de change de reference : code banque (2), code guichet (3), numero de compte (13, ecrit plus petit comme a la main), cle RIB (2). Les 20 chiffres restent aussi dans la grille R.I.B. du bas de la lettre.
Cache-busting : 2026.11.10.9
Nouveautes de la version 2026.11.10.8 :

Cheques et traites (traite) : toutes les zones du modele sont desormais renseignees, comme sur la lettre de change de reference - date de creation, signataire, tireur, domiciliation (agence bancaire + adresse), bon pour aval, signatures, nom du cheque ou de la banque.
Cheques et traites (traite) : la date de creation (date d'emission) est ecrite dans la case « Date de creation » et le tireur dans le champ « Tireur » ; l'exemple imprime est masque.
Cheques et traites : la saisie de demonstration remplit desormais tous les champs (numero, RIB 20 chiffres, montant, montant en lettres, dates, tireur, banque, adresse, telephone, signatures, aval), pour que l'apercu montre la mise en page complete.
Cache-busting : 2026.11.10.8
Nouveautes de la version 2026.11.10.7 :

Cheques et traites : les champs du modele se deplacent a la souris (ou au doigt) directement dans le panneau Apercu, pour regler la mise en page sans reprendre les coordonnees a la main.
Cheques et traites : la position de chaque champ est memorisee par poste et par type de document (cheque, traite) ; elle s'applique a l'apercu et a l'impression du modele.
Cheques et traites : nouveau bouton "Reposer les champs" dans le panneau Apercu pour revenir a la mise en page d'origine.
Cache-busting : 2026.11.10.7
Nouveautes de la version 2026.11.10.6 :

Cheques et traites : format reel des papiers, cheque 175 x 80 mm et traite 175 x 115 mm (apercu, impression et reglages d'impression).
Cheques et traites : le montant du cheque est desormais ecrit dans le champ B.P.D (en haut a droite du modele) ; il n'occupe plus la zone centrale.
Cheques et traites (traite) : date d'emission et lieu de creation corriges, les valeurs sont ecrites dans les cases du formulaire sous leur libelle.
Cheques et traites : suppression des aplats gris qui masquaient les zones pre-imprimees de la traite (montant, date d'emission) : les aplats reprennent desormais la teinte exacte du papier.
Cheques et traites : le montant et le RIB s'ecrivent chiffre par chiffre dans les cases pre-imprimees (cases X de la ligne I.B. du cheque, grille R.I.B. de la traite).
Cheques et traites (traite) : le RIB est ecrit dans les cases comme sur la lettre de change - code banque (2 chiffres), code guichet (3), numero de compte (13), cle RIB (2), soit 20 chiffres ; le champ RIB n'accepte que les chiffres (20 maximum).
Cheques et traites : le champ "Montant en lettres" se remplit tout seul quand on choisit un decaissement (1250.500 -> "Mille deux cent cinquante dinars").
Cheques et traites : nouveau bouton "Imprimer le modele" (impression du cheque ou de la traite sur le papier pre-imprime, aux dimensions 175 x 80 mm et 175 x 115 mm).
Cheques et traites : le texte des modeles s'adapte a la largeur du papier (a l'apercu comme a l'impression).
Cache-busting : 2026.11.10.6
Nouveautes de la version 2026.11.10.5 :

Cheques et traites : suppression du bloc de modeles papier affiche en haut de la page. Les modeles cheque et traite restent visibles dans le panneau Apercu (et a l'impression).
Nettoyage du code associe (styles .cheque-model-preview, rendu des modeles dupliques).
Cache-busting : 2026.11.10.5
Nouveautes de la version 2026.11.10.4 :

Cheques et traites : les modeles papier (cheque et lettre de change) s'affichent directement dans la page, au-dessus du formulaire de saisie et dans le panneau Apercu.
Cheques et traites : position des champs (numero, reference, montant, beneficiaire, RIB, dates, signature, aval...) alignee sur les zones pre-imprimees des deux papiers, avec masquage des valeurs d'exemple imprimees.
Correction de l'apercu des modeles qui restait invisible hors impression (largeur nulle des conteneurs).
Cache-busting : 2026.11.10.4
Nouveautes de la version 2026.11.09.1 :

Info societe sur tous les etats d'impression (facture, devis, commande, BL...) : chaque info sur sa ligne (Telephone, Email, Matricule Fiscale, RIB, Adresse), sans numerotation.
Fenetre de confirmation pour Valider / Facturer / Supprimer : question dynamique selon le type de document (ex. "Voulez-vous facturer la BL n° ... ?"), icone et bouton adaptes, support clavier (Echap/Entree). Seuls les boutons de la toolbar Valider/Supprimer concernes.
Facturer BL : detection correcte du bouton "Valider et Facturer" (data-livraison-toolbar-validate-facturer) et affichage de la question "Voulez-vous facturer la BL n° ... ?"
Suppression : question "Supprimer [type] n° ... ? Cette action est definitive."
Affichage du numero de document dans la confirmation (recherche dans ligne selectionnee .selected-row, fallback multi-patterns pour tous types de liste : BL, factures, commandes, devis, etc.)
Annulation : si l'utilisateur clique "Annuler", l'action est bien bloquee (preventDefault + stopImmediatePropagation AVANT l'attente).
Page Societe : les 5 champs cles (Telephone, Email, Matricule Fiscale, RIB, Adresse) passes en tete du formulaire, chacun sur pleine largeur.
Cache-busting : 2026.11.09.1
Nouveautes de la version 2026.11.06.2 :

TEJ : TauxTVA et MontantTVA sont desormais ecrits dans chaque operation, meme quand aucune taxe n'est due (0.00 et 0). Ces deux valeurs parfois absentes du fichier etaient refusees par la plateforme en erreur interne "Cannot read field "scale" because "val" is null".
TEJ : nouveau champ "Matricule TEJ" dans Parametres > Societe, place pres du matricule fiscal. Renseigne, il devient l'identifiant du declarant (noeud Declarant et nom du fichier de depot) ; laisse vide, l'export conserve le matricule fiscal, comme avant.
Base de donnees : la colonne Societes.MatriculeTej est ajoutee par le script idempotent update-matricule-tej.sql (installation cliente et depot SQL manuel) et par l'application au demarrage. Les bases existantes se mettent a jour sans reinstallation.
Recherche globale : reservee aux roles Superviseur et Administrateur. Le champ est masque pour les autres comptes et le serveur refuse la requete (403) avec le message "Recherche reservee aux administrateurs.".
Stock actuel : la colonne "Prix achat HT" et la statistique "Valeur stock" sont retirees de la liste ; la colonne "Valeur" reste affichee.
Validation locale (Test-TejXml.ps1) : signalement des commentaires XML, interdits par le cahier des charges et introduits quand un fichier est modifie a la main, et controle de coherence entre le TTC des operations, les totaux et le timbre fiscal.
Nouveautes de la version 2026.11.06.1 :

TEJ : le fichier de depot est nomme selon la regle officielle "MATRICULEFISCAL-EXERCICE-MOIS-CODEACTE.xml" (exemple 0001238L-2024-01-0.xml), aligne sur la periode et l'acte declares dans le contenu ; les exports modificatifs et annulatifs portent l'acte 1. Correction du refus "Le nom de fichier est invalide" sur tej.finances.gov.tn.
TEJ : les libelles du beneficiaire (raison sociale, adresse, activite) sont nettoies des caracteres interdits par le cahier des charges - accents translitteres, esperluette remplacee par "et", signes < > ; * " et doubles tirets retires ; les textes en arabe sont conserves tels quels.
TEJ : fichier telecharge en UTF-8 sans signature BOM, conforme a l'attendu de la plateforme.
TEJ : le nom affiche au telechargement reprend celui calcule par le serveur (export unitaire, export en lot et declaration groupee).
TEJ : matricule fiscal de la societe invalide (7 chiffres + lettre attendus) = message d'erreur explicite au lieu d'un fichier refuse.
Validation locale (Test-TejXml.ps1) : controle du nom du fichier, coherence nom/contenu (declarant, periode, acte), signalement des caracteres speciaux et des sequences "OR/AND" avant depot.
Nouveautes de la version 2026.11.06 :

Devis et commandes, client comme fournisseur : le bouton "Supprimer" devient "Annuler". Le document reste au repertoire avec le statut Annulee (tracabilite) au lieu d'etre efface ; l'annulation est refusee sur un document deja valide ou deja annule.
Liste articles : un bouton "Colonnes" place dans l'en-tete, a cote du titre, ouvre le selecteur de colonnes. Chacun choisit les colonnes affichees (famille, categorie, unites, conversions, TVA, prix achat, stock min/max, gestion par lot...), Code et Designation restant toujours visibles. "Tout afficher" reactive toutes les colonnes, la croix ou la touche Echap referment le panneau, et le choix est memorise sur le poste.
Recherche globale : les articles trouves s'affichent en tableau (code, designation, stock disponible, prix vente HT, statut) directement dans le combobox, sans deplacer la fenetre vers la liste.
Recherche globale : un clic sur un article ouvre une fenetre flottante avec sa fiche complete - donnees (code a barres, QR, famille, categorie, unites, TVA, statut), prix (achat et vente, HT et TTC, marge) et stock (total, valeur, cout moyen pondere, detail par depot avec lots et peremptions) - et un bouton "Modifier dans Liste articles".
Recherche globale : un clic sur un document, un client ou un fournisseur ouvre desormais la page concernee dans un onglet de l'espace de travail, comme le fait le menu lateral, au lieu de recharger toute la fenetre et de fermer les onglets ouverts.
Stock actuel : la colonne "Cout moyen" est remplacee par "Prix vente HT" et une colonne "Prix achat HT" est ajoutee ; la statistique "Valeur stock" se calcule sur le prix achat HT ; la devise n'est plus repetee dans chaque colonne de prix.
Nouveautes de la version 2026.11.05.3 :

Commande client : echeancier d'acomptes facultatif (jusqu'a 12 echeances en pourcentage ou en montant, avec date d'effet). Chaque echeance due genere une facture d'acompte (numerotation AC) en Non Valider a la validation de la commande ; les echeances qui echent plus tard se generent depuis la consultation de la commande.
Facture de solde : les acomptes valides sont detraques du net a payer, automatiquement au "Valider et Facturer" du bon de livraison et via le bouton "Deduire les acomptes" du formulaire facture.
Liste des factures clients : les factures d'acompte apparaissent avec le badge "Acompte", restent en consultation seule et consomment le plafond credit du client.
Encaissements : les factures d'acompte validees se regler comme les factures client ; elles apparaissent dans la liste "Importer documents client" apres selection du client.
Blocage plafond credit : un superviseur (compte a role eleve) peut lever le blocage a la validation d'une commande, d'une facture ou d'un bon de livraison avec son email, son mot de passe et un motif obligatoire ; chaque levee est tracee dans le journal d'audit et un delai anti-force-brute s'applique apres des tentatives echouees.
Parametres > General > Autre : interrupteur "Plafond credit : autoriser la derogation superviseur" pour desactiver la levee par code superviseur.
Nouveautes de la version 2026.11.05.1 (version finale) :

Mise a jour par fichier (delta) : le poste ne telecharge plus le package complet, seulement les fichiers recents (quelques Mo au lieu de ~90 Mo). Desormais, chaque nouvelle publication ne transfere que les fichiers modifies ou supprimes.
Fenetre flottante de progression : apres le clic "Mettre a jour", la page de connexion affiche au centre de l'ecran le pourcentage de telechargement et d'installation, fichier par fichier.
Installation a 100 % : en fin de telechargement, le serveur IIS redemarre automatiquement et le cache du navigateur est purge ; a la reconnexion, le poste affiche immediatement la nouvelle version.
Notification de mise a jour : "Plus tard" n'est plus un refus definitif ; le bandeau se represente de lui-meme au bout de 5 minutes et pour chaque nouvelle version publiee.
Reparation : erreur "Aucune source de mise a jour valide" quand une release GitHub avait ete regeneree sans changer de numero ; le manifest est desormais re-sonde en frais avant chaque installation.
Nouveau module Cout de Revient : charges accessoires validees et reparties sur les articles, consultation du cout par article/depot avec historique des variations, ajustement manuel motive et reinitialisation, simulateur full costing, analyse des marges, valorisation du stock au cout de revient.
Manuel client PDF du module Cout de Revient integre a l'application (bouton "Manuel PDF" dans le Simulateur).
Nouveautes de la version 2026.11.03 :

Mise a jour obligatoire : cette version doit etre installee immediatement (banniere rouge, pas d'option "Plus tard").
Encaissements et Decaissements : les factures / BL a regler se choisissent desormais via une liste a cases a cocher ; on peut importer plusieurs documents d'un coup en un seul enregistrement.
Encaissements et Decaissements : le champ "Montant encaisse" / "Montant regle" affiche la somme de tous les documents importes (total calcule, lecture seule).
Fiche fournisseur : solde initial active par defaut ; controle du plafond de credit bloque la facturation et la commande quand le seuil est depasse.
Import BL : le timbre fiscal est conserve lors de la generation de la facture depuis un bon de livraison.
Page A propos : logo Android affiche pres du QR code de l'application mobile.
Nouveautes de la version 2026.11.02.3 :

Notification de mise a jour sur le bureau Windows : des qu'une version plus recente est publiee, une notification s'affiche sur le poste, eveillee a l'ouverture de session puis toutes les 30 minutes. Elle reprend le meme diagnostic que la banniere interne (comparaison de la version du hub a celle installee) et n'alerte qu'une seule fois par version.
La notification ne telecharge ni n'installe rien : le service "KI-GEST Update" continue d'appliquer la mise a jour en arriere-plan ; le toast avertit seulement.
Reparage : l'installeur et le point d'entree Install-UpdateTask replacent desormais la tache de notification KI-GEST-CheckUpdate, y compris apres un deploiement qui vide le site.
Nouveautes de la version 2026.11.01.2 :

Application mobile : licence des l'ouverture. Le numero de serie est remis par le revendeur (ki-commercial@outlook.com) et recopie sur le telephone. Une activation reussie affiche la duree accordee, par exemple "Licence activee : 365 jour(s) restant(s) (expire le 01/11/2027)" ; un numero refuse affiche "Licence incorrecte" avec le nombre de tentatives qui restent
Application mobile : trois tentatives par appareil, puis blocage de 15 minutes. Le compte a rebours s'affiche sur le telephone, le hub refuse tout numero pendant la fermeture (meme un numero valide), et une activation reussie remet le compteur a trois
Application mobile : plus de demonstration de 30 jours. Toute installation neuve de l'APK reclame une licence. Une licence activee ne se reactive pas sur le meme appareil, et "Effacer" ne peut plus rouvrir la saisie d'un numero encore dans sa duree ; en revanche un numero expire se remplace
Application mobile : l'exemption Superviseur / Administrateur est un droit de session, pas un droit d'appareil. Elle ne s'ecrit dans aucune memoire et se retire des la deconnexion
Licence mobile : les numeros se generent et se controlent depuis le dossier tools (KiGestLicense.exe -Mobile / New-KiGestMobileLicense.ps1). Le numero est signe pour l'identifiant de l'appareil : recopie sur un autre telephone, il sera refuse. La page Licence du poste n'affiche plus que cet identifiant a dicter
Poste web : la demonstration de 30 jours reste en place, seule l'application mobile la perd
Nouveautes de la version 2026.10.30.4 :

Notification de mise a jour : une reponse "deja a jour" n'est plus figee pour 6 heures. Elle expire au bout de 60 secondes et la sonde GitHub revient toutes les 10 minutes ; l'onglet Mise a jour force toujours la sonde et l'application reinterroge le hub des qu'un onglet revient au premier plan. Une release publiee quelques minutes apres une sonde est donc annoncee sans redemarrage
Page Stock : les quantites s'affichent telles qu'elles sont saisies (7 reste 7, 7,5 reste 7,5) au lieu d'etre forcees a trois decimales, et une colonne Unites affiche l'unite de stock definie sur la fiche article
Application mobile : la confirmation de validation d'un document remplace la fenetre systeme Android par une boite dialogue au theme KI-GEST (icone, numero du document, boutons Annuler / Valider)
Nouveautes de la version 2026.10.29 :

Impression des documents sur les postes a distance (connexion via NetBird) : le logo de la societe ne s'imprime plus en cadre vide. L'impression attend que le logo soit reellement charge et decode et, en secours, le recupere directement en base64 avant d'imprimer
Nouveautes de la version 2026.10.28.2 :

Ecran d'accueil : badge d'etat en temps reel (vert = operationnel ; rouge + notification si SQL Server injoignable ou si NetBird installe mais hors reseau ; NetBird ignore quand il n'est pas installe) et logo KI-GEST avec tiret
Connexion : salutation selon l'heure (Bonjour le matin, Bon appetit l'apres-midi, Bonsoir le soir)
Mise a jour : nouvel onglet "Nouveautes" affichant le descriptif de la derniere version depuis GitHub
Liste clients et Liste fournisseurs : "Annuler" apres "Modifier" revient a la liste actualisee au lieu de rester bloque en modification
Caisse / fin de journee : la notification "Caisse a cloturer" se declenche des qu'il existe des encaissements especes valides du jour a l'heure reglee
Nouveautes de la version 2026.10.26.29 :

Mise a jour : installeurs publies via MediaFire avec les liens de partage embarques dans la configuration (Update:Provider=MediaFire) ; un poste installe est desormais notifie puis telecharge sa mise a jour depuis MediaFire
Matricule fiscal (client, fournisseur, societe) : validation du format (7 chiffres + cle, ou complet 7 chiffres / cle / TVA / categorie / 3 chiffres) avec auto-format et blocage de l'enregistrement si le format est invalide
Retenue a la source : etat "Valide" corrige (VALIDE et non VALIDEE) et calcul aligne sur le calculateur officiel (base hors timbre, retenue arrondie a 3 decimales, net = TTC - retenue)
Nouveautes de la version 2026.10.26.28 :

Mise a jour : publication via MediaFire (outil d'upload Deploy/MediaFire + liens de partage par fichier dans Update:MediaFire:*) ; la notification compare la version du dossier MediaFire a celle installee sur le poste
Nouveautes de la version 2026.10.26.27 :

Mise a jour : la source de mise a jour peut desormais etre un dossier MediaFire (Update:Provider=MediaFire + Update:HubUrl = URL du dossier) ; l'application y lit version.txt, affiche les nouveautes, puis telecharge l'installeur (KI-GEST-Install-PosteLocal.exe / PosteExterieur) via le lien de partage resolu a la volee ; le hub classique reste disponible en repassant Update:Provider=Hub
Nouveautes de la version 2026.10.26.26 :

Liste clients : apres modification + enregistrement d'un client depuis la liste, retour automatique au tableau des clients avec donnees actualisees (au lieu de rester bloque sur la fiche)
Liste fournisseurs : idem, retour automatique au tableau actualise apres enregistrement d'un fournisseur modifie
Nouveautes de la version 2026.10.26.25 :

Installation PosteLocal : le programme d'installation met desormais a jour une base KI-GEST deja existante (re-application non destructive des donnees de reference) au lieu de l'ignorer ; sur une base neuve il installe la base complete (schema + donnees)
Installation : les donnees de reference (types de retenue TypeRetenue, dictionnaire des codes TEJ, mapping TypeRetenue -> code d'operation) sont appliquees directement par l'installeur
Nouveautes de la version 2026.10.26.24 :

TEJ : le code d'operation de chaque type de retenue est pilote depuis la base (nouvelle table TypeRetenue_TEJ_Mapping, alignee sur le XSD officiel) au lieu d'une liste figee dans le code
TEJ : types auparavant en erreur "Type de retenue TEJ introuvable" (ex. Salaries etrangers non-residents) desormais declarables avec leur code d'operation ; message clair et aucun XML pour les types non declarables (TVA, avances, exoneres)
TEJ : correction de conformite au schema officiel du XML genere (beneficiaire non-resident = Resident 0 ; ActeDepot = rectificatif pour les exports modificatif/annulatif)
Installation : les tables de reference TEJ (dictionnaire des codes + mapping) sont creees et peuplees automatiquement au demarrage, sur le hub comme sur chaque poste client
Nouveautes de la version 2026.10.26.23 :

Securite : les droits par page/action sont desormais appliques cote serveur (un compte ne peut plus modifier un module qui ne lui est pas autorise, meme en appellant l'API directement ; desactivable via Security:EnforcePageAccess)
Retenue a la source : statut TEJ par defaut A_DECLARER (au lieu de NON_APPLICABLE)
Nouveautes de la version 2026.10.26.22 :

Bon d'echange : le stock disponible diminue reellement de la quantite echangee (l'article rendu n'est plus reintegre deux fois ; il reste en Quarantaine depuis le bon de retour)
Nouveautes de la version 2026.10.26.21 :

Fiche client et fiche fournisseur : champ Nom mis automatiquement en majuscules
Fiche fournisseur : solde initial desactive par defaut (= 0)
Fiche client : timbre fiscal saisi sans decimale
Bon de reception achat : combo Statut affiche en orange quand la valeur est Quarantaine
Prix d'achat : mise a jour proposee depuis la reception, la commande et la facture fournisseur
Facture client : timbre fiscal charge automatiquement depuis la fiche client
Reglement client : montant restant affiche en bas du document
Nouveautes de la version 2026.10.26.20 :

Demande de fonds : impression en fiche A4 signable (signature employe + signature responsable)
Demande de fonds : suppression avec bouton dedie (compteur de numero revalue)
Numerotation : le compteur est diminue de 1 quand le dernier document est supprime (tous les documents : ventes, achats, retenues, transferts, alimentations, demandes de fonds)
Nouveautes de la version 2026.10.25.19 :

Reglement : nouveau menu "Demande de fonds" (l'employe soumet et suit ses demandes ; les roles sureleves approuvent ou refusent)
Demande de fonds : table SQL dediee, API server-side et page avec impression A4
Nouveautes de la version 2026.10.25.18 :

TEJ : exports XML Annulatif et Modificatif (arrete du 10/05/2024) avec bouton Marquer declaree
TEJ : fichier XML avec en-tete UTF-8 corrigee et timbre fiscal place selon le schema officiel (plus de refus plateforme)
TEJ : type "Acquisition fonds de commerce" declarable (code RS6_000001)
Fournisseur : categorie personne physique (PP) detectee automatiquement via la CIN
