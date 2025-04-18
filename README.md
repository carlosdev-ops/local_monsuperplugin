# 📦 Plugin Moodle : local_monsuperplugin

**local_monsuperplugin** est un plugin local pour Moodle, développé à des fins d'apprentissage, d'expérimentation et de démonstration.  
Il affiche un message de bienvenue configurable via l'administration du site.

> 📅 Dernière mise à jour : 2025-04-18

---

## 🎯 Objectifs

- Apprendre à structurer un plugin local
- Comprendre le cycle de vie d’un plugin Moodle
- Utiliser l’API de configuration (settings)
- Manipuler les chaînes de langue (`get_string`)
- Utiliser `get_config()` pour lire un paramètre depuis la base

---

## 🗂️ Structure du plugin

```bash
local/monsuperplugin/
├── index.php                      # Page principale du plugin
├── version.php                    # Informations du plugin
├── settings.php                   # Configuration dans l'administration
├── db/
│   └── access.php                 # Capacités (permissions) [vide pour l’instant]
├── lang/
│   └── en/
│       └── local_monsuperplugin.php  # Fichier de langue anglaise
└── README.md                      # Documentation du plugin
```

---

## ⚙️ Fonctionnalité

Le plugin :
- Affiche une page protégée par `require_login()`
- Utilise `get_config('local_monsuperplugin', 'welcomemessage')` pour afficher un message personnalisé
- Permet à un administrateur de modifier ce message via l’interface graphique de Moodle

---

## 🔧 Installation

1. Cloner ce dépôt dans le répertoire `moodle/local/` :

```bash
cd /var/www/moodle/local
git clone git@github.com:carlosdev-ops/local_monsuperplugin.git
```

2. Aller dans l’administration Moodle et installer le plugin.

3. Configurer le message d’accueil via :
```
Administration du site → Plugins → Plugins locaux → Mon super plugin
```

---

## 🧪 Exemple de configuration

Message configuré :
```
Bienvenue à tous les utilisateurs de la plateforme de test Moodle !
```

Ce message s'affichera sur la page :
```
http://votre-moodle.local/local/monsuperplugin/
```

---

## 🧑‍💻 Auteur

Carlos Costa  
GitHub : [@carlosdev-ops](https://github.com/carlosdev-ops)  
Projet personnel d'apprentissage

---

## 🔗 Liens utiles

- [Moodle Developer Docs](https://moodledev.io/)
- [API Plugins Moodle](https://moodledev.io/docs/apis/core_plugin)
- [Structure des plugins Moodle](https://moodledev.io/docs/components/plugins)

---

## 🪛 Licence

Ce projet est libre et ouvert à tous les développeurs souhaitant s’exercer sur Moodle.
