---
title: Müşteri ve ürün karlılığını değerlendir
description: Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Commerce verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024279"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="a7404-103">Müşteri ve ürün karlılığını değerlendirme</span><span class="sxs-lookup"><span data-stu-id="a7404-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7404-104">Bu makale, bellek içi ve gerçek zamanlı analizleri Dynamics 365 Commerce verilerinizden müşteriler ve ürün karlılığı bilgilerine erişmek, keşfetmek ve bunlar hakkında bilgi edinmek için nasıl kullanabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="a7404-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="a7404-105">Commerce'in bir parçası olarak, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi müşterilere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="a7404-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="a7404-106">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="a7404-106">Sales amount</span></span>
- <span data-ttu-id="a7404-107">Miktar</span><span class="sxs-lookup"><span data-stu-id="a7404-107">Quantity</span></span>
- <span data-ttu-id="a7404-108">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="a7404-108">Gross profit margin</span></span>
- <span data-ttu-id="a7404-109">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="a7404-109">Margin percentage</span></span>

<span data-ttu-id="a7404-110">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi müşteriler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a7404-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="a7404-111">**Mağaza yönetimi** çalışma alanı &gt; **Retail ve Commerce** &gt; **Kanallar** &gt; **Mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi müşteriler raporu**</span><span class="sxs-lookup"><span data-stu-id="a7404-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="a7404-112">**Inquiries and reports** section &gt; **Retail ve Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report** (Sorgular ve raporlar bölümü Dynamics AX > Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > En iyi müşteriler raporu)</span><span class="sxs-lookup"><span data-stu-id="a7404-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="a7404-113">Benzer şekilde, kullanıcılar aşağıdaki kriterlerden birine göre kuruluş hiyerarşisinin farklı düzeylerinde en iyi ürünlere (10'dan 100'e) ilişkin kârlılığı inceleyebilir:</span><span class="sxs-lookup"><span data-stu-id="a7404-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="a7404-114">Satış tutarı</span><span class="sxs-lookup"><span data-stu-id="a7404-114">Sales amount</span></span>
- <span data-ttu-id="a7404-115">Miktar</span><span class="sxs-lookup"><span data-stu-id="a7404-115">Quantity</span></span>
- <span data-ttu-id="a7404-116">Brüt kar marjı</span><span class="sxs-lookup"><span data-stu-id="a7404-116">Gross profit margin</span></span>
- <span data-ttu-id="a7404-117">Marj yüzdesi</span><span class="sxs-lookup"><span data-stu-id="a7404-117">Margin percentage</span></span>

<span data-ttu-id="a7404-118">Bu değerlendirme için, aşağıdaki konumlardan birinden açabileceğiniz, hazır **En iyi ürünler** raporunu kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a7404-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="a7404-119">**Mağaza yönetimi** çalışma alanı &gt; **Retail ve Commerce** &gt; **Kanallar** &gt; **Mağaza yönetimi** &gt; **Raporlar** &gt; **En ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="a7404-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="a7404-120">**Kategori ve ürün yönetimi** çalışma alanı &gt; **Retail ve Commerce** &gt; **Ürünler ve kategoriler** &gt; **Mağaza yönetimi** &gt; **Raporlar** &gt; **En iyi ürünler raporu**</span><span class="sxs-lookup"><span data-stu-id="a7404-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="a7404-121">**Inquiries and reports** section &gt; **Retail ve Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report** (Sorgular ve raporlar bölümü Dynamics AX > Perakende ve ticaret > Sorgular ve raporlar > Satış raporları > En iyi müşteriler raporu)</span><span class="sxs-lookup"><span data-stu-id="a7404-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
