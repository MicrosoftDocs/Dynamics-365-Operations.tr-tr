---
title: İlk dağıtım sırasında Commerce site oluşturucu için güvenlik grubu yapılandırılamıyor
description: Bu konu, Yeni bir e-ticaret kiracısının ilk dağıtımı sırasında, Microsoft Dynamics Lifecycle Services (LCS) içindeki e-ticaret bileşenlerini oluştururken Commerce Site Builder için Microsoft Azure Active Directory (Azure AD) güvenlik grubunun bir seçenek olarak görünmemesiyle ilgili sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801519"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="64b5e-103">İlk dağıtım sırasında Commerce site oluşturucu için güvenlik grubu yapılandırılamıyor</span><span class="sxs-lookup"><span data-stu-id="64b5e-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64b5e-104">Bu konu, Yeni bir e-ticaret kiracısının ilk dağıtımı sırasında, Microsoft Dynamics Lifecycle Services (LCS) içindeki e-ticaret bileşenlerini oluştururken Commerce Site Builder için Microsoft Azure Active Directory (Azure AD) güvenlik grubunun bir seçenek olarak görünmemesiyle ilgili sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="64b5e-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="64b5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64b5e-105">Description</span></span>

<span data-ttu-id="64b5e-106">Commerce Site Builder bileşenini içeren yeni bir e-ticaret kiracısı dağıtma işleminin parçası olarak e-ticaret bileşenleri oluşturduğunuzda, Azure AD güvenlik grubu iletişim kutusunda bir seçenek olarak görünmez.</span><span class="sxs-lookup"><span data-stu-id="64b5e-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="64b5e-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="64b5e-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="64b5e-108">E-ticaret sitesini doğru Kiracıdaki bir kullanıcıyla sağlama</span><span class="sxs-lookup"><span data-stu-id="64b5e-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="64b5e-109">[Azure portal](https://portal.azure.com/)'a gidin.</span><span class="sxs-lookup"><span data-stu-id="64b5e-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="64b5e-110">E-ticaret sitenize yönelik LCS projesinin sağlandığı kiracının altında, [Azure Active Directory kullanarak temel grup oluşturma ve üye ekleme](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) konusundaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="64b5e-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="64b5e-111">[LCS](https://lcs.dynamics.com/)'ye gidin ve oluşturduğunuz Azure AD güvenlik grubuyla aynı kiracıyı paylaşan bir hesap kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="64b5e-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="64b5e-112">Hesabın Azure AD güvenlik grubunu görüntülemek için erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="64b5e-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="64b5e-113">E-ticaret sitesini yapılandırmak için kurulum adımlarını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="64b5e-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="64b5e-114">E-ticaret bileşenlerini sağladığınızda güvenlik grubu iletişim kutusunda bir seçenek olarak görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="64b5e-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="64b5e-115">İletişim kutusundaki alanın güvenlik grupları listesiyle doldurulmasını sağlamak için, oluşturduğunuz Azure AD güvenlik grubunun adını girdikten sonra **Enter**'ı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="64b5e-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="64b5e-116">Arama sonuçları, arama metniyle başlayan ve kullanıcının erişimi olan tüm Azure AD güvenlik gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="64b5e-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="64b5e-117">Daha geniş arama sonuçlarına izin vermek için daha kısa bir arama terimi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64b5e-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64b5e-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64b5e-118">Additional resources</span></span>

[<span data-ttu-id="64b5e-119">Azure Active Directory kullanarak temel grup oluşturma ve üye ekleme</span><span class="sxs-lookup"><span data-stu-id="64b5e-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="64b5e-120">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="64b5e-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
