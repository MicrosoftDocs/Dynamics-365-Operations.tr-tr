---
title: Kiralama günlüğü adlarını ayarlama
description: Bu konu, kiralama günlüğü adlarının nasıl tanımlanacağını açıklamaktadır. Kiralama günlüğü adları, Varlık kiralamada girişlerin nakledildiği günlükleri belirtir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880898"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="8d2ec-104">Kiralama günlüğü adlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8d2ec-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d2ec-105">Kiralama günlüğü adları, Varlık kiralama hareketlerinin nakledildiği günlükleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="8d2ec-106">Yalnızca **Varlık kiralama** günlük türüne atanmış günlük adları, **Varlık kiralama parametreleri** sayfasında **İlk Kabul** ve **Aylık Günlük Adı** alanlarında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="8d2ec-107">Yalnızca **satıcı faturası kaydı** günlük türü **Satıcı günlüğü adı** alanına atanabilir.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="8d2ec-108">Kiralama günlüğü adlarını yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="8d2ec-109">**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="8d2ec-110">**Genel** sekmesindeki **İlk kabul günlük adı** alanında bir günlük seçin.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="8d2ec-111">Tüm ilk kabul günlüğü girişleri bu günlük adına nakledilecek.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="8d2ec-112">**Fatura günlük adı** alanında, bir günlük seçin.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="8d2ec-113">Kiralama defteri için **Satıcıya öde** seçeneği **Evet** olarak ayarlanmışsa kiralama ve gider ödeme faturaları bu günlük adına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="8d2ec-114">**Kiralama günlüğü adı** alanında, bir günlük seçin.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="8d2ec-115">Tüm amortisman, faiz ve kısa süreli yeniden sınıflama girişleri bu günlük adına nakledilecek.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="8d2ec-116">Kiralama defteri için **Satıcıya öde** seçeneği **Hayır** olarak ayarlanmışsa kira ödemeleri ve gider ödeme girişleri de bu günlük adına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="8d2ec-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
