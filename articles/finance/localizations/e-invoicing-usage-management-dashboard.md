---
title: Kullanım yönetimi panosu
description: Bu konu, Elektronik Faturalama hizmetinin kullanımını izlemek ve uyumlu kalmak için Kullanım yönetimi panosunun nasıl kullanılacağını açıklar.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130518"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="5f27a-103">Kullanım yönetimi panosu</span><span class="sxs-lookup"><span data-stu-id="5f27a-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f27a-104">**Kullanım Yönetimi** panosu, Elektronik Faturalama servisinin kullanımını izlemenize yardımcı olur ve bu nedenle kuruluşunuzun aylık kullanım açısından uyumlu kalmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="5f27a-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="5f27a-105">Uyumluluk, gönderme biriminin hesaplanmasıyla ve elde edilen birim ile kullanılan birim arasındaki sapmaları belirlemek için alınan gönderilerle karşılaştırarak belirlenir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="5f27a-106">Pano, aşağıdaki göstergeleri içerir:</span><span class="sxs-lookup"><span data-stu-id="5f27a-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="5f27a-107">Lisans uyumluluğu amaçları için tüketimi izlemek amacıyla kullanabileceğiniz bir maliyet göstergesi:</span><span class="sxs-lookup"><span data-stu-id="5f27a-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="5f27a-108">Aylık kullanım (dışarı aktarma)</span><span class="sxs-lookup"><span data-stu-id="5f27a-108">Usage per month (export)</span></span>

- <span data-ttu-id="5f27a-109">Elektronik Faturalama hizmetinin kullanımını yönetim amaçlarını izlemek için kullanabileceğiniz üç operasyon göstergesi:</span><span class="sxs-lookup"><span data-stu-id="5f27a-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="5f27a-110">Özelliğe göre kullanım</span><span class="sxs-lookup"><span data-stu-id="5f27a-110">Usage by feature</span></span>
    - <span data-ttu-id="5f27a-111">Ortama göre kullanım</span><span class="sxs-lookup"><span data-stu-id="5f27a-111">Usage by environment</span></span>
    - <span data-ttu-id="5f27a-112">Aylık kullanım (içeri aktarma)</span><span class="sxs-lookup"><span data-stu-id="5f27a-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="5f27a-113">Ölçüm kapsamı</span><span class="sxs-lookup"><span data-stu-id="5f27a-113">Measurement scope</span></span>

- <span data-ttu-id="5f27a-114">Ölçü birimi:</span><span class="sxs-lookup"><span data-stu-id="5f27a-114">Unit of measure:</span></span> 

    <span data-ttu-id="5f27a-115">**Kullanım yönetimi** panosu, iş belgelerinin ve içe aktarılan elektronik faturaların gönderimini sayar.</span><span class="sxs-lookup"><span data-stu-id="5f27a-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="5f27a-116">Kuruluş:</span><span class="sxs-lookup"><span data-stu-id="5f27a-116">Organization:</span></span> 

    <span data-ttu-id="5f27a-117">Sayım, Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'taki örneklerin sayısından veya Elektronik Faturalama hizmetinin etkinleştirildiği tüzel kişilik sayısından bağımsız olarak, kuruluşunuzun kiracı kimliğine göre özetlenir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="5f27a-118">Gösterge: Aylık kullanım (dışa aktar)</span><span class="sxs-lookup"><span data-stu-id="5f27a-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="5f27a-119">Bu gösterge, kuruluşunuzun tanımlı bir dönemde kestiği elektronik faturalar hakkında ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5f27a-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="5f27a-120">Kapsam</span><span class="sxs-lookup"><span data-stu-id="5f27a-120">Scope</span></span>
- <span data-ttu-id="5f27a-121">Bu iş belgelerinin içerdiği satır sayısına bakmaksızın, Finance ve Supply Chain Management'tan Elektronik Faturalama hizmetine gönderilen iş belgelerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="5f27a-122">Elektronik Faturalama servisi tarafından başarıyla işlenen gönderilen iş belgelerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="5f27a-123">Özellik kurulumunda tanımlanan eylemlerin akışı tamamlandığında, bir belge başarıyla işlenmiş olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="5f27a-124">Bir elektronik fatura harici bir web servisine gönderildiğinde, sayım işlemi web hizmeti işlemenin sonuçlarından (kabul edildi, reddedildi veya şema doğrulama hatası) bağımsız olur.</span><span class="sxs-lookup"><span data-stu-id="5f27a-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="5f27a-125">Web servisi, Elektronik Faturalama servisinin isteğini alıp yanıtlamışsa gönderim geçerli bir sayım olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="5f27a-126">**Özel durum:** Finance ve Supply Chain Management'tan Elektronik Faturalama hizmetine yeniden gönderme yapıldığında iş belgeleri sayılmaz (örneğin elektronik faturanın durumunu değiştirmek için aynı iş belgesi yeniden giriş işlemi yapılması gerektiği senaryolarda).</span><span class="sxs-lookup"><span data-stu-id="5f27a-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="5f27a-127">Örneğin, Brezilya elektronik faturasının (mali belge) gönderilmesi geçerli olarak sayılır, ancak bunun iptal isteği sayılmaz.</span><span class="sxs-lookup"><span data-stu-id="5f27a-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="5f27a-128">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="5f27a-128">Calculation</span></span>

<span data-ttu-id="5f27a-129">Bakiye hesabı aşağıdaki gibi hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="5f27a-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="5f27a-130">Bakiye = Ücretsiz + Satın alınan – Kullanılan</span><span class="sxs-lookup"><span data-stu-id="5f27a-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="5f27a-131">Where:</span><span class="sxs-lookup"><span data-stu-id="5f27a-131">Where:</span></span>

- <span data-ttu-id="5f27a-132">Ücretsiz:</span><span class="sxs-lookup"><span data-stu-id="5f27a-132">Free:</span></span>
  
    <span data-ttu-id="5f27a-133">Müşterinin ayda gönderebileceği, ücretsiz iş belgeleri hacmi.</span><span class="sxs-lookup"><span data-stu-id="5f27a-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="5f27a-134">Elektronik Faturalama servisine gönderilebilecek 100 iş belgesi paketini içerir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="5f27a-135">Ücretsiz hacim birikimli değildir ve kalan bakiye bir sonraki döneme aktarılmaz.</span><span class="sxs-lookup"><span data-stu-id="5f27a-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="5f27a-136">Satın alınan:</span><span class="sxs-lookup"><span data-stu-id="5f27a-136">Purchased:</span></span>
  
    <span data-ttu-id="5f27a-137">Elektronik Faturalama servisine gönderilebilecek 1,000 iş belgesi paketi.</span><span class="sxs-lookup"><span data-stu-id="5f27a-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="5f27a-138">Kuruluşunuz için aylık olarak bu paketin edinilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="5f27a-139">Satın alınan hacim birikimli değildir ve kalan bakiye bir sonraki döneme aktarılmaz.</span><span class="sxs-lookup"><span data-stu-id="5f27a-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="5f27a-140">Kullanılan:</span><span class="sxs-lookup"><span data-stu-id="5f27a-140">Used:</span></span> 

    <span data-ttu-id="5f27a-141">Tanımlanan ölçütlere göre, Elektronik Faturalama servisine gönderilen iş belgesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="5f27a-142">Organizasyonunuz, ücretsiz 100 gönderilik aylık hacmini aşmayı planlıyorsa, Elektronik Faturalama hizmeti için Microsoft lisans ilkesiyle uyumlu kalmasını sağlamak için zirve hacmi satın alın.</span><span class="sxs-lookup"><span data-stu-id="5f27a-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="5f27a-143">Şu anda, satın alınan birimin, çoklu 1.000'lik gönderim paketi olarak alım tarihine göre el ile girilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="5f27a-144">Gösterge: Özelliğe göre kullanım</span><span class="sxs-lookup"><span data-stu-id="5f27a-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="5f27a-145">Bu gösterge, tanımlanan bir dönemde elektronik faturaların gönderilmesi için elektronik faturalama özelliklerinin kullanımını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="5f27a-146">Hesaplama:</span><span class="sxs-lookup"><span data-stu-id="5f27a-146">Calculation:</span></span>
  
    <span data-ttu-id="5f27a-147">Kullanılan = İş belgelerinin Elektronik Faturalama hizmetine gönderilmesi sırasında her bir elektronik faturalama özelliğinin kaç kez kullanıldığı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="5f27a-148">Gösterge: Ortama göre kullanım</span><span class="sxs-lookup"><span data-stu-id="5f27a-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="5f27a-149">Bu gösterge, tanımlanan bir dönem içindeki elektronik faturalama servis ortamlarının kullanımını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="5f27a-150">Hesaplama:</span><span class="sxs-lookup"><span data-stu-id="5f27a-150">Calculation:</span></span>
    
    <span data-ttu-id="5f27a-151">Kullanılan = İş belgelerinin Elektronik Faturalama hizmetine gönderilmesi sırasında her bir elektronik faturalama servis ortamının kaç kez kullanıldığı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="5f27a-152">Gösterge: Aylık kullanım (içe aktar)</span><span class="sxs-lookup"><span data-stu-id="5f27a-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="5f27a-153">Bu gösterge, tanımlı bir dönemde Elektronik Faturalama servisi tarafından Finance ve Supply Chain Management'a göre elektronik faturaların içe aktarılma hacmini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="5f27a-154">Kapsam:</span><span class="sxs-lookup"><span data-stu-id="5f27a-154">Scope:</span></span>

    <span data-ttu-id="5f27a-155">Finance ve Supply Chain Management'a aktarılan elektronik faturalar, bu elektronik faturaların içerdiği satır sayısından bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="5f27a-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="5f27a-156">Hesaplama:</span><span class="sxs-lookup"><span data-stu-id="5f27a-156">Calculation:</span></span>

    <span data-ttu-id="5f27a-157">Alınan = Finance ve Supply Chain Management'a aktarılan elektronik faturaların sayısı.</span><span class="sxs-lookup"><span data-stu-id="5f27a-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="5f27a-158">İşlevler</span><span class="sxs-lookup"><span data-stu-id="5f27a-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="5f27a-159">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5f27a-159">Purchase</span></span>

<span data-ttu-id="5f27a-160">**Aylık kullanım (dışa aktar)** sekmesinde, alınan gönderimler tutarını el ile kaydetmek için **Satın al** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5f27a-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="5f27a-161">Belirli bir tarih için, **Yeni**'yi seçin ve bu tarihte elde edilen **Paketler** sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="5f27a-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="5f27a-162">**Miktar** aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="5f27a-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="5f27a-163">Miktar = Paket \* 1.000</span><span class="sxs-lookup"><span data-stu-id="5f27a-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="5f27a-164">Hesaplanan **Miktar**, **Ay başına gösterge (dışa aktar)** göstergesindeki **Satın alınan** değerini yansıtır.</span><span class="sxs-lookup"><span data-stu-id="5f27a-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="5f27a-165">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f27a-165">Update</span></span>

<span data-ttu-id="5f27a-166">Eylem bölmesinde, hesaplamayı yenilemek ve sayfada ve grafikte gösterilen verileri güncelleştirmek için **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5f27a-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="5f27a-167">Geçmiş verilerini sıfırla</span><span class="sxs-lookup"><span data-stu-id="5f27a-167">Reset history data</span></span>

<span data-ttu-id="5f27a-168">Eylem bölmesinde, göstergelerin hesaplandığı veritabanını yenilemek için **Geçmiş verileri sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5f27a-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="5f27a-169">**Kullanım yönetimi** panosu, parasal tutarları göstermez.</span><span class="sxs-lookup"><span data-stu-id="5f27a-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="5f27a-170">Bunun yerine, yalnızca sayılan gönderimlerin ve içe aktarılan belgelerin hacmini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f27a-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
