---
title: Generar una lista de extremos de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: Encuentre información acerca de cómo generar una lista de prioridades de los extremos de detección automática.
ms.openlocfilehash: ccecacc9c8beef464727efbc9d1fced7a81f9b7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763074"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a>Generar una lista de extremos de detección automática

Encuentre información acerca de cómo generar una lista de prioridades de los extremos de detección automática.
  
Es la primera tarea en el [proceso de detección automática](autodiscover-for-exchange.md) generar una lista de extremos de detección automática para su aplicación probar. Estos extremos de detección automática pueden proceder de una [búsqueda de SCP](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) o se pueden derivar de la dirección de correo electrónico del usuario. Al final, puede acabar con un gran número de extremos. Vamos a echar un vistazo a cómo se puede organizar por prioridad. 
  
## <a name="start-with-scp-lookup"></a>Iniciar con búsqueda de SCP
<a name="bk_StartWithScp"> </a>

Los extremos de detección automática que proceden de una [búsqueda de SCP](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) deben tener prioridad superior en la lista. Los administradores pueden configurar objetos SCP para enrutar a su cliente al extremo de detección automática más cercano o más eficaz, por lo que es una buena idea de comenzar con estos extremos. Debido a que el proceso de búsqueda de SCP tiene su propio esquema de asignación de prioridades, los resultados de una búsqueda de SCP son ya prioriza, como se indica a continuación: 
  
1. Extremos de detección automática de objetos SCP en el ámbito del sitio de Active Directory al que pertenece el equipo cliente.
    
2. Extremos de detección automática de objetos SCP no el ámbito de cualquier sitio de Active Directory.
    
3. Extremos de detección automática de objetos SCP el ámbito de un sitio de Active Directory diferente que el sitio al que pertenece el equipo cliente.
    
Una vez que tenga los resultados del proceso de búsqueda de SCP, puede agregar extremos que se derivan de la dirección de correo electrónico del usuario. Éstos pueden servir como un valor predeterminado del conjunto de extremos y de reserva en caso de que no hay ningún resultado de la SCP o los extremos devueltos por la búsqueda de SCP no son suficientes.
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a>Agregar extremos derivados de dirección de correo electrónico del usuario
<a name="bk_AddDerivedEndpoints"> </a>

Cuando no funciona la búsqueda de SCP o los extremos devueltos por la búsqueda de SCP no devuelven una respuesta correcta, puede derivar un conjunto de extremos de detección automática predeterminada de dirección de correo electrónico del usuario. Estos extremos deben ser una prioridad menor que los que proceden de una búsqueda de SCP, pero es posible que necesite si la búsqueda de SCP no se realizó correctamente.
  
### <a name="to-derive-autodiscover-endpoints"></a>Para derivar los extremos de detección automática

1. Extraer el nombre de dominio de la dirección de correo electrónico del usuario. Por ejemplo, si la dirección de correo electrónico del usuario es Sadie.Daniels@contoso.com, el nombre de dominio sería contoso.com.
    
2. Construir direcciones URL de extremo sin extensiones de archivo en los siguientes formatos:
    
  - "https://" + dominio + "/ detección automática y detección automática"
    
  - "https://autodiscover." + dominio + "/ detección automática y detección automática"
    
Después de compilar la lista de direcciones URL de extremo que se derivan de búsqueda de SCP y dirección de correo electrónico del usuario, es posible que deba revisar las extensiones de nombre de archivo en esas direcciones URL, dependiendo de si está utilizando el [servicio web de detección automática de SOAP](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) o la [POX Servicio web de detección automática](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a>Agregar o reemplazar las extensiones de nombre de archivo en las direcciones URL de extremo
<a name="bk_FileExtensions"> </a>

El servicio Detección automática, puede acceder mediante el servicio web de detección automática de SOAP o el servicio web de detección automática de POX. Cada servicio usa direcciones URL de extremo similar, con la única diferencia que se va a la extensión de nombre de archivo. El servicio web de detección automática de SOAP utiliza la extensión de nombre de archivo "SVC", y el servicio web de detección automática de POX utiliza la extensión de nombre de archivo ".xml".
  
De forma predeterminada, el extremo de detección automática devuelven las direcciones URL de una búsqueda de SCP son direcciones URL de POX. Sin embargo, si usa la detección automática de SOAP, simplemente puede cambiar la extensión de nombre de archivo de ".xml" a "SVC" y probar una solicitud SOAP.
  
Para las direcciones URL derivadas extremo de detección automática, se omite la extensión de archivo. Agregue la extensión de archivo apropiada para el servicio web de detección automática que usa antes de intentar la dirección URL.
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a>Ejemplo: Generación de una lista de extremos de detección automática
<a name="bk_Example"> </a>

Vamos a echar un vistazo a un ejemplo. Sadie Daniels (Sadie.Daniels@contoso.com) está usando una aplicación de servicios Web de Exchange (EWS) por primera vez. La aplicación utiliza la detección automática para que se configure. Equipo de Sadie está unido al dominio contoso.com y se encuentra en el sitio de Redmond Active Directory. La aplicación genera la lista de extremos de detección automática que se muestra en la figura 1.
  
**La figura 1: Lista ejemplo de extremos de detección automática**

![Lista de ejemplo de extremos de detección automática, que muestra los extremos obtenidos de la búsqueda de SCP que presentan mayor prioridad que los extremos derivados.](media/Ex15_Autodiscover_GenerateList_Example.png)
  
La aplicación de EWS en este ejemplo, prefiere el servicio web de detección automática de SOAP, por lo que cambia la extensión de nombre de archivo para los resultados de la SCP a "SVC" antes de enviar solicitudes SOAP a ellos.
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_NextSteps"> </a>

Después de generar una lista de extremos de detección automática, intente enviando [solicitudes a esos extremos](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="see-also"></a>Ver también


- [Detección automática de Exchange](autodiscover-for-exchange.md)
    
- [Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    

