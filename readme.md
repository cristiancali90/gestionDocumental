# Electronic Document Management System

- You can watch the <a href="https://www.youtube.com/watch?v=TyFW9PKqMuE">Demo</a>

Whoever having this error: SQLSTATE[42S02]: Base table or view not found: 1146 Table 'edms_latest.users' doesn't exist (SQL: select * from `users`

  where `status` = 0) FOLLOW THESE STEPS TO SOLVE THE ISSUE:
1- once you clone the project run composer install
2-   just comment all lines in boot function (app/Providers/AppServiceProvider.php) except first line (Schema::defaultStringLength(191);)

3- run php artisan migrate
4- uncomment the lines 
5- run php artisan serve and you are good to go

si hay problemas en bd relacionado con 
NO_AUTO_CREATE_USER

validar si existe la variable en mysql con 
SELECT @@GLOBAL.sql_mode;


ejecutar esta instruccion en mysql para removerla
SET @@global.sql_mode = 'STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO';


Para que una aplicación web de gestión de documentos digitales cumpla con los requisitos establecidos por el Archivo General de la Nación (AGN) en Colombia, debe tener en cuenta los siguientes aspectos:

Cumplimiento de las normativas y regulaciones establecidas por el AGN: La aplicación web debe cumplir con las normas y regulaciones establecidas por el AGN para la gestión de documentos digitales, como la resolución 3564 de 2015, la resolución 3723 de 2016 y la resolución 20203000764335 de 2020.

Capacidades de almacenamiento y seguridad: La aplicación web debe contar con una capacidad de almacenamiento adecuada y garantizar la seguridad de los documentos digitales almacenados, utilizando medidas de seguridad física y lógica que permitan proteger la información contra posibles accesos no autorizados, modificaciones, pérdidas o daños.

Interoperabilidad y compatibilidad: La aplicación web debe ser compatible con diferentes plataformas y dispositivos, así como interoperable con otros sistemas de gestión de documentos digitales.

Gestión de metadatos: La aplicación web debe permitir la gestión de metadatos, que son datos que describen y proporcionan información sobre los documentos digitales, como el autor, la fecha de creación, la ubicación, el formato, entre otros.

Control de versiones: La aplicación web debe permitir la gestión de versiones de los documentos digitales, para llevar un registro de las modificaciones realizadas y asegurar la integridad de los documentos.

Control de accesos y permisos: La aplicación web debe permitir la gestión de accesos y permisos, para que solo los usuarios autorizados puedan acceder a los documentos digitales y realizar acciones sobre ellos.

Auditoría y trazabilidad: La aplicación web debe contar con mecanismos de auditoría y trazabilidad que permitan conocer quién ha accedido a los documentos digitales, qué acciones ha realizado y cuándo las ha realizado.

Las principales normas y regulaciones que aplican a la gestión documental electrónica en Colombia son:

Ley 1712 de 2014: Ley de Transparencia y Acceso a la Información Pública, que establece el derecho de los ciudadanos a acceder a la información pública y promueve la transparencia en la gestión pública.

Ley 962 de 2005: Ley de Simplificación de Trámites Administrativos, que establece medidas para la simplificación y racionalización de los trámites y procedimientos administrativos.

Decreto 1078 de 2015: Reglamentario Único del Sector de Tecnologías de la Información y las Comunicaciones, que establece las condiciones para el uso de tecnologías de la información y las comunicaciones en la gestión pública.

Resolución 0643 de 2016: Reglamenta el uso de medios electrónicos y sistemas informáticos para la gestión documental y de archivo en las entidades públicas.

Norma Técnica Colombiana NTC-ISO 30300:2013: Sistemas de Gestión para los documentos, que establece los requisitos para la gestión de documentos electrónicos.

Norma Técnica Colombiana NTC-ISO 30301:2013: Sistemas de Gestión para los documentos de Archivo, que establece los requisitos para la gestión de documentos de archivo.

Guía para la Gestión Documental Electrónica en el Sector Público Colombiano, publicada por el Archivo General de la Nación, que establece los lineamientos para la gestión documental electrónica en las entidades públicas.

Es importante tener en cuenta que el cumplimiento de estas normas y regulaciones es fundamental para garantizar la legalidad y validez de los documentos electrónicos en Colombia. Por lo tanto, una aplicación web de gestión documental para entidades públicas en Colombia debe cumplir con estas normas y regulaciones para asegurar que los documentos digitales sean válidos y legales.