---
title: Bakım zamanlaması maliyeti
description: Bu konuda Varlık Yönetimi'nde bakım zamanlaması maliyeti açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71b958839a914d90a86a0dcd16a09285ca6dcfa4
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875935"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="42d08-103">Bakım zamanlaması maliyeti</span><span class="sxs-lookup"><span data-stu-id="42d08-103">Maintenance schedule cost</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="42d08-104">Varlık Yönetiminde, bakım zamanlaması satırlarında bütçe maliyetlerini hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42d08-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="42d08-105">Bu, örneğin bir sonraki yıla ait planlı önleyici bakım işleriyle ilgili maliyetler gibi beklenen maliyetlere genel bakış almak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="42d08-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="42d08-106">Hesaplamalar, "Bakım planları","Bakım sırası" ve "Bakım talepleri" türünde mevcut bakım zamanlaması satırlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="42d08-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="42d08-107">**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Bakım zamanlaması maliyeti**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42d08-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="42d08-108">**Bakım zamanlaması maliyeti** iletişim kutusunda, mali boyutlarda gruplanmış maliyetleri görmek isterseniz bir **Mali boyut kümesi** seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42d08-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="42d08-109">Mali boyut kümeleri, **Genel muhasebe** > **Hesap planı** > **Boyutlar** > **Mali boyut kümeleri**'nde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="42d08-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="42d08-110">İşlem yapılacak yerleşimlerle ilgili olarak bakım zamanlaması satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42d08-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="42d08-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="42d08-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="42d08-112">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım zamanlaması satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="42d08-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="42d08-113">Belirli varlıklar için hesaplama yapmak isterseniz **Eklenecek kayıtlar** hızlı sekmesinde **Filtre**'ye tıklayın ve ilgili varlıkları seçin.</span><span class="sxs-lookup"><span data-stu-id="42d08-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="42d08-114">Gerekirse, maliyet hesaplaması için **Beklenen başlangıç** tarihini belirtebilir veya farklı bir **Durum** seçebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42d08-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="42d08-115">Maliyet hesaplamasını başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42d08-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="42d08-116">**Bakım zamanlaması maliyeti** sekmesinde > **Gruplama ölçütü...** eylem bölmesi gruplarında, maliyet hesaplamasının gereken ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42d08-116">On the **Maintenance schedule cost** tab > in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="42d08-117">Seçilen eylem bölmesi grubu düğmeleri mavi renkte vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="42d08-117">The selected action pane group buttons are highlighted in blue color.</span></span> <span data-ttu-id="42d08-118">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42d08-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="42d08-119">Yeni bir maliyet hesaplaması yapmak isterseniz **Maliyeti hesapla** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42d08-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>


![Şekil 1](media/17-preventive-maintenance.png)

