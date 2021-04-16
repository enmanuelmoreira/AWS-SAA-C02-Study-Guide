# AWS SAA-C02 Study Guide
Esta guía de estudio lo ayudará a aprobar el examen más reciente de AWS Certified Solutions Architect - Associate. Idealmente, debería consultar esta guía mientras trabaja con el siguiente material:

  1. Stephane Maarek's <a href="https://links.datacumulus.com/aws-certified-sa-associate-coupon">Ultimate AWS Certified Solutions Architect Associate 2021 course</a> (permanent discount available through this link) or A Cloud Guru's <a href="https://acloud.guru/learn/aws-certified-solutions-architect-associate">AWS Certified Solutions Architect Associate SAA-C02 course</a>
  2. The FAQs for the most critical services, included in the recommended reading list below
  3. Tutorials Dojo's <a href="https://www.udemy.com/course/aws-certified-solutions-architect-associate-amazon-practice-exams-saa-c02/">AWS Certified Solutions Architect Associate Practice Exams </a>
  4. Andrew Brown's <a href="https://www.youtube.com/watch?v=Ia-UEYYR44s">AWS Certified Solutions Architect - Associate 2020 (PASS THE EXAM!) | Ad-Free Course
</a> 

*Nota*:
Si en algún momento se siente inseguro de su progreso y necesita más tiempo, puede posponer la fecha del examen de AWS. Asegúrese también de mantenerse al día con las discusiones en curso en <a href="https://reddit.com/r/AWSCertifications/">r/AWSCertifications</a> ya que encontrará consejos relevantes para el examen, material de estudio y consejos de otros examinandos. Antes de experimentar con AWS, es muy importante asegurarse de saber qué es <a href="https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc">gratis</a> y lo que no es. Se pueden encontrar las preguntas frecuentes relevantes sobre el nivel gratuito <a href="https://aws.amazon.com/free/free-tier-faqs/">aquí</a>. Finalmente, Udemy a menudo tiene sus cursos a la venta de vez en cuando. Podría valer la pena esperar para comprar el examen de práctica Tutorial Dojo o el curso de Stephane Maarek, dependiendo de la urgencia con la que necesite el contenido.



## Tabla de Contenidos
1. <a href="#introduction">Introduction</a>

2. <a href="#identity-access-management-iam">Identity Access Management (IAM)</a>

3. <a href="#simple-storage-service-s3">Simple Storage Service (S3)</a>

4. <a href="#cloudfront">CloudFront</a>

5. <a href="#snowball">Snowball</a>

6. <a href="#storage-gateway">Storage Gateway</a>

7. <a href="#elastic-compute-cloud-ec2">Elastic Compute Cloud (EC2)</a>

8. <a href="#elastic-block-store-ebs">Elastic Block Store (EBS)</a>

9. <a href="#elastic-network-interfaces-eni">Elastic Network Interfaces (ENI)</a>

10. <a href="#security-groups">Security Groups</a>

11. <a href="#web-application-firewall-waf">Web Application Firewall (WAF)</a>

12. <a href="#cloudwatch">CloudWatch</a>

13. <a href="#cloudtrail">CloudTrail</a>

14. <a href="#elastic-file-system-efs">Elastic File System (EFS)</a>

15. <a href="#amazon-fsx-for-windows">Amazon FSx for Windows</a>

16. <a href="#amazon-fsx-for-lustre">Amazon FSx for Lustre</a>

17. <a href="#relational-database-service-rds">Relational Database Service (RDS)</a>

18. <a href="#aurora">Aurora</a>

19. <a href="#dynamodb">DynamoDB</a>

20. <a href="#redshift">Redshift</a>

21. <a href="#elasticache">ElastiCache</a>

22. <a href="#route53">Route53</a>

23. <a href="#elastic-load-balancers-elb">Elastic Load Balancers (ELB)</a>

24. <a href="#auto-scaling">Auto Scaling</a>

25. <a href="#virtual-private-cloud-vpc"> Virtual Private Cloud (VPC)</a>

26. <a href="#simple-queuing-service-sqs"> Simple Queuing Service (SQS)</a>

27. <a href="#simple-workflow-service-swf"> Simple Workflow Service (SWF)</a>

28. <a href="#simple-notification-service-sns"> Simple Notification Service (SNS)</a>

29. <a href="#kinesis"> Kinesis </a>

30. <a href="#lambda"> Lambda </a>

31. <a href="#api-gateway"> API Gateway </a>

32. <a href="#cloudformation">CloudFormation </a>

33. <a href="#cloudformation">ElasticBeanstalk</a>

34. <a href="#aws-organizations">AWS Organizations</a>

35. <a href="#miscellaneous">Miscellaneous</a>

## Introducción

<a href="https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate-Exam-Guide_v1.1_2019_08_27_FINAL.pdf">**Guía oficial del examen AWS Solutions Architect - Associate (SAA-C02)**</a>

### Contenido del Examen:
![Screen Shot 2020-06-05 at 2 49 08 PM](https://user-images.githubusercontent.com/13093517/83912374-c2b87900-a73b-11ea-9691-b38383b43ff9.png)

*Domain 1: Design Resilient Architectures*

  1.1 - Design a multi-tier architecture solution

  1.2 - Design highly available and/or fault-tolerant architectures

  1.3 - Design decoupling mechanisms using AWS services

  1.4 - Choose appropriate resilient storage


*Domain 2: Design High-Performing Architectures*

  2.1 - Identify elastic and scalable **compute** solutions for a workload

  2.2 - Select high-performing and scalable **storage** solutions for a workload

  2.3 - Select high-performing **networking** solutions for a workload

  2.4 - Choose high-performing **database** solutions for a workload


*Domain 3: Design Secure Applications and Architectures*

  3.1 - Design secure access to AWS resources

  3.2 - Design secure application tiers

  3.3 - Select appropriate data security options


*Domain 4: Design Cost-Optimized Architectures*

  4.1 - Identify cost-effective **storage** solutions

  4.2 - Identify cost-effective **compute** and **database** services

  4.3 - Design cost-optimized **network** architectures



### Lectura Recomendada:

Puede cubrir mucho terreno si echa un vistazo a lo que ya sabe o lo que puede inferir que es verdad. En particular, lea la primera oración de cada párrafo y si no tiene dudas sobre lo que se dice en esa oración, pase a la primera oración del párrafo siguiente. Tome notas siempre que sea necesario.

  1. <a href="https://docs.aws.amazon.com/wellarchitected/latest/framework/wellarchitected-framework.pdf">AWS Well-Architected Framework</a>

  2. <a href="https://aws.amazon.com/vpc/faqs/">Amazon VPC FAQs</a>

  3. <a href="https://aws.amazon.com/autoscaling/faqs/"> AWS Autoscaling FAQs</a>

  4. <a href="https://aws.amazon.com/ec2/faqs/">Amazon EC2 FAQs</a>

  5. <a href="https://aws.amazon.com/ec2/autoscaling/faqs/"> Amazon EC2 Auto Scaling FAQs </a>

  6. <a href="https://aws.amazon.com/ebs/faqs/">Amazon EBS FAQs</a>

  7. <a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html"> Elastic network interfaces</a>

  8. <a href="https://aws.amazon.com/s3/faqs/">Amazon S3 FAQs</a> 
  
  9. <a href="https://aws.amazon.com/elasticloadbalancing/faqs/"> Elastic Load Balancing FAQs</a>

  10. <a href="https://aws.amazon.com/route53/faqs/"> Amazon Route 53 FAQs</a>

  11. <a href="https://aws.amazon.com/storagegateway/faqs/"> AWS Storage Gateway FAQs</a>

  12. <a href="https://aws.amazon.com/efs/faq/"> Amazon EFS FAQs</a>

  13. <a href="https://aws.amazon.com/fsx/windows/faqs/">Amazon FSx for Windows File Server FAQs</a>

  14. <a href="https://aws.amazon.com/fsx/lustre/faqs/">Amazon FSx for Lustre FAQs</a>
  
  15. <a href="https://aws.amazon.com/organizations/faqs/">AWS Organizations FAQs</a>

## Identity Access Management (IAM)

### Simplificando IAM:

IAM ofrece un centro de control centralizado dentro de AWS y se integra con todos los demás servicios de AWS. IAM viene con la capacidad de compartir el acceso en varios niveles de permiso y admite la capacidad de usar la federación de identidad (el proceso de delegar la autenticación a una parte externa confiable como Facebook o Google) para acceso temporal o limitado. IAM incluye compatibilidad con MFA y le permite configurar una política de rotación de contraseñas personalizada en toda su organización.
También cumple con PCI DSS, es decir, el estándar de seguridad de datos de la industria de tarjetas de pago. (pasa las regulaciones de seguridad de tarjetas de crédito exigidas por el gobierno).

### Entidades de IAM:

**Usuarios** - cualquier usuario final individual, como un empleado, arquitecto de sistemas, CTO, etc.

**Grupos** - cualquier colección de personas similares con permisos compartidos, como administradores de sistemas, empleados de recursos humanos, equipos de finanzas, etc. Cada usuario dentro de su grupo específico heredará los permisos establecidos para el grupo.

**Roles** - cualquier servicio de software que necesite permisos para hacer su trabajo, por ejemplo, AWS Lambda que necesita permisos de escritura en S3 o un grupo de instancias EC2 que necesitan permisos de lectura de una base de datos RDS MySQL.

**Políticas** - conjuntos de reglas documentadas que se aplican para otorgar o limitar el acceso. Para que los usuarios, grupos o roles establezcan correctamente los permisos, utilizan políticas. Las políticas están escritas en JSON y puede usar políticas personalizadas para sus necesidades específicas o usar las políticas predeterminadas establecidas por AWS.

![Screen Shot 2020-06-06 at 10 49 48 PM](https://user-images.githubusercontent.com/13093517/83959193-11533980-a848-11ea-9d03-d8133e0aaa86.png)

Las políticas de IAM están separadas de las demás entidades anteriores porque no son una identidad de IAM. En cambio, se adjuntan a las identidades de IAM para que la identidad de IAM en cuestión pueda realizar su función necesaria.

### Detalles Clave de IAM:

- IAM es un servicio de AWS global que no está limitado por regiones. Cualquier usuario, grupo, rol o política es accesible globalmente.

- La cuenta raíz con acceso de administrador completo es la cuenta que se utiliza para registrarse en AWS. Por lo tanto, la dirección de correo electrónico utilizada para crear la cuenta de AWS para su uso probablemente debería ser la dirección de correo electrónico oficial de la empresa.

- Los nuevos usuarios no tienen permisos cuando se crean sus cuentas por primera vez. Esta es una forma segura de delegar el acceso, ya que los permisos deben otorgarse intencionalmente.

- Al unirse al ecosistema de AWS por primera vez, los nuevos usuarios reciben un ID de clave de acceso y un ID de clave de acceso secreta cuando les otorga acceso programático. Estos se crean solo una vez específicamente para que el nuevo usuario se una, por lo que si se pierden, simplemente genere una nueva ID de clave de acceso y una nueva ID de clave de acceso secreta. Las claves de acceso solo se utilizan para la AWS CLI y el SDK, por lo que no puede utilizarlas para acceder a la consola.

- Al crear su cuenta de AWS, es posible que tenga un proveedor de identidad existente dentro de su empresa que ofrezca inicio de sesión único (SSO). Si este es el caso, es útil, eficiente y completamente posible reutilizar sus identidades existentes en AWS. Para ello, permite que uno de los directorios activos asuma una función de IAM. Esto se debe a que la función Federación de ID de IAM permite que un servicio externo tenga la capacidad de asumir un rol de IAM.

- Los roles de IAM se pueden asignar a un servicio, como una instancia EC2, antes de su primer uso / creación o después de su uso / creación. Puede cambiar los permisos tantas veces como necesite. Todo esto se puede hacer utilizando la consola de AWS y las herramientas de línea de comandos de AWS.

- No puede anidar grupos de IAM. Los usuarios individuales de IAM pueden pertenecer a varios grupos, pero no es posible crear subgrupos para que un grupo de IAM esté incrustado dentro de otro grupo de IAM.

- Con las políticas de IAM, puede agregar fácilmente etiquetas que ayuden a definir qué recursos son accesibles por quién. Luego, estas etiquetas se utilizan para controlar el acceso a través de una política de IAM en particular. Por ejemplo, las instancias EC2 de producción y desarrollo pueden etiquetarse como tales. Esto garantizaría que las personas que solo deberían poder acceder a las instancias de desarrollo no puedan acceder a las instancias de producción.  

### Priority Levels in IAM:
- **Explicit Deny**: Denies access to a particular resource and this ruling cannot be overruled.

- **Explicit Allow**: Allows access to a particular resource so long as there is not an associated Explicit Deny.

- **Default Deny (or Implicit Deny)**: IAM identities start off with no resource access. Access instead must be granted.


## Simple Storage Service (S3)

### Simplificando S3:
S3 proporciona a los desarrolladores y equipos de TI un almacenamiento de objetos seguro, duradero y altamente escalable. El almacenamiento de objetos, a diferencia del almacenamiento en bloque, es un término general que se refiere a los datos compuestos por tres cosas:

  1.) los datos que desea almacenar

  2.) una cantidad ampliable de metadatos

  3.) un identificador único para que se puedan recuperar los datos

Esto lo convierte en un candidato perfecto para alojar archivos o directorios y un mal candidato para alojar bases de datos o sistemas operativos. La siguiente tabla destaca las diferencias clave entre el almacenamiento de objetos y bloques:

![Screen Shot 2020-06-05 at 3 34 57 PM](https://user-images.githubusercontent.com/13093517/83915925-352c5780-a742-11ea-975b-53d4e5d07e7c.png)


Los datos cargados en S3 se distribuyen en varios archivos e instalaciones. Los archivos cargados en S3 tienen un límite superior de 5 TB por archivo y la cantidad de archivos que se pueden cargar es prácticamente ilimitada. Los depósitos de S3, que contienen todos los archivos, se nombran en un espacio de nombres universal, por lo que se requiere unicidad. Todas las cargas exitosas devolverán una respuesta HTTP 200.

### Detalles Clave de S3:
- Los Objetos (archivos o directorios normales) se almacenan en S3 con una clave, valor, ID de versión y metadatos. También pueden contener torrents y sub-recursos para listas de control de acceso que son básicamente permisos para el objeto en sí.
- El modelo de coherencia de datos para S3 garantiza el acceso de lectura inmediato para nuevos objetos después de las solicitudes PUT iniciales. Estos nuevos objetos se introducen en AWS por primera vez y, por lo tanto, no es necesario actualizarlos en ningún lugar, por lo que están disponibles de inmediato.
- El modelo de consistencia de datos para S3 asegura la consistencia de lectura eventual para PUTS y DELETES de objetos ya existentes. Esto se debe a que el cambio tarda un poco en propagarse por toda la red de Amazon.
- Debido al eventual modelo de coherencia al actualizar los objetos existentes en S3, es posible que esas actualizaciones no se reflejen de inmediato. A medida que se realizan actualizaciones de objetos en la misma clave, es posible que se proporcione al usuario una versión anterior del objeto cuando se realice la siguiente solicitud de lectura.
- Amazon garantiza una durabilidad del 99,999999999% (o 11 9 s) para todas las clases de almacenamiento S3, excepto su clase de almacenamiento de redundancia reducida.
- S3 tiene las siguientes características:

  1.) variabilidad de precios y almacenamiento por niveles

  2.) gestión del ciclo de vida para caducar contenido antiguo

  3.) control de versiones para control de versiones

  4.) cifrado para la privacidad

  5.) eliminado por MFA para evitar la eliminación accidental o maliciosa de contenido

  6.) listas de control de acceso y políticas de depósito para proteger los datos

- S3 se factura por:

  1.) tamaño de almacenamiento

  2.) número de solicitudes

  3.) precios de gestión de almacenamiento (conocidos como niveles)

  4.) precios de transferencia de datos (objetos que salen o ingresan a AWS a través de Internet)

  5.) Aceleración de transferencia (aumento de velocidad opcional para objetos en movimiento a través de Cloudfront)

  6.) replicación entre regiones (más HA de la que se ofrece de forma predeterminada)

- Las políticas de bucket protegen los datos a nivel de bucket, mientras que el control de acceso enumera los datos seguros a nivel de objeto más granular.
- De forma predeterminada, todos los buckets recién creados son privados.
- S3 se puede configurar para crear registros de acceso que se pueden enviar a otro bucket en la cuenta actual o incluso a una cuenta separada todos juntos. Esto hace que sea fácil monitorear quién accede a qué dentro de S3.
- Hay tres formas diferentes de compartir buckets de S3 entre cuentas de AWS:

  1.) Solo para acceso programático, use IAM y políticas de depósito para compartir buckets completos.

  2.) Solo para acceso mediante programación, utilice ACL y políticas de bucket para compartir objetos.

  3.) Para acceder a través de la consola y la terminal, utilice roles de IAM de cuentas cruzadas

- S3 es un gran candidato para el alojamiento de sitios web estáticos. Cuando habilita el alojamiento de sitios web estáticos para S3, necesita un archivo index.html y un archivo error.html. El alojamiento de sitios web estáticos crea un punto final del sitio web al que se puede acceder a través de Internet.
- Cuando se cargan nuevos archivos y tiene habilitado el control de versiones, no se heredarán las propiedades de la versión anterior.

### Clases de Almacenamiento S3:
**S3 Standard** - Disponibilidad del 99,99% y durabilidad de 11 9 s. Los datos de esta clase se almacenan de forma redundante en varios dispositivos en varias instalaciones y están diseñados para resistir el fallo de 2 centros de datos simultáneos.

**S3 Infrequently Accessed (IA)** - Para los datos que se necesitan con menos frecuencia, pero cuando se necesitan, los datos deben estar disponibles rápidamente. La tarifa de almacenamiento es más barata, pero se le cobra por la recuperación.

**S3 One Zone Infrequently Accessed (una mejora del RRS antiguo / almacenamiento de redundancia reducida)** -  Para cuando desee los menores costos de IA, pero no requiera alta disponibilidad. Esto es incluso más económico debido a la falta de HA.

**S3 Intelligent Tiering** - Utiliza ML / AI incorporados para determinar la clase de almacenamiento más rentable y luego mueve automáticamente sus datos al nivel apropiado. Lo hace sin gastos generales operativos ni impacto en el rendimiento.

**S3 Glacier** - clase de almacenamiento de bajo costo para el archivo de datos. Esta clase es para fines de almacenamiento puro donde la recuperación no se necesita a menudo en absoluto. Los tiempos de recuperación varían de minutos a horas. Existen diferentes métodos de recuperación según cuán aceptables sean los tiempos de recuperación predeterminados para usted:

    Expedito: de 1 a 5 minutos, pero esta opción es la más cara.
    Estándar: 3-5 horas para restaurar.
    A granel: 5 - 12 horas. Esta opción tiene el costo más bajo y es buena para un gran conjunto de datos.

La duración expedita indicada anteriormente podría ser más prolongada durante situaciones excepcionales de demanda inusualmente alta en todo AWS. Si es absolutamente crítico tener acceso rápido a sus datos de Glacier bajo cualquier circunstancia, debe comprar * Capacidad Aprovisionada *. La capacidad aprovisionada garantiza que las recuperaciones aceleradas siempre funcionan dentro de las limitaciones de tiempo de 1 a 5 minutos.

**S3 Deep Glacier** - El almacenamiento S3 de menor costo donde la recuperación puede demorar 12 horas.

<img width="1246" alt="storage_types" src="https://user-images.githubusercontent.com/13093517/83919060-e1247180-a747-11ea-9336-e92ee163ac7a.png">

### Encriptación en S3:
Los datos de S3 se pueden cifrar tanto en tránsito como en reposo.

**Encryption In Transit**:Cuando el tráfico que pasa de un extremo a otro es indescifrable. Cualquiera que escuche a escondidas entre el servidor A y el servidor B no podrá entender la información que pasa. El cifrado en tránsito para S3 siempre se logra mediante SSL / TLS.

**Encryption At Rest**: Cuando los datos inmóviles que se encuentran dentro de S3 están encriptados. Si alguien irrumpe en un servidor, aún no podrá acceder a la información encriptada dentro de ese servidor. El cifrado en reposo se puede realizar en el lado del servidor o en el lado del cliente. El lado del servidor es cuando S3 cifra sus datos mientras se escriben en el disco y los descifra cuando accede a ellos. El lado del cliente es cuando usted personalmente cifra el objeto por su cuenta y luego lo carga en S3.

Puede cifrar en el lado del servidor compatible con AWS de las siguientes maneras:
- **S3 Managed Keys / SSE - S3 (server side encryption S3 )** - cuando Amazon administra las claves de cifrado y descifrado automáticamente. En este escenario, concede un poco de control a Amazon a cambio de facilidad de uso.
- **AWS Key Management Service / SSE - KMS** - 
cuando Amazon y usted administran juntos las claves de cifrado y descifrado.
- **Server Side Encryption w/ customer provided keys / SSE - C** - cuando le doy a Amazon mis propias claves que administro. En este escenario, concede facilidad de uso a cambio de un mayor control.

### Control de Versiones en S3:
- Cuando el control de versiones está habilitado, S3 almacena todas las versiones de un objeto, incluidas todas las escrituras e incluso las eliminaciones.
- Es una gran función para realizar copias de seguridad implícitas del contenido y para reversiones fáciles en caso de error humano.
- Puede considerarse análogo a Git.
- Una vez que se habilita el control de versiones en un bucket, no se puede deshabilitar, solo suspender.
- El control de versiones se integra con las reglas del ciclo de vida para que pueda establecer reglas para que caduquen o migren datos según su versión.
- El control de versiones también tiene la capacidad de control por MFA para proporcionar una capa adicional de seguridad.

### Gestión del Ciclo de Vida de S3:
- Automatiza el movimiento de objetos entre los diferentes niveles de almacenamiento.
- Se puede utilizar junto con el control de versiones.
- Las reglas del ciclo de vida se pueden aplicar a las versiones actuales y anteriores de un objeto.

### Replicación entre Regiones en S3:
- La replicación entre regiones solo funciona si el control de versiones está habilitado.
- Cuando la replicación entre regiones está habilitada, no se transfieren datos preexistentes. Solo se replican las cargas nuevas en el depósito original. Todas las actualizaciones posteriores se replican.
- Cuando replica el contenido de un depósito a otro, puede cambiar la propiedad del contenido si lo desea. También puede cambiar el nivel de almacenamiento del nuevo depósito con el contenido replicado.
- Cuando los archivos se eliminan en el depósito original (mediante un marcador de eliminación, ya que el control de versiones evita eliminaciones verdaderas), esas eliminaciones no se replican.
- <a href="https://aws.amazon.com/solutions/cross-region-replication-monitor/">Descripción general de la replicación entre regiones</a>
- <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-what-is-isnot-replicated.html#replication-what-is-not-replicated ">Qué se replica y qué no, como objetos encriptados, eliminaciones, elementos en el glaciar, etc.</a>

### S3 Transfer Acceleration:
- La aceleración de transferencia hace uso de la red CloudFront al enviar o recibir datos en puntos de presencia CDN (llamados ubicaciones de borde) en lugar de cargas o descargas más lentas en el origen.
- Esto se logra subiendo a una URL distinta para la ubicación de borde en lugar del depósito en sí. Esto luego se transfiere a través de la red troncal de AWS a una velocidad mucho más rápida.
- <a href="https://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html">Puede probar la velocidad de aceleración de la transferencia directamente en comparación con las cargas regulares.</a>

### S3 Event Notications:
La función de notificación de Amazon S3 le permite recibir y enviar notificaciones cuando ocurren ciertos eventos en su depósito. Para habilitar las notificaciones, primero debe configurar los eventos que desea que Amazon S3 publique (objeto nuevo agregado, objeto antiguo eliminado, etc.) y los destinos a los que desea que Amazon S3 envíe las notificaciones de eventos. Amazon S3 admite los siguientes destinos donde puede publicar eventos:
- **Amazon Simple Notification Service (Amazon SNS)** - Un servicio web que coordina y gestiona la entrega o envío de mensajes a endpoints o clientes suscritos.
- **Amazon Simple Queue Service (Amazon SQS)** - SQS ofrece colas alojadas confiables y escalables para almacenar mensajes mientras viajan entre computadoras.
- **AWS Lambda** - AWS Lambda es un servicio informático en el que puede cargar su código y el servicio puede ejecutar el código en su nombre mediante la infraestructura de AWS. Empaqueta y carga su código personalizado en AWS Lambda cuando crea una función Lambda. El evento S3 que activa la función Lambda también puede servir como entrada del código.

###  S3 y ElasticSearch:
- Si usa S3 para almacenar archivos de registro, ElasticSearch proporciona capacidades de búsqueda completas para registros y puede usarse para buscar en los datos almacenados en un depósito de S3.
- Puede integrar su dominio ElasticSearch con S3 y Lambda. En esta configuración, cualquier registro nuevo recibido por S3 activará una notificación de evento a Lambda, que a su vez ejecutará el código de su aplicación en los nuevos datos de registro. Una vez que su código termine de procesarse, los datos se transmitirán a su dominio ElasticSearch y estarán disponibles para su observación.

### Maximizing S3 Read/Write Performance:
- Si la tasa de solicitud de lectura y escritura de objetos en S3 es extremadamente alta, puede usar nombres secuenciales basados ​​en fechas para sus prefijos para mejorar el rendimiento. Las versiones anteriores de AWS Docs también sugerían usar claves hash o cadenas aleatorias para prefijar el nombre del objeto. En tales casos, las particiones utilizadas para almacenar los objetos estarán mejor distribuidas y, por lo tanto, permitirán un mejor rendimiento de lectura / escritura en sus objetos.
- Si sus datos de S3 reciben una gran cantidad de solicitudes GET de los usuarios, debe considerar el uso de Amazon CloudFront para optimizar el rendimiento. Al integrar CloudFront con S3, puede distribuir contenido a través de la caché de CloudFront a sus usuarios para obtener una latencia más baja y una tasa de transferencia de datos más alta. Esto también tiene la ventaja adicional de enviar menos solicitudes directas a S3, lo que reducirá los costos. Por ejemplo, suponga que tiene algunos objetos que son muy populares. CloudFront recupera esos objetos de S3 y los almacena en caché. Luego, CloudFront puede atender solicitudes futuras de objetos desde su caché, reduciendo la cantidad total de solicitudes GET que envía a Amazon S3.
- <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/request-rate-perf-considerations.html "> Más información sobre cómo garantizar un alto rendimiento en S3</a>

### S3 Server Access Logging:
- El registro de acceso al servidor proporciona registros detallados de las solicitudes que se realizan a un bucket. Los registros de acceso al servidor son útiles para muchas aplicaciones. Por ejemplo, la información del registro de acceso puede ser útil en auditorías de seguridad y acceso. También puede ayudarlo a conocer su base de clientes y comprender mejor su factura de Amazon S3.
- De forma predeterminada, el registro está deshabilitado. Cuando el registro está habilitado, los registros se guardan en un depósito en la misma región de AWS que el depósito de origen.
- Cada registro de registro de acceso proporciona detalles sobre una única solicitud de acceso, como el solicitante, el nombre del depósito, la hora de la solicitud, la acción de la solicitud, el estado de la respuesta y un código de error, si es relevante.
- Funciona de la siguiente forma:
   - S3 recopila periódicamente registros de acceso del depósito que desea supervisar
   - S3 luego consolida esos registros en archivos de registro
   - S3 finalmente carga los archivos de registro en su depósito de monitoreo secundario como objetos de registro

### S3 Multipart Upload:
- La carga de varias partes le permite cargar un solo objeto como un conjunto de partes. Cada parte es una parte contigua de los datos del objeto. Puede cargar estas partes del objeto de forma independiente y en cualquier orden.
- Se recomiendan cargas de varias partes para archivos de más de 100 MB y es * la única forma * de cargar archivos de más de 5 GB. Logra la funcionalidad cargando sus datos en paralelo para aumentar la eficiencia.
- Si falla la transmisión de cualquier parte, puede retransmitir esa parte sin afectar a otras partes. Una vez que se cargan todas las partes de su objeto, Amazon S3 ensambla estas partes y crea el objeto.
- Posibles razones por las que querría utilizar la carga multiparte:
  - La carga de varias partes ofrece la posibilidad de comenzar una carga antes de conocer el tamaño final del objeto.
  - La carga de varias partes ofrece un rendimiento mejorado.
  - La carga de varias partes ofrece la capacidad de pausar y reanudar la carga de objetos.
  - La carga de varias partes ofrece una recuperación rápida de problemas de red.
- Puede utilizar un SDK de AWS para cargar un objeto en partes. Alternativamente, puede realizar la misma acción a través de la AWS CLI.
- También puede paralelizar descargas desde S3 usando ** recuperaciones de rango de bytes **. Si hay una falla durante la descarga, la falla se localiza solo en el rango de bytes específico y no en todo el objeto.

### S3 Pre-signed URLs:
- Todos los objetos de S3 son privados de forma predeterminada; sin embargo, el propietario del objeto de un depósito privado con objetos privados puede compartir opcionalmente esos objetos sin tener que cambiar los permisos del depósito para que sea público.
- Esto se hace creando una URL firmada previamente. Con sus propias credenciales de seguridad, puede otorgar permiso por tiempo limitado para descargar o ver sus objetos privados de S3.
- Cuando crea una URL firmada previamente para su objeto S3, debe hacer lo siguiente:
  - Proporcionar sus credenciales de seguridad.
  - Especifiquar un bucket.
  - Especifiquar una clave de objeto.
  - Especifiquar el método HTTP (GET para descargar el objeto).
  - Especifiquar la fecha y hora de vencimiento.
  
- Las URL pre-firmadas son válidas solo por la duración especificada y cualquiera que reciba la URL pre-firmada dentro de esa duración puede acceder al objeto.
- El siguiente diagrama destaca cómo funcionan las URL firmadas previamente:

![Screen Shot 2020-06-09 at 8 20 53 PM](https://user-images.githubusercontent.com/13093517/84213482-c6773300-aa8e-11ea-84a1-3c17e14197bc.png)

### S3 Select:
- S3 Select es una función de Amazon S3 que está diseñada para extraer solo los datos que necesita de un objeto, lo que puede mejorar drásticamente el rendimiento y reducir el costo de las aplicaciones que necesitan acceder a los datos en S3.
- La mayoría de las aplicaciones tienen que recuperar todo el objeto y luego filtrar solo los datos necesarios para un análisis más detallado. S3 Select permite que las aplicaciones descarguen el trabajo pesado de filtrar y acceder a datos dentro de objetos al servicio Amazon S3.
- Por ejemplo, imaginemos que es un desarrollador en un gran minorista y necesita analizar los datos de ventas semanales de una sola tienda, pero los datos de las 200 tiendas se guardan en un nuevo CSV editado con GZIP todos los días.
  - Sin S3 Select, necesitaría descargar, descomprimir y procesar todo el CSV para obtener los datos que necesita.
  - Con S3 Select, puede usar una expresión SQL simple para devolver solo los datos de la tienda que le interesa, en lugar de recuperar el objeto completo.
- Al reducir el volumen de datos que deben cargar y procesar sus aplicaciones, S3 Select puede mejorar el rendimiento de la mayoría de las aplicaciones que acceden con frecuencia a los datos de S3 hasta en un 400% porque se trata de una cantidad significativamente menor de datos.
- También puede utilizar S3 Select para Glacier.


## CloudFront

### Simplificando CloudFront:
El servicio AWS CDN se llama CloudFront. Ofrece contenido y activos almacenados en caché para aumentar el rendimiento global de su aplicación. Los componentes principales de CloudFront son las ubicaciones de borde (puntos finales de caché), el origen (fuente de verdad original que se almacenará en caché, como una instancia EC2, un bucket de S3, un Elastic Load Balancer o una configuración de Route 53) y la distribución (el disposición de ubicaciones de borde desde el origen o básicamente la propia red). <a href="https://aws.amazon.com/cloudfront/features/">Más información sobre las funciones de CloudFront</a>

### Detalles Clave de CloudFront:
- Cuando el contenido se almacena en caché, se hace durante un cierto límite de tiempo llamado Time To Live, o TTL, que siempre se expresa en segundos.
- Si es necesario, CloudFront puede ofrecer sitios web completos, incluido contenido dinámico, estático, de transmisión e interactivo.
- Las solicitudes siempre se enrutan y almacenan en caché en la ubicación de borde más cercana para el usuario, propagando así los nodos CDN y garantizando el mejor rendimiento para solicitudes futuras.
- Hay dos tipos diferentes de distribuciones:
  - ** Distribución web **: sitios web, elementos en caché normales, etc.
  - ** RTMP **: contenido de transmisión, adobe, etc.
- Las ubicaciones de borde no son solo de lectura. Se pueden escribir en los que luego devolverán el valor de escritura al origen.
- El contenido en caché se puede invalidar o borrar manualmente más allá del TTL, pero esto conlleva un costo.
- Puede invalidar la distribución de ciertos objetos o directorios completos para que el contenido se cargue directamente desde el origen cada vez. La invalidación del contenido también es útil al depurar si el contenido extraído del origen parece correcto, pero extraer ese mismo contenido desde una ubicación de borde parece incorrecto.
- Puede configurar una conmutación por error para el origen creando un grupo de origen con dos orígenes en su interior. Un origen actuará como primario y el otro como secundario. CloudFront cambiará automáticamente entre los dos cuando falle el origen principal.
- Amazon CloudFront entrega su contenido desde cada ubicación de borde y ofrece una función SSL personalizada de IP dedicada. SNI Custom SSL funciona con la mayoría de los navegadores modernos.
- Si ejecuta cargas de trabajo compatibles con PCI o HIPAA y necesita registrar datos de uso, puede hacer lo siguiente:
    - Habilitar los registros de acceso de CloudFront.
    - Capturar las solicitudes que se envían a la API de CloudFront.
- Se utiliza una identidad de acceso de origen (OAI) para compartir contenido privado a través de CloudFront. La OAI es un usuario virtual que se utilizará para otorgarle a su distribución de CloudFront permiso para obtener un objeto privado de su origen (por ejemplo, el bucket S3).

### URLs y Cookies Firmadas CloudFront:
- Las URL firmadas de CloudFront y las cookies firmadas brindan la misma funcionalidad básica: le permiten controlar quién puede acceder a su contenido. Estas funciones existen porque muchas empresas que distribuyen contenido a través de Internet desean restringir el acceso a documentos, datos comerciales, transmisiones de medios o contenido destinado a usuarios seleccionados. Por ejemplo, los usuarios que han pagado una tarifa deberían poder acceder a contenido privado que los usuarios del nivel gratuito no deberían.
- Si desea ofrecer contenido privado a través de CloudFront y está tratando de decidir si usar URL firmadas o cookies firmadas, considere lo siguiente:
  - Utilice URL firmadas para los siguientes casos:
    - Quiere utilizar una distribución RTMP. Las cookies firmadas no son compatibles con las distribuciones RTMP.
    - Quiere restringir el acceso a archivos individuales, por ejemplo, una descarga de instalación para su aplicación.
    - Sus usuarios están usando un cliente (por ejemplo, un cliente HTTP personalizado) que no admite cookies.
  - Utilice cookies firmadas para los siguientes casos:
    - Quiere proporcionar acceso a varios archivos restringidos. Por ejemplo, todos los archivos de un video en formato HLS o todos los archivos en el área de usuarios pagos de un sitio web.
    - No desea cambiar sus URL actuales.

## Snowball

### Simplificando Snowball:
Snowball es un disco físico gigante que se utiliza para migrar grandes cantidades de datos a AWS. Es una solución de transporte de datos a escala de petabytes. El uso de un disco grande como Snowball ayuda a eludir los problemas comunes de transferencia de datos a gran escala, como los altos costos de red, los largos tiempos de transferencia y los problemas de seguridad. Las bolas de nieve son extremadamente seguras por diseño y una vez que se completa la transferencia de datos, las bolas de nieve se borran de sus datos.

### Detalles Clave de Snowball:
- Snowball es una buena opción para un trabajo de transferencia de datos si necesita una transferencia de datos segura y rápida que va desde terabytes a muchos petabytes en AWS.
- Snowball también puede ser la elección correcta si no desea realizar costosas actualizaciones a su infraestructura de red existente, si experimenta con frecuencia grandes acumulaciones de datos, si se encuentra en un entorno físicamente aislado o si se encuentra en un área donde las conexiones a Internet de alta velocidad no están disponibles o tienen un costo prohibitivo.
- Como regla general, si se tarda más de una semana en cargar sus datos en AWS utilizando la capacidad de reserva de su conexión a Internet existente, entonces debería considerar usar Snowball.
- Por ejemplo, si tiene una conexión de 100 Mb que puede dedicar únicamente a transferir sus datos y necesita transferir 100 TB de datos en total, la transferencia tardará más de 100 días en completarse a través de esa conexión. Puede realizar la misma transferencia en aproximadamente una semana utilizando varias bolas de nieve.
- Aquí hay una referencia sobre cuándo se debe considerar Snowball en función de la cantidad de días que llevaría realizar la misma transferencia a través de una conexión a Internet:

![Screen Shot 2020-06-07 at 10 53 22 PM](https://user-images.githubusercontent.com/13093517/83988618-c271d680-a911-11ea-9594-a82f690a786b.png)

### Snowball Edge y Snowmobile:
- Snowball Edge es un tipo específico de Snowball que viene con capacidades de cómputo * y * de almacenamiento a través de AWS Lambda y tipos de instancias EC2 específicas. Esto significa que puede ejecutar código dentro de su bola de nieve mientras sus datos están en camino a un centro de datos de Amazon. Esto permite el soporte de cargas de trabajo locales en ubicaciones remotas o fuera de línea y, como resultado, Snowball Edge no necesita estar limitado a un servicio de transferencia de datos. Un caso de uso interesante es el de los aviones de pasajeros. Los aviones a veces vuelan con bordes de bola de nieve a bordo para que puedan almacenar grandes cantidades de datos de vuelo y calcular las funciones necesarias para los propios sistemas del avión. Los bordes de bola de nieve también se pueden agrupar localmente para un rendimiento aún mejor.
- Snowmobile es una solución de transferencia de datos a escala exabyte. Es una solución de transporte de datos para 100 petabytes de datos y está contenida dentro de un contenedor de envío de 45 pies transportado por un semirremolque. Esta transferencia masiva tiene sentido si desea trasladar todo su centro de datos con años de datos a la nube.

## Storage Gateway

### Simplificando Storage Gateway:
Storage Gateway es un servicio que conecta los entornos locales con el almacenamiento basado en la nube para integrar de forma segura y sin problemas una aplicación local con un backend de almacenamiento en la nube. y Volume Gateway como una forma de almacenar unidades de disco duro virtuales en la nube.


### Detalles Clave de Storage Gateway:
- El servicio Storage Gateway puede ser un dispositivo físico o una imagen de VM descargada en un host en un centro de datos local. Actúa como un puente para enviar o recibir datos de AWS.
- Storage Gateway puede colocarse sobre el hipervisor ESXi de VMWare para máquinas Linux y el hipervisor Hyper-V de Microsoft para máquinas Windows.
- Los tres tipos de Storage Gateways son los siguientes:
  - **File Gateway** - Funciona a través de NFS o SMB y se utiliza para almacenar archivos en S3 a través de un punto de montaje del sistema de archivos de red en la máquina virtual suministrada. En pocas palabras, puede pensar en un File Gateway como un montaje de sistema de archivos en S3.
  - **Volume Gateway** - Funciona a través de iSCSI y se utiliza para almacenar copias de unidades de disco duro o unidades de disco duro virtual en S3. Estos se pueden lograr a través de * Stored Volumes * o * Cached Volumes *. En pocas palabras, puede pensar en Volume Gateway como una forma de almacenar unidades de disco duro virtuales en la nube. 
  - **Tape Gateway** - Funciona como un arreglo de cintas virtual
- La información relevante del archivo que pasa a través de Storage Gateway, como la propiedad del archivo, los permisos, las marcas de tiempo, etc., se almacena como metadatos de los objetos a los que pertenecen. Una vez que estos detalles de archivo se almacenan en S3, se pueden administrar de forma nativa. Esto significa que todas las funciones de S3, como el control de versiones, la administración del ciclo de vida, las políticas de depósito, la replicación entre regiones, etc., se pueden aplicar como parte de Storage Gateway.
- Las aplicaciones que interactúan con AWS a través de Volume Gateway se realizan a través del protocolo de bloque iSCSI. Los datos escritos en estos volúmenes se pueden respaldar de forma asíncrona en AWS Elastic Block Store (EBS) como instantáneas puntuales del contenido de los volúmenes. Este tipo de instantáneas actúan como copias de seguridad incrementales que capturan solo el estado cambiado de manera similar a una solicitud de extracción en Git. Además, todas las instantáneas se comprimen para reducir los costos de almacenamiento.
- Tape Gateway ofrece una forma duradera y rentable de archivar y replicar datos en S3 mientras se deshace de las cintas (almacenamiento de datos de la vieja escuela). Virtual Tape Library, o VTL, aprovecha la infraestructura de copia de seguridad existente basada en cintas para almacenar datos en cartuchos de cintas virtuales que usted crea en Tape Gateway. Es una excelente manera de modernizar y mover copias de seguridad a la nube.

### Stored Volumes vs. Cached Volumes:
- Los ** volúmenes almacenados ** de Volume Gateway le permiten almacenar datos localmente en las instalaciones y respaldan los datos en AWS como una fuente de datos secundaria. Los volúmenes almacenados permiten el acceso de baja latencia a conjuntos de datos completos, al tiempo que brindan alta disponibilidad en una solución de nube híbrida. Además, puede montar volúmenes almacenados en la infraestructura de la aplicación como unidades iSCSI, de modo que cuando los datos se escriben en estos volúmenes, los datos se escriben en el hardware local y se respaldan de forma asíncrona como instantáneas en AWS EBS o S3.
  - En el siguiente diagrama de una arquitectura de volumen almacenado, los datos se entregan al usuario desde la red de área de almacenamiento, el almacenamiento conectado a la red o el almacenamiento conectado directamente dentro de su centro de datos. S3 existe solo como una copia de seguridad segura y confiable.
  - ![Screen Shot 2020-06-08 at 5 10 33 PM](https://user-images.githubusercontent.com/13093517/84080932-05cc5380-a9ab-11ea-8dd5-a80717b1b067.png)

- Los ** volúmenes en caché ** de Volume Gateway se diferencian porque no almacenan el conjunto de datos completo localmente como los volúmenes almacenados. En cambio, AWS se utiliza como fuente de datos principal y el hardware local se utiliza como capa de almacenamiento en caché. Solo los componentes utilizados con más frecuencia se conservan en la infraestructura local, mientras que los datos restantes se proporcionan desde AWS. Esto minimiza la necesidad de escalar la infraestructura local y, al mismo tiempo, mantiene el acceso de baja latencia a los datos más referenciados.
  - En el siguiente diagrama de una arquitectura de volumen en caché, los datos a los que se accede con más frecuencia se entregan al usuario desde la red de área de almacenamiento, el almacenamiento conectado a la red o el almacenamiento conectado directamente dentro de su centro de datos. S3 proporciona el resto de los datos de AWS.
  - ![Screen Shot 2020-06-08 at 5 17 02 PM](https://user-images.githubusercontent.com/13093517/84081406-e5e95f80-a9ab-11ea-82d2-8bd1a53876ba.png)


## Elastic Compute Cloud (EC2)

### Simplificnado EC2:
EC2 genera instancias de servidor de tamaño variable que pueden escalar hacia arriba y hacia abajo rápidamente. Una instancia es un servidor virtual en la nube. Con Amazon EC2, puede instalar y configurar el sistema operativo y las aplicaciones que se ejecutan en su instancia. Su configuración en el lanzamiento es una copia en vivo de la * Imagen de máquina de Amazon (AMI) * que especificó cuando lanzó la instancia. EC2 tiene un marco de tiempo extremadamente reducido para aprovisionar y arrancar nuevas instancias y EC2 garantiza que pague sobre la marcha, pague por lo que use, pague menos a medida que use más y pague incluso menos cuando reserve capacidad. Cuando su instancia EC2 se está ejecutando, se le cobra en CPU, memoria, almacenamiento y redes. Cuando se detiene, solo se le cobra por el almacenamiento de EBS.

### Detalles Clave EC2:
- Puede desplegar diferentes tipos de instancias desde una única AMI. Un tipo de instancia determina esencialmente el hardware de la computadora host que se usa para su instancia. Cada tipo de instancia ofrece diferentes capacidades de procesamiento y memoria. Debe seleccionar un tipo de instancia en función de la cantidad de memoria y potencia informática que necesita para la aplicación o el software que planea ejecutar sobre la instancia.
- Puede desplegar varias instancias de una AMI, como se muestra en la siguiente figura:

![architecture_ami_instance](https://user-images.githubusercontent.com/13093517/84097031-64a4c380-a9d1-11ea-8358-1c3eec1c4471.png)

- Tiene la opción de utilizar la tenencia dedicada con su instancia. Esto significa que dentro de un centro de datos de AWS, tiene acceso exclusivo al hardware físico. Naturalmente, esta opción tiene un costo elevado, pero tiene sentido si trabaja con tecnología que tiene una política de licencias estricta.
- Con EC2 VM Import, puede importar máquinas virtuales existentes a AWS siempre que esos hosts utilicen los formatos de virtualización VMware ESX, VMware Workstation, Microsoft Hyper-V o Citrix Xen.
- Cuando lanza una nueva instancia EC2, EC2 intenta colocar la instancia de tal manera que todas sus máquinas virtuales se distribuyen en diferentes hardware para limitar las fallas a una sola ubicación. Puede utilizar grupos de ubicación para influir en la ubicación de un grupo de instancias interdependientes que satisfagan las necesidades de su carga de trabajo. Hay una explicación sobre los grupos de ubicación en una sección a continuación.
- Cuando lanza una instancia en Amazon EC2, tiene la opción de pasar datos de usuario a la instancia cuando se inicia. Estos datos de usuario se pueden utilizar para ejecutar tareas o scripts de configuración automatizada comunes. Por ejemplo, puede pasar un script bash que garantice que htop esté instalado en el nuevo host EC2 y esté siempre activo.
- De forma predeterminada, la dirección IP pública de una instancia EC2 se libera cuando la instancia se detiene, incluso si se detiene temporalmente. Por lo tanto, es mejor hacer referencia a una instancia por su nombre de host DNS externo. Si necesita una dirección IP pública persistente que pueda asociarse a la misma instancia, utilice una dirección IP elástica que sea básicamente una dirección IP estática.
- Si tiene requisitos para autogestionar una base de datos SQL, EC2 puede ser una alternativa sólida a RDS. Para garantizar una alta disponibilidad, recuerde tener al menos otra instancia EC2 en una zona de disponibilidad separada, de modo que incluso si una instancia de base de datos deja de funcionar, las otras seguirán estando disponibles.
- Una imagen dorada es simplemente una AMI que ha personalizado completamente a su gusto con todos los detalles de software / datos / configuración necesarios establecidos y listos para usar una vez. Esta AMI personal puede ser la fuente desde la que lanza nuevas instancias.
- Las verificaciones del estado de la instancia verifican el estado del servidor EC2 en ejecución, la verificación del estado de los sistemas monitorea el estado del hipervisor subyacente. Si alguna vez nota un problema de estado del sistema, simplemente detenga la instancia e iníciela nuevamente (no es necesario reiniciar), ya que la VM se iniciará nuevamente en un nuevo hipervisor.

### EC2 Instance Pricing:
- ** Instancias Bajo Demanda ** se basan en una tarifa fija por hora o segundo. Como su nombre lo indica, puede iniciar una instancia On-Demand siempre que la necesite y detenerla cuando ya no la necesite. No hay ningún requisito para un compromiso a largo plazo.
- ** Instancias Reservadas ** garantizan que mantengas el uso exclusivo de una instancia en términos de contrato de 1 o 3 años. El compromiso a largo plazo proporciona descuentos significativamente reducidos a la tarifa por hora.
- ** Instancias Puntuales ** aprovechan el exceso de capacidad de Amazon y funcionan de manera interesante. Para poder utilizarlos, debe pujar económicamente por el acceso. Debido a que las instancias de spot solo están disponibles cuando Amazon tiene un exceso de capacidad, esta opción solo tiene sentido si su aplicación tiene horarios de inicio y finalización flexibles. No se le cobrará si su instancia se detiene debido a un cambio de precio (p. Ej., Otra persona acaba de ofertar un precio más alto por el acceso) y, por lo tanto, su carga de trabajo no se completa. Sin embargo, si cancela la instancia usted mismo, se le cobrará la hora en que se ejecutó la instancia. Las instancias de spot se utilizan normalmente en trabajos de procesamiento por lotes.

### Standard Reserved vs. Convertible Reserved vs. Scheduled Reserved:
- **Standard Reserved Instances** tienen reservas inflexibles que tienen un descuento del 75% en las instancias On-Demand. Las instancias reservadas estándar no se pueden mover entre regiones. Puede elegir si una instancia reservada se aplica a una zona de disponibilidad específica oa una región completa, pero no puede cambiar la región.
- **Convertible Reserved Instances** son instancias que tienen un descuento del 54% de las instancias bajo demanda, pero también puede modificar el tipo de instancia en cualquier momento. Por ejemplo, sospecha que después de unos meses su VM podría necesitar cambiar de uso general a memoria optimizada, pero aún no está seguro. Por lo tanto, si cree que en el futuro podría necesitar cambiar el tipo de VM o actualizar la capacidad de sus VM, elija Instancias reservadas convertibles. Sin embargo, no hay ningún tipo de instancia de degradación con esta opción.
- **Scheduled Reserved Instances** están reservados de acuerdo con una línea de tiempo especificada que establezca. Por ejemplo, puede usar Instancias reservadas programadas si ejecuta software educativo que solo debe estar disponible durante el horario escolar. Esta opción le permite ajustar mejor su capacidad necesaria con un programa recurrente para que pueda ahorrar dinero.

### Ciclo de Vida de una Instancia EC2:
La siguiente tabla destaca los muchos estados de instancia en los que una VM puede estar en un momento dado.

| Instance state | Description | Billing |
| ------------- | ------------- |--------------|
| `pending` | La instancia se está preparando para entrar en el estado `running`. Una instancia entra en estado pendiente cuando se lanza por primera vez, o cuando se inicia después de estar en el estado `stopped`.  | No facturando
| `running`  | La instancia se está ejecutando y lista para usarse.  | Facturando |
| `stopping`  | La instancia se está preparando para detenerse o dejar de hibernar.  | No facturando si se está preparando para detenerse. Facturado si se prepara para hibernar |
| `stopped` | La instancia está apagada y no se puede utilizar. La instancia se puede iniciar en cualquier momento. | No Facturando |
| `shutting-down`  | La instancia se está preparando para ser terminada.  | No facturando |
| `terminated`  | La instancia se ha eliminado de forma permanente y no se puede iniciar.  | No Facturado |

**Nota**: Las Instancias reservadas que se rescinden se facturan hasta el final de su vigencia. 
 
### EC2 Security:
- Cuando implementa una instancia Amazon EC2, usted es responsable de la administración del sistema operativo invitado (incluidas las actualizaciones y los parches de seguridad), cualquier software de aplicación o utilidades instaladas en las instancias y la configuración del firewall provisto por AWS (llamado seguridad grupo) en cada instancia.
- Con EC2, la protección de terminación de la instancia está deshabilitada de forma predeterminada. Esto significa que no tiene una protección contra la finalización accidental de su instancia. Debe activar esta función si desea un poco de protección adicional.
- Amazon EC2 utiliza criptografía de clave pública para cifrar y descifrar la información de inicio de sesión. La criptografía de clave pública utiliza una clave pública para cifrar un dato, como una contraseña, y el destinatario utiliza su clave privada para descifrar los datos. Las claves pública y privada se conocen como par de claves.
- Puede cifrar el volumen de su dispositivo raíz, que es donde instala el sistema operativo subyacente. Puede hacer esto durante el tiempo de creación de la instancia o con herramientas de terceros como bit locker. Por supuesto, los volúmenes de EBS adicionales o secundarios también se pueden cifrar.
- De forma predeterminada, una instancia EC2 con un volumen raíz de AWS Elastic Block Store (EBS) adjunto se eliminará al mismo tiempo cuando finalice la instancia. Sin embargo, se conservará cualquier volumen de EBS adicional o secundario que también esté adjunto a la misma instancia. Esto se debe a que el volumen raíz de EBS es para instalaciones de SO y otras configuraciones de bajo nivel. Esta regla se puede modificar, pero normalmente es más fácil arrancar una nueva instancia con un nuevo volumen de dispositivo raíz que utilizar una antigua.


### EC2 Placement Groups:
- Los grupos de ubicación equilibran la compensación entre la tolerancia al riesgo y el rendimiento de la red cuando se trata de su flota de instancias EC2. Cuanto más se preocupe por el riesgo, más aisladas desea que estén sus instancias entre sí. Cuanto más se preocupe por el rendimiento, más unidas querrá que sus instancias estén entre sí.
- Hay tres tipos diferentes de grupos de ubicación EC2:

  1.) Grupos de ubicación agrupados
    - La agrupación de ubicaciones en clúster es cuando coloca todas sus instancias EC2 en una única zona de disponibilidad. Esto se recomienda para aplicaciones que necesitan la menor latencia posible y requieren el mayor rendimiento de red.
    - Solo se pueden lanzar ciertas instancias en este grupo (computación optimizada, GPU optimizada, almacenamiento optimizado y memoria optimizada).
  
  2.) Grupos de colocación de propagación
    - La agrupación de ubicación de propagación es cuando se coloca cada instancia de EC2 individual sobre su propio hardware distinto para aislar la falla.
    - Sus máquinas virtuales viven en racks independientes, con entradas de red independientes y requisitos de alimentación independientes. Se recomiendan los grupos de ubicación de propagación para aplicaciones que tienen una pequeña cantidad de instancias críticas que deben mantenerse separadas entre sí.
  
  3.) Grupos de ubicación particionados
    - La agrupación de ubicaciones particionada es similar a la agrupación de ubicaciones de propagación, pero difiere porque puede tener varias instancias EC2 dentro de una sola partición. En cambio, la falla está aislada en una partición (digamos 3 o 4 instancias en lugar de 1), sin embargo, disfruta de los beneficios de la proximidad para mejorar el rendimiento de la red.
    - Con este grupo de ubicación, tiene varias instancias que viven juntas en el mismo hardware dentro de diferentes zonas de disponibilidad en una o más regiones.
    - Si desea un equilibrio entre la tolerancia al riesgo y el rendimiento de la red, utilice Grupos de ubicación con particiones.
  
- Cada nombre de grupo de ubicación dentro de su AWS debe ser único.
- Puede mover una instancia existente a un grupo de ubicación con la garantía de que está en un estado detenido. Puede mover la instancia a través de la CLI o un SDK de AWS, pero no la consola. También puede tomar una instantánea de la instancia existente, convertirla en una AMI e iniciarla en el grupo de ubicación donde desee que esté.

## Elastic Block Store (EBS)

### Simplificando EBS:
Un volumen de Amazon EBS es un dispositivo de almacenamiento duradero a nivel de bloque que puede adjuntar a una única instancia EC2. Puede pensar en EBS como un disco duro virtual basado en la nube. Puede utilizar los volúmenes de EBS como almacenamiento principal para los datos que requieren actualizaciones frecuentes, como la unidad del sistema para una instancia o el almacenamiento para una aplicación de base de datos. También puede utilizarlos para aplicaciones de alto rendimiento que realizan exploraciones de disco continuas.

### Detalles Clave de EBS:
- Los volúmenes de EBS persisten independientemente de la vida útil de una instancia EC2.
- Cada volumen de EBS se replica automáticamente dentro de su zona de disponibilidad para proteger tanto de fallas de componentes como de recuperación ante desastres (similar a Standard S3).
- Hay cinco tipos diferentes de almacenamiento de EBS:
  - Propósito general (SSD)
  - IOPS aprovisionadas (SSD, construido para la velocidad)
  - Unidad de disco duro con rendimiento optimizado (magnético, construido para cargas de datos más grandes)
  - Unidad de disco duro fría (magnética, diseñada para cargas de trabajo a las que se accede con menos frecuencia)
  - Magnético
- EBS Volumes ofrece un SLA del 99,999%.
- Donde sea que esté su instancia EC2, su volumen estará en la misma zona de disponibilidad
- Un volumen de EBS solo se puede adjuntar a una instancia EC2 a la vez.
- Después de crear un volumen, puede adjuntarlo a cualquier instancia EC2 en la misma zona de disponibilidad.
- Amazon EBS ofrece la capacidad de crear instantáneas (copias de seguridad) de cualquier volumen de EBS y escribir una copia de los datos en el volumen en S3, donde se almacena de forma redundante en varias zonas de disponibilidad.
- Una instantánea de EBS refleja el contenido del volumen durante un instante concreto en el tiempo.
- Una imagen (AMI) es lo mismo, pero incluye un sistema operativo y un cargador de arranque para que pueda usarse para arrancar una instancia.
- Las AMI también se pueden considerar como servidores iniciables prefabricados. Las AMI siempre se utilizan al lanzar una instancia.
- Cuando aprovisiona una instancia EC2, lo primero que se le pide que especifique es una AMI. Puede elegir una AMI prefabricada o elegir la suya propia creada a partir de una instantánea de EBS.
- También puede utilizar los siguientes criterios para ayudar a elegir su AMI:
  - Sistema operativo
  - Arquitectura (32 bits o 64 bits)
  - Región
  - Permisos de lanzamiento
  - Almacenamiento del dispositivo raíz (más información en la sección correspondiente a continuación)
- Puede copiar AMI en regiones completamente nuevas.
- Al copiar AMI a nuevas regiones, Amazon no copiará los permisos de lanzamiento, las etiquetas definidas por el usuario o los permisos del depósito de Amazon S3 de la AMI de origen a la nueva AMI. Debe asegurarse de que esos detalles estén configurados correctamente para las instancias en la nueva región.
- Puede cambiar los volúmenes de EBS sobre la marcha, incluidos el tamaño y el tipo de almacenamiento

### SSD vs. HDD:
- Los volúmenes respaldados por SSD están diseñados para cargas de trabajo transaccionales que involucran operaciones frecuentes de lectura / escritura, donde el atributo de rendimiento dominante es IOPS. ** Regla de oro **: ¿Su carga de trabajo será pesada en IOPS? Planifique para SSD.
- Los volúmenes respaldados por HDD están diseñados para grandes cargas de trabajo de transmisión en las que el rendimiento (medido en MiB / s) es una mejor medida de rendimiento que IOPS. ** Regla de oro **: ¿Su carga de trabajo será pesada? Planifique para HDD.

![hdd_vs_ssd](https://user-images.githubusercontent.com/13093517/84944872-76165b80-b0b4-11ea-819c-a93deb999ea2.png)


### EBS Snapshots:
- Las instantáneas de EBS son copias puntuales de volúmenes. Puede pensar en las instantáneas como fotografías del estado actual del disco y el estado de todo lo que contiene.
- Una instantánea está restringida a la región donde se creó.
- Las instantáneas solo capturan el estado de cambio desde que se tomó la última instantánea. Esto es lo que se registra en cada nueva instantánea, no el estado completo del servidor.
- Por este motivo, es posible que la creación de la primera instantánea lleve algún tiempo. Esto se debe a que el cambio de estado de la primera instantánea es todo el nuevo volumen. Solo después se capturará el delta porque entonces habrá algo anterior con lo que comparar.
- Las instantáneas de EBS se producen de forma asíncrona, lo que significa que un volumen se puede utilizar normalmente mientras se realiza una instantánea.
- Al crear una instantánea para un dispositivo raíz futuro, se considera que las mejores prácticas son detener la instancia en ejecución donde se encuentra el dispositivo original antes de tomar la instantánea.
- La forma más sencilla de mover una instancia EC2 y un volumen a otra zona de disponibilidad es tomar una instantánea.
- Al crear una imagen a partir de una instantánea, si desea implementar un tipo de volumen diferente para la nueva imagen (por ejemplo, SSD de uso general -> HDD optimizado de rendimiento), debe asegurarse de que la virtualización de la nueva imagen sea asistida por hardware.
- Un breve resumen para crear copias de instancias EC2: Instancia antigua -> Instantánea -> Imagen (AMI) -> Nueva instancia
- No puede eliminar una instantánea de un volumen de EBS que se utiliza como dispositivo raíz de una AMI registrada. Si se eliminó la instantánea original, la AMI no podría usarla como base para crear nuevas instancias. Por esta razón, AWS lo protege de eliminar accidentalmente la instantánea de EBS, ya que podría ser fundamental para sus sistemas. Para eliminar una instantánea de EBS adjunta a una AMI registrada, primero elimine la AMI y luego se puede eliminar la instantánea.



### EBS Root Device Storage:
- Todos los volúmenes raíz de AMI (donde está instalado el sistema operativo de EC2) son de dos tipos: respaldados por EBS o respaldados por el almacén de instancias
- Cuando elimina una instancia EC2 que estaba usando un volumen raíz respaldado por el almacén de instancias, su volumen raíz también se eliminará. Sin embargo, los volúmenes adicionales o secundarios persistirán.
- Si usa un volumen raíz respaldado por EBS, el volumen raíz no terminará con su instancia EC2 cuando la instancia se desconecte. Los volúmenes respaldados por EBS no son dispositivos de almacenamiento temporal como los volúmenes respaldados por Instance Store.
- Los volúmenes respaldados por EBS se lanzan desde una instantánea de AWS EBS, como su nombre lo indica
- Los volúmenes respaldados por el almacén de instancias se inician desde una plantilla almacenada en AWS S3. Son efímeros, ¡así que tenga cuidado al cerrar una instancia!
- Los almacenes de instancias secundarios para un dispositivo raíz respaldado por un almacén de instancias deben instalarse durante el aprovisionamiento original del servidor. No puede agregar más después del hecho. Sin embargo, puede agregar volúmenes de EBS a la misma instancia después de la creación del servidor.
- Con estos inconvenientes de los volúmenes de Instance Store, ¿por qué elegir uno? Porque tienen una tasa de IOPS muy alta. Entonces, si bien un almacén de instancias no puede proporcionar persistencia de datos, puede proporcionar IOPS mucho más altas en comparación con el almacenamiento conectado a la red como EBS.
- Además, los almacenes de instancias son ideales para el almacenamiento temporal de información que cambia con frecuencia, como búferes, cachés, datos temporales y otro contenido temporal, o para datos que se replican en una flota de instancias, como un grupo de web con equilibrio de carga. servidores.
- ¿Cuándo usar uno sobre el otro?
  - Utilice EBS para datos de base de datos, registros críticos y configuraciones de aplicaciones.
  - Utilice el almacenamiento de instancia para datos en proceso, registros no críticos y estado transitorio de la aplicación.
  - Utilice S3 para los datos compartidos entre sistemas, como conjuntos de datos de entrada y resultados procesados, o para los datos estáticos que necesita cada nuevo sistema cuando se inicia.

### EBS Encryption:
- El cifrado de EBS ofrece una solución de cifrado sencilla para los recursos de EBS que no requiere que cree, mantenga y proteja su propia infraestructura de gestión de claves.
- Utiliza claves maestras del cliente (CMK) de AWS Key Management Service (AWS KMS) al crear instantáneas y volúmenes cifrados.
- Puede cifrar tanto el dispositivo raíz como los volúmenes secundarios de una instancia EC2. Cuando crea un volumen de EBS cifrado y lo adjunta a un tipo de instancia compatible, se cifran los siguientes tipos de datos:
  - Datos en reposo dentro del volumen
  - Todos los datos que se mueven entre el volumen y la instancia.
  - Todas las instantáneas creadas a partir del volumen.
  - Todos los volúmenes creados a partir de esas instantáneas
- EBS cifra su volumen con una clave de datos utilizando el algoritmo AES-256.
- Las instantáneas de volúmenes cifrados también se cifran naturalmente. Los volúmenes restaurados a partir de instantáneas cifradas también están cifrados. Solo puede compartir instantáneas sin cifrar.
- La antigua forma de cifrar un dispositivo raíz era crear una instantánea de una instancia EC2 aprovisionada. Al hacer una copia de esa instantánea, habilitó el cifrado durante la creación de la copia. Finalmente, una vez que se cifró la copia, creó una AMI a partir de la copia cifrada y solía tener una instancia EC2 con cifrado en el dispositivo raíz. Debido a lo complejo que es esto, ahora puede simplemente cifrar los dispositivos raíz como parte de las opciones de aprovisionamiento de EC2.

## Elastic Network Interfaces (ENI)

### Simplificando ENI:
Una interfaz de red elástica es un componente de red que representa una tarjeta de red virtual. Cuando aprovisiona una nueva instancia, se adjuntará una ENI automáticamente y podrá crear y configurar interfaces de red adicionales si lo desea. Cuando mueve una interfaz de red de una instancia a otra, el tráfico de red se redirige a la nueva instancia.

### Detalles Clave de ENI:
- ENI se utiliza principalmente para soluciones de red de bajo presupuesto y alta disponibilidad.
- Sin embargo, si sospecha que necesita un alto rendimiento de red, puede usar ENI de redes mejoradas.
- Red mejorada ENI utiliza virtualización de E / S de raíz única para proporcionar capacidades de red de alto rendimiento en tipos de instancias compatibles. SR-IOV proporciona mayor E / S y menor rendimiento y garantiza mayor ancho de banda, mayor rendimiento de paquetes por segundo (PPS) y latencias entre instancias más bajas de manera constante. SR-IOV hace esto al dedicar la interfaz a una sola instancia y omitir de manera efectiva partes del hipervisor, lo que permite un mejor rendimiento.
- Agregar más ENI no necesariamente acelerará el rendimiento de su red, pero el ENI de redes mejoradas sí lo hará.
- No hay ningún cargo adicional por usar ENI de red mejorada y el mejor rendimiento de red que proporciona. El único inconveniente es que Enhanced Networking ENI no está disponible en todos los tipos y familias de instancias EC2.
- Puede adjuntar una interfaz de red a una instancia EC2 de las siguientes formas:
  - Cuando está funcionando (conexión en caliente)
  - Cuando se detiene (adjunto caliente)
  - Cuando se inicia la instancia (conexión en frío).
- Si una instancia EC2 falla con ENI configurado correctamente, usted (o más probablemente, el código que se ejecuta en su nombre) puede conectar la interfaz de red a una instancia en espera activa. Debido a que las interfaces ENI mantienen sus propias direcciones IP privadas, direcciones IP elásticas y direcciones MAC, el tráfico de red comenzará a fluir hacia la instancia en espera tan pronto como conecte la interfaz de red a la instancia de reemplazo. Los usuarios experimentarán una breve pérdida de conectividad entre el momento en que falla la instancia y el momento en que la interfaz de red se conecta a la instancia en espera, pero no se requieren cambios en la tabla de rutas de la VPC ni en su servidor DNS.
- Para instancias que funcionan con Machine Learning y High Performance Computing, use EFA (Elastic Fabric Adapter). Los EFA aceleran el trabajo requerido de los casos de uso anteriores. EFA proporciona una latencia más baja y más consistente y un rendimiento más alto que el transporte TCP que se usa tradicionalmente en los sistemas informáticos de alto rendimiento basados ​​en la nube.
- EFA también puede usar la omisión del sistema operativo (solo en Linux) que permitirá que las aplicaciones ML y HPC interactúen con el Elastic Fabric Adapter directamente, en lugar de enrutarse normalmente a él a través del sistema operativo. Esto le da un gran aumento de rendimiento.
- Puede habilitar un registro de flujo de VPC en su interfaz de red para capturar información sobre el tráfico IP que entra y sale de una interfaz de red.

## Security Groups

### Simplificando Security Groups:
Los grupos de seguridad se utilizan para controlar el acceso (SSH, HTTP, RDP, etc.) con EC2. Actúan como un firewall virtual para que sus instancias controlen el tráfico entrante y saliente. Cuando lanza una instancia en una VPC, puede asignar hasta cinco grupos de seguridad a la instancia y los grupos de seguridad actúan a nivel de instancia, no a nivel de subred.

### Detalles Clave de los Security Groups:
- Los grupos de seguridad controlan el tráfico entrante y saliente para sus instancias (actúan como un cortafuegos para las instancias EC2) mientras que las NACL controlan el tráfico entrante y saliente para sus subredes (actúan como un cortafuegos para las subredes). Los grupos de seguridad generalmente controlan la lista de puertos que pueden usar sus instancias EC2 y las NACL controlan qué red o lista de direcciones IP pueden conectarse a toda su VPC.
- Cada vez que realiza un cambio en un grupo de seguridad, ese cambio se produce de inmediato.
- Siempre que crea una regla de entrada, se crea una regla de salida inmediatamente. Esto se debe a que los grupos de seguridad tienen * estado *. Esto significa que cuando crea una regla de entrada para un grupo de seguridad, se crea una regla de salida correspondiente para que coincida. Esto contrasta con las NACL que son * sin estado * y requieren intervención manual para crear reglas de entrada y salida.
- Las reglas del grupo de seguridad se basan en PERMITIR y no existe el concepto de DENEGAR cuando se trata de grupos de seguridad. Esto significa que no puede denegar explícitamente o incluir en la lista negra puertos específicos a través de Grupos de seguridad, solo puede denegarlos implícitamente excluyéndolos en su lista PERMITIDOS
- Debido al detalle anterior, todo está bloqueado por defecto. Debe ingresar y permitir intencionalmente el acceso a ciertos puertos.
- Los grupos de seguridad son específicos de una sola VPC, por lo que no puede compartir un grupo de seguridad entre varias VPC. Sin embargo, puede copiar un grupo de seguridad para crear un nuevo grupo de seguridad con las mismas reglas en otra VPC para la misma cuenta de AWS.
- Los grupos de seguridad son regionales y pueden abarcar zonas de disponibilidad, pero no pueden ser interregionales.
- Existen reglas de salida si necesita conectar su servidor a un servicio diferente, como un punto final de API o un backend de base de datos. Sin embargo, debe habilitar la regla ALLOW para el puerto correcto para que el tráfico pueda salir de EC2 e ingresar al otro servicio de AWS.
- Puede adjuntar varios grupos de seguridad a una instancia EC2 y puede tener varias instancias EC2 bajo el paraguas de un grupo de seguridad.
- Puede especificar la fuente de su grupo de seguridad (básicamente, a quién se le permite eludir el firewall virtual) para que sea una única dirección IP ** / 32 **, un rango de IP o incluso un grupo de seguridad separado.
- No puede bloquear direcciones IP específicas con grupos de seguridad (use NACL en su lugar)
- Puede aumentar el límite de su grupo de seguridad enviando una solicitud a AWS.

## Web Application Firewall (WAF)

### Simplificando WAF:
AWS WAF es una aplicación web que le permite permitir o bloquear las solicitudes HTTP vinculadas a CloudFront, API Gateway, Application Load Balancers, EC2 y otros puntos de entrada de Capa 7 en su entorno de AWS. AWS WAF le brinda control sobre la forma en que el tráfico llega a sus aplicaciones al permitirle crear reglas de seguridad que bloquean patrones de ataque comunes, como inyección de SQL o secuencias de comandos entre sitios, y reglas que filtran patrones de tráfico específicos que usted puede definir. El conjunto de reglas predeterminado de WAF aborda problemas como los 10 principales riesgos de seguridad de OWASP y se actualiza periódicamente cada vez que se descubren nuevas vulnerabilidades.

### Detalles Clave de WAF:
- Como se mencionó anteriormente, WAF funciona como un firewall de capa 7. Esto le otorga la capacidad de monitorear condiciones granulares basadas en la web, como parámetros de cadenas de consulta de URL. Este nivel de detalle ayuda a detectar tanto el juego sucio como los problemas honestos con las solicitudes que se transfieren a su entorno de AWS.
- Con WAF, puede establecer condiciones como qué direcciones IP pueden realizar qué tipo de solicitudes o acceder a qué tipo de contenido.
- Con base en estas condiciones, el punto final correspondiente permitirá la solicitud sirviendo el contenido solicitado o devolverá un estado HTTP 403 Prohibido.
- En el nivel más simple, AWS WAF le permite elegir uno de los siguientes comportamientos:
  - **Permitir todas las solicitudes excepto las que especifique**: esto es útil cuando desea que CloudFront o un Balanceador de carga de aplicaciones proporcionen contenido para un sitio web público, pero también desea bloquear las solicitudes de los atacantes.
  - **Bloquear todas las solicitudes excepto las que especifique**: esto es útil cuando desea entregar contenido para un sitio web restringido cuyos usuarios son fácilmente identificables por propiedades en las solicitudes web, como las direcciones IP que utilizan para navegar el sitio web.
  - **Contar las solicitudes que coincidan con las propiedades que especifique**: cuando desee permitir o bloquear solicitudes basadas en nuevas propiedades en solicitudes web, primero puede configurar AWS WAF para que cuente las solicitudes que coinciden con esas propiedades sin permitir o bloquear esas solicitudes. Esto le permite confirmar que no configuró accidentalmente AWS WAF para bloquear todo el tráfico a su sitio web. Cuando esté seguro de haber especificado las propiedades correctas, puede cambiar el comportamiento para permitir o bloquear solicitudes.

### Capacidades de protección WAF:
- Las diferentes características de la solicitud que se pueden utilizar para limitar el acceso:
  - La dirección IP desde la que se origina una solicitud
  - El país desde el que se origina una solicitud
  - Los valores que se encuentran en los encabezados de la solicitud.
  - Cualquier cadena que aparezca en la solicitud (ya sea cadenas específicas o cadenas que coincidan con un patrón de expresión regular)
  - La duración de la solicitud
  - Cualquier presencia de código SQL (probablemente un intento de inyección de SQL)
  - Cualquier presencia de un script (probablemente un intento de scripting entre sitios)
- También puede usar NACL para bloquear direcciones IP maliciosas, prevenir inyecciones de SQL / XSS y bloquear solicitudes de países específicos. Sin embargo, es una buena forma practicar la defensa en profundidad.
- Negar o bloquear a los usuarios malintencionados en el nivel WAF tiene la ventaja adicional de proteger su ecosistema AWS en su límite más externo.

## CloudWatch

### Simplificando CloudWatch:
Amazon CloudWatch es un servicio de supervisión y observabilidad. Le proporciona datos y conocimientos prácticos para supervisar sus aplicaciones, responder a los cambios de rendimiento de todo el sistema, optimizar la utilización de recursos y obtener una vista unificada del estado operativo.

### Detalles Clave de CloudWatch:
- CloudWatch recopila datos operativos y de supervisión en forma de registros, métricas y eventos.
- Puede usar CloudWatch para detectar comportamientos anómalos en sus entornos, configurar alarmas, visualizar registros y métricas en paralelo, tomar acciones automatizadas, solucionar problemas y descubrir información para mantener sus aplicaciones
funcionando fluidamente.
- Dentro del dominio informático, CloudWatch puede informarle sobre el estado de las instancias EC2, los grupos de ajuste de escala automático, los equilibradores de carga elásticos y las comprobaciones de estado de Route53.
Dentro de los dominios de almacenamiento y entrega de contenido, CloudWatch puede informarle sobre el estado de EBS Volumes, Storage Gateways y CloudFront.
- Con respecto a EC2, CloudWatch solo puede monitorear métricas de nivel de host como CPU, red, disco y verificaciones de estado para información como el estado del hipervisor subyacente.
- CloudWatch *NO* es CloudTrail, por lo que es importante saber que solo CloudTrail puede monitorear el acceso a AWS por razones de seguridad y auditoría. CloudWatch tiene que ver con el rendimiento. CloudTrail tiene que ver con la auditoría.
- CloudWatch con EC2 supervisará los eventos cada 5 minutos de forma predeterminada, pero puede tener intervalos de 1 minuto si utiliza la supervisión detallada.

![Screen Shot 2020-06-17 at 8 16 23 PM](https://user-images.githubusercontent.com/13093517/84963455-71af6a00-b0d7-11ea-8168-15dd791bf000.png)

- Puede personalizar sus paneles de CloudWatch para obtener información.
- Existe un agente CloudWatch multiplataforma que se puede instalar tanto en instancias basadas en Linux como en Windows. Este agente le permite seleccionar las métricas que se recopilarán, incluidas las métricas de recursos secundarios, como el núcleo por CPU. Puede utilizar este agente único para recopilar métricas del sistema y archivos de registro de instancias de Amazon EC2 y servidores locales.
- Las siguientes métricas no se recopilan de las instancias EC2 a través de CloudWatch:
  - Utilización de la memoria
  - Utilización de intercambio de disco
  - Utilización del espacio en disco
  - Utilización de archivos de página
  - Recolección de registros
- Si necesita la información anterior, puede recuperarla a través del agente oficial de CloudWatch o puede crear una métrica personalizada y enviar los datos por su cuenta a través de un script personalizado.
- Propósito clave de CloudWatch:
  - Recopilar métricas
  - Recoger registros
  - Recoger eventos
  - Crear alarmas
  - Crear dashboards

### CloudWatch Logs:
- Puede usar Amazon CloudWatch Logs para monitorear, almacenar y acceder a sus archivos de registro desde instancias Amazon EC2, AWS CloudTrail, Amazon Route 53 y otras fuentes. Luego, puede recuperar los datos de registro asociados de CloudWatch Logs.
- Le ayuda a centralizar los registros de todos sus sistemas, aplicaciones y servicios de AWS que utiliza, en un único servicio altamente escalable.
- Puede crear grupos de registros para unir unidades lógicas de CloudWatch Logs.
- Puede transmitir archivos de registro personalizados para obtener más información.

### CloudWatch Events:
- Amazon CloudWatch Events ofrece un flujo casi en tiempo real de eventos del sistema que describen cambios en los recursos de AWS.
- Puede usar eventos para activar lambdas, por ejemplo, mientras usa alarmas para informarle que algo salió mal.

### CloudWatch Alarms:
- Las alarmas de CloudWatch envían notificaciones o realizan cambios automáticamente en los recursos que está monitoreando según las reglas que usted define.
- Por ejemplo, puede crear alarmas personalizadas de CloudWatch que activarán notificaciones como la superación de un umbral de facturación establecido.
- Las alarmas de CloudWatch tienen dos estados: `ok` o `alarm`

### CloudWatch Metrics:
- Las métricas de CloudWatch representan un conjunto de puntos de datos ordenados por tiempo.
- Se trata básicamente de una variable que puede supervisar a lo largo del tiempo para ayudar a saber si todo está bien, p. Ej. Utilización de CPU por hora.
- CloudWatch Metrics le permite realizar un seguimiento de las métricas de alta resolución a intervalos de un minuto hasta por segundo.

### CloudWatch Dashboards:
- Los paneles de CloudWatch son páginas de inicio personalizables en la consola de CloudWatch que puede usar para monitorear sus recursos en una sola vista.
- Estos paneles se integran con CloudWatch Metrics y CloudWatch Alarms para crear vistas personalizadas de las métricas y alarmas para sus recursos de AWS.

## CloudTrail

### Simplificando CloudTrail:
AWS CloudTrail es un servicio que permite la gobernanza, el cumplimiento, la auditoría operativa y la auditoría de riesgos de su cuenta de AWS. Con él, puede registrar, monitorear continuamente y retener la actividad de la cuenta relacionada con las acciones en su infraestructura de AWS. CloudTrail proporciona un historial de eventos de la actividad de su cuenta de AWS, incluidas las acciones realizadas a través de la Consola de administración de AWS, los SDK de AWS, las herramientas de línea de comandos, las llamadas a la API y otros servicios de AWS. Es un servicio regional, pero puede configurar CloudTrail para recopilar senderos en todas las regiones.

### Detalles Clave de CloudTrail:
- CloudTrail Events registra las llamadas o actividades de la API.
- CloudTrail Events almacena los últimos 90 días de eventos en su Historial de eventos. Esto está habilitado de manera predeterminada y no tiene costo adicional.
- Este historial de eventos simplifica el análisis de seguridad, el seguimiento de cambios de recursos y la resolución de problemas.
- Hay dos tipos de eventos que se pueden registrar en CloudTrail: eventos de gestión y eventos de datos.
- Los eventos de administración brindan información sobre las operaciones de administración que se realizan en los recursos de su cuenta de AWS.
- Piense en los eventos de administración como cosas que normalmente hacen las personas cuando están en AWS. Ejemplos:
  - un usuario inicia sesión
  - una política cambiada
  - una configuración de seguridad recién creada
  - una eliminación de la regla de registro
- Los eventos de datos proporcionan información sobre las operaciones de recursos realizadas en o en un recurso.
- Piense en los eventos de datos como cosas que normalmente hace el software cuando llega a varios puntos finales de AWS. Ejemplos:
  - Actividad de API a nivel de objeto de S3
  - Actividad de ejecución de la función Lambda
- De forma predeterminada, CloudTrail registra eventos de administración, pero no eventos de datos.
- De forma predeterminada, los archivos de registro de eventos de CloudTrail se cifran mediante el cifrado del lado del servidor (SSE) de Amazon S3. También puede optar por cifrar sus archivos de registro con una clave de AWS Key Management Service (AWS KMS). Como estos registros se almacenan en S3, puede definir las reglas del ciclo de vida de Amazon S3 para archivar o eliminar archivos de registro automáticamente. Si desea recibir notificaciones sobre la entrega y validación de archivos de registro, puede configurar las notificaciones de Amazon SNS.

## Elastic File System (EFS)

### Simplificando EFS:
EFS proporciona un sistema de archivos NFS elástico simple y completamente administrado para su uso dentro de AWS. EFS escala de forma automática e instantánea la capacidad de almacenamiento de su sistema de archivos hacia arriba o hacia abajo a medida que agrega o elimina archivos sin interrumpir su aplicación.

### Detalles Clave de EFS:
- En EFS, la capacidad de almacenamiento es elástica (crece y se reduce automáticamente) y su tamaño cambia según la adición o eliminación de archivos.
- Si bien EBS monta un volumen de EBS en una instancia, puede adjuntar un volumen de EFS en varias instancias de EC2.
- Las instancias EC2 se comunican con el sistema de archivos remoto mediante el protocolo NFSv4. Esto hace que sea necesario abrir el puerto NFS para nuestro grupo de seguridad (reglas de firewall EC2) para permitir el tráfico entrante en ese puerto.
- Dentro de un volumen EFS, el estado de destino de montaje le permitirá saber qué instancias están disponibles para montar
- Con EFS, solo paga por el almacenamiento que usa, por lo que paga sobre la marcha. No se requiere aprovisionamiento previo.
- EFS puede escalar hasta los petabytes y puede admitir miles de conexiones NFS simultáneas.
- Los datos se almacenan en varias zonas de disponibilidad en una región y EFS garantiza la coherencia de lectura tras escritura.
- Es mejor para el almacenamiento de archivos al que accede una flota de servidores en lugar de solo un servidor.

## Amazon FSx para Windows

### Simplificando Amazon FSx para Windows:
Amazon FSx para Windows File Server proporciona un sistema de archivos nativo de Microsoft totalmente administrado.

### Detalles Clave de Amazon FSx para Windows:
- Con FSx para Windows, puede mover fácilmente sus aplicaciones basadas en Windows que requieren almacenamiento de archivos en AWS.
- Está construido en Windows Server y existe únicamente para aplicaciones basadas en Microsoft, por lo que si necesita almacenamiento de archivos basado en SMB, elija FSx.
- FSx para Windows también permite la conectividad entre los servidores locales y AWS, por lo que esos mismos servidores locales también pueden hacer uso de Amazon FSx.
- Puede utilizar Microsoft Active Directory para autenticarse en el sistema de archivos.
- Amazon FSx para Windows proporciona varios niveles de seguridad y cumplimiento para ayudar a garantizar que sus datos estén protegidos. Amazon FSx cifra automáticamente sus datos en reposo y en tránsito.
- Puede acceder a Amazon FSx para Windows desde una variedad de recursos informáticos, no solo desde EC2.
- Puede implementar su Amazon FSx para Windows en una sola AZ o en una configuración Multi-AZ.
- Puede utilizar SSD o HDD para el dispositivo de almacenamiento según sus requisitos.
- FSx para Windows admite copias de seguridad automáticas diarias y los administradores también realizan copias de seguridad cuando es necesario.
- FSx para Windows elimina el contenido duplicado y comprime el contenido común
- De forma predeterminada, todos los datos están encriptados en reposo.

## Amazon FSx para Lustre

### Simplificando Amazon FSx para Lustre:
Amazon FSx para Lustre hace que sea fácil y rentable iniciar y ejecutar el sistema de archivos de código abierto Lustre para aplicaciones informáticas de alto rendimiento. Con FSx para Lustre, puede iniciar y ejecutar un sistema de archivos que puede procesar conjuntos de datos masivos a cientos de gigabytes por segundo de rendimiento, millones de IOPS y latencias de menos de milisegundos.

### Detalles Clave de Amazon FSx para Lustre:
- FSx para Lustre es compatible con las AMI basadas en Linux más populares, incluidas Amazon Linux, Amazon Linux 2, Red Hat Enterprise Linux (RHEL), CentOS, SUSE Linux y Ubuntu.
- Dado que el sistema de archivos Lustre está diseñado para cargas de trabajo informáticas de alto rendimiento que normalmente se ejecutan en clústeres informáticos, elija EFS para el sistema de archivos normal de Linux si sus requisitos no coinciden con este caso de uso.
- FSx Lustre tiene la capacidad de almacenar y recuperar datos directamente en S3 por sí solo.

## Relational Database Service (RDS)

### Simplificando RDS:
RDS es un servicio administrado que facilita la configuración, el funcionamiento y el escalado de una base de datos relacional en AWS. Proporciona una capacidad rentable y redimensionable al tiempo que automatiza o subcontrata tareas de administración que requieren mucho tiempo, como el aprovisionamiento de hardware, la configuración de la base de datos, la aplicación de parches y las copias de seguridad.

### Detalles Clave de RDS:
- RDS viene en seis sabores diferentes:
  - Servidor SQL
  - Oracle
  - Servidor MySQL
  - PostgreSQL
  - MariaDB
  - Aurora
- Piense en RDS como el motor de base de datos en el que se encuentran varias bases de datos.
- RDS tiene dos características clave al escalar horizontalmente:
  - Leer la replicación para mejorar el rendimiento
  - Multi-AZ para alta disponibilidad
- En el mundo de las bases de datos, el *Procesamiento de transacciones en línea (OLTP)* difiere del *Procesamiento analítico en línea (OLAP)* en términos del tipo de consulta que realizaría. OLTP proporciona datos para la lógica empresarial que, en última instancia, compone el funcionamiento principal de su plataforma o aplicación. OLAP es obtener información sobre los datos que ha almacenado para tomar mejores decisiones estratégicas como empresa.
- RDS se ejecuta en máquinas virtuales, pero no tiene acceso a esas máquinas. No puede SSH en una instancia de RDS, por lo que no puede parchear el sistema operativo. Esto significa que AWS es responsable de la seguridad y el mantenimiento de RDS. Puede aprovisionar una instancia EC2 como base de datos si necesita o desea administrar el servidor subyacente usted mismo, pero no con un motor RDS.
- El hecho de que no pueda acceder a la máquina virtual directamente, no significa que RDS no tenga servidor. Sin embargo, existe Aurora sin servidor (que se explica a continuación) que tiene un propósito específico.
- Las colas de SQS se pueden usar para almacenar escrituras de base de datos pendientes si su aplicación tiene problemas con una carga de escritura alta. Estas escrituras se pueden agregar a la base de datos cuando la base de datos esté lista para procesarlas. Agregar más IOPS también ayudará, pero esto por sí solo no eliminará por completo la posibilidad de que se pierdan las escrituras. Sin embargo, una cola asegura que las escrituras en la base de datos no se pierdan.

### RDS Multi-AZ:
- La recuperación ante desastres en AWS siempre busca garantizar que las copias en espera de los recursos se mantengan en un área geográfica separada. De esta manera, si alguna vez ocurre un desastre (desastre natural, conflicto político, etc.) donde están sus recursos originales, las copias no se verán afectadas.
- Cuando aprovisiona una instancia de base de datos Multi-AZ, Amazon RDS crea automáticamente una instancia de base de datos principal y replica de forma síncrona los datos en una instancia en espera en una zona de disponibilidad (AZ) diferente. Cada AZ se ejecuta en su propia infraestructura independiente, físicamente distinta y está diseñada para ser altamente confiable.
- Con una configuración Multi-AZ, EC2 se conecta a su almacén de datos RDS utilizando una dirección DNS enmascarada como una cadena de conexión. Si la base de datos principal falla, Multi-AZ es lo suficientemente inteligente como para detectar esa falla y actualizar automáticamente la dirección DNS para que apunte a la secundaria. No se requiere intervención manual y AWS se encarga de intercambiar la dirección IP en DNS.
- Multi-AZ es compatible con todos los tipos de DB excepto aurora. Esto se debe a que Aurora es completamente tolerante a fallas por sí sola.
- La función Multi-AZ permite una alta disponibilidad en las zonas de disponibilidad y no en las regiones.
- Durante una conmutación por error, el antiguo primario recuperado se convierte en el nuevo secundario y el secundario promovido se convierte en primario. Una vez que se recupera la base de datos original, se iniciará un proceso de sincronización en el que las dos bases de datos se reflejan entre sí una vez para sincronizarse con los nuevos datos que el primario anterior fallido podría haberse perdido.
- Puede forzar una conmutación por error para una configuración Multi-AZ reiniciando la instancia principal
- Con una configuración Multi-AZ RDS, las copias de seguridad se toman desde el modo de espera.

### RDS Read Replicas:
- La replicación de lectura se utiliza exclusivamente para mejorar el rendimiento.
- Con una configuración de réplica de lectura, EC2 se conecta al backend RDS mediante una dirección DNS y cada escritura que recibe la base de datos maestra también se pasa a una base de datos secundaria para que se convierta en una copia perfecta de la maestra. Esto tiene el efecto general de reducir el número de transacciones en el maestro porque las bases de datos secundarias pueden consultarse para obtener los mismos datos.
- Sin embargo, si fallara la base de datos maestra, no hay conmutación por error automática. Tendría que crear manualmente una nueva cadena de conexión para sincronizar con una de las réplicas de lectura para que se convierta en un maestro por sí solo. Luego, tendría que actualizar sus instancias EC2 para que apunten a la réplica de lectura. Puede tener hasta tener copias de su base de datos maestra con replicación de lectura.
- Puede promover réplicas de lectura para que sean su propia base de datos de producción si es necesario.
- Las réplicas de lectura son compatibles con los seis tipos de DB además de RDS.
- Cada réplica de lectura tendrá su propio punto final de DNS.
- Las copias de seguridad automatizadas deben estar habilitadas para usar réplicas de lectura.
- Puede tener réplicas de lectura con Multi-AZ activado o tener la réplica de lectura en una región completamente separada. Incluso puede haber leído réplicas de réplicas de lectura, pero tenga cuidado con la latencia o el retraso de replicación.
La advertencia para las réplicas de lectura es que están sujetas a pequeñas cantidades de retraso de replicación. Esto se debe a que es posible que les falten algunas de las últimas transacciones, ya que no se actualizan tan rápido como las primarias. Los diseñadores de aplicaciones deben considerar qué consultas tienen tolerancia a datos ligeramente obsoletos. Esas consultas deben ejecutarse en la réplica de lectura, mientras que aquellas que exigen datos completamente actualizados deben ejecutarse en el nodo principal.

### RDS Backups:
- Cuando se trata de RDS, existen dos tipos de copias de seguridad:
  - copias de seguridad automatizadas
  - instantáneas de la base de datos
- **Las copias de seguridad automatizadas** le permiten recuperar su base de datos en cualquier momento dentro de un período de retención (entre uno y 35 días). Las copias de seguridad automatizadas tomarán una instantánea diaria completa y también almacenarán registros de transacciones a lo largo del día. Cuando realiza una recuperación de la base de datos, RDS primero elegirá la copia de seguridad diaria más reciente y aplicará los registros de transacciones relevantes de ese día. Dentro del período de retención establecido, esto le brinda la capacidad de realizar una recuperación de un punto en el tiempo hasta el segundo preciso.
Las copias de seguridad automatizadas están habilitadas de forma predeterminada. Los datos de la copia de seguridad se almacenan libremente hasta el tamaño de su base de datos real (por lo que por cada GB guardado en RDS, esa misma cantidad se almacenará libremente en S3 hasta el límite de GB de la base de datos). Las copias de seguridad se realizan dentro de una ventana definida, por lo que la latencia puede aumentar a medida que se suspende la E / S de almacenamiento para que se realice una copia de seguridad de los datos.
- Las **instantáneas de base de datos** las realiza manualmente el administrador. Una clave diferente de las copias de seguridad automatizadas es que se conservan incluso después de que finaliza la instancia de RDS original. Con las copias de seguridad automatizadas, los datos de la copia de seguridad en S3 se borran junto con el motor RDS. Es por eso que se le pregunta si desea tomar una instantánea final de su base de datos cuando vaya a eliminarla.
- Cuando va a restaurar una base de datos a través de copias de seguridad automáticas o instantáneas de base de datos, el resultado es el aprovisionamiento de una instancia de RDS completamente nueva con su propio punto final de base de datos para poder alcanzarla.

### RDS Security:
- Puede autenticarse en su instancia de base de datos mediante la autenticación de base de datos de IAM. La autenticación de la base de datos IAM funciona con MySQL y PostgreSQL. Con este método de autenticación, no necesita usar una contraseña cuando se conecta a una instancia de base de datos. En su lugar, usa un token de autenticación.
- Un token de autenticación es una cadena única que Amazon RDS genera a pedido. Los tokens de autenticación tienen una duración de 15 minutos. No es necesario que almacene las credenciales de usuario en la base de datos porque la autenticación se administra externamente mediante IAM.
- La autenticación de la base de datos de IAM proporciona los siguientes beneficios:
  - El tráfico de red hacia y desde la base de datos se cifra mediante Secure Sockets Layer (SSL).
  - Puede usar IAM para administrar de forma centralizada el acceso a los recursos de su base de datos, en lugar de administrar el acceso individualmente en cada instancia de base de datos.
  - Para las aplicaciones que se ejecutan en Amazon EC2, puede usar credenciales de perfil específicas para su instancia EC2 para acceder a su base de datos en lugar de una contraseña, para mayor seguridad
- El cifrado en reposo es compatible con los seis tipos de DB para RDS. El cifrado se realiza mediante el servicio AWS KMS. Una vez que se habilita el cifrado de la instancia de RDS, los datos de la base de datos se cifran, así como todas las copias de seguridad (automáticas o instantáneas) y las réplicas de lectura.
- Una vez cifrados sus datos, Amazon RDS gestiona la autenticación del acceso y el descifrado de sus datos de forma transparente con un impacto mínimo en el rendimiento. No es necesario que modifique las aplicaciones cliente de su base de datos para utilizar el cifrado.
- El cifrado de Amazon RDS está disponible actualmente para todos los motores de base de datos y tipos de almacenamiento. Sin embargo, debe asegurarse de que el tipo de instancia subyacente admita el cifrado de base de datos.
- Solo puede habilitar el cifrado para una instancia de base de datos de Amazon RDS cuando la crea, no después de que se crea la instancia de base de datos y
Las instancias de base de datos que están cifradas no se pueden modificar para deshabilitar el cifrado.

### RDS Enhanced Monitoring:
- RDS viene con una función de monitoreo mejorado. Amazon RDS proporciona métricas en tiempo real para el sistema operativo (SO) en el que se ejecuta su instancia de base de datos. Puede ver las métricas de su instancia de base de datos mediante la consola o consumir la salida JSON de monitoreo mejorado de CloudWatch Logs en un sistema de monitoreo de su elección.
- De forma predeterminada, las métricas de Monitoreo mejorado se almacenan en los registros de CloudWatch durante 30 días. Para modificar la cantidad de tiempo que las métricas se almacenan en los registros de CloudWatch, cambie la retención del grupo de registros de métricas del sistema operativo RDS en la consola de CloudWatch.
- Tenga en cuenta que existen diferencias clave entre CloudWatch y las métricas de monitoreo mejoradas. CloudWatch recopila métricas sobre el uso de CPU del hipervisor para una instancia de base de datos y Enhanced Monitoring recopila sus métricas de un agente en la instancia. Como resultado, es posible que encuentre diferencias entre las mediciones, porque la capa del hipervisor realiza una pequeña cantidad de trabajo que se puede recoger e interpretar como parte de la métrica.

## Aurora

### Simplificando Aurora:
Aurora es la base de datos insignia de AWS conocida por combinar el rendimiento y la disponibilidad de las bases de datos empresariales tradicionales con la simplicidad y la rentabilidad de las bases de datos de código abierto. Es un RDBMS compatible con MySQL / PostgreSQL que proporciona la seguridad, disponibilidad y confiabilidad de las bases de datos comerciales a una décima parte del costo de la competencia. Es mucho más eficaz como base de datos de AWS debido a los multiplicadores de rendimiento de 5x y 3x para MySQL y PostgreSQL respectivamente.

### Detalles Clave de Aurora:
- En caso de una falla en la infraestructura, Aurora realiza una conmutación por error automática a una réplica propia.
- Amazon Aurora generalmente involucra un clúster de instancias de base de datos en lugar de una sola instancia. Cada conexión es manejada por una instancia de base de datos específica. Cuando se conecta a un clúster de Aurora, el nombre de host y el puerto que especifica apuntan a un controlador intermedio llamado punto final. Aurora usa el mecanismo de punto final para abstraer estas conexiones. Por lo tanto, no tiene que codificar todos los nombres de host o escribir su propia lógica para equilibrar la carga y redireccionar las conexiones cuando algunas instancias de base de datos no están disponibles.
- De forma predeterminada, hay 2 copias en un mínimo de 3 zonas de disponibilidad para un total de 6 copias para todos sus datos de Aurora. Esto le permite manejar la pérdida potencial de hasta 2 copias de sus datos sin afectar la disponibilidad de escritura y hasta 3 copias de sus datos sin afectar la disponibilidad de lectura.
- El almacenamiento Aurora se recupera automáticamente y los bloques de datos y los discos se escanean continuamente en busca de errores. Si se encuentra alguno, esos errores se reparan automáticamente.
- La replicación de Aurora difiere de las réplicas de RDS en el sentido de que es posible que las réplicas de Aurora estén en espera como parte de una configuración de varias zonas de disponibilidad, así como un destino para el tráfico de lectura. En RDS, el modo de espera multi-AZ no se puede configurar para ser un punto final de lectura y solo las réplicas de lectura pueden cumplir esa función.
- Con la replicación de Aurora, puede tener hasta quince copias. Si desea obtener MySQL o PostgreSQL en sentido descendente a medida que replica las copias, solo puede tener 5 o 1.
- La conmutación por error automatizada solo es posible con la replicación de lectura de Aurora
- Para obtener más información sobre las diferencias entre la replicación RDS y la replicación Aurora, consulte lo siguiente:

![Screen Shot 2020-06-18 at 3 02 39 PM](https://user-images.githubusercontent.com/13093517/85061446-d240b480-b174-11ea-9dc4-f40d82743250.png)

- Las copias de seguridad automatizadas siempre están habilitadas en las instancias de Aurora y las copias de seguridad no afectan el rendimiento de la base de datos. También puede tomar instantáneas que tampoco afectan el rendimiento. Sus instantáneas se pueden compartir entre cuentas de AWS.
- Una táctica común para migrar bases de datos RDS a Aurora RD es crear una réplica de lectura de una base de datos RDS MariaDB / MySQL como una base de datos Aurora. Luego, simplemente promueva la base de datos Aurora en una instancia de producción y elimine la antigua base de datos MariaDB / MySQL.
- Aurora comienza con 10 GB y escala por 10 GB hasta 64 TB mediante el ajuste de escala automático del almacenamiento. La potencia informática de Aurora escala hasta 32 vCPU y 244 GB de memoria

### Aurora Serverless:
- Aurora Serverless es una configuración simple de autoescalado bajo demanda para las ediciones de Aurora compatibles con MySQL / PostgreSQl. Con Aurora Serverless, su instancia se escala automáticamente hacia arriba o hacia abajo y se inicia o se apaga según el uso de su aplicación. Los casos de uso de este servicio son cargas de trabajo poco frecuentes, intermitentes e impredecibles.
- Esto también lo hace posible más barato porque solo paga por invocación
- Con Aurora Serverless, simplemente crea un punto final de base de datos, opcionalmente especifica el rango de capacidad de la base de datos deseada y conecta sus aplicaciones.
- Elimina la complejidad de administrar las instancias y la capacidad de la base de datos. La base de datos se iniciará, cerrará y escalará automáticamente para adaptarse a las necesidades de su aplicación. Escalará sin problemas la capacidad informática y de memoria según sea necesario, sin interrumpir las conexiones del cliente.

### Aurora Cluster Endpoints:
- Con los extremos del clúster, asigna cada conexión a la instancia o grupo de instancias adecuado según su caso de uso.
- Puede conectarse a puntos finales de clúster asociados con diferentes roles o trabajos en su base de datos Aurora. Esto se debe a que diferentes instancias o grupos de instancias realizan diferentes funciones.
- Por ejemplo, para realizar declaraciones DDL, puede conectarse a la instancia principal. Para realizar consultas, puede conectarse al punto final del lector, y Aurora realiza automáticamente el equilibrio de carga entre todas las réplicas de Aurora detrás del punto final del lector. Para el diagnóstico o el ajuste, puede conectarse a un punto final diferente para examinar los detalles.
- Dado que la entrada para su instancia de base de datos sigue siendo la misma después de una conmutación por error, su aplicación puede reanudar el funcionamiento de la base de datos sin la necesidad de una intervención administrativa manual para ninguno de sus puntos finales.

### Aurora Reader Endpoints:
- Los puntos finales de Aurora Reader son un subconjunto de la idea anterior de puntos finales de clúster. Utilice el punto final del lector para operaciones de lectura, como consultas. Al procesar esas declaraciones en las réplicas de Aurora de solo lectura, este extremo reduce la sobrecarga en la instancia principal.
- Hay hasta 15 réplicas de lectura de Aurora porque un punto final de lector ayuda a manejar el tráfico de consultas de solo lectura.
- También ayuda al clúster a escalar la capacidad para manejar consultas SELECT simultáneas, proporcional al número de réplicas de Aurora en el clúster. Cada clúster de base de datos Aurora tiene un punto final de lector.
- Si el clúster contiene una o más réplicas de Aurora, el extremo del lector equilibra la carga de cada solicitud de conexión entre las réplicas de Aurora. En ese caso, solo puede realizar declaraciones de solo lectura como SELECT en esa sesión. Si el clúster solo contiene una instancia principal y no hay réplicas de Aurora, el extremo del lector se conecta directamente a la instancia principal. En ese caso, puede realizar operaciones de escritura a través del punto final.

## DynamoDB

### Simplificando DynamoDB:
Amazon DynamoDB es una base de datos de documentos y valores clave que ofrece un rendimiento de milisegundos de un solo dígito a cualquier escala. Es una base de datos que no es SQL, completamente administrada, de varias regiones, varios maestros y duradera. Viene con seguridad incorporada, respaldo y restauración, y almacenamiento en caché en memoria para aplicaciones a escala de Internet.

### Detalles Clave de DynamoDB:
- Los componentes principales de DynamoDB son:
  - una colección que sirve como mesa fundamental
  - un documento que es equivalente a una fila en una base de datos SQL
  - pares clave-valor que son los campos dentro del documento o fila
- La conveniencia de las bases de datos no relacionales es que cada fila puede verse completamente diferente según su caso de uso. No es necesario que haya uniformidad. Por ejemplo, si necesita una nueva columna para una entrada en particular, tampoco necesita asegurarse de que esa columna exista para las otras entradas.
- DynamoDB admite modelos basados ​​en documentos y valores clave. Es ideal para dispositivos móviles, web, juegos, tecnología publicitaria, IoT, etc.
- DynamoDB se almacena a través de SSD, por eso es tan rápido.
- Se distribuye en 3 centros de datos geográficamente distintos.
- El modelo de consistencia predeterminado es Lecturas eventualmente consistentes, pero también hay Lecturas fuertemente consistentes.
- La diferencia entre los dos modelos de consistencia es la regla de un segundo. Con Eventual Consistent Reads, todas las copias de datos generalmente se alcanzan en un segundo. Una lectura repetida después de un corto período de tiempo debería devolver los datos actualizados. Sin embargo, si necesita leer datos actualizados en menos de un segundo y esto debe ser una garantía, las lecturas consistentes son su mejor opción.
- Si se enfrenta a un escenario que requiere que el esquema, o la estructura de sus datos, cambie con frecuencia, entonces debe elegir una base de datos que proporcione una forma flexible y no rígida de agregar o eliminar nuevos tipos de datos. Este es un ejemplo clásico de elegir entre una base de datos relacional y una base de datos no relacional (NoSQL). En este escenario, elija DynamoDB.
- Un sistema de base de datos relacional no se escala bien por las siguientes razones:
  - Normaliza los datos y los almacena en múltiples tablas que requieren múltiples consultas para escribir en el disco.
  - Por lo general, incurre en los costos de rendimiento de un sistema de transacciones compatible con ACID.
  - Utiliza uniones costosas para reensamblar las vistas requeridas de los resultados de la consulta.
- La cardinalidad alta es buena para el rendimiento de E / S de DynamoDB. Cuanto más distintos sean los valores de clave de su partición, mejor. Hace que las solicitudes enviadas se distribuyan por el espacio particionado.
- DynamoDB utiliza el procesamiento paralelo para lograr un rendimiento predecible. Puede visualizar cada partición o nodo como un servidor de base de datos independiente de tamaño fijo con cada partición o nodo responsable de un bloque de datos definido. En terminología SQL, este concepto se conoce como fragmentación, pero, por supuesto, DynamoDB no es una base de datos basada en SQL. Con DynamoDB, los datos se almacenan en unidades de estado sólido (SSD).

### DynamoDB Accelerator (DAX):
- Amazon DynamoDB Accelerator (DAX) es una caché en memoria totalmente administrada y de alta disponibilidad que puede reducir los tiempos de respuesta de Amazon DynamoDB de milisegundos a microsegundos, incluso a millones de solicitudes por segundo.
- Con DAX, sus aplicaciones siguen siendo rápidas y receptivas, incluso cuando se le presentan volúmenes de solicitudes sin precedentes. No se requiere ajuste.
- DAX le permite escalar bajo demanda a un clúster de diez nodos, lo que le brinda millones de solicitudes por segundo.
- DAX hace más que simplemente aumentar el rendimiento de lectura al tener caché de escritura. Esto también mejora el rendimiento de escritura.
- Al igual que DynamoDB, DAX está completamente administrado. Ya no necesita preocuparse por las tareas de administración, como el aprovisionamiento de hardware o software, la instalación y la configuración, la aplicación de parches de software, el funcionamiento de un clúster de caché distribuido confiable o la replicación de datos en varias instancias a medida que escala.
- Esto significa que no es necesario que los desarrolladores administren la lógica de almacenamiento en caché. DAX es completamente compatible con las llamadas API de DynamoDB existentes.
- DAX le permite aprovisionar un clúster de DAX para varias tablas de DynamoDB, varios clústeres de DAX para una sola tabla de DynamoDB o en algún punto intermedio, lo que le brinda la máxima flexibilidad.
- DAX está diseñado para HA, por lo que, en caso de falla de una AZ, conmutará por error a una de sus réplicas en otra AZ. Esto también se gestiona automáticamente.

### DynamoDB Streams:
- Un flujo de DynamoDB es un flujo ordenado de información sobre cambios en elementos en una tabla de Amazon DynamoDB. Cuando habilita una transmisión en una tabla, DynamoDB captura información sobre cada modificación de los elementos de datos en la tabla.
- Amazon DynamoDB está integrado con AWS Lambda para que pueda crear desencadenadores: fragmentos de código que responden automáticamente a eventos en DynamoDB Streams.
- Inmediatamente después de que se modifica un elemento de la tabla, aparece un nuevo registro en el flujo de la tabla. AWS Lambda sondea la transmisión e invoca su función Lambda de forma sincrónica cuando detecta nuevos registros de transmisión. La función Lambda puede realizar cualquier acción que especifique, como enviar una notificación o iniciar un flujo de trabajo.
- Con los activadores, puede crear aplicaciones que reaccionen a las modificaciones de datos en las tablas de DynamoDB.
- Siempre que una aplicación crea, actualiza o elimina elementos de la tabla, DynamoDB Streams escribe un registro de flujo con los atributos de clave principal de los elementos que se modificaron. Un registro de flujo contiene información sobre una modificación de datos en un solo elemento en una tabla de DynamoDB. Puede configurar la transmisión para que los registros de la transmisión capturen información adicional, como las imágenes "antes" y "después" de los elementos modificados.

### DynamoDB Global Tables
- Global Tables es una solución de replicación multirregional y multimaestro para un rápido rendimiento local de aplicaciones distribuidas globalmente.
- Global Tables replica sus tablas de Amazon DynamoDB automáticamente en las regiones de AWS que elija.
- Se basa en transmisiones de DynamoDB y es redundante en varias regiones para fines de recuperación de datos o alta disponibilidad. La conmutación por error de la aplicación es tan simple como redirigir las llamadas de DynamoDB de su aplicación a otra región de AWS.
- Global Tables elimina el difícil trabajo de replicar datos entre regiones y resolver conflictos de actualización, lo que le permite concentrarse en la lógica empresarial de su aplicación. No es necesario que vuelva a escribir sus aplicaciones para hacer uso de tablas globales.
- La latencia de replicación con tablas globales suele ser inferior a un segundo.


## Redshift

### Simplificando Redshift:
Amazon Redshift es un servicio de almacenamiento de datos a escala de petabytes totalmente administrado en la nube. El servicio Amazon Redshift gestiona todo el trabajo de configurar, operar y escalar un almacén de datos. Estas tareas incluyen la capacidad de aprovisionamiento, la supervisión y la copia de seguridad del clúster, y la aplicación de parches y actualizaciones al motor de Amazon Redshift.

### Detalles Clave de Redshift:
- Un clúster de Amazon Redshift es un conjunto de nodos que consta de un nodo líder y uno o más nodos de cómputo. El tipo y la cantidad de nodos de cómputo que necesita depende del tamaño de sus datos, la cantidad de consultas que ejecutará y el rendimiento de ejecución de consultas que necesita.
- Redshift se utiliza para inteligencia empresarial y extrae conjuntos de datos muy grandes y complejos para realizar consultas complejas con el fin de recopilar información a partir de los datos.
- Se ajusta al caso de uso del procesamiento analítico en línea (OLAP). Redshift es una poderosa tecnología para el descubrimiento de datos que incluye capacidades para visualización de informes casi ilimitada, cálculos analíticos complejos y planificación de escenarios predictivos "qué pasaría si" (presupuesto, previsión, etc.).
- Dependiendo de sus necesidades de almacenamiento de datos, puede comenzar con un clúster pequeño de un solo nodo y escalar fácilmente a un clúster de varios nodos más grande a medida que cambien sus requisitos. Puede agregar o quitar nodos informáticos al clúster sin interrumpir el servicio.
- Si tiene la intención de mantener su clúster en funcionamiento durante un año o más, puede ahorrar dinero reservando nodos de cómputo para un período de uno o tres años.
- Las instantáneas son copias de seguridad puntuales de un clúster. Estas copias de seguridad están habilitadas de forma predeterminada con un período de retención de 1 día. El período máximo de retención es de 35 días.
- Redshift también puede replicar de forma asincrónica sus instantáneas en una región diferente si lo desea.
- Un clúster de Redshift de alta disponibilidad requeriría 3 copias de sus datos. Una copia estaría activa en Redshift y las otras estarían en espera en S3.
- Redshift puede tener hasta 128 nodos de cómputo en un clúster de varios nodos. El nodo líder siempre gestiona las conexiones de los clientes y transmite las consultas a los nodos de cálculo que almacenan los datos reales y realizan las consultas.
- Redshift puede lograr eficiencia a pesar de las muchas partes y piezas de su arquitectura mediante el uso de compresión en columnas de almacenes de datos que contienen datos similares. Además, Redshift no requiere índices o vistas materializadas, lo que significa que puede tener un tamaño relativamente más pequeño en comparación con una base de datos OLTP que contiene la misma cantidad de información. Finalmente, al cargar datos en una tabla de Redshift, Redshift tomará automáticamente una muestra de los datos y seleccionará el esquema de compresión más apropiado.
- Redshift también viene con procesamiento paralelo masivo (MPP) para aprovechar todos los nodos en su clúster de múltiples nodos. Esto se hace distribuyendo uniformemente los datos y la carga de consultas en todos los nodos. Debido a esto, el escalado horizontal aún conserva un gran rendimiento.
- Redshift se cifra en tránsito mediante SSL y en reposo mediante AES-256. De forma predeterminada, Redshift administrará todas las claves, pero también puede hacerlo a través de AWS CloudHSM o AWS KMS.
- Redshift se factura por:
  - Compute Node Hours (horas totales que sus nodos no líderes dedicaron a consultar datos)
  - Copias de seguridad
  - Transferencia de datos dentro de una VPC (pero no fuera de ella)
- Redshift no es multi-AZ, si desea multi-AZ, deberá activar un clúster separado que ingiera la misma entrada. También puede restaurar instantáneas manualmente a una nueva zona de disponibilidad en caso de una interrupción.
- Cuando aprovisiona un clúster de Amazon Redshift, está bloqueado de forma predeterminada para que nadie tenga acceso a él. Para otorgar acceso entrante a otros usuarios a un clúster de Amazon Redshift, asocie el clúster con un grupo de seguridad.
- Amazon Redshift proporciona almacenamiento gratuito para instantáneas que equivale a la capacidad de almacenamiento de su clúster hasta que lo elimine. Después de alcanzar el límite de almacenamiento de instantáneas gratuitas, se le cobrará por cualquier almacenamiento adicional a la tarifa normal. Debido a esto, debe evaluar cuántos días necesita para mantener las instantáneas automatizadas y configurar su período de retención en consecuencia, y eliminar las instantáneas manuales que ya no necesite.
- Independientemente de si habilita las instantáneas automáticas, puede tomar una instantánea manual cuando lo desee. Amazon Redshift nunca eliminará automáticamente una instantánea manual. Las instantáneas manuales se conservan incluso después de eliminar su clúster de Redshift. Debido a que las instantáneas manuales acumulan cargos por almacenamiento, es importante que las elimine manualmente si ya no las necesita

## Redshift Spectrum:
- Amazon Redshift Spectrum se utiliza para ejecutar consultas en exabytes de datos no estructurados en Amazon S3, sin necesidad de carga ni ETL.
- Las consultas de Redshift Spectrum emplean un paralelismo masivo para ejecutarse muy rápido contra grandes conjuntos de datos. Gran parte del procesamiento ocurre en la capa Redshift Spectrum y la mayoría de los datos permanecen en Amazon S3.
- Las consultas de Redshift Spectrum utilizan mucho menos de la capacidad de procesamiento de su clúster que otras consultas.
- El clúster y los archivos de datos en Amazon S3 deben estar en la misma región de AWS.
- Las tablas externas de S3 son de solo lectura. No puede realizar operaciones de inserción, actualización o eliminación en tablas externas.

## Redshift Enhanced VPC Routing:
- Cuando utiliza el enrutamiento de VPC mejorado de Amazon Redshift, Redshift fuerza todo el tráfico (como el tráfico de COPIA y DESCARGA) entre su clúster y sus repositorios de datos a través de su Amazon VPC.
- Si el enrutamiento de VPC mejorado no está habilitado, Amazon Redshift enruta el tráfico a través de Internet, incluido el tráfico a otros servicios dentro de la red de AWS.
- Al utilizar el enrutamiento de VPC mejorado, puede utilizar funciones de VPC estándar, como grupos de seguridad de VPC, listas de control de acceso a la red (ACL), puntos de enlace de VPC, políticas de puntos de enlace de VPC, puertas de enlace de Internet y servidores del sistema de nombres de dominio (DNS).

  
## ElastiCache

### Simplificanod ElastiCache:
El servicio ElastiCache facilita la implementación, el funcionamiento y el escalado de un caché en memoria en la nube. Le ayuda a mejorar el rendimiento de sus bases de datos existentes al recuperar datos de almacenes de datos en memoria de alto rendimiento y baja latencia.

### Detalles Clave de ElastiCache:
- El servicio es excelente para mejorar el rendimiento de las aplicaciones web al permitirle recibir información localmente en lugar de depender únicamente de bases de datos relativamente distantes.
- Amazon ElastiCache ofrece Redis y Memcached completamente administrados para las aplicaciones más exigentes que requieren tiempos de respuesta inferiores a milisegundos.
- Para los datos que no cambian con frecuencia y que se solicitan con frecuencia, tiene mucho sentido almacenar en caché dichos datos en lugar de consultarlos desde la base de datos.
- Las configuraciones comunes que mejoran el rendimiento de la base de datos incluyen la introducción de réplicas de lectura de una base de datos primaria y la inserción de una capa de almacenamiento en caché en la arquitectura de almacenamiento.
- MemcacheD es para propósitos simples de almacenamiento en caché con escalado horizontal y rendimiento de subprocesos múltiples, pero si necesita más complejidad para su entorno de almacenamiento en caché, elija Redis.
- Una comparación más entre MemcacheD y Redis para ElastiCache:
![Screen Shot 2020-06-18 at 8 18 34 PM](https://user-images.githubusercontent.com/13093517/85083820-edc1b480-b1a0-11ea-88b0-15f90bd60282.png)

- Otra ventaja de usar ElastiCache es que al almacenar en caché los resultados de la consulta, paga el precio de la consulta de la base de datos solo una vez sin tener que volver a ejecutar la consulta a menos que los datos cambien.
- Amazon ElastiCache puede escalar horizontalmente, escalar hacia adentro y escalar hacia arriba para cumplir con las demandas fluctuantes de las aplicaciones. El escalado de memoria y escritura es compatible con la fragmentación. Las réplicas proporcionan escalado de lectura.

## Route53

### Simplificando Route53:
Amazon Route 53 es un servicio de Sistema de nombres de dominio (DNS) escalable y de alta disponibilidad. Puede usar Route 53 para realizar tres funciones principales en cualquier combinación: registro de dominio, enrutamiento DNS y verificación de estado.

### Detalles Clave de Route53:
- El DNS se utiliza para mapear nombres de dominio legibles por humanos en una dirección de protocolo de Internet de manera similar a como las guías telefónicas mapean nombres de empresas con números de teléfono.
- AWS tiene su propio registrador de dominios.
- Cuando compra un nombre de dominio, cada dirección DNS comienza con un registro SOA (Inicio de autoridad). El registro SOA almacena información sobre el nombre del servidor que inició la transferencia de propiedad, el administrador que ahora usará el dominio, los metadatos actuales disponibles y el número predeterminado de segundos o TTL.
- Los hosts de dominio de nivel superior (.org, .com, .uk, etc.) utilizan registros NS, o registros del servidor de nombres, para dirigir el tráfico a los servidores de contenido. Los servidores DNS de contenido contienen los registros DNS autorizados.
- Los navegadores hablan con los dominios de nivel superior cada vez que se les consulta y encuentran un nombre de dominio que no reconocen.
  1. Los navegadores solicitarán los registros DNS autorizados asociados con el dominio.
  2. Debido a que el dominio de nivel superior contiene registros NS, el TLD puede, a su vez, consultar a los servidores de nombres por su propia SOA.
  3. Dentro de la SOA, estará la información solicitada.
  4. Una vez recopilada esta información, será devuelta al navegador original solicitándola.
- En resumen: Navegador -> TLD -> NS -> SOA -> Registro DNS. La canalización se invierte cuando se encuentra el registro DNS correcto.
- Los servidores de nombres autorizados almacenan información de registro de DNS, generalmente un proveedor de alojamiento de DNS o un registrador de dominios como GoDaddy que ofrece alojamiento y registro de DNS.
- Hay una multitud de registros DNS para Route53. Éstos son algunos de los más comunes:
  - **Registros A**: estos son el tipo fundamental de registro DNS. La "A" en los registros A significa "dirección". Estos registros son utilizados por una computadora para emparejar directamente un nombre de dominio con una dirección IP. Tanto IPv4 como IPv6 son compatibles con "AAAA" en referencia a la versión de IPv6. ** A: URL -> IPv4 ** y ** AAA: URL -> IPv6 **.
  - **Registros CName**: también denominado nombre canónico. Estos registros se utilizan para convertir un nombre de dominio en otro nombre de dominio. Por ejemplo, el dominio de la versión móvil de un sitio web puede ser un CName del dominio de la versión del navegador de ese mismo sitio web en lugar de una dirección IP separada. Esto permitiría a los usuarios móviles que visitan el sitio y recibir la versión móvil. ** CNAME: URL -> URL **.
  - **Registros de alias**: estos registros se utilizan para asignar sus dominios a los recursos de AWS, como equilibradores de carga, puntos finales de CDN y depósitos de S3. Los registros de alias funcionan de manera similar a CNames en el sentido de que asigna un dominio a otro. Sin embargo, la diferencia clave es que al apuntar su registro de Alias ​​a un servicio en lugar de un nombre de dominio, tiene la capacidad de cambiar libremente sus nombres de dominio si es necesario y no tiene que preocuparse por qué registros podrían asignarse a él. Los registros de alias le brindan una funcionalidad dinámica. ** Alias: URL -> Recurso de AWS **.
  - **Registros PTR**: estos registros son lo opuesto a un registro A. Los registros PTR asignan una IP a un dominio y se utilizan en búsquedas DNS inversas como una forma de obtener el nombre de dominio de una dirección IP. ** PTR: IPv4 -> URL **.
- Otra diferencia importante entre los registros CNames y Alias ​​es que no se puede usar un CName para el nombre de dominio simple (el registro vértice en toda su configuración de DNS / el registro primario que se usará). Los CNames siempre deben ser registros secundarios que se puedan asignar a otro registro secundario o al registro vértice. El primario siempre debe ser de tipo Alias ​​o A Record para que funcione.
- Debido a la naturaleza dinámica de los registros de Alias, a menudo se recomiendan para la mayoría de los casos de uso y deben usarse cuando sea posible.
- TTL es la longitud que un registro DNS se almacena en caché en los servidores de resolución o en la propia caché del usuario para que se pueda recuperar una asignación más reciente de IP a dominio. El tiempo de vida se mide en segundos y cuanto más bajo es el TTL, más rápido se propagan los cambios de DNS a través de Internet. La mayoría de los proveedores, por ejemplo, tienen un TTL que dura 48 horas.
- Puede crear verificaciones de estado para enviarle una Notificación simple si surge algún problema con la configuración de su DNS.
- Además, las verificaciones de estado de Route53 se pueden utilizar para cualquier punto final de AWS al que se pueda acceder a través de Internet. Esto lo convierte en una opción ideal para monitorear el estado de sus puntos de enlace de AWS.

### Políticas de Enrutamiento en Route53:
- Cuando crea un registro, elige una política de enrutamiento, que determina cómo Amazon Route 53 responde a las consultas de DNS. Las políticas de enrutamiento disponibles son:
  - Enrutamiento simple
  - Enrutamiento ponderado
  - Enrutamiento basado en latencia
  - Enrutamiento de conmutación por error
  - Enrutamiento por geolocalización
  - Enrutamiento de proximidad geográfica
  - Enrutamiento de respuestas multivalor
- **Enrutamiento simple** se usa cuando solo necesita un solo registro en su DNS con una o más direcciones IP detrás del registro en caso de que desee equilibrar la carga. Si especifica varios valores en una política de enrutamiento simple, Route53 devuelve una IP aleatoria de las opciones disponibles.
- **Enrutamiento ponderado** se utiliza cuando desea dividir su tráfico según los pesos asignados. Por ejemplo, si desea que el 80% de su tráfico vaya a una zona de disponibilidad y el resto a otra, utilice el enrutamiento ponderado. Esta política es muy útil para probar cambios de características y, debido a las características de división del tráfico, puede funcionar como un medio para realizar implementaciones azul-verde. Al crear enrutamiento ponderado, debe especificar un nuevo registro para cada dirección IP. No puede agrupar las distintas direcciones IP en un registro como con el enrutamiento simple.
- **Enrutamiento basado en latencia**, como su nombre lo indica, se basa en configurar el enrutamiento en función de cuál sería la latencia más baja para un usuario determinado. Para utilizar el enrutamiento basado en latencia, debe crear un conjunto de registros de recursos de latencia en la misma región que el recurso EC2 o ELB correspondiente que recibe el tráfico. Cuando Route53 recibe una consulta para su sitio, selecciona el conjunto de registros que le da al usuario la velocidad más rápida. Al crear enrutamiento basado en latencia, debe especificar un nuevo registro para cada IP.
- **Enrutamiento de conmutación por error** se utiliza cuando desea configurar una configuración de conmutación por error activa-pasiva. Route53 supervisará el estado de su primario para que pueda realizar una conmutación por error cuando sea necesario. También puede configurar manualmente verificaciones de estado para monitorear todos los puntos finales si desea reglas más detalladas.
- **Enrutamiento de geolocalización** le permite elegir dónde se enviará el tráfico en función de la ubicación geográfica de sus usuarios.
- **Enrutamiento por proximidad geográfica** le permite elegir a dónde se enviará el tráfico en función de la ubicación geográfica de sus usuarios *y* sus recursos. Puede elegir enrutar más o menos tráfico en función de un peso específico que se conoce como sesgo. Este sesgo expande o reduce la disponibilidad de una región geográfica, lo que facilita el cambio de tráfico de los recursos en una ubicación a los recursos en otra. Para utilizar este método de enrutamiento, debe habilitar el flujo de tráfico de Route53. Si desea controlar el tráfico global, utilice el enrutamiento de proximidad geográfica. Si desea que el tráfico permanezca en una región local, utilice el enrutamiento de geolocalización.
- **El enrutamiento de valores múltiples** es prácticamente lo mismo que el enrutamiento simple, pero el enrutamiento de valores múltiples le permite realizar comprobaciones de estado en cada conjunto de registros. Esto asegura entonces que solo se devolverá aleatoriamente una IP en buen estado en lugar de cualquier IP.

## Elastic Load Balancers (ELB)

### Simplificando ELB:
Elastic Load Balancing distribuye automáticamente el tráfico de aplicaciones entrante a través de múltiples destinos, como instancias Amazon EC2, contenedores Docker, direcciones IP y funciones Lambda. Puede manejar la carga variable del tráfico de su aplicación en una única zona de disponibilidad o en varias zonas de disponibilidad. Elastic Load Balancing ofrece tres tipos de balanceadores de carga que cuentan con alta disponibilidad, escalado automático y seguridad sólida necesaria para que sus aplicaciones sean tolerantes a fallas.

### Detalles Clave de ELB:
- Los equilibradores de carga pueden estar conectados a Internet o ser internos de la aplicación.
- Para enrutar el tráfico del dominio a un balanceador de carga ELB, use Amazon Route 53 para crear un registro de alias que apunte a su balanceador de carga. Es preferible un registro de Alias ​​a un CName, pero ambos pueden funcionar.
- Los ELB no tienen direcciones IPv4 predefinidas; debe resolverlos con DNS en su lugar. Su equilibrador de carga nunca tendrá su propia IP de forma predeterminada, pero puede crear una IP estática para un equilibrador de carga de red porque los LB de red son para fines de alto rendimiento.
- Las instancias detrás del ELB se informan como "InService" u "OutOfService".
Cuando una instancia EC2 detrás de un ELB falla en una verificación de estado, el ELB deja de enviar tráfico a esa instancia.
- Una configuración de doble pila para un equilibrador de carga significa equilibrio de carga sobre IPv4 e IPv6
- En AWS, hay tres tipos de LB:
  - LB de aplicación
  - LB de red
  - LB clásicos.
- **Application LBs** son los más adecuados para el tráfico HTTP (S) y equilibran la carga en la capa 7. Son lo suficientemente inteligentes como para ser conscientes de las aplicaciones y los Application Load Balancers también admiten enrutamiento basado en ruta, enrutamiento basado en host y soporte para aplicaciones en contenedores. Por ejemplo, si cambia el idioma de su navegador web al francés, una aplicación LB tiene visibilidad de los metadatos que recibe de su navegador, que contienen detalles sobre el idioma que utiliza. Para optimizar su experiencia de navegación, lo dirigirá a los servidores en francés en el backend detrás del LB. También puede crear un enrutamiento de solicitudes avanzado, moviendo el tráfico a servidores específicos según las reglas que usted mismo establezca para casos específicos.
- **Network LBs** son los más adecuados para el tráfico TCP donde se requiere rendimiento y equilibran la carga en la capa 4. Son capaces de administrar millones de solicitudes por segundo mientras mantienen una latencia extremadamente baja.
- **LB clásicos** son el producto ELB heredado y se equilibran en HTTP (S) o TCP, pero no en ambos. A pesar de que son los LB más antiguos, aún admiten funciones como sesiones fijas y encabezados X-Fordered-For.
- Si necesita una gestión de aplicaciones flexible y la terminación de TLS, debe utilizar Application Load Balancer. Si se necesita un rendimiento extremo y una IP estática para su aplicación, entonces debe usar Network Load Balancer. Si su aplicación está construida dentro de la red EC2 Classic, entonces debe usar Classic Load Balancer.
- El ciclo de vida de una solicitud para ver un sitio web detrás de un ELB:
  1. El navegador solicita la dirección IP del equilibrador de carga de DNS.
  2. DNS proporciona la IP.
  3. Con la IP a mano, su navegador realiza una solicitud HTTP para una página HTML desde Load Balancer.
  4. Los dispositivos perimetrales de AWS comprueban y verifican su solicitud antes de pasarla al LB.
  5. El LB encuentra un servidor web activo para pasar la solicitud HTTP.
  6. El servidor web devuelve el archivo HTML solicitado.
  7. El navegador recibe el archivo HTML que solicitó y muestra la representación gráfica del mismo en la pantalla.
- Los balanceadores de carga son un servicio regional. No equilibran la carga en diferentes regiones. Debe proporcionar un nuevo ELB en cada región en la que opere.
- Si tu aplicación deja de responder, recibirás un error 504 cuando accedas a tu balanceador de carga. Esto significa que la aplicación tiene problemas y el error podría haber aparecido en el balanceador de carga desde los servicios detrás de ella. No significa necesariamente que haya un problema con el LB en sí.

### Características Avanzadas de ELB:
- Para habilitar la resolución de DNS IPv6, debe crear un segundo registro de recursos DNS para que el registro ** ALIAS AAAA ** se resuelva en el balanceador de carga junto con el registro IPv4.
- El encabezado X-Fordered-For, a través del Protocolo Proxy, es simplemente la idea de que los balanceadores de carga reenvíen la dirección IP del solicitante junto con la solicitud real de información de los servidores detrás de los LB. Normalmente, los servidores detrás de los LB solo ven que la IP que lo envía pertenece al Load Balancer. Por lo general, no tienen idea del verdadero origen de la solicitud, ya que solo conocen la computadora (el LB) que les pide que hagan algo. Pero a veces es posible que deseemos enrutar la IP original a los servidores backend para casos de uso específicos y que se ignore la dirección IP de LB. El encabezado X-Fordered-For lo hace posible.
- Sticky Sessions vincula a un usuario determinado a una instancia específica durante la duración de su estancia en la aplicación o el sitio web. Esto significa que todas sus interacciones con la aplicación se dirigirán al mismo host cada vez. Si necesita un disco local para que su aplicación funcione, las sesiones fijas son excelentes, ya que se garantiza a los usuarios un acceso constante al mismo almacenamiento efímero en una instancia en particular. La desventaja de las sesiones pegajosas es que, si se realizan incorrectamente, pueden frustrar el propósito del equilibrio de carga. Todo el tráfico podría, hipotéticamente, estar vinculado a la misma instancia en lugar de distribuirse uniformemente.
- Los patrones de ruta crean un oyente con reglas para reenviar solicitudes basadas en la ruta URL establecida dentro de esas solicitudes de usuario. Este método, conocido como enrutamiento basado en rutas, asegura que el tráfico se pueda dirigir específicamente a múltiples servicios de back-end.
Por ejemplo, con Path Patterns puede enrutar solicitudes generales a un grupo objetivo y solicitudes para renderizar imágenes a otro grupo objetivo. Por lo tanto, la URL "www.example.com/" se reenviará a un servidor que se utiliza para contenido general, mientras que "www.example.com/photos" se reenviará a otro servidor que procesa imágenes.


### ELB Cross Zone Load Balancing:
- El equilibrio de carga entre zonas garantiza una distribución uniforme entre las zonas de disponibilidad en lugar de solo dentro de una única zona de disponibilidad.
- Si el equilibrio de carga entre zonas está deshabilitado, cada nodo del equilibrador de carga distribuye las solicitudes de manera uniforme entre las instancias registradas solo en su zona de disponibilidad.
- El equilibrio de carga entre zonas reduce la necesidad de mantener un número equivalente de instancias en cada zona de disponibilidad habilitada y mejora la capacidad de su aplicación para manejar la pérdida de una o más instancias.
- Sin embargo, se recomienda mantener aproximadamente un número equivalente de instancias en cada zona de disponibilidad habilitada para lograr una mayor tolerancia a errores.
- Para entornos donde los clientes almacenan en caché las búsquedas de DNS, las solicitudes entrantes pueden favorecer una de las zonas de disponibilidad. Al utilizar el equilibrio de carga entre zonas, este desequilibrio en la carga de solicitudes se distribuye en todas las instancias disponibles en la región.

### ELB Security:
- ELB admite terminación SSL / TLS y HTTPS. Se desea la terminación en el equilibrador de carga porque el descifrado consume muchos recursos y CPU. Poner la carga del descifrado en el equilibrador de carga permite que las instancias EC2 gasten su poder de procesamiento en tareas de aplicaciones, lo que ayuda a mejorar el rendimiento general.
- Los Elastic Load Balancers (junto con CloudFront) admiten Perfect Forward Secrecy. Ésta es una función que proporciona salvaguardias adicionales contra la escucha clandestina de datos cifrados en tránsito mediante el uso de una clave de sesión exclusivamente aleatoria. Esto se hace asegurándose de que la parte en uso de un sistema de cifrado cambie automática y frecuentemente las claves que utiliza para cifrar y descifrar la información. Entonces, si esta última clave se ve comprometida, solo expondrá una pequeña parte de los datos recientes del usuario.
- Los Classic Load Balancers no admiten la indicación de nombre de servidor (SNI). SNI permite al servidor (el LB en este caso) alojar de forma segura varios certificados TLS para varios sitios, todo bajo una única dirección IP (el registro de alias o el registro de CName en este caso). Para permitir SNI, debe usar un balanceador de carga de aplicaciones en su lugar o usarlo con una distribución web de CloudFront.

## Auto Scaling

### Simplificando Auto Scaling:
AWS Auto Scaling le permite crear planes de escalado que automatizan la forma en que los grupos de diferentes recursos responden a los cambios en la demanda. Puede optimizar la disponibilidad, los costos o un equilibrio de ambos. AWS Auto Scaling crea automáticamente todas las políticas de escalado y establece objetivos según sus preferencias.

### Detalles Clave de Auto Scaling:
- Auto Scaling es un beneficio importante de las economías de escala de la nube, por lo que si alguna vez tiene un requisito para escalar, piense automáticamente en utilizar el servicio Auto Scaling.
- Auto Scaling tiene tres componentes:
  - **Grupos**: Estos son componentes lógicos. Un grupo de servidores web de instancias EC2, un grupo de bases de datos de instancias RDS, etc.
  - **Plantillas de configuración**: los grupos utilizan una plantilla para configurar y lanzar nuevas instancias para adaptarse mejor a las necesidades de escalado. Puede especificar información para las nuevas instancias, como la AMI que se utilizará, el tipo de instancia, los grupos de seguridad, los dispositivos de bloqueo para asociarlos con las instancias y más.
  - **Opciones de escala**: Las opciones de escala ofrecen varias formas de escalar sus grupos de Auto Scaling. Puede basar el desencadenante de escalado en la ocurrencia de una condición específica o en una programación.
- La siguiente imagen resalta el estado de un grupo de escala automática. Los cuadrados naranjas representan instancias activas. Los cuadrados punteados representan instancias potenciales que pueden y se activarán cuando sea necesario. El número mínimo, el número máximo y la capacidad deseada de instancias son completamente configurables.

![Screen Shot 2020-06-19 at 4 44 18 PM](https://user-images.githubusercontent.com/13093517/85178368-50bc5580-b24c-11ea-9acc-45ca5742e889.png)

- Cuando utiliza Auto Scaling, sus aplicaciones obtienen los siguientes beneficios:
  - **Mejor tolerancia a fallas**: Auto Scaling puede detectar cuando una instancia no está en buen estado, finalizarla y lanzar una instancia para reemplazarla. También puede configurar Auto Scaling para utilizar varias zonas de disponibilidad. Si una zona de disponibilidad deja de estar disponible, Auto Scaling puede lanzar instancias en otra para compensar.
  - **Mejor disponibilidad**: Auto Scaling puede ayudarlo a garantizar que su aplicación siempre tenga la cantidad adecuada de capacidad para manejar las demandas de tráfico actuales.
- Cuando se trata de escalar realmente sus grupos de instancias, el servicio de Auto Scaling es flexible y se puede hacer de varias maneras:
  - Auto Scaling puede escalar en función de la demanda de sus instancias. Esta opción automatiza el proceso de escalado al especificar ciertos umbrales que, cuando se alcanzan, activarán el escalado. Esta es la implementación más popular de Auto Scaling.
  - Auto Scaling puede garantizar el número actual de instancias en todo momento. Esta opción siempre mantendrá la cantidad de servidores que desea ejecutar incluso cuando fallan.
  - Auto Scaling puede escalar solo con intervención manual. Si desea controlar todo el escalado usted mismo, esta opción tiene sentido.
  - Auto Scaling puede escalar según un cronograma. Si puede predecir de manera confiable los picos de tráfico, esta opción tiene sentido.
  - Auto Scaling basado en el escalado predictivo. Esta opción permite a AWS AI / ML obtener más información sobre su entorno para predecir el mejor momento para escalar tanto para mejorar el rendimiento como para ahorrar costos.
- Al mantener la instancia en ejecución actual, Auto Scaling realizará verificaciones de estado ocasionales en las instancias en ejecución para garantizar que todas estén en buen estado. Cuando el servicio detecta que una instancia no está en buen estado, terminará esa instancia y luego mostrará una nueva en línea.
- Al diseñar HA para su Auto Scaling, utilice varias AZ y varias regiones siempre que pueda.
- Auto Scaling le permite suspender y luego reanudar uno o más de los procesos de Auto Scaling en su grupo de Auto Scaling. Esto puede resultar muy útil cuando desee investigar un problema en su aplicación sin activar el proceso de Auto Scaling al realizar cambios.
- Puede especificar su configuración de lanzamiento con varios grupos de Auto Scaling. Sin embargo, solo puede especificar una configuración de inicio para un grupo de Auto Scaling a la vez.
- No puede modificar una configuración de lanzamiento después de haberla creado. Si desea cambiar la configuración de lanzamiento para un grupo de Auto Scaling, debe crear una nueva configuración de lanzamiento y actualizar su grupo de Auto Scaling para heredar esta nueva configuración de lanzamiento.

### Auto Scaling Default Termination Policy:
- La política de terminación predeterminada para un grupo de Auto Scaling es terminar automáticamente una instancia detenida, por lo que, a menos que lo haya configurado para hacer lo contrario, detener una instancia resultará en la terminación independientemente de si desea que eso suceda o no. Se activará una nueva instancia en su lugar.
- La política de terminación predeterminada evitará las instancias que usted le indique en caso de que algunos servidores estén ejecutando aplicaciones o sistemas críticos. Estos servidores críticos están protegidos contra el "escalado", que es solo el proceso de eliminación de instancias que se consideran superfluas para los requisitos.
- La política de terminación predeterminada está diseñada para ayudar a garantizar que la arquitectura de su red abarque las zonas de disponibilidad de manera uniforme. Con la política de terminación predeterminada, el comportamiento del grupo de Auto Scaling es el siguiente:
  - Si hay instancias en varias zonas de disponibilidad, finalizará una instancia de la zona de disponibilidad con la mayor cantidad de instancias. Si hay más de una zona de disponibilidad con el mismo número máximo de instancias, elegirá la zona de disponibilidad donde las instancias utilizan la configuración de lanzamiento más antigua.
  - A continuación, determinará qué instancias desprotegidas en la zona de disponibilidad seleccionada utilizan la configuración de lanzamiento más antigua. Si existe una de esas instancias, la terminará.
  - Si hay varias instancias para finalizar, determinará qué instancias desprotegidas están más cerca de la siguiente hora de facturación. (Esto le ayuda a maximizar el uso de sus instancias EC2 y administrar sus costos de uso de Amazon EC2). Si hay algunas instancias que coinciden con este criterio, se cancelarán.
- Este diagrama de flujo puede proporcionar más claridad sobre cómo la política de Auto Scaling predeterminada decide qué instancias eliminar:

![Screen Shot 2020-06-19 at 5 19 02 PM](https://user-images.githubusercontent.com/13093517/85180270-0093c200-b251-11ea-97e3-ed9a80ee5d65.png)

## Auto Scaling Cooldown Period:
- El período de enfriamiento es una configuración configurable para su grupo de Auto Scaling que ayuda a garantizar que no inicie o finalice instancias adicionales antes de que la actividad de escalado anterior entre en vigor.
- Después de que Auto Scaling Group escala utilizando una política, espera a que se complete el período de enfriamiento antes de reanudar más actividades de escalado si es necesario.
- El período de espera predeterminado es de 300 segundos, pero se puede modificar.

## Virtual Private Cloud (VPC)

### Simplificando VPC:
VPC le permite aprovisionar una sección aislada lógicamente de la nube de AWS donde puede lanzar servicios y sistemas dentro de una red virtual que defina. Al tener la opción de seleccionar qué recursos de AWS son públicos y cuáles no, VPC proporciona un control mucho más granular sobre la seguridad.

### Detalles Clave de VPC:
- Puede pensar en VPC como su propio centro de datos virtual en la nube. Tienes el control total de tu propia red; incluyendo el rango de IP, la creación de subredes (subredes), la configuración de tablas de rutas y las pasarelas de red utilizadas.
- A continuación, puede lanzar instancias EC2 en una subred de su elección, seleccionar las direcciones IP que estarán disponibles para las instancias, asignarles grupos de seguridad y crear listas de control de acceso a la red (NACL) para las propias subredes como protección adicional.
- Esta personalización le brinda mucho más control para especificar y personalizar la configuración de su infraestructura. Por ejemplo, puede tener una subred pública para que sus servidores web reciban tráfico HTTP y luego una subred privada diferente para su servidor de base de datos donde el acceso a Internet está prohibido.
- Utiliza subredes para utilizar de manera eficiente redes que tienen una gran cantidad de hosts
- Las VPC vienen con una defensa en profundidad por diseño. Desde la subred (NACL) hasta el servidor individual (grupo de seguridad) y más allá de la propia aplicación (prácticas de codificación segura), puede configurar varios niveles de protección contra usuarios y programas maliciosos.
- La VPC predeterminada para su entorno de AWS permite que todas las subredes tengan una ruta de salida a Internet, lo que significa que todas las subredes de la VPC predeterminada son accesibles a través de Internet. La configuración predeterminada le permite implementar instancias inmediatamente y cada instancia EC2 tendrá una dirección IP pública y privada.
- Hay una VPC predeterminada por región. Sin embargo, puede tener tantas VPC personalizadas como desee y todas son privadas de forma predeterminada.
- Cuando crea una VPC personalizada, no se crean nuevas subredes de forma predeterminada. Debes crearlos por separado. Lo mismo ocurre con una puerta de enlace a Internet. Si desea que su VPC tenga acceso a Internet, también debe crear la puerta de enlace para que todo el mundo pueda acceder a la red públicamente.
- Debido a esto, cuando crea un IGW, inicialmente estará en un estado separado. Deberá asignarlo manualmente a la VPC personalizada.
- Sin embargo, una vez que crea una VPC personalizada, lo siguiente se crea de forma predeterminada:
  - una tabla de ruta
  - una NACL
  - un grupo de seguridad
  
![Screen Shot 2020-06-19 at 6 26 37 PM](https://user-images.githubusercontent.com/13093517/85183681-8cf6b280-b25a-11ea-8b54-d1e54ba754a6.png)

- Estos componentes, que se explicarán con mayor profundidad en caso de que aún no se conozcan, en realidad corresponden al flujo de tráfico de cómo llegarán los datos a sus instancias. Ya sea que el tráfico se origine desde fuera de la VPC o desde dentro de ella, primero debe pasar por la tabla de rutas a través del enrutador para saber dónde está el destino deseado. Una vez que se conoce, el tráfico pasa a través de la seguridad a nivel de subred como se describe en la NACL. Si la NACL considera que el tráfico es válido, el tráfico pasa a la seguridad de nivel de instancia como lo describe el grupo de seguridad. Si el tráfico no se ha reducido en este punto, solo entonces llegará a su instancia prevista.
- El asistente de VPC es una herramienta automatizada que resulta útil para crear VPC personalizadas.
- Puedes tener tu VPC en hardware dedicado para que la red sea exclusiva a nivel físico, pero esta opción es sumamente cara. Afortunadamente, si una VPC está en un alojamiento dedicado, siempre se puede volver a cambiar al alojamiento predeterminado. Esto se puede hacer a través de la AWS CLI, SDK o API. Sin embargo, los hosts existentes en el hardware dedicado primero deben estar en un estado "detenido".
- Cuando crea una VPC, debe asignarle un bloque CIDR IPv4. Este bloque CIDR es un rango de direcciones IPv4 privadas que sus instancias heredarán cuando las cree.
- El rango de IP de una VPC predeterminada es siempre **/ 16**.
- Al crear rangos de IP para sus subredes, el bloque CIDR **/ 16** es el rango más grande de IP que se puede usar. Esto se debe a que las subredes deben tener tantas IP o menos IP que la VPC a la que pertenece. Un bloque CIDR **/ 28** es el rango de IP más pequeño disponible para subredes.
- Con CIDR en general, **/ 32** denota una sola dirección IP y **/ 0** se refiere a toda la red. Cuanto más alto sea el CIDR, más estrecho será el rango de IP.
- La información anterior sobre las direcciones IP se refiere tanto a las direcciones IP públicas como a las privadas.
- Las direcciones IP privadas no son accesibles a través de Internet y, en su lugar, se utilizan para la comunicación entre las instancias en su VPC. Cuando lanza una instancia en una VPC, se asigna una dirección IP privada del rango de direcciones IPv4 de la subred a la interfaz de red predeterminada (eth0) de la instancia.
- Esto significa que todas las instancias dentro de una VPC tienen una IP privada, pero solo aquellas seleccionadas para comunicarse con el mundo externo tienen una IP pública.
- Cuando lanza una instancia en una subred que tiene acceso público a través de una puerta de enlace de Internet, se crean tanto una dirección IP pública como una dirección IP privada. En cambio, la dirección IP pública se asigna a la interfaz de red principal (eth0) que se crea para la instancia. Externamente, la dirección IP pública se asigna a la dirección IP privada a través de la traducción de direcciones de red (NAT).
- Opcionalmente, puede asociar un bloque CIDR IPv6 con su VPC y subredes, y asignar direcciones IPv6 de ese bloque a los recursos de su VPC.
- Las VPC son específicas de la región y puede tener hasta cinco VPC por región.
- De forma predeterminada, AWS está configurado para tener una subred en cada zona de disponibilidad de las regiones donde se encuentra su aplicación.
- En una arquitectura de VPC ideal y segura, se inician los servidores web o los equilibradores de carga elásticos en la subred pública y los servidores de base de datos en la subred privada.
- A continuación, se muestra un ejemplo de una aplicación hipotética detrás de una configuración típica de VPC:

![Screen Shot 2020-06-21 at 6 20 09 PM](https://user-images.githubusercontent.com/13093517/85236432-dd514a00-b3eb-11ea-9ab0-1b5acf4b8894.png)

- Los grupos de seguridad pueden abarcar subredes, pero no VPC. ICMP garantiza que las instancias de un grupo de seguridad puedan hacer ping a otras en un grupo de seguridad diferente. Es compatible con IPv4 e IPv6.

### VPC Subnets:
- Si una red tiene una gran cantidad de hosts sin subdivisiones agrupadas lógicamente, administrar muchos hosts puede ser un trabajo tedioso. Por lo tanto, utiliza subredes para dividir una red y facilitar la administración.
- Cuando cree una subred, asegúrese de especificar en qué VPC desea colocarla. Puede asignar rangos de IPv4 e IPv6 a sus subredes.
- Los principales beneficios de las subredes:
  - Mejoran el flujo de tráfico y, por lo tanto, la velocidad y el rendimiento de toda la red. Una puerta de enlace de Internet (IGW) que recibe un paquete y verifica a cuál de las 5 subredes se debe entregar el paquete es mucho más rápido que verificar 100 instancias individualmente. Y si el destino de un paquete está dentro de la subred desde donde se origina, el tráfico permanece dentro de la subred y no satura el resto de la VPC.
  - Las subredes funcionan como grupos lógicos para colocar sus entidades dentro de. Hace que sea mucho más fácil configurar recursos similares como un grupo en lugar de para cada instancia individual.
- Amazon siempre reserva cinco direcciones IP dentro de una subred. Las primeras cuatro direcciones IP y la última dirección IP de cada bloque CIDR de subred siempre no estarán disponibles para su uso.

### Network Access Control Lists:
- Las listas de control de acceso a la red (o NACL) son como grupos de seguridad pero para subredes en lugar de instancias. La principal diferencia entre los grupos de seguridad y las NACL es que los grupos de seguridad tienen * estado *, lo que significa que puede realizar tanto reglas de autorización como denegación que pueden ser divergentes, dependiendo de si el tráfico es entrante o saliente, para esa regla.
- La siguiente tabla destaca las diferencias entre NACL y subredes.

| NACL | Security Group |
| ------------- | ------------- |
| Opera a nivel de subred | Opera a nivel de instancia | 
| Soporta permitir reglas y denegar reglas  | Los soportes solo permiten reglas |
| Es stateless: el tráfico de retorno debe estar explícitamente permitido por las reglas  |  Es stateful: El tráfico de retorno se permite automáticamente, independientemente de las reglas. |
| Procesamos las reglas en orden, comenzando con la regla con el número más bajo, al decidir si permitir el tráfico.  |  Evaluamos todas las reglas antes de decidir si permitimos el tráfico. |
| Se aplica automáticamente a todas las instancias de las subredes con las que está asociado (por lo tanto, proporciona una capa adicional de defensa si las reglas del grupo de seguridad son demasiado permisivas). |  Se aplica a una instancia solo si alguien especifica el grupo de seguridad al iniciar la instancia, o asocia el grupo de seguridad con la instancia más adelante. |
- Debido a que las NACL no tienen estado, también debe asegurarse de que existan reglas de salida junto con las reglas de entrada para que la entrada y la salida puedan fluir sin problemas.
- La NACL predeterminada que viene con una nueva VPC tiene una regla predeterminada para permitir todas las entradas y salidas. Esto significa que existe, pero no hace nada ya que todo el tráfico lo atraviesa libremente.
- Sin embargo, cuando crea una nueva NACL (en lugar de usar la predeterminada que viene con la VPC), las reglas predeterminadas negarán todas las entradas y salidas.
- Si crea una nueva NACL, debe asociar las subredes que desee a ella manualmente para que puedan heredar el conjunto de reglas de la NACL. Si no asigna explícitamente una subred a una NACL, AWS la asociará con su NACL predeterminada.
- Las NACL se evalúan antes que los grupos de seguridad y usted bloquea las direcciones IP maliciosas con NACL, no con grupos de seguridad.
- Una subred solo puede seguir las reglas enumeradas por una NACL a la vez. Sin embargo, una NACL puede describir las reglas para cualquier número de subredes. Las reglas entrarán en vigor de inmediato.
- Las reglas de ACL de red se evalúan por número de regla, de menor a mayor, y se ejecutan inmediatamente cuando se encuentra una regla de permitir / denegar coincidente. Debido a esto, el orden importa con los números de sus reglas.
- Cuanto menor sea el número de una regla en la lista, más antigüedad tendrá esa regla. Enumere sus reglas en consecuencia.

- Si está utilizando NAT Gateway junto con su NACL, debe garantizar la disponibilidad del rango de puertos efímeros de NAT Gateway dentro de las reglas de su NACL. Debido a que el tráfico de la puerta de enlace NAT puede aparecer en cualquiera de los puertos del rango mientras dure su conexión, debe asegurarse de que todos los puertos posibles estén contabilizados y abiertos.
- NACL puede tener un pequeño impacto en la forma en que las instancias EC2 en una subred privada se comunicarán con cualquier servicio, incluidos los puntos finales de VPC.


### NAT Instances vs. NAT Gateways:
- La conexión de una puerta de enlace de Internet a una VPC permite que las instancias con IP públicas accedan directamente a Internet. NAT hace algo similar, sin embargo, es para instancias que no tienen una IP pública. Sirve como un paso intermedio que permite a las instancias privadas enmascarar primero su propia IP privada como la IP pública de NAT antes de acceder a Internet.
- Desea que sus instancias privadas accedan a Internet para que puedan tener actualizaciones de software normales. NAT impide cualquier iniciación de una conexión de Internet.
- **Instance NAT** son instancias EC2 individuales que realizan la función de proporcionar subredes privadas un medio para acceder de forma segura a Internet.
- Debido a que son instancias individuales, la alta disponibilidad no es una función incorporada y pueden convertirse en un punto de estrangulamiento en su VPC. No son tolerantes a fallas y sirven como un solo punto de falla. Si bien es posible utilizar grupos de escalado automático, scripts para automatizar la conmutación por error, etc. para evitar cuellos de botella, es mucho mejor utilizar NAT Gateway como alternativa para una solución escalable.
- **NAT Gateway** es un servicio administrado que se compone de varias instancias vinculadas entre sí dentro de una zona de disponibilidad para lograr HA de forma predeterminada.
- Para lograr más HA y una arquitectura independiente de zona, cree una puerta de enlace NAT para cada zona de disponibilidad y configure su enrutamiento para garantizar que los recursos usen la puerta de enlace NAT en su zona de disponibilidad correspondiente.
- Las instancias NAT están en desuso, pero aún se pueden usar. Las puertas de enlace NAT son el medio preferido para lograr la traducción de direcciones de red.
- No es necesario aplicar parches a las puertas de enlace NAT, ya que AWS administra el servicio. Sin embargo, es necesario aplicar parches a las instancias NAT porque son solo instancias EC2 individuales.
- Debido a que la comunicación siempre debe iniciarse desde sus instancias privadas, necesita una regla de ruta para enrutar el tráfico desde una subred privada a su puerta de enlace NAT.
- Su instancia de NAT / puerta de enlace tendrá que vivir en una subred pública, ya que su subred pública es la subred configurada para tener acceso a Internet.
- Al crear instancias NAT, es importante recordar que las instancias EC2 tienen verificaciones de origen / destino de forma predeterminada. Lo que hacen estas comprobaciones es garantizar que cualquier tráfico que encuentre debe ser generado por la instancia o ser el destinatario previsto de ese tráfico. De lo contrario, el tráfico se descarta porque la instancia EC2 no es ni el origen ni el destino.
- Entonces, debido a que las instancias NAT actúan como una especie de proxy, * debe * deshabilitar las comprobaciones de origen / destino al pensar en una instancia NAT.

### Bastion Hosts:
- Los hosts bastión son equipos con fines especiales diseñados y configurados para resistir ataques. Este servidor generalmente ejecuta un solo programa y se elimina más allá de este propósito para reducir los vectores de ataque.
- El propósito de Bastion Hosts es acceder de forma remota a las instancias detrás de la subred privada para fines de administración del sistema sin exponer el host a través de una puerta de enlace de Internet.
- La mejor manera de implementar un Host de bastión es crear una pequeña instancia EC2 que solo tenga una regla de grupo de seguridad para una única dirección IP. Esto garantiza la máxima seguridad.
- Está perfectamente bien usar una instancia pequeña en lugar de una grande porque la instancia solo se usará como un servidor de salto que conecta diferentes servidores entre sí.
- Si va a utilizar RDP o SSH en las instancias de su subred privada, utilice un Host de bastión. Si va a proporcionar tráfico de Internet a las instancias de su subred privada, use un NAT.
- Al igual que las puertas de enlace NAT y las instancias NAT, los hosts bastión viven dentro de una subred pública.
- Hay AMI de Host Bastion prefabricadas.

### Route Tables:
- Las tablas de enrutamiento se utilizan para garantizar que las subredes puedan comunicarse entre sí y que el tráfico sepa adónde dirigirse.
- Cada subred que crea se asocia automáticamente con la tabla de enrutamiento principal para la VPC.
- Puede tener varias tablas de enrutamiento. Si no desea que su nueva subred se asocie con la tabla de enrutamiento predeterminada, debe especificar que desea que se asocie con una tabla de enrutamiento diferente.
- Debido a este comportamiento predeterminado, existe un posible problema de seguridad a tener en cuenta: si la tabla de enrutamiento predeterminada es pública, las nuevas subredes asociadas a ella también serán públicas.
- La mejor práctica es asegurarse de que la tabla de enrutamiento predeterminada a la que se asocian nuevas subredes sea privada.
- Esto significa que se asegura de que no haya una ruta a Internet para la tabla de rutas predeterminada. Luego, puede crear una tabla de enrutamiento personalizada que sea pública en su lugar. Las nuevas subredes no tendrán automáticamente una ruta de salida a Internet. Si desea que una nueva subred sea de acceso público, simplemente puede asociarla con la tabla de enrutamiento personalizada.
- Las tablas de enrutamiento se pueden configurar para acceder a los puntos finales (servicios públicos a los que se accede de forma privada) y no solo a Internet.

### Internet Gateway:
- Si la puerta de enlace de Internet no está conectada a la VPC, que es el requisito previo para que se pueda acceder a las instancias desde Internet, naturalmente no se podrá acceder a las instancias de su VPC.
- Si desea que toda su VPC permanezca privada (y no solo algunas subredes), no adjunte un IGW.
- Cuando se asigna una dirección IP pública a una instancia EC2, Internet Gateway la registra efectivamente como un punto final público válido. Sin embargo, cada instancia solo conoce su IP privada y no su IP pública. Solo el IGW conoce las IP públicas que pertenecen a las instancias.
- Cuando una instancia EC2 inicia una conexión a la Internet pública, la solicitud se envía utilizando la IP pública como fuente, aunque la instancia no sepa nada al respecto. Esto funciona porque el IGW realiza su propia traducción NAT donde las direcciones IP privadas se asignan a las direcciones IP públicas y viceversa para el tráfico que entra y sale de la VPC.
- Entonces, cuando el tráfico de Internet está destinado al punto final de IP pública de una instancia, el IGW lo recibe y reenvía el tráfico a la instancia EC2 utilizando su IP privada interna.
- Solo puede tener un IGW por VPC.
- **Resumiendo**: IGW conecta *su VPC con Internet*.

### Virtual Private Networks (VPNs):
- Las VPC también pueden servir como puente entre su centro de datos corporativo y la nube de AWS. Con una red privada virtual (VPN) de VPC, su VPC se convierte en una extensión de su entorno local.
- Naturalmente, las instancias que lanza en su VPC no pueden comunicarse con sus propios servidores locales. Puede permitir el acceso primero:
  - adjuntar una puerta de enlace privada virtual a la VPC
  - crear una tabla de ruta personalizada para la conexión
  - actualización de las reglas de su grupo de seguridad para permitir el tráfico desde la conexión
  - crear la propia conexión VPN gestionada.
- Para activar la conexión VPN, también debe definir un recurso de puerta de enlace del cliente en AWS, que proporciona información de AWS sobre su dispositivo de puerta de enlace del cliente. Y debe configurar una dirección IP enrutable a Internet de la interfaz externa de la puerta de enlace del cliente.
- Una puerta de enlace de cliente es un dispositivo físico o una aplicación de software en el lado local de la conexión VPN.
- Aunque el término "conexión VPN" es un concepto general, una conexión VPN para AWS siempre se refiere a la conexión entre su VPC y su propia red. AWS admite conexiones VPN de seguridad de protocolo de Internet (IPsec).
- El siguiente diagrama ilustra una sola conexión VPN.

![Screen Shot 2020-06-21 at 6 13 17 PM](https://user-images.githubusercontent.com/13093517/85236301-e857aa80-b3ea-11ea-9de9-08d150d34864.png)

- La VPC anterior tiene una puerta de enlace privada virtual adjunta (nota: no una puerta de enlace de Internet) y hay una red remota que incluye una puerta de enlace de cliente que debe configurar para habilitar la conexión VPN. Configure el enrutamiento para que cualquier tráfico de la VPC destinado a su red se enrute a la puerta de enlace privada virtual.
- **Resumiendo**: las VPN conectan su *infraestructura local con su VPC* a través de Internet.


### AWS DirectConnect:
- Direct Connect es un servicio de AWS que establece una conexión de red dedicada entre sus instalaciones y AWS. Puede crear esta conectividad privada para reducir los costos de red, aumentar el ancho de banda y brindar una experiencia de red más consistente en comparación con las conexiones regulares basadas en Internet.
- El caso de uso de Direct Connect son cargas de trabajo de alto rendimiento o si necesita una conexión estable o confiable
- VPN se conecta a su local a través de Internet y DirectConnect se conecta a su local a través de un túnel privado.
- Los pasos para configurar una conexión AWS DirectConnect:
  1. Cree una interfaz virtual en la consola DirectConnect. Esta es una interfaz virtual pública.
  2. Vaya a la consola de VPC y luego a las conexiones VPN. Cree una puerta de enlace de clientes para su local.
  3. Cree una puerta de enlace privada virtual y conéctela al entorno de VPC deseado.
  4. Seleccione Conexiones VPN y cree una nueva conexión VPN. Seleccione tanto la puerta de enlace del cliente como la puerta de enlace privada virtual.
  5. Una vez que la conexión VPN esté disponible, configure la VPN en la puerta de enlace del cliente o en el firewall local.
- El flujo de datos hacia AWS a través de DirectConnect tiene el siguiente aspecto: enrutador local -> línea dedicada -> su propia jaula / DMZ -> línea de conexión cruzada -> enrutador AWS Direct Connect -> red troncal de AWS -> nube de AWS
- **Redumiento**: DirectConnect conecta su *infraestructura local con su VPC* a través de un túnel no público.


### VPC Endpoints:
- Los puntos de enlace de VPC garantizan que pueda conectar su VPC a los servicios de AWS admitidos sin necesidad de una puerta de enlace de Internet, un dispositivo NAT, una conexión VPN o AWS Direct Connect. El tráfico entre su VPC y otros servicios de AWS permanece dentro del ecosistema de Amazon y estos Endpoints son dispositivos virtuales que son HA y sin restricciones de ancho de banda.
- Estos funcionan básicamente al adjuntar un ENI a una instancia EC2 que puede comunicarse fácilmente con una amplia gama de servicios de AWS.
- ** Los puntos finales de puerta de enlace ** se basan en la creación de entradas en una tabla de enrutamiento y apuntarlas a puntos finales privados utilizados para S3 o DynamoDB. Los puntos finales de puerta de enlace son principalmente solo un objetivo que usted establece.
- ** Los puntos de enlace de la interfaz ** utilizan AWS PrivateLink y tienen una dirección IP privada, por lo que son su propia entidad y no solo un objetivo en una tabla de rutas. Debido a esto, cuestan $ .01 / hora. Los extremos de Gateway son gratuitos, ya que son solo una nueva ruta para configurar.
- Interface Endpoint aprovisiona una interfaz de red elástica o ENI (piense en una tarjeta de red) dentro de su VPC. Sirven como entrada y salida para el tráfico que entra y sale de otro servicio de AWS compatible. Utiliza un registro DNS para dirigir su tráfico a la dirección IP privada de la interfaz. Gateway Endpoint utiliza el prefijo de ruta en su tabla de rutas para dirigir el tráfico destinado a S3 o DynamoDB al Gateway Endpoint (piense en 0.0.0.0/0 -> igw).
- Para proteger su punto final de interfaz, utilice Grupos de seguridad. Pero para proteger el punto final de la puerta de enlace, utilice las políticas de punto final de VPC.
- **Resumiendo**: los puntos de enlace de VPC conectan su *VPC con los servicios de AWS* a través de un túnel no público.

### AWS PrivateLink:
- AWS PrivateLink simplifica la seguridad de los datos compartidos con aplicaciones basadas en la nube al eliminar la exposición de los datos a la Internet pública. AWS PrivateLink proporciona conectividad privada entre diferentes VPC, servicios de AWS y aplicaciones locales, de forma segura en la red de Amazon.
- Es similar al servicio AWS Direct Connect en el sentido de que establece conexiones privadas a la nube de AWS, excepto que Direct Connect vincula entornos locales a AWS. PrivateLink, por otro lado, protege el tráfico de los entornos de VPC que ya están en AWS.
- Esto es útil porque los diferentes servicios de AWS a menudo se comunican entre sí a través de Internet. Si no desea ese comportamiento y, en cambio, desea que los servicios de AWS solo se comuniquen dentro de la red de AWS, use AWS PrivateLink. Al no atravesar Internet, PrivateLink reduce la exposición a vectores de amenazas como la fuerza bruta y los ataques distribuidos de denegación de servicio.
- PrivateLink le permite publicar un "punto final" con el que otros pueden conectarse desde su propia VPC. Es similar a un punto final de VPC normal, pero en lugar de conectarse a un servicio de AWS, las personas pueden conectarse a su punto final.
- Además, querrá utilizar grupos de seguridad y conectividad IP privada para que sus servicios funcionen como si estuvieran alojados directamente en su red privada.
- Recuerde que AWS PrivateLink se aplica a las aplicaciones / servicios que se comunican entre sí dentro de la red de AWS. Para que las VPC se comuniquen entre sí dentro de la red de AWS, use VPC Peering.
- **Resumiendo**: AWS PrivateLink conecta sus *servicios de AWS con otros servicios de AWS* a través de un túnel no público.

### VPC Peering:
- El emparejamiento de VPC le permite conectar una VPC con otra a través de una ruta de red directa utilizando las IP privadas que pertenecen a ambas. Con el intercambio de tráfico de VPC, las instancias de diferentes VPC se comportan como si estuvieran en la misma red.
- Puede crear una interconexión de VPC entre sus propias VPC, independientemente de si están en la misma región o no, y con una VPC en una cuenta de AWS completamente diferente.
- El emparejamiento de VPC generalmente se realiza de tal manera que hay una VPC central que se empareja con otras. Solo la VPC central puede comunicarse con las otras VPC.
- No puede realizar emparejamiento transitivo para VPC no centrales. Las VPC no centrales no pueden pasar por la VPC central para llegar a otra VPC no central. Debe configurar un nuevo portal entre nodos no centrales si necesita que se comuniquen entre sí.
- El siguiente diagrama resalta la idea anterior. VPC B es libre de comunicarse con VPC A con VPC Peering habilitado entre ambos. Sin embargo, la VPC B no puede continuar la conversación con la VPC C. Solo la VPC A puede comunicarse con la VPC C.

![Screen Shot 2020-06-19 at 6 12 02 PM](https://user-images.githubusercontent.com/13093517/85183188-e1009780-b258-11ea-8a81-ad0612cd1053.png)

- Vale la pena saber qué configuraciones de intercambio de tráfico de VPC no son compatibles:
  - Bloques CIDR superpuestos
  - Peering transitivo
  - Enrutamiento de borde a borde a través de una puerta de enlace o dispositivo de conexión (conexión VPN, puerta de enlace de Internet, conexión AWS Direct Connect, etc.)
- Puede mirar a través de regiones, pero no puede tener una subred extendida en varias zonas de disponibilidad. Sin embargo, puede tener varias subredes en la misma zona de disponibilidad.
- **Resumiendo**: VPC Peering conecta su *VPC a otra VPC* a través de un túnel no público.

### VPC Flow Logs:
- VPC Flow Logs es una función que captura la información de IP de todo el tráfico que entra y sale de su VPC. Los datos del registro de flujo se envían a un depósito de S3 o CloudWatch donde puede ver, recuperar y manipular estos datos.
- Puede capturar el flujo de tráfico en varias etapas a lo largo de su recorrido:
  - Tráfico que entra y sale de la VPC (como en IGW)
  - Tráfico que entra y sale de la subred
  - Tráfico que entra y sale de la interfaz de red de la instancia EC2 (eth0, eth1, etc.)
- Los registros de flujo de VPS capturan los metadatos del paquete y no el contenido del paquete. Cosas como:
  - La IP de origen
  - La IP de destino
  - El tamaño del paquete
  - Todo lo que pueda observarse desde fuera del paquete.
- Sus registros de flujo se pueden configurar para registrar tráfico válido, tráfico no válido o ambos
- Puede hacer que los registros de flujo se obtengan de una VPC diferente en comparación con la VPC donde se encuentran sus registros de flujo. Sin embargo, la otra VPC debe interconectarse a través de VPC Peering y en su cuenta a través de AWS Organizations.
- Puede personalizar sus registros etiquetándolos.
- Una vez que crea un registro de flujo, no puede cambiar su configuración. Debes hacer uno nuevo.
- No todo el tráfico IP se supervisa en los registros de flujo de VPC. La siguiente es una lista de cosas que los registros de flujo ignoran:
  - Solicitudes de consulta de metadatos de instancia
  - Tráfico DHCP
  - Solicitudes de consulta al servidor DNS de AWS
  
  ### AWS Global Accelerator:
- AWS Global Accelerator acelera la conectividad para mejorar el rendimiento y la disponibilidad para los usuarios. Global Accelerator se encuentra en la parte superior de la red troncal de AWS y dirige el tráfico a puntos finales óptimos en todo el mundo. De forma predeterminada, Global Accelerator le proporciona dos direcciones IP estáticas que puede utilizar.
- Global Accelerator ayuda a reducir la cantidad de saltos para llegar a sus recursos de AWS. Sus usuarios solo necesitan llegar a una ubicación de borde y, una vez allí, todo seguirá siendo interno a la red global de AWS. Normalmente, se necesitan muchas redes para llegar a la aplicación en su totalidad y las rutas hacia y desde la aplicación pueden variar. Con cada salto, existe un riesgo relacionado con la seguridad o con la falla.

![Screen Shot 2020-06-21 at 5 50 02 PM](https://user-images.githubusercontent.com/13093517/85235996-aa0cbc00-b3e7-11ea-9e85-039f0ba6e770.png)

- En resumen, Global Accelerator es una canalización rápida y confiable entre el usuario y la aplicación.
- Es como ir de viaje (tráfico web) y detenerse para pedir direcciones en partes posiblemente inseguras de la ciudad (se visitan varias redes que pueden aumentar los riesgos de seguridad) en lugar de tener un GPS (acelerador global) que lo lleva directamente a donde se encuentra quiere ir (punto final) sin tener que hacer paradas innecesarias.
- Puede confundirse con Cloudfront, pero CloudFront es un caché para contenido que proviene de un servidor de origen distante.
- Mientras que CloudFront simplemente almacena en caché el contenido estático en la ubicación de AWS Point Of Presence (POP) más cercana, el acelerador global utilizará el mismo Amazon POP para aceptar las solicitudes iniciales y enrutarlas directamente a los servicios.
- El enrutamiento basado en latencia de Route53 también puede parecer similar a Global Accelerator, pero Route 53 es simplemente para ayudar a elegir qué región usará el usuario. Route53 no tiene nada que ver con proporcionar una ruta de red rápida.
- Global Accelerator también proporciona una rápida conmutación por error regional.

## Simple Queuing Service (SQS)

### Simplificando SQS:
SQS es un servicio basado en web que le da acceso a una cola de mensajes que puede usarse para almacenar mensajes mientras espera que una cola los procese. Ayuda en el desacoplamiento de sistemas y el escalado horizontal de los recursos de AWS.

### Detalles Clave de SQS:
- El objetivo de SQS es desacoplar el trabajo entre sistemas. De esta manera, los servicios descendentes de un sistema pueden realizar el trabajo cuando están listos para hacerlo en lugar de cuando los servicios ascendentes les proporcionan datos.
- En un entorno hipotético de AWS que se ejecuta sin SQS, la *Aplicación A* pasaría los datos de la *Aplicación B* independientemente de si la Aplicación B estaba lista para recibir la información. Sin embargo, con SQS, hay un paso intermedio en el que los datos se almacenan temporalmente en un búfer. Espera allí hasta que la Aplicación B extrae los datos almacenados temporalmente. SQS no es un servicio basado en push, por lo que es necesario que SQS funcione en conjunto con otro servicio que lo consulta en busca de información.
- Hay dos tipos de colas SQS; **estándar** y **FIFO**. Las colas estándar pueden recibirse desordenadas en función del tamaño del mensaje o de cualquier otro modo que las colas SQS decidan optimizar. Las colas FIFO garantizan que el orden de los mensajes que entraron en la cola es el mismo que el orden de los mensajes que la abandonan.
- Las colas SQS estándar garantizan que un mensaje se entregue al menos una vez y, debido a esto, en ocasiones es posible que un mensaje se entregue más de una vez debido a la arquitectura asincrónica y altamente distribuida. Con las colas estándar, tiene un número casi ilimitado de transacciones por segundo.
- Las colas FIFO SQS garantizan el procesamiento de una sola vez y están limitadas a 300 transacciones por segundo.
- Los mensajes en la cola se pueden guardar desde un minuto hasta 14 días y el período de retención predeterminado es de 4 días.
- Los tiempos de espera de visibilidad en SQS son el mecanismo por el cual los mensajes marcados para entrega desde la cola reciben un marco de tiempo para que un lector los reciba en su totalidad. Esto se hace haciéndolos invisibles temporalmente para otros lectores. Si el mensaje no se procesa por completo dentro del límite de tiempo, el mensaje vuelve a ser visible. Esta es otra forma de duplicar los mensajes. Si desea reducir la posibilidad de duplicación, aumente el tiempo de espera de visibilidad.
- El tiempo de espera de visibilidad máximo es de 12 horas.
- Recuerde siempre que los mensajes en la cola de SQS seguirán existiendo incluso después de que la instancia EC2 los haya procesado, hasta que elimine ese mensaje. Debe asegurarse de eliminar el mensaje después del procesamiento para evitar que el mensaje se reciba y se procese nuevamente una vez que expire el tiempo de espera de visibilidad.
- Una cola SQS puede contener un número ilimitado de mensajes.
- No puede establecer una prioridad para los elementos individuales en la cola de SQS. Si la prioridad de la mensajería es importante, cree dos colas SQS independientes. Las instancias EC2 pueden sondear primero las colas SQS para el mensaje de prioridad y, una vez completadas, los mensajes de la segunda cola pueden procesarse a continuación.

### SQS Polling:
- El sondeo es el medio por el cual consulta a SQS por mensajes o trabajo. Amazon SQS proporciona sondeos cortos y largos para recibir mensajes de una cola. De forma predeterminada, las colas utilizan un sondeo corto.
- **Sondeo largo de SQS**: esta técnica de sondeo solo regresará de la cola una vez que haya un mensaje, independientemente de si la cola está actualmente llena o vacía. De esta manera, el lector debe esperar a que se establezca el tiempo de espera o que finalmente llegue un mensaje. El sondeo largo de SQS no devuelve una respuesta hasta que llega un mensaje a la cola, lo que reduce el costo general con el tiempo.
- **Sondeo corto de SQS**: esta técnica de sondeo regresará inmediatamente con un mensaje que ya está almacenado en la cola o con las manos vacías.
- ReceiveMessageWaitTimeSeconds es el atributo de cola que determina si está utilizando sondeo corto o largo. De forma predeterminada, su valor es cero, lo que significa que está utilizando un sondeo corto. Si se establece en un valor mayor que cero, entonces es un sondeo largo.
- Cada vez que sondea la cola, incurres en un cargo. Por lo tanto, es importante decidir cuidadosamente una estrategia de sondeo que se adapte a su caso de uso.

## Simple Workflow Service (SWF)

### Simplificando SWF:
SWF es un servicio web que facilita la coordinación del trabajo entre componentes de aplicaciones distribuidas. SWF tiene una variedad de casos de uso que incluyen procesamiento de medios, backend de aplicaciones web, flujos de trabajo de procesos comerciales y canalizaciones analíticas.

### Detalles Clave de SWF:
- SWF es una forma de coordinar tareas entre la aplicación y las personas. Es un servicio que combina flujos de trabajo digitales y orientados a las personas.
- Un ejemplo de un flujo de trabajo orientado a las personas es el proceso en el que los trabajadores del almacén de Amazon encuentran y envían su artículo como parte de su pedido de Amazon.
- SWF proporciona una API orientada a tareas y garantiza que una tarea se asigne solo una vez y nunca se duplique. Usando nuevamente a los trabajadores del almacén de Amazon como ejemplo, esto tendría sentido. Amazon no querría enviarte el mismo artículo dos veces, ya que perderían dinero.
- La canalización SWF se compone de tres aplicaciones de trabajador diferentes que ayudan a completar un trabajo:
  - Los actores SWF son trabajadores que activan el inicio de un flujo de trabajo.
  - Los SWF Deciders son trabajadores que controlan el flujo del flujo de trabajo una vez que se ha iniciado.
  - SWF Activity Workers son los trabajadores que realmente llevan a cabo la tarea hasta su finalización.
- Con SWF, las ejecuciones del flujo de trabajo pueden durar hasta un año en comparación con el período de retención máximo de 14 días para SQS.

## Simple Notification Service (SNS)

### Simplificando SNS:
Simple Notification Service es un servicio de mensajería basado en empuje que proporciona un método altamente escalable, flexible y rentable para publicar mensajes personalizados a los suscriptores que desean estar informados sobre un tema determinado.

### Detalles Clave de SNS:
- SNS se utiliza principalmente para enviar alarmas o alertas.
- SNS proporciona temas para mensajería de muchos a muchos de alto rendimiento, basada en push.
- Con los temas de Amazon SNS, sus sistemas de publicadores pueden distribuir mensajes a una gran cantidad de puntos de enlace de suscriptores para el procesamiento paralelo, incluidas las colas de Amazon SQS, las funciones de AWS Lambda y los webhooks HTTP / S. Además, SNS se puede utilizar para distribuir notificaciones a los usuarios finales mediante dispositivos móviles, SMS y correo electrónico.
- Puede enviar estas notificaciones push a dispositivos Apple, Google, Fire OS y Windows.
- SNS le permite agrupar a varios destinatarios mediante temas. Un tema es un punto de acceso que permite a los destinatarios suscribirse dinámicamente para obtener copias idénticas de la misma notificación.
- Un tema puede admitir entregas a varios tipos de terminales. Cuando publica en un tema, SNS formatea apropiadamente copias de ese mensaje para enviar a cualquier tipo de dispositivo.
- Para evitar que se pierdan los mensajes, los mensajes se almacenan de forma redundante en varias zonas de disponibilidad.
- No hay sondeos largos o cortos involucrados con SNS debido al envío instantáneo de mensajes
- SNS tiene una entrega de mensajes flexible a través de múltiples protocolos de transporte y tiene una API simple.

## Kinesis 

### Simplificando Kinesis:
Amazon Kinesis facilita la recopilación, el procesamiento y el análisis de datos de transmisión en tiempo real para que pueda obtener información oportuna y reaccionar rápidamente a la nueva información. Con Amazon Kinesis, puede ingerir datos en tiempo real como video, audio, registros de aplicaciones, flujos de clics de sitios web y datos de telemetría de IoT para aprendizaje automático, análisis y otras aplicaciones. Amazon Kinesis le permite procesar y analizar los datos a medida que llegan y responder al instante en lugar de tener que esperar hasta que se recopilen todos sus datos antes de que pueda comenzar el procesamiento.

### Detalles Clave de Kinesis:
- Amazon Kinesis facilita la carga y el análisis de los grandes volúmenes de datos que ingresan a AWS.
- Kinesis se utiliza para procesar flujos de datos en tiempo real (datos que se generan continuamente) desde dispositivos que envían datos constantemente a AWS para que dichos datos se puedan recopilar y analizar.
- Es un servicio completamente administrado que se escala automáticamente para igualar el rendimiento de sus datos y no requiere una administración continua. También puede agrupar, comprimir y cifrar los datos antes de cargarlos, lo que minimiza la cantidad de almacenamiento utilizado en el destino y aumenta la seguridad.
- Hay tres tipos diferentes de Kinesis:
  - Corrientes de Kinesis
    - Kinesis Streams funciona donde los productores de datos transmiten sus datos a Kinesis Streams, que puede retener los datos que ingresan desde un día hasta 7 días. Una vez dentro
      Kinesis Streams, los datos están contenidos en fragmentos.
    - Kinesis Streams puede capturar y almacenar continuamente terabytes de datos por hora de cientos de miles de fuentes, como flujos de clics de sitios web, finanzas
      transacciones, feeds de redes sociales, registros de TI y eventos de seguimiento de ubicación. Por ejemplo: solicitudes de compra de una gran tienda en línea como Amazon, precios de las acciones, Netflix
      contenido, contenido de Twitch, datos de juegos en línea, posicionamiento e indicaciones de Uber, etc.
      
- Kinesis Firehose
    - Amazon Kinesis Firehose es la forma más sencilla de cargar datos de transmisión en almacenes de datos y herramientas de análisis. Cuando los datos se transmiten a Kinesis Firehose, no hay
      almacenamiento persistente allí para aferrarse a él. Los datos deben analizarse a medida que ingresan, por lo que es opcional tener funciones Lambda dentro de su Kinesis Firehose. Una vez
      procesado, envía los datos a otro lugar.
    - Kinesis Firehose puede capturar, transformar y cargar datos de transmisión en Amazon S3, Amazon Redshift, Amazon Elasticsearch Service y Splunk, lo que permite casi tiempo real
      análisis con las herramientas y los paneles de inteligencia empresarial existentes que ya utiliza en la actualidad.
      
- Análisis de Kinesis
    - Kinesis Analytics funciona con Kinesis Streams y Kinesis Firehose y puede analizar datos sobre la marcha. Los datos de Kinesis Analytics también se envían a otro lugar una vez
      está terminado de procesar. Analiza sus datos dentro del propio servicio de Kinesis.

- Las claves de partición se utilizan con Kinesis para que pueda organizar los datos por fragmentos. De esta manera, a la entrada de un dispositivo en particular se le puede asignar una clave que limitará su destino a un fragmento específico.
- Las claves de partición son útiles si desea mantener el orden dentro de su fragmento.
- Los consumidores, o las instancias EC2 que leen de Kinesis Streams, pueden ingresar a los fragmentos para analizar lo que hay allí. Una vez que terminan de analizar o analizar los datos, los consumidores pueden pasar los datos a varios lugares para su almacenamiento, como una base de datos o un S3.
- La capacidad total de una transmisión de Kinesis es la suma de los datos dentro de sus fragmentos constituyentes.
- Siempre puede aumentar la capacidad de escritura asignada a su tabla de particiones.

## Lambda

### Simplificando Lambda:
AWS Lambda le permite ejecutar código sin aprovisionar ni administrar servidores. Solo paga por el tiempo de cálculo que consume. Con Lambda, puede ejecutar código para prácticamente cualquier tipo de aplicación o servicio de backend, todo sin necesidad de administración. Carga su código y Lambda se encarga de todo lo necesario para ejecutar y escalar su código con alta disponibilidad. Puede configurar su código para que se active automáticamente desde otros servicios de AWS o para que lo llamen directamente desde cualquier aplicación web o móvil.

### Detalles Clave de Lambda:
- Lambda es un servicio informático en el que carga su código como una función y AWS proporciona los detalles necesarios debajo de la función para que la función se ejecute correctamente.
- AWS Lambda es la última capa de abstracción. Usted solo se preocupa por el código, AWS hace todo lo demás.
- Lambda es compatible con Go, Python, C #, PowerShell, Node.js y Java
- Cada función de Lambda se asigna a una solicitud. Lambda escala horizontalmente automáticamente.
- El precio de Lambda depende del número de solicitudes y el primer millón es gratuito. Cada millón después es $ 0,20.
- Lambda también tiene un precio según el tiempo de ejecución de su código, redondeado a los 100 MB más cercanos y la cantidad de memoria que asigna su código.
- Lambda funciona a nivel mundial.
- Las funciones Lambda pueden activar otras funciones Lambda.
- Puede utilizar Lambda como un servicio impulsado por eventos que se ejecuta en función de los cambios en su ecosistema de AWS.
- También puede utilizar Lambda como controlador en respuesta a eventos HTTP a través de llamadas a la API a través de AWS SDK o API Gateway.

![Screen Shot 2020-06-30 at 9 19 33 AM](https://user-images.githubusercontent.com/13093517/86130894-df35a000-bab2-11ea-9908-acbe3e8d4824.png)

- Cuando crea o actualiza funciones de Lambda que utilizan variables de entorno, AWS Lambda las cifra mediante AWS Key Management Service. Cuando se invoca su función Lambda, esos valores se descifran y se ponen a disposición del código Lambda.
- La primera vez que crea o actualiza funciones de Lambda que utilizan variables de entorno en una región, se crea automáticamente una clave de servicio predeterminada dentro de AWS KMS. Esta clave se utiliza para cifrar variables de entorno. Sin embargo, si desea utilizar ayudantes de cifrado y utilizar KMS para cifrar las variables de entorno después de crear su función Lambda, debe crear su propia clave de AWS KMS y elegirla en lugar de la clave predeterminada.
- Para permitir que su función Lambda acceda a los recursos dentro de una VPC privada, debe proporcionar información de configuración adicional específica de la VPC que incluya los ID de subred de VPC y los ID de grupo de seguridad. AWS Lambda utiliza esta información para configurar interfaces de red elásticas (ENI) que permiten que su función se conecte de forma segura a otros recursos dentro de una VPC privada.

- AWS X-Ray le permite depurar su función Lambda en caso de comportamiento inesperado.

### Lambda@Edge:
- Puede utilizar Lambda @ Edge para permitir que sus funciones de Lambda personalicen el contenido que ofrece CloudFront.
- Agrega capacidad de cómputo a sus ubicaciones de borde de CloudFront y le permite ejecutar las funciones en ubicaciones de AWS más cercanas a los espectadores de su aplicación. Las funciones se ejecutan en respuesta a eventos de CloudFront, sin aprovisionar ni administrar servidores. Puede utilizar las funciones de Lambda para cambiar las solicitudes y respuestas de CloudFront en los siguientes puntos:
  - Después de que CloudFront recibe una solicitud de un espectador (solicitud de espectador)
  - Antes de que CloudFront reenvíe la solicitud al origen (solicitud de origen)
  - Después de que CloudFront recibe la respuesta del origen (respuesta del origen)
  - Antes de que CloudFront envíe la respuesta al espectador (respuesta del espectador)
  
![Screen Shot 2020-06-30 at 9 27 48 AM](https://user-images.githubusercontent.com/13093517/86131713-fc1ea300-bab3-11ea-8190-1d13128bee92.png)

- Usaría Lambda @ Edge para simplificar y reducir la infraestructura de origen.

## API Gateway

### Simplificando API Gateway:
API Gateway es un servicio completamente administrado para desarrolladores que facilita la creación, publicación, administración y seguridad de API completas. Con unos pocos clics en la Consola de administración de AWS, puede crear una API que actúa como una "puerta de entrada" para que las aplicaciones accedan a los datos, la lógica empresarial o la funcionalidad de sus servicios de back-end, como las cargas de trabajo que se ejecutan en EC2). en AWS Lambda o cualquier aplicación web.

### Detalles Clave de API Gateway:
- Amazon API Gateway maneja todas las tareas involucradas en la aceptación y procesamiento de hasta cientos de miles de llamadas API simultáneas, incluida la administración del tráfico, la autorización y el control de acceso, el monitoreo y la administración de versiones de API.
- Amazon API Gateway no tiene tarifas mínimas ni costos de inicio. Solo paga por las llamadas a la API que recibe y la cantidad de datos transferidos.
- API Gateway hace lo siguiente para sus API:
  - Expone puntos finales HTTP (S) para una funcionalidad RESTful
  - Utiliza la funcionalidad sin servidor para conectarse a Lambda y DynamoDB
  - Puede enviar cada punto final de la API a un objetivo diferente
  - Funciona de forma económica y eficiente.
  - Se escala fácilmente y sin esfuerzo.
  - Puede acelerar las solicitudes para prevenir ataques
  - Seguimiento y control del uso a través de una clave API
  - Puede ser controlado por versión
  - Puede conectarse a CloudWatch para monitoreo y observabilidad
- Dado que API Gateway puede funcionar con AWS Lambda, puede ejecutar sus API y código sin necesidad de mantener servidores.
- Amazon API Gateway proporciona limitación en varios niveles, incluido el global y mediante una llamada de servicio.
  - En software, un proceso de aceleración, o un controlador de aceleración, como a veces se le llama, es un proceso responsable de regular la velocidad a la que se realiza el procesamiento de la aplicación, ya sea de forma estática o dinámica.
  - Se pueden establecer límites de regulación para velocidades y ráfagas estándar. Por ejemplo, los propietarios de API pueden establecer un límite de frecuencia de 1000 solicitudes por segundo para un método específico en sus API REST y también configurar Amazon API Gateway para manejar una ráfaga de 2000 solicitudes por segundo durante unos segundos.
  - Amazon API Gateway rastrea la cantidad de solicitudes por segundo. Cualquier solicitud que supere el límite recibirá una respuesta HTTP 429. Los SDK de cliente generados por Amazon API Gateway reintentan las llamadas automáticamente cuando se encuentran con esta respuesta.
- Puede agregar almacenamiento en caché a las llamadas a la API aprovisionando una caché de Amazon API Gateway y especificando su tamaño en gigabytes. La caché se aprovisiona para una etapa específica de sus API. Esto mejora el rendimiento y reduce el tráfico enviado a su back-end. La configuración de caché le permite controlar la forma en que se crea la clave de caché y el tiempo de vida (TTL) de los datos almacenados para cada método. Amazon API Gateway también expone API de administración que lo ayudan a invalidar la caché para cada etapa.
- Puede habilitar el almacenamiento en caché de API para mejorar la latencia y reducir la E / S para su punto final.
- Al almacenar en caché para una etapa de API en particular (versión controlada por versión), almacena en caché las respuestas para un TTL en particular en segundos.
- API Gateway es compatible con AWS Certificate Manager y puede utilizar certificados TLS / SSL gratuitos.
- Con API Gateway, hay dos tipos de llamadas a API:
  - Llamadas a la API de API Gateway para crear, modificar, eliminar o implementar API REST. Estos se registran en CloudTrail.
  - Llamadas a la API configuradas por los desarrolladores para ofrecer su funcionalidad personalizada: no se registran en CloudTrail.

### Cross Origin Resource Sharing:
- En informática, la política del mismo origen es un concepto importante en el que un navegador web permite que los scripts contenidos en una página accedan a los datos de otra página, pero solo si ambas páginas tienen el mismo origen.
- Los navegadores imponen este comportamiento, pero herramientas como cURL y PostMan lo ignoran.
- El intercambio de recursos de origen cruzado (CORS) es una forma en que el servidor en el origen puede relajar la política del mismo origen. CORS permite compartir recursos restringidos como fuentes que se solicitan desde otro dominio fuera del dominio original desde donde se compartió el primer recurso.
- CORS define una forma para que las aplicaciones web cliente que se cargan en un dominio interactúen con recursos en un dominio diferente. Con la compatibilidad con CORS, puede crear aplicaciones web enriquecidas del lado del cliente con Amazon S3 y permitir de forma selectiva el acceso de origen cruzado a sus recursos de Amazon S3.
- Si alguna vez encuentra un error que menciona que una política de origen no se puede leer en el recurso remoto, debe habilitar CORS en API Gateway.
- CORS se aplica en el lado del cliente (navegador web).
- Un ejemplo común de este problema es si está utilizando un sitio con Javascript / AJAX para varios dominios en API Gateway. Debería asegurarse de que CORS esté habilitado.
- CORS no evita los ataques XSS, pero protege contra los ataques CSRF. Lo que hace es controlar quién puede utilizar los datos proporcionados por su punto final. Entonces, si tiene un sitio web meteorológico con devoluciones de llamada a una API que verifica el pronóstico, podría evitar que alguien escriba un sitio web que atienda llamadas de JavaScript en su API cuando navegue a su sitio web.
- Cuando alguien intenta las llamadas maliciosas, su navegador leerá los encabezados CORS y no permitirá que se realice la solicitud, protegiéndolo así del ataque.

## CloudFormation

### Simplificando CloudFormation:
CloudFormation es una herramienta automatizada para aprovisionar entornos completos basados ​​en la nube. Es similar a Terraform, donde codifica las instrucciones de lo que desea tener dentro de la configuración de su aplicación (X muchos servidores web de tipo Y con una base de datos de tipo Z en el backend, etc.). Hace que sea mucho más fácil describir lo que desea en el marcado y hacer que AWS haga el trabajo de aprovisionamiento real involucrado.

### Detalles Clave de CloudFormation:
- El caso de uso principal de CloudFormation es para configuraciones avanzadas y entornos de producción, ya que es complejo y tiene muchas características sólidas.
- Las plantillas de CloudFormation se pueden utilizar para crear, actualizar y eliminar infraestructura.
- Las plantillas están escritas en YAML o JSON
- Una configuración completa de CloudFormation se denomina pila.
- Una vez que se crea una plantilla, AWS creará la pila correspondiente. Esta es la representación viva y activa de dicha plantilla. Una plantilla puede crear un número infinito de pilas.
- El campo * Recursos * es el único campo obligatorio al crear una plantilla de CloudFormation
- Los activadores de reversión le permiten monitorear la creación de la pila a medida que se construye. Si ocurre un error, puede activar una reversión como su nombre lo indica.
- <a href="https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.updateDate&quickstart-all.sort-order=desc">AWS Quick Starts se compone de muchas pilas de CloudFormation de alta calidad diseñadas por ingenieros de AWS.</a>
- Una plantilla de ejemplo que pondría en marcha una instancia EC2:

![Screen Shot 2020-07-01 at 8 44 52 AM](https://user-images.githubusercontent.com/13093517/86245210-27b69180-bb77-11ea-8dff-3d663957a8e2.png)

- Para cualquier recurso lógico en la pila, CloudFormation creará un recurso físico correspondiente en su cuenta de AWS. El trabajo de CloudFormation es mantener sincronizados los recursos físicos y lógicos.
- Una plantilla se puede actualizar y luego usar para actualizar la misma stack.

## ElasticBeanstalk

### Simplificando ElasticBeanstalk:
ElasticBeanstalk es otra forma de programar su proceso de aprovisionamiento mediante la implementación de aplicaciones existentes en la nube. ElasticBeanstalk está dirigido a desarrolladores que saben muy poco sobre la nube y quieren la forma más sencilla de implementar su código.

### Detalles Clave de ElasticBeanstalk:
- Simplemente cargue su aplicación y ElasticBeanstalk se encargará de la infraestructura subyacente.
- ElasticBeanstalk tiene aprovisionamiento de capacidad, lo que significa que puede usarlo con autoescalado desde el principio.
ElasticBeanstalk aplica actualizaciones a su aplicación al tener listo un duplicado con la versión ya actualizada. Este duplicado luego se intercambia con el original. Esto se hace como medida preventiva en caso de que falle su aplicación actualizada. Si la aplicación falla, ElasticBeanstalk volverá a la copia original con la versión anterior y los usuarios que estén usando su aplicación no experimentarán tiempo de inactividad.
- Puede usar ElasticBeanstalk incluso para alojar Docker, ya que Elastic Beanstalk admite la implementación de aplicaciones web desde contenedores. Con los contenedores Docker, puede definir su propio entorno de ejecución, su propia plataforma, lenguaje de programación y cualquier dependencia de la aplicación (como administradores de paquetes o herramientas) que no son compatibles con otras plataformas. ElasticBeanstalk facilita la implementación de Docker, ya que los contenedores de Docker ya son autónomos e incluyen toda la información de configuración y el software necesarios para su ejecución.

## AWS Organizations

### Simplificando AWS Organizations:
AWS Organizations es un servicio de administración de cuentas que le permite consolidar varias cuentas de AWS en una organización que usted crea y administra de forma centralizada.

### Detalles Clave de AWS Organizations:
- Las mejores prácticas son usar la cuenta raíz para administrar la facturación solo con cuentas separadas que se usan para implementar recursos.
- El objetivo de AWS Organizations es implementar permisos en las cuentas separadas debajo de la cuenta raíz y hacer que esas políticas se filtren. AWS Organizations le ayuda a controlar su entorno de forma centralizada a medida que crece y escala sus cargas de trabajo en AWS.
- Puede utilizar unidades organizativas (OU) para agrupar cuentas similares y administrarlas como una sola unidad. Esto simplifica enormemente la gestión de sus cuentas.
- Puede adjuntar un control basado en políticas a una OU y todas las cuentas dentro de la OU heredarán automáticamente la política. Por lo tanto, si los desarrolladores de su empresa tienen su propia cuenta de AWS de espacio aislado, pueden tratarse como una sola unidad y estar restringidos por las mismas políticas.
- Con las organizaciones de AWS, podemos habilitar o deshabilitar servicios mediante políticas de control de servicios (SCP) en general en unidades organizativas o, más específicamente, en cuentas individuales.
- Utilice SCP con AWS Organizations para establecer controles de acceso de modo que todos los principales de IAM (usuarios y roles) se adhieran a ellos. Con las SCP, puede especificar *Condiciones*, *Recursos* y *NotAction* para denegar el acceso a las cuentas de su organización o unidad organizativa. Por ejemplo, puede utilizar SCP para restringir el acceso a regiones de AWS específicas o evitar la eliminación de recursos comunes, como un rol de IAM utilizado para sus administradores centrales.

## Misceláneos

La siguiente sección incluye servicios, características y técnicas que pueden aparecer en el examen. También es muy útil conocerlos como ingeniero que utiliza AWS. Si los siguientes elementos aparecen en el examen, no se probarán en detalle. Solo tendrás que saber cuál es el significado detrás del nombre. Es una gran idea aprender cada elemento en profundidad para el beneficio de su carrera, pero no es necesario para el examen.

### Qué es Amazon Cognito? 
- Antes de hablar sobre Amazon Cognito, primero es importante comprender qué es Web Identity Federation. Web Identity Federation le permite dar a sus usuarios acceso a los recursos de AWS después de que se hayan autenticado con éxito en un proveedor de identidad basado en web como Facebook, Google, Amazon, etc. Después de un inicio de sesión exitoso en estos servicios, el usuario recibe un código de autenticación de el proveedor de identidad que se puede utilizar para obtener credenciales de AWS temporales.
- Amazon Cognito es el servicio de Amazon que proporciona Federación de identidad web. No es necesario que escriba el código que le dice a los usuarios que inicien sesión en Facebook o que inicien sesión en Google en su aplicación. Cognito ya lo hace por ti.
- Una vez autenticado en un proveedor de identidad (digamos con Facebook como ejemplo), el proveedor proporciona un token de autenticación. Este token de autenticación se proporciona a cognito, que responde con acceso limitado a su entorno de AWS. Tú dices qué tan limitado te gustaría que fuera este acceso en la función de IAM.
- El trabajo de Cognito es intermediario entre su aplicación y los autenticadores legítimos.
- * Cognito User Pools * son directorios de usuarios que se utilizan para la funcionalidad de registro e inicio de sesión en su aplicación. La autenticación exitosa genera un token web JSON. Recuerde que los grupos de usuarios deben estar basados ​​en usuarios. Maneja el registro, la recuperación y la autenticación.
- * Cognito Identity Pools * se utilizan para permitir a los usuarios acceso temporal a servicios directos de AWS como S3 o DynamoDB. Los grupos de identidades realmente entran y le otorgan el rol de IAM.
- La autenticación basada en SAML se puede utilizar para permitir el inicio de sesión en la Consola de administración de AWS para usuarios que no son de IAM.
- En particular, puede utilizar Microsoft Active Directory, que también implementa Security Assertion Markup Language (SAML).
- Puede utilizar Amazon Cognito para entregar credenciales temporales con privilegios limitados a su aplicación para que sus usuarios puedan acceder a los recursos de AWS.
- Los grupos de identidades de Amazon Cognito admiten identidades autenticadas y no autenticadas.
- Puede recuperar un identificador único de Amazon Cognito (ID de identidad) para su usuario final inmediatamente si está permitiendo usuarios no autenticados o después de haber configurado los tokens de inicio de sesión en el proveedor de credenciales si está autenticando usuarios.
- Cuando necesite agregar autenticación fácilmente a su aplicación móvil y de escritorio, piense en Amazon Cognito.

### Qué es AWS Resource Access Manager?
- AWS Resource Access Manager (RAM) es un servicio que le permite compartir recursos de AWS de forma fácil y segura con cualquier cuenta de AWS o dentro de su organización de AWS. Puede compartir AWS Transit Gateways, subredes, configuraciones de AWS License Manager y recursos de reglas de resolución de Amazon Route 53 con RAM.
- Muchas organizaciones utilizan varias cuentas para crear aislamiento administrativo o de facturación y para limitar el impacto de los errores como parte del servicio de AWS Organizations.
- RAM elimina la necesidad de crear recursos duplicados en varias cuentas, lo que reduce la sobrecarga operativa de administrar esos recursos en cada una de las cuentas que posee.
- Puede crear recursos de forma centralizada en un entorno de varias cuentas y utilizar la RAM para compartir esos recursos entre cuentas en tres sencillos pasos: crear un recurso compartido, especificar recursos y especificar cuentas.
- RAM está disponible sin cargo adicional.

### Qué es Athena?
- Athena es un servicio de consulta interactivo que le permite interactuar y consultar datos de S3 utilizando comandos SQL estándar. Esto es beneficioso para las consultas programáticas para el desarrollador promedio. No tiene servidor, no requiere aprovisionamiento y usted paga por consulta y por TB escaneado. Básicamente, convierte S3 en una base de datos compatible con SQL utilizando Athena.
- Ejemplos de casos de uso:
  - Consultas de registros que se vuelcan en depósitos de S3 como alternativa o complemento a la pila de ELK
  - Configuración de consultas para ejecutar informes comerciales basados ​​en los datos que ingresan regularmente a S3
  - Ejecución de consultas sobre datos de flujo de clics para tener una mejor perspectiva del comportamiento del cliente

### Qué es AWS Macie?
- Para comprender a Macie, es importante comprender la PII o la información de identificación personal:
  - Datos personales utilizados para establecer la identidad de una persona que pueden ser explotados.
  - Ejemplos: número de seguro social, número de teléfono, domicilio, dirección de correo electrónico, D.O.B, número de pasaporte, etc.
- Amazon Macie es un servicio de seguridad con tecnología ML que lo ayuda a evitar la pérdida de datos al descubrir, clasificar y proteger automáticamente los datos confidenciales almacenados en Amazon S3. Amazon Macie utiliza el aprendizaje automático para reconocer datos confidenciales, como información de identificación personal (PII) o propiedad intelectual, asigna un valor comercial y proporciona visibilidad sobre dónde se almacenan estos datos y cómo se utilizan en su organización.
- Puede estar informado de las detecciones a través de los paneles, alertas o informes de Macie.
- Macie también puede analizar los registros de CloudTrail para ver quién pudo haber interactuado con datos confidenciales.
- Macie monitorea continuamente la actividad de acceso a los datos para detectar anomalías y envía alertas cuando detecta un riesgo de acceso no autorizado o fugas de datos involuntarias.
- Macie tiene la capacidad de detectar permisos de acceso global que se establecen inadvertidamente en datos confidenciales, detectar la carga de claves API dentro del código fuente y verificar que los datos confidenciales del cliente se almacenan y acceden de una manera que cumpla con sus estándares de cumplimiento.

### Qué es AWS KMS?
- AWS Key Management Service (AWS KMS) es un servicio administrado que le facilita la creación y el control de las claves de cifrado que se utilizan para cifrar sus datos. Las claves maestras que crea en AWS KMS están protegidas por módulos criptográficos validados por FIPS 140-2.
- AWS KMS está integrado con la mayoría de los demás servicios de AWS que cifran sus datos con claves de cifrado que usted administra. AWS KMS también está integrado con AWS CloudTrail para proporcionar registros de uso de claves de cifrado para ayudarlo a satisfacer sus necesidades de auditoría, normativas y de cumplimiento.
- Puede configurar su aplicación para utilizar la API de KMS para cifrar todos los datos antes de guardarlos en el disco.

### Qué es AWS Secrets Manager?
- AWS Secrets Manager es un servicio de AWS que le facilita la administración de secretos.
- Los secretos pueden ser credenciales de base de datos, contraseñas, claves API de terceros e incluso texto arbitrario. Puede almacenar y controlar el acceso a estos secretos de forma centralizada mediante la consola de Secrets Manager, la interfaz de línea de comandos (CLI) de Secrets Manager o la API y los SDK de Secrets Manager.
- En el pasado, cuando creaba una aplicación personalizada que recupera información de una base de datos, normalmente tenía que incrustar las credenciales (el secreto) para acceder a la base de datos directamente en la aplicación. Cuando llegó el momento de rotar las credenciales, tuvo que hacer mucho más que crear nuevas credenciales. Tuvo que invertir tiempo para actualizar la aplicación para usar las nuevas credenciales. Luego tuvo que distribuir la aplicación actualizada. Si tenía varias aplicaciones que compartían credenciales y no actualizaba una de ellas, la aplicación se rompería.
- Debido a este riesgo, muchos clientes han optado por no rotar regularmente sus credenciales, lo que efectivamente sustituye un riesgo por otro (funcionalidad frente a seguridad).
- Secrets Manager le permite reemplazar las credenciales codificadas en su código (incluidas las contraseñas), con una llamada API a Secrets Manager para recuperar el secreto mediante programación.
- Esto ayuda a garantizar que el secreto no se vea comprometido por alguien que examine su código, porque el secreto simplemente no está ahí.
- Además, puede configurar Secrets Manager para que gire automáticamente el secreto según un horario que usted especifique. Esto le permite reemplazar los secretos a largo plazo por otros a corto plazo, lo que ayuda a reducir significativamente el riesgo de compromiso.

### Qué es AWS STS?
- AWS Security Token Service (AWS STS) es el servicio que puede utilizar para crear y proporcionar a los usuarios de confianza credenciales de seguridad temporales que pueden controlar el acceso a sus recursos de AWS.
- Las credenciales de seguridad temporales funcionan de manera casi idéntica a las credenciales de clave de acceso a largo plazo que pueden utilizar los usuarios de IAM.
- Las credenciales de seguridad temporales son a corto plazo, como su nombre lo indica. Se pueden configurar para que duren desde unos minutos hasta varias horas. Una vez que caducan las credenciales, AWS ya no las reconoce ni permite ningún tipo de acceso desde las solicitudes de API realizadas con ellas.

### Qué es OpsWorks?
- AWS OpsWorks es un servicio de administración de configuración que proporciona instancias administradas de Chef y Puppet. Chef y Puppet son plataformas de automatización que le permiten utilizar código para automatizar las configuraciones de sus servidores.
- OpsWorks le permite usar Chef y Puppet para automatizar cómo se configuran, implementan y administran los servidores en sus instancias Amazon EC2 o entornos informáticos locales.
- OpsWorks tiene tres ofertas: AWS Opsworks para Chef Automate, AWS OpsWorks para Puppet Enterprise y AWS OpsWorks Stacks.
- AWS OpsWorks Stacks le permite administrar aplicaciones y servidores en AWS y en las instalaciones. Con OpsWorks Stacks, puede modelar su aplicación como una pila que contiene diferentes capas, como equilibrio de carga, base de datos y servidor de aplicaciones.
- OpsWorks Stacks es lo suficientemente complejo como para que pueda implementar y configurar instancias de Amazon EC2 en cada capa o conectarse a otros recursos como bases de datos de Amazon RDS.

### Qué es Elastic Transcoder?
- Un transcodificador de medios en la nube. Básicamente, es un servicio que convierte archivos multimedia de su formato original al formato multimedia especificado, ya sea para teléfonos, tabletas, PC, etc.
- Debido al soporte integrado para diferentes tipos de medios, puede confiar en que la calidad resultante será buena.
- Con Elastic Transcoder, paga por minuto del trabajo de transcodificación y la resolución del trabajo terminado.

### Qué es AWS Directory Service?
- AWS Directory Service proporciona varias formas de utilizar Amazon Cloud Directory y Microsoft Active Directory (AD) con otros servicios de AWS.
- Los directorios almacenan información sobre usuarios, grupos y dispositivos, y los administradores los utilizan para administrar el acceso a la información y los recursos.
- AWS Directory Service proporciona múltiples opciones de directorio para los clientes que desean utilizar aplicaciones existentes de Microsoft AD o Lightweight Directory Access Protocol (LDAP) en la nube. También ofrece esas mismas opciones a los desarrolladores que necesitan un directorio para administrar usuarios, grupos, dispositivos y acceso.

### Qué es IoT Core?
- AWS IoT Core es un servicio en la nube administrado que permite que los dispositivos conectados interactúen de manera fácil y segura con aplicaciones en la nube y otros dispositivos.
- AWS IoT Core proporciona comunicación segura y procesamiento de datos en diferentes tipos de dispositivos y ubicaciones conectados para que pueda crear fácilmente aplicaciones de IoT.

### Qué es AWS WorkSpaces?
- Amazon WorkSpaces es una solución de escritorio como servicio (DaaS) administrada y segura. Puede utilizar Amazon WorkSpaces para aprovisionar escritorios Windows o Linux en solo unos minutos y escalar rápidamente para proporcionar miles de escritorios a los trabajadores de todo el mundo.
- Amazon WorkSpaces lo ayuda a eliminar la complejidad en la administración del inventario de hardware, las versiones y parches del sistema operativo y la infraestructura de escritorio virtual (VDI), lo que ayuda a simplificar su estrategia de entrega de escritorio.
- Con Amazon WorkSpaces, sus usuarios obtienen un escritorio rápido y receptivo de su elección al que pueden acceder desde cualquier lugar, en cualquier momento y desde cualquier dispositivo compatible.

### Qué es AWS Fargate?
- AWS Fargate es un motor informático sin servidor para contenedores.
- El tipo de lanzamiento de Fargate le permite ejecutar sus aplicaciones en contenedores sin la necesidad de aprovisionar y administrar la infraestructura de backend. Simplemente registre la definición de su tarea y Fargate lanzará el contenedor por usted.
- Funciona tanto con Amazon Elastic Container Service (ECS) como con Amazon Elastic Kubernetes Service (EKS).
- Fargate le facilita la tarea de concentrarse en la creación de sus aplicaciones. Elimina la necesidad de aprovisionar y administrar servidores, le permite especificar y pagar recursos por aplicación y mejora la seguridad a través del aislamiento de aplicaciones por diseño.

### Qué es Amazon Elastic Container Service?
- Amazon Elastic Container Service (Amazon ECS) es un servicio de orquestación de contenedores completamente administrado.
- Amazon ECS elimina la necesidad de instalar, operar y escalar su propia infraestructura de administración de clústeres. Con simples llamadas a la API, puede iniciar y detener aplicaciones habilitadas para contenedores, consultar el estado completo de su clúster y acceder a muchas funciones conocidas como grupos de seguridad, Elastic Load Balancing, volúmenes de EBS y roles de IAM.
- Puede utilizar Amazon ECS para programar la ubicación de contenedores en su clúster en función de sus necesidades de recursos y requisitos de disponibilidad. También puede integrar su propio programador o programadores de terceros para cumplir con los requisitos específicos del negocio o de la aplicación.
- Puede optar por ejecutar sus clústeres de ECS mediante AWS Fargate, que es computación sin servidor para contenedores. Fargate elimina la necesidad de aprovisionar y administrar servidores, le permite especificar y pagar los recursos por aplicación y mejora la seguridad mediante el aislamiento de aplicaciones por diseño.

### Qué es Amazon Elastic Kubernetes Service?
- Amazon Elastic Kubernetes Service (Amazon EKS) es un servicio de Kubernetes totalmente administrado. EKS se ejecuta upstream Kubernetes y está certificado en conformidad con Kubernetes para que pueda aprovechar todos los beneficios de las herramientas de código abierto de la comunidad. También puede migrar fácilmente cualquier aplicación estándar de Kubernetes a EKS sin necesidad de refactorizar su código.
- Kubernetes es un software de código abierto que le permite implementar y administrar aplicaciones en contenedores a escala. Kubernetes agrupa los contenedores en agrupaciones lógicas para su administración y detección, luego los lanza a clústeres de instancias EC2. Con Kubernetes, puede ejecutar aplicaciones en contenedores, incluidos microservicios, trabajadores de procesamiento por lotes y plataformas como servicio (PaaS) con el mismo conjunto de herramientas en las instalaciones y en la nube.
- Amazon EKS aprovisiona y escala el plano de control de Kubernetes, incluidos los servidores de API y la capa de persistencia de backend, en varias zonas de disponibilidad de AWS para una alta disponibilidad y tolerancia a fallas. Amazon EKS detecta y reemplaza automáticamente los nodos del plano de control en mal estado y proporciona parches para el plano de control.
- Sin Amazon EKS, debe ejecutar el plano de control de Kubernetes y el clúster de nodos de trabajo usted mismo. Con Amazon EKS, aprovisiona sus nodos trabajadores mediante un solo comando en la consola de EKS, la CLI o la API, y AWS maneja el aprovisionamiento, el escalado y la administración del plano de control de Kubernetes en una configuración segura y de alta disponibilidad. Esto elimina una carga operativa significativa para ejecutar Kubernetes y le permite concentrarse en crear aplicaciones en lugar de administrar la infraestructura de AWS.
- Puede ejecutar EKS mediante AWS Fargate, que es una computación sin servidor para contenedores. Fargate elimina la necesidad de aprovisionar y administrar servidores, le permite especificar y pagar recursos por aplicación y mejora la seguridad a través del aislamiento de aplicaciones por diseño.
- Amazon EKS está integrado con muchos servicios de AWS para brindar escalabilidad y seguridad para sus aplicaciones. Estos servicios incluyen Elastic Load Balancing para distribución de carga, IAM para autenticación, Amazon VPC para aislamiento y AWS CloudTrail para registro.

### Qué significa pilot light?
- El término `pilot light` se utiliza a menudo para describir un escenario de recuperación ante desastres en el que siempre se ejecuta una versión mínima de un entorno en la nube.
- La idea de la luz piloto es una analogía que proviene del calentador de gas. En un calentador de gas, una pequeña llama que siempre está encendida y puede encender rápidamente todo el horno para calentar una casa. Este escenario es similar al escenario de copia de seguridad y restauración.
- Por ejemplo, con AWS puede mantener una luz piloto configurando y ejecutando los elementos centrales más críticos de su sistema en AWS. Cuando llegue el momento de la recuperación, podrá aprovisionar rápidamente un entorno de producción a gran escala alrededor del núcleo crítico que siempre se ha estado ejecutando.

### Que son las implementaciones Blue-Green?
- Uno de los desafíos de la automatización de implementaciones es el corte de la etapa final de prueba a la producción en vivo. Por lo general, debe hacer esto rápidamente para minimizar el tiempo de inactividad.
- El enfoque de implementación Blue-Green hace esto al garantizar que tenga dos entornos de producción, lo más idénticos posible. En cualquier momento uno de ellos, digamos azul por ejemplo, está activo. Mientras prepara una nueva versión de su software, realiza la etapa final de prueba en el entorno ecológico. Una vez que el software está funcionando en el entorno verde, cambia el enrutador para que todas las solicitudes entrantes vayan al entorno verde; el azul ahora está inactivo.
- La implementación blue-green también le brinda una forma rápida de retroceder: si algo sale mal, vuelva a cambiar el enrutador a su entorno azul.
- CloudFormation y CodeDeploy (la versión de Jenkins de AWS) admiten esta técnica de implementación.

### Qué es Amazon Data Lifecycle Manager?
- Puede utilizar Amazon Data Lifecycle Manager (Amazon DLM) para automatizar la creación, retención y eliminación de instantáneas tomadas para realizar copias de seguridad de sus volúmenes de Amazon EBS.
- La automatización de la gestión de instantáneas le ayuda a:
  - Proteja los datos valiosos mediante la aplicación de un programa de copias de seguridad regular.
  - Conserve las copias de seguridad según lo requieran los auditores o el cumplimiento interno.
  - Reduzca los costos de almacenamiento eliminando las copias de seguridad obsoletas.
- El uso de Amazon DLM significa que ya no necesita recordar tomar sus instantáneas de EBS, lo que reduce la carga cognitiva de los ingenieros.

### Qué es Route Origin Authorization?
- Puede traer parte o todo su rango de direcciones IPv4 públicas desde su red local a su cuenta de AWS. Continúa siendo propietario del rango de direcciones, pero AWS lo anuncia en Internet. Después de traer el rango de direcciones a AWS, aparece en su cuenta como un grupo de direcciones.
- Luego, puede crear una dirección IP elástica a partir de su grupo de direcciones y usarla con sus recursos de AWS, como instancias EC2, puertas de enlace NAT y Equilibradores de carga de red. Esto también se llama "Traiga sus propias direcciones IP (BYOIP)".
- Para asegurarse de que solo usted pueda traer su rango de direcciones a su cuenta de AWS, debe autorizar a Amazon a publicitar el rango de direcciones y proporcionar pruebas de que usted es el propietario del rango de direcciones.
- El beneficio de ROA es que puede migrar aplicaciones preexistentes a AWS sin que sus socios y clientes cambien sus listas blancas de direcciones IP.

### Que es Amazon MQ?
- Amazon MQ es un servicio de agente de mensajes administrado que facilita la configuración y el funcionamiento de agentes de mensajes en la nube.
- El servicio se utiliza al migrar servicios y aplicaciones a la nube desde su sitio web, que es en lo que se diferencia de Amazon SQS.
- Amazon MQ admite corredores de durabilidad optimizados respaldados por Amazon EFS para admitir alta disponibilidad y durabilidad de mensajes, y corredores de rendimiento optimizados respaldados por Amazon EBS para admitir aplicaciones de alto volumen que requieren baja latencia y alto rendimiento.
- Puede pasar fácilmente de cualquier agente de mensajes a Amazon MQ porque no tiene que volver a escribir ningún código de mensajería en sus aplicaciones.
- Amazon MQ es adecuado para profesionales de TI, desarrolladores y arquitectos empresariales que administran ellos mismos un intermediario de mensajes, ya sea en las instalaciones o en la nube, y desean pasar a un servicio en la nube completamente administrado sin volver a escribir el código de mensajería en sus aplicaciones.

### Qué es AWS Config?
- AWS Config es un servicio que le permite evaluar, auditar y evaluar las configuraciones de sus recursos de AWS. Config monitorea y registra continuamente sus configuraciones de recursos de AWS y le permite automatizar la evaluación de las configuraciones registradas en comparación con las configuraciones deseadas.
- Con Config, puede revisar los cambios en las configuraciones y las relaciones entre los recursos de AWS, profundizar en los historiales de configuración de recursos detallados y determinar su cumplimiento general con las configuraciones especificadas en sus pautas internas. Esto le permite simplificar la auditoría de cumplimiento, el análisis de seguridad, la gestión de cambios y la resolución de problemas operativos.
- AWS Config le permite hacer lo siguiente: ·
  - Evalúe sus configuraciones de recursos de AWS para la configuración deseada. ·
  - Obtenga una instantánea de las configuraciones actuales de los recursos admitidos que están asociados con su cuenta de AWS. ·
  - Recupere configuraciones de uno o más recursos que existen en su cuenta. ·
  - Recuperar configuraciones históricas de uno o más recursos. ·
  - Reciba una notificación cada vez que se crea, modifica o elimina un recurso.
  - Ver relaciones entre recursos. Por ejemplo, es posible que desee buscar todos los recursos que utilizan un grupo de seguridad en particular.
