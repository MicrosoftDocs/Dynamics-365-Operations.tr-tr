---
title: İşlem otomasyonu
description: Bu konu, işlem otomasyonunun toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya nasıl izin verdiğini açıklamaktadır.
author: RyanCCarlson2
ms.date: 04/20/2021
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
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920841"
---
# <a name="process-automation"></a><span data-ttu-id="6ec88-103">İşlem otomasyonu</span><span class="sxs-lookup"><span data-stu-id="6ec88-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6ec88-104">İşlem otomasyonu, toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya izin verir.</span><span class="sxs-lookup"><span data-stu-id="6ec88-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="6ec88-105">Zamanlanan işin güncelleştirilmiş takvim görünümü, son kullanıcıların zamanlanmış ve tamamlanmış işleri görüntülemesine ve üzerlerinde işlem yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6ec88-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="6ec88-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="6ec88-106">Administration</span></span>

<span data-ttu-id="6ec88-107">Tüm işlem otomasyonlarının merkezi yönetim sayfası, **Kurulum** menüsünün altında Sistem Yönetimi modülünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="6ec88-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="6ec88-108">Bu sayfa, sistemde ayarlanan tüm otomatik işlemleri (serileri) listeler.</span><span class="sxs-lookup"><span data-stu-id="6ec88-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="6ec88-109">Bu sayfa, ayrıca, doğrudan bu sayfadan yeni işlem otomasyonları eklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6ec88-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="6ec88-110">Bir seri ayarladıktan sonra, bu listeden her bir seriyi yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ec88-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="6ec88-111">Tüm seriyi düzenlemeyi, silmeyi veya tüm oluşumları liste görünümünde görüntülemeyi ya da zamanlanan işi bir süre duraklatmak istiyorsanız seriyi devre dışı bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ec88-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="6ec88-112">Özellik yönetiminde devre dışı bırakılan tüm işlemler, özellik devre dışı bırakıldığında gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="6ec88-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="6ec88-113">Ek olarak, süreç otomasyonu zamanlama altyapısı devre dışı bırakılan bir özellik için herhangi bir oluşum veya arka plan işlemi zamanlamaz.</span><span class="sxs-lookup"><span data-stu-id="6ec88-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="6ec88-114">Özelliğin yeniden etkinleştirilmesi, geçmişte zamanlanmış oluşumların veya arka plan işlemlerinin hemen çalışmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="6ec88-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="6ec88-115">İşlem otomasyonu planlama altyapısı,**İşlem otomasyonu yoklama sistem işi** sistem toplu işinin çalışmasına dayanır.</span><span class="sxs-lookup"><span data-stu-id="6ec88-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="6ec88-116">İş, herhangi bir anda değiştirilmemelidir veya üzerinde değişiklik yapılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ec88-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="6ec88-117">Takvim görünümü</span><span class="sxs-lookup"><span data-stu-id="6ec88-117">Calendar view</span></span>

<span data-ttu-id="6ec88-118">İşlem otomasyonunun önemli yararlarından biri, zamanlanmış işi basit bir takvim görünümünde görme yeteneğidir.</span><span class="sxs-lookup"><span data-stu-id="6ec88-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="6ec88-119">Bu görünüm bir seferde bir haftalık çalışmayı görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6ec88-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="6ec88-120">Bu görünümü **Süreç otomasyonu** sayfasının sağ tarafında görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="6ec88-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="6ec88-121">Görünüm, seçili seriler için zamanlanan işle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="6ec88-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="6ec88-122">[![İşlem otomasyonu takvimi](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="6ec88-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="6ec88-123">Oluşum değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="6ec88-123">Occurrence changes</span></span>

<span data-ttu-id="6ec88-124">Her oluşum, kendilerinden çıkan serilerin tanımladığı diğer oluşumları etkilemeden değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6ec88-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="6ec88-125">Zamanlanan işin oluşumları takvim görünümünden **Görüntüle/Düzenle** düğmesi ve **Oluşum** seçilerek düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="6ec88-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="6ec88-126">Bu sayfa, ilk başta seri kurulum sihirbazında gösterilen tüm ayarlara erişmenizi sağlar ve seçili oluşumda tek başına bir değişiklik yapma yeteneğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6ec88-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="6ec88-127">Zamanlanan işin bir oluşumu, takvim görünümünden **Devre dışı bırak** düğmesi seçilerek de kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ec88-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="6ec88-128">Geliştirici belgesi</span><span class="sxs-lookup"><span data-stu-id="6ec88-128">Developer documentation</span></span>

<span data-ttu-id="6ec88-129">Süreç otomasyonu altyapısı geliştiricilerin süreç otomasyonu altyapısını genişletmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6ec88-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="6ec88-130">[Süreç otomasyonu altyapısı](../process-automation/process-automation-framework.md) belgeleri, işlem otomasyonu sihirbazıyla zamanlanmış toplu iş sunucusu tarafından çalıştırılmasını ve takvim görünümünde otomatik olarak gösterilmesini istediğiniz özel işlemleri nasıl oluşturacağınız hakkında bilgiler sağlayacak.</span><span class="sxs-lookup"><span data-stu-id="6ec88-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
