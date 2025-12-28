# Data Dictionary

Este documento describe las variables incluidas en el dataset de reclamaciones de seguros de auto, así como consideraciones relevantes sobre su uso en el análisis.

| Column | Data Type | Description | Notes |
|------|----------|-------------|------|
| months_as_customer | INT | Meses que tiene el cliente con la compañía | Puede no representar la antigüedad de la póliza actual, sino la relación total del cliente con la aseguradora. |
| age | INT | Edad del cliente | |
| policy_number | INT | Identificador único de la póliza | |
| policy_bind_date | DATE | Fecha de inicio de vigencia de la póliza | Se detectan inconsistencias con incident_date |
| policy_state | VARCHAR | Estado donde se emitió la póliza | No necesariamente coincide con el estado del siniestro |
| policy_csl | VARCHAR | Combined Single Limit (CSL) Límite único combinado de responsabilidad civil. | 100/300 → hasta 100 mil por persona, 300 mil por evento. |
| policy_deductable | DECIMAL(10,2) | Deducible a cargo del asegurado | |
| policy_annual_premium | DECIMAL(10,2) | Prima anual de la póliza | Monto que el asegurado paga al año por su seguro de auto. |
| umbrella_limit | DECIMAL(10,2) | Limite de cobertura adicional RC catastrofica | Es una cobertura extra que entra cuando se agotan los límites básicos. |
| insured_zip | VARCHAR | Código postal del asegurado | |
| insured_sex | VARCHAR | Genero del asegurado | Masculino / Femenino |
| insured_edication_level | Nivel de estudios del asegurado | |
| insured_ocupation | Ocupación del asegurado | |
| insured_hobbies| Pasatiempos del asegurado | |
| insured_relationship | Estado civil del asegurado | | 
| capital_gains | Ganancias financieras anuales declaradas por el asegurado | |
| capital_loss | Pérdidas financieras anuales declaradas por el asegurado | |
| icident_date | DATE | Fecha de ocurrencia del siniestro | Fecha de ocurrencia no es igual a fecha de reporte a la aseguradora |
| incident_type | Tipo de siniestro | Colisión, Robo, Estacionado, etc | 
| collision_type | Tipo de colisión | En caso de no aplicar se indica con el simbolo "?" | 
| incident_severity | Gravedad del siniestro | |
| authorities_contacted | Autoridad reportada | |
| incident_state | Estado donde ocurrio el siniestro | |
| incident_city | Ciudad donde ocurrio el siniestro | |
