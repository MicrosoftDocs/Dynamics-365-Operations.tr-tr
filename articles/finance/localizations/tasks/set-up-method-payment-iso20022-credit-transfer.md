---
title: ISO20022 alacak transferi için ödeme yöntemini ayarlama
description: Bu yordam, elektronik raporlama kullanılarak bir dosya oluşturmak için ISO20022 alacak transferi için satıcı ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ae91ce361ab3e4e799ec82ca9e05c9e11d81ed1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256582"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="32901-103">ISO20022 alacak transferi için ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="32901-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32901-104">Bu yordam, elektronik raporlama kullanılarak bir dosya oluşturmak için ISO20022 alacak transferi için satıcı ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32901-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="32901-105">Bu görevi tamamlamadan önce biçim yapılandırmalarını dışa aktarmanız ve ödeme hesaplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="32901-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="32901-106">Bu görev, DEMF demo veri şirketi kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="32901-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="32901-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="32901-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="32901-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="32901-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="32901-109">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="32901-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="32901-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="32901-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="32901-111">Örneğin, Ödeme yöntemi alanına "SEPA CT" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="32901-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="32901-112">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="32901-112">Click Edit.</span></span>
4. <span data-ttu-id="32901-113">Dönem alanında "Toplam"ı seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="32901-114">Dönem türü alanında "Elektronik ödeme"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="32901-115">Dosya biçimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="32901-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="32901-116">Genel elektronik raporlama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="32901-117">Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="32901-118">Listede ISO20022 Alacak Transferi (DE) değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="32901-119">Liste boşsa, satıcı ödemesi biçim yapılandırması içe aktarılmamıştır ve etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="32901-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="32901-120">Hesap türü alanında "Banka"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="32901-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="32901-121">Ödeme hesabı alanında "DEMF OPER" değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="32901-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="32901-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="32901-122">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]