---
title: Malzeme çekme modülü için giriş yapma
description: Bu konu malzeme çekme modülü için giriş yapmayı ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270595"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="b2d69-103">Malzeme çekme modülü için giriş yapma</span><span class="sxs-lookup"><span data-stu-id="b2d69-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2d69-104">Bu konu malzeme çekme modülü için giriş yapmayı ele almaktadır ve bu modülün Microsoft Dynamics 365 Commerce'ta nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b2d69-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b2d69-105">Malzeme çekme modülü için giriş yapma, Dynamics 365 Commerce müşteri giriş özelliğini kullanan müşterilerin geldiğini mağazaya bildirmek için bir onay sayfası sağlar.</span><span class="sxs-lookup"><span data-stu-id="b2d69-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="b2d69-106">Malzeme çekme modülü için giriş yapma aynı zamanda teslimatı kolaylaştırmak amacıyla müşterilerden ek bilgiler toplayan bir form yapılandırmanıza da olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b2d69-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="b2d69-107">Bu bilgilere müşterinin park yeri numarası ve müşterinin aracının marka ve modeli dahildir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="b2d69-108">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="b2d69-108">Module properties</span></span>

| <span data-ttu-id="b2d69-109">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="b2d69-109">Property name</span></span> | <span data-ttu-id="b2d69-110">Değerler</span><span class="sxs-lookup"><span data-stu-id="b2d69-110">Values</span></span> | <span data-ttu-id="b2d69-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2d69-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b2d69-112">Onay metni</span><span class="sxs-lookup"><span data-stu-id="b2d69-112">Confirmation text</span></span> | <span data-ttu-id="b2d69-113">Metin dizesi</span><span class="sxs-lookup"><span data-stu-id="b2d69-113">Text string</span></span> | <span data-ttu-id="b2d69-114">Giriş onayı sayfasında görünen başlığın içeriği.</span><span class="sxs-lookup"><span data-stu-id="b2d69-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="b2d69-115">QR kodunu göster</span><span class="sxs-lookup"><span data-stu-id="b2d69-115">Show QR code</span></span> | <span data-ttu-id="b2d69-116">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b2d69-116">**True** or **False**</span></span> | <span data-ttu-id="b2d69-117">Bu özellik, **Doğru** olarak ayarlandığında, giriş onayı sayfası sipariş onay kodunu temsil eden bir QR kodu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="b2d69-118">Ek bilgi başlığı</span><span class="sxs-lookup"><span data-stu-id="b2d69-118">Additional information heading</span></span> | <span data-ttu-id="b2d69-119">Metin dizesi</span><span class="sxs-lookup"><span data-stu-id="b2d69-119">Text string</span></span> | <span data-ttu-id="b2d69-120">Ek bilgi alanları yapılandırıldığında görüntülenen başlık içeriği.</span><span class="sxs-lookup"><span data-stu-id="b2d69-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="b2d69-121">Ek bilgi anahtarları</span><span class="sxs-lookup"><span data-stu-id="b2d69-121">Additional information keys</span></span> | <span data-ttu-id="b2d69-122">Kaynak kodu/kaynak değer çifti</span><span class="sxs-lookup"><span data-stu-id="b2d69-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="b2d69-123">Her bir anahtar, müşterilerden ek bilgi toplamak için kullanılan bir form alanı ve ilişkili bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b2d69-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="b2d69-124">Ek bilgi anahtarları \> Kaynak kodu</span><span class="sxs-lookup"><span data-stu-id="b2d69-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="b2d69-125">Metin dizesi</span><span class="sxs-lookup"><span data-stu-id="b2d69-125">Text string</span></span> | <span data-ttu-id="b2d69-126">Her bir bilgi, müşterilerden ek bilgi toplamak için kullanılan bir form alanı ve ilişkili bir etiket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b2d69-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="b2d69-127">Bu özellik, ek bilgi anahtarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b2d69-127">This property identifies the additional information key.</span></span> <span data-ttu-id="b2d69-128">Satış noktasında (POS) oluşturulan görevde, bu özelliğin değeri, talimatlar alanında etiket olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="b2d69-129">Ek bilgi anahtarları \> Kaynak değeri</span><span class="sxs-lookup"><span data-stu-id="b2d69-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="b2d69-130">Metin dizesi</span><span class="sxs-lookup"><span data-stu-id="b2d69-130">Text string</span></span> | <span data-ttu-id="b2d69-131">POS'taki görevde yer alan metin alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="b2d69-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="b2d69-132">Ek bilgi anahtarları \> Zorunlu</span><span class="sxs-lookup"><span data-stu-id="b2d69-132">Additional information keys \> Required</span></span> | <span data-ttu-id="b2d69-133">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="b2d69-133">**True** or **False**</span></span> | <span data-ttu-id="b2d69-134">Bu özellik, müşterilerin devam edebilmek için form alanını doldurmaları gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="b2d69-135">Bu özellik **Doğru** olarak ayarlandığında, form etiketinin yanında bir yıldız görüntülenir ve herhangi bir değer girilmediğinde müşterilerin devam etmesini önlemek için null denetimi yapılır.</span><span class="sxs-lookup"><span data-stu-id="b2d69-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="b2d69-136">Bir sayfaya malzeme çekme modülü için giriş yapmayı ekleme</span><span class="sxs-lookup"><span data-stu-id="b2d69-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="b2d69-137">Giriş onayı için oluşturduğunuz yeni sayfaya, malzeme çekme modülü için giriş yapma eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="b2d69-138">Bu sayfa, e-postadaki **Buradayım** bağlantısını veya düğmesini seçen müşteriler için giriş onayı deneyimi görevini üstlenecek.</span><span class="sxs-lookup"><span data-stu-id="b2d69-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="b2d69-139">Ek bilgiler formunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b2d69-139">Configure the additional information form</span></span>

<span data-ttu-id="b2d69-140">Ek bilgi anahtarları yapılandırılmamışsa modül, müşteriye varsayılan olarak giriş onayı sayfasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="b2d69-141">Giriş onayı gösterildiğinde, POS'ta siparişin çekildiği mağaza için bir görev oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b2d69-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="b2d69-142">Bir veya daha fazla ek bilgi anahtarı yapılandırıldığında önce müşterilerden bilgi girmeleri istenir.</span><span class="sxs-lookup"><span data-stu-id="b2d69-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="b2d69-143">**Gönder**'i seçtiklerinde, giriş onayı görüntülenir ve POS'ta bir görev oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b2d69-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b2d69-144">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b2d69-144">Additional resources</span></span>

[<span data-ttu-id="b2d69-145">Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b2d69-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
