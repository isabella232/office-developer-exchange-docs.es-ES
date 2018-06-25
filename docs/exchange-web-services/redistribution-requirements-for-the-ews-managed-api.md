---
title: Requisitos de redistribución para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Obtenga información acerca de cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
ms.openlocfilehash: d8fc57c4a2b3ed7d6218aeeed0fe88c2d3e0fbe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763294"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Requisitos de redistribución para la API administrada de EWS

Obtenga información acerca de cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
  
Al diseñar la aplicación de la API administrada de EWS, también desea tener en cuenta cómo se liberará a los usuarios. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Redistribuir su aplicación de API administrada de EWS

A menos que la aplicación se encuentra en el servidor de Exchange, necesita redistribuir los ensamblados de la API administrada de EWS. La descarga de la API administrada de EWS contiene dos ensamblados que se pueden redistribuir: Microsoft.Exchange.WebServices.dll y Microsoft.Exchange.WebServices.Auth.dll. Cuando diseñe cómo se liberará a la aplicación de la API administrada de EWS, tenga en cuenta la información siguiente:
  
- La API administrada de EWS se ha diseñado para que puede descargarlo y distribuir con la aplicación que se dirige a un servidor de Exchange. Como alternativa, la aplicación puede descargar la API administrada de EWS.
    
- Puede usar la API administrada de EWS para comunicarse con un servidor de Exchange que ejecuta Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2007.
    
- En las versiones de la API administrada de EWS empezando con la versión 2.1, puede instalar la API en la caché de ensamblados Global (GAC). El archivo MSI agregará automáticamente el archivo DLL en la GAC y estará accesible en el equipo por equipo, no en cada usuario.
    
Los términos de licencia se incluyen en la descarga de la API administrada de EWS. Revise los términos para obtener la información relevante acerca de qué puede hacer con la API administrada de EWS.
  
## <a name="see-also"></a>Vea también


- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [API administrada de EWS (descarga)](http://aka.ms/ews-managed-api-readme)
    

