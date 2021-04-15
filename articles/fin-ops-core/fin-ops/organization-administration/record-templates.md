---
title: Kayıt şablonlarına genel bakış
description: Bu makale, kayıt şablonları kavramını tanıtır ve bunların bilgi paylaşan kayıtları oluşturmada nasıl kullanılabileceklerini açıklar.
author: pvillads
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d802d8bb86313dba512f52ec977b4dd18aa25c61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747549"
---
# <a name="record-templates-overview"></a><span data-ttu-id="30b5c-103">Kayıt şablonlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="30b5c-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30b5c-104">Bu makale, kayıt şablonları kavramını tanıtır ve bunların bilgi paylaşan kayıtları oluşturmada nasıl kullanılabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="30b5c-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="30b5c-105">Kayıt şablonları kayıtları daha çabuk oluşturmanıza yardımcı olabilir ancak bazı kayıt türleri için yalnızca kayıt şablonları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30b5c-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="30b5c-106">Örneğin, San Francisco içinde bulunan bir araba kiralama işletme için kiralama bilgilerini girdiğiniz düşünün.</span><span class="sxs-lookup"><span data-stu-id="30b5c-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="30b5c-107">Müşterilerin çoğu San Francisco alanından büyük olasılıkla olduğundan, **durum**, **Ülke**, ve **Şehir** alanları kiralık formdaki değerleri otomatik olarak doldurabilseniz iyi olurdu.</span><span class="sxs-lookup"><span data-stu-id="30b5c-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="30b5c-108">Şablonları yalnızca erişiminiz olan alanlarda uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30b5c-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="30b5c-109">Ancak, tüm şablon başlıkları yeni bir kayıt oluşturduğunuzda size görünür olur - ayrıca, tüm kullanıcıların kullanımına açık şablonlar oluşturuyorsanız diğer kullanıcılara da.</span><span class="sxs-lookup"><span data-stu-id="30b5c-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="30b5c-110">Şablonları adlandırırken bunu dikkate almayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="30b5c-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="30b5c-111">Örneğin, tüm kullanıcıların şirketteki bazı çalışanların prim bazlı maaş aldığı gizliyse adlarda "prim" gibi sözcükleri kullanmaktan kaçının.</span><span class="sxs-lookup"><span data-stu-id="30b5c-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="30b5c-112">Erişiminiz olan bir veya daha şablonun belirli bir form için olması ve formda yeni bir kayıt oluşturmak istediğinizde **Bir şablon seç** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="30b5c-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="30b5c-113">Listeden bir şablon seçtiğinizde, yeni kayıt oluşturulur ve seçtiğiniz şablona dayalı varsayılan bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="30b5c-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="30b5c-114">Yeni kayıtlar oluştururken şablonları kullanmak istemiyorsanız, **Şablon seç** sayfasında **Tekrar sorma** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="30b5c-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="30b5c-115">Şablon seçimi iletişim kutusunu yeniden görüntülemek için, herhangi bir kayıt üzerine sağ tıklayın **Kayıt bilgileri**'ne tıklayın ve ardından **Şablon seçimini göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="30b5c-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]