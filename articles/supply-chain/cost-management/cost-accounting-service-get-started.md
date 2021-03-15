---
title: Maliyet muhasebesi hizmetini (özel önizleme) kullanmaya başlama
description: Bu konu, maliyet muhasebesi hizmeti için lisans ayrıntılarını ve yükleme yönergelerini sağlar.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011859"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Maliyet muhasebesi hizmetini (özel önizleme) kullanmaya başlama

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Bu konuda belirtilen işlev özel bir önizleme sürümünün bir parçası olarak sunulur. Bu konunun içeriği ve tanımladığı işlevsellik değişebilir. Önizleme sürümleri hakkında daha fazla bilgi için bkz. [Bir sürüm hizmeti güncelleştirmeleriyle ilgili SSS](../../fin-ops-core/fin-ops/get-started/one-version.md).

Maliyet muhasebesi hizmeti, ayarlamış olduğunuz maliyet muhasebesi defterlerinde çoklu stok hesapları yapmanıza olanak tanır. Her bir maliyet muhasebesi defterini bir *kural* ile ilişkilendirirsiniz. Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:

- Maliyet nesnesi
- Giriş ölçümü esası
- Maliyet akışı varsayımı
- Maliyet öğesi

> [!NOTE]
> Maliyet muhasebesi hizmetini açsanız bile, Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi de yapabilirsiniz.

Maliyet muhasebesi hizmeti bir eklentidir. Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir. Bu nedenle, üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.

Maliyet muhasebesi hizmeti şu anda Dynamics 365 Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir. Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Maliyet muhasebesi hizmetini (özel önizleme) alma

> [!IMPORTANT]
> Maliyet muhasebesi hizmetini kullanmak için, LCS'nin etkin olduğu yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) ve Dynamics 365 Supply Chain Management sürüm 10.0.11 veya üstünü çalıştırıyor olmanız gerekir.

Maliyet muhasebesi hizmet özel önizlemesine kaydolmak için lütfen LCS ortam kimliğinizi [Maliyet muhasebesi hizmetine (özel önizleme)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29) e-posta ile gönderin. Program için onay aldığınızda, maliyet muhasebesi hizmeti beta anahtarını içeren bir takip e-postası alacaksınız. Beta anahtarını aldığınızda, [eklentiyi yükleyerek](#install) devam edebilirsiniz.

## <a name="licensing"></a>Lisans

Maliyet muhasebesi hizmeti Supply Chain Management için kullanılabilir olan stok muhasebesi standart özellikleri ile birlikte lisanslanır. Maliyet muhasebesi hizmetini kullanmak için ek lisans satın almanız gerekmez.

## <a name="install-the-add-in"></a><a name="install"></a>Eklentiyi yükleme

Maliyet muhasebesi hizmetini kullanmak için, aşağıdaki yordamda açıklandığı şekilde Supply Chain Management için maliyet muhasebesi hizmeti eklentisini yükleyin.

1. Maliyet muhasebesi hizmetine (özel önizleme) [kaydolun](#sign-up).

1. LCS'de oturum açın

1. **Özellik yönetimi önizlemesi**'ne gidin.

1. Artı işaretini (**+**) seçin.

1. **Kod** alanına maliyet muhasebesi hizmeti için eklenti beta anahtarınızı girin. (Anahtarınızı e-posta ile almış olmanız gerekir.)

1. **Engellemeyi Kaldır**'ı seçin.

1. Hizmeti eklemek istediğiniz LCS ortamını açın.

1. **Tüm ayrıntılar**'a gidin.

1. **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.

1. **Yeni eklenti yükle**'yi seçin.

1. **Maliyet muhasebesi hizmeti**'ni seçin.

1. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.

1. **Yükle**'yi seçin.

1. **Ortam eklentileri** hızlı sekmesinde, maliyet muhasebesi hizmetinin yüklenmekte olduğunu görmelisiniz. Birkaç dakika sonra, durum **Yükleniyor** yerine **Yüklü** olarak değişmelidir. (Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, maliyet muhasebesi hizmeti kullanıma hazırdır.

## <a name="set-up-the-integration"></a>Tümleştirmeyi ayarlama

Maliyet muhasebesi hizmeti ve Dynamics 365 Supply Chain Management arasındaki tümleştirmeyi ayarlamak için:

1. **Sistem yönetimi > Özellik Yönetimi** bölümüne gidin.

1. **Güncelleştirmeleri denetle**'yi seçin.

1. **Tümü** sekmesini açın ve *Maliyet muhasebesi hizmeti* adlı özelliği arayın.

1. **Şimdi etkinleştir**'i seçin.

1. **Maliyet yönetimi > Maliyet muhasebesi hizmeti > Kurulum > Maliyet muhasebesi hizmeti parametreleri > Tümleştirme parametreleri**'ne gidin.

1. **Uygulama kodu** alanına aşağıdaki kodu girin:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. **Veri hizmeti son noktası** alanında, aşağıdaki URL'yi girin:<br>https://operationsdataservice.operations365.dynamics.com/

1. **Maliyet muhasebesi hizmeti son noktası** alanında, aşağıdaki URL'yi girin:<br>https://costaccountingservice.operations365.dynamics.com/

1. Maliyet muhasebesi hizmeti artık kullanıma hazır.

## <a name="related-resources"></a>İlgili kaynaklar

[Maliyet muhasebesi hizmeti giriş sayfası](cost-accounting-service-home.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]