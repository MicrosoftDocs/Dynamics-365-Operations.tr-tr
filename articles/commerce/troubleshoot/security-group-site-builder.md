---
title: İlk dağıtım sırasında Commerce site oluşturucu için güvenlik grubu yapılandırılamıyor
description: Bu makale, Yeni bir e-ticaret kiracısının ilk dağıtımı sırasında, Microsoft Dynamics Lifecycle Services (LCS) içindeki e-ticaret bileşenlerini oluştururken Commerce Site Builder için Microsoft Azure Active Directory (Azure AD) güvenlik grubunun bir seçenek olarak görünmemesiyle ilgili sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 797df828df16547eb3aef1f9865a663281fb9224
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899027"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>İlk dağıtım sırasında Commerce site oluşturucu için güvenlik grubu yapılandırılamıyor

[!include [banner](../../includes/banner.md)]

Bu makale, Yeni bir e-ticaret kiracısının ilk dağıtımı sırasında, Microsoft Dynamics Lifecycle Services (LCS) içindeki e-ticaret bileşenlerini oluştururken Commerce Site Builder için Microsoft Azure Active Directory (Azure AD) güvenlik grubunun bir seçenek olarak görünmemesiyle ilgili sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Commerce Site Builder bileşenini içeren yeni bir e-ticaret kiracısı dağıtma işleminin parçası olarak e-ticaret bileşenleri oluşturduğunuzda, Azure AD güvenlik grubu iletişim kutusunda bir seçenek olarak görünmez.

## <a name="resolution"></a>Çözünürlük

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>E-ticaret sitesini doğru Kiracıdaki bir kullanıcıyla sağlama

1. [Azure portal](https://portal.azure.com/)'a gidin.
1. E-ticaret sitenize yönelik LCS projesinin sağlandığı kiracının altında, [Azure Active Directory kullanarak temel grup oluşturma ve üye ekleme](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) konusundaki yönergeleri izleyin.
1. [LCS](https://lcs.dynamics.com/)'ye gidin ve oluşturduğunuz Azure AD güvenlik grubuyla aynı kiracıyı paylaşan bir hesap kullanarak oturum açın. Hesabın Azure AD güvenlik grubunu görüntülemek için erişimi olmalıdır.
1. E-ticaret sitesini yapılandırmak için kurulum adımlarını tamamlayın. E-ticaret bileşenlerini sağladığınızda güvenlik grubu iletişim kutusunda bir seçenek olarak görünmelidir.

> [!NOTE]
> İletişim kutusundaki alanın güvenlik grupları listesiyle doldurulmasını sağlamak için, oluşturduğunuz Azure AD güvenlik grubunun adını girdikten sonra **Enter**'ı seçmelisiniz. Arama sonuçları, arama metniyle başlayan ve kullanıcının erişimi olan tüm Azure AD güvenlik gruplarını listeler. Daha geniş arama sonuçlarına izin vermek için daha kısa bir arama terimi kullanabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Azure Active Directory kullanarak temel grup oluşturma ve üye ekleme](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Yeni bir e-ticaret kiracısını dağıtma](../deploy-ecommerce-site.md)