# JobAlert CI

Application SaaS pour diffuser automatiquement par WhatsApp les annonces d'emplois et de concours aux abonnés en Côte d'Ivoire.

## 🚀 Fonctionnalités

- Page d'inscription utilisateur (Nom, Numéro WhatsApp, Email optionnel)
- Intégration des paiements Mobile Money (Wave, Orange Money, MTN, Moov)
- Base de données Google Sheets
- Dashboard administrateur pour ajouter des offres
- Automatisation des envois WhatsApp
- Tableau de bord utilisateur avec historique 7 jours
- Deux formules d'abonnement (Standard 2500 CFA/mois, Premium 5000 CFA/mois)

## 🛠️ Technologies utilisées

- **Frontend**: Next.js 14, React, Tailwind CSS
- **Backend**: Next.js API Routes (TypeScript)
- **Base de données**: Google Sheets (via Google Sheets API)
- **Authentification**: JWT
- **Paiements**: APIs Mobile Money (Wave, Orange, MTN, Moov)
- **Notifications**: WhatsApp Cloud API

## 📁 Structure du projet

```
JobalertCI/
├── app/                 # Pages et API Next.js
├── lib/                 # Logique métier et utilitaires
├── public/              # Fichiers statiques
├── prisma/              # Schéma Prisma (désactivé)
├── .env                 # Variables d'environnement
├── package.json         # Dépendances
└── README.md            # Documentation
```

## 🚀 Installation

1. **Cloner le projet**:
   ```bash
   git clone <url-du-projet>
   cd JobalertCI
   ```

2. **Installer les dépendances**:
   ```bash
   npm install
   ```

3. **Configuration de Google Sheets**:
   - Le projet utilise Google Sheets comme base de données
   - La base de données est déjà configurée avec l'ID: `1SB7HPL5Xc_tKG9Wl4zZr96TZNXeDtM9pjt0I0qvKq2M`
   - Le fichier `jobalert-service-account.json` contient les identifiants d'authentification

4. **Configuration des variables d'environnement**:
   - Vérifiez le fichier `.env` pour les paramètres de configuration
   - Configurez les clés API pour WhatsApp et les paiements mobiles

5. **Démarrer l'application**:
   ```bash
   npm run dev
   ```

## ☁️ Déploiement sur Vercel

1. **Prérequis**:
   - Compte Vercel (https://vercel.com)
   - Variables d'environnement configurées

2. **Configuration des variables d'environnement**:
   - Dans le dashboard Vercel, allez dans "Settings" > "Environment Variables"
   - Ajoutez toutes les variables du fichier `.env` avec leurs valeurs de production

3. **Déploiement**:
   ```bash
   # Installer Vercel CLI
   npm i -g vercel
   
   # Se connecter à Vercel
   vercel login
   
   # Déployer le projet
   vercel --prod
   ```

4. **Configuration du domaine** (optionnel):
   - Dans le dashboard Vercel, allez dans "Settings" > "Domains"
   - Ajoutez votre domaine personnalisé
   - Configurez les DNS selon les instructions

## 🧪 Tester la connexion à la base de données

```bash
node test-google-sheets-connection.js
```

## 📊 Base de données

Le projet utilise Google Sheets comme base de données via l'API Google Sheets. La structure est la suivante :

- **Users**: Informations des utilisateurs
- **Subscriptions**: Abonnements des utilisateurs
- **JobOffers**: Offres d'emploi et de concours
- **JobNotifications**: Historique des notifications envoyées
- **Admins**: Comptes administrateurs

## 🔐 Authentification

- **JWT** pour l'authentification des utilisateurs et administrateurs
- **Bcrypt** pour le hachage des mots de passe

## 💰 Paiements Mobile Money

Intégration avec les APIs de:
- Wave
- Orange Money
- MTN Mobile Money
- Moov Africa

## 📱 WhatsApp Integration

Utilisation de WhatsApp Cloud API pour l'envoi automatique des notifications.

## 🎨 Design

- Interface responsive avec Tailwind CSS
- Design moderne et intuitif
- Expérience utilisateur optimisée pour mobile

## 📞 Support

Pour toute question ou assistance, contactez l'équipe de développement.

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 🤝 Contribution

1. Fork le projet
2. Créer une branche pour votre fonctionnalité
3. Commiter vos changements
4. Pousser vers la branche
5. Ouvrir une Pull Request

## 🎯 Roadmap

### Version 1.1
- [ ] Notifications push web
- [ ] Export des données en Excel
- [ ] Statistiques avancées

### Version 1.2
- [ ] Application mobile React Native
- [ ] Intégration Telegram
- [ ] Système de parrainage

### Version 2.0
- [ ] IA pour catégorisation automatique
- [ ] Recommandations personnalisées
- [ ] Multi-pays (Burkina Faso, Sénégal, Mali)

---

**Développé avec ❤️ pour la communauté ivoirienne** 🇨🇮