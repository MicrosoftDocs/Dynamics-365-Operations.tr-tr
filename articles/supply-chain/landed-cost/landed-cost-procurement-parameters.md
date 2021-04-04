---
title: Varış yeri maliyeti için satın alma ve tedarik parametreleri
description: Bu konuda, Varış yeri maliyeti modülünü kullandığınızda ilgili Satın alma ve tedarik parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500754"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="350c6-103">Varış yeri maliyeti için satın alma ve tedarik parametreleri</span><span class="sxs-lookup"><span data-stu-id="350c6-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="350c6-104">**Satın alma ve tedarik parametreleri** sayfasında, özellikle **Varış yeri maliyeti** modülünü kullandığınızda ilgili olan birkaç ayar vardır.</span><span class="sxs-lookup"><span data-stu-id="350c6-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="350c6-105">Satın alma siparişi başlığında değişiklik yapıldığında satın alma siparişi satırlarının otomatik olarak güncelleştirilip güncelleştirilmeyeceğini belirtmek için **Satın alma ve tedarik parametreleri** sayfasından açılan **Sipariş satırlarını güncelleştir** iletişim kutusunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="350c6-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="350c6-106">Bu kurulumu tamamlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="350c6-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="350c6-107">**Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="350c6-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="350c6-108">**Genel** sekmesinde **Sipariş satırlarını güncelleştir** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="350c6-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="350c6-109">**Sipariş satırlarını güncelleştir** iletişim kutusu, sipariş başlığında, sipariş satırlarındaki ilgili alanlara otomatik güncelleştirmeler de uygulayabilen alanları listeler.</span><span class="sxs-lookup"><span data-stu-id="350c6-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="350c6-110">Listedeki her alanı aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="350c6-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="350c6-111">**Her zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları otomatik olarak güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="350c6-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="350c6-112">**Hiçbir zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları hiçbir zaman güncelleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="350c6-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="350c6-113">**İstem**: Kullanıcıdan sipariş satırlarının güncelleştirilip güncelleştirilmeyeceğini seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="350c6-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
