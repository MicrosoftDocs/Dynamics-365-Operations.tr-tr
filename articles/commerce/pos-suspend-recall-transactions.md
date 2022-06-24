---
title: Satış noktasında (POS) bir hareketi askıya alıp devam ettirmek
description: Bu makale, kullanıcıların Dynamics 365 Commerce kullanarak sürmekte olan bir hareketi nasıl askıya alabileceklerini ve sonra başka bir kayıtta nasıl devam ettirebileceklerini açıklar.
author: jblucher
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 761adb5e1dc1c9f6ecea42ae739fe44e1f87faeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850209"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Satış noktasında (POS) bir hareketi askıya alıp devam ettirmek

[!include [banner](includes/banner.md)]


Satış noktası (POS) kullanıcıları, sürmekte olan hareketleri askıya alabilir ve onları daha sonra farklı bir kayıtta devam ettirebilirler. Hareketler çoğunlukla bir hareketi, geçerli hareket üzerindeki ilerlemeyi kaybetmeden başka bir görev için serbest bırakmakta kullanılır. Örneğin, bir mağaza çalışanı bir müşterinin işlemini bir mobil cihazda işlemeye başlıyor ancak bunu bir nakit çekmecesi olan bir kasadan tamamlamak zorunda. Bu durumda, mağaza çalışanı hareketi askıya almak mobil aygıtta ve daha sonra geri alıp onu bir kayıt üzerinde devam edebilirsiniz.

## <a name="configure-suspend-and-resume-functionality"></a>Askıya alma ve devam ettirme özelliğini yapılandırma

### <a name="pos-operations"></a>POS işlemleri

İki [POS işlemi](pos-operations.md), POS'un askıya alma ve devam ettirme senaryolarını desteklemesini sağlar. Bu işlemleri [düğme kılavuzlarına](pos-screen-layouts.md) hareket sayfası üzerinde veya hoş geldiniz sayfasında atayabilirsiniz.

- 503: Hareketi askıya al
- 504: Hareketi geri çağır

### <a name="receipt-template"></a>Giriş şablonu

POS, hareket askıya alındığında bir yazılı slip oluşturmak üzere yapılandırılabilir. Bu slip daha sonra hareketi hızlıca tespit etmek ve geri çağırmak için kullanılabilir.

POS'un bir slip yazdırmasını etkinleştirmek için **Askıya alınmış hareket** giriş biçimini mağazanın giriş profiline eklemeniz gerekir. Giriş biçimini, hareket hakkında belirli ayrıntıları dahil etmesi veya dışarıda bırakması üzerine tasarlayabilirsiniz. Örneğin, biçim taramayı desteklemek için bir barkod içerebilir.

### <a name="receipt-numbering"></a>Makbuz numaralandırma

Yazdırılmış giriş oluşturan diğer POS hareketi türleri gibi, mağazanın işlev profilindeki askıya alınmış **Giriş numaralandırma** bölümünde bir numara serisi tanımlayabilirsiniz.

### <a name="void-when-closing-shift"></a>Vardiya kapanışında hükümsüz kıl

**Vardiya kapanırken geçersiz** seçeneğini, kullanıcıların askıya alınmış hareketleri vardiyaları bitmeden önce tamamlamalarını veya hükümsüz kılmalarını gerektirmek için kullanabilirsiniz. **Vardiya kapatma** operasyonu sırasında POS, kullanıcıların kalan askıya alınmış hareketleri görüntülemesini veya hükümsüz kılmasını isteyebilir.

## <a name="suspend-and-resume-a-transaction"></a>Bir hareketi askıya almak ve devam ettirmek

### <a name="suspend-a-transaction"></a>Bir hareketi askıya al

Yeterli ayrıcalıklara sahip kullanıcılar ve **Hareketi askıya al** operasyonunu ekran düzenlerinde bulunduranlar, daha sonra başka bir kayıtta geri çağrılmak üzere bir hareketi askıya alabilirler.

Hareketler, yalnızca aşağıdaki türde satırları **içermiyorlarsa** askıya alınabilirler:

- Etkin ödeme satırları
- Hediye kartı satırları (bir hediye kartı vermek veya hediye kartı bakiyesine eklemek için)

Askıya alınmış bir hareke, mağaza için satış bilgisini veya stok kullanılabilirlik bilgisini etkilemez.

### <a name="resume-a-suspended-transaction"></a>Askıya alınmış bir hareketi devam ettirmek

Askıya alınmış hareketler, aynı mağazada yeterli ayrıcalıklara sahip herhangi bir kullanıcı ve **Hareketi geri çağır** operasyonunu içeren bir düzene sahip bir kullanıcı tarafından geri çağrılabilir ve devam ettirebilir.

Askıya alınmış bir hareketi hızlı ve kolay şekilde geri çağırmak için **Hareketi geri çağır** operasyonunda hareketlerin listesini görüntülerken yazdırılmış slip üzerindeki barkodu taratın.

### <a name="considerations-for-offline-mode"></a>Çevrimdışı mod için değerlendirmeler

- POS çevrim içi moddayken askıya alınmış herhangi bir hareket, çevrimdışı modda devam ettirilemez çünkü veri, çevirmdışı veritabanına eşitlenmemiştir.
- Bir hareketi, POS çevrimdışı moddayken askıya alırsanız, siz hareketi askıya aldıktan sonraki herhangi bir zamanda POS'un tekrar çevrimiçi moda döndürülmemiş olması şartıyla onu çevrimdışı modda geri çağırabilirsiniz. POS çevrimiçi moda geri geçtiğinde, askıya alınmış hareketler çevrimiçi veritabanına taşınır ve çevrimdışı veritabanından kaldırılır. Bu nedenle, hareketler yalnızca çevrimiçi modda devam ettirilebilir. POS'u çevrimdışı moda geri çevirirseniz, askıya alınmış bu hareketi devam ettiremezsiniz çünkü çevrimdışı veritabanından halihazırda kaldırılmıştır.

### <a name="void-a-suspended-transaction"></a>Askıya alınmış bir hareketi hükümsüz kılmak

Askıya alınmış hareketleri, hareketi geri çağırarak ve sonra **Hareketi hükümsüz kıl** operasyonunu gerçekleştirerek veya hareketi **Hareketi geri çağır** listesinde seçerek ve uygulama çubuğunda **Hükümsüz kıl** seçeneğini işaretleyerek hükümsüz kılabilirsiniz. Alternatif olarak, mağaza, kullanıcıları askıya alınmış hareketleri vardiyaları bittiklerinde hükümsüz kılmaları konusunda uyarmak üzere yapılandırılabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]