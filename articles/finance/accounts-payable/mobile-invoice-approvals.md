---
title: Mobil fatura onayları
description: Bu konu, mobil için satıcı faturası onaylarını bir kullanım durumu olarak kullanarak mobil senaryolar tasarlamak amacıyla partik bir yaklaşım sunmak üzere hazırlanmıştır.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448767"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="77de6-103">Mobil fatura onayları</span><span class="sxs-lookup"><span data-stu-id="77de6-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77de6-104">Mobil özellikler, bir işletmenin mobil deneyimler tasarlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="77de6-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="77de6-105">Gelişmiş senaryolar için platform geliştiricilerin de yeteneklerini istedikleri gibi genişletmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="77de6-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="77de6-106">Mobildeki yeni kavramlardan bazıları hakkında bilgi edinmek için en etkili yol, bir kaç senaryo tasarlama işleminde ilerlemektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="77de6-107">Bu konu, mobil için satıcı faturası onaylarını bir kullanım durumu olarak kullanarak mobil senaryolar tasarlamak amacıyla partik bir yaklaşım sunmak üzere hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="77de6-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="77de6-108">Bu konu, senaryoların farklı çeşitlerini tasarlamanıza yardımcı olur ve satıcı faturalarıyla ilgili olmayan diğer senaryolara da uygulanablir.</span><span class="sxs-lookup"><span data-stu-id="77de6-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="77de6-109">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="77de6-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="77de6-110">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="77de6-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="77de6-111">Açıklama</span><span class="sxs-lookup"><span data-stu-id="77de6-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77de6-112">Mobil el kitabı ön okuma</span><span class="sxs-lookup"><span data-stu-id="77de6-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="77de6-113">Mobil platform</span><span class="sxs-lookup"><span data-stu-id="77de6-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="77de6-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="77de6-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="77de6-115">Sürüm 1611 ve Platform güncelleştirmesi 3'e sahip bir ortam (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="77de6-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="77de6-116">KB 3204341 numaralı düzeltmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="77de6-117">Görev kaydedici, Platform güncelleştirmesi 3'te (Kasım 2016 güncellemesi) bulunan açılır iletişim kutusu için yanlışlıkla iki Kapat komutu kaydedebilir.</span><span class="sxs-lookup"><span data-stu-id="77de6-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="77de6-118">KB 3207800 numaralı düzeltmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="77de6-119">Bu düzeltme, eklerin Platform güncelleştirmesi 3'te (Kasım 2016 güncelleştirmesi) bulunan mobil istemcide görüntülenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="77de6-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="77de6-120">KB 3208224 numaralı düzeltmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="77de6-121">Sürüm 7.0.1'e (Mayıs 2016) dahil edilen mobil satıcı faturası onayı uygulaması için uygulama kodu.</span><span class="sxs-lookup"><span data-stu-id="77de6-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="77de6-122">Mobil uygulama yüklenmiş olan bir Android, iOS veya Windows cihazı.</span><span class="sxs-lookup"><span data-stu-id="77de6-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="77de6-123">Uygulamayı ilgili uygulama mağazasında arayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="77de6-124">Giriş</span><span class="sxs-lookup"><span data-stu-id="77de6-124">Introduction</span></span>
<span data-ttu-id="77de6-125">Satıcı faturaları için mobil onaylar "Önkoşullar" bölümünde açıklanan üç düzeltmenin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="77de6-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="77de6-126">Bu düzeltmeler fatura onayları için bir çalışma alanı sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="77de6-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="77de6-127">Mobil bağlamında çalışma alanının ne olduğunu öğrenmek için, "Önkoşullar" bölümünde belirtilen mobil el kitabını okuyun.</span><span class="sxs-lookup"><span data-stu-id="77de6-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="77de6-128">Fatura onayları çalışma alanının tasarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="77de6-129">Her kuruluş satıcı faturaları için kendi iş sürecini farklı şekilde düzenler ve tanımlar.</span><span class="sxs-lookup"><span data-stu-id="77de6-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="77de6-130">Satıcı fatura onayları için bir mobil deneyim tasarlamadan önce iş sürecinin aşağıdaki yönlerini göz önünde bulundurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="77de6-131">Fikir, cihaz üzerindeki kullanıcı deneyimini en iyi duruma getirmek için mümkün olduğunca çok veri noktası kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="77de6-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="77de6-132">Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="77de6-133">Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="77de6-134">Faturada kaç adet fatura satırı var?</span><span class="sxs-lookup"><span data-stu-id="77de6-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="77de6-135">Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.</span><span class="sxs-lookup"><span data-stu-id="77de6-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="77de6-136">Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu?</span><span class="sxs-lookup"><span data-stu-id="77de6-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="77de6-137">Bu soruya yanıt Evet ise, aşağıdaki soruları göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="77de6-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="77de6-138">Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, bölmeler vb.) vardır?</span><span class="sxs-lookup"><span data-stu-id="77de6-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="77de6-139">Yine, 80-20 kuralını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="77de6-140">Faturaların fatura başlığında da hesap dağıtımları var mı?</span><span class="sxs-lookup"><span data-stu-id="77de6-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="77de6-141">Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="77de6-142">Bu konuda hesap dağıtımlarının nasıl düzenleneceği açıklanmamaktadır çünkü bu işlevsellik şu anda mobil senaryolar için desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="77de6-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="77de6-143">Kullanıcılar cihazda fatura için ekleri görmek ister mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="77de6-144">Fatura onayları için mobil deneyimi tasarımı, bu sorulara bağlı olarak farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="77de6-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="77de6-145">Amaç, bir kuruluş içinde mobildeki iş süreci için kullanıcı deneyimini en iyi duruma getirmektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="77de6-146">Bu konunun devamında, yukarıdaki sorulara verilecek farklı yanıtları temel alan iki senaryo çeşidine bakacağız.</span><span class="sxs-lookup"><span data-stu-id="77de6-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="77de6-147">Genel bir yönerge olarak, mobil tasarımcıyla çalışırken güncelleştirmelerin kaybolmasını önlemek için değişiklikleri "yayımlamadığınızdan' emin olun.</span><span class="sxs-lookup"><span data-stu-id="77de6-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="77de6-148">Contoso için basit bir fatura onayı senaryosu tasarlama</span><span class="sxs-lookup"><span data-stu-id="77de6-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77de6-149">Senaryo özniteliği</span><span class="sxs-lookup"><span data-stu-id="77de6-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="77de6-150">Yanıt</span><span class="sxs-lookup"><span data-stu-id="77de6-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77de6-151">Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="77de6-152">Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="77de6-152">Vendor name</span></span></li>
<li><span data-ttu-id="77de6-153">Fatura toplamı</span><span class="sxs-lookup"><span data-stu-id="77de6-153">Invoice total</span></span></li>
<li><span data-ttu-id="77de6-154">Fatura hesabı</span><span class="sxs-lookup"><span data-stu-id="77de6-154">Invoice account</span></span></li>
<li><span data-ttu-id="77de6-155">Fatura numarası</span><span class="sxs-lookup"><span data-stu-id="77de6-155">Invoice number</span></span></li>
<li><span data-ttu-id="77de6-156">Fatura tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-156">Invoice date</span></span></li>
<li><span data-ttu-id="77de6-157">Fatura açıklaması</span><span class="sxs-lookup"><span data-stu-id="77de6-157">Invoice description</span></span></li>
<li><span data-ttu-id="77de6-158">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-158">Due date</span></span></li>
<li><span data-ttu-id="77de6-159">Fatura para birimi</span><span class="sxs-lookup"><span data-stu-id="77de6-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-160">Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="77de6-161">Tedarik kategorisi</span><span class="sxs-lookup"><span data-stu-id="77de6-161">Procurement category</span></span></li>
<li><span data-ttu-id="77de6-162">Miktar</span><span class="sxs-lookup"><span data-stu-id="77de6-162">Quantity</span></span></li>
<li><span data-ttu-id="77de6-163">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="77de6-163">Unit price</span></span></li>
<li><span data-ttu-id="77de6-164">Satır net tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-164">Line net amount</span></span></li>
<li><span data-ttu-id="77de6-165">Vergi beyan tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-166">Faturada kaç adet fatura satırı var?</span><span class="sxs-lookup"><span data-stu-id="77de6-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="77de6-167">Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.</span><span class="sxs-lookup"><span data-stu-id="77de6-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="77de6-168">1</span><span class="sxs-lookup"><span data-stu-id="77de6-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-169">Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu?</span><span class="sxs-lookup"><span data-stu-id="77de6-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="77de6-170">Evet</span><span class="sxs-lookup"><span data-stu-id="77de6-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-171">Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, vb.) vardır?</span><span class="sxs-lookup"><span data-stu-id="77de6-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="77de6-172">Yine, 80-20 kuralını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="77de6-173">Genişletilmiş fiyat: 2 Satış vergisi: 0 Giderler: 0</span><span class="sxs-lookup"><span data-stu-id="77de6-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-174">Faturaların fatura başlığında da hesap dağıtımları var mı?</span><span class="sxs-lookup"><span data-stu-id="77de6-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="77de6-175">Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="77de6-176">Kullanılmıyor</span><span class="sxs-lookup"><span data-stu-id="77de6-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-177">Kullanıcılar cihazda fatura için ekleri görmek ister mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="77de6-178">Evet</span><span class="sxs-lookup"><span data-stu-id="77de6-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="77de6-179">Çalışma alanını oluştur</span><span class="sxs-lookup"><span data-stu-id="77de6-179">Create the workspace</span></span>

1.  <span data-ttu-id="77de6-180">Tarayıcıdan uygulamada oturum açın.</span><span class="sxs-lookup"><span data-stu-id="77de6-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="77de6-181">Oturum açtıktan sonra, URL'ye aşağıdaki örnekte gösterildiği gibi **&mode=mobile** ekleyin ve sayfayı yenileyin: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="77de6-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="77de6-182">Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="77de6-183">Mobil uygulama tasarımcısı Görev kaydedicinin göründüğü şekilde görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="77de6-184">Yeni bir çalışma alanı oluşturmak için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="77de6-185">Bu örnek için çalışma alanı adı **Onaylarım**'dır.</span><span class="sxs-lookup"><span data-stu-id="77de6-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="77de6-186">Açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="77de6-186">Enter a description.</span></span>
6.  <span data-ttu-id="77de6-187">Çalışma alanı rengi seçin.</span><span class="sxs-lookup"><span data-stu-id="77de6-187">Select a workspace color.</span></span> <span data-ttu-id="77de6-188">Çalışma alanı rengi, bu çalışma alanı için mobil deneyimin genel tarzı olarak kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="77de6-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="77de6-189">Çalışma alanı için bir simge seçin.</span><span class="sxs-lookup"><span data-stu-id="77de6-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="77de6-190">**Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-190">Click **Done**</span></span>
9.  <span data-ttu-id="77de6-191">Değişikliklerinizi kaydetmek için **Çalışma alanını yayımla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="77de6-192">Bana atanan satıcı faturaları</span><span class="sxs-lookup"><span data-stu-id="77de6-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="77de6-193">İlk tasarlamanız gereken mobil sayfa incelenmek üzere kullanıcıya atılan faturaların listesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="77de6-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="77de6-194">Bu mobil sayfayı tasarlamak için **VendMobileInvoiceAssignedToMeListPage** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="77de6-195">Bu yordamı tamamlamadan önce, en az bir satıcı faturasının gözden geçirilmek üzere size atandığından ve fatura satırında iki dağıtım olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="77de6-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="77de6-196">Bu kurulum bu senaryo için gereksinimleri karşılar.</span><span class="sxs-lookup"><span data-stu-id="77de6-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="77de6-197">**Borç hesapları** modülündeki **Bana atanmış bekleyen satıcı faturalarının** listesi sayfasının mobil sürümünü açmak için URL'de menü öğesi adını **VendMobileInvoiceAssignedToMeListPage** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77de6-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="77de6-198">Sisteminizde size atanan fatura sayısına bağlı olarak, sayfa bu faturaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="77de6-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="77de6-199">Belirli bir faturayı bulmak için soldaki filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77de6-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="77de6-200">Ancak, bu örnek için bize belirli bir fatura gerekmiyor.</span><span class="sxs-lookup"><span data-stu-id="77de6-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="77de6-201">Yalnızca mobil sayfanızı tasarlamanıza olanak tanıyacak size atanmış bazı faturalar olması gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="77de6-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="77de6-202">Kullanılabilir yeni sayfalar özellikle satıcı faturası için mobil senaryolar geliştirmek üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="77de6-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="77de6-203">Bu nedenle, bu sayfaları kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="77de6-204">URL aşağıdaki URL'ye benzer olmalıdır ve bunu girdikten sonra resimde gösterilen sayfada şu görünmelidir: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="77de6-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="77de6-205">[![Bana atanmış bekleyen satıcı faturaları sayfası](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="77de6-206">Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="77de6-207">Çalışma alanınızı seçin ve **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="77de6-208">İlk mobil sayfayı oluşturmak için **Sayfa ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="77de6-209">**Satıcı faturalarım** gibi bir ad ve **Bana gözden geçirilmek üzere atanan satıcı faturaları** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="77de6-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="77de6-210">**Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-210">Click **Done**.</span></span>
7.  <span data-ttu-id="77de6-211">Mobil tasarımcıda, **Alanlar** sekmesinde, **Alanları seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="77de6-212">Liste sayfasındaki sütunlar aşağıda gösterilene benzemelidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="77de6-213">[![Bana atanmış bekleyen satıcı faturaları sayfasındaki sütunlar](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="77de6-214">Mobil sayfada kullanıcılara gösterilecek sütunları liste sayfasından ekleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="77de6-215">Sütunları ekleme sıranız alanların son kullanıcıya gösterileceği sıradır.</span><span class="sxs-lookup"><span data-stu-id="77de6-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="77de6-216">Alanların sıralamasını değiştirmenin tek yolu tüm alanları yeniden seçmektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="77de6-217">Bu senaryonun gereksinimlerine bağlı olarak, aşağıdaki sekiz alan gereklidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="77de6-218">Ancak, bazı kullanıcılar mobil cihazda sunmak için sekiz alanın çok fazla bilgi olduğunu düşünebilir.</span><span class="sxs-lookup"><span data-stu-id="77de6-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="77de6-219">Bu nedenle, mobil liste görünümünde yalnızca en önemli alanları göstereceğiz.</span><span class="sxs-lookup"><span data-stu-id="77de6-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="77de6-220">Geri kalan alanlar, daha sonra tasarlayacağımız ayrıntılar görünümünde gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="77de6-221">Şu an için, aşağıdaki alanları ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="77de6-221">For now, we will add the following fields.</span></span> <span data-ttu-id="77de6-222">Mobil sayfaya eklemek için bu sütunlardaki artı işaretini (**+**) tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="77de6-223">Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="77de6-223">Vendor name</span></span>
    - <span data-ttu-id="77de6-224">Fatura toplamı</span><span class="sxs-lookup"><span data-stu-id="77de6-224">Invoice total</span></span>
    - <span data-ttu-id="77de6-225">Fatura hesabı</span><span class="sxs-lookup"><span data-stu-id="77de6-225">Invoice account</span></span>
    - <span data-ttu-id="77de6-226">Fatura numarası</span><span class="sxs-lookup"><span data-stu-id="77de6-226">Invoice number</span></span>
    - <span data-ttu-id="77de6-227">Fatura tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-227">Invoice date</span></span>

    <span data-ttu-id="77de6-228">Alanlar eklendikten sonra, mobil sayfa aşağıdaki resme benzer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="77de6-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="77de6-229">[![Alanlar eklendikten sonra sayfa](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="77de6-230">Daha sonra iş akışı eylemlerini etkinleştirebilmemiz için, şimdi aşağıdaki sütunları da eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="77de6-231">Tamamlanan görevi göster</span><span class="sxs-lookup"><span data-stu-id="77de6-231">Show complete task</span></span>
    - <span data-ttu-id="77de6-232">Göreve temsilci atamayı göster</span><span class="sxs-lookup"><span data-stu-id="77de6-232">Show delegate task</span></span>
    - <span data-ttu-id="77de6-233">Görevi geri çağırmayı göster</span><span class="sxs-lookup"><span data-stu-id="77de6-233">Show recall task</span></span>
    - <span data-ttu-id="77de6-234">Görevi reddetmeyi göster</span><span class="sxs-lookup"><span data-stu-id="77de6-234">Show reject task</span></span>
    - <span data-ttu-id="77de6-235">Talep tamamlama görevini göster</span><span class="sxs-lookup"><span data-stu-id="77de6-235">Show request completion task</span></span>
    - <span data-ttu-id="77de6-236">Yeniden gönderme görevini göster</span><span class="sxs-lookup"><span data-stu-id="77de6-236">Show resubmit task</span></span>

10. <span data-ttu-id="77de6-237">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="77de6-238">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="77de6-239">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="77de6-240">**Fatura** altından borç hesapları parametrelerindeki **Bekleyen satıcı faturaları listesinde fatura toplamını görüntüle**'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="77de6-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="77de6-241">Yalnızca bu parametre etkinleştirilerek, fatura toplamlarının bekleyen satıcı faturaları liste sayfasında gösterilmek üzere hesaplanacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="77de6-242">Bu, ön koşul olan 3208224 no'lu düzeltmenin bir parçası olan yeni bir yetenektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="77de6-243">Satıcı faturası ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="77de6-243">Vendor invoice details</span></span>

<span data-ttu-id="77de6-244">Mobil için fatura ayrıntıları sayfasını tasarlamak için **VendMobileInvoiceHeaderDetails** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="77de6-245">Sisteminizdeki faturaların sayısına bağlı olarak, bu sayfanın en eski faturayı (ilk oluşturulan fatura) gösterdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="77de6-246">Belirli bir faturayı bulmak için soldaki filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77de6-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="77de6-247">Ancak, bu örnek için bize belirli bir fatura gerekmiyor.</span><span class="sxs-lookup"><span data-stu-id="77de6-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="77de6-248">Mobil sayfayı tasarlayabilmek için sadece bazı fatura verileri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="77de6-249">[![İş akışı sayfası](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="77de6-250">URL'de formu açmak için menü öğesinin adını **VendMobileInvoiceHeaderDetails** olarak değiştirin</span><span class="sxs-lookup"><span data-stu-id="77de6-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="77de6-251">Mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın.</span><span class="sxs-lookup"><span data-stu-id="77de6-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="77de6-252">**Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="77de6-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="77de6-253">Daha önce oluşturduğunuz **Satıcı faturalarım** sayfasını seçin ve **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="77de6-254">**Alanlar** ssekmesinde **Izgara** sütun başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="77de6-255">**Özellikler &gt; Sayfa ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="77de6-256">**Not:** **Izgara** başlığına tıkladığınızde ve sayfa eklediğinizde, ayrıntılar sayfasıyla ilişki otomatik olarak kurulur.</span><span class="sxs-lookup"><span data-stu-id="77de6-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="77de6-257">**Fatura ayrıntıları** gibi bir sayfa başlığı ve **Fatura başlığı ve satır ayrıntılarını görüntüle** gibi bir açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="77de6-258">**Alanları seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-258">Click **Select fields**.</span></span> <span data-ttu-id="77de6-259">Ekleme sıranızın alanların son kullanıcıya gösterileceği sıra olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="77de6-260">Alanların sıralamasını değiştirmenin tek yolu tüm alanları yeniden seçmektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="77de6-261">Bu senaryonın gerekliliklerini temel alarak başlıktan aşağıdaki alanları ekleyin:</span><span class="sxs-lookup"><span data-stu-id="77de6-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="77de6-262">Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="77de6-262">Vendor name</span></span>
   - <span data-ttu-id="77de6-263">Fatura toplamı</span><span class="sxs-lookup"><span data-stu-id="77de6-263">Invoice total</span></span>
   - <span data-ttu-id="77de6-264">Fatura hesabı</span><span class="sxs-lookup"><span data-stu-id="77de6-264">Invoice account</span></span>
   - <span data-ttu-id="77de6-265">Fatura numarası</span><span class="sxs-lookup"><span data-stu-id="77de6-265">Invoice number</span></span>
   - <span data-ttu-id="77de6-266">Fatura tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-266">Invoice date</span></span>
   - <span data-ttu-id="77de6-267">Fatura açıklaması</span><span class="sxs-lookup"><span data-stu-id="77de6-267">Invoice description</span></span>
   - <span data-ttu-id="77de6-268">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-268">Due date</span></span>
   - <span data-ttu-id="77de6-269">Fatura para birimi</span><span class="sxs-lookup"><span data-stu-id="77de6-269">Invoice currency</span></span>

10. <span data-ttu-id="77de6-270">Sayfadaki satır kılavuzundan aşağıdaki alanları ekleyin:</span><span class="sxs-lookup"><span data-stu-id="77de6-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="77de6-271">Tedarik kategorisi</span><span class="sxs-lookup"><span data-stu-id="77de6-271">Procurement category</span></span>
    - <span data-ttu-id="77de6-272">Miktar</span><span class="sxs-lookup"><span data-stu-id="77de6-272">Quantity</span></span>
    - <span data-ttu-id="77de6-273">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="77de6-273">Unit price</span></span>
    - <span data-ttu-id="77de6-274">Satır net tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-274">Line net amount</span></span>
    - <span data-ttu-id="77de6-275">Vergi beyan tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-275">1099 amount</span></span>

11. <span data-ttu-id="77de6-276">Önceki iki adımda tüm alanları ekledikten sonra **Bitti**'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="77de6-277">Bu sayfa aşağıda gösterilene benzemelidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="77de6-278">[![Alanlar eklendikten sonra sayfa](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="77de6-279">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="77de6-280">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="77de6-281">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="77de6-282">İş akışı eylemleri</span><span class="sxs-lookup"><span data-stu-id="77de6-282">Workflow actions</span></span>

<span data-ttu-id="77de6-283">İş akışı eylemleri eklemek için **VendMobileInvoiceHeaderDetails** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="77de6-284">Bu sayfayı açmak için daha önce yaptığınız gibi URL'deki menü öğesi adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77de6-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="77de6-285">Ardından mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın.</span><span class="sxs-lookup"><span data-stu-id="77de6-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="77de6-286">Ayrıntılar sayfasında iş akışı eylemlerini eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="77de6-287">Tasarım yapacağınız iş akışı eylemlerini kullanılabilir yapacak uygun durumdaki faturaların size atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="77de6-288">İş akışı eylemlerini kaydedin</span><span class="sxs-lookup"><span data-stu-id="77de6-288">Record workflow actions</span></span>
1.  <span data-ttu-id="77de6-289">**Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="77de6-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="77de6-290">Daha önce oluşturduğunuz **Fatura ayrıntılarım** sayfasını seçin ve **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="77de6-291">**Eylemler** sekmesinde **Eylem ekle** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="77de6-292">**Onayla** gibi bir eylem başlığı ve **Faturayı onayla** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="77de6-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="77de6-293">Girdiğiniz eylem başlığının mobil uygulamada kullanıcıya gösterilen eylemin adı olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="77de6-294">**Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-294">Click **Done**.</span></span>
6.  <span data-ttu-id="77de6-295">**Alanları seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="77de6-296">**VendMobileInvoiceHeaderDetails** sayfasında iş akışı işleminde ilerleyin ve kaydetmek istediğiniz eylemi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="77de6-297">Bu işlem sırasında iş akışı yorumları girdiğinizden emin olun, böylece mobil deneyime bir yorum alanı da eklenmiş olur.</span><span class="sxs-lookup"><span data-stu-id="77de6-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="77de6-298">İş akışı eylemi çalıştırıldıktan sonra **Bitti**'ye tıklayarak Alan seç görevini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="77de6-299">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="77de6-300">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="77de6-301">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="77de6-302">Gerekli tüm iş akışı eylemlerini kaydetmek önceki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="77de6-303">Bir .js dosyası oluştur</span><span class="sxs-lookup"><span data-stu-id="77de6-303">Create a .js file</span></span>
1. <span data-ttu-id="77de6-304">Not Defteri'ni veya Microsoft Visual Studio'yu açın ve aşağıdaki kodu yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="77de6-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="77de6-305">Dosyayı .js dosyası olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="77de6-305">Save the file as a .js file.</span></span> <span data-ttu-id="77de6-306">Bu kod şunu yapar:</span><span class="sxs-lookup"><span data-stu-id="77de6-306">This code does the following:</span></span>
    - <span data-ttu-id="77de6-307">Mobil listesi sayfasında daha önce eklediğimiz iş akışıyla ilgili ekstra sütunları gizler.</span><span class="sxs-lookup"><span data-stu-id="77de6-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="77de6-308">Bu sütunları uygulamanın bağlan hakkında bilgisi olması ve bir sonraki adımın gerçekleştirilebilmesi için ekledik.</span><span class="sxs-lookup"><span data-stu-id="77de6-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="77de6-309">Etkin olan iş akışı adımını temel alarak , yalnızca bu eylemleri göstermek için mantık uygular.</span><span class="sxs-lookup"><span data-stu-id="77de6-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="77de6-310">Sayfalardaki ve koddaki diğer denetimlerin adının çalışma alanındaki isimlerle aynı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="77de6-311">**Mantık** sekmesini seçerek kod dosyasını çalışma alanına yükleyin</span><span class="sxs-lookup"><span data-stu-id="77de6-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="77de6-312">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="77de6-313">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="77de6-314">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="77de6-315">Satıcı faturası ekleri</span><span class="sxs-lookup"><span data-stu-id="77de6-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="77de6-316">Sayfanın sağ üst kısmındaki **Ayarlar** (dişli) düğmesine ve ardından **Mobil uygulama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="77de6-317">**Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="77de6-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="77de6-318">Daha önce oluşturduğunuz <strong>Fatura ayrıntıları \*\*sayfasını seçin ve \*\*Düzenle</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="77de6-319">**Belge yönetimi** seçeneğini aşağıda gösterildiği gibi **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="77de6-320">**Not:** Mobil cihazda ekleri göstermek için hiçbir gereklilik yoksa, bu seçeneği varsayılan ayar olan **Hayır** olarak bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77de6-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Belge yönetimi](./media/docmanagement-216x300.png)

5. <span data-ttu-id="77de6-322">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="77de6-323">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="77de6-324">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="77de6-325">Satıcı faturası satırı dağıtımları</span><span class="sxs-lookup"><span data-stu-id="77de6-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="77de6-326">Bu senaryonun gereksinimleri yalnızca satır düzeyinde dağıtımlar olacağını ve bir faturada yalnızca bir satır bulunacağını onaylamaktadır.</span><span class="sxs-lookup"><span data-stu-id="77de6-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="77de6-327">Bu senaryo basit olduğundan, mobil cihazdaki kullanıcı deneyimi de kullanıcının dağıtımları görüntülemek için birçok satırın ayrıntısına bakmasını gerektirmeyecek kadar basit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="77de6-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="77de6-328">Satıcı faturalarında fatura başlığından tüm dağıtımları gösterme seçeneği bulunur.</span><span class="sxs-lookup"><span data-stu-id="77de6-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="77de6-329">Bu deneyim mobil senaryo için ihtiyacımız olan şeydir.</span><span class="sxs-lookup"><span data-stu-id="77de6-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="77de6-330">Bu nedenle, mobil senaryonun bu bölümünü tasarlamak için **VendMobileInvoiceAllDistributionTree** sayfasını kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="77de6-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="77de6-331">Gereksinimleri bilmek bize hangi belirli sayfayı kullanacağımıza ve senaryoyu tasarlarken tam olarak mobil deneyimi kullanıcı için ne kadar en iyi duruma getireceğimize karar vermede yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="77de6-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="77de6-332">İkinci senaryoda, bu senaryo için gereksinimler farklılık gösterdiğinden dağıtımları göstermek için farklı bir sayfa kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="77de6-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="77de6-333">Daha önce yaptığınız gibi URL'deki menü öğesi adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77de6-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="77de6-334">Görüntülenen sayfa aşağıdaki resimde gösterilen sayfaya benzemelidir.</span><span class="sxs-lookup"><span data-stu-id="77de6-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="77de6-335">[![Tüm dağıtımlar sayfası](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="77de6-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="77de6-336">Mobil tasarımcıyı **Ayarlar** (dişli) düğmesinden açın.</span><span class="sxs-lookup"><span data-stu-id="77de6-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="77de6-337">**Düzenle** düğmesine tıklayarak çalışma alanında düzenleme modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="77de6-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="77de6-338">**Not:** İki yeni sayfanın otomatik olarak oluşturulduğunu görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="77de6-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="77de6-339">Önceki bölümde belge yönetimini açmış olduğunuzdan, sistem bu sayfaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77de6-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="77de6-340">Bu yeni sayfaları yok sayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77de6-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="77de6-341">**Sayfa ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="77de6-342">**Muhasebeyi görüntüle** gibi bir sayfa başlığı ve **Fatura için muhasebeyi görüntüle** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="77de6-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="77de6-343">**Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-343">Click **Done**.</span></span>

7.  <span data-ttu-id="77de6-344">**Alan** sekmesinde, **Alanları seçin**'e tıklayın, dağıtımlar sayfasından aşağıdaki alanları seçin ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="77de6-345">Tutar</span><span class="sxs-lookup"><span data-stu-id="77de6-345">Amount</span></span>
    2.  <span data-ttu-id="77de6-346">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="77de6-346">Currency</span></span>
    3.  <span data-ttu-id="77de6-347">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="77de6-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="77de6-348">Dağıtım ızgarası içim **Açıklama** sütununu seçmedik çünkü bu senaryonun gereksinimleri genişletilmiş fiyatın dağıtımları olacak tek tutar olduğunu onayladı.</span><span class="sxs-lookup"><span data-stu-id="77de6-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="77de6-349">Bu nedenle, kullanıcının dağıtım yapılacak tutar türünü belirlemek için başka bir alan istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="77de6-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="77de6-350">Ancak, sonraki senaryoda, bu bilgiyi **kullanacağız** çünkü bu senaryo için gereksinimler diğer tutar türlerinin (örneğin, satış vergisi) dağıtımları olduğunu belirtiyor.</span><span class="sxs-lookup"><span data-stu-id="77de6-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="77de6-351">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="77de6-352">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="77de6-353">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="77de6-354">"Hesap görüntüleme" sayfasına gezinti ekleme</span><span class="sxs-lookup"><span data-stu-id="77de6-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="77de6-355">**Muhasebeyi görüntüle** mobil sayfası şu anda şimdiye kadar tasarlanan mobil sayfalara bağlı değildir.</span><span class="sxs-lookup"><span data-stu-id="77de6-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="77de6-356">Kullanıcı mobil cihazda **Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gidemeyeceğinden, **Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gezinme olanağı sağlamamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="77de6-357">Bu gezintiyi JavaScript aracılığıyla ek bir mantık kullanarak kurarız.</span><span class="sxs-lookup"><span data-stu-id="77de6-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="77de6-358">Daha önce oluşturduğunuz .js dosyasını açın ve aşağıdaki kodda vurgulanan satırları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="77de6-359">Bu kod iki şey gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="77de6-359">This code does two things:</span></span>
    1.  <span data-ttu-id="77de6-360">Bu, kullanıcıların doğrudan çalışma alanından **Muhasebeyi görüntüle** sayfasına gidememesini garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="77de6-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="77de6-361">**Fatura ayrıntıları** sayfasından **Muhasebeyi görüntüle** sayfasına gitme denetimi kurar.</span><span class="sxs-lookup"><span data-stu-id="77de6-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="77de6-362">Sayfalardaki ve koddaki diğer denetimlerin adının çalışma alanındaki isimlerle aynı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="77de6-363">Önceki kodun üzerine yazmak için **Mantık** sekmesini seçerek kod dosyasını çalışma alanına yükleyin</span><span class="sxs-lookup"><span data-stu-id="77de6-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="77de6-364">Düzenleme modundan çıkmak için **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="77de6-365">Çalışma alanından çıkmak için **Geri**'ye ve sonra **Bitti**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="77de6-366">Çalışmanızı kaydetmek için **Çalışma alanını yayımla**'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="77de6-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="77de6-367">Doğrulama</span><span class="sxs-lookup"><span data-stu-id="77de6-367">Validation</span></span>

<span data-ttu-id="77de6-368">Mobil cihazınızdan uygulamayı açıp kurulumunuza bağlanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="77de6-369">Satıcı faturalarının gözden geçirilmek üzere size atandığı şirkette oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="77de6-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="77de6-370">Aşağıdaki eylemleri gerçekleştirebilmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="77de6-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="77de6-371">**Onaylarım** çalışma alanına bakın.</span><span class="sxs-lookup"><span data-stu-id="77de6-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="77de6-372">**Onaylarım** çalışma alanı ayrıntılarına bakın **Satıcı faturalarım** sayfasını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="77de6-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="77de6-373">**Satıcı faturalarım** sayfasının ayrıntılarına bakın ve size atanmış olan faturaların listesini görün.</span><span class="sxs-lookup"><span data-stu-id="77de6-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="77de6-374">Faturalardan birinin ayrıntılarına bakın ve fatura başlığı ayrıntılarını ve satır ayrıntılarını görün.</span><span class="sxs-lookup"><span data-stu-id="77de6-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="77de6-375">Ayrıntılar sayfasında eklerin bağlantısına bakın ve bu bağlantıyı ekler listesine gitmek ve ekleri görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="77de6-376">Ayrıntılar sayfasında, **Muhasebeyi görüntüle** sayfasının bağlantısına bakın ve bu bağlantıyı dağıtımlar sayfasına gitmek ve dağıtımları görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="77de6-377">Ayrıntılar sayfasında aşağıdaki **Eylemler** menüsüne tıklayın ve iş akışı adımı için geçerli olan iş akışı eylemlerini gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="77de6-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="77de6-378">Fabrikam için karmaşık bir fatura onayı senaryosu tasarlama</span><span class="sxs-lookup"><span data-stu-id="77de6-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77de6-379">Senaryo özniteliği</span><span class="sxs-lookup"><span data-stu-id="77de6-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="77de6-380">Yanıt</span><span class="sxs-lookup"><span data-stu-id="77de6-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77de6-381">Kullanıcı mobil deneyimde fatura başlığından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="77de6-382">Satıcı adı</span><span class="sxs-lookup"><span data-stu-id="77de6-382">Vendor name</span></span></li>
<li><span data-ttu-id="77de6-383">Fatura tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-383">Invoice amount</span></span></li>
<li><span data-ttu-id="77de6-384">Fatura hesabı</span><span class="sxs-lookup"><span data-stu-id="77de6-384">Invoice account</span></span></li>
<li><span data-ttu-id="77de6-385">Fatura numarası</span><span class="sxs-lookup"><span data-stu-id="77de6-385">Invoice number</span></span></li>
<li><span data-ttu-id="77de6-386">Fatura tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-386">Invoice date</span></span></li>
<li><span data-ttu-id="77de6-387">Fatura açıklaması</span><span class="sxs-lookup"><span data-stu-id="77de6-387">Invoice description</span></span></li>
<li><span data-ttu-id="77de6-388">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="77de6-388">Due date</span></span></li>
<li><span data-ttu-id="77de6-389">Fatura para birimi</span><span class="sxs-lookup"><span data-stu-id="77de6-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-390">Kullanıcı mobil deneyimde fatura satırlarından hangi alanları ve hangi sırayla görmek ister?</span><span class="sxs-lookup"><span data-stu-id="77de6-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="77de6-391">Tedarik kategorisi</span><span class="sxs-lookup"><span data-stu-id="77de6-391">Procurement category</span></span></li>
<li><span data-ttu-id="77de6-392">Miktar</span><span class="sxs-lookup"><span data-stu-id="77de6-392">Quantity</span></span></li>
<li><span data-ttu-id="77de6-393">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="77de6-393">Unit price</span></span></li>
<li><span data-ttu-id="77de6-394">Satır net tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-394">Line net amount</span></span></li>
<li><span data-ttu-id="77de6-395">Vergi beyan tutarı</span><span class="sxs-lookup"><span data-stu-id="77de6-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-396">Faturada kaç adet fatura satırı var?</span><span class="sxs-lookup"><span data-stu-id="77de6-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="77de6-397">Burada 80-20 kuralını uygulayın ve yüzde 80 için iyileştirme yapın.</span><span class="sxs-lookup"><span data-stu-id="77de6-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="77de6-398">5</span><span class="sxs-lookup"><span data-stu-id="77de6-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-399">Kullanıcılar incelemeler sırasında mobil cihazda muhasebe dağıtımlarını (fatura kodlama) görmek istiyor mu?</span><span class="sxs-lookup"><span data-stu-id="77de6-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="77de6-400">Evet</span><span class="sxs-lookup"><span data-stu-id="77de6-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-401">Bir fatura satırı için kaç tane hesap dağıtımı (genişletilmiş fiyat, satış vergisi, giderler, vb.) vardır?</span><span class="sxs-lookup"><span data-stu-id="77de6-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="77de6-402">Yine, 80-20 kuralını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="77de6-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="77de6-403">Genişletilmiş fiyat: 2 Satış vergisi: 2 Giderler: 2</span><span class="sxs-lookup"><span data-stu-id="77de6-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77de6-404">Faturaların fatura başlığında da hesap dağıtımları var mı?</span><span class="sxs-lookup"><span data-stu-id="77de6-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="77de6-405">Öyleyse, bu hesap dağıtımlarının cihazda kullanılabilir olması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="77de6-406">Kullanılmıyor</span><span class="sxs-lookup"><span data-stu-id="77de6-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="77de6-407">Kullanıcılar cihazda fatura için ekleri görmek ister mi?</span><span class="sxs-lookup"><span data-stu-id="77de6-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="77de6-408">Evet</span><span class="sxs-lookup"><span data-stu-id="77de6-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="77de6-409">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="77de6-409">Next steps</span></span>

<span data-ttu-id="77de6-410">Senaryo 1 için senaryo 2 gereksinimleri temel alınarak aşağıdaki çeşitlemeler yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="77de6-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="77de6-411">Bu bölümü mobil uygulama deneyiminizi geliştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77de6-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="77de6-412">Senaryo 2'de daha fazla fatura satırı beklendiğinden, tasarımda yapılacak aşağıdaki değişiklikler mobil cihazdaki kullanıcı deneyimini en iyi duruma getirmeye yardımcı olacaktır:</span><span class="sxs-lookup"><span data-stu-id="77de6-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="77de6-413">Fatura satırlarını ayrıntılar sayfasında görüntülemek yerine (senaryo 1'de olduğu gibi), kullanıcılar satırları ayrı bir mobil sayfada görüntülemeyi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="77de6-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="77de6-414">Bu senaryoda birden fazla fatura satırı olması beklendiğinden, mobil için dağıtımları tasarlamak amacıyla **VendMobileInvoiceAllDistributionTree** sayfası kullanılırsa (senaryo 1'de olduğu gibi), kullanıcı için satırları dağıtımlarla ilişkilendirmek kafa karıştırıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="77de6-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="77de6-415">Bu nedenle, dağıtımlar sayfasını tasarlamak için **VendMobileInvoiceLineDistributionTree** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="77de6-416">İdeal olarak, bu senaryoda dağıtımların bir fatura satırı bağlamında gösterilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="77de6-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="77de6-417">Bu nedenle, kullanıcının dağıtımlar sayfasını görmek için bir satırın ayrıntılarına inebildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="77de6-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="77de6-418">Senaryo 1'de başlık ve ayrıntılar sayfaları için yaptığınız gibi, detaylandırma kurmak için sayfa bağlantısı yeteneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="77de6-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="77de6-419">Senaryo 2'deki dağıtımlarda birden fazla tutar türü olması beklendiğinden (satış vergisi, giderler, vb.) tutar türü açıklamasını görüntülemek yararlı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="77de6-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="77de6-420">(Bu bilgiyi senaryo 1'de atlamıştık.)</span><span class="sxs-lookup"><span data-stu-id="77de6-420">(We omitted this information in scenario 1.)</span></span>




