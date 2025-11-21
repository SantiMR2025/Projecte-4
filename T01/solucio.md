# FASE 1
## 1. Què copiar? (Priorització): 
les dades mes critiques dun servei seria els documents de projectes despres anirien la base de dades i el menys important serian les carpetes personals dels usuaris, perque la informacio mes valiosa es la que depenen el treballadors i la que mes es triguaria a refer.

## 2. Periodicitat i Tipus de Còpia: 
la mes important faria servir cada setman perque es necesita sempre tenir la versio mes actual pero no pot ser meny per el tamany que ocupen, les no tan importats seria el mateix, cada setmana per els mateixos motius i els menys importamts cada mes.

## 3. Mitjans i Ubicació: 
per la mes importat faria servis cintes magnetiques i cloud, simplement per tenir un a l'edifici que sgui resistent i el cloud per tenir informacio fora de les instalacions/edifici, les no tant important amb nas i cloud, les menys important amb disc dur extern.

# Fase 2: Treball per parelles

Treballant per parelles:

1. **Discussió i Consens:** Comparen les seves respostes individuals (Fase 1).

2. **Elaboració d'una Proposta Unificada:** Heu de consensuar i dissenyar el vostre propi *Esquema 3-2-1 de Còpies* (3 còpies, 2 mitjans, 1 fora de lloc) basat en els requisits del cas.

| **Element**               | **Proposta de la Parella** | **Justificació** |
|---------------------------|-----------------------------|-------------------|
| **Dades Crítiques**       | Base de dades               | La base de dades es la mes important ja que es la que compte dades personal de clients la quals que si perden ho perden tot. |
| **Periodicitat (BD)**     | Setmanalment                | Diariament porque si la hacemos mensualmente seria una perdida de informacion muy importante si es que se llega a perder aunque tenga la copia i semanalmente tampoco por basiamente lo mismo, ademas hacerla diariamente nos ahorramos problemas y tampoco es que pese mucho.                  |
| **Tipus de Còpia (BD)**   |      Diferencial                       |  Porque al contener informacion tan importante, tener la copia de que se ha echo cada dia es bastante seguro, ya que es muy normal que algun usuario te pida la copia exacta de un dia enconcreto        |
| **Mitjà 1 (Local)**       |            RDX                 |   Porque al ser la que estara dentro de la empresa i la que se usara la primera, interesa que sea rapida, ademas que estara protegit de terceras personas que pasan per la empresa                |
| **Mitjà 2 (Extern)**      |             Cloud                |   perque si es perd o hi ha algun desastre en la empresa tenim la seguretat que tindrem una copia de seguretat en el cloud la qual sabem que no s'haura perdun en el desastre de l'empresa                |



# Fase 3: Treball en grup

## 1) Datos Objeto de Copia

### 1.1 Servidor

#### **Datos críticos:**
- Base de dades
- Documents de Projectes
- carpeta de documents

#### **Datos no críticos:**
- Carpetes Personals dels Usuaris
  

#### **Frecuencia de copia del servidor**

**Datos críticos:**
- Frecuencia: per la base de dades i la carpeta de documents sera amb una frecuencia de diariament, mentre que els documents de projectes es fara amb una frecuecia setmanalment
- Tipo de copia: per la base de dades el tipus sera de diferencial, per la carpeta de documents sera incremental, i per els documents de projectes el tipus sera de manera total

**Datos no críticos:**
- Frecuencia: amb una frequencia mensual
- Tipo de copia: total 

---

### 1.2 Equipos Clientes

#### **Datos críticos (Documentos, trabajos, etc.):**
- Frecuencia: los documentos 
- Tipo de copia: …

#### **Datos no críticos:**
- Frecuencia: …
- Tipo de copia: …

---

## 2) Cronograma Semanal Detallado

| **Día**     | **Datos** | **Tipo de copia** | **Medio** |
|-------------|-----------|--------------------|-----------|
| **Lunes**    |           |                    |           |
| **Martes**   |           |                    |           |
| **Miércoles**|           |                    |           |
| **Jueves**   |           |                    |           |
| **Viernes**  |           |                    |           |
| **Sábado**   |           |                    |           |
| **Domingo**  |           |                    |           |

*(Rellena con BD, documentos, carpetas personales, etc.)*

---

## 3) Elección de Medios y Ubicación (Regla 3-2-1)

### 3.1 Medio 1 (Local)
- **Tipo de medio:** … (NAS, HDD externo, etc.)
- **Ubicación:** … (sala de servidores, rack, etc.)
- **Responsable:** …

### 3.2 Medio 2 (Externo)
- **Tipo de medio externo:** … (Cloud, cinta LTO…)
- **Proveedor:** … (Google Cloud, Azure, AWS…)
- **Frecuencia de actualización:** …
- **Responsable:** …

### 3.3 Ubicación Fuera de Lugar
- **Ubicación física o lógica:** …
- **Tipo de datos almacenados:** …
- **Método de acceso / seguridad:** …
- **Responsable del mantenimiento:** …

---

## 4) Estrategia de Recuperación (RTO / RPO)

### **Objetivos**
- **RPO (Recovery Point Objective):** 4 horas  
- **RTO (Recovery Time Objective):** 4 horas  

### **Cómo se garantiza el cumplimiento**
- **Tipo de copia:** …
- **Dónde están almacenadas las copias rápidas:** …

#### **Procedimiento de recuperación paso a paso:**
1. …
2. …
3. …

#### **Personal responsable de realizar o supervisar la recuperación:**
- …

---

## **Firma del grupo**
- **Alumno 1:** …
- **Alumno 2:** …
- **Alumno 3:** …
- **Alumno 4:** …
