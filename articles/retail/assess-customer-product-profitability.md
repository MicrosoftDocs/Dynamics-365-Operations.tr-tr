---
title: Müşteri ve ürün karlılığını değerlendir
description: Bu makale, bellek içi ve gerçek zamanlı analizleri Microsoft Dynamics 365 for Retail verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "326021"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="96b15-103">Müşteri ve ürün karlılığını değerlendirme</span><span class="sxs-lookup"><span data-stu-id="96b15-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96b15-104">Bu makale, bellek içi ve gerçek zamanlı analizleri Microsoft Dynamics 365 for Retail verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="96b15-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="96b15-105">Dynamics 365 for Retail'ın bir parçası olarak, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi müşterilere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="96b15-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="96b15-106">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="96b15-106">Sales amount</span></span>
- <span data-ttu-id="96b15-107">Miktar</span><span class="sxs-lookup"><span data-stu-id="96b15-107">Quantity</span></span>
- <span data-ttu-id="96b15-108">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="96b15-108">Gross profit margin</span></span>
- <span data-ttu-id="96b15-109">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="96b15-109">Margin percentage</span></span>

<span data-ttu-id="96b15-110">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi müşteriler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="96b15-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="96b15-111">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi müşteriler raporu**</span><span class="sxs-lookup"><span data-stu-id="96b15-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="96b15-112">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **En iyi müşteriler raporu**</span><span class="sxs-lookup"><span data-stu-id="96b15-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="96b15-113">Benzer şekilde, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi ürünlere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="96b15-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="96b15-114">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="96b15-114">Sales amount</span></span>
- <span data-ttu-id="96b15-115">Miktar</span><span class="sxs-lookup"><span data-stu-id="96b15-115">Quantity</span></span>
- <span data-ttu-id="96b15-116">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="96b15-116">Gross profit margin</span></span>
- <span data-ttu-id="96b15-117">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="96b15-117">Margin percentage</span></span>

<span data-ttu-id="96b15-118">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi ürünler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="96b15-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="96b15-119">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="96b15-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="96b15-120">**Kategori ve ürün yönetimi** çalışma alanı &gt; **Retail** &gt; **Ürünler ve kategoriler** &gt; **Perakende mağazası yönetimi** &gt; **Raporlar** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="96b15-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="96b15-121">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="96b15-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
