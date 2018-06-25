---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: El elemento SmtpAddress representa la dirección de Protocolo Simple de transferencia de correo (SMTP) de una cuenta que se usará para la suplantación o una dirección de destinatario de Protocolo Simple de transferencia de correo (SMTP) de un calendario o un contacto solicitud para compartir.
ms.openlocfilehash: 39588f0892cdcec819a1972547155730be5785f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837511"
---
# <a name="smtpaddress"></a><span data-ttu-id="2e6b1-103">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="2e6b1-103">SmtpAddress</span></span>

<span data-ttu-id="2e6b1-104">El elemento **SmtpAddress** representa la dirección de Protocolo Simple de transferencia de correo (SMTP) de una cuenta que se usará para la suplantación o una dirección de destinatario de Protocolo Simple de transferencia de correo (SMTP) de un calendario o un contacto solicitud para compartir.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-104">The **SmtpAddress** element represents the Simple Mail Transfer Protocol (SMTP) address of an account to be used for impersonation or a Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span> 
  
```xml
<SmtpAddress/>
```

<span data-ttu-id="2e6b1-105">**SmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="2e6b1-105">**SmtpAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2e6b1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e6b1-106">Attributes and elements</span></span>

<span data-ttu-id="2e6b1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e6b1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e6b1-108">Attributes</span></span>

<span data-ttu-id="2e6b1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e6b1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e6b1-110">Child elements</span></span>

<span data-ttu-id="2e6b1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e6b1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e6b1-112">Parent elements</span></span>

|<span data-ttu-id="2e6b1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e6b1-113">**Element**</span></span>|<span data-ttu-id="2e6b1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e6b1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e6b1-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="2e6b1-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="2e6b1-116">Representa una cuenta para suplantar a cuando se usa el encabezado SOAP ExchangeImpersonation.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="2e6b1-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="2e6b1-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="2e6b1-118">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="2e6b1-118">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="2e6b1-119">Representa a un destinatario no válido para un uso compartido del calendario o un contacto mensaje para compartir.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-119">Represents an invalid recipient for a calendar sharing or contact sharing message.</span></span>  <br/> |
|[<span data-ttu-id="2e6b1-120">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="2e6b1-120">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="2e6b1-121">Representa una colección de destinatarios que se concederá acceso a la carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-121">Represents a collection of recipients that will be granted access to the shared folder.</span></span>  <br/> |
|[<span data-ttu-id="2e6b1-122">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="2e6b1-122">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="2e6b1-123">Define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-123">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e6b1-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2e6b1-124">Text value</span></span>

<span data-ttu-id="2e6b1-125">Se requiere un valor de texto que representa una dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-125">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e6b1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e6b1-126">Remarks</span></span>

<span data-ttu-id="2e6b1-127">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2e6b1-127">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e6b1-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e6b1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e6b1-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e6b1-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e6b1-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e6b1-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2e6b1-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e6b1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e6b1-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e6b1-132">Validation File</span></span>  <br/> |<span data-ttu-id="2e6b1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e6b1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e6b1-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e6b1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e6b1-135">False</span><span class="sxs-lookup"><span data-stu-id="2e6b1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e6b1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e6b1-136">See also</span></span>

- [<span data-ttu-id="2e6b1-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e6b1-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

