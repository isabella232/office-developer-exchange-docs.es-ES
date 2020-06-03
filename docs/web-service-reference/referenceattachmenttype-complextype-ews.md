---
title: ReferenceAttachmentType complexType (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: 24f5a62eadd490b5b0000dfe048850c44540f266
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528737"
---
# <a name="referenceattachmenttype-complextype-ews"></a>ReferenceAttachmentType complexType (EWS)

## <a name="type-information"></a>Información de tipos

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|**Archivo de esquema** <br/> |Types. xsd  <br/> |
|**Base de extensión** <br/> |t:AttachmentType  <br/> |
   
## <a name="definition"></a>Definición

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## <a name="elements-and-attributes"></a>Elementos y atributos

Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición. 
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|[AttachLongPathName](attachlongpathname.md) <br/> |XS: String  <br/> ||
   
### <a name="attributes"></a>Atributos

Ninguno.
  

