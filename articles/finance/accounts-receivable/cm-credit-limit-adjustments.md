---
title: Alacak limiti ayarlamaları
description: Bu konu, kredi limiti ayarlamalarının nasıl yapılacağını ve ekleneceğini açıklamaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d55a7c5e24213f70a1b71f89691f0e5be8c36f10
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976583"
---
# <a name="credit-limit-adjustments"></a>Alacak limiti ayarlamaları 

[!include [banner](../includes/banner.md)]

Kredi limiti ayarlamaları, kredi yöneticilerinin bir deftere nakil işlemiyle tek bir müşterinin, bir müşteri grubunun veya tüm müşterilerin kredi limitlerini ve kredi bitiş tarihlerini güncelleştirmelerini sağlar. Kredi limiti ayarlama girişlerini; müşterileri ve müşteri kredi gruplarını güncelleştirmek için ekleyebilir veya otomatik kredi limitlerini hesaplamak için kullanabilirsiniz. Girişler daha sonra incelenebilir, bir iş akışıyla onaya gönderilebilir ve müşteri hesaplarına nakledilebilir.

## <a name="set-up-credit-limit-adjustments"></a>Kredi limiti ayarlamaları

**Kredi limiti ayarlama** sayfasındaki (**Kredi yönetimi \> Kredi limiti ayarlamaları \> Kredi limiti ayarlamaları**) Kredi limiti ayarlama günlüğünde girişler oluşturabilirsiniz.

1. **Yeni**'yi seçin. Kredi limiti ayarlama numarası olan yeni bir giriş grubu oluşturulur.
2. Kredi limiti ayarlama türünü seçin:

    - Müşterinin kredi limitini değiştirmek için **Kredi limiti**'ni seçin.
    - Müşterinin geçerli kredi limitini değiştirmek yerine geçici bir kredi limiti oluşturmak için **Geçici kredi limiti**'ni seçin. Geçici kredi limitleri, bir müşterinin belirli bir döneme ait kredi limitini geçersiz kılar. Bu dönem sona erdikten sonra, müşterinin kredi limiti yeniden kullanılır.
3. Açıklama girin. 

**Deftere nakledildi** onay kutusu işaretlenirse, kredi limitleri uygulanmıştır. **Onay durumu** alanı, günlüğün iş akışı durumunu gösterir. İş akışı isteğe bağlıdır.

### <a name="add-credit-limit-adjustments"></a>Kredi limiti ayarlamalarını ekleme

Kredi limiti ayarlamalarını el ile eklemek için **Satırlar**'ı seçin ve aşağıdaki adımları izleyin.

1. Bir müşteriye ilişkin kredi limiti ayarlaması eklemek için **Müşteri ayarlamaları** menüsünü kullanın. Müşteri kredi grubuna kredi limiti eklemek için **Müşteri kredi grubu ayarlamaları**'nı seçin.
2. Yeni kredi limitine göre güncelleştirilmesi gereken fatura müşterisi hesabı için bir müşteri hesabı girin. Adım 1'de **Müşteri kredi grubu ayarlamaları**'nı seçtiyseniz müşteri kredi grubunu girin. Aynı günlük satırına hem müşteri hesabı hem de müşteri kredi grubu kodu giremezsiniz.

    Geçerli kredi limiti gösterilir ve ad otomatik olarak görüntülenir.

3. Kredi limiti girişi deftere nakledildiği zaman geçerli kredi limitinin yerini alması gereken yeni kredi limitini girin.
4. Müşteri kredi limitine ilişkin yeni sona erme tarihini tanımlamak için bir tarih girin. Kredi limiti ayarlaması oluştururken bir kredi limiti bitiş tarihi girmeniz gerekir.

**Onay durumu** alanı, günlük satırının iş akışı durumunu gösterir.

Kredi limiti ayarlamalarının otomatik olarak oluşturulmasını istiyorsanız, eylem bölmesindeki **Oluştur** menüsünü kullanabilirsiniz.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Geçici kredi limiti ayarlamaları ekleme

Geçici kredi limiti ayarlamalarını el ile eklemek istiyorsanız, günlük satırları için bu adımları izleyin.

1. Bir müşteriye ilişkin kredi limiti ayarlaması eklemek için **Müşteri ayarlamaları** menüsünü kullanın. Müşteri kredi grubuna kredi limiti eklemek için **Müşteri kredi grubu ayarlamaları**'nı seçin.
2. Yeni kredi limitine göre güncelleştirilmesi gereken fatura müşterisi hesabı için bir müşteri hesabı girin. Adım 1'de **Müşteri kredi grubu ayarlamaları**'nı seçtiyseniz müşteri kredi grubunu girin. Aynı günlük satırına hem müşteri hesabı hem de müşteri kredi grubu kodu giremezsiniz.

    Etkin veya ileriye yönelik bir geçici kredi limiti zaten varsa, her geçici kredi limiti için geçerli geçici kredi limiti ve tarih aralıkları görünür. Ad otomatik olarak görüntülenir.

3. Geçerli kredi limitinin yerini alacak yeni kredi limitini girin.
4. **Yeni başlangıç tarihi** ve **Yeni bitiş tarihi** alanlarında, ileriye yönelik kredi limitinin geçerli olduğu dönemi tanımlayın. Kredi limiti ayarlama günlüğü oluştururken kredi limiti bitiş tarihleri girmeniz gerekir.

**Onay durumu** alanı, günlük satırının iş akışı durumunu gösterir.

## <a name="generate-credit-limit-adjustments"></a>Kredi limiti ayarlamalarını oluşturma

Kredi limitlerinin otomatik olarak ayarlanmasını da sağlayabilirsiniz. Eylem bölmesinde **Oluştur**'u seçin ve ardından aşağıdaki seçeneklerden birini belirleyin:

- Varolan müşteriden
- Varolan müşteri kredi grubundan
- Otomatik alacak limitleri

### <a name="from-existing-customer"></a>Varolan müşteriden

Varolan müşterilerden günlük satırları oluşturabilirsiniz. **Oluştur \> Varolan müşteriden**'i seçerseniz, müşterileri seçme ve yeni limitleri hesaplama için ölçütler belirtebileceğiniz bir iletişim kutusu görüntülenir.

1. Kredi limitinde bir tutar eklemek veya çıkarmak için bir ayarlama değeri girin. Geçerli kredi limitini azaltmak için negatif bir değer, artırmak için pozitif bir değer girin.
2. **Değer türü** alanında, adım 1'de girdiğiniz değerin yeni kredi limitini hesaplamak için nasıl kullanılacağını seçin:

    - Kredi limitini bir tutarla değiştirmek için **Sabit değer**i seçin.
    - Kredi limitini bir yüzdeyle değiştirmek için **Yüzde**'yi seçin.

3. Hesaplanan kredi limitini yuvarlamak için kullanılacak bir değer girin. Örneğin, kredi limitini en yakın 10,00 para birimine yuvarlamak için **10,00** girin.
4. Kalan tutarın aşağıya veya yukarıya yuvarlanacağını belirtmek için **Yuvarlama şekli** alanını ayarlayın.
5. Tarihleri ayarlamak için kullanılan yöntemi seçin.

    - **Mutlak**'ı seçerseniz, kredi limitlerinin tarih aralığını tanımlayan tarihleri girebilirsiniz.
    - **Göreli**'yi seçerseniz, aralık için mahsup tarihleri girebilirsiniz. Kredi limiti için geçerli tarih aralığı mahsupla ayarlanacaktır.

6. Dahil edilen müşterilerin listesini filtrelemek için **Eklenecek kayıtlar** hızlı sekmesini kullanın. Filtre eklemezseniz, tüm müşteriler için kredi limiti girişleri oluşturulur.
7. Kredi limiti ayarlama girişlerini oluşturmak için **Tamam**'ı seçin.

### <a name="from-existing-customer-credit-group"></a>Varolan müşteri kredi grubundan

Varolan müşteri kredi gruplarından günlük satırları oluşturabilirsiniz. **Oluştur \> Varolan müşteri kredi grubundan**'ı seçerseniz, müşteri kredi gruplarını seçme ve yeni limitleri hesaplama için ölçütler belirtebileceğiniz bir iletişim kutusu görüntülenir. Ölçütler, varolan müşterilerden günlük satırlarını oluşturmak için kullanılan ölçütlerle aynıdır. Önceki bölümde verilen adımlara bakın.

### <a name="automatic-credit-limits"></a>Otomatik alacak limitleri

Müşteri kredi limitlerini tanımlamak ve güncelleştirmek için otomatik kredi limitleri oluşturabilirsiniz. Otomatik kredi limitleri bir risk grubu için oluşturulur ve puanlama gruplarında kullanılan belirli değerlere dayanır. Kredi limiti girişleri oluşturmak için bu otomatik kredi limitlerini kullanabilirsiniz. Bir müşteri belirli bir risk grubuna atandıysa ve müşterinin kredi bilgileri otomatik kredi limiti ölçütlerine uyuyorsa, kredi limiti ayarlama girişi oluşturulur.

#### <a name="create-automatic-credit-limits"></a>Otomatik kredi limitleri oluşturma

Kredi limiti ayarlamalarını kullanarak otomatik kredi limitleri oluşturursunuz. **Oluştur \> Otomatik kredi limitleri**'ni seçtiğinizde, müşterilerin atandığı risk gruplarına dayalı olarak oluşturulacak yeni kredi limitleri için bitiş tarihi ayarlayabileceğiniz bir iletişim kutusu görüntülenir. Bitirdiğinizde, kredi limiti ayarlama satırlarını oluşturmak için **Tamam**'ı seçin.

### <a name="post-adjustments"></a>Ayarlamaları deftere nakletme

Kredi limiti ayarlama satırları oluşturduktan sonra, girişleri deftere nakletmek ve müşteri kredi limitlerini güncelleştirmek için, eylem bölmesindeki **Deftere naklet** düğmesini kullanabilirsiniz. Bununla birlikte, bir iş akışı ayarladıysanız, günlüğü onaya göndermek için eylem bölmesinde **İş akışı \> Gönder**'i seçmeniz gerekir.

### <a name="credit-limit-adjustments-workflows"></a>Alacak limiti ayarlamaları için iş akışları

**Kredi limiti ayarlamaları** iş akışları, bir iş akışı onay süreci üzerinden kredi limiti ayarlamaları göndermek için kullanılabilir. **Kredi yönetimi iş akışı** sayfasında (**Kredi yönetimi \> Kurulum \> Kredi yönetimi iş akışı**) iki iş akışı oluşturabilirsiniz:

- **Kredi limiti ayarlamaları** – Bu iş akışı, üst bilgi düzeyinde girişleri onaylamak için kullanılabilir.
- **Kredi limiti ayarlamaları satırı** – Bu iş akışı, ayarlama girişlerini onaylamak için kullanılabilir, böylece girişler iş akışı ölçütlerine farklı kişiler tarafından onaylanabilir.

> [!NOTE]
> **Kredi limiti ayarlamaları** iş akışı oluşturduğunuzda, bu iş akışını, satırlar onaylandıktan sonra ayarlamalar otomatik olarak deftere nakledilecek şekilde ayarlayabilirsiniz. İş akışına **Günlüğü otomatik olarak deftere naklet** görevini eklemeniz yeterlidir.
