---
title: Müşteri ve ürün karlılığını değerlendir
description: Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Retail verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.
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
ms.openlocfilehash: 5a9bebf948bd4602556f70a5a79690621a03261e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023602"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="406fc-103">Müşteri ve ürün karlılığını değerlendirme</span><span class="sxs-lookup"><span data-stu-id="406fc-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="406fc-104">Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Retail verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="406fc-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="406fc-105">Retail'in bir parçası olarak, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi müşterilere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="406fc-105">As part of Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="406fc-106">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="406fc-106">Sales amount</span></span>
- <span data-ttu-id="406fc-107">Miktar</span><span class="sxs-lookup"><span data-stu-id="406fc-107">Quantity</span></span>
- <span data-ttu-id="406fc-108">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="406fc-108">Gross profit margin</span></span>
- <span data-ttu-id="406fc-109">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="406fc-109">Margin percentage</span></span>

<span data-ttu-id="406fc-110">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi müşteriler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="406fc-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="406fc-111">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi müşteriler raporu**</span><span class="sxs-lookup"><span data-stu-id="406fc-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="406fc-112">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **En iyi müşteriler raporu**</span><span class="sxs-lookup"><span data-stu-id="406fc-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="406fc-113">Benzer şekilde, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi ürünlere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="406fc-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="406fc-114">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="406fc-114">Sales amount</span></span>
- <span data-ttu-id="406fc-115">Miktar</span><span class="sxs-lookup"><span data-stu-id="406fc-115">Quantity</span></span>
- <span data-ttu-id="406fc-116">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="406fc-116">Gross profit margin</span></span>
- <span data-ttu-id="406fc-117">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="406fc-117">Margin percentage</span></span>

<span data-ttu-id="406fc-118">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi ürünler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="406fc-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="406fc-119">**Perakende mağaza yönetimi** çalışma alanı &gt; **Perakende** &gt; **Kanallar** &gt; **Perakende mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="406fc-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="406fc-120">**Kategori ve ürün yönetimi** çalışma alanı &gt; **Retail** &gt; **Ürünler ve kategoriler** &gt; **Perakende mağazası yönetimi** &gt; **Raporlar** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="406fc-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="406fc-121">**Sorgular ve raporlar** bölümü &gt; **Perakende** &gt; **Sorgular ve raporlar** &gt; **Satış raporları** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="406fc-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
