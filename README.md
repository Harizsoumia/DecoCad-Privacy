# 🔒 Politique de Confidentialité — Bot Messenger Decocad

> **Dernière mise à jour :** Septembre 2026  
> **Portée :** Agent conversationnel automatisé (Facebook Messenger API / n8n / OpenAI)

---

## 📋 1. Overview & Engagement

La présente politique de confidentialité définit les modalités de collecte, de traitement et de protection des données à caractère personnel traitées par l'agent conversationnel automatisé (bot Messenger) de la page **Decocad**. 

En interagissant avec notre bot, l'utilisateur accepte les pratiques décrites ci-dessous. Notre architecture est conçue selon les principes de minimisation des données et de sécurité dès la conception (*Privacy by Design*).

---

## 🛠️ 2. Données Collectées

Dans le cadre du traitement des commandes et de la relation client, le système collecte automatiquement et de manière structurée :

| Catégorie | Données Collectées | Finalité Technique |
| :--- | :--- | :--- |
| **Identifiants Réseau** | *Page-Scoped User ID* (PSID) | Maintien de l'état de la session conversationnelle (*State Management*). |
| **Profil Public** | Nom et prénom public Facebook | Personnalisation du contexte d'échange. |
| **Contenu des échanges** | Historique des messages texte et vocaux | Analyse du besoin par l'IA et résolution des requêtes. |
| **Données de Logistique** | Adresse de livraison, numéro de téléphone | Traitement, confirmation et suivi des expéditions. |

---

## 🔄 3. Architecture Technique & Data Workflow

L'exécution des traitements repose sur un pipeline automatisé sécurisé :

```text
[Utilisateur Facebook]
       │
       ▼ (Webhook / HTTPS TLS 1.3)
[Meta Graph API (Messenger)]
       │
       ▼
[Workflow Engine: n8n] ──(Nettoyage & Sécurisation JSON)
       │
       ├────► [LLM Processing: OpenAI API] (Analyse contextuelle en Darija Algérienne)
       │
       └────► [Database/Storage: Google Sheets API] (Structuration des commandes)
