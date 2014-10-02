#Open Stack vs Open Nebula

##OpenStack

###Caracteristicas/Pros:
- Modelo *Public Cloud*, en el cuál la finalidad es la provisión de recursos virtualizados al público (Similar a Eucalyptus)
- Escrito completamente en Python
- Fácil *deployment*. Necesita pocos parametros de configuración para empezar a trabajar con él
- Es más abierto que OpenNebula, permitiendo a las diversas organizaciones soltura a la hora de hacer cambios e incluír nuevas features en las APIs.
- Actualmente es la plataforma con la comunidad de participantes más amplia, muy por encima del resto de plataformas.
- Totalmente Open-Source con extensiones Open-Core por parte de los vendor

###Contras:
- En la primera release de cada versión suelen haber problemas de conexionado entre los distintos módulos. Esto es debido a que los equipos de desarrollo pecan de poca comunicación entre ellos, trabajando cada uno en un módulo concreto de OPenStack y sin preocuparse de la interconexión de módulos hasta últimos momentos del proyecto.
- Las features de las releases son condicionadas por acuerdos entre los *vendors* (RedHat, HP, IBM) y no por los usuarios. OpenNebula se podría decir que está un nivel por debajo, es decir, que no compite al mismo nivel que OPenStack, sino que compite a nivel de los *vendors*
- El que haya tantos módulos interconexionados entre sí hace difícil el manejo del proyecto de forma global. Para cada módulo de OpenStack, existe un TLS que se encarga de dirigirlo durante un año, habiendo cada año elecciones para ver quién será el TLS. El cambio de TLS de un año a otro conlleva consecuencias, ya que el siguiente TLS no posee un seguimiento claro de lo que ha hecho el anterior y que campos ha abarcado, disponiendo sólo de informes de seguimiento rutinarios.
- Los mecanismos de failover son algo rudimentarios, basándose en tener a un host activo todo el rato que no hace nada hasta que haya situación de fallo.
- Compatible con EC2

#Empresas
- Dell
- Mirantis

##OpenNebula

###Caracteristivas/Pros:
- Modelo *Enterprise Cloud*, en el cuál la finalidad es facilitar la gestión de los recursos de los DataCenters, a modo de extensión de la virtualización. (Similar a VMware)
- Escrito en C++, C, Ruby, Java, Shell script, lex, yacc.
- El desarrollo de las features va en función de las necesidades de los usuarios, y no de los *vendors*
- Ofrece un diseño centralizado de administración de los diferentes subsistemas.
- Ofrece un Sistema de administración de recursos escalado: Una persona que tenga contratada cieros recursos los puede subcontratar a terceros (VDC)
- Administración centralizada para diferentes instancias de OpenNebula mediante un *single access pooint*
- Compatible con la mayoría de EC2
- Totalmente Open-Source (no OpenCore)

###Contras:
- En comparación con el resto de plataformas, tiene una comunidad reducida.
- Los mecanismos de *failover* o backup son solo parciales.