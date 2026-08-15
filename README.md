# creality-K1C

📚 Ressources, Root et Astuces pour Creality K1C

Ce document regroupe les liens officiels, les procédures de mise à jour strictes, le root, et des astuces pour bypass les tests forcés au démarrage.
🔗 Liens Utiles et Officiels

    Fichiers d'origine clé USB (Dump intégral) : Google Drive
    Firmware officiel K1C : Creality Cloud
    Wiki officiel Creality : wiki.creality.com
    Firmware Recovery Tool (Outil de récupération officiel) : GitHub Creality
    Releases Officielles Klipper (K1 Series) : GitHub Creality

⚠️ Procédure de mise à jour stricte

Veuillez suivre l'instruction ci-dessous strictement avant d'installer le dernier micrologiciel. Sinon, l'installation du dernier micrologiciel risque d'échouer et de briquer l'imprimante.

    Pour les micrologiciels V1.2.9.14 et antérieurs :
        Mettre à jour vers V1.2.9.15 (via USB Drive)
        Mettre à jour vers V1.2.9.22 (via OTA/USB Drive)
        Mettre à jour vers V1.3.0.30 (via OTA/USB Drive)
        Mettre à jour vers V1.3.1.4 (via USB Drive ou Creality Cloud APP)

    Pour les micrologiciels V1.2.9.17 à 1.2.9.21 :
        Mettre à jour vers V1.2.9.22 (via OTA/USB Drive)
        Mettre à jour vers V1.3.0.30 (via OTA/USB Drive)
        Mettre à jour vers V1.3.1.4 (via USB Drive ou Creality Cloud APP)

    Pour le micrologiciel V1.3.0.30 :
        Mettre à jour vers V1.3.1.4 (via USB Drive ou Creality Cloud APP)

    Pour les micrologiciels V1.3.1.4 et au-dessus :Vous pouvez installer les derniers micrologiciels directement.

🔓 Root et installation du Helper Script (Guilouz)

Le Helper Script de Guilouz est indispensable pour débloquer le plein potentiel de la K1C (ajout de modules, Camera, Remote Access, etc.).
1. Activer le Root

    Sur l'écran de l'imprimante : "Paramètre" ==> "Information du compte root" ==> patienter 30 secondes ==> "Oui".

2. Connexion SSH

Connectez-vous en SSH à l'imprimante (via PuTTY ou MobaXterm).

    Utilisateur : root
    Mot de passe : creality_2023 (Note : sur certaines versions, le mot de passe est simplement creality).

3. Installation du script

Dans le terminal SSH, rendez-vous dans le dossier des données utilisateur :

cd /usr/data

Clonez le dépôt du script (en profondeur 1 pour aller plus vite) :
bash
 
  
 
 
git clone --depth 1 https://github.com/Guilouz/Creality-Helper-Script.git /usr/data/helper-script
 
 

Lancez le script d'installation :
bash
 
  
 
 
sh /usr/data/helper-script/helper.sh
 
 

⚠️ Si vous rencontrez une erreur de clone (problème de certificat SSL), entrez cette commande avant de relancer le git clone :
bash
 
  
 
 
git config --global http.sslVerify false
 
 
4. Modules recommandés à installer

Une fois dans le menu du Helper Script, installez les modules de votre choix :

     Essentials (KlipperScreen, etc.)
     Utilities (Mainsail, Fluiss, etc.)
     Improvements
     Camera
     Remote access

🛠️ Astuces de Premier Démarrage (Bypass Selftest)

Pour passer les tests forcés au premier démarrage ou après une mise à jour du firmware, vous pouvez utiliser un fichier de débogage.

Procédure :

    Prenez un fichier texte vide sur votre PC.
    Renommez-le exactement : debugmode_JumpSelftest
    ATTENTION : Assurez-vous qu'il n'a aucune extension (pas de .txt à la fin). Si Windows cache les extensions, affichez-les dans l'explorateur pour être sûr.
    Copiez ce fichier à la racine de votre clé USB.
    Branchez la clé USB sur l'imprimante et allumez-la. Les tests de calibrage forcés seront automatiquement ignorés.


🔓 Décryptage des Logs Cachés (Archives ZIP)

Creality chiffre certaines archives de logs complètes (ou fichiers de configuration cachés) pour empêcher les utilisateurs de voir l'intégralité des données système de la machine. 

Si vous avez extrait une archive .zip provenant de l'imprimante et qu'elle vous demande un mot de passe pour s'ouvrir, voici la clé de décompression (toujours fonctionnelle à ce jour) :

    Mot de passe de l'archive ZIP : 

    q!ew5rN7@U2s7;L

Comment l'utiliser :

    Téléchargez et installez le logiciel gratuit 7-Zip ou WinRAR sur votre PC Windows.
    Faites un clic droit sur le fichier .zip protégé.
    Choisissez "Extraire ici" (ou "Extraire vers...").
    Une fenêtre va s'ouvrir vous demandant le mot de passe.
    Copiez-collez la clé ci-dessus et validez. Vous aurez alors accès aux fichiers système et logs bruts non filtrés par Creality.
