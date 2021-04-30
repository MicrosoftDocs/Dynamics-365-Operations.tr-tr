---
title: Vergi Hesaplama (Önizleme)
description: Bu konu, Vergi Hesaplama özelliğinin tüm kapsamını ve özelliklerini açıklar.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892361"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="8922f-103">Vergi Hesaplama (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="8922f-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8922f-104">Vergi Hesaplama, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir.</span><span class="sxs-lookup"><span data-stu-id="8922f-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="8922f-105">Tax Engine tam olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="8922f-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="8922f-106">Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="8922f-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="8922f-107">Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.</span><span class="sxs-lookup"><span data-stu-id="8922f-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="8922f-108">Vergi Hesaplama hizmeti Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile tümleşir.</span><span class="sxs-lookup"><span data-stu-id="8922f-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8922f-109">Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.</span><span class="sxs-lookup"><span data-stu-id="8922f-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="8922f-110">Vergi Hesaplama, artan ölçeklenebilirlik sağlayan mikro hizmet tabanlı bir vergi altyapısıdır.</span><span class="sxs-lookup"><span data-stu-id="8922f-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="8922f-111">Aşağıdaki görevleri yerine getirmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="8922f-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="8922f-112">Vergi Hesaplama'yı Regulatory Configuration Service (RCS) aracılığıyla yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8922f-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="8922f-113">RCS, elektronik raporlama (ER) tasarımcısının gelişmiş bir sürümüdür ve bağımsız bir hizmet olarak edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="8922f-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="8922f-114">Vergi kodlarının ve oranlarının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="8922f-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="8922f-115">Vergi kayıt numarasının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="8922f-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="8922f-116">Formül ve koşulları tanımlamak için vergi hesaplama tasarımcısını yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="8922f-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="8922f-117">Vergi belirleme ve hesaplama çözümünü tüzel kişilerle paylaşma.</span><span class="sxs-lookup"><span data-stu-id="8922f-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="8922f-118">Vergi hesaplama hizmetini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden vergi hesaplama servisi eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="8922f-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8922f-119">Sonra, RCS'deki kurulumu tamamlayın ve Finance ve Supply Chain Management vergi hesaplama hizmetini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="8922f-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="8922f-120">Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="8922f-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="8922f-121">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="8922f-121">Availability</span></span>

<span data-ttu-id="8922f-122">Vergi Hesaplama, yalnızca korumalı alan ortamlarında ve seçili müşteriler için bir genel önizleme programı aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8922f-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="8922f-123">Sonuç olarak, tüm müşteriler ve üretim ortamlarında genellikle kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8922f-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="8922f-124">Yeni özellikler sunulmaya devam edilmektedir. Bu nedenle, desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel belgeleri kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="8922f-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="8922f-125">Vergi Hesaplama aşağıdaki Azure bölgelerinde dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="8922f-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="8922f-126">Ayrıca, müşteri gereksinimlerine göre daha fazla Azure bölgesinde kullanılacak şekilde dağıtılacaktır.</span><span class="sxs-lookup"><span data-stu-id="8922f-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="8922f-127">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="8922f-127">United States</span></span>
- <span data-ttu-id="8922f-128">Avrupa</span><span class="sxs-lookup"><span data-stu-id="8922f-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="8922f-129">Vergi Hesaplama, Dynamics 365 şirket içi dağıtımlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="8922f-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="8922f-130">Ayrıca Dynamics AX 2012 gibi önceki sürümleri de desteklemez.</span><span class="sxs-lookup"><span data-stu-id="8922f-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="8922f-131">Özellikle ilgili önemli noktalar</span><span class="sxs-lookup"><span data-stu-id="8922f-131">Feature highlights</span></span>

- <span data-ttu-id="8922f-132">Vergiyi otomatik olarak belirlemek ve hesaplamak için yapılandırılabilir vergi matrisi</span><span class="sxs-lookup"><span data-stu-id="8922f-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="8922f-133">Çoklu vergisi kayıt numarası desteği</span><span class="sxs-lookup"><span data-stu-id="8922f-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="8922f-134">Vergi belirleme ve hesaplama için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="8922f-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="8922f-135">Çoklu vergi kayıt numaralarının belirlenmesi için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="8922f-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="8922f-136">Desteklenen işlemler</span><span class="sxs-lookup"><span data-stu-id="8922f-136">Supported transactions</span></span>

<span data-ttu-id="8922f-137">Vergi Hesaplama tüzel kişilik ve işlem tarafından etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8922f-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="8922f-138">Aşağıdaki işlemler desteklenir:</span><span class="sxs-lookup"><span data-stu-id="8922f-138">The following transactions are supported:</span></span>

- <span data-ttu-id="8922f-139">Satış işlemi</span><span class="sxs-lookup"><span data-stu-id="8922f-139">Sales process</span></span>

    - <span data-ttu-id="8922f-140">Satış teklifi</span><span class="sxs-lookup"><span data-stu-id="8922f-140">Sales quotation</span></span>
    - <span data-ttu-id="8922f-141">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="8922f-141">Sales order</span></span>
    - <span data-ttu-id="8922f-142">Onay</span><span class="sxs-lookup"><span data-stu-id="8922f-142">Confirmation</span></span>
    - <span data-ttu-id="8922f-143">Malzeme çekme listesi</span><span class="sxs-lookup"><span data-stu-id="8922f-143">Picking list</span></span>
    - <span data-ttu-id="8922f-144">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="8922f-144">Packing slip</span></span>
    - <span data-ttu-id="8922f-145">Satış faturası</span><span class="sxs-lookup"><span data-stu-id="8922f-145">Sales invoice</span></span>
    - <span data-ttu-id="8922f-146">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="8922f-146">Credit note</span></span>
    - <span data-ttu-id="8922f-147">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="8922f-147">Return order</span></span>
    - <span data-ttu-id="8922f-148">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="8922f-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="8922f-149">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="8922f-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="8922f-150">Satın alma işlemi</span><span class="sxs-lookup"><span data-stu-id="8922f-150">Purchase process</span></span>

    - <span data-ttu-id="8922f-151">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="8922f-151">Purchase order</span></span>
    - <span data-ttu-id="8922f-152">Onay</span><span class="sxs-lookup"><span data-stu-id="8922f-152">Confirmation</span></span>
    - <span data-ttu-id="8922f-153">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="8922f-153">Receipts list</span></span>
    - <span data-ttu-id="8922f-154">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="8922f-154">Product receipt</span></span>
    - <span data-ttu-id="8922f-155">Satınalma faturası</span><span class="sxs-lookup"><span data-stu-id="8922f-155">Purchase invoice</span></span>
    - <span data-ttu-id="8922f-156">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="8922f-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="8922f-157">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="8922f-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="8922f-158">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="8922f-158">Credit note</span></span>
    - <span data-ttu-id="8922f-159">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="8922f-159">Return order</span></span>
    - <span data-ttu-id="8922f-160">Satınalma talebi</span><span class="sxs-lookup"><span data-stu-id="8922f-160">Purchase requisition</span></span>
    - <span data-ttu-id="8922f-161">Satın alma talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="8922f-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="8922f-162">Teklif talebi</span><span class="sxs-lookup"><span data-stu-id="8922f-162">Request for quotation</span></span>
    - <span data-ttu-id="8922f-163">Teklif talebi başlık sair masrafı</span><span class="sxs-lookup"><span data-stu-id="8922f-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="8922f-164">Teklif talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="8922f-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="8922f-165">Stok işlemi</span><span class="sxs-lookup"><span data-stu-id="8922f-165">Inventory process</span></span>

    - <span data-ttu-id="8922f-166">Transfer emri - sevk</span><span class="sxs-lookup"><span data-stu-id="8922f-166">Transfer order – ship</span></span>
    - <span data-ttu-id="8922f-167">Transfer emri - al</span><span class="sxs-lookup"><span data-stu-id="8922f-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="8922f-168">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8922f-168">Related resources</span></span>

[<span data-ttu-id="8922f-169">Vergi hizmetini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8922f-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="8922f-170">Çoklu KDV kayıt numarası</span><span class="sxs-lookup"><span data-stu-id="8922f-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="8922f-171">Transfer emri için vergi özelliği desteği</span><span class="sxs-lookup"><span data-stu-id="8922f-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="8922f-172">Vergi hizmetinde uzantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8922f-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)