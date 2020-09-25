---
title: Kaynak kapasitesini eşitleme
description: Bu konu, bir kaynağın takvimler ve projelerde kapasitesini eşitleme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760682"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="f7849-103">Kaynak kapasitesini eşitleme</span><span class="sxs-lookup"><span data-stu-id="f7849-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7849-104">Kaynak eşitleme işlemleri, takvim ve temel takvim bilgilerini, proje kaynak planlamasına doğru çekilmesinin sağlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f7849-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="f7849-105">Takvim değiştirilse, işlemler proje kaynak planlama için gerekli güncelleştirmeleri yapar.</span><span class="sxs-lookup"><span data-stu-id="f7849-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="f7849-106">İşlemler performansı iyileştirmeye yardımcı olur çünkü takvimin kaynak bilgisi önceden eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="f7849-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="f7849-107">Bu nedenle, kaynak zamanlama bilgisine güncelleştirmeler daha hızlı gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="f7849-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="f7849-108">İşlemleri tek tek planlamak yerine toplu iş olarak planlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="f7849-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="f7849-109">Aksi halde, birisinin bilgiler son eşitlendiğinde dahil edilen tarihleri unutma riski vardır.</span><span class="sxs-lookup"><span data-stu-id="f7849-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="f7849-110">Dahil olan tarihler kullanılmazsa, tarih eşitleme sırasında boşluklar oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="f7849-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Takvim eşitleme](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="f7849-112">Kaynak kapasite toplamlarını eşitle</span><span class="sxs-lookup"><span data-stu-id="f7849-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="f7849-113">Eşitleme işlemi, tüm kaynak takvim bilgilerini eşitlemek üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f7849-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="f7849-114">Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki değişikliklerle ilgili temel takvim bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="f7849-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="f7849-115">Projeye yeni kaynaklar eklenirse, eşitleme güncellenen takvim bilgilerinin kullanılmasının sağlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f7849-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="f7849-116">Eşitleme herhangi bir zamanda yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="f7849-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="f7849-117">Toplu iş kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="f7849-117">We recommend that you use a batch.</span></span> <span data-ttu-id="f7849-118">Eşitleme sırasında kapasite rezervasyonunda seçenekler bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f7849-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="f7849-119">**Proje yönetimi ve muhasebe** &gt; **Periyodik** &gt; **Kapasite eşitleme** &gt; **Kaynakların kapasite toplamlarını eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f7849-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="f7849-120">Aşağıdaki tabloda seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f7849-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="f7849-121">Seçenek</span><span class="sxs-lookup"><span data-stu-id="f7849-121">Option</span></span>      | <span data-ttu-id="f7849-122">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7849-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="f7849-123">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="f7849-123">Period code</span></span> | <span data-ttu-id="f7849-124">İsteğe bağlı olarak Genel muhasebe tarihi aralık kodunu, kaynak kapasite yuvarlamaları için eşitleme işlemi için başlangıç ve bitiş tarihlerini ayarlamak için seçin.</span><span class="sxs-lookup"><span data-stu-id="f7849-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="f7849-125">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="f7849-125">Start date</span></span>  | <span data-ttu-id="f7849-126">Kaynak kapasite yuvarlamaları için eşitleme işlemi için başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="f7849-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="f7849-127">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="f7849-127">End date</span></span>    | <span data-ttu-id="f7849-128">Kaynak kapasite yuvarlamaları için eşitleme işlemi için bitiş tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="f7849-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="f7849-129">[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="f7849-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
