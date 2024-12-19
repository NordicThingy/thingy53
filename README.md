# Station Météo Matter avec thingy:53

Il facilite la réception des données via Matter. Grâce à ce code, vous pouvez facilement interagir avec les capteurs et les services fournis par le Thingy:53.

**Matériel nécessaire:**
- Thingy:53
- Câble USB-C
- nRF Connect for Desktop avec l'outil programmer
- Visual Studio Code (VS Code)
- nRF Connect sur téléphone

**Installation et Configuration:**
Pour exécuter ce projet, vous devez installer et configurer le nRF Connect for Desktop et Visual Studio Code (VS Code). 

Note : Assurez-vous que la chaîne d'outils (Toolchain) et le SDK sont installés sur le disque C:\ de l'ordinateur, dans un dossier dédié. Le dossier contenant le code pour le Thingy:91 doit également être placé dans un dossier de programmation sur le disque C:\.

Suivez les étapes ci-dessous pour la configuration :
1. Installation des outils en ligne de commande nRF
  - Téléchargez et installez les nRF Command Line Tools depuis le lien suivant : https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download.
  - Les nRF Command Line Tools incluent nrfjprog, un outil essentiel pour flasher le firmware sur vos kits de développement Nordic.

2. Installation de Visual Studio Code
  - Rendez-vous sur https://code.visualstudio.com/download et installez la version de VS Code correspondant à votre système d'exploitation.

3. Installation du nRF Connect Extension Pack dans VS Code
  - Dans la barre d'activités de VS Code, cliquez sur l'icône Extensions.
  - Recherchez nRF Connect for VS Code Extension Pack, puis cliquez sur Installer.

Le nRF Connect Extension Pack dans VS Code permet de :
  - Développer, créer, déboguer et déployer des applications embarquées basées sur le SDK nRF Connect.
  - Interagir avec le compilateur, l'éditeur de liens, le système de construction complet, un débogueur compatible RTOS, et le SDK nRF Connect.
  - Utiliser un éditeur visuel pour les fichiers Devicetree et un terminal série intégré.

4. Installation de la chaîne d'outils (Toolchain) sur VS Code
- Lors du premier lancement de l'extension nRF Connect for VS Code (cliquez sur l'extension dans la barre de gauche), vous serez invité à installer une Toolchain. Si aucune n'est détectée, procédez ainsi :
    - Cliquez sur Installer la Toolchain.
    - Choisissez une version compatible avec la version du SDK nRF Connect que vous utiliserez (la dernière version recommandée).
    - L'installation peut prendre quelques minutes.

5. Installation du SDK nRF Connect

Dans nRF Connect pour VS Code, cliquez sur Gérer le SDK.

Dans cette section, vous pourrez installer, désinstaller et sélectionner la version active du SDK.
- Cliquez sur Installer le SDK pour afficher les versions disponibles et choisir celle que vous souhaitez utiliser et installer la, le mieux est de sélectionner la dernière sans parenthèse.
- Une fois ces étapes terminées, votre environnement est prêt pour le développement avec le SDK nRF Connect et Visual Studio Code.

**Envoi du code au Thingy:53:**
- Connectez la carte Thingy:53 à votre ordinateur via un câble micro-USB.
- Allumez la carte en appuyant sur le bouton SW1 puis en activant l'interrupteur ON/OFF.

![thingy53](https://github.com/user-attachments/assets/3cd97461-9562-450e-85fc-998dda2f8b63)
-  Ouvrez nRF Connect for Desktop, puis l'outil Programmer (à installer si nécessaire).
- Cliquez sur Select a Device et sélectionnez le Thingy:53 dans la liste.
- Dans Add File, cliquez sur Browse, allez dans le dossier téléchargé > ouvrez le dossier .zip.
- Cliquez ensuite sur Write, puis Write à nouveau dans la fenêtre de confirmation pour flasher le code.

**Pairage avec Matter :**
1. Activation du mode de pairage
- Appuyez sur le bouton utilisateur du Thingy:53 jusqu'à ce que la LED clignote, indiquant le mode de pairage.

2. Ajout au réseau Matter
- télécharger et lancez une application Matter sur un appareil compatibles (smartphone ou hub domestique) (exemple avec Google Home à télécharger sur un téléphone)
- Ouvrir l'application et connectez vous avec un compte Google
- Suivez les instructions pour configurer un domicile si ce n’est pas encore fait.
- Dans l’application Google Home, dans le sous menu Appareils, cliquez sur Ajouter un appareil, puis sur "Appareil compatible avec Matter"
- Scannez le QR code fourni avec le Thingy:53 avec la nouvelle page ouverte
- Une fois le Thingy:53 ajouté à Google Home, il aparaitra comme un dispositif dans votre réseau domestique
- L'application affichera les données disponibles provenant des capteurs.

⚠️Il faut un appareil connecté Google pour que cette méthode fonctionne (Wifi, écran, enceinte)
Si vous n'en avez pas, il existe d'autres applications
