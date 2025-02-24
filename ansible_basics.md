TAREA 4: INVESTIGACIÓN

1 ¿Qué es Ansible y por qué es "sin agente" (agentless)?
Ansible es una herramienta de automatización y gestión de configuración que permite 
administrar infraestructuras de manera sencilla mediante archivos YAML. Es "sin agente"
porque no requiere la instalación de software en los nodos administrados; en su lugar, se
conecta a ellos usando SSH y ejecuta tareas remotas. Esto simplifica la administración y reduce
la sobrecarga de recursos en los servidores gestionados.


2 diferencia entre un comando ad-hoc y un playbook
Un comando ad-hoc es una instrucción rápida que ejecutas directamente en la línea de
comandos de Ansible sin necesidad de escribir un archivo de configuración. 
Es útil para tareas simples como reiniciar servicios o copiar archivos.

Un playbook es un archivo YAML que contiene una serie de tareas organizadas en una secuencia lógica. 
Permite definir configuraciones complejas, aplicar cambios de forma repetible y garantizar
idempotencia.


3 ¿Qué es la idempotencia y por qué es importante en Ansible?
La idempotencia significa que ejecutar la misma tarea varias veces producirá el mismo
resultado sin efectos secundarios inesperados. En Ansible, esto es crucial porque garantiza que
la infraestructura mantenga un estado predecible sin aplicar cambios innecesarios. Por
ejemplo, si defines que un paquete debe estar instalado, Ansible solo lo instalará si aún no está
presente, evitando reinstalaciones innecesarias.


4 ¿Cómo funcionan los handlers y cuándo deberías usarlos?
Los handlers son tareas especiales en Ansible que solo se ejecutan cuando son notificadas por
otra tarea. Se usan principalmente para acciones que deben ocurrir solo cuando hay cambios,
como reiniciar un servicio después de modificar su configuración. 


5 ¿Cómo verificas errores de sintaxis en un playbook de Ansible?
Puedes verificar errores de sintaxis usando el comando:
ansible-playbook “nombre_del_playbook.yml” –syntax-check
Esto revisa que la estructura del archivo sea válida antes de ejecutarlo, ayudando a detectar
errores como mala indentación, nombres incorrectos de módulos o sintaxis YAML incorrecta.
