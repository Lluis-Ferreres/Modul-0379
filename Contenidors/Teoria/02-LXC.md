## Contenidors LXC
**Creació de contenidors LXC**  
Els contenidors es generen a partir de plantilles. Durant la instal·lació podem descarregar un conjunt de plantilles en local.  
Per tenir el contingut més actualitzat, el millor és descarregar les plantilles des del núvol. Aquí veiem un exemple de com es pot realitzar:  
`lxc-create -n test -t download -- -d centos -r 9-Stream -a amd64`

**lxc-create**: és l'ordre que permet generar nous contenidors  
**-n test**: amb l'opcio -n posarem un nom al nostre contenidor per facilitar-nos la gestió, doncs ens permetrà reconèixer amb més facilitat de quina és la feina que realitzarà aquest contenidor  
**-t download**: paràmetre que indica que les plantilles (templates) es descarreguen del núvol  
**--**: permet introduir la informació necessària per descarregar la plantilla des de la mateixa línia d'ordres si la coneixem o esperar a que ens la mostri l'assistent durant la creació  
**-d centos**: podem indicar la distribució, en aquest cas centos  
**-r 9-Stream**: també la versió a descarregar  
**-a amd64**: i finalment la plataforma o arquitectura amb la que necessitem treballar

Si no coneixem alguna d'aquestes dades durant la creació l'assistent ens guiarà mostrant-nos les diferents opcions disponibles. Si triem aquesta forma de creació, podem fer l'ordre reduïda:  
`lxc-create -n test -t download --`

**Eliminar contenidors LXC**  
En cas de necessitar esborrar un contenidor, utilitzarem la següent ordre seguint amb l'exemple a utilitzar a tota la guia:  
`lxc-destroy test`

**lxc-destroy**: ordre per eliminar un contenidor  
**test**: nom del contenidor a eliminar

D'aquesta forma s'eliminarà el contenidor de nom *test*

**Entrar al contenidor LXC**  
Per utilitzar el contenidor es poden realitzar diferents tipus de connexions, per exemple SSH. Una forma de connectar amb el contenidor des de la terminal un cop instal·lat i sense res configurat, pot ser la següent:  
`lxc-attach test`

**lxc-attach**: ordre de LXC per connectar a un contenidor  
**test**: nom del contenidor on volem accedir

**Gestionar la xarxa del contenidor LXC**  
Els contenidors s'emmagatzemen al sistema hoste i és allà on es defineixen les seves característiques (amb els fitxers de configuració dels recursos) i l'espai d'emmagatzematge que necessitin.

En el cas de la xarxa, podem localitzar en aquesta ruta els fitxers de configuració que ens permetran modificar allò que sigui necessari:  
`/var/lib/lxc/test/config`

**/var/lib/lxc**: serà comuna per defecte per tots els contenidors  
**test**: correspondrà al nom del contenidor, per seguir amb l'exemple és test  
**/config**: és el fitxer a modificar si cal


*Apunts en desenvolupament*
## Més informació
Agraïments a les següents webs:  
[Tutorial Oficial](https://linuxcontainers.org/lxc/introduction/ "Tutorial contenidors LXC")
