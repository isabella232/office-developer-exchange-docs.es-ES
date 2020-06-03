---
title: Requisitos de redistribución para la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Descubra cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
ms.openlocfilehash: e64b4cdb8938caa819ba30621112a25946ef0424
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463828"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Requisitos de redistribución para la API administrada de EWS

Descubra cómo puede redistribuir los ensamblados de la API administrada de EWS con su aplicación.
  
A medida que diseña la aplicación de la API administrada de EWS, también querrá tener en cuenta cómo se lanzará a los usuarios. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Redistribuir la aplicación de API administrada de EWS

A menos que la aplicación se encuentre en el servidor de Exchange, tendrá que redistribuir los ensamblados de la API administrada de EWS. La descarga de la API administrada de EWS contiene dos ensamblados que puede redistribuir: Microsoft. Exchange. webservices. dll y Microsoft. Exchange. webservices. auth. dll. Tenga en cuenta la siguiente información cuando diseñe el modo en que va a liberar la aplicación de la API administrada de EWS:
  
- La API administrada de EWS se diseñó para poder descargarla y distribuirla con la aplicación destinada a un servidor de Exchange. Como alternativa, la aplicación puede descargar la API administrada de EWS.
    
- Puede usar la API administrada de EWS para comunicarse con un servidor de Exchange que ejecuta Exchange Online, Exchange online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2007.
    
- En las versiones de la API administrada de EWS a partir de la versión 2,1, puede instalar la API en la memoria caché de ensamblados global (GAC). El MSI agregará automáticamente el archivo DLL a la GAC y será accesible por equipo, no por cada usuario.
    
Los términos de licencia se incluyen en la descarga de la API administrada de EWS. Revise los términos de la información autoritativa sobre lo que puede hacer con la API administrada de EWS.
  
## <a name="see-also"></a>Vea también


- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [API administrada de EWS (descargar)](https://aka.ms/ews-managed-api-readme)
    

