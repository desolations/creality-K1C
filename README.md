# creality-K1C

Fichiers d'origine clé USB :
https://drive.google.com/file/d/1fL6c-QzP4bHb-R6DtrqvfmHobE6odOhC/view?usp=drive_link

Lien vers le firwmare pour K1C :
https://www.crealitycloud.com/downloads/firmware/flagship-series/k1c

Wiki officiel Creality :
https://wiki.creality.com/en/k1-flagship-serieshttps://wiki.creality.com/en/k1-flagship-series

 Firmware recovery tool :
 https://github.com/CrealityOfficial/K1_Series_Annex/releases/tag/V1.0.0

 Release :
 https://github.com/CrealityOfficial/K1_Series_Klipper/releases

 Klipper :
 https://github.com/Guilouz/Creality-Helper-Script-Wiki

 Root and Install Klipper to Creality K1C :
 https://guilouz.github.io/Creality-Helper-Script-Wiki/firmwares/install-and-update-rooted-firmware-k1/

 Install via script :
 https://guilouz.github.io/Creality-Helper-Script-Wiki/helper-script/helper-script-installation/

Veuillez suivre l'instruction ci-dessous strictement avant d'installer le dernier micrologiciel. Sinon, l'installation du dernier micrologiciel risque de faire faillite.

Pour les micrologiciels V1.2.9.14 et antérieurs:
 :: Mise à jour de V1.2.9.15via USB Drive
 :: Mise à jour de V1.2.9.22via OTA/USB Drive
 :: Mise à jour de V1.3.30via OTA/USB Drive
 :: Mise à jour de V1.3.1.4via USB Drive ou à partir de Creality Cloud APP

Pour le micrologiciel V1.2.9.17 à 1.2.9.21:
 :: Mise à jour de V1.2.9.22via OTA/USB Drive
 :: Mise à jour de V1.3.30via OTA/USB Drive
 :: Mise à jour de V1.3.1.4via USB Drive ou à partir de Creality Cloud APP

Pour le micrologiciel V1.3.0.30:
 :: Mise à jour de V1.3.1.4via USB Drive ou à partir de Creality Cloud APP

Pour les micrologiciels V1.3.1.4 et au-dessus:
Vous pouvez installer les derniers micrologiciels ci-dessous.


1) ROOT :

   "Paramètre" ==> "information du compte root" ==> patienter 30s ==> "oui"

2) SSH connect

   user = " root "
   password = " creality_2023 "

3) Folder
  go to folder " usr/data "

4) GIT
   paste :
   git clone --depth 1 https://github.com/Guilouz/Creality-Helper-Script.git /usr/data/helper-script

   run :
   sh /usr/data/helper-script/helper.sh

   If you encounter an issue to clone Helper Script repository, enter this command before cloning:
   git config --global http.sslVerify false

5) Install
   - Essentials
   - Utilities
   - Improvements
   - Camera
   - Remote access
