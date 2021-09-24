---
title: Referencia de la clase CChkSGFiles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Busque información de referencia para la API CHKSGFILES en Exchange 2013.
ms.openlocfilehash: 2daf31c41a47684b85ede196b415884335c3ca79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510536"
---
# <a name="cchksgfiles-class-reference"></a>Referencia de la clase CChkSGFiles

Busque información de referencia para la API CHKSGFILES en Exchange 2013.
  
**Se aplica a:** Exchange Server 2013 
  
La API CHKSGFILES permite que las aplicaciones de copia de seguridad y restauración comprueben la integridad de Exchange Server y bases de datos del registro de transacciones de 2013 mediante programación. Puede usar esta API en las aplicaciones de copia de seguridad y restauración que usan el Servicio de instantáneas de volumen (VSS).
  
> [!NOTE]
> Storage no están disponibles en Exchange 2013. La compatibilidad con grupos de almacenamiento se quitó de las versiones de Exchange a partir Exchange Server 2010. Para la compatibilidad con versiones anteriores con bases de datos y grupos de almacenamiento en versiones de Exchange anteriores a Exchange 2010, la API chksgfiles permite especificar grupos de almacenamiento. Al ejecutar CHKSGFILES en Exchange bases de datos de 2013, debe establecer parámetros que especifiquen un identificador de grupo de almacenamiento en una cadena vacía. 
  
## <a name="file-location"></a>Ubicación del archivo
<a name="bk_fileslocation"> </a>

La API CHKSGFILES se incluye como parte de Exchange 2013. Puede usar esta API en un equipo que tenga instalada la función de servidor Buzón de correo. 
  
De forma predeterminada, la DLL CHKSGFILES está instalada en el directorio C:\Program Files\Microsoft\Exchange\V15\Bin.
  
Exchange 2013 incluye solo una versión de 64 bits (amd64) de la API CHKSGFILES. 
  
Puede descargar un archivo .zip que incluya la biblioteca CHKSGFILE.lib y los archivos de encabezado CHKSGFILES.hxx para su uso en la aplicación personalizada desde el Centro de descarga de [Microsoft](https://www.microsoft.com/download/details.aspx?id=36802).
  
## <a name="development-languages"></a>Idiomas de desarrollo
<a name="bk_developmentlanguages"> </a>

La API CHKSGFILES está diseñada para su uso con versiones de Visual Studio a partir de Visual Studio 2005 en C/C++nativo. La API CHKSGFILES no está diseñada para su uso en código administrado. Aunque puede crear un ensamblado de interoperabilidad COM con CHKSGFILES, no se envía un ensamblado de interoperabilidad COM compatible con Exchange 2013.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Función CChkSGFiles.CMaxDbPerSG](cchksgfiles-cmaxdbpersg-function.md)
    
- [Función CChkSGFiles.Delete](cchksgfiles-delete-function.md)
    
- [Enumeración CChkSGFiles.ERR](cchksgfiles-err-enumeration.md)
    
- [Función CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md)
    
- [Función CChkSGFiles.ErrCheckDbPages](cchksgfiles-errcheckdbpages-function.md)
    
- [Función CChkSGFiles.ErrCheckLogs](cchksgfiles-errchecklogs-function.md)
    
- [Función CChkSGFiles.ErrGetHeader (reservada)](cchksgfiles-errgetheader-function-reserved.md)
    
- [Función CChkSGFiles.ErrInit](cchksgfiles-errinit-function.md)
    
- [Función CChkSGFiles.ErrTerm](cchksgfiles-errterm-function.md)
    
- [Enumeración CChkSGFiles.iDbInvalid](cchksgfiles-idbinvalid-enumeration.md)
    
- [Función CChkSGFiles.New](cchksgfiles-new-function.md)
    
- [Enumeración CChkSGFiles.NO_FLAGS](cchksgfiles-no_flags-enumeration.md)
    
- [Estructura CChkSGFiles.PAGE_INFO](cchksgfiles-page_info-struct.md)
    
- [Función CChkSGFiles.PgnoFromFileOffset](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>Ver también

- [Desarrollo de Exchange y Exchange Online](../exchange-server-development.md)
- [Copia de seguridad, restauración y recuperación ante desastres](https://technet.microsoft.com/library/dd876874)
    

