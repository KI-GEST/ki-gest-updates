Bientot : version 2026.11.04 (en preparation) :
- Nouveau module Cout de Revient : charges accessoires validees et reparties sur les articles, consultation du cout par article/depot avec historique des variations, ajustement manuel motive et reinitialisation, simulateur full costing, analyse des marges, valorisation du stock au cout de revient.
- Manuel client PDF du module Cout de Revient integre a l'application (bouton « Manuel PDF » dans le Simulateur).
Nouveautes de la version 2026.11.03 :
- Mise a jour obligatoire : cette version doit etre installee immediatement (banniere rouge, pas d'option « Plus tard »).
- Encaissements et Decaissements : les factures / BL a regler se choisissent desormais via une liste a cases a cocher ; on peut importer plusieurs documents d'un coup en un seul enregistrement.
- Encaissements et Decaissements : le champ « Montant encaisse » / « Montant regle » affiche la somme de tous les documents importes (total calcule, lecture seule).
- Fiche fournisseur : solde initial active par defaut ; controle du plafond de credit bloque la facturation et la commande quand le seuil est depasse.
- Import BL : le timbre fiscal est conserve lors de la generation de la facture depuis un bon de livraison.
- Page A propos : logo Android affiche pres du QR code de l'application mobile.

Nouveautes de la version 2026.11.02.3 :
- Notification de mise a jour sur le bureau Windows : des qu'une version plus recente est publiee, une notification s'affiche sur le poste, eveillee a l'ouverture de session puis toutes les 30 minutes. Elle reprend le meme diagnostic que la banniere interne (comparaison de la version du hub a celle installee) et n'alerte qu'une seule fois par version.
- La notification ne telecharge ni n'installe rien : le service « KI-GEST Update » continue d'appliquer la mise a jour en arriere-plan ; le toast avertit seulement.
- Reparage : l'installeur et le point d'entree Install-UpdateTask replacent desormais la tache de notification KI-GEST-CheckUpdate, y compris apres un deploiement qui vide le site.

Nouveautes de la version 2026.11.01.2 :
- Application mobile : licence des l'ouverture. Le numero de serie est remis par le revendeur (ki-commercial@outlook.com) et recopie sur le telephone. Une activation reussie affiche la duree accordee, par exemple « Licence activee : 365 jour(s) restant(s) (expire le 01/11/2027) » ; un numero refuse affiche « Licence incorrecte » avec le nombre de tentatives qui restent
- Application mobile : trois tentatives par appareil, puis blocage de 15 minutes. Le compte a rebours s'affiche sur le telephone, le hub refuse tout numero pendant la fermeture (meme un numero valide), et une activation reussie remet le compteur a trois
- Application mobile : plus de demonstration de 30 jours. Toute installation neuve de l'APK reclame une licence. Une licence activee ne se reactive pas sur le meme appareil, et « Effacer » ne peut plus rouvrir la saisie d'un numero encore dans sa duree ; en revanche un numero expire se remplace
- Application mobile : l'exemption Superviseur / Administrateur est un droit de session, pas un droit d'appareil. Elle ne s'ecrit dans aucune memoire et se retire des la deconnexion
- Licence mobile : les numeros se generent et se controlent depuis le dossier tools (KiGestLicense.exe -Mobile / New-KiGestMobileLicense.ps1). Le numero est signe pour l'identifiant de l'appareil : recopie sur un autre telephone, il sera refuse. La page Licence du poste n'affiche plus que cet identifiant a dicter
- Poste web : la demonstration de 30 jours reste en place, seule l'application mobile la perd

Nouveautes de la version 2026.10.30.4 :
- Notification de mise a jour : une reponse « deja a jour » n'est plus figee pour 6 heures. Elle expire au bout de 60 secondes et la sonde GitHub revient toutes les 10 minutes ; l'onglet Mise a jour force toujours la sonde et l'application reinterroge le hub des qu'un onglet revient au premier plan. Une release publiee quelques minutes apres une sonde est donc annoncee sans redemarrage
- Page Stock : les quantites s'affichent telles qu'elles sont saisies (7 reste 7, 7,5 reste 7,5) au lieu d'etre forcees a trois decimales, et une colonne Unites affiche l'unite de stock definie sur la fiche article
- Application mobile : la confirmation de validation d'un document remplace la fenetre systeme Android par une boite dialogue au theme KI-GEST (icone, numero du document, boutons Annuler / Valider)

Nouveautes de la version 2026.10.29 :
- Impression des documents sur les postes a distance (connexion via NetBird) : le logo de la societe ne s'imprime plus en cadre vide. L'impression attend que le logo soit reellement charge et decode et, en secours, le recupere directement en base64 avant d'imprimer

Nouveautes de la version 2026.10.28.2 :
- Ecran d'accueil : badge d'etat en temps reel (vert = operationnel ; rouge + notification si SQL Server injoignable ou si NetBird installe mais hors reseau ; NetBird ignore quand il n'est pas installe) et logo KI-GEST avec tiret
- Connexion : salutation selon l'heure (Bonjour le matin, Bon appetit l'apres-midi, Bonsoir le soir)
- Mise a jour : nouvel onglet « Nouveautes » affichant le descriptif de la derniere version depuis GitHub
- Liste clients et Liste fournisseurs : « Annuler » apres « Modifier » revient a la liste actualisee au lieu de rester bloque en modification
- Caisse / fin de journee : la notification « Caisse a cloturer » se declenche des qu'il existe des encaissements especes valides du jour a l'heure reglee

Nouveautes de la version 2026.10.26.29 :
- Mise a jour : installeurs publies via MediaFire avec les liens de partage embarques dans la configuration (Update:Provider=MediaFire) ; un poste installe est desormais notifie puis telecharge sa mise a jour depuis MediaFire
- Matricule fiscal (client, fournisseur, societe) : validation du format (7 chiffres + cle, ou complet 7 chiffres / cle / TVA / categorie / 3 chiffres) avec auto-format et blocage de l'enregistrement si le format est invalide
- Retenue a la source : etat « Valide » corrige (VALIDE et non VALIDEE) et calcul aligne sur le calculateur officiel (base hors timbre, retenue arrondie a 3 decimales, net = TTC - retenue)

Nouveautes de la version 2026.10.26.28 :
- Mise a jour : publication via MediaFire (outil d'upload Deploy/MediaFire + liens de partage par fichier dans Update:MediaFire:*) ; la notification compare la version du dossier MediaFire a celle installee sur le poste

Nouveautes de la version 2026.10.26.27 :
- Mise a jour : la source de mise a jour peut desormais etre un dossier MediaFire (Update:Provider=MediaFire + Update:HubUrl = URL du dossier) ; l'application y lit version.txt, affiche les nouveautes, puis telecharge l'installeur (KI-GEST-Install-PosteLocal.exe / PosteExterieur) via le lien de partage resolu a la volee ; le hub classique reste disponible en repassant Update:Provider=Hub

Nouveautes de la version 2026.10.26.26 :
- Liste clients : apres modification + enregistrement d'un client depuis la liste, retour automatique au tableau des clients avec donnees actualisees (au lieu de rester bloque sur la fiche)
- Liste fournisseurs : idem, retour automatique au tableau actualise apres enregistrement d'un fournisseur modifie

Nouveautes de la version 2026.10.26.25 :
- Installation PosteLocal : le programme d'installation met desormais a jour une base KI-GEST deja existante (re-application non destructive des donnees de reference) au lieu de l'ignorer ; sur une base neuve il installe la base complete (schema + donnees)
- Installation : les donnees de reference (types de retenue TypeRetenue, dictionnaire des codes TEJ, mapping TypeRetenue -> code d'operation) sont appliquees directement par l'installeur

Nouveautes de la version 2026.10.26.24 :
- TEJ : le code d'operation de chaque type de retenue est pilote depuis la base (nouvelle table TypeRetenue_TEJ_Mapping, alignee sur le XSD officiel) au lieu d'une liste figee dans le code
- TEJ : types auparavant en erreur « Type de retenue TEJ introuvable » (ex. Salaries etrangers non-residents) desormais declarables avec leur code d'operation ; message clair et aucun XML pour les types non declarables (TVA, avances, exoneres)
- TEJ : correction de conformite au schema officiel du XML genere (beneficiaire non-resident = Resident 0 ; ActeDepot = rectificatif pour les exports modificatif/annulatif)
- Installation : les tables de reference TEJ (dictionnaire des codes + mapping) sont creees et peuplees automatiquement au demarrage, sur le hub comme sur chaque poste client

Nouveautes de la version 2026.10.26.23 :
- Securite : les droits par page/action sont desormais appliques cote serveur (un compte ne peut plus modifier un module qui ne lui est pas autorise, meme en appellant l'API directement ; desactivable via Security:EnforcePageAccess)
- Retenue a la source : statut TEJ par defaut A_DECLARER (au lieu de NON_APPLICABLE)

Nouveautes de la version 2026.10.26.22 :
- Bon d'echange : le stock disponible diminue reellement de la quantite echangee (l'article rendu n'est plus reintegre deux fois ; il reste en Quarantaine depuis le bon de retour)

Nouveautes de la version 2026.10.26.21 :
- Fiche client et fiche fournisseur : champ Nom mis automatiquement en majuscules
- Fiche fournisseur : solde initial desactive par defaut (= 0)
- Fiche client : timbre fiscal saisi sans decimale
- Bon de reception achat : combo Statut affiche en orange quand la valeur est Quarantaine
- Prix d'achat : mise a jour proposee depuis la reception, la commande et la facture fournisseur
- Facture client : timbre fiscal charge automatiquement depuis la fiche client
- Reglement client : montant restant affiche en bas du document

Nouveautes de la version 2026.10.26.20 :
- Demande de fonds : impression en fiche A4 signable (signature employe + signature responsable)
- Demande de fonds : suppression avec bouton dedie (compteur de numero revalue)
- Numerotation : le compteur est diminue de 1 quand le dernier document est supprime (tous les documents : ventes, achats, retenues, transferts, alimentations, demandes de fonds)

Nouveautes de la version 2026.10.25.19 :
- Reglement : nouveau menu "Demande de fonds" (l'employe soumet et suit ses demandes ; les roles sureleves approuvent ou refusent)
- Demande de fonds : table SQL dediee, API server-side et page avec impression A4

Nouveautes de la version 2026.10.25.18 :
- TEJ : exports XML Annulatif et Modificatif (arrete du 10/05/2024) avec bouton Marquer declaree
- TEJ : fichier XML avec en-tete UTF-8 corrigee et timbre fiscal place selon le schema officiel (plus de refus plateforme)
- TEJ : type « Acquisition fonds de commerce » declarable (code RS6_000001)
- Fournisseur : categorie personne physique (PP) detectee automatiquement via la CIN
