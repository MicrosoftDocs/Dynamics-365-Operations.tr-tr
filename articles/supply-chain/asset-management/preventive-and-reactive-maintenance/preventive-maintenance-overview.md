---
title: Önleyici bakıma genel bakış
description: Bu konuda Varlık Yönetimi'nde önleyici bakım açıklanmaktadır.
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
ms.openlocfilehash: 3b43c795426f40cb43962976824c44a7702d91b7
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875934"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="08501-103">Önleyici bakıma genel bakış</span><span class="sxs-lookup"><span data-stu-id="08501-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="08501-104">Bu konuda Varlık Yönetimi'nde önleyici bakım açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="08501-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="08501-105">Önleyici bakım, düzenli hizmet, kalibrasyon ve incelemeler gibi planlı bakım işlerinin dahil olduğu bir disiplindir.</span><span class="sxs-lookup"><span data-stu-id="08501-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="08501-106">**Varlık Yönetimi**'nde, bakım planları oluşturabilir ve bunları varlıklarda ve işlem yapılacak yerleşimlerde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08501-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="08501-107">İşlem yapılacak yerleşimlerde bakım sıralarını da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08501-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="08501-108">Varlıklardaki bakım planları varlığın yüklü olduğu yerden bağımsız olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="08501-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="08501-109">İşlem yapılacak yerleşimdeki bakım planları ve bakım sıraları yerleşimde şu anda yüklü olan varlıklar için etkindir.</span><span class="sxs-lookup"><span data-stu-id="08501-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="08501-110">Varlıklarda bakım planları ayarlamak veya işlem yapılacak yerleşimlerde bakım sıraları ayarlamak yerine aynı iş rutininde ilgili bakım işi türlerini gerçekleştirmek istediğiniz birden çok varlığı içeren bakım sıraları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="08501-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="08501-111">İşlem yapılacak yerleşimlerde oluşturulmak yerine varlıklardan oluşturulan bakım sıraları, aynı işlem yapılacak yerleşime yüklenmeyen bir bakım sırası için varlık sayısını seçebileceğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="08501-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="08501-112">Bakım planları tek bir varlıkta önleyici ve reaktif bakım için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08501-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="08501-113">Bakım sıraları, bir varlık grubu veya kümesinde önleyici bakım için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08501-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="08501-114">Bakım planları ve bakım sıraları, iş emri teklifleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08501-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="08501-115">İş emri teklifleri, paketlenebilen ve iş emirlerine dönüştürülebilen bakım zamanlaması satırları olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="08501-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="08501-116">Aşağıdaki şekilde, bakım planları ve bakım sıralarını temel alarak bakım planları ve bakım sıraları oluşturmaktan varlıklar için iş emirleri oluşturmaya kadar iş akışına bir genel bakış sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="08501-116">The figure below provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![Şekil 1](media/01-preventive-maintenance.png)

