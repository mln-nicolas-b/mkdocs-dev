## Documentation 

La documentation est fournie par MkDocs. 
Chaque personnes ayant les droits requis sur le dépôt peut l'éditer pour ajouter 
ou mettre à jour des informations.

### Installation

Installer MkDocs simplement avec le gestionnaire de paquet python :

```bash
sudo pip3 install mkdocs
```

Le thème de MkDocs est **Material**, il s'installe également avec le gestionnaire de paquet python :

```bash
sudo pip3 install mkdocs-material
```

Un plugin est actuellement en phase de test pour l'intégration de solution de schématisation.  
Étant dans la configuration de MkDocs, il est également à installer avec le gestionnaire de paquet python :

```bash
sudo pip3 install mkdocs-kroki-plugin
```

### Configuration

La configuration du wiki se trouve à la racine du dépôt, dans le fichier *mkdocs.yaml*.

Si besoin, il est possible de rajouter de nouvelle entrées dans la navigation.  
Chaque entrée correspond à un menu de la navigation et chaque sous entrée correspond 
à une redirection d'url.

```yaml
nav:
  - Home: index.md
  - Proxmox:
    - 'Installation': 'proxmox/#installation'
    - 'Gestion des accès': 'proxmox/#gestion-des-acces'
    - 'Problèmes connus': 'proxmox/#problemes-connus'
    - 'Gestion de la virtualisation': 'proxmox/#gestion-de-la-virtualisation'
  - PfSense: 
    - 'OVH': 'pfsense/#ovh'
    - 'Gestion du réseau': 'pfsense/#gestion-du-reseau'
    - 'Gestion des accès': 'pfsense/#les-acces'
    - 'Wireguard': 'pfsense/#wireguard'
    - 'REST API': 'pfsense/#rest-api'
```

!!! warning
    Ne pas toucher les configuration de plugins sans connaissances du système MkDocs !

### Usage

Lors de l'édition locale de du wiki, il est particulièrement pratique de pouvoir visualiser le rendu des modifications opérées.  
Pour cela, il est possible de déployer le wiki localement :

```bash
mkdocs serve
```

!!! tip
    Ne pas oublier de commiter le code puis de le pousser sur la branch main pour 
    mettre à disposition à tous les collaborateurs, la dernière version du wiki.

Lorsque le résultat final est obtenu, il suffit le pousser sur la branch distante :

```bash
mkdocs gh-deploy
```

!!! info
    MkDocs gère seul le déploiement du wiki sur github.  
    Le code va ainsi être transformer en site statique puis poussé sur une branch distinct.  
    Les pages github pointent sur la racine de cette branche pour exposer le wiki.

Documentation accessible [ici](https://vigilant-bassoon-10fe5865.pages.github.io/)
