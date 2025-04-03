scripts_copieurs_xerox
Fichiers
Copieurs Xerox.csv : Listing des copieurs
Script INSTALL CONFIG PRINTERS + Task planner.ps1 : script d'installation des pilotes, imprimantes et configurations. Ce script crée également une tâche dans le planificateur pour copier si nécessaire la configuration de préférence pour les impressions couleurs
Script MAJ COLOR PREF PRINTERS.ps1 : script automatisé via planificateur de tâches
install.ps1 / uninstall.ps1 : scripts d'installation / désinstallation
Génération du package intunewin
Télécharger l'utilitaire de packaging depuis le site officiel de Microsoft, se positionner dans un shell Powershelle dans le répertoire de téléchargment de l'utilitaire et lancer la commande suivante :

.\IntuneWinAppUtil.exe -c "C:\Users\AliceQUERIC\ARMLB\Pays de Brest - t5_informatique\Infrastructure\Ordinateurs\Scripts paramétrage\Copieurs\scripts_copieurs_xerox" -s "C:\Users\AliceQUERIC\ARMLB\Pays de Brest - t5_informatique\Infrastructure\Ordinateurs\Scripts paramétrage\Copieurs\scripts_copieurs_xerox\install.ps1" -o "C:\Users\AliceQUERIC\ARMLB\Pays de Brest - t5_informatique\Infrastructure\Intune"

Génération de l'application Win32
Commande d'installation
Lors de la création de l'application Win32 sur Intune, utiliser la commande d'installation suivante : Powershell.exe -NoProfile -ExecutionPolicy ByPass -File .\install.ps1

Utiliser la commande de désinstallation : Powershell.exe -NoProfile -ExecutionPolicy ByPass -File .\uninstall.ps1

Vérification de l'installation
Spécifier le mode de vérification par clé de registre en vérifiant que la clé HKLM:\SYSTEM\CurrentControlSet\Control\Print\Printers\Bellevue Accueil\PrinterDriverData existe.
