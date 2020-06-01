---
title: Operación UpdateItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: La operación UpdateItem se usa para actualizar las propiedades de los elementos de tarea en el almacén de Exchange.
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459808"
---
# <a name="updateitem-operation-task"></a><span data-ttu-id="7060b-103">Operación UpdateItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="7060b-103">UpdateItem operation (task)</span></span>

<span data-ttu-id="7060b-104">La operación UpdateItem se usa para actualizar las propiedades de los elementos de tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7060b-104">The UpdateItem operation is used to update task item properties in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7060b-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7060b-105">Remarks</span></span>

<span data-ttu-id="7060b-106">No puede usar los servicios web Exchange para enviar solicitudes de tareas.</span><span class="sxs-lookup"><span data-stu-id="7060b-106">You cannot use Exchange Web Services to send task requests.</span></span> <span data-ttu-id="7060b-107">Los servicios Web de Exchange pueden devolver solicitudes de tareas creadas por MicrosoftOfficeOutlook.</span><span class="sxs-lookup"><span data-stu-id="7060b-107">Exchange Web Services can return task requests that are created by MicrosoftOfficeOutlook.</span></span> <span data-ttu-id="7060b-108">Si ya se ha enviado una solicitud de tarea, una solicitud para actualizar la tarea devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="7060b-108">If a task request has already been sent, a request to update the task will return an error.</span></span>
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a><span data-ttu-id="7060b-109">Actualización de la ocurrencia actual de una tarea recurrente</span><span class="sxs-lookup"><span data-stu-id="7060b-109">Updating the Current Occurrence of a Recurring Task</span></span>

<span data-ttu-id="7060b-110">El resultado de una operación UpdateItem en tareas periódicas difiere del resultado de la operación UpdateItem en una sola tarea recurrente.</span><span class="sxs-lookup"><span data-stu-id="7060b-110">The result of an UpdateItem operation on recurring tasks differs from the result of the UpdateItem operation on a single, nonrecurring task.</span></span> <span data-ttu-id="7060b-111">Los cambios en una ocurrencia de una tarea repetitiva provocan que las tareas de uso único se generen cuando se realicen las siguientes actualizaciones:</span><span class="sxs-lookup"><span data-stu-id="7060b-111">Changes to an occurrence of a recurring task cause one-off tasks to be generated when the following updates are made:</span></span>
  
1. <span data-ttu-id="7060b-112">La propiedad status de una tarea regenerada o nonregenerating recurrente se establece en **completada**.</span><span class="sxs-lookup"><span data-stu-id="7060b-112">The status property of a regenerating or nonregenerating recurrent task is set to **Completed**.</span></span>
    
2. <span data-ttu-id="7060b-113">Se cambia la fecha de inicio o la fecha de finalización de una tarea periódica nonregenerating.</span><span class="sxs-lookup"><span data-stu-id="7060b-113">The start date or end date of a nonregenerating recurrent task is changed.</span></span>
    
<span data-ttu-id="7060b-114">Por ejemplo, si una solicitud de **UpdateItem** establece el valor completado de una tarea recurrente en **true**, el **UpdateItemResponse** incluirá un nuevo identificador y changekey que representan una tarea de un solo uso recién creada.</span><span class="sxs-lookup"><span data-stu-id="7060b-114">For example, if an **UpdateItem** request sets the Completed value of a recurring task to **true**, the **UpdateItemResponse** will include a new Id and ChangeKey that represent a newly created one-off task.</span></span> <span data-ttu-id="7060b-115">El identificador que se incluyó en la solicitud sigue siendo válido y la tarea recurrente representada por ese identificador se ha actualizado para representar la siguiente ocurrencia.</span><span class="sxs-lookup"><span data-stu-id="7060b-115">The Id that was included in the request is still valid and the recurring task that is represented by that Id has been updated to represent the next occurrence.</span></span> <span data-ttu-id="7060b-116">La ChangeKey que se incluyó en la solicitud ya no es válida porque se ha actualizado la tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="7060b-116">The ChangeKey that was included in the request is no longer valid because the recurring task has been updated.</span></span> 
  
<span data-ttu-id="7060b-117">Puede usar la [operación GetItem](getitem-operation.md) para obtener el último **changekey** de la tarea repetitiva.</span><span class="sxs-lookup"><span data-stu-id="7060b-117">You can use the [GetItem operation](getitem-operation.md) to get the latest **ChangeKey** for the recurring task.</span></span> 
  
<span data-ttu-id="7060b-118">Para las tareas no periódicas o para la última repetición de una tarea repetitiva, la respuesta UpdateItem devuelve el mismo **identificador** que se pasó y devuelve el **changekey**actualizado asociado.</span><span class="sxs-lookup"><span data-stu-id="7060b-118">For nonrecurring tasks or for the last occurrence of a recurring task, the UpdateItem response returns the same **Id** that was passed to it and returns the associated updated **ChangeKey**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7060b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7060b-119">See also</span></span>



[<span data-ttu-id="7060b-120">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="7060b-120">UpdateItem operation</span></span>](updateitem-operation.md)

