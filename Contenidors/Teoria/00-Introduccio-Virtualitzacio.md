# Virtualització

La **virtualització** sorgeix per aprofitar al màxim el rendiment del maquinari.

El concepte ja apareix a finals dels anys 60 i principis dels 70 als sistemes de temps compartit de l'empresa IBM. Com aquelles màquines eren extremadament cares, s'havien d'aconseguir beneficis a nivell de rendiment computacional.  
Des d'aleshores la tecnologia ha evolucionat molt, però la finalitat avui en dia és la mateixa: maximitzar el rendiment dels centres de dades, augmentant la seguretat i fiabilitat dels sistemes.

Les noves CPUs incorporen més núclis, més RAM, els sistemes gestionen més capacitat d'emmagatzematge i han de respondre més ràpidament davant errors i problemes de connectivitat. La virtualització ajuda a resoldre gran part d'aquestes necessitats, amb un menor temps de reacció si alguna cosa falla.

## Tipus de hypervisors

Els **hypervisors** són elements que gestionaran la virtualització dintre de l'ordinador amfitrió, on s'executarà una màquina virtual o hoste.

1. **Tipus 1: nadius o bare metal**, s'executa un sistema operatiu molt lleuger que permet la creació de màquines virtuals. Alguns exemples són: *Oracle VM, Microsoft Hyper-V, VMware ESXi i Xen*.
2. **Tipus 2: allotjat**. En aquest cas es necessita un sistema operatiu complet amb un programari específic que permet l'execució de les màquines virtuals. Exemples: *Oracle VirtualBox, VMware Server i Workstation, Microsoft Virtual PC, KVM, QEMU i Parallels*.

## Tipus de virtualització

Dintre dels diferents tipus de virtualització trobarem:

1. Màquina virtual: es simula tot el maquinari d'un ordinador per executar el software necessari. Normalment és més pesada d'executar doncs ha de transformar les peticions d'un determinat tipus de controladors a execució d'ordres a la màquina real, el que fa baixar el rendiment de la màquina amfitriona.
2. Contenidors: s'aprofita el nucli del sistema operatiu per tal d'executar el programari, redueix el consum de recursos i és molt més lleugera.

En aquest mòdul treballarem els **contenidors**, on veurem diferents tipus per tal de poder triar la millor opció davant d'una necessitat.
