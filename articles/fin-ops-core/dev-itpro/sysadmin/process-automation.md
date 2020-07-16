---
title: İşlem otomasyonu
description: Bu konu, işlem otomasyonunun toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya nasıl izin verdiğini açıklamaktadır.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508197"
---
# <a name="process-automation"></a><span data-ttu-id="8807c-103">İşlem otomasyonu</span><span class="sxs-lookup"><span data-stu-id="8807c-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8807c-104">İşlem otomasyonu, toplu iş sunucusuyla çalıştırılacak işlemlere ilişkin basit zamanlamaya izin verir.</span><span class="sxs-lookup"><span data-stu-id="8807c-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="8807c-105">Zamanlanan işin güncelleştirilmiş takvim görünümü, son kullanıcıların zamanlanmış ve tamamlanmış işleri görüntülemesine ve üzerlerinde işlem yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8807c-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="8807c-106">Yönetim</span><span class="sxs-lookup"><span data-stu-id="8807c-106">Administration</span></span>

<span data-ttu-id="8807c-107">Tüm işlem otomasyonlarının merkezi yönetim sayfası, **Kurulum** menüsünün altında Sistem Yönetimi modülünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="8807c-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="8807c-108">Bu sayfa, sistemde ayarlanan tüm otomatik işlemleri (serileri) listeler.</span><span class="sxs-lookup"><span data-stu-id="8807c-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="8807c-109">Bu sayfa, ayrıca, doğrudan bu sayfadan yeni işlem otomasyonları eklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8807c-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="8807c-110">Bir seri ayarladıktan sonra, bu listeden her bir seriyi yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8807c-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="8807c-111">Tüm seriyi düzenlemeyi, silmeyi veya tüm oluşumları liste görünümünde görüntülemeyi ya da zamanlanan işi bir süre duraklatmak istiyorsanız seriyi devre dışı bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8807c-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="8807c-112">Takvim görünümü</span><span class="sxs-lookup"><span data-stu-id="8807c-112">Calendar view</span></span> 
<span data-ttu-id="8807c-113">İşlem otomasyonunun önemli yararlarından biri, zamanlanmış işi basit bir takvim görünümünde görme yeteneğidir.</span><span class="sxs-lookup"><span data-stu-id="8807c-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="8807c-114">Bu görünüm bir seferde bir haftalık çalışmayı görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8807c-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="8807c-115">Bu görünümü **İşlem otomasyonu** sayfasının sağ tarafında görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="8807c-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="8807c-116">Görünüm, seçili seriler için zamanlanan işle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="8807c-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="8807c-117">[![İşlem otomasyonu takvimi](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="8807c-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="8807c-118">Oluşum değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="8807c-118">Occurrence changes</span></span>
<span data-ttu-id="8807c-119">Her oluşum, kendilerinden çıkan serilerin tanımladığı diğer oluşumları etkilemeden değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8807c-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="8807c-120">Zamanlanan işin oluşumları takvim görünümünden **Görüntüle/Düzenle** düğmesi ve **Oluşum** seçilerek düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="8807c-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="8807c-121">Bu, ilk başta seri kurulum sihirbazında gösterilen tüm ayarlara erişmenizi sağlar ve seçili oluşumda tek başına bir değişiklik yapma yeteneğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="8807c-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="8807c-122">Zamanlanan işin bir oluşumu, takvim görünümünden **Devre dışı bırak** düğmesi seçilerek de kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="8807c-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="8807c-123">Geliştirici belgesi</span><span class="sxs-lookup"><span data-stu-id="8807c-123">Developer documentation</span></span> 
<span data-ttu-id="8807c-124">Geliştiricilerin işlem otomasyonu çerçevesini genişletmesine olanak tanımak için şu anda geliştirici belgeleri yazılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8807c-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="8807c-125">Bu belgeler, işlem otomasyonu sihirbazıyla zamanlanmış toplu iş sunucusu tarafından çalıştırılmasını ve takvim görünümünde otomatik olarak gösterilmesini istediğiniz özel işlemleri nasıl oluşturacağınız hakkında bilgiler sağlayacak.</span><span class="sxs-lookup"><span data-stu-id="8807c-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
