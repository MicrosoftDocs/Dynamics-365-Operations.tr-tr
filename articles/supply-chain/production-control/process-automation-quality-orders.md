---
title: Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın
description: Bu konu, kalite emirleri örneğini kullanarak iş süreçlerini otomatikleştirmek için Power Automate kullanmak için kaynaklar sağlar.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115225"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="7da4b-103">Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın</span><span class="sxs-lookup"><span data-stu-id="7da4b-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7da4b-104">Kuruluşlar, standart iş süreçlerini otomatikleştirmek, personele daha uygun etkileşimler sağlamak ve iş süreçlerini otomatik olarak yönlendirmek için çeşitli veri sinyallerini ve sistemlerini kullanmak için artan bir talebe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7da4b-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="7da4b-105">Robotik süreç otomasyonu (RPA) ve Microsoft Power Automate, işletmeler tekrarlayan süreçleri otomatikleştirmek için kodsuz bir deneyim kullanabilir, böylece verimlilik ve doğruluk kazanabilirler.</span><span class="sxs-lookup"><span data-stu-id="7da4b-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="7da4b-106">Supply Chain Management için indirilebilir otomasyon çözümü şablonu, örnek olarak kalite emirlerini kullanarak iş süreçlerini otomatikleştirmek için Power Automate'in nasıl kullanılabileceğini sunar.</span><span class="sxs-lookup"><span data-stu-id="7da4b-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="7da4b-107">Otomasyon çözüm şablonsunu [buradan](https://aka.ms/D365SCMQualityOrderRPASolution) indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da4b-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="7da4b-108">Bu özelliğe ve özelliklerine genel bir bakış için aşağıdaki videoya bakın: [Dynamics 365 Supply Chain Management'ta kalite emirleri oluşturmak için RPA kullanma](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="7da4b-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="7da4b-109">![RPA ile otomasyon seçenekleri](media/rpa-automation-options.png "RPA ile otomasyon seçenekleri")</span><span class="sxs-lookup"><span data-stu-id="7da4b-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="7da4b-110">Power Automate çözüm şablonu, Supply Chain Management'ta kalite emirlerinin oluşturulmasını otomatikleştiren bir bulut otomasyon akışı ve bir masaüstü otomasyon akışı içerir.</span><span class="sxs-lookup"><span data-stu-id="7da4b-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="7da4b-111">Otomasyon, kullanıcı girişi veya makine sinyalleri (Nesnelerin İnterneti (IoT dahil)) dahil olmak üzere birçok olay ve sinyale yanıt olarak başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="7da4b-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="7da4b-112">*Q-Order* Power Application örneği çözüm şablonuna dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="7da4b-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="7da4b-113">Kullanıcının bir madde QR kodunu taramasına, miktar girmesine ve kamera kullanarak resim eklemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da4b-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="7da4b-114">Çözüm parametreleri, otomasyonu bir üretim tesisindeki belirli bir kullanım örneği için yapılandırmak üzere dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="7da4b-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="7da4b-115">![Kalite emri oluştur](media/rpa-create-quality-roder.png "Kalite emri oluştur")</span><span class="sxs-lookup"><span data-stu-id="7da4b-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="7da4b-116">Kalite emri oluşturmayı otomatikleştirmek için örnek çözümü indirme, yükleme ve kullanma hakkında eksiksiz bir adım adım kılavuz için, bkz. [Power Automate Desktop kullanarak robotik süreç otomasyonu ile Dynamics 365 Supply Chain Management'ta kalite emri oluşturmayı otomatikleştirme](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="7da4b-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

