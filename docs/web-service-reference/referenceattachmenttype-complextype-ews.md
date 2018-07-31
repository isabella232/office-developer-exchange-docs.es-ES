---
title: ReferenceAttachmentType complexType (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: c53686ccd032cabcc3f64a3a6684f29afe63a9b1
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354179"
---
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="21227-102">ReferenceAttachmentType complexType (EWS)</span><span class="sxs-lookup"><span data-stu-id="21227-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="21227-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="21227-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21227-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21227-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21227-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="21227-105">**Schema file**</span></span> <br/> |<span data-ttu-id="21227-106">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21227-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="21227-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="21227-107">**Extension base**</span></span> <br/> |<span data-ttu-id="21227-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="21227-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21227-109">Definición</span><span class="sxs-lookup"><span data-stu-id="21227-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="21227-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="21227-110">Elements and attributes</span></span>

<span data-ttu-id="21227-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="21227-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="21227-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21227-112">Child elements</span></span>

|<span data-ttu-id="21227-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="21227-113">**Element**</span></span>|<span data-ttu-id="21227-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="21227-114">**Type**</span></span>|<span data-ttu-id="21227-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21227-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21227-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="21227-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="21227-117">xs:string</span><span class="sxs-lookup"><span data-stu-id="21227-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="21227-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="21227-118">Attributes</span></span>

<span data-ttu-id="21227-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21227-119">None.</span></span>
  

