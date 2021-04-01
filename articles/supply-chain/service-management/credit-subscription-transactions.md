---
title: Abonelik işlemlerini alacaklandırma
description: Bu konu, abonelik hareketlerinin nasıl kredilendirileceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4238c625930767990d28a206b10a4d71841f2ad8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247514"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="b1ddb-103">Abonelik işlemlerini alacaklandırma</span><span class="sxs-lookup"><span data-stu-id="b1ddb-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="b1ddb-104">Abonelik işlemlerini alacaklandırma</span><span class="sxs-lookup"><span data-stu-id="b1ddb-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="b1ddb-105">**Servis yönetimi** \> **Ortak** \> **Servis abonelikleri** \> **Tüm servis abonelikleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="b1ddb-106">Bir alacak dekontu oluşturmak istediğiniz abonelik işlemine iliştirilmiş aboneliği seçin.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="b1ddb-107">**Analiz** sekmesini seçin ve Eylem Bölmesinde **Ücret hareketleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="b1ddb-108">**Ücret hareketleri** formundan bir alacak dekontu oluşturmak istediğiniz hareketi seçin.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="b1ddb-109">**İşlevler** \> **Alacak dekontu için seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="b1ddb-110">**Alacak dekontu için seç** formundan, alacaklandırmak istediğiniz hareketi seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b1ddb-111">Alacak dekontunu oluşturduğunuzda, <STRONG>Alacak dekontları</STRONG>'nı seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="b1ddb-112">Bu, <STRONG>Fatura oluştur</STRONG> iletişim kutusundaki <STRONG>Faturalama yöntemi</STRONG> listesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="b1ddb-113">**Servis yönetimi parametreleri** formundaki **Alacaklandırma kapsamındaki tahakkuklara ters işlem uygula** alanı **El ile** olarak ayarlanmışsa, hareket için bir alacak dekontu teklifi oluşturmadan önce tahakkuk ettirilen her gelir hareketini tek tek ters kaydetmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1ddb-114">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b1ddb-114">See also</span></span>

[<span data-ttu-id="b1ddb-115">Fatura abonelik hareketleri</span><span class="sxs-lookup"><span data-stu-id="b1ddb-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]