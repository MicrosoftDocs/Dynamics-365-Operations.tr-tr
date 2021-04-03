---
title: Şirket başına Kazanç yönetimi parametrelerini yapılandırma
description: Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimiyle ilgili şirket başıan parametreleri yapılandırın.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 31f30c3d268132327074e931b714b5b2ee3ec5ac
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466652"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="31bd4-103">Şirket başına Kazanç yönetimi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="31bd4-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31bd4-104">Yararlar sunan her organizasyon için, kazançlar onayı e-postaları ayarlarını konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="31bd4-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="31bd4-105">E-posta ayarlarını yapılandırma onayı</span><span class="sxs-lookup"><span data-stu-id="31bd4-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="31bd4-106">**Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="31bd4-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="31bd4-107">**Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="31bd4-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="31bd4-108">Alan</span><span class="sxs-lookup"><span data-stu-id="31bd4-108">Field</span></span> | <span data-ttu-id="31bd4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="31bd4-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="31bd4-110">**Onay e-postası gönder**</span><span class="sxs-lookup"><span data-stu-id="31bd4-110">**Send confirmation email**</span></span> | <span data-ttu-id="31bd4-111">Bu özellik açık olduğunda, çalışan self servis 'deki sosyal haklar kayıt deneyiminden çıktığında çalışanlara bir onay e-postası gönderilir.</span><span class="sxs-lookup"><span data-stu-id="31bd4-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="31bd4-112">**Onay e-postası şablonu**</span><span class="sxs-lookup"><span data-stu-id="31bd4-112">**Confirmation email template**</span></span> | <span data-ttu-id="31bd4-113">Kayıt onayını gönderirken kullanılacak organizasyon e-posta şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="31bd4-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="31bd4-114">Şablon seçmezseniz, aşağıdaki genel e-posta gönderilir:</span><span class="sxs-lookup"><span data-stu-id="31bd4-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="31bd4-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="31bd4-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="31bd4-116">Tebrikler!</span><span class="sxs-lookup"><span data-stu-id="31bd4-116">Congratulations!</span></span> <span data-ttu-id="31bd4-117">Sosyal haklar kaydını başarıyla tamamladınız.</span><span class="sxs-lookup"><span data-stu-id="31bd4-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="31bd4-118">Teşekkür ederiz,</span><span class="sxs-lookup"><span data-stu-id="31bd4-118">Thank you,</span></span><br><span data-ttu-id="31bd4-119"><Company/Org name> Kazançlar.</span><span class="sxs-lookup"><span data-stu-id="31bd4-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="31bd4-120">**Gönderenin varsayılan e-posta adresi**</span><span class="sxs-lookup"><span data-stu-id="31bd4-120">**Default email sender address**</span></span> | <span data-ttu-id="31bd4-121">Onay e-postası gönderilirken kullanılacak e-posta adresi.</span><span class="sxs-lookup"><span data-stu-id="31bd4-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="31bd4-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="31bd4-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]