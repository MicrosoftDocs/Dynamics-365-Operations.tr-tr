---
title: Satış eğilimlerini ve modellerini analiz etme
description: Dynamics 365 Retail'te satış eğilimleri ve modellerini gerçek zamanlı inceleyebilirsiniz.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, SysReportViewerForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c54e707d312d7ac3bbcad71a914e528859038a13
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025829"
---
# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="c0caa-103">Satış eğilimlerini ve modellerini analiz etme</span><span class="sxs-lookup"><span data-stu-id="c0caa-103">Analyze sales trends and patterns</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0caa-104">Dynamics 365 Retail'te satış eğilimleri ve modellerini gerçek zamanlı inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0caa-104">You can study sales trends and patterns in real time in Dynamics 365 Retail.</span></span>

<span data-ttu-id="c0caa-105">Retail'in bir parçası olarak, kullanıcılar kuruluş hiyerarşisinin farklı düzeylerindeki satış eğilimleri ve modellerini, kullanıma hazır **Yıla göre kanal satışları** raporunu kullanarak, yıllara göre gerçek zamanlı inceleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c0caa-105">As part of Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="c0caa-106">Bu raporu aşağıdaki konumların herhangi birinden açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c0caa-106">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="c0caa-107">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **Kanal yıla göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="c0caa-108">**Perakende mağaza mali bilgileri** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza mali bilgileri** &gt; **Raporlar** &gt; **Kanal yıla göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
- <span data-ttu-id="c0caa-109">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **Kanal yıla göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="c0caa-110">Kullanıcılar kuruluş hiyerarşisinin farklı düzeylerindeki satış eğilimleri ve modellerini, yeni **Yıla göre kanal satışları** raporunu kullanarak, seçilen dönem için saate göre inceleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="c0caa-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="c0caa-111">Bu raporu aşağıdaki konumların herhangi birinden açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c0caa-111">You can open this report from any of the following locations:</span></span>

- <span data-ttu-id="c0caa-112">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **Kanal saate göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="c0caa-113">**Perakende mağaza mali bilgileri** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza mali bilgileri** &gt; **Raporlar** &gt; **Kanal saate göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
- <span data-ttu-id="c0caa-114">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **Kanal saate göre satışlar raporu**</span><span class="sxs-lookup"><span data-stu-id="c0caa-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>
