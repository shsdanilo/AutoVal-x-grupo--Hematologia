/* 
NOMBRE: AdvAV - AutoVal x grupo - Trigger - Hemograma - v1.1 solo aplica a hematologia
OBJETIVO: AutoValidacion de resultados por Grupo - controla que solo se active la autovalidacion cuando todos los examenes del grupo cumplan los limites
ACCION ESPECIFICA: Configura modo de validacion en "Por Defecto" segun el cumplimiento de los limites de autovalidacion de todo el grupo y el modo de configuracion
USO: Se debe copiar este codigo y crear uno nuevo por cada grupo definido. Se implementa en "Regla experta" de los examenes que hagan parte del listado de grupo definido mas abajo en la seccion de configuracion.
Se debe usar ademas el MISPL complementario NOMBRE: AdvAV - AutoVal x grupo - NewReq - XXX" en el campo trigger del mismo examen
IDENTIFICADOR -> PP-191219-001-1
Desarrollado para -> CL16.0.3
Tabla: Request
Return: logical
Desarrollado por: Daniel Garcia 
Fecha modificacion: 20191219
Version 1.0

Fecha de modificacion: 20200304

				

Control de Cambios ->
Version 1.0: Liberacion de desarrollo
Si se encuentra que se viola esta regla, se retiene todo el grupo

*/