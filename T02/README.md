
# Introducció al Cas

A la tasca anterior heu dissenyat una política de còpies de seguretat pel nostre nou client **"Muntatges i Serveis Tècnics SL"**. Ara toca passar a l’acció i portar a la pràctica l’estudi anterior. El client demana que s’elaborin unes guies tècniques amb proves de concepte per tal que el seu personal estigui qualificat per implantar el pla de còpies de seguretat.

---

## Part 1: Còpia de Seguretat dels Equips Clients Windows

Encara que en principi el DPR no contemplaria fer còpia dels arxius locals dels equips clients, se’ns demana fer una excepció amb l’equip Windows del director de l’empresa. En aquest equip es guarda informació important que no es vol tenir accessible al servidor de fitxers de l’empresa.

### Objectiu:
Definir una política de còpies de seguretat seguint l’esquema **3-2-1**:
- **Còpia 1:** Disc secundari local.
- **Còpia 2:** Cloud (Google Drive) utilitzant **Duplicati**.

### Prova de concepte:
1. Crear una màquina virtual **Windows 11** amb dos discos:
   - Disc 1: Sistema operatiu.
   - Disc 2: 10 GB per emmagatzemar còpies.
2. Simular Google Drive amb un compte extern (no escolar).
3. Configuració:
   - Còpia del perfil d’usuari **cada hora** al disc secundari.
   - Còpia **diària a les 18:00** a Google Drive.
4. Documentar:
   - Instal·lació de **Duplicati**.
   - Configuració dels plans de còpia.
   - Proves:
     - Afegir arxius a **Documents**.
     - Esborrar contingut i restaurar des del disc secundari.
     - Restaurar des del cloud.

---

## Part 2: Còpia de Seguretat Servidor Linux

La solució proposada és **Duplicity**, que permet còpies locals i remotes. Combinat amb **cron**, es poden implementar polítiques automàtiques.

### Prova de concepte:
1. Crear una màquina virtual **Ubuntu Server** amb un segon disc de 10 GB.
2. Inicialitzar i formatar en **XFS**. Muntar manualment a `/media/backup`.
3. Instal·lar **Duplicity**.
4. Crear usuaris addicionals i arxius de prova (4 arxius de 10 MB).
5. Fer còpia de `/home`.
6. Esborrar arxius i restaurar.
7. Afegir nou arxiu (4 MB) i fer còpia incremental.
8. Desmuntar unitat de backup.

### Automatització:
- Crear **script `fullbackup.sh`**:
  - Còpia completa de `/home`.
  - Emmagatzemar al volum muntat.
  - Usar variable d’entorn `PASSPHRASE`:
    ```bash
    export PASSPHRASE=contrasenya
    ```
  - Donar permisos d’execució.
- Programar amb **cron**:
  - Execució com a root **diumenges a les 23:00**.
- Crear **script `incrementalbackup.sh`**:
  - Còpia incremental.
  - Configurar `PASSPHRASE`.
- Programar amb **cron**:
  - Execució com a root **de dilluns a dissabte a les 23:00**.

---

## Materials i Links de Suport
- [Duplicati](https://duplicati.com/)
- [Creando archivos con fsutil (Windows)](https://waytoit.wordpress.com/2015/03/15/creando-archivos-con-fsutil/)
- [Creando archivos de prueba en Linux](https://waytoit.wordpress.com/2015/03/21/creando-archivos-de-prueba-en-linux/)
- [Duplicity man page](http://manpages.ubuntu.com/manpages/trusty/man1/duplicity.1.html)
- [Programant tasques amb cron](https://geekytheory.com/programar-tareas-en-linux-usando-crontab)
