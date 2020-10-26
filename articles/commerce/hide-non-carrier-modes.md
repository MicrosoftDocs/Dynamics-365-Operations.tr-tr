---
title: Taşıyıcı dışı teslimat modlarını POS'taki sevkiyat seçeneklerinden gizleme
description: Bu konu, satış noktasında (POS) sevkiyat emirleri oluşturulurken, taşıyıcı dışı teslimat modlarının seçim için görüntülenmesini engelleyebilecek bir yapılandırma seçeneği açıklamaktadır.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 38d57ed5f8d2b8725cd11156f0135988bb76e047
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983001"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="10dcc-103">Taşıyıcı dışı teslimat modlarını POS'taki sevkiyat seçeneklerinden gizleme</span><span class="sxs-lookup"><span data-stu-id="10dcc-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="10dcc-104">Bu konuda, satış noktası (POS) uygulaması için kullanılabilen bir yapılandırma seçeneği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="10dcc-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="10dcc-105">Bu yapılandırma seçeneği, POS'ta sevkiyat emirleri oluşturulduğunda, teslim modunun seçimine ilişkin davranışı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="10dcc-106">Kullanıcılar POS 'ta müşteri sevkiyat emirleri oluştururken, sevkiyat için bir teslimat modu seçebilir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="10dcc-107">Bu işlev, siparişin tamamının mı yoka yalnızca seçili satırların mı sevk edileceğinden bağımsız olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="10dcc-108">Varsayılan olarak, bir teslimat modunun seçildiği iletişim kutusu bir kanal, madde ve teslimat adresi birleşimi için geçerli teslimat modlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="10dcc-109">Bu teslimat şekilleri Headquarters'taki **Teslimat şekli** sayfasında (**Satış ve pazarlama \> Kurulum \> Dağıtım \> Teslimat şekli**) tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="10dcc-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="10dcc-110">**Teslim alınan** veya **Çekme** gibi "taşıyıcı dışı" teslimat şekilleri de iletişim kutusunda seçim için görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="10dcc-111">Ancak, iletişim kutusunda taşıyıcı dışı teslimat şekillerini gizlemenize olanak sağlayan bir özellik eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="10dcc-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="10dcc-112">Bu özelliği açmak için, **Commerce parametreleri** sayfasında **Müşteri siparişleri** sekmesinde **Sevk emirleri için yalnızca taşıyıcı modu seçeneklerini göster** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="10dcc-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="10dcc-113">Bu özelliği açtıktan ve bilgileri kanal veritabanıyla eşitlemek için uygun dağıtım işlerini çalıştırdıktan sonra, POS'ta sevkiyat emri oluşturma işlemi sırasında, taşıyıcı dışı teslimat şekilleri seçim için görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="10dcc-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>
