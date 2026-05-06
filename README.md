# LAB10 - Laboratoire de Sécurité Android (Instrumentation Frida)

Ce projet est un laboratoire d'étude sur l'instrumentation dynamique d'applications Android utilisant **Frida**.

## Étape 1 : Installation du client Frida

Le « client » correspond aux outils installés sur votre ordinateur (frida-tools et bibliothèque Python) qui permettront d'envoyer des scripts d'injection vers l'application.

### 1.1. Préparer Python et pip

<img width="592" height="79" alt="image" src="https://github.com/user-attachments/assets/e0623572-1e09-41e5-8e59-4f87f5642dfe" />

### 1.2. Installer frida et frida-tools

<img width="890" height="455" alt="image" src="https://github.com/user-attachments/assets/0328bbf4-396e-44a7-819b-cd27f1c666de" />

- Vérifications CLI:

  <img width="379" height="491" alt="image" src="https://github.com/user-attachments/assets/552cd10c-035f-46c7-9121-97bb8507fe78" />
  

##  Étape 2 : Installation des outils Android (ADB)

Pour que Frida puisse communiquer avec votre application `LAB10SEC`, vous devez configurer le pont de débogage Android (**ADB**).

<img width="419" height="125" alt="image" src="https://github.com/user-attachments/assets/91d44cb2-b80b-4756-9e7e-11ba6c35a1f3" />

## Étape 3 — Récupérer et déployer frida-server (Android)

### 3.1. Identifier l’architecture CPU de l’appareil

<img width="281" height="31" alt="image" src="https://github.com/user-attachments/assets/62c079fc-59d9-4a99-86be-7032e5f39922" />

### 3.2. Télécharger frida-server compatible

 -frida-server-17.9.1-android-x86_64.xz
 
### 3.3. Décompresser l’archive téléchargée

<img width="182" height="128" alt="image" src="https://github.com/user-attachments/assets/f147b808-4c72-45c0-a636-bfdecb02e46d" />

### 3.4. Copier frida-server vers l’appareil Android

<img width="451" height="31" alt="image" src="https://github.com/user-attachments/assets/c778a346-a781-4b4c-ba95-513c95570e1e" />

### 3.5. Rendre le fichier exécutable

<img width="403" height="38" alt="image" src="https://github.com/user-attachments/assets/3a7184c8-1eed-430f-867e-b4e509014936" />

### 3.6. Lancer frida-server

<img width="554" height="73" alt="image" src="https://github.com/user-attachments/assets/463433d8-7869-4797-a735-273873138762" />

### 3.7. Vérifier que frida-server est bien actif

<img width="415" height="490" alt="image" src="https://github.com/user-attachments/assets/e9f5c29f-59fd-4bbc-b4ce-1c51924b68f7" />


<img width="550" height="478" alt="image" src="https://github.com/user-attachments/assets/be534285-ba95-4fb3-a2dd-bef23790e316" />


<img width="497" height="32" alt="image" src="https://github.com/user-attachments/assets/c6dd87d9-f0fa-483c-9039-ee30a8b3589f" />


### 3.8. Configurer la redirection de ports ADB

<img width="345" height="72" alt="image" src="https://github.com/user-attachments/assets/942fa00f-dfd5-4c9d-866d-49656c0b0f1c" />

## Étape 4 — Test de connexion depuis le PC

<img width="359" height="494" alt="image" src="https://github.com/user-attachments/assets/895d3fac-17c7-4e7d-8270-df8fee04e0bb" />

<img width="371" height="317" alt="image" src="https://github.com/user-attachments/assets/69354a73-7079-48ef-8348-6256931f1b2e" />

## Étape 5 — Injection minimale pour valider

### 5.1 Test simple avec l’API Java

<img width="569" height="91" alt="image" src="https://github.com/user-attachments/assets/c7a7c2c6-69a0-40b8-8d82-6fb07e699045" />


<img width="289" height="184" alt="image" src="https://github.com/user-attachments/assets/27ef0652-64ae-491e-b774-9b1c2796a421" />


### 5.2 Test simple avec un hook natif

<img width="256" height="137" alt="image" src="https://github.com/user-attachments/assets/d76dfed2-e7b3-460a-aa33-16fdc1d228b1" />

## Etape 6 : - Explorer la console interactive Frida dans un contexte de sécurité

### 6.1 Vérifier l’architecture du processus

<img width="561" height="49" alt="image" src="https://github.com/user-attachments/assets/a9dfc69c-f50a-4cbd-9625-f245c13f2e50" />

### 6.2 Identifier le module principal de l’application

<img width="627" height="198" alt="image" src="https://github.com/user-attachments/assets/a0423212-fd97-4da7-9cab-0679f4a37c40" />

### 6.3 Inspecter une bibliothèque système critique

<img width="798" height="196" alt="image" src="https://github.com/user-attachments/assets/6cadba61-f744-4646-b942-c158fbe409e6" />

### 6.4 Vérifier la présence d’une fonction sensible

<img width="925" height="364" alt="image" src="https://github.com/user-attachments/assets/c1915a87-3039-4c0d-94cf-02300e4700a0" />

### 6.5 Lister les bibliothèques chargées

<img width="712" height="946" alt="image" src="https://github.com/user-attachments/assets/e55f2596-10d8-4752-bc7f-39ec8b4cc383" />

### 6.6 Lister les threads actifs

<img width="718" height="64" alt="image" src="https://github.com/user-attachments/assets/3bb7e3ce-e603-4be2-a8e5-802544377f34" />

## Étape 7 - Observer les bibliothèques de chiffrement, le stockage local et les appels réseau sensibles

#### 7.1 Repérer les bibliothèques liées au chiffrement

<img width="930" height="964" alt="image" src="https://github.com/user-attachments/assets/1549171e-5b76-4ebc-b0bb-0f24208ed722" />

### 7.2 Vérifier la présence d’une fonction réseau sensible

<img width="925" height="82" alt="image" src="https://github.com/user-attachments/assets/38978ae2-771e-46e4-bc3f-076a9ce5f600" />

### 7.3 Installer un hook sur connect

<img width="404" height="173" alt="image" src="https://github.com/user-attachments/assets/c7bad424-f1da-457f-90cd-b2e0b91ba9ce" />

### 7.4 Installer un hook sur send et recv

<img width="413" height="332" alt="image" src="https://github.com/user-attachments/assets/337a964c-bed1-4b07-8e7e-81e978d37de6" />


