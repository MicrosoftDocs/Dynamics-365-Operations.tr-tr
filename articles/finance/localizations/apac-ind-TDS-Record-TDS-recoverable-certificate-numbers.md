---
title: TDS düşürülebilir sertifikası numaralarını kaydetme
description: Bu konu; belirli bir satıcı, müşteri veya genel muhasebe için alınan Kaynakta Kesilen Vergi (TDS) sertifikaları için sertifika numaraları ve tarihlerini kaydetmek için Düşürülebilir sertifikalar sayfasının nasıl kullanılacağını anlatır.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023644"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="f84e0-103">TDS düşürülebilir sertifikası numaralarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="f84e0-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f84e0-104">Bu konu; belirli bir satıcı, müşteri veya genel muhasebe için alınan Kaynakta Kesilen Vergi (TDS) sertifikaları için sertifika numaraları ve tarihlerini kaydetmek için **Düşürülebilir sertifikalar** sayfasının nasıl kullanılacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="f84e0-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="f84e0-105">TDS hareketleri için kaydedilen TDS sertifika numaralarını ve tarihlerini güncelleştirmek için bu sayfada **Sertifikayı güncelleştir** sayfasını (**Genel muhasebe \> Dönemsel \> Stopaj vergisi \>Güncelleştirme sertifikası**) kullanın.</span><span class="sxs-lookup"><span data-stu-id="f84e0-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="f84e0-106">TDS sertifika numaralarını güncelleştirmeyi bitirdikten sonra, bunları kapatın.</span><span class="sxs-lookup"><span data-stu-id="f84e0-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="f84e0-107">TDS sertifika numaralarını ve tarihlerini kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="f84e0-108">**Vergi \> Dolaylı vergi \> Stopaj vergisi \> Düşürülebilir sertifikaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="f84e0-109">[![Düşürülebilir sertifikaları sayfası](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="f84e0-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="f84e0-110">**Düşürülebilir sertifikaları** sayfasında, **Vergi türü** alanında **TDS** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="f84e0-111">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="f84e0-112">**Sertifika numarası** alanında, TDS sertifika numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="f84e0-113">**Hesap türü** alanında, TDS sertifikasının alındığı hesabın türünü seçin: **Satıcı**, **Müşteri** veya **Genel muhasebe**.</span><span class="sxs-lookup"><span data-stu-id="f84e0-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="f84e0-114">**Hesap** alanında, seçtiğiniz hesap türüne bağlı olarak satıcı, müşteri veya genel muhasebe hesap numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="f84e0-115">**Ad** alanı; satıcı, müşteri veya genel muhasebe hesabının adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f84e0-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="f84e0-116">**Sertifika tutarı** alanına TDS sertifikasının tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="f84e0-117">**Tarih** alanında, sertifika numarası için sertifika tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="f84e0-118">TDS sertifika numarası ve tarihinin güncelleştirildiği TDS hareketlerini görüntüleyebileceğiniz **Sertifika hareketleri** sayfasını açmak için **Sorgular**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="f84e0-119">Bu bilgiler, **Sertifikayı güncelleştir** sayfasında (**Vergi \> Beyannameler \> Stopaj vergisi \>Sertifikayı güncelleştir**) güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f84e0-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="f84e0-120">**Sertifikayı güncelleştir** sayfası, her TDS hareketiyle ilgili olarak aşağıdaki bilgileri gösterir:</span><span class="sxs-lookup"><span data-stu-id="f84e0-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="f84e0-121">**Tarih** - TDS hareketinin deftere nakil tarihi.</span><span class="sxs-lookup"><span data-stu-id="f84e0-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="f84e0-122">**Fiş** – TDS hareketinin fiş numarasını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="f84e0-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="f84e0-123">**Kaynak** – TDS hareketinin içinde oluşturulduğu modül.</span><span class="sxs-lookup"><span data-stu-id="f84e0-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="f84e0-124">**Hesap** – TDS hareketinin adına oluşturulduğu satıcı, müşteri veya genel muhasebe hesabı numarası.</span><span class="sxs-lookup"><span data-stu-id="f84e0-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="f84e0-125">**Ad** – TDS hareketinin adına oluşturulduğu satıcı, müşteri veya genel muhasebe hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="f84e0-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="f84e0-126">**Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.</span><span class="sxs-lookup"><span data-stu-id="f84e0-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="f84e0-127">**Vergi tutarı** – Hareket için hesaplanan TDS vergi tutarı.</span><span class="sxs-lookup"><span data-stu-id="f84e0-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="f84e0-128">**Sertifika tarihi** – TDS hareketi için güncelleştirilen TDS sertifika tarihi.</span><span class="sxs-lookup"><span data-stu-id="f84e0-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="f84e0-129">**Sertifika numarası** – TDS hareketi için güncelleştirilen TDS sertifika numarası.</span><span class="sxs-lookup"><span data-stu-id="f84e0-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="f84e0-130">**Düşürülebilir sertifikaları** sayfasında, **Sertifikayı güncelleştir** sayfasında TDS hareketlerinin güncelleştirmesini bitirdikten sonra TDS sertifika numarasını kapatmak için **Kapalı** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="f84e0-131">Sayfadaki tüm kayıtlar için **Kapalı** onay kutusunu seçmek için **Tümünü işaretle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f84e0-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f84e0-132">**Kapalı** onay kutusunun seçili olduğu TDS sertifika numaraları, **Sertifikayı güncelleştir** sayfasında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="f84e0-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
