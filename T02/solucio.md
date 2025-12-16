# **GUIA BACKUPS T02**
# Windows11
## Instalacio de duplicati
Entrem a la pagiaweb i iniciem sesio/crear un compte  
![img](img/img03.png)

Descarregue el duplicati.setup
![img](img/img01.png)

Initzialitzem el duplicati.setup
![img](img/img02.png)

## Configuracio
Initzialitzar la aplicacio de duplicati i seleccionem la opcio de backups
![img](img/img04.png)

1.Posem un nom i una contraseña al backup
![img](img/img05.png)

2. Seleccionem ha on voldrem guardar el backup 
![img](img/img11.png)

3. Seleccionem de que volem fer el backup si de una carpeta o de tot el sistema
![img](img/img16.png)

4. Indeiquem cada cuant volem que faci els nous backups
![img](img/img12.png)

5. Seleccionem de quina mida es fara el backup i li donem a submit
![img](img/img08.png)

## Backup
Iniciem la aplicacio de duplicati iseleccionem la opcio de restore
![img](img/img04.png)

Escollim quin backup volem initzialitzar (si tens mes d'un) i despres esperem a que el Backup termini
![img](img/img17.png)


# Ubuntus
Inicialitzem i formatem el disc amb XFS
![img](img/img18.png)

Creem la carpeta per muntar-lo

![img](img/img19.png)


Muntem manualment el disc

![img](img/img20.png)


Comprovem que hem montat el disc

![img](img/img21.png)


Instalem duplicity
![img](img/img22.png)

Creem dos usuaris
![img](img/img23.png)
![img](img/img24.png)

Creem 4 fitchers de 10 MB 
![img](img/img25.png)

Crem el backup de les carpetes que em creat

![img](img/img26.png)
![img](img/img27.png)


Borrem les 4 carpetas ateriors
![img](img/img28.png)

Fem el Buckup i comprovem que s'han recuperat
![img](img/img2.png)
![img](img/img29.png)

Creem un quint fitxer de 4 MB
![img](img/img30.png)


Fem una copia incremental
![img](img/img.png)

Posem aquest script en l'archiu fullbackup.sh
![img](img/img.png)

Donem permisos d'execucio a l'archiu
![img](img/img.png)


Programar còpia completa amb cron com a root
![img](img/img.png)

Afegim la seguent línia
![img](img/img.png)

Escrivim el seguent script a larchiu incrementalbackup.sh
![img](img/img.png)

Donem permisos d'execucio a l'archiu
![img](img/img.png)

Programar còpia incremental amb cron com a root
![img](img/img.png)

Afegim la seguent línia
![img](img/img.png)
