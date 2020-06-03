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
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="614da-102">ReferenceAttachmentType complexType (EWS)</span><span class="sxs-lookup"><span data-stu-id="614da-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="614da-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="614da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="614da-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="614da-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="614da-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="614da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="614da-106">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="614da-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="614da-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="614da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="614da-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="614da-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="614da-109">Definición</span><span class="sxs-lookup"><span data-stu-id="614da-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="614da-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="614da-110">Elements and attributes</span></span>

<span data-ttu-id="614da-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="614da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="614da-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="614da-112">Child elements</span></span>

|<span data-ttu-id="614da-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="614da-113">**Element**</span></span>|<span data-ttu-id="614da-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="614da-114">**Type**</span></span>|<span data-ttu-id="614da-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="614da-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="614da-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="614da-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="614da-117">XS: String</span><span class="sxs-lookup"><span data-stu-id="614da-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="614da-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="614da-118">Attributes</span></span>

<span data-ttu-id="614da-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="614da-119">None.</span></span>
  

