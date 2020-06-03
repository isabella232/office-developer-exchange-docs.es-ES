---
title: Referencia de clase función cchksgfiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Busque información de referencia para la API de CHKSGFILES en Exchange 2013.
ms.openlocfilehash: 38b1f2c900767c22594636f0c6ddf4855961aec4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526735"
---
# <a name="cchksgfiles-class-reference"></a>Referencia de clase función cchksgfiles

Busque información de referencia para la API de CHKSGFILES en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
La API CHKSGFILES permite que las aplicaciones de copia de seguridad y restauración comprueben la integridad de las bases de datos y los archivos de registro de transacciones de Exchange Server 2013 mediante programación. Puede usar esta API en las aplicaciones de copia de seguridad y restauración que usan el servicio de instantáneas de volumen (VSS).
  
> [!NOTE]
> Los grupos de almacenamiento no están disponibles en Exchange 2013. La compatibilidad con grupos de almacenamiento se ha quitado de las versiones de Exchange a partir de Exchange Server 2010. Para la compatibilidad con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange 2010, la API CHKSGFILES permite especificar grupos de almacenamiento. Cuando ejecuta CHKSGFILES en bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento en una cadena vacía. 
  
## <a name="file-location"></a>Ubicación del archivo
<a name="bk_fileslocation"> </a>

La API CHKSGFILES se incluye como parte de Exchange 2013. Puede usar esta API en un equipo que tenga instalado el rol de servidor buzón de correo. 
  
De forma predeterminada, la DLL CHKSGFILES se instala en el directorio C:\Program Files\Microsoft\Exchange\V15\Bin.
  
Exchange 2013 incluye solo una versión de 64 bits (amd64) de la API CHKSGFILES. 
  
Puede descargar un archivo. zip que incluya la biblioteca CHKSGFILE. lib y los archivos de encabezado CHKSGFILES. HXX para usarlos en la aplicación personalizada desde el [centro de descarga de Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).
  
## <a name="development-languages"></a>Lenguajes de desarrollo
<a name="bk_developmentlanguages"> </a>

La API de CHKSGFILES está pensada para usarse con versiones de Visual Studio que comienzan con Visual Studio 2005 en C/C++ nativo. La API de CHKSGFILES no está pensada para su uso en código administrado. Aunque se puede crear un ensamblado de interoperabilidad COM con CHKSGFILES, no se incluye un ensamblado de interoperabilidad COM compatible con Exchange 2013.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Función función cchksgfiles. CMaxDbPerSG](cchksgfiles-cmaxdbpersg-function.md)
    
- [Función función cchksgfiles. Delete](cchksgfiles-delete-function.md)
    
- [Enumeración función cchksgfiles. ERR](cchksgfiles-err-enumeration.md)
    
- [Función función cchksgfiles. ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md)
    
- [Función función cchksgfiles. ErrCheckDbPages](cchksgfiles-errcheckdbpages-function.md)
    
- [Función función cchksgfiles. ErrCheckLogs](cchksgfiles-errchecklogs-function.md)
    
- [Función función cchksgfiles. ErrGetHeader (reservada)](cchksgfiles-errgetheader-function-reserved.md)
    
- [Función función cchksgfiles. ErrInit](cchksgfiles-errinit-function.md)
    
- [Función función cchksgfiles. ErrTerm](cchksgfiles-errterm-function.md)
    
- [Enumeración función cchksgfiles. iDbInvalid](cchksgfiles-idbinvalid-enumeration.md)
    
- [Función función cchksgfiles. New](cchksgfiles-new-function.md)
    
- [Enumeración función cchksgfiles. NO_FLAGS](cchksgfiles-no_flags-enumeration.md)
    
- [Struct función cchksgfiles. PAGE_INFO](cchksgfiles-page_info-struct.md)
    
- [Función función cchksgfiles. PgnoFromFileOffset](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md)
- [Copia de seguridad, restauración y recuperación ante desastres](https://technet.microsoft.com/library/dd876874)
    

