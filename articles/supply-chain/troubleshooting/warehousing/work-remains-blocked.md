---
title: Çalışma durdurulmaya devam edildi
description: Çalışma durdurulmaya devam edildi
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924142"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="a5dab-103">Çalışma durdurulmaya devam edildi</span><span class="sxs-lookup"><span data-stu-id="a5dab-103">Work remains blocked</span></span>

<span data-ttu-id="a5dab-104">Hata kodu: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="a5dab-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="a5dab-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a5dab-105">Symptoms</span></span>

<span data-ttu-id="a5dab-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="a5dab-106">The system shows the following error message:</span></span>

> <span data-ttu-id="a5dab-107">İlgili %2 dalgasının durumu %3 olduğundan, %1 işi engellenmiş olarak kaldı.</span><span class="sxs-lookup"><span data-stu-id="a5dab-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="a5dab-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="a5dab-108">Cause</span></span>

<span data-ttu-id="a5dab-109">Aşağıdaki koşullardan biri tarafından gösterildiği gibi çalışma şu anda dalgada işleniyor ve durdurulamıyor:</span><span class="sxs-lookup"><span data-stu-id="a5dab-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="a5dab-110">**Durdurma nedenleri** sekmesinde, bir veya daha fazla satır için **İş durdurma nedeni** alanı, *Dalga işleniyor* olarak ayarlı.</span><span class="sxs-lookup"><span data-stu-id="a5dab-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="a5dab-111">Eylem Bölmesi sekmesinin **İlgili bilgiler** sekmesindeki **İlgili bilgiler** grubunda **Dalga**'yı seçtiğinizde, **Dalga durumu** *İşleniyor* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a5dab-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="a5dab-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a5dab-112">Resolution</span></span>

<span data-ttu-id="a5dab-113">Eylem Bölmesinde **İlgili bilgiler** sekmesindeki **İlgili bilgiler** grubunda **Dalga**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="a5dab-114">Ardından, **Dalgalar** sayfasında, Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Dalga verisini temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="a5dab-115">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="a5dab-115">Workaround</span></span>

<span data-ttu-id="a5dab-116">Önceki adımlar sorunu gidermezse, aşağıdaki adımları izleyerek işi iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5dab-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="a5dab-117">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a5dab-118">**Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="a5dab-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-119">Select **OK**.</span></span>
1. <span data-ttu-id="a5dab-120">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a5dab-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="a5dab-121">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="a5dab-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
