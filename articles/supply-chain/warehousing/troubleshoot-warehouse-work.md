---
title: Ambar işiyle ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar işiyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970259"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="18768-103">Ambar işiyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="18768-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18768-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar işiyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="18768-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="18768-105">İzleme boyut grubunda boş çıkış ve boş girişe izin verildiğinde, seri numarası maddeleri olan plakaları taşıyamıyorum.</span><span class="sxs-lookup"><span data-stu-id="18768-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="18768-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="18768-106">Issue description</span></span>

<span data-ttu-id="18768-107">İzleme boyutu grubunda, seri numarasında *Boş çıkışa izin verilir* ve *Boş girişe izin verilir* ayarları varsa ve aynı konumda bazılarında seri numarası olan ve bazılarında olmayan birden fazla plaka varsa **Hareket** menüsü öğesini kullanarak bir plakaları taşıyamazsınız.</span><span class="sxs-lookup"><span data-stu-id="18768-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18768-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="18768-108">Issue resolution</span></span>

<span data-ttu-id="18768-109">Bu sorun [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687)'da dağıtılan değişikliklerle düzeltilecektir.</span><span class="sxs-lookup"><span data-stu-id="18768-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="18768-110">Boş girişe ve boş çıkışa izin verildiğinde, bu değişiklikler **Seri numarası** alanını isteğe bağlı yapar.</span><span class="sxs-lookup"><span data-stu-id="18768-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="18768-111">Hareketleri işlediğimde ambar uygulamasında aşağıdaki hata iletisini alıyorum: "Bu işlemde %1 adlı stok sahibine izin verilmiyor."</span><span class="sxs-lookup"><span data-stu-id="18768-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="18768-112">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="18768-112">Issue description</span></span>

<span data-ttu-id="18768-113">Ambar uygulaması, hareketleri oluşturmak için kullanıldığında **Sahip** izleme boyutu eksiktir.</span><span class="sxs-lookup"><span data-stu-id="18768-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="18768-114">Supply Chain Management istemcisinden alınan düzenli bir stok transferi günlüğü, istendiği gibi çalışır ve yalnızca **Sahip** boyutu doldurulmuşsa deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="18768-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="18768-115">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="18768-115">Issue resolution</span></span>

<span data-ttu-id="18768-116">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="18768-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="18768-117">Şu anda, ambar yönetimi işlemleri yalnızca tüzel kişiliklerin sahip olduğu stokları destekler.</span><span class="sxs-lookup"><span data-stu-id="18768-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
