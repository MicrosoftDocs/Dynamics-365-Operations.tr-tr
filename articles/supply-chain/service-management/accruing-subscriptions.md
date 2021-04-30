---
title: Tahakkuk eden abonelikler
description: Servis abonelikleriyle, işlem harcını faturaladığınız tarihi izleyen dönemlerde geliri el ile tahakkuk ettirebilirsiniz.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a2b581c8ae52f4c379e8e511dc898a8d106d149
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908072"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="9008c-103">Tahakkuk eden abonelikler</span><span class="sxs-lookup"><span data-stu-id="9008c-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9008c-104">Servis abonelikleriyle, işlem harcını faturaladığınız tarihi izleyen dönemlerde geliri el ile tahakkuk ettirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="9008c-105">Abonelik ücreti için ayarladığınız fatura dönemi için tahakkuk dönemleri oluşturulur, ve tahakkuk dönemlerinde aboneliğin dönem kodu temel alınır.</span><span class="sxs-lookup"><span data-stu-id="9008c-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="9008c-106">Geliri tahakkuk ettirebilir ve tahakkuk eden geliri ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="9008c-107">Alacak tutarlarına ters tahakkuk işlemi uygulama</span><span class="sxs-lookup"><span data-stu-id="9008c-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="9008c-108">Faturalanmış abonelik tutarlarını alacaklandırabilir, tahakkuk eden tutarlara ters işlem uygulamak için iki yöntem kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9008c-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="9008c-109">Hareket için bir alacak dekont teklifi oluşturmadan önce her tahakkuk eden gelir hareketini el ile ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="9008c-110">Bu, el ile yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="9008c-110">This is the manual method.</span></span> <span data-ttu-id="9008c-111">(el ile)</span><span class="sxs-lookup"><span data-stu-id="9008c-111">(manual)</span></span>

  - <span data-ttu-id="9008c-112">Alacak dekontunun deftere nakledildiği tarihte veya tahakkukun orijinal deftere nakil tarihinde tahakkuk eden tutarlara tersine işlem uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="9008c-113">Daha fazla bilgi için bkz. [Abonelik parametreleri (form)](/dynamicsax-2012//subscription-parameters-form).</span><span class="sxs-lookup"><span data-stu-id="9008c-113">For more information, see [Subscription parameters (form)](/dynamicsax-2012//subscription-parameters-form).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="9008c-114">Gereksinimler kurulumu</span><span class="sxs-lookup"><span data-stu-id="9008c-114">Setup requirements</span></span>

<span data-ttu-id="9008c-115">Geliri tahakkuk ettirmek için, aşağıdaki veri gereksinimlerinin karşılandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9008c-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="9008c-116">Hesap kurulumu</span><span class="sxs-lookup"><span data-stu-id="9008c-116">Account setup</span></span>

<span data-ttu-id="9008c-117">**Proje** modülünde **Süren İş - abonelik** ve **Tahakkuk eden gelir - abonelik** hesapları ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9008c-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="9008c-118">Tahakkuk eden geliri deftere naklettiğinizde, **Süren iş - abonelik** hesabı tahakkuk tutarında borçlandırılır ve **Tahakkuk eden gelir - abonelik** hesabı tahakkuk tutarında alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="9008c-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="9008c-119">Abonelik gelirinin tahakkuku için hesapların kurulumu</span><span class="sxs-lookup"><span data-stu-id="9008c-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="9008c-120">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Deftere nakil** \> **Genel muhasebe deftere nakil ayarı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="9008c-121">**Gelir hesapları** sekmesine tıklayın, **Süren iş - abonelik** veya **Tahakkuk eden gelir - abonelik** seçeneğini belirterek hesapları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="9008c-122">Abonelik grubu kurulumu</span><span class="sxs-lookup"><span data-stu-id="9008c-122">Subscription group setup</span></span>

<span data-ttu-id="9008c-123">Abonelikler için gelir tahakkuku yapabilmek için **Gelir tahakkuku** onay kutusunun seçilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9008c-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="9008c-124">Bu, aboneliğe eklenmiş gruba yönelik **Abonelik grupları** formunda bulunur.</span><span class="sxs-lookup"><span data-stu-id="9008c-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="9008c-125">**Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="9008c-126">Abonelik grubunda gelir tahakkukunu etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9008c-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="9008c-127">**Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="9008c-128">Dönemler</span><span class="sxs-lookup"><span data-stu-id="9008c-128">Periods</span></span>

<span data-ttu-id="9008c-129">Faturalama dönem kodunu ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9008c-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="9008c-130">Gelirin, faturalama için kullandığınız zaman aralığı içinde tahakkuk edilmesini istemediğiniz sürece, tahakkuk dönemini ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="9008c-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="9008c-131">Aşağıdaki tablo, hangi faturalama dönemleri için hangi tahakkuk dönemlerini ayarlayabileceğinize ilişkin genel bir fikir sağlar:</span><span class="sxs-lookup"><span data-stu-id="9008c-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9008c-132">Faturalama dönemi</span><span class="sxs-lookup"><span data-stu-id="9008c-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="9008c-133">Tahakkuk dönemi</span><span class="sxs-lookup"><span data-stu-id="9008c-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9008c-134"><strong>Yıllar</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9008c-135"><strong>Yıllar</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-136"><strong>Üç aylık dönem</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-137"><strong>Ay</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-138"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9008c-139"><strong>Üç aylık dönem</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9008c-140"><strong>Üç aylık dönem</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-141"><strong>Ay</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-142"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9008c-143"><strong>Ay</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9008c-144"><strong>Ay</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="9008c-145"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9008c-146"><strong>Hafta</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9008c-147"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9008c-148"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9008c-149"><strong>Gün</strong></span><span class="sxs-lookup"><span data-stu-id="9008c-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9008c-150">Fatura dönemini ayarlama genel abonelik grubu kurulumunun zorunlu bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="9008c-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="9008c-151">Ayrıca abonelik grubu için bir tahakkuk dönemi ayarlamak isteyip istemediğinize karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="9008c-152">Abonelik grubu için tahakkuk dönemi ayarlarsanız, bu dönem **Dönem kodu** alanında önerilir.</span><span class="sxs-lookup"><span data-stu-id="9008c-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="9008c-153">Bu alan, abonelik geliri tahakkuk ettirdiğinizde **Abonelik Geliri Tahakkuku** formunda yer alır.</span><span class="sxs-lookup"><span data-stu-id="9008c-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="9008c-154">Bununla birlikte, tahakkuk dönemi abonelik grubu hakkında isteğe bağlı bir bilgidir.</span><span class="sxs-lookup"><span data-stu-id="9008c-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9008c-155"><STRONG>Abonelik geliri tahakkuku</STRONG> formunu açmak için aşağıdaki yolu kullanın.</span><span class="sxs-lookup"><span data-stu-id="9008c-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="9008c-156"><STRONG>Hizmet yönetimi</STRONG> &gt; <STRONG>Periyodik</STRONG> &gt; <STRONG>Servis abonelikleri</STRONG> &gt; <STRONG>Abonelik geliri tahakkuku</STRONG>'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="9008c-157">Hareketler</span><span class="sxs-lookup"><span data-stu-id="9008c-157">Transactions</span></span>

<span data-ttu-id="9008c-158">Tahakkuk eden geliri deftere naklederken oluşturulan genel muhasebe hareketlerinin sayısı denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9008c-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="9008c-159">Aboneliklerde, genel muhasebe hareketlerinin toplam olarak mı yoksa satır başına olarak mı oluşturulacağını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="9008c-160">Tahakkuk eden hareketler için görüntülenecek deftere nakil ayrıntılarının düzeyini belirleme</span><span class="sxs-lookup"><span data-stu-id="9008c-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="9008c-161">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9008c-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="9008c-162">**Mali** sekmesinde, **Fatura** alanında, **Toplam** veya **Satır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9008c-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="9008c-163">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9008c-163">See also</span></span>

[<span data-ttu-id="9008c-164">Abonelik geliri tahakkuku</span><span class="sxs-lookup"><span data-stu-id="9008c-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]