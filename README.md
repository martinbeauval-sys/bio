# Page lien en bio Instagram — Martin Beauval

Page mobile unique, sans dépendance, hébergée sur GitHub Pages : https://martinbeauval-sys.github.io/bio/
Dépôt : martinbeauval-sys/bio (branche main, racine). Mise à jour = modifier `index.html`, `git push`, en ligne en une minute.

## Contenu (v2 du 22/09/2026, d'après la page Notion « Tasks remise en forme IG », 3b9d669b2f38809da777c7632ce62250)
Objectifs du brief : (1) rediriger un lead au bon endroit, (2) montrer que Martin n'est pas un formateur. D'où le pitch « Opérateur, pas formateur » et six boutons d'intention « Je veux… », dans l'ordre du brief, groupés France / Maroc :
1. Tout comprendre sur la conciergerie Airbnb → vidéo « Formation Gratuite Conciergerie : se lancer en partant de zéro » (ZiOWY0g6M4k), bouton principal jaune.
2. Automatiser ma conciergerie → vidéo « Quel logiciel pour ton Airbnb en 2026 » (LrCqVi3I-NE).
3. Ouvrir ma structure de gestion locative au Maroc → lereseau-ma.com/rejoindre/doc (UTM passés de youtube à instagram/bio).
4. Devenir conseiller immobilier au Maroc → join.saafka.com.
5. Investir au Maroc → saafka.com/acheter.
6. Vendre mon logement au Maroc → saafka.com/vendre.
Les six cibles répondaient 200 le 22/09 à 23h50. Contact : contact@mbgroup.com comme demandé (voir « En attente »).

## Contenu v1 (remplacé)
- En-tête : portrait (`assets/martin.jpg`, source Node/Ressources Node/Founder/PDP.png), nom, « 26 ans · entrepreneur et investisseur immobilier », pastille France & Maroc, phrase de positionnement (celle du fichier INSTAGRAM.md : « je construis les entreprises qui font tourner l'immobilier »).
- Commencer ici : masterclass gratuite ménage (funnel GitHub Pages).
- Mes entreprises : ConciergElite (conciergelite.fr), Saafka (saafka.com), Node (agencenode.com).
- Me suivre : YouTube @martinbeauval.conciergelite.
- Preuves : +600 conciergeries, 2 pays, 4 entreprises.
- Pied : Instagram, YouTube, email. L'adresse est une variable en bas du HTML (`CONTACT_EMAIL`).

## En attente de Martin
1. Page Notion reçue le 22/09 à 23h40, intégrée en v2.
2. L'adresse email : `mbgroup.com` appartient à un tiers depuis 1997 (GoDaddy), `contact@mbgroup.com` ne peut pas exister pour Martin. `martinbeauval.com` et `martinbeauval.fr` sont libres au 22/09/2026. Claude ne crée ni domaine ni boîte mail (paiement et identifiants).
3. Le lien court : un domaine à Martin (ex. martinbeauval.com) pointé sur ce dépôt (CNAME) donnerait `martinbeauval.com` en bio. Sans domaine, l'adresse GitHub reste la seule.

## DA
Même famille que les stories Média / Rencontres : fond #0f1216, halo doré, Poppins ExtraBold, jaune ConciergElite #f8d74f pour l'action principale. Zone max 480 px, une colonne, cartes tactiles de 84 px de haut.

- Vérification 22/09 23h55 : rendu pleine hauteur validé sur 375 px (six cartes, pied, aucun débordement). Piège outil : la capture du navigateur intégré est noire après un défilement en émulation mobile ; prendre une capture en viewport 375x1560 à la place.

## v3 (23/09/2026, 00h15) — retours de Martin
- « Ne pas ressembler à un site généré par l'IA » : plus de fond sombre, de cartes, de dégradés ni de halo. Papier clair #f3efe6, encre noire, nom en Instrument Serif, liens en Inter, liste numérotée à filets fins, un seul accent jaune (surlignage de « tout comprendre »).
- Tout visible sans défiler sur 375x812 (hauteur du document = hauteur de l'écran, pied à 798 px). Une règle `max-height:700px` resserre encore sur les petits écrans.
- Supprimés : pitch « Opérateur, pas formateur », les trois chiffres, l'icône @, la ligne « © 2026 ». Gardés : Instagram et YouTube avec leurs vrais pictogrammes (SVG inline), la ligne contact.
- Six liens dans l'ordre exact de la page Notion, libellés repris de la page.
- Hébergement : Martin ne veut pas d'adresse GitHub. Netlify et Vercel n'ont ni CLI ni jeton sur ce Mac, et Netlify n'est pas connecté dans Chrome : impossible sans que Martin se connecte ou achète un domaine.

## v4 (23/09/2026, 00h30) et domaine
- Pied de page supprimé (plus de ligne contact, plus d'icônes). Surlignage jaune des mots-clés voulus par Martin, ligne par ligne, avec `box-decoration-break:clone` pour que le surlignage suive les retours à la ligne.
- Domaine : Martin achète `martinbeauval.com` (libre le 23/09 à 00h30, .com et .fr). Registrar proposé : OVH (une adresse email MX Plan incluse avec le domaine : `contact@martinbeauval.com` gratuite).
- À faire dès l'achat : (1) zone DNS chez OVH : 4 enregistrements A sur `@` vers 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153, et un CNAME `www` vers `martinbeauval-sys.github.io.` ; (2) `gh api -X PUT repos/martinbeauval-sys/bio/pages -f cname=martinbeauval.com` puis HTTPS forcé ; (3) fichier `CNAME` à la racine du dépôt ; (4) mettre `https://martinbeauval.com` en bio du compte @martinbeauval.immo.

## Domaine en place (23/09/2026, 01h05)
- Commande OVH 259074789 payée par Martin (9,59 € TTC, 1 an, compte MB GROUP, identifiant mw141066-ovh). Domaine livré vers 00h40, NS dns111/ns111.ovh.net.
- Zone DNS posée en mode textuel : 4 A `@` vers 185.199.108-111.153, CNAME `www` vers martinbeauval-sys.github.io., MX et SPF OVH conservés ; entrées A/TXT OVH par défaut et `ftp` retirées.
- GitHub Pages : `cname=martinbeauval.com`, fichier CNAME dans le dépôt ; certificat HTTPS en cours d'émission (`https_enforced` à passer à true dès que https répond, script en tâche de fond).
- http://martinbeauval.com répond 200 sur la page.
- Zimbra : organisation MB GROUP, domaine martinbeauval.com en « configuration recommandée » (OVH pose MX/SPF/DKIM Zimbra). Compte `contact@martinbeauval.com` prérempli (Martin Beauval, offre Starter incluse) ; le mot de passe est saisi par Martin, jamais par Claude.
- Pièges : la fenêtre modale OVH dépasse la hauteur de la fenêtre Chrome, le bouton Suivant s'atteint par Tab ou par la touche End ; le mode textuel de la zone n'est pas dans l'arbre d'accessibilité, saisie au clavier après cmd+A.
- 09h08 : certificat HTTPS émis (il a fallu retirer puis remettre le domaine côté GitHub pour déclencher l'émission), HTTPS forcé, http redirige en 301 vers https, www répond. Boîte contact@martinbeauval.com créée par Martin (Starter, 15 Go, active). Chantier terminé.
