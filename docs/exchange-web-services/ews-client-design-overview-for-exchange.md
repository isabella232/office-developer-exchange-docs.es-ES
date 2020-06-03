---
title: Introducción al diseño de EWS cliente de Exchange
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: Obtenga información sobre las consideraciones de diseño para desarrollar con EWS para Exchange.
localization_priority: Priority
ms.openlocfilehash: 0ac4fe1be0800008af572ebc296e004aa29d8daf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455425"
---
# <a name="ews-client-design-overview-for-exchange"></a>Introducción al diseño de EWS cliente de Exchange

Obtenga información sobre las consideraciones de diseño para desarrollar con EWS para Exchange. 
  
En este artículo se proporciona información general sobre el diseño de una aplicación de servicios Web de Exchange (EWS). Puede usar esta información para determinar si EWS es la API adecuada para su aplicación y, si es así, qué tipo de implementación de cliente debe usar. En este artículo también se proporciona información sobre los procedimientos recomendados para diseñar aplicaciones que puedan dirigirse a Office 365, Exchange Online y versiones de Exchange a partir de Exchange 2007, en una base de código y puntos de decisión importantes para dirigirse a servidores de Exchange locales, en lugar de dirigirse a Exchange Online.
  
## <a name="is-ews-the-right-api-for-your-application"></a>¿La API correcta de la aplicación es EWS?
<a name="IsEWSRight"> </a>

Antes de empezar a diseñar la aplicación, es importante tener en cuenta si EWS es la API adecuada. Si está desarrollando en Exchange Server o Exchange Online, EWS es la tecnología de acceso de cliente preferida. El desarrollo de acceso de cliente para versiones de Exchange a partir de Exchange 2007 se ha centrado principalmente en EWS. Las nuevas funciones de acceso de cliente que se implementan en Outlook usan EWS, incluidas las características de disponibilidad fuera de la oficina (OOF) que se incluyen en Exchange 2007 y las sugerencias de correo y la funcionalidad de obtener salas incorporadas en Exchange 2010. Esto representa una inversión confirmada en EWS para socios internos y externos que desarrollan aplicaciones de cliente de Exchange.
  
EWS es la API de acceso de cliente principal para las aplicaciones cliente de Exchange. Sin embargo, en algunos casos, puede considerar otras API de Exchange para el desarrollo de aplicaciones cliente. Por ejemplo, Exchange ActiveSync proporciona las siguientes ventajas con respecto a EWS:
  
- La estructura XML se ha acortado para convertir a Exchange ActiveSync en un protocolo más compacto.  
- Exchange ActiveSync contiene un mecanismo de directivas para controlar el acceso de clientes y proporcionar otras soluciones de mensajería para móviles de empresa sólidas.
    
> [!NOTE]
> Necesita una licencia para poder desarrollar clientes de Exchange ActiveSync. Para obtener información sobre las diferencias entre Exchange ActiveSync y EWS, consulte [Choosing Between Exchange ActiveSync and Exchange Web Services (EWS)](https://msdn.microsoft.com/library/dn144954%28v=exchg.140%29.aspx). 
  
MAPI RPC sobre HTTP es otra opción de programación para las aplicaciones cliente de Exchange. Sin embargo, MAPI RPC sobre HTTP no proporciona una interfaz intuitiva para la comunicación entre clientes y el servidor.
  
Para obtener más información sobre las tecnologías de desarrollo de Exchange, consulte [explorar la API administrada de EWS, EWS y servicios Web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).
  
## <a name="options-for-ews-client-development"></a>Opciones para el desarrollo de cliente EWS
<a name="EWSClientOptions"> </a>

Hay varias opciones disponibles para desarrollar en Exchange con EWS. La mejor opción dependerá de la plataforma de desarrollo, las herramientas, las implementaciones disponibles y los requisitos de aplicación de la organización. Las siguientes son las cuatro opciones principales que están disponibles para crear aplicaciones de cliente de EWS:
  
- La API administrada EWS
- La API Java EWS
- Los servidores proxy generados automáticamente de EWS
- Una API de cliente EWS personalizada
    
### <a name="ews-managed-api"></a>API administrada EWS

La [API administrada de EWS](https://aka.ms/ews-managed-api-readme) es un cliente de servicio web personalizado. Es la API de acceso de cliente estándar para las aplicaciones de .NET Framework. 
  
Estas son algunas de las ventajas de usar la API administrada de EWS:
  
- Proporciona un modelo de objetos intuitivo.   
- Abstrae las complejidades de la descripción del servicio en los archivos de esquema y WSDL.   
- Incluye lógica empresarial del lado cliente.   
- Controla las solicitudes y respuestas Web, y la serialización y deserialización de objetos.   
- Es compatible con Microsoft.
    
Sin embargo, tenga en cuenta que la API administrada de EWS no es una solución completa. Algunas funciones no se implementan en la API administrada de EWS. Aunque la API administrada de EWS no implementa toda la funcionalidad de EWS, puede ser la mejor opción para el desarrollo de aplicaciones cliente, por los motivos siguientes:
  
- Puede usar .NET Framework para el desarrollo.
- Implementa la detección automática además de la mayoría de las partes del modelo de objetos EWS.
- Implementa la lógica empresarial del lado cliente para trabajar con EWS, en la clase [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) . 
    
Puede elegir usar la API del servicio Web EWS en lugar de la API administrada de EWS por cualquiera de los siguientes motivos:
  
- La aplicación no utiliza .NET Framework. 
- No desea distribuir el ensamblado de la API administrada de EWS. 
- La aplicación usa características que no se implementan en la API administrada de EWS.
    
Para obtener más información, vea Introducción [a las aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md).
  
> [!NOTE]
> La API administrada EWS ya está disponible como proyecto de código abierto en [GitHub](https://aka.ms/ews-managed-api-github). Puede usar la biblioteca de código abierto para: 
> - Contribuir con correcciones de errores y mejoras a la API. 
> - Obtener correcciones y mejoras antes de que estén disponibles en una versión oficial.
> - Tener acceso a una implementación más completa y actualizada de la API, para usarla como referencia o para crear nuevas bibliotecas en nuevas plataformas.
> 
> Le agradecemos las [aportaciones](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) que realice a través de GitHub. 
  
### <a name="ews-java-api"></a>API Java EWS

La API Java de EWS es un proyecto de código abierto en [GitHub](https://github.com/OfficeDev/ews-java-api) que la comunidad puede actualizar y extender. Es similar a la [API administrada de EWS](https://msdn.microsoft.com/library/office/jj220535%28v=exchg.80%29.aspx) y usa respuestas y solicitudes SOAP de EWS a través de la red. Aunque no se puede acceder a todas [las operaciones SOAP de EWS](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) mediante la API de Java EWS, con la [creación reciente](https://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) del proyecto de código abierto, estamos mirando a la comunidad para salvar esta brecha. Tenga en cuenta que el soporte técnico de Microsoft, con un contrato de soporte técnico adecuado, solucionará las preguntas relacionadas con el protocolo SOAP de EWS, pero no la API de Java EWS en sí. La API de Java EWS está disponible para la descarga y la contribución de la comunidad en [GitHub](https://github.com/OfficeDev/ews-java-api).

  
### <a name="ews-autogenerated-proxies"></a>Servidores proxy generados automáticamente de EWS

Las API de cliente generadas automáticamente se generan a partir de las definiciones de esquema XML y WSDL de EWS. Los generadores del modelo de objetos de cliente están disponibles para muchos idiomas. En general, los modelos de objetos generados automáticamente administran la serialización y deserialización de objetos. No incluyen la lógica empresarial y el proceso de autogeneración suelen crear artefactos que hacen que el modelo de objetos sea menos intuitivo de usar. La compatibilidad con Exchange cubre el código XML que el cliente envía y recibe, pero no el modelo de objetos.
  
### <a name="custom-ews-client-api"></a>API de cliente EWS personalizada

Para algunas aplicaciones que usan un pequeño conjunto de funciones de EWS, puede crear una API de cliente personalizada para comunicarse con Exchange. Esto le permite consumir menos recursos del sistema. Esto es útil para los clientes que se ejecutan en dispositivos con memoria restringida, como los clientes que ejecutan .NET micro Framework.
  
## <a name="ews-client-features"></a>Características de cliente de EWS
<a name="EWSFeatures"> </a>

Independientemente de la opción de desarrollo que elija, debe tener en cuenta cómo se implementan las características de EWS en el cliente. La disponibilidad de la característica se basa en la versión del esquema EWS a la que se destina la aplicación. Como los esquemas EWS son compatibles con versiones anteriores y posteriores, si se crea una aplicación destinada a una versión de esquema anterior, como Exchange Server 2007 SP1, la aplicación también funcionará con una versión de esquema posterior, como el servicio Exchange Server 2013 SP1, así como Exchange Online. 
  
Debido a que el esquema controla las características y las actualizaciones de características, le recomendamos que use la base de código común más temprana que tenga como objetivo las características de EWS que desea implementar en la aplicación cliente. Muchas aplicaciones pueden dirigirse a la versión Exchange2007_SP1, ya que el esquema de Exchange 2007 SP1 contiene casi todas las funciones principales de Exchange para trabajar con elementos y carpetas en el almacén de Exchange. Le recomendamos que mantenga bifurcaciones de código para cada versión de esquema EWS. Las siguientes son las versiones de esquema que están disponibles en este momento. 
  
```XML
  <xs:simpleType name="ExchangeVersionType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange2007" />
      <xs:enumeration value="Exchange2007_SP1" />
      <xs:enumeration value="Exchange2010" />
      <xs:enumeration value="Exchange2010_SP1" />
      <xs:enumeration value="Exchange2010_SP2" />
      <xs:enumeration value="Exchange2013" />
      <xs:enumeration value="Exchange2013_SP1" />
    </xs:restriction>
  </xs:simpleType>
```

Las versiones del esquema se mantienen en el tipo simple **ExchangeVersionType** . 
  
Para obtener información sobre las características que están disponibles en cada versión del esquema de EWS, consulte [versiones del esquema de EWS en Exchange](ews-schema-versions-in-exchange.md).
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Disponibilidad de características de API de servicio Web en Exchange y la API administrada de EWS](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)   
- [Versiones del esquema EWS en Exchange](ews-schema-versions-in-exchange.md)  
- [Opciones de configuración de EWS en Exchange](configuration-options-for-ews-in-exchange.md)  
- [Comparación de la programación de clientes de Exchange Online y Exchange local](comparing-exchange-online-and-exchange-on-premises-client-programming.md)   
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)  
- [Requisitos de redistribución para la API administrada de EWS](redistribution-requirements-for-the-ews-managed-api.md)  
- [Instrumentar solicitudes de cliente para EWS y REST en Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a>Vea también
 
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md) 
- [Tipos de aplicación de EWS](ews-application-types.md)
    

