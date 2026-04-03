# LAB10 - Laboratoire de Sécurité Android (Instrumentation Frida)

Ce projet est un laboratoire d'étude sur l'instrumentation dynamique d'applications Android utilisant **Frida**.

## 🛠 Étape 1 : Installation du client Frida

Le « client » correspond aux outils installés sur votre ordinateur (frida-tools et bibliothèque Python) qui permettront d'envoyer des scripts d'injection vers l'application.

### 1.1. Préparer Python et pip

<img width="446" height="32" alt="image" src="https://github.com/user-attachments/assets/623335b9-6b90-4cb2-baeb-9435240cf55e" />

<img width="491" height="41" alt="image" src="https://github.com/user-attachments/assets/133dd994-adf8-498a-9039-aba8883ac66f" />

### 1.2. Installer frida et frida-tools

<img width="167" height="34" alt="image" src="https://github.com/user-attachments/assets/21d7ffd7-9f4a-40df-a4a1-c0038715c893" />

<img width="491" height="352" alt="image" src="https://github.com/user-attachments/assets/c753b09d-9eb0-4c80-a4fa-4a58bfd447fd" />

<img width="488" height="38" alt="image" src="https://github.com/user-attachments/assets/e07f2bd1-c1d8-4f49-8527-c6549f70feae" />

*Résultat attendu : un numéro de version (ex: 16.x.y).*

## 📱 Étape 2 : Installation des outils Android (ADB)

Pour que Frida puisse communiquer avec votre application `LAB10SEC`, vous devez configurer le pont de débogage Android (**ADB**).

## Étape 2 — Installation des outils Android (ADB)

🔹 Télécharger Platform Tools

👉 https://developer.android.com/tools/releases/platform-tools

🔹 Vérifier ADB

<img width="413" height="128" alt="image" src="https://github.com/user-attachments/assets/e26d8175-ea34-4355-83e4-826531f40f6d" />



🔹 Activer le débogage USB

## Étape 3 — Récupérer et déployer frida-server (Android)

🔹 3.1 Identifier l’architecture CPU

Avant d’installer frida-server, il faut connaître l’architecture de ton appareil :

<img width="362" height="30" alt="image" src="https://github.com/user-attachments/assets/2dd3842c-0622-419d-ad4d-f2d19d706f31" />

🔹 3.2 Télécharger frida-server

👉 Page officielle :
https://github.com/frida/frida/releases

🔹 3.3 Décompresser le fichier

- Après extraction → renommer en : frida-server

🔹 3.4 Copier vers Android

<img width="438" height="36" alt="image" src="https://github.com/user-attachments/assets/e21e4e69-4f19-4101-8630-c14247e7c8b6" />

🔹 3.5 Donner les permissions

<img width="485" height="25" alt="image" src="https://github.com/user-attachments/assets/5e811230-8c14-47fe-929e-6d8550353691" />

🔹 3.6 Lancer frida-server

<img width="487" height="17" alt="image" src="https://github.com/user-attachments/assets/bb73f001-bba0-45a8-bcc4-e746d8740f3d" />

🔹 3.7 Vérifier que Frida fonctionne
adb shell ps | grep frida

📌 Si grep ne fonctionne pas :

adb shell ps

→ vérifier manuellement frida-server

🔹 3.8 Configurer la redirection de ports
adb forward tcp:27042 tcp:27042
adb forward tcp:27043 tcp:27043
✅ Test final

Sur ton PC :

frida-ps -U
🎯 Résultat attendu :

Liste des processus Android affichée

