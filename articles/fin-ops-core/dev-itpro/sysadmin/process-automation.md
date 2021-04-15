---
title: İşlem otomasyonu
description: Bu konu, işlem otomasyonunun toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya nasıl izin verdiğini açıklamaktadır.
author: RyanCCarlson2
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 509decec3c3d3b598a2457cddba4896730480ec6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745937"
---
# <a name="process-automation"></a><span data-ttu-id="3c798-103">İşlem otomasyonu</span><span class="sxs-lookup"><span data-stu-id="3c798-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3c798-104">İşlem otomasyonu, toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya izin verir.</span><span class="sxs-lookup"><span data-stu-id="3c798-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="3c798-105">Zamanlanan işin güncelleştirilmiş takvim görünümü, son kullanıcıların zamanlanmış ve tamamlanmış işleri görüntülemesine ve üzerlerinde işlem yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c798-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="3c798-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="3c798-106">Administration</span></span>

<span data-ttu-id="3c798-107">Tüm işlem otomasyonlarının merkezi yönetim sayfası, **Kurulum** menüsünün altında Sistem Yönetimi modülünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="3c798-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="3c798-108">Bu sayfa, sistemde ayarlanan tüm otomatik işlemleri (serileri) listeler.</span><span class="sxs-lookup"><span data-stu-id="3c798-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="3c798-109">Bu sayfa, ayrıca, doğrudan bu sayfadan yeni işlem otomasyonları eklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c798-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="3c798-110">Bir seri ayarladıktan sonra, bu listeden her bir seriyi yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c798-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="3c798-111">Tüm seriyi düzenlemeyi, silmeyi veya tüm oluşumları liste görünümünde görüntülemeyi ya da zamanlanan işi bir süre duraklatmak istiyorsanız seriyi devre dışı bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c798-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="3c798-112">Özellik yönetiminde devre dışı bırakılan tüm işlemler, özellik devre dışı bırakıldığında gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="3c798-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="3c798-113">Ek olarak, süreç otomasyonu zamanlama altyapısı devre dışı bırakılan bir özellik için herhangi bir oluşum veya arka plan işlemi zamanlamaz.</span><span class="sxs-lookup"><span data-stu-id="3c798-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="3c798-114">Özelliğin yeniden etkinleştirilmesi, geçmişte zamanlanmış oluşumların veya arka plan işlemlerinin hemen çalışmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="3c798-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="3c798-115">Takvim görünümü</span><span class="sxs-lookup"><span data-stu-id="3c798-115">Calendar view</span></span>

<span data-ttu-id="3c798-116">İşlem otomasyonunun önemli yararlarından biri, zamanlanmış işi basit bir takvim görünümünde görme yeteneğidir.</span><span class="sxs-lookup"><span data-stu-id="3c798-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="3c798-117">Bu görünüm bir seferde bir haftalık çalışmayı görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c798-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="3c798-118">Bu görünümü **Süreç otomasyonu** sayfasının sağ tarafında görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="3c798-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="3c798-119">Görünüm, seçili seriler için zamanlanan işle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="3c798-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="3c798-120">[![İşlem otomasyonu takvimi](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="3c798-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="3c798-121">Oluşum değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="3c798-121">Occurrence changes</span></span>

<span data-ttu-id="3c798-122">Her oluşum, kendilerinden çıkan serilerin tanımladığı diğer oluşumları etkilemeden değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3c798-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="3c798-123">Zamanlanan işin oluşumları takvim görünümünden **Görüntüle/Düzenle** düğmesi ve **Oluşum** seçilerek düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="3c798-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="3c798-124">Bu sayfa, ilk başta seri kurulum sihirbazında gösterilen tüm ayarlara erişmenizi sağlar ve seçili oluşumda tek başına bir değişiklik yapma yeteneğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c798-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="3c798-125">Zamanlanan işin bir oluşumu, takvim görünümünden **Devre dışı bırak** düğmesi seçilerek de kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="3c798-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="3c798-126">Geliştirici belgesi</span><span class="sxs-lookup"><span data-stu-id="3c798-126">Developer documentation</span></span>

<span data-ttu-id="3c798-127">Süreç otomasyonu altyapısı geliştiricilerin süreç otomasyonu altyapısını genişletmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c798-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="3c798-128">[Süreç otomasyonu altyapısı](../process-automation/process-automation-framework.md) belgeleri, işlem otomasyonu sihirbazıyla zamanlanmış toplu iş sunucusu tarafından çalıştırılmasını ve takvim görünümünde otomatik olarak gösterilmesini istediğiniz özel işlemleri nasıl oluşturacağınız hakkında bilgiler sağlayacak.</span><span class="sxs-lookup"><span data-stu-id="3c798-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]