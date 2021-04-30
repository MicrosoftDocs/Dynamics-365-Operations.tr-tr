---
title: İş ayrıntısı API'sı
description: Bu konu, Dynamics 365 Human Resources'taki İş ayrıntısı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f15282bf72340cb1a832ff3264361472d0a6c70
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882093"
---
# <a name="job-detail-api"></a><span data-ttu-id="fe536-103">İş ayrıntısı API'sı</span><span class="sxs-lookup"><span data-stu-id="fe536-103">Job detail API</span></span>

<span data-ttu-id="fe536-104">Bu konu, Dynamics 365 Human Resources'taki İş ayrıntısı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe536-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="fe536-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="fe536-105">Properties</span></span>

| <span data-ttu-id="fe536-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="fe536-106">Property</span></span><br><span data-ttu-id="fe536-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="fe536-107">**Physical name**</span></span><br><span data-ttu-id="fe536-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="fe536-108">**_Type_**</span></span> | <span data-ttu-id="fe536-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="fe536-109">Use</span></span> | <span data-ttu-id="fe536-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe536-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fe536-111">**İş Kodu**</span><span class="sxs-lookup"><span data-stu-id="fe536-111">**Job ID**</span></span><br><span data-ttu-id="fe536-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="fe536-112">mshr_jobid</span></span><br><span data-ttu-id="fe536-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="fe536-113">*String*</span></span> | <span data-ttu-id="fe536-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="fe536-114">Read-only</span></span><br><span data-ttu-id="fe536-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="fe536-115">Required</span></span> | <span data-ttu-id="fe536-116">Bir iş için benzersiz kimlik.</span><span class="sxs-lookup"><span data-stu-id="fe536-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="fe536-117">**Piyasa fiyatı alt eşiği**</span><span class="sxs-lookup"><span data-stu-id="fe536-117">**Market price low threshold**</span></span><br><span data-ttu-id="fe536-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="fe536-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="fe536-119">*Ondalık*</span><span class="sxs-lookup"><span data-stu-id="fe536-119">*Decimal*</span></span> | | <span data-ttu-id="fe536-120">Pozisyonu benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="fe536-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
