---
title: Çift yazmanın Finance and Operations uygulamalarında ve Dataverse'ta yapılandırıldığını denetleme
description: Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f389bcf133cc7e6a086167d5e26c1b8795d0fa30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685551"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="68997-103">Çift yazmanın Finance and Operations uygulamalarında ve Dataverse'ta yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="68997-103">Verify that dual-write is configured in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="68997-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="68997-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="68997-105">Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="68997-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="68997-106">Çift yazmanın Finance and Operations uygulamalarında yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="68997-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="68997-107">Güncelleştirme için satırları kaydetmeye çalıştığınızda gördüğünüz hataların çift yazma işleminden kaynaklanıp kaynaklanmadığını belirlemek için, önce çift yazma işleminin yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="68997-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="68997-108">Finance and Operations uygulamada yönetici ayrıcalıklarınız varsa **çalışma alanları \>veri yönetimi**'ne gidin ve **çift-yazılır** döşemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="68997-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="68997-109">Bağlı ortamların ayrıntıları ve çalışmakta olan tablo eşlemeleri listesi gösteriliyorsa çift yazma hizmeti yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="68997-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Yönetici ayrıcalıklarınız olduğunda Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_1.png)

+ <span data-ttu-id="68997-111">Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="68997-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="68997-112">Aşağıdaki çizimde yer alan örnekte, çift yazma yapılandırılmış olmasına rağmen müşteri grubu ve ödeme koşulları başvuru verileri Dataverse'te bulunmadığından Finance and Operations uygulamasında müşteri satırı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="68997-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Yönetici ayrıcalıklarınız olmadığında Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_2.png)

<span data-ttu-id="68997-114">Finance and Operations Uygulamalarda veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="68997-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="68997-115">Çift yazmanın Dataverse'ta yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="68997-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="68997-116">Veri oluşturduğunuzda, Dataverse içindeki sayfalarda **Şirket** alanını görüyorsanız, Çift-yazılır olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="68997-116">When you create data, if you see the **Company** field on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse bağlantı doğrulanıyor](media/verify_cds.png)

<span data-ttu-id="68997-118">Dataverse'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="68997-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="68997-119">Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Dataverse'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Dataverse'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="68997-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>
