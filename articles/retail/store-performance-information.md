---
title: Mağaza performansını analiz etme
description: Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Retail verilerinizi temel alan mağaza performansına erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b2ea6ad2e3d9589face06cd5f950973209c17d41
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017794"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="5ac9d-103">Mağaza performansını analiz etme</span><span class="sxs-lookup"><span data-stu-id="5ac9d-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ac9d-104">Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Retail verilerinizi temel alan mağaza performansına erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="5ac9d-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="5ac9d-105">Retail'in bir parçası olarak, kullanıcılar mağaza performansını aşağıdaki konumlardan birinden yeni **Kanal özeti** raporunu açarak seçilen bir dönemdeki farklı kuruluş hiyerarşisi düzeylerinde gerçek zamanlı olarak inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="5ac9d-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="5ac9d-106">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **Kanal özet raporu**</span><span class="sxs-lookup"><span data-stu-id="5ac9d-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5ac9d-107">**Perakende mağaza mali bilgileri** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza mali bilgileri** &gt; **Raporlar** &gt; **Kanal özet raporu**</span><span class="sxs-lookup"><span data-stu-id="5ac9d-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="5ac9d-108">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **Kanal özet raporu**</span><span class="sxs-lookup"><span data-stu-id="5ac9d-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="5ac9d-109">Bu rapor aşağıdaki özetlerin anlık görüntüsünü mağaza performansının bir parçası olarak sunar:</span><span class="sxs-lookup"><span data-stu-id="5ac9d-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="5ac9d-110">Brüt satış özeti</span><span class="sxs-lookup"><span data-stu-id="5ac9d-110">Gross sales summary</span></span>
- <span data-ttu-id="5ac9d-111">Ödeme türü özeti</span><span class="sxs-lookup"><span data-stu-id="5ac9d-111">Tender type summary</span></span>
- <span data-ttu-id="5ac9d-112">Vergi özeti</span><span class="sxs-lookup"><span data-stu-id="5ac9d-112">Tax summary</span></span>
- <span data-ttu-id="5ac9d-113">Fiyat geçersiz kılma özeti</span><span class="sxs-lookup"><span data-stu-id="5ac9d-113">Price overrides summary</span></span>
- <span data-ttu-id="5ac9d-114">İskonto özeti</span><span class="sxs-lookup"><span data-stu-id="5ac9d-114">Discounts summary</span></span>
