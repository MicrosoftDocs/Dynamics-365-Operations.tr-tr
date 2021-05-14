---
title: Kalite yönetimi test gereçleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle testlerin kullanılabilmesi için, test araçlarının nasıl oluşturulacağını açıklar.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956865"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="cc230-103">Kalite yönetimi test gereçleri</span><span class="sxs-lookup"><span data-stu-id="cc230-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc230-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle testlerin kullanılabilmesi için, test araçlarının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="cc230-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cc230-105">**Test araçları** sayfasını, kalite emirleriyle ilgili testleri gerçekleştirmek için kullanılan cihazlar hakkında ayrıntılı bilgi tanımlamak ve görüntülemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc230-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="cc230-106">Test araçları isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cc230-106">Test instruments are optional.</span></span> <span data-ttu-id="cc230-107">Ancak, bu araçlar çalışanların belirli bir testi gerçekleştirmek için hangi cihaz veya aracı kullanmaları gerektiğini bilmelerini sağlamaya yardımcı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="cc230-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="cc230-108">Test aracı örneği</span><span class="sxs-lookup"><span data-stu-id="cc230-108">Test instrument example</span></span>

<span data-ttu-id="cc230-109">Elektrik bileşenleri üzerinde çeşitli testler gerçekleştiriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="cc230-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="cc230-110">Bazı testler, bileşenlerin voltaj çıkışı, bir test sıcaklıkları ve bir test de ağırlıkları içindir.</span><span class="sxs-lookup"><span data-stu-id="cc230-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="cc230-111">Her bir testi gerçekleştirmek için farklı araçlar, cihazlar veya ekipman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc230-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="cc230-112">Örneğin, voltaj ölçmek için bir voltaj ölçer kullanılır, sıcaklığı ölçmek için bir termometre kullanılır ve ağırlığı ölçmek için bir tartı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc230-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="cc230-113">Bu cihazların her birini bir test aracı olarak yapılandırabilir ve test sonuçlarının kaydedilmesi için gereken ölçü birimini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc230-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="cc230-114">Örneğin, voltaj ölçerden gelen sonuçlar volt olarak kaydedilir, termometreden gelen sonuçlar Fahrenhayt veya Santigrat derece olarak kaydedilir ve tartının sonuçları libre veya kilogram olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="cc230-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="cc230-115">Yeni bir test aracı oluşturma</span><span class="sxs-lookup"><span data-stu-id="cc230-115">Create a test instrument</span></span>

1. <span data-ttu-id="cc230-116">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Test araçları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="cc230-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="cc230-117">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc230-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cc230-118">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="cc230-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cc230-119">**Test aracı** – Test aracı için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="cc230-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="cc230-120">**Açıklama** – Test aracının detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="cc230-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="cc230-121">**Birim** – Aracın sonuçları ölçeceği birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc230-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="cc230-122">**Duyarlık** alanı, seçtiğiniz birime göre otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="cc230-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="cc230-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cc230-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc230-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cc230-124">Additional resources</span></span>

- [<span data-ttu-id="cc230-125">Kalite yönetimi testi</span><span class="sxs-lookup"><span data-stu-id="cc230-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="cc230-126">Kalite yönetimi test grupları</span><span class="sxs-lookup"><span data-stu-id="cc230-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
