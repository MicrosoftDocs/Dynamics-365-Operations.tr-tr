---
title: Kiralama parametrelerini yapılandırma (Önizleme)
description: Bu konuda, Varlık kiralamayla ilgili yapılandırma ayarları (ör. güvenlik bilgileri ve muhasebe ayarları) açıklanmaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e5f0aeddfa9d3f27500b033d4b4fb0fb1731105a28be4a6934b2328d62df6ec1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779050"
---
# <a name="configure-lease-parameters"></a>Kiralama parametrelerini yapılandırma

[!include [banner](../includes/banner.md)]

Birçok yapılandırma ayarı, Varlık kiralamanın davranışını etkiler. Bu ayarlar günlük adlarını, genel parametreleri ve deftere nakil profili ayarlarını içerir.

1. **Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.
2. **Kiralamalar** sekmesinde, **Genel** hızlı sekmesini seçin.

    **El ile sınıflandırmayı geçersiz kılmaya izin ver** parametresi, ödeme planı onaylanmadan önce kiralama sınıflandırmasının geçersiz kılınıp kılınamayacağını belirler.

    **Tüzel kişilikler arası toplu iş** parametresi, geçerli tüzel kişilikten diğer tüzel kişiliklerin defterine nakil yapıp yapamayacağınızı belirler. Bu parametre açıksa erişiminiz olan tüzel kişilikler için günlük girişleri oluşturabilirsiniz.

3. Ödeme planları onaylanan kiralamaların silinmesine izin vermek için **Onaylanan kiralamaların silinmesine izin ver** seçeneğini **Evet** olarak ayarlayın. Bu seçeneğin ayarı ne olursa olsun, kiralamalar ile deftere nakledilen veya nakledilmeyen hareketler ilişkilendirilmişse kiralamalar silinemez. Bir kiralama kaydını silindikten sonra geri alamazsınız. Silinen bir kiralama için el ile veya veri kaynakları üzerinden kayıt yüklerseniz, yüklenen bilgiler mevcut bir kiralamanın güncelleştirilmesi olarak değil yeni bir kiralama olarak kabul edilir.

    Bu seçeneği **Evet** olarak ayarlarsanız ve defterin hareket türü **Kümülatif Yakalama Seçeneği A veya B** ise sistem, **Alternatif borçlanma oranı** alanını **Defter kurulumu** sayfasındaki **Geçişte alternatif borçlanma oranı** değerine ayarlar. Bu seçenek **Hayır** olarak ayarlanırsa, defterin geçiş türüne bakılmaksızın, üst kiralamadaki oran **Defter ayrıntıları** sayfasındaki **Alternatif borçlanma oranı** alanının değerine ayarlanır.

4. Amortisman gider hareketlerinin tersine çevrilmesine izin vermek için **Kapalı defter sürümünde amortisman ters işlemlerine izin ver** seçeneğini **Evet** olarak ayarlayın. Defter sürümü kapalı olsa bile gider hareketleri tersine çevrilebilir.

    > [!NOTE]
    > Bu seçeneği **Hayır** olarak tutmanızı öneririz. Bu seçeneğin ayarı, kapatılmış bir defter sürümüne yanlışlıkla amortisman uygulanmasını önlemek için doğrulama ve denetim amaçlı kullanılır. Seçenek **Hayır** olarak kaldığında, net defter değerinin ve gelecekteki amortisman hesaplamalarının doğru olmasına yardımcı olursunuz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
