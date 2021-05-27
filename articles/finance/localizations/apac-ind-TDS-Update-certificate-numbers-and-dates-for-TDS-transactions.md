---
title: TDS hareketleri için sertifika numaraları ve tarihlerini güncelleştirme
description: Bu konu; Kaynakta Kesilen Vergide (TDS) bir satıcı, müşteri ve genel muhasebe hesapları için kaydedilen düşürülebilir sertifika numaralarını güncelleştirmeyi açıklar.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023654"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="176b0-103">TDS hareketleri için sertifika numaraları ve tarihlerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="176b0-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="176b0-104">Bu konu; Kaynakta Kesilen Vergide (TDS) bir satıcı, müşteri ve genel muhasebe hesapları için kaydedilen düşürülebilir sertifika numaralarını güncelleştirmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="176b0-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="176b0-105">TDS hareketleriyle ilgili sertifikaları **Düşürülebilir sertifikaları** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="176b0-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="176b0-106">**Sertifikaları Güncelleştir** sayfasını kullanarak sertifikaları güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="176b0-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="176b0-107">TDS hareketleri için sertifika numaralarını ve tarihlerini güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="176b0-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="176b0-108">**Vergi \> Beyanlar \> Stopaj vergisi \> Sertifikayı güncelleştir**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="176b0-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="176b0-109">[![Sertifikayı güncelleştir sayfası](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="176b0-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="176b0-110">**Sertifikayı güncelleştir** sayfasında, **Seçim** bölümünde, **Vergi türü** alanında, **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="176b0-111">**Sertifika numarası** alanında, müşterinin veya satıcının TDS sertifika numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="176b0-112">**Sertifika numarası** alanı, yalnızca **Düşürülebilir sertifikaları** sayfasında **Kapalı** onay kutusunun seçili olmadığı TDS sertifika numaralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="176b0-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="176b0-113">**Sertifika tarihi** alanı, sertifika tarihini gösterir.</span><span class="sxs-lookup"><span data-stu-id="176b0-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="176b0-114">**Hesap türü** alanı, TDS sertifika numarasının hangi hesap türü için alındığını gösterirken **Ad** alanında hesabın adı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="176b0-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="176b0-115">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, TDS hareketlerini görüntülemek için dönemin başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="176b0-116">Seçili dönemde deftere nakledilen TDS hareketlerini görüntülemek için **Verileri göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="176b0-117">**Genel bakış** sekmesinde, üst bölmedeki ızgara, seçilen dönemde satıcı veya müşteri için deftere nakledilen her TDS hareketiyle ilgili aşağıdaki bilgileri gösterir:</span><span class="sxs-lookup"><span data-stu-id="176b0-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="176b0-118">**Fiş** – TDS hareketinin fiş numarasını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="176b0-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="176b0-119">**Tarih** - TDS hareketinin tarihi.</span><span class="sxs-lookup"><span data-stu-id="176b0-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="176b0-120">**Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.</span><span class="sxs-lookup"><span data-stu-id="176b0-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="176b0-121">**Vergi tutarı** – Hareket için hesaplanan TDS vergi tutarı.</span><span class="sxs-lookup"><span data-stu-id="176b0-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="176b0-122">Belirli TDS hareketlerini üst ızgaradan aşağı ızgaraya taşımak için, hareketleri seçin ve **Dahil et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="176b0-123">Alternatif olarak, Tüm TDS hareketlerini üst ızgaradan aşağı ızgaraya taşımak için **Tümünü dahil et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="176b0-124">Belirli TDS hareketlerini veya tüm TDS hareketlerini alt ızgaradan üst ızgaraya taşımak için, **Hariç tut** veya **Tümünü hariç tut** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="176b0-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="176b0-125">TDS hareketleri için alt ızgaradaki **Sertifika numarası** ve **Sertifika tarihi** alanlarını güncelleştirmek için **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="176b0-126">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Düşürülebilir sertifikası**'na gidin ve **Sertifika hareketleri** sayfasında yeni sertifika numaralarına sahip güncelleştirilmiş hareket satırlarını görüntülemek için **Sorgulama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="176b0-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="176b0-127">[![Sertifika hareketleri sayfası](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="176b0-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
