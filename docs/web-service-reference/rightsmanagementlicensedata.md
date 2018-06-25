---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: El elemento RightsManagementLicenseData especifica información acerca de la licencia de administración de derechos para un elemento.
ms.openlocfilehash: ec2ba1dc155afe239c499246095f86fc621910a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837234"
---
# <a name="rightsmanagementlicensedata"></a><span data-ttu-id="dc5b4-103">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="dc5b4-103">RightsManagementLicenseData</span></span>

<span data-ttu-id="dc5b4-104">El elemento **RightsManagementLicenseData** especifica información acerca de la licencia de administración de derechos para un elemento.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-104">The **RightsManagementLicenseData** element specifies information about the rights management license for an item.</span></span> 
  
```XML
<RightsManagementLicenseData>
   <RightsManagedMessageDecryptionStatus/>
   <RmsTemplateId/>
   <TemplateName/>
   <TemplateDescription/>
   <EditAllowed/>
   <ReplyAllowed/>
   <ReplyAllAllowed/>
   <ForwardAllowed/>
   <ModifyRecipientsAllowed/>
   <ExtractAllowed/>
   <PrintAllowed/>
   <ExportAllowed/>
   <ProgrammaticAccessAllowed/>
   <IsOwner/>
   <ContentOwner/>
   <ContentExpiryDate/>
</RightsManagementLicenseData>
```

 <span data-ttu-id="dc5b4-105">**RightsManagementLicenseDataType**</span><span class="sxs-lookup"><span data-stu-id="dc5b4-105">**RightsManagementLicenseDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc5b4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc5b4-106">Attributes and elements</span></span>

<span data-ttu-id="dc5b4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc5b4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc5b4-108">Attributes</span></span>

<span data-ttu-id="dc5b4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc5b4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc5b4-110">Child elements</span></span>

<span data-ttu-id="dc5b4-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [RMSTemplateId](rmstemplateid.md) | [TemplateName](templatename.md) | [DescripciónPlantilla](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md)  |  [ ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md)  |  [ ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span><span class="sxs-lookup"><span data-stu-id="dc5b4-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [RMSTemplateId](rmstemplateid.md) | [TemplateName](templatename.md) | [TemplateDescription](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md) | [ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md) | [ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc5b4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dc5b4-112">Parent elements</span></span>

<span data-ttu-id="dc5b4-113">[Elemento](item.md) | [mensaje](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [tarea](task.md) | [PostItem ](postitem.md)  |  [CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="dc5b4-113">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc5b4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc5b4-114">Remarks</span></span>

<span data-ttu-id="dc5b4-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc5b4-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc5b4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc5b4-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dc5b4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc5b4-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc5b4-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc5b4-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dc5b4-119">Schema name</span></span>  <br/> |<span data-ttu-id="dc5b4-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="dc5b4-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc5b4-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dc5b4-121">Validation file</span></span>  <br/> |<span data-ttu-id="dc5b4-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc5b4-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc5b4-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dc5b4-123">Can be empty</span></span>  <br/> ||
   

