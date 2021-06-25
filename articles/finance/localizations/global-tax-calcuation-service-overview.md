---
title: Vergi Hesaplama (Önizleme)
description: Bu konu, Vergi Hesaplama özelliğinin tüm kapsamını ve özelliklerini açıklar.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184113"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="08eeb-103">Vergi Hesaplama (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="08eeb-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="08eeb-104">Vergi Hesaplama, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="08eeb-105">Tax Engine tam olarak konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="08eeb-106">Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="08eeb-107">Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.</span><span class="sxs-lookup"><span data-stu-id="08eeb-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="08eeb-108">Vergi Hesaplama hizmeti Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile tümleşir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="08eeb-109">Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08eeb-110">Vergi Hesaplama hizmetini etkinleştirdiğinizde, ilgili veriler üzerinde bazı işlemler servis verilerinizi barındıran veri merkezinden farklı bir veri merkezinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="08eeb-111">Vergi Hesaplama servisini etkinleştirmeden önce [Hükümler ve Koşullar](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)'ı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="08eeb-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="08eeb-112">Gizliliğiniz bizim için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-112">Your privacy is important to us.</span></span> <span data-ttu-id="08eeb-113">Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.</span><span class="sxs-lookup"><span data-stu-id="08eeb-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="08eeb-114">Vergi Hesaplama, artan ölçeklenebilirlik sağlayan mikro hizmet tabanlı bir vergi altyapısıdır.</span><span class="sxs-lookup"><span data-stu-id="08eeb-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="08eeb-115">Aşağıdaki görevleri yerine getirmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="08eeb-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="08eeb-116">Vergi Hesaplama'yı Regulatory Configuration Service (RCS) aracılığıyla yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="08eeb-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="08eeb-117">RCS, elektronik raporlama (ER) tasarımcısının gelişmiş bir sürümüdür ve bağımsız bir hizmet olarak edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="08eeb-118">Vergi kodlarının ve oranlarının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="08eeb-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="08eeb-119">Vergi kayıt numarasının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="08eeb-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="08eeb-120">Formül ve koşulları tanımlamak için vergi hesaplama tasarımcısını yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="08eeb-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="08eeb-121">Vergi belirleme ve hesaplama çözümünü tüzel kişilerle paylaşma.</span><span class="sxs-lookup"><span data-stu-id="08eeb-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="08eeb-122">Vergi hesaplama hizmetini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden vergi hesaplama servisi eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="08eeb-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="08eeb-123">Sonra, RCS'deki kurulumu tamamlayın ve Finance ve Supply Chain Management vergi hesaplama hizmetini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="08eeb-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="08eeb-124">Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="08eeb-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="08eeb-125">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="08eeb-125">Availability</span></span>

<span data-ttu-id="08eeb-126">Vergi Hesaplama, yalnızca korumalı alan ortamlarında ve seçili müşteriler için bir genel önizleme programı aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="08eeb-127">Sonuç olarak, tüm müşteriler ve üretim ortamlarında genellikle kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="08eeb-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="08eeb-128">Yeni özellikler sunulmaya devam edilmektedir. Bu nedenle, desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel belgeleri kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="08eeb-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="08eeb-129">Vergi Hesaplama aşağıdaki Azure bölgelerinde dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="08eeb-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="08eeb-130">Ayrıca, müşteri gereksinimlerine göre daha fazla Azure bölgesinde kullanılacak şekilde dağıtılacaktır.</span><span class="sxs-lookup"><span data-stu-id="08eeb-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="08eeb-131">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="08eeb-131">United States</span></span>
- <span data-ttu-id="08eeb-132">Avrupa</span><span class="sxs-lookup"><span data-stu-id="08eeb-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="08eeb-133">Vergi Hesaplama, Dynamics 365 şirket içi dağıtımlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="08eeb-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="08eeb-134">Ayrıca Dynamics AX 2012 gibi önceki sürümleri de desteklemez.</span><span class="sxs-lookup"><span data-stu-id="08eeb-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="08eeb-135">Özellikle ilgili önemli noktalar</span><span class="sxs-lookup"><span data-stu-id="08eeb-135">Feature highlights</span></span>

- <span data-ttu-id="08eeb-136">Vergiyi otomatik olarak belirlemek ve hesaplamak için yapılandırılabilir vergi matrisi</span><span class="sxs-lookup"><span data-stu-id="08eeb-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="08eeb-137">Çoklu vergisi kayıt numarası desteği</span><span class="sxs-lookup"><span data-stu-id="08eeb-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="08eeb-138">Vergi belirleme ve hesaplama için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="08eeb-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="08eeb-139">Çoklu vergi kayıt numaralarının belirlenmesi için transfer emri desteği</span><span class="sxs-lookup"><span data-stu-id="08eeb-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="08eeb-140">Desteklenen işlemler</span><span class="sxs-lookup"><span data-stu-id="08eeb-140">Supported transactions</span></span>

<span data-ttu-id="08eeb-141">Vergi Hesaplama tüzel kişilik ve işlem tarafından etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="08eeb-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="08eeb-142">Aşağıdaki işlemler desteklenir:</span><span class="sxs-lookup"><span data-stu-id="08eeb-142">The following transactions are supported:</span></span>

- <span data-ttu-id="08eeb-143">Satış işlemi</span><span class="sxs-lookup"><span data-stu-id="08eeb-143">Sales process</span></span>

    - <span data-ttu-id="08eeb-144">Satış teklifi</span><span class="sxs-lookup"><span data-stu-id="08eeb-144">Sales quotation</span></span>
    - <span data-ttu-id="08eeb-145">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="08eeb-145">Sales order</span></span>
    - <span data-ttu-id="08eeb-146">Onay</span><span class="sxs-lookup"><span data-stu-id="08eeb-146">Confirmation</span></span>
    - <span data-ttu-id="08eeb-147">Malzeme çekme listesi</span><span class="sxs-lookup"><span data-stu-id="08eeb-147">Picking list</span></span>
    - <span data-ttu-id="08eeb-148">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="08eeb-148">Packing slip</span></span>
    - <span data-ttu-id="08eeb-149">Satış faturası</span><span class="sxs-lookup"><span data-stu-id="08eeb-149">Sales invoice</span></span>
    - <span data-ttu-id="08eeb-150">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="08eeb-150">Credit note</span></span>
    - <span data-ttu-id="08eeb-151">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="08eeb-151">Return order</span></span>
    - <span data-ttu-id="08eeb-152">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="08eeb-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="08eeb-153">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="08eeb-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="08eeb-154">Satın alma işlemi</span><span class="sxs-lookup"><span data-stu-id="08eeb-154">Purchase process</span></span>

    - <span data-ttu-id="08eeb-155">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="08eeb-155">Purchase order</span></span>
    - <span data-ttu-id="08eeb-156">Onay</span><span class="sxs-lookup"><span data-stu-id="08eeb-156">Confirmation</span></span>
    - <span data-ttu-id="08eeb-157">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="08eeb-157">Receipts list</span></span>
    - <span data-ttu-id="08eeb-158">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="08eeb-158">Product receipt</span></span>
    - <span data-ttu-id="08eeb-159">Satınalma faturası</span><span class="sxs-lookup"><span data-stu-id="08eeb-159">Purchase invoice</span></span>
    - <span data-ttu-id="08eeb-160">Başlık sair masrafları</span><span class="sxs-lookup"><span data-stu-id="08eeb-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="08eeb-161">Satır sair masrafları</span><span class="sxs-lookup"><span data-stu-id="08eeb-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="08eeb-162">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="08eeb-162">Credit note</span></span>
    - <span data-ttu-id="08eeb-163">Sipariş iadesi</span><span class="sxs-lookup"><span data-stu-id="08eeb-163">Return order</span></span>
    - <span data-ttu-id="08eeb-164">Satınalma talebi</span><span class="sxs-lookup"><span data-stu-id="08eeb-164">Purchase requisition</span></span>
    - <span data-ttu-id="08eeb-165">Satın alma talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="08eeb-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="08eeb-166">Teklif talebi</span><span class="sxs-lookup"><span data-stu-id="08eeb-166">Request for quotation</span></span>
    - <span data-ttu-id="08eeb-167">Teklif talebi başlık sair masrafı</span><span class="sxs-lookup"><span data-stu-id="08eeb-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="08eeb-168">Teklif talebi satır sair masrafı</span><span class="sxs-lookup"><span data-stu-id="08eeb-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="08eeb-169">Stok işlemi</span><span class="sxs-lookup"><span data-stu-id="08eeb-169">Inventory process</span></span>

    - <span data-ttu-id="08eeb-170">Transfer emri - sevk</span><span class="sxs-lookup"><span data-stu-id="08eeb-170">Transfer order – ship</span></span>
    - <span data-ttu-id="08eeb-171">Transfer emri - al</span><span class="sxs-lookup"><span data-stu-id="08eeb-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="08eeb-172">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="08eeb-172">Related resources</span></span>

[<span data-ttu-id="08eeb-173">Vergi hizmetini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="08eeb-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="08eeb-174">Çoklu KDV kayıt numarası</span><span class="sxs-lookup"><span data-stu-id="08eeb-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="08eeb-175">Transfer emri için vergi özelliği desteği</span><span class="sxs-lookup"><span data-stu-id="08eeb-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="08eeb-176">Vergi hizmetinde uzantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="08eeb-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
