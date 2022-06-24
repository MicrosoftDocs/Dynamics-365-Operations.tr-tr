---
title: Nakit yönetimi iyileştirmeleri
description: Bu makale, Dynamics 365 Commerce için POS içindeki nakit yönetimi iyileştirmelerini açıklar.
author: anpurush
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1719e309183042cd7f56be3df8cbbec31cea7c79
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849079"
---
# <a name="cash-management-improvements"></a>Nakit yönetimi iyileştirmeleri

[!include [banner](includes/banner.md)]


Nakit yönetimi fiziksel depolardaki perakendecilere yönelik bir anahtar işlevdir. Perakendeciler mağazalarının, bir mağazadaki farklı kasalara ve kasiyerlerin nakit olarak izlenebilme ve hareket etme sorumlulumının tam olarak sağlanmasına yardımcı olabilecek sistemlere sahip olmasını ister. Her türlü farkı bağdaştırmak ve sorumluluğu belirleyebilmeleri gerekir.


Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında nakit yönetimi yeteneklerine sahiptir. Ancak, 10.0.3 sürümünden önceki Retail sürümlerinde, nakit yönetimi işlevselliği mağazalardaki nakit hareketlerinin eksiksiz izlenebilmesini sağlayacak kadar sağlam değildir. Perakendeciler bir mağazanın nakit olarak mutabakat yapabilse de, bir nakit tutarsızlık durumunda sorumluluğu tam olarak belirleyemez.


Retail 10.0.3 ve sonraki sürümlerde perakendeciler, nakit işleme için izlenebilirlik kazanacaktır. Takip edilebilirliğin bir parçası olarak, perakendeciler kasalar, iki taraflı nakit hareketleri ve mutabakat sağlama nakit yönetimi hareketleri tanımayabilir.

## <a name="set-up-traceability-and-define-safes"></a>İzlenebilirliği ayarla ve güvenliği tanımla

Yeni nakit yönetimi işlevini ayarlamak için, mağazalar için işlevsellik profilini yapılandırma üzere aşağıdaki adımları izleyin.

1. **Retail and Commerce \> Kanal ayarı \> POS ayarı \> POS profilleri \> İşlev profilleri**'ne gidin ve nakit yönetimi için iyileştirmeleri gerçekleştirmek istediğiniz mağazalara bağlı bir işlev profili seçin.
2. İşlevsellik profilinin **İşlevler** hızlı sekmesinde, **Gelişmiş nakit yönetimi** altında, **Nakit izlenebilirliğini etkinleştir** ayarını **Evet** olarak ayarlayın.
3. Kasalar ayarlamak için **Retail and Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin ve bir mağaza seçin.
4. **Mağazalar** sayfasındaki Eylem Bölmesinde, **Kurulum** sekmesinin **Ayarla** grubunda **Kasalar**'ı seçin. Bu seçeneği kullanarak, bir mağaza için birden çok kasa tanımlayabilir ve saklayabilirsiniz.
4. İşlevselliğin kullanılabilmesi için önce, bu yapılandırmaları kanal veritabanıyla eşitlemek üzere **1070 kanal yapılandırması** dağıtım zamanlamasını çalıştırmanız gerekir.

## <a name="additional-cash-management-changes"></a>Ek nakit yönetimi değişiklikleri

Retail sürüm 10.0.3 ve sonrasında, nakit hareketleriyle ilgili aşağıdaki yetenekler de sağlanır:

- "Başlangıç tutarını bildir" konusunda istenen bir kullanıcının nakit kaynağını girmesi gerekir. Kullanıcı, mağazada tanımlanan kasaları arayabilir ve nakdin teslim alındığı güvenine, kasaya koyabilmek için güvenli bir şekilde seçim yapabilir.
- "Ödeme kaldırma" işlemi yapan bir kullanıcının, açık olan "float girişi" hareketleri listesinde operasyona karşı gerçekleştirilen hareketi seçmesi istenir. Karşılık gelen float girişi sistemde yoksa, kullanıcı bağlantılı olmayan bir ödeme kaldırma hareketi oluşturabilir.
- "Float girişi" işlemi, kullanıcının açık "ödeme kaldırma" hareketleri listesinde, kayan noktalı giriş operasyonunu hareket eden bir listede seçmesini ister. Karşılık gelen ödeme kaldırma sistemde yoksa, kullanıcı bağlantılı olmayan bir float girişi hareketi oluşturabilir.
- "Güvenli bırakma" yapan bir kullanıcının, nakit atılmakta olduğu güvenli seçmek isteyip istemediğiniz sorulur.
- Bir mağazada tanımlanan kasalar için kullanıcılar başlangıç tutarını bildirmek, bir kasa devri girişi yapmak, bir ödeme kaldırma işlemi yapmak ve bir banka fişi oluşturmak gibi operasyonları yönetebilir.
- Uygun kullanıcı ayrıcalıklarına sahip kullanıcılar için, "vardiyaları yönet" operasyonları etkin, askıya alınmış ve kör kapalı vardiyaların nakit bakiyelerini gösterir.
- Vardiya içinde veya vardiyalar arasında nakit hareketlerinde mutabakat sağlamak için mutabakat sağlanacak vardiyayı seçin ve **Mutabakat sağlama**'yı seçin. Açılan görünüm, ayrı sekmelerde mutabakat sağlanan ve mutabakat sağlanmamış hareketlerin listesini gösterir. Kullanıcılar bu görünümden, mutabakat sağlanmamış hareketleri seçebilir ve bunların mutabakatını yapabilir veya önceden mutabakat yapılan hareketleri seçebilir.
- Mutabakat sırasında, seçilen hareket dengelenmemiş ise, kullanıcı, dengesiz mutabakat için neden açıklaması girmelidir. Kullanıcılar tek bir hareketi seçip gereken neden açıklamasıyla mutabakat yapabilirler.
- Kullanıcılar, vardiya kapatılıncaya kadar hareketlerin mutabakatını ve mutabakatlaştıralmaya devam edebilir. Bir vardiya kapatıldıktan sonra hareketler mutabakat geri alınamaz.
- Kullanıcı vardiyayı kapatmayı seçtiğinde, Commerce, vardiyada hiçbir mutabakat sağlanmamış nakit yönetimi hareketi olmadığını doğrular. Mutabakatı yapılmamış hareketler varsa kullanıcılar bir vardiyayı kapatamaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]