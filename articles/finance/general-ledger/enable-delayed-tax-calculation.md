---
title: Günlükte ertelenen vergi hesaplamasını etkinleştirme
description: Bu konu, günlük satırlarının hacmi çok büyük olduğunda vergi hesaplama performansını artırmak için **Günlükte ertlenen vergi hesaplamasını etkinleştir** özelliğinin nasıl kullanılacağını açıklamaktadır.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180302"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="80d1d-103">Günlükte ertelenen vergi hesaplamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="80d1d-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="80d1d-104">Bu konu, günlük satırlarının hacmi çok büyük olduğunda vergi hesaplama performansını artırmak için **Günlükte ertlenen vergi hesaplamasını etkinleştir** özelliğinin nasıl kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="80d1d-105">Günlükteki geçerli satış vergisi hesaplama, kullanıcı vergiyle ilgili alanları güncelleştirdiğinde (satış vergisi grubu/madde satış vergisi grubu gibi) gerçek zamanlı olarak tetiklenen bir davranıştır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="80d1d-106">Günlük satırı düzeyindeki her güncelleştirme, tüm günlük satırlarındaki vergi tutarını yeniden hesaplar.</span><span class="sxs-lookup"><span data-stu-id="80d1d-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="80d1d-107">Kullanıcının gerçek zamanlı hesaplanan vergi tutarını görebilmesine yardımcı olur, ancak günlük satırları hacmi çok büyük olduğunda performans sorununa neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="80d1d-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="80d1d-108">Bu özellik, performans sorununu çözmek için vergi hesaplamasını erteleme seçeneği sunar.</span><span class="sxs-lookup"><span data-stu-id="80d1d-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="80d1d-109">Bu özellik açık ise, vergi tutarı yalnızca Kullanıcı "Satış Vergisi" komutunu tıklattığında veya günlüğü deftere naklederken hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="80d1d-110">Kullanıcı, parametreyi üç düzeyde açıp kapatabilir:</span><span class="sxs-lookup"><span data-stu-id="80d1d-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="80d1d-111">Tüzel kişiliğe göre</span><span class="sxs-lookup"><span data-stu-id="80d1d-111">By legal entity</span></span>
- <span data-ttu-id="80d1d-112">Günlük adına göre</span><span class="sxs-lookup"><span data-stu-id="80d1d-112">By journal name</span></span>
- <span data-ttu-id="80d1d-113">Günlük başlığına göre</span><span class="sxs-lookup"><span data-stu-id="80d1d-113">By journal header</span></span>

<span data-ttu-id="80d1d-114">Sistem, günlük başlığındaki parametre değerini son değer olarak alacaktır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="80d1d-115">Günlük başlığındaki parametre değeri varsayılan olarak günlük adından alınır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="80d1d-116">Günlük adı oluşturulduğunda, günlük adının parametre değeri varsayılan olarak genel muhasebe parametresi içinden alınır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="80d1d-117">Bu parametre açıksa, günlükteki "Gerçek satış vergisi tutarı" ve "Hesaplanan satış vergisi tutarı" alanları gizlenir.</span><span class="sxs-lookup"><span data-stu-id="80d1d-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="80d1d-118">Amaç, kullanıcının vergi hesaplamasını tetiklemeye başlamadan önce bu iki alanın değeri her zaman 0 olarak gösterileceği için kullanıcının kafasını karıştırmamaktır.</span><span class="sxs-lookup"><span data-stu-id="80d1d-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="80d1d-119">Tüzel kişiliğe göre ertelenen vergi hesaplamasını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="80d1d-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="80d1d-120">**Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="80d1d-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="80d1d-121">**Satış vergisi** sekmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="80d1d-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="80d1d-122">**Genel** hızlı sekmesi altında **Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın</span><span class="sxs-lookup"><span data-stu-id="80d1d-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="80d1d-123">Günlük adına göre ertelenen vergi hesaplamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="80d1d-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="80d1d-124">**Genel muhasebe > Günlük ayarı > Günlük adları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="80d1d-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="80d1d-125">**Genel** hızlı sekmesi altında **Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın</span><span class="sxs-lookup"><span data-stu-id="80d1d-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="80d1d-126">Günlüğe göre ertelenen vergi hesaplamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="80d1d-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="80d1d-127">**Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin</span><span class="sxs-lookup"><span data-stu-id="80d1d-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="80d1d-128">**Yeni**'ye tıklayın</span><span class="sxs-lookup"><span data-stu-id="80d1d-128">Click **New**</span></span>
3. <span data-ttu-id="80d1d-129">Bir günlük adı seçin</span><span class="sxs-lookup"><span data-stu-id="80d1d-129">Select a journal name</span></span>
4. <span data-ttu-id="80d1d-130">**Kurulum**’a tıklayın</span><span class="sxs-lookup"><span data-stu-id="80d1d-130">Click **Setup**</span></span>
5. <span data-ttu-id="80d1d-131">**Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın</span><span class="sxs-lookup"><span data-stu-id="80d1d-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
