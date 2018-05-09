---
title: "Kayıt şablonları"
description: "Bu makale, kayıt şablonları kavramını tanıtır ve bunların bilgi paylaşan kayıtları oluşturmada nasıl kullanılabileceklerini açıklar."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2f2c7f302a01593e7327dfe0510fadb3886bddd7
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="record-templates"></a><span data-ttu-id="1bb72-103">Kayıt şablonları</span><span class="sxs-lookup"><span data-stu-id="1bb72-103">Record templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bb72-104">Bu makale, kayıt şablonları kavramını tanıtır ve bunların bilgi paylaşan kayıtları oluşturmada nasıl kullanılabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1bb72-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="1bb72-105">Kayıt şablonları, Microsoft Dynamics 365 for Finance and Operations'da kayıtları daha hızlı oluşturmanıza yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1bb72-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1bb72-106">Microsoft Dynamics 365 for Finance and Operations'da yalnızca bazı kayıt türleri için kayıt şablonları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb72-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="1bb72-107">Örneğin, San Francisco içinde bulunan bir araba kiralama işletme için kiralama bilgilerini girdiğiniz düşünün.</span><span class="sxs-lookup"><span data-stu-id="1bb72-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="1bb72-108">Müşterilerin çoğu San Francisco alanından büyük olasılıkla olduğundan, **durum**, **Ülke**, ve **Şehir** alanları kiralık formdaki değerleri otomatik olarak doldurabilseniz iyi olurdu.</span><span class="sxs-lookup"><span data-stu-id="1bb72-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="1bb72-109">Yalnızca erişiminiz olan Finance and Operations alanları için şablonları uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb72-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="1bb72-110">Ancak, tüm şablon başlıkları yeni bir kayıt oluşturduğunuzda size görünür olur - ayrıca, tüm kullanıcıların kullanımına açık şablonlar oluşturuyorsanız diğer kullanıcılara da.</span><span class="sxs-lookup"><span data-stu-id="1bb72-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="1bb72-111">Şablonları adlandırırken bunu dikkate almayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1bb72-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="1bb72-112">Örneğin, tüm kullanıcıların şirketteki bazı çalışanların prim bazlı maaş aldığı gizliyse adlarda "prim" gibi sözcükleri kullanmaktan kaçının.</span><span class="sxs-lookup"><span data-stu-id="1bb72-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="1bb72-113">Erişiminiz olan bir veya daha şablonun belirli bir form için olması ve formda yeni bir kayıt oluşturmak istediğinizde **Bir şablon seç** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1bb72-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="1bb72-114">Listeden bir şablon seçtiğinizde, yeni kayıt oluşturulur ve seçtiğiniz şablona dayalı varsayılan bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="1bb72-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="1bb72-115">Yeni kayıtlar oluştururken şablonları kullanmak istemiyorsanız, **Şablon seç** sayfasında **Tekrar sorma** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1bb72-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="1bb72-116">Şablon seçimi iletişim kutusunu yeniden görüntülemek için, herhangi bir kayıt üzerine sağ tıklayın **Kayıt bilgileri**'ne tıklayın ve ardından **Şablon seçimini göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1bb72-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




