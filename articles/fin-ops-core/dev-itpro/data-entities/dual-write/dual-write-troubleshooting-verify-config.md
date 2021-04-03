---
title: Finance and Operations uygulamalarında ve Dataverse'te çift yazma yapılandırmasını doğrulama
description: Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0a1da32713f3d4d19b4d343c5b67b416a6c4ffbb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566777"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="54636-103">Finance and Operations uygulamalarında ve Dataverse'te çift yazma yapılandırmasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="54636-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="54636-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="54636-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="54636-105">Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Dataverse'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="54636-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="54636-106">Çift yazmanın Finance and Operations uygulamalarında yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="54636-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="54636-107">Güncelleştirme için satırları kaydetmeye çalıştığınızda gördüğünüz hataların çift yazma işleminden kaynaklanıp kaynaklanmadığını belirlemek için, önce çift yazma işleminin yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="54636-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="54636-108">Finance and Operations uygulamada yönetici ayrıcalıklarınız varsa **çalışma alanları \>veri yönetimi**'ne gidin ve **çift-yazılır** döşemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="54636-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="54636-109">Bağlı ortamların ayrıntıları ve çalışmakta olan tablo eşlemeleri listesi gösteriliyorsa çift yazma hizmeti yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="54636-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Yönetici ayrıcalıklarınız olduğunda Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_1.png)

+ <span data-ttu-id="54636-111">Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="54636-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="54636-112">Aşağıdaki çizimde yer alan örnekte, çift yazma yapılandırılmış olmasına rağmen müşteri grubu ve ödeme koşulları başvuru verileri Dataverse'te bulunmadığından Finance and Operations uygulamasında müşteri satırı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="54636-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Yönetici ayrıcalıklarınız olmadığında Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_2.png)

<span data-ttu-id="54636-114">Finance and Operations Uygulamalarda veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="54636-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="54636-115">Çift yazmanın Dataverse'ta yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="54636-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="54636-116">Veri oluşturduğunuzda, Dataverse içindeki sayfalarda **Şirket** sütununu görüyorsanız çift yazma özelliği yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="54636-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse bağlantı doğrulanıyor](media/verify_cds.png)

<span data-ttu-id="54636-118">Dataverse'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="54636-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="54636-119">Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Dataverse'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Dataverse'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="54636-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]