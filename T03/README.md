
# Pla de Contingència i Continuïtat del Negoci  
## Introducció al Cas

Recordeu el cas del portàtil al que no es podia accedir? En aquella situació la vostra perícia tant a l’hora de recuperar l’accés com a la posterior fortificació de l’accés, va deixar prou impressionat al client. Per tant, ha requerit que hi participeu en el seu nou encàrrec.

El client ha encarregat l’elaboració d’un **Pla de Contingència i Continuïtat del Negoci**, que inclou el **Pla de Recuperació davant Desastres (DRP)**. Aquest pla contempla tots els processos per restaurar dades, hardware i software crític davant d’un esdeveniment catastròfic, amb l’objectiu de recuperar l’activitat normal el més ràpid possible.

Un dels punts clau és assegurar que els treballadors disposin ràpidament dels seus equips en cas de robatori, avaria, etc. Per això, cal crear **imatges de restauració del sistema** que permetin reinstal·lar tot (SO, configuracions, aplicacions) sense processos manuals llargs.

Els equips del client són **GNU/Linux Zorin OS 18** amb aplicacions ja configurades.

---

## Fase 1: Anàlisi i Justificació de la Solució Tècnica

Cal investigar eines per crear imatges del disc complet, que permetin restaurar-lo mantenint configuracions i aplicacions. Existeixen solucions comercials i comunitàries.

### Comparativa (2 comercials + 2 comunitat)

| Producte        | Tipus       | Característiques principals | Preu aproximat |
|-----------------|------------|-----------------------------|---------------|
| **Acronis Cyber Protect** | Comercial | Backup complet, clonació, protecció ransomware | Des de 85 €/any |
| **EaseUS Todo Backup** | Comercial | Clonació de disc, còpies incrementals, suport multiplataforma | Des de 59 €/any |
| **Clonezilla** | Comunitat | Clonació i restauració, suport per múltiples FS, gratuït | Gratuït |
| **Rescuezilla** | Comunitat | Interfície gràfica, còpia i restauració fàcil, compatible amb Clonezilla | Gratuït |

**Proposta:**  
Recomanem **Rescuezilla** per la seva simplicitat, compatibilitat amb formats habituals i cost nul. Ideal per entorns Linux i proves ràpides.

---

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

### Objectiu:
- Crear una imatge completa del sistema.
- Restaurar la imatge sobre una màquina neta (VM idèntica).

### Procediment amb Rescuezilla:
1. **Preparació:**
   - Descarregar ISO de [Rescuezilla](https://rescuezilla.com).
   - Crear màquina virtual amb Zorin OS 18 (OVA proporcionada).
   - Afegir segon disc per emmagatzemar la imatge.

2. **Crear imatge del sistema:**
   - Arrencar la VM amb Rescuezilla.
   - Seleccionar opció **Backup**.
   - Triar disc origen (Zorin OS) i destí (disc secundari).
   - Configurar compressió i iniciar còpia.

3. **Restaurar imatge:**
   - Crear nova VM idèntica (sense SO).
   - Arrencar amb Rescuezilla.
   - Seleccionar opció **Restore**.
   - Triar imatge guardada i disc destí.
   - Confirmar restauració.

4. **Validació:**
   - Reiniciar la VM restaurada.
   - Comprovar que les configuracions i aplicacions es mantenen.

---

## Materials i Links de Suport
- [INCIBE: ¿Ya tienes tu Plan de Recuperación ante Desastres?](https://www.incibe.es/empresas/blog/tienes-tu-plan-recuperacion-desastres)
- [Rescuezilla - Pàgina oficial](https://rescuezilla.com)
