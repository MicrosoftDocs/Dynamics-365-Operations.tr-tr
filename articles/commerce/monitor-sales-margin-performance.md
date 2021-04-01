---
title: Satış ve kar marjı performansını izle
description: Dynamics 365 Commerce kullanarak satış ve kar marjı performansını gerçek zamanlı izleyebilirsiniz.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4d8d6a99e0ed3f331051d504e3a1ce2bd403cc17
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251319"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="3f5bd-103">Satış ve kar performansını izleme</span><span class="sxs-lookup"><span data-stu-id="3f5bd-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f5bd-104">Dynamics 365 Commerce kullanarak satış ve kar marjı performansını gerçek zamanlı izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f5bd-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3f5bd-105">Commerce'ın bir parçası olarak kullanıcılar, aşağıdaki boyutlar için kuruluş hiyerarşisinin farklı düzeylerindeki satış ve kar marjı performansını gerçek zamanlı olarak izleyebilirler:</span><span class="sxs-lookup"><span data-stu-id="3f5bd-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="3f5bd-106">Ürünler</span><span class="sxs-lookup"><span data-stu-id="3f5bd-106">Products</span></span>
- <span data-ttu-id="3f5bd-107">Kategoriler</span><span class="sxs-lookup"><span data-stu-id="3f5bd-107">Categories</span></span>
- <span data-ttu-id="3f5bd-108">İskontolar</span><span class="sxs-lookup"><span data-stu-id="3f5bd-108">Discounts</span></span>
- <span data-ttu-id="3f5bd-109">Dönem olarak yıl</span><span class="sxs-lookup"><span data-stu-id="3f5bd-109">Years as time period</span></span>
- <span data-ttu-id="3f5bd-110">Kayıtlar/terminaller</span><span class="sxs-lookup"><span data-stu-id="3f5bd-110">Registers/terminals</span></span>
- <span data-ttu-id="3f5bd-111">Personel/çalışanlar</span><span class="sxs-lookup"><span data-stu-id="3f5bd-111">Staff/employees</span></span>
- <span data-ttu-id="3f5bd-112">Müşteriler</span><span class="sxs-lookup"><span data-stu-id="3f5bd-112">Customers</span></span>
- <span data-ttu-id="3f5bd-113">İşletme birimleri</span><span class="sxs-lookup"><span data-stu-id="3f5bd-113">Operating units</span></span>

<span data-ttu-id="3f5bd-114">Ayrıca, hiyerarşik ızgara yapısından yararlanan iki benzersiz rapor kullanıcıların, en üst kategori düğümünden varsayılan ürününün kategori hiyerarşisindeki bireysel kategori alt düğümlerine kadar detaylara inerek, satış ve kar marjı performansını izlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3f5bd-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="3f5bd-115">Kullanıcılar, ayrıca raporlama amacıyla varsayılan kuruluş hiyerarşisi olarak tanımlanan kuruluş hiyerarşisindeki en üst faaliyet biriminden bireysel bir kanala kadar ayrıntılara inebilirler.</span><span class="sxs-lookup"><span data-stu-id="3f5bd-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="3f5bd-116">Raporları aşağıdaki konumların herhangi birinden açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3f5bd-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="3f5bd-117">**Mağaza yönetimi** çalışma alanı &gt; **Perakende ve Ticaret** &gt; **Kanallar** &gt; **Mağaza yönetimi** &gt; **Raporlar**</span><span class="sxs-lookup"><span data-stu-id="3f5bd-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3f5bd-118">**Kategori ve ürün yönetimi** çalışma alanı &gt; **Retail ve Ticaret** &gt; **Ürün ve kategoriler** &gt; **Mağaza yönetimi** &gt; **Raporlar**</span><span class="sxs-lookup"><span data-stu-id="3f5bd-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3f5bd-119">**Fiyatlandırma ve iskonto yönetimi** çalışma alanı &gt; **Retail ve Ticaret** &gt; **Fiyatlandırma ve iskontolar** &gt; **Mağaza yönetimi** &gt; **Raporlar**</span><span class="sxs-lookup"><span data-stu-id="3f5bd-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="3f5bd-120">**Sorgular ve raporlar** bölümü &gt; **Retail ve Ticaret** &gt; **Sorgular ve raporlar** &gt; **Satış raporları**</span><span class="sxs-lookup"><span data-stu-id="3f5bd-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]