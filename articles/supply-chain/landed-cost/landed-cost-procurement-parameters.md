---
title: Varış yeri maliyeti için satın alma ve tedarik parametreleri
description: Bu konuda, Varış yeri maliyeti modülünü kullandığınızda ilgili Satın alma ve tedarik parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020995"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="b3c49-103">Varış yeri maliyeti için satın alma ve tedarik parametreleri</span><span class="sxs-lookup"><span data-stu-id="b3c49-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3c49-104">**Satın alma ve tedarik parametreleri** sayfasında, özellikle **Varış yeri maliyeti** modülünü kullandığınızda ilgili olan birkaç ayar vardır.</span><span class="sxs-lookup"><span data-stu-id="b3c49-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="b3c49-105">Satın alma siparişi başlığında değişiklik yapıldığında satın alma siparişi satırlarının otomatik olarak güncelleştirilip güncelleştirilmeyeceğini belirtmek için **Satın alma ve tedarik parametreleri** sayfasından açılan **Sipariş satırlarını güncelleştir** iletişim kutusunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3c49-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="b3c49-106">Bu kurulumu tamamlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b3c49-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="b3c49-107">**Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="b3c49-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="b3c49-108">**Genel** sekmesinde **Sipariş satırlarını güncelleştir** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="b3c49-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="b3c49-109">**Sipariş satırlarını güncelleştir** iletişim kutusu, sipariş başlığında, sipariş satırlarındaki ilgili alanlara otomatik güncelleştirmeler de uygulayabilen alanları listeler.</span><span class="sxs-lookup"><span data-stu-id="b3c49-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="b3c49-110">Listedeki her alanı aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b3c49-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="b3c49-111">**Her zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları otomatik olarak güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b3c49-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b3c49-112">**Hiçbir zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları hiçbir zaman güncelleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="b3c49-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b3c49-113">**İstem**: Kullanıcıdan sipariş satırlarının güncelleştirilip güncelleştirilmeyeceğini seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="b3c49-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
