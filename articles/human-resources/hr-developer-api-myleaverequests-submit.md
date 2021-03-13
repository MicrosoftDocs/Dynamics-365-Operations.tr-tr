---
title: Bir izin isteğini iş akışına gönderme
description: Microsoft Dynamics 365 Human Resources'ta, iş akışına bırakma isteği göndermek için MyLeaveRequests Submit () uygulama programlama arabirimini (API) kullanabilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be70edbe1439340377fd01b9760d49d3a75348
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115524"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="7a54c-103">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="7a54c-103">Submit a leave request to workflow</span></span>

<span data-ttu-id="7a54c-104">Microsoft Dynamics 365 Human Resources'ta, iş akışına bırakma isteği göndermek için MyLeaveRequests Submit () uygulama programlama arabirimini (API) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a54c-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="7a54c-105">Bu API, MyLeaveRequests OData varlığı üzerinde bir eylem olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="7a54c-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a54c-106">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7a54c-106">Prerequisites</span></span>

<span data-ttu-id="7a54c-107">İzin isteği veritabanına kaydedilmelidir ve MyLeaveRequests varlığı aracılığıyla alınabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a54c-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="7a54c-108">İzinler</span><span class="sxs-lookup"><span data-stu-id="7a54c-108">Permissions</span></span>

<span data-ttu-id="7a54c-109">Bu API 'YI çağırmak için aşağıdaki izinlerden biri gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="7a54c-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7a54c-110">İzinler ve bunların seçilmesi hakkında daha fazla bilgi için, bkz [Kimlik doğrulama](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="7a54c-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="7a54c-111">İzin türü</span><span class="sxs-lookup"><span data-stu-id="7a54c-111">Permission type</span></span>                    | <span data-ttu-id="7a54c-112">İzinler (en az ayrıcalıklı-büyük ayrıcalıklı)</span><span class="sxs-lookup"><span data-stu-id="7a54c-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7a54c-113">Yetkilendirilen (İş veya okul hesabı)</span><span class="sxs-lookup"><span data-stu-id="7a54c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="7a54c-114">Kullanıcı\_kimliğine bürünme</span><span class="sxs-lookup"><span data-stu-id="7a54c-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="7a54c-115">HTTPS isteği</span><span class="sxs-lookup"><span data-stu-id="7a54c-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="7a54c-116">İstek OData standartlarına uygun.</span><span class="sxs-lookup"><span data-stu-id="7a54c-116">The request conforms to OData standards.</span></span> <span data-ttu-id="7a54c-117">{requestId}, {leaveType}, {leaveDate} ve {dataArea} parametreleri, MyLeaveRequests varlığı için bileşik doğal anahtarı oluşturan alanlara başvuruda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="7a54c-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="7a54c-118">MyLeaveRequests varlığının alanları izin talebindeki tek bir satıra başvuruda bulunduğu sürece, API gönder çağrısı, tüm izin vermez isteği (tüm satırlar) iş akışına gönderir.</span><span class="sxs-lookup"><span data-stu-id="7a54c-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="7a54c-119">İstek başlıkları</span><span class="sxs-lookup"><span data-stu-id="7a54c-119">Request headers</span></span>

| <span data-ttu-id="7a54c-120">Başlık</span><span class="sxs-lookup"><span data-stu-id="7a54c-120">Header</span></span>         | <span data-ttu-id="7a54c-121">Value</span><span class="sxs-lookup"><span data-stu-id="7a54c-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="7a54c-122">Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="7a54c-122">Authorization</span></span>  | <span data-ttu-id="7a54c-123">Taşıyıcı {token} (gerekli)</span><span class="sxs-lookup"><span data-stu-id="7a54c-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="7a54c-124">İçerik Türü</span><span class="sxs-lookup"><span data-stu-id="7a54c-124">Content-Type</span></span>   | <span data-ttu-id="7a54c-125">Uygulama/json</span><span class="sxs-lookup"><span data-stu-id="7a54c-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="7a54c-126">İstek gövdesi</span><span class="sxs-lookup"><span data-stu-id="7a54c-126">Request body</span></span>

<span data-ttu-id="7a54c-127">Bu yöntem için bir istek gövdesi sağlamamalısınız.</span><span class="sxs-lookup"><span data-stu-id="7a54c-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="7a54c-128">Yanıt</span><span class="sxs-lookup"><span data-stu-id="7a54c-128">Response</span></span>

<span data-ttu-id="7a54c-129">Başarılı bir yanıt, her zaman **204 içerik yok** yanıtıdır.</span><span class="sxs-lookup"><span data-stu-id="7a54c-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="7a54c-130">Yetkisiz arayıcılar **401 izinsiz** veya **403 Yasak** yanıt alır.</span><span class="sxs-lookup"><span data-stu-id="7a54c-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="7a54c-131">Gönderme işlemi başarısız olursa (örneğin, doğrulama nedeniyle), yanıt bir **500 sunucu hatası** olur ve yanıt gövdesinde daha ayrıntılı bir JSON nesnesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a54c-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="7a54c-132">Örnek</span><span class="sxs-lookup"><span data-stu-id="7a54c-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="7a54c-133">Doğrulama ve hata iletileri</span><span class="sxs-lookup"><span data-stu-id="7a54c-133">Validation and error messages</span></span>

<span data-ttu-id="7a54c-134">Gönderme API'sine yapılan çağrının bir parçası olarak İnsan Kaynakları gönderme işleminden önce iş mantığı doğrulaması yapar ve bu da bırakma isteğinin gönderme için geçerli bir durumda olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a54c-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="7a54c-135">Doğrulama başarısız olursa yanıt olarak alabileceğiniz olası hata iletileri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7a54c-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="7a54c-136">Talep '{LeaveTypeId}' bakiyesini {date} tarihinde izin verilen minimum bakiyenin altına indirecek.</span><span class="sxs-lookup"><span data-stu-id="7a54c-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="7a54c-137">Tamamlandı durumundaki istek süresi gönderilemez.</span><span class="sxs-lookup"><span data-stu-id="7a54c-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="7a54c-138">Hiçbir değişiklik yapılmadı olarak istek gönderilemiyor veya kaydedilemiyor.</span><span class="sxs-lookup"><span data-stu-id="7a54c-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="7a54c-139">Tutarı veya izin tipini ekleyin veya güncelleştirin ve yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="7a54c-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="7a54c-140">Girilen zaman isteği, aynı tarihle aynı tarihe sahip bir veya daha fazla gün içeriyor ve mevcut bekleyen istek olarak bu türü bırak.</span><span class="sxs-lookup"><span data-stu-id="7a54c-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="7a54c-141">Lütfen değişiklik yapmak için varolan isteği geri çekin.</span><span class="sxs-lookup"><span data-stu-id="7a54c-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="7a54c-142">'{ReasonCodeId}' neden kodu istekteki izin türlerinin hiçbiri için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="7a54c-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="7a54c-143">'{LeaveTypeId}' Çıkış türü neden kodu gerektiriyor.</span><span class="sxs-lookup"><span data-stu-id="7a54c-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="7a54c-144">Uygun türü ve neden kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7a54c-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="7a54c-145">Kapatma saati başarıyla gönderilmedi.</span><span class="sxs-lookup"><span data-stu-id="7a54c-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="7a54c-146">Kapatma zamanı taslak istek olarak kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="7a54c-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a54c-147">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7a54c-147">See also</span></span>

- [<span data-ttu-id="7a54c-148">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="7a54c-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="7a54c-149">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="7a54c-149">Authentication</span></span>](hr-developer-api-authentication.md)