---
title: Referencia de clase CChkSGFiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Busque información de referencia para la API CHKSGFILES en Exchange 2013.
ms.openlocfilehash: 583ac5e16ab60d119c3028bf81123e9f60a58ff4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19762979"
---
# <a name="cchksgfiles-class-reference"></a>Referencia de clase CChkSGFiles

Busque información de referencia para la API CHKSGFILES en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
La API de CHKSGFILES permite a las aplicaciones de copia de seguridad y restauración comprobar la integridad de los archivos de registro de transacciones de Exchange Server 2013 y las bases de datos mediante programación. Puede usar esta API en copia de seguridad y restauración de las aplicaciones que usan el servicio de instantáneas de volumen (VSS).
  
> [!NOTE]
> Grupos de almacenamiento no están disponibles en Exchange 2013. Compatibilidad con grupos de almacenamiento se ha quitado de las versiones de Exchange a partir de Exchange Server 2010. Para la compatibilidad con versiones anteriores con las bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange 2010, la API de CHKSGFILES permite especificar grupos de almacenamiento. Cuando ejecuta CHKSGFILES frente a las bases de datos de Exchange 2013, debe establecer los parámetros que especifican un identificador de grupo de almacenamiento de información en una cadena vacía. 
  
## <a name="file-location"></a>Ubicación de archivo
<a name="bk_fileslocation"> </a>

La API CHKSGFILES se distribuye como parte de Exchange 2013. Puede usar esta API en un equipo que tenga instalado el rol de servidor de buzón de correo. 
  
De forma predeterminada, la DLL de CHKSGFILES está instalada en el directorio C:\Program Files\Microsoft\Exchange\V15\Bin.
  
Exchange 2013 incluye sólo una versión de 64 bits (amd64) de la API CHKSGFILES. 
  
Puede descargar un archivo .zip que incluye la biblioteca de CHKSGFILE.lib y los archivos de encabezado de CHKSGFILES.hxx para su uso en la aplicación personalizada desde el [Centro de descarga de Microsoft](http://www.microsoft.com/en-us/download/details.aspx?id=36802).
  
## <a name="development-languages"></a>Lenguajes de desarrollo
<a name="bk_developmentlanguages"> </a>

La API CHKSGFILES está pensada para su uso con las versiones de Visual Studio desde Visual Studio 2005 en C o C++ nativo. La API CHKSGFILES no está pensada para su uso en código administrado. Aunque se puede crear un ensamblado de interoperabilidad COM con CHKSGFILES, no ofrecemos un ensamblado de interoperabilidad COM compatible con Exchange 2013.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG (función)](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete (función)](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR (enumeración)](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders (función)](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages (función)](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs (función)](cchksgfiles-errchecklogs-function.md)
    
- [Función CChkSGFiles.ErrGetHeader (reservado)](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit (función)](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm (función)](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid (enumeración)](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New (función)](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS (enumeración)](cchksgfiles-no_flags-enumeration.md)
    
- [Estructura de CChkSGFiles.PAGE_INFO](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset (función)](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md)
- [Copia de seguridad, restauración y recuperación ante desastres](http://technet.microsoft.com/en-us/library/dd876874)
    

