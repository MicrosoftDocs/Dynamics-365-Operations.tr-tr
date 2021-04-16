---
title: Vergi hesaplama hizmeti (Önizleme)
description: Bu konu, vergi hesaplama servisinin tüm kapsamını ve özelliklerini açıklar.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818236"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="a0312-103">Vergi hesaplama hizmeti (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="a0312-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a0312-104">Vergi hesaplama Servisi, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir.</span><span class="sxs-lookup"><span data-stu-id="a0312-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="a0312-105">Tax Engine tam olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0312-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="a0312-106">Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="a0312-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="a0312-107">Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.</span><span class="sxs-lookup"><span data-stu-id="a0312-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="a0312-108">Vergi hesaplama servisi Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile birleşir.</span><span class="sxs-lookup"><span data-stu-id="a0312-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a0312-109">Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.</span><span class="sxs-lookup"><span data-stu-id="a0312-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="a0312-110">Vergi hesaplama Servisi, artan ölçeklenebilirlik sağlayan Microsoft tabanlı bir vergi altyapısıdır.</span><span class="sxs-lookup"><span data-stu-id="a0312-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="a0312-111">Aşağıdaki görevleri yerine getirmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="a0312-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="a0312-112">Vergi hesaplama hizmetini Regulatory Configuration Service (RCS) aracılığıyla yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="a0312-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="a0312-113">RCS, elektronik raporlama (ER) tasarımcısının gelişmiş bir sürümüdür ve bağımsız bir hizmet olarak edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0312-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="a0312-114">Vergi kodlarının ve oranlarının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="a0312-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="a0312-115">Vergi kayıt numarasının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="a0312-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="a0312-116">Formül ve koşulları tanımlamak için vergi hesaplama tasarımcısını yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="a0312-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="a0312-117">Vergi belirleme ve hesaplama çözümünü tüzel kişilerle paylaşma.</span><span class="sxs-lookup"><span data-stu-id="a0312-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="a0312-118">Vergi hesaplama hizmetini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden vergi hesaplama servisi eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="a0312-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a0312-119">Sonra, RCS'deki kurulumu tamamlayın ve Finance ve Supply Chain Management vergi hesaplama hizmetini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a0312-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="a0312-120">Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="a0312-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="a0312-121">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="a0312-121">Availability</span></span>

<span data-ttu-id="a0312-122">Vergi hesaplama hizmeti yalnızca, korumalı alan ortamlarında ve seçili müşteriler için ortak bir önizleme programı aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a0312-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="a0312-123">Sonuç olarak, tüm müşteriler ve üretim ortamlarında genellikle kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0312-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="a0312-124">Yeni özellikler vergi hesaplama hizmetinde sunulmaya devam edecek.</span><span class="sxs-lookup"><span data-stu-id="a0312-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="a0312-125">Bu nedenle, desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel belgeleri kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="a0312-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="a0312-126">Vergi hesaplama hizmeti aşağıdaki Azure bölgelerinde dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="a0312-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="a0312-127">Ayrıca, müşteri gereksinimlerine göre daha fazla Azure bölgesinde kullanılacak şekilde dağıtılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0312-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="a0312-128">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="a0312-128">United States</span></span>
- <span data-ttu-id="a0312-129">Avrupa</span><span class="sxs-lookup"><span data-stu-id="a0312-129">Europe</span></span>
- <span data-ttu-id="a0312-130">Fransa</span><span class="sxs-lookup"><span data-stu-id="a0312-130">France</span></span>
- <span data-ttu-id="a0312-131">Birleşik Krallık</span><span class="sxs-lookup"><span data-stu-id="a0312-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="a0312-132">Vergi hesaplama Servisi, Dynamics 365 şirket içi dağıtımlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="a0312-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="a0312-133">Ayrıca Dynamics AX 2012 gibi önceki sürümleri de desteklemez.</span><span class="sxs-lookup"><span data-stu-id="a0312-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="a0312-134">Özellikle ilgili önemli noktalar</span><span class="sxs-lookup"><span data-stu-id="a0312-134">Feature highlights</span></span>

- <span data-ttu-id="a0312-135">Vergiyi otomatik olarak belirlemek ve hesaplamak için yapılandırılabilir vergi matrisi</span><span class="sxs-lookup"><span data-stu-id="a0312-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="a0312-136">Çoklu katma değer vergisi (KDV) kayıt numaraları desteği</span><span class="sxs-lookup"><span data-stu-id="a0312-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="a0312-137">Vergi belirleme ve hesaplama için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="a0312-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="a0312-138">Çoklu KDV kayıt numaralarının belirlenmesi için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="a0312-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="a0312-139">Desteklenen işlemler</span><span class="sxs-lookup"><span data-stu-id="a0312-139">Supported transactions</span></span>

<span data-ttu-id="a0312-140">Vergi hesaplama servisi tüzel kişilik ve işlem tarafından etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0312-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="a0312-141">Aşağıdaki işlemler desteklenir:</span><span class="sxs-lookup"><span data-stu-id="a0312-141">The following transactions are supported:</span></span>

- <span data-ttu-id="a0312-142">Satış işlemi</span><span class="sxs-lookup"><span data-stu-id="a0312-142">Sales process</span></span>

    - <span data-ttu-id="a0312-143">Satış teklifi</span><span class="sxs-lookup"><span data-stu-id="a0312-143">Sales quotation</span></span>
    - <span data-ttu-id="a0312-144">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="a0312-144">Sales order</span></span>
    - <span data-ttu-id="a0312-145">Onay</span><span class="sxs-lookup"><span data-stu-id="a0312-145">Confirmation</span></span>
    - <span data-ttu-id="a0312-146">Malzeme çekme listesi</span><span class="sxs-lookup"><span data-stu-id="a0312-146">Picking list</span></span>
    - <span data-ttu-id="a0312-147">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="a0312-147">Packing slip</span></span>
    - <span data-ttu-id="a0312-148">Satış faturası</span><span class="sxs-lookup"><span data-stu-id="a0312-148">Sales invoice</span></span>
    - <span data-ttu-id="a0312-149">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="a0312-149">Credit note</span></span>
    - <span data-ttu-id="a0312-150">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="a0312-150">Return order</span></span>
    - <span data-ttu-id="a0312-151">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="a0312-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="a0312-152">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="a0312-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="a0312-153">Satın alma işlemi</span><span class="sxs-lookup"><span data-stu-id="a0312-153">Purchase process</span></span>

    - <span data-ttu-id="a0312-154">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="a0312-154">Purchase order</span></span>
    - <span data-ttu-id="a0312-155">Onay</span><span class="sxs-lookup"><span data-stu-id="a0312-155">Confirmation</span></span>
    - <span data-ttu-id="a0312-156">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="a0312-156">Receipts list</span></span>
    - <span data-ttu-id="a0312-157">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="a0312-157">Product receipt</span></span>
    - <span data-ttu-id="a0312-158">Satınalma faturası</span><span class="sxs-lookup"><span data-stu-id="a0312-158">Purchase invoice</span></span>
    - <span data-ttu-id="a0312-159">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="a0312-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="a0312-160">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="a0312-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="a0312-161">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="a0312-161">Credit note</span></span>
    - <span data-ttu-id="a0312-162">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="a0312-162">Return order</span></span>
    - <span data-ttu-id="a0312-163">Satınalma talebi</span><span class="sxs-lookup"><span data-stu-id="a0312-163">Purchase requisition</span></span>
    - <span data-ttu-id="a0312-164">Satın alma talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="a0312-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="a0312-165">Teklif talebi</span><span class="sxs-lookup"><span data-stu-id="a0312-165">Request for quotation</span></span>
    - <span data-ttu-id="a0312-166">Teklif talebi başlık sair masrafı</span><span class="sxs-lookup"><span data-stu-id="a0312-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="a0312-167">Teklif talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="a0312-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="a0312-168">Stok işlemi</span><span class="sxs-lookup"><span data-stu-id="a0312-168">Inventory process</span></span>

    - <span data-ttu-id="a0312-169">Transfer emri - sevk</span><span class="sxs-lookup"><span data-stu-id="a0312-169">Transfer order – ship</span></span>
    - <span data-ttu-id="a0312-170">Transfer emri - al</span><span class="sxs-lookup"><span data-stu-id="a0312-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="a0312-171">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a0312-171">Related resources</span></span>

[<span data-ttu-id="a0312-172">Vergi hizmetini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="a0312-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="a0312-173">Çoklu KDV kayıt numarası</span><span class="sxs-lookup"><span data-stu-id="a0312-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="a0312-174">Transfer emri için vergi özelliği desteği</span><span class="sxs-lookup"><span data-stu-id="a0312-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="a0312-175">Vergi hizmetinde uzantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0312-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
