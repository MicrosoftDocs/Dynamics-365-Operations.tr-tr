---
title: Ödeme modülü hata referans kodları
description: Bu makalede, Microsoft Dynamics 365 Commerce'te kullanıcının karşılaştığı hata iletilerinde gösterilen ödeme modülü hata referans kodları açıklanmaktadır.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728258"
---
# <a name="checkout-module-error-reference-codes"></a>Ödeme modülü hata referans kodları

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te kullanıcının karşılaştığı hata iletilerinde gösterilen ödeme modülü hata kodları açıklanmaktadır.

Dynamics 365 Commerce'te, çevrimiçi müşterilere sunulan çevrimiçi kanal ödeme hatalarına dahil edilebilecek standartlaştırılmış hata referansları kullanıma sunulmuştur. Commerce sürüm 10.0.31 ve üstünde ödeme modülündeki hata iletileri, hata kodlarını içerir ve çevrimiçi müşteriye gereksiz bilgiler gösterilmez. Hata kodları, bu makalede açıklanan hatalara atıfta bulunur.

Karşılaşılan hataya bağlı olarak, bu makaledeki tabloda aşağıdaki ayrıntılar bulunur:

- Hataya neden olan koşulun açıklaması veya ek ayrıntılar
- Ortam veya ödeme bağlayıcısı yapılandırmalarında dikkat edilmesi gereken bilgiler
- Ek yardım gerekirse destek olayında başvurulabilecek bilgiler

## <a name="prerequisites"></a>Ön Koşullar

Aşağıda listelenen ödeme modülü hata referans kodlarını etkinleştirmek için sitenizin site oluşturucusunda **Site ayarları \> Uzantılar**'a gidin ve **Kart ve ödeme** bölümünde **Gelişmiş Çevrimiçi Kanal Hatası Ekran Mesajlaşmasını Etkinleştir**'i seçin. 

## <a name="checkout-module-error-reference-codes"></a>Ödeme modülü hata referans kodları

Müşteriler tarafından sağlanan veya çevrimiçi mağazada deneyimlenen hata kodu referansları hakkında daha ayrıntılı bilgi edinmek için aşağıdaki tabloyu kullanın. **Hata açıklaması** sütununu görüntülemek için sağa kaydırın.

| Hata kodu | Dynamics ile ilişkili hata kodu | Hata açıklaması |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Ödeme yetkisi alınamadı. **TokenizedPaymentCard** öğesinde Kart Türü Kodu eksik veya girilen Kart Türü Kodu desteklenmiyor. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Reddedildi. Ödeme yetkisi alınamadı. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Ödeme yetkisi alınamadı. Müşteriden ek bilgi alınması gerekiyor. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Üzgünüz, bir sorun oluştu. Kart ödemesi kabulü sonucunu alamadık. Tekrar deneyin veya sistem yöneticinizle iletişime geçin. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Satıcı ödeme özellikleri eksik olduğundan ödeme yapılamıyor. Sistem yöneticinize başvurun. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | İşlem için ödeme hizmeti alınamadı. Bu ödeme türü için ödeme yöntemi ayarlarınızı kontrol edin. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Müşteri hesabı ödemesi zaten uygulandı ve hareket başına yalnızca bir ödemeye izin veriliyor. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Müşteri hesabı sınırı, ödenmesi gereken tutardan farklı. Farklı bir ödeme yöntemi deneyin veya ek yardım için müşteri desteğine başvurun. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Müşteri hesabı ödemesi, listelenen öğelerin vadesi gelen toplamını aşıyor. Daha sonra tekrar deneyin veya yardım için müşteri desteğine başvurun. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Müşteri hesabı ödemesi kendi hesabını veya ödeme satırında eşleşen fatura hesabını gerektirir. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Müşteri hesabı ödemesi şu anda işlenemiyor. Taban sınır değeri aşıldı. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Bu müşterinin açık hesapla ödeme yapmasına izin verilmiyor. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Üzgünüz, bir sorun oluştu. Ödeme iptal edilemedi. Tekrar deneyin. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Ödeme işlenirken bir hata oluştu. Daha sonra tekrar deneyin. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Bağlılık programı ödeme tutarı bu harekette kullanılan bağlılık programı kartı için izin verilen değeri aşıyor. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Bağlılık programı para iadesi tutarı bu harekette kullanılan bağlılık programı kartı için izin verilen değeri aşıyor. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Bağlılık programı kartı numarası bulunamadı. Bağlılık programı kartı numarasını etkinleştirin veya farklı bir kart numarası girin ve ardından yeniden deneyin. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Bağlılık programı kart numarası kullanılamıyor. Farklı bir kart numarası girin ve yeniden deneyin. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Bu bağlılık programı kartı, bu hareket için bağlılık programı puanlarını kullanmaya uygun değil. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Hediye kartı numarası ile ilgili bir hata oluştu. Farklı bir hediye kartı deneyin veya ek yardım için müşteri desteğine başvurun. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Tutar, hediye kartı bakiyesini aşıyor. Farklı bir tutar girin ve yeniden deneyin. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Hareket birden fazla bağlılık programı ödeme satırı içeremez. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Ödeme bilgileri eksik veya hatalı olabilir. Ödeme bilgilerini doğrulayın ve yeniden deneyin. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Siparişiniz şu anda işlenemiyor. Daha sonra tekrar deneyin. |
| CCR025     | Ödeme API'si için Ön Uç Zaman Aşımı | Ön uç işlemi zaman aşımına uğradı. Siparişin Dynamics 365 Commerce Headquarters'ta işlenip işlenmediğini onaylayın. |
| CCR026     | Değiştirilen Orijinal Yetkilendirilen Tutar | Sipariş tutarı, ödeme ağ geçidiyle işlenen orijinal yetkilendirme tutarından farklı bir tutar olarak değişti. Bunun nedeni bir kuponun, promosyonun veya satışın zaman aşımına uğraması olabilir. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Ödeme işlenirken bir hata oluştu. Sepet API'sine sağlanan referans, beklenenden farklı bir referans (ödeme işlemi sırasındaki olası tutarsızlığa dikkat edin). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Ödeme yöntemi denenirken bir hatayla karşılaşıldı. Hesap ayarlarınızı gözden geçirmek veya farklı bir ödeme yöntemiyle tekrar denemek için destek ekibine başvurun. |

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](dev-itpro/payments-retail.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)
