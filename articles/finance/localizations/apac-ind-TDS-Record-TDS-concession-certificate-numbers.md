---
title: TDS imtiyaz sertifikası numaralarını kaydetme
description: Bu konu, satıcılara verilen Kaynakta Kesilen Vergi (TDS) imtiyaz sertifikası numaralarının nasıl kaydedileceğini açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023646"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="40930-103">TDS imtiyaz sertifikası numaralarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="40930-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40930-104">Bu konu, satıcılara verilen Kaynakta Kesilen Vergi (TDS) imtiyaz sertifikası numaralarının nasıl kaydedileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="40930-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="40930-105">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi imtiyazları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="40930-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="40930-106">**Vergi türü** alanında, TDS vergi türü için imtiyaz sertifikalarını kaydetmek üzere **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="40930-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="40930-107">Bir satır oluşturmak için, **Genel bakış** sekmesinde **Alt+N**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="40930-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="40930-108">[![Yeni satırın başlığı](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="40930-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="40930-109">**Stopaj vergisi kodu** alanında, satıcı imtiyaz sertifikalarının verildiği TDS vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="40930-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="40930-110">**Stopaj vergisi kodu adı** alanı, TDS vergi kodunun adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40930-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="40930-111">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, imtiyazlı temele göre satıcı için TDS'yi hesaplamak üzere TDS vergi kodunu kullanan imtiyaz sertifikasının geçerlilik süresini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="40930-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="40930-112">**Açıklamalar** alanına açıklamaları girin.</span><span class="sxs-lookup"><span data-stu-id="40930-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="40930-113">**Bölüm** alanında, TDS imtiyaz sertifikasının altında bulunduğu yasal bölüm kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="40930-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="40930-114">Bölüm kodu 197 ise, "A" değeri Form 26Q'daki "Kesinti olmaması/düşük kesinti nedeni" sütununda ve Form 27Q'da "Kesinti olmaması/düşük kesinti/brütleştirme (varsa) nedeni" sütununda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="40930-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="40930-115">Bölüm kodu 197A ise, bu iki sütunda da "B" değeri görünür.</span><span class="sxs-lookup"><span data-stu-id="40930-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="40930-116">Satıcılara ait TDS imtiyaz sertifikası numaralarını kaydetmek için **Sertifika** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="40930-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="40930-117">**Satıcı hesabı** alanında, TDS imtiyaz sertifikasının verildiği satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="40930-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="40930-118">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, TDS imtiyaz sertifikasının geçerlilik dönemini belirtin.</span><span class="sxs-lookup"><span data-stu-id="40930-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="40930-119">TDS'nin imtiyazlı temele göre hesaplanması, satıcı için sertifikanın oluşturulduğu döneme dayanır.</span><span class="sxs-lookup"><span data-stu-id="40930-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="40930-120">**Sertifika** alanında, TDS imtiyaz sertifika numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="40930-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="40930-121">[![Sertifika hızlı sekmesi](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="40930-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="40930-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="40930-122">Close the page.</span></span>
