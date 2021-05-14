---
title: İş, durdurulduğu için iptal edilemiyor
description: İş, durdurulduğu için iptal edilemiyor
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924291"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="1d505-103">İş, durdurulduğu için iptal edilemiyor</span><span class="sxs-lookup"><span data-stu-id="1d505-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="1d505-104">Hata kodu: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="1d505-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="1d505-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="1d505-105">Symptoms</span></span>

<span data-ttu-id="1d505-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="1d505-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1d505-107">%1 işi, neden türü %2 tarafından engellendiğinden iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="1d505-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="1d505-108">İşin iptal edilebilmesi için öncelikle durdurmanın kaldırılması gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="1d505-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="1d505-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="1d505-109">Cause</span></span>

<span data-ttu-id="1d505-110">İş durdurulmuş ve iptal edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="1d505-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="1d505-111">**Çalışma** sayfasında, **Genel** sekmesinde, **Durdurulmuş** seçeneği *Evet* olarak ayarlı.</span><span class="sxs-lookup"><span data-stu-id="1d505-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="1d505-112">Bu ayar, çalışmanın durdurulduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d505-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="1d505-113">**Durdurma nedenleri** sekmesi, çalışmanın neden durdurulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d505-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="1d505-114">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="1d505-114">Resolution</span></span>

<span data-ttu-id="1d505-115">Çalışmanın durdurmasını kaldırmak için, **Durdurma nedenleri** sekmesini seçin ve aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="1d505-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="1d505-116">**Çalışma durdurma nedeni** alanı *Tanımsız neden* olarak ayarlanmışsa: Eylem Bölmesinde, **Çalışma** sekmesinde, **Çalışma** grubunda, **Çalışma engelini kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d505-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="1d505-117">**Çalışma durdurma nedeni** alanı, *Dalga işleniyor* olarak ayarlanmışsa : Eylem Bölmesinde, **İlgili bilgiler** sekmesinde, **İlgili bilgiler** grubunda **Dalga** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d505-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="1d505-118">Ardından, **Dalgalar** sayfasında, Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Dalga verisini temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d505-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="1d505-119">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="1d505-119">Workaround</span></span>

<span data-ttu-id="1d505-120">Önceki adımlar sorunu gidermezse, aşağıdaki adımları izleyerek işi iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d505-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="1d505-121">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1d505-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="1d505-122">**Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d505-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="1d505-123">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d505-123">Select **OK**.</span></span>
1. <span data-ttu-id="1d505-124">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1d505-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="1d505-125">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="1d505-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
