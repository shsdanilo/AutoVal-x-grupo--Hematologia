/* 
NOMBRE: AdvAV - AutoVal x grupo - Trigger - Hemograma - v2.0 solo aplica a hematologia
OBJETIVO: AutoValidacion de resultados por Grupo - controla que solo se active la autovalidacion cuando todos los examenes del grupo cumplan los limites
ACCION ESPECIFICA: Configura modo de validacion en "Por Defecto" segun el cumplimiento de los limites de autovalidacion de todo el grupo y el modo de configuracion. Se debe configurar la autovalidacion de tedos los examenes incluidos en el listado, de lo contrario todo sera retenido.
USO: Se debe copiar este codigo y crear uno nuevo por cada grupo definido. Se implementa en "Regla experta" de los examenes que hagan parte del listado de grupo definido mas abajo en la seccion de configuracion.
Se aplica en el campo instrumento>comunicacion>En Mensaje final de Resultado.
Se debe usar ademas el MISPL complementario NOMBRE: AdvAV - AutoVal x grupo - NewReq - XXX" en el campo trigger de cada uno de los examenes listados en la configuracion.
IDENTIFICADOR -> PP-220914-001-1
Desarrollado para -> ADM1.2
Tabla: Sample
Return: logical
Desarrollado por: Daniel Garcia 
Fecha modificacion: 20220914
Version 2.0

Fecha de modificacion: 20200304

				

Control de Cambios ->
Version 1.0 -> Liberacion de desarrollo
Version 1.1 -> Se modifica para implementar validacion de hemoglobina frente a hematocritos
				El valor del un tercio del hematocrito debe tener una diferencia menor al 10% respecto a la hemoglobina medida 
				variacion permitida > variacion real
                0.1(HCT/3)>ABS((HCT/3)-HGB)
				ejemplo> 
				Si HCT = 45
				entonces HGB =15 +- 10%
Si se encuentra que se viola esta regla, se retiene todo el grupo
Version 2.0 -> Se cambia el sitio de ejecucion del MISPL, del sitio original Trigger de cada examen, al Mensaje en final de resultado de cada instrumento.

*/