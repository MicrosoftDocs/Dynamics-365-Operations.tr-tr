---
title: Dalga, temizlik için uygun değil
description: Dalga, temizlik için uygun değil
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924339"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="ff7f1-103">Dalga, temizlik için uygun değil</span><span class="sxs-lookup"><span data-stu-id="ff7f1-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="ff7f1-104">Hata kodu: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="ff7f1-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff7f1-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="ff7f1-105">Symptoms</span></span>

<span data-ttu-id="ff7f1-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="ff7f1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ff7f1-107">%1 dalgası temizleme işlemi için uygun değil.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="ff7f1-108">Dalga verileri temizlenemiyor.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="ff7f1-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="ff7f1-109">Cause</span></span>

<span data-ttu-id="ff7f1-110">Aşağıdaki koşullardan biri tarafından gösterildiği gibi dalga şu anda işlenmektedir:</span><span class="sxs-lookup"><span data-stu-id="ff7f1-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="ff7f1-111">**Dalga durumu** alanının ayarı *Yürütülüyor* olarak ayarlanmış.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="ff7f1-112">Eylem bölmesinin **Dalga** sekmesindeki **Dalga** grubunda **Toplu iş**'i seçtiğinizde, **Durum** alanı *Sonlandırıldı*, *Hata* veya *İptal edildi* olarak ayarlanmaz.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="ff7f1-113">Bu nedenle, bir toplu iş şu anda çalışıyor.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff7f1-114">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="ff7f1-114">Resolution</span></span>

<span data-ttu-id="ff7f1-115">Eylem bölmesinde, **Dalga** sekmesinde, **Dalga** grubunda, **Toplu iş**'i seçin ve aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="ff7f1-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="ff7f1-116">**Durum** alanı *Yürütülüyor* olarak ayarlanmışsa: Eylem bölmesinde, **Toplu iş** sekmesinde, **Toplu iş** grubunda, **Görevleri görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="ff7f1-117">İlerlemeyi **Toplu iş görevleri** sayfasını yenileyerek izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="ff7f1-118">**Durum** alanı *Yürütülüyor* olarak ayarlanmamışsa: Eylem bölmesinde, **Toplu iş** sekmesinde, **İşlevler** grubunda, **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="ff7f1-119">**Yeni durum seç** alanında, *Bekliyor*'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="ff7f1-120">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ff7f1-120">Then select **OK**.</span></span>
