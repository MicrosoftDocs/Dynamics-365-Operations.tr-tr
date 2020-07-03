---
title: Satıcı ödemesi tutma koşulları oluşturma ve uygulama
description: Bu konu, satıcı ödemeleri için bekletme koşullarının nasıl ayarlanacağı ve bakımını yapılacağı hakkında bilgi sağlar.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410277"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Satıcı ödemesi tutma koşulları oluşturma ve uygulama

[!include [banner](../includes/banner.md)] 

Bir proje için satıcı ödeme bekletme koşullarının kurulması, organizasyonunuz bir satıcıya yapılan ödemelerin bir bölümünü korumak istediğinde faydalıdır. Örneğin, ürünler teslim edilene kadar satıcıya ödeme tutmak istediğinizde. Satıcı ödeme Bekletme koşulları, bir satıcı sözleşmesi üzerinde anlaşdığınızda belirtilebilir.

## <a name="create-vendor-payment-retention-terms"></a>Satıcı ödemesi tutma koşulları oluşturma

Bekletmeyle ilgili satıcı ödemesi yüzdesini ve serbest bırakılacak daha önceden tutulan tutarların yüzdesini girebilirsiniz. Sözleşme belirtilen tamamlanma durumuna ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur. Bekletme koşullarını ayarladıktan sonra, bunları o satıcının herhangi bir projesine uygulayabilirsiniz.

Satıcı ödemeleriyle ilgili bekletme koşullarını ayarlamak ve sürdürmek için aşağıdaki adımları kullanın. 

1. **Proje yönetimi ve muhasebe** > **bekletme** > **satıcı ödeme Bekletme koşulları**'na gidin.
2. Yeni bir satıcı bekletme koşulu eklemek için **yeni**'yi seçin. Yeni terimin **kural kodu** değeri otomatik olarak girilir. 
3. **Açıklama** alanına kısa bir açıklama girin ve **şartlar** hızlı sekmesinde, aşağıdakiler için terim değerleri girmek üzere **satır ekle**'yi seçin:

   - **Teslim edilen birim yüzdesi** : Terimin tamamlanma yüzdesini girin. Proje tamamlanma durumu, belirtilen yüzdeye eşit oluncaya kadar tutarlar satıcı faturalarında otomatik olarak korunur. Örneğin, 50.00 girerseniz, projenin yüzde 50'si tamamlanana kadar tutarlar korunur.
   - **Tutulacak yüzde**: korunacak satıcı faturası tutarının yüzdesini girin. Örneğin, 10,00 girerseniz, bir satıcı faturasındaki tutarın yüzde 10'u, proje **teslim edilen birim yüzdesi** alanında ayarlandığı gibi tamamlanma yüzdesine ulaşıncaya kadar tutulur.
   - **Serbest bırakma yüzdesi** : Seçilen proje düzeyi için serbest bırakılacak daha önceden tutulan tutarların yüzdesini girmek için **satır ekle**'yi seçin.

> [!NOTE]
> Proje tamamlamada farklı düzeylerde birden fazla kilometre taşına sahipseniz, her bir bekletme kuralı için ayrı bir satıcı bekletme terimi satırı girin. Her satır, proje tamamlamada atanan her düzey için farklı bir bekletme yüzdesi ve farklı bir sürüm yüzdesi belirtebilir.

Bir satıcı için satıcı tutma şartları oluşturduktan sonra, bunları şartları bir projesine uygulayabilirsiniz.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Satıcıya bekletme koşullarını projeye Uygula

1. **Proje yönetimi ve hesap** > **Projeler** > **Tüm projeler**'e gidin ve proje listesi sayfasından bir proje açın.
2. **Satıcı sözleşmeleri** hızlı sekmesinde **Satır ekle**'yi seçin.
3. **Hesap kodu** alanında aşağıdaki seçeneklerden birini belirleyin: 

   - **Tablo** – Satıcı tutma koşulları tek bir satıcıya uygulanır.
   - **Grup** – Satıcı tutma koşulları bir satıcı grubundaki tüm satıcılar için geçerlidir.
   - **Tümü** – Satıcı tutma koşulları tüm satıcılara uygulanır.

4. **Satıcı/satıcı grubu alanında**, satıcı bekletme koşullarının uygulanacağı satıcıyı veya satıcı grubunu seçin. Önceki adımda **tümü** seçeneğini belirlediyseniz , bu alan kullanılamaz.
5. **Satıcı tutma şartları** alanında, önceki yordamda oluşturduğunuz tutma şartlarını seçin.
6. Proje için satıcı için ayarlanmış ödeme ödemesi (PWP) koşulları varsa, bir projenin eşik yüzdesini **PWP eşik yüzdesi** alanına girin.

Satıcı Bekletme koşulları Ayrıca satıcı için oluşturduğunuz satınalma siparişlerinde de görüntülenir.
