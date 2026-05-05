# 🔐 LAB 13 – Bypass Root Detection Android avec Objection

---

## 🎯 Objectif

Réaliser un bypass de la détection de root sur une application Android (DIVA) en utilisant Frida et Objection.

---

## 🧰 Outils utilisés

- Frida  
- Objection  
- ADB (Android Debug Bridge)  
- Android Emulator / Téléphone rooté  
- Application DIVA  

---

## ⚙️ Étapes réalisées

---

### 🔹 1. Installation d’Objection

Commande :

pip install objection

📸 Capture :

<img width="1651" height="531" alt="9" src="https://github.com/user-attachments/assets/12286a4e-fe52-48d3-b7be-29f7e43c1963" />

---

### 🔹 2. Vérification de l’environnement

Commandes :

objection version  
frida-ps -U  

📸 Capture :

<img width="705" height="498" alt="10" src="https://github.com/user-attachments/assets/a3009054-e9cd-43f7-9f3d-f7b3df2986fa" />

---

### 🔹 3. Identification de l’application cible

Commande :

frida-ps -Uai  

Application utilisée :

jakhar.aseem.diva  

---

### 🔹 4. Lancement d’Objection

Commande utilisée :

objection -g jakhar.aseem.diva explore --startup-command "android root disable"

Commande recommandée :

objection -n jakhar.aseem.diva start --startup-command "android root disable"

📸 Capture :

<img width="1168" height="491" alt="11" src="https://github.com/user-attachments/assets/502b4f61-887f-4a94-8edb-3df278a7bfcb" />

---

### 🔹 5. Bypass de la détection root

Commande :

android root disable  

✔️ Actions réalisées :

- Hook des fonctions de détection root  
- Modification des valeurs retournées  
- Blocage des vérifications système  

---

### 🔹 6. Résultat

- ❌ Avant : Root détecté  
- ✅ Après : Root non détecté  
- ✅ Application fonctionne normalement  

---


## 🏁 Conclusion

- Les protections root côté Java sont faibles  
- Frida + Objection permettent un bypass rapide  
- Les protections natives sont plus sécurisées  

---
