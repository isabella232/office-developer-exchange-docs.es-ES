---
title: Requisitos de redistribución de la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: Descubra cómo puede redistribuir los ensamblados de LA API administrada ews con la aplicación.
ms.openlocfilehash: f43156838c735cfc17106deb7860329d3da6c07a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531333"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>Requisitos de redistribución de la API administrada de EWS

Descubra cómo puede redistribuir los ensamblados de LA API administrada ews con la aplicación.
  
A medida que diseñe la aplicación de LA API administrada de EWS, también tendrá en cuenta cómo la liberará a los usuarios. 
  
## <a name="redistributing-your-ews-managed-api-application"></a>Redistribuir la aplicación de LA API administrada de EWS

A menos que la aplicación se encuentra en el Exchange, deberá redistribuir los ensamblados de la API administrada ews. La descarga de la API administrada ews contiene dos ensamblados que puede redistribuir: Microsoft.Exchange.WebServices.dll y Microsoft.Exchange.WebServices.Auth.dll. Tenga en cuenta la siguiente información al diseñar cómo liberará la aplicación de LA API administrada ews:
  
- La API administrada ews se diseñó de forma que pueda descargarla y distribuirla con la aplicación destinada a un Exchange servidor. Como alternativa, la aplicación puede descargar la API administrada de EWS.
    
- Puede usar la API administrada ews para comunicarse con un servidor de Exchange que ejecute Exchange Online, Exchange Online como parte de Office 365 o una versión local de Exchange a partir de Exchange Server 2007.
    
- En las versiones de la API administrada ews a partir de la versión 2.1, puede instalar la API en la caché global de ensamblados (GAC). MSI agregará automáticamente el DLL a la GAC y será accesible por equipo, no por usuario.
    
Los términos de licencia se incluyen en la descarga de la API administrada de EWS. Revise los términos de la información relevante acerca de lo que puede hacer con la API administrada ews.
  
## <a name="see-also"></a>Ver también


- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [API administrada ews (descarga)](https://aka.ms/ews-managed-api-readme)
    

