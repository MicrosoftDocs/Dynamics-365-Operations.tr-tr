---
title: Çift yazmanın Finance and Operations uygulamalarında ve Common Data Service'ta yapılandırıldığını denetleme
description: Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Common Data Service'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.
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
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997242"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="7652d-103">Çift yazmanın Finance and Operations uygulamalarında ve Common Data Service'ta yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="7652d-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7652d-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="7652d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="7652d-105">Bu konu, Çift-yazılır'ın Finance and Operations uygulamalarda ve Common Data Service'de yapılandırılıp yapılandırılmadığını nasıl belirleyebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7652d-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="7652d-106">Çift yazmanın Finance and Operations uygulamalarında yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="7652d-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="7652d-107">Güncelleştirme için kayıtları kaydetmeye çalıştığınızda gördüğünüz hataların çift dosyadan gelip gelmediğini belirlemek için, önce çift Yazımın konfigüre edilmiş olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="7652d-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="7652d-108">Finance and Operations uygulamada yönetici ayrıcalıklarınız varsa **çalışma alanları \>veri yönetimi** 'ne gidin ve **çift-yazılır** döşemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="7652d-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="7652d-109">Bağlı ortamların ayrıntıları ve çalışmakta olan varlık haritaları listesi gösteriliyorsa, çift yazım yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="7652d-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Yönetici ayrıcalıklarınız olduğunda Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_1.png)

+ <span data-ttu-id="7652d-111">Yönetici ayrıcalıklarınız yoksa, *\<entity name\> varlığına veri yazılamıyor* hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7652d-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="7652d-112">Aşağıdaki çizimde yer alarak, Çift yazılı konfigüre edilmiş, ancak müşteri grubu ve ödeme koşulları referans verileri Common Data Service' nde bulunmadığından, Finance and Operations uygulamada müşteri kaydı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="7652d-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Yönetici ayrıcalıklarınız olmadığında Finance and Operations uygulama bağlantısı doğrulanıyor](media/verify_fin_ops_2.png)

<span data-ttu-id="7652d-114">Finance and Operations Uygulamalarda veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="7652d-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="7652d-115">Çift yazmanın Common Data Service'ta yapılandırıldığını denetleme</span><span class="sxs-lookup"><span data-stu-id="7652d-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="7652d-116">Veri oluşturduğunuzda, Common Data Service içindeki sayfalarda **Şirket** alanını görüyorsanız, Çift-yazılır olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="7652d-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Common Data Service bağlantı doğrulanıyor](media/verify_cds.png)

<span data-ttu-id="7652d-118">Common Data Service'te veri oluştururken sorunları nasıl giderileceğine ilişkin bilgi için, bkz [Canlı eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="7652d-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="7652d-119">Hata ayrıntılarının nasıl görüntüleneceği hakkında bilgi için Common Data Service'de veri oluştururken herhangi bir hatayla karşılaşırsanız, bkz. [Hata ayrıntılarını görüntülemek için Common Data Service'te eklenti izleme günlüklerini etkinleştirin ve görüntüleyin](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="7652d-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
