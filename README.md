## Configuration des clés SSH pour GitHub

### Génération de la paire de clés SSH

1. Ouvrez un terminal sur votre système d'exploitation.

2. Exécutez la commande suivante pour générer une nouvelle paire de clés SSH :
   ```bash
   ssh-keygen -t rsa -b 4096 -C "votre@email.com"
   ```
   Veillez à remplacer "votre@email.com" par votre propre adresse e-mail.

3. Suivez les instructions à l'écran pour spécifier l'emplacement où enregistrer la paire de clés et, si nécessaire, un mot de passe pour sécuriser votre clé privée.

### Ajout de la clé publique à votre compte GitHub

1. Copiez le contenu de votre clé publique en utilisant la commande suivante (sur Unix/Linux) :
   ```bash
   cat ~/.ssh/id_rsa.pub
   ```
   Sur Windows, utilisez cette commande :
   ```bash
   type C:\chemin\vers\votre\fichier\id_rsa.pub
   ```

2. Connectez-vous à votre compte GitHub et accédez aux paramètres de sécurité.

3. Cliquez sur "Clés SSH et GPG" dans la barre latérale.

4. Cliquez sur "Nouvelle clé SSH".

5. Collez le contenu de votre clé publique dans le champ "Clé" et donnez-lui un titre descriptif.

6. Cliquez sur "Ajouter une clé SSH" pour enregistrer la clé sur votre compte GitHub.

### Utilisation de la clé SSH pour les opérations Git

1. Assurez-vous que votre clé privée est chargée dans votre agent SSH en utilisant la commande suivante :
   ```bash
   ssh-add ~/.ssh/id_rsa
   ```

2. Vous pouvez désormais cloner, pousser et accéder à vos dépôts GitHub sans avoir à entrer de nom d'utilisateur ou de mot de passe.
