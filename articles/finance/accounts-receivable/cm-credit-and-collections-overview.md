---
title: Alacak ve tahsilatlara genel bakış
description: Bu konu, alacak ve tahsilatlar işlevselliğine genel bir bakış sağlamaktadır.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.custom: intro-internal
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 81518cf7e70e8283d55e0b031bb1c48f1fad840f
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337291"
---
# <a name="credit-and-collections-overview"></a>Alacak ve tahsilatlara genel bakış

[!include [banner](../includes/banner.md)]

Müşterileriniz için kredi limitlerini yönetebilir ve gerekli olduklarında, tahsilat faaliyetleri gerçekleştirebilirsiniz.

## <a name="credit-management"></a>Alacak yönetimi

Müşteri kredi yönetimi, oluşturduğunuz kredi kurallarına göre kredi limitlerini yönetmenizi ve deftere nakil işlemi aracılığıyla satış siparişlerinin akışını denetlemenizi sağlar.

Kredi yönetimi işlemi aşağıdaki adımlardan herhangi birini içerebilir:

- Müşterilerin kredi tutarı hakkında ek bilgiler sağlamak için kredi niteliklerini güncelleştirin.
- Kredi limiti ayarlamalarını kullanarak müşteriler için kredi limitleri oluşturun.
- Kredi limiti ayarlamalarını kullanarak geçici kredi limitleri oluşturun. Bu şekilde, iş gereksinimlerine göre müşteri kredi limitlerini geçici olarak artırabilir veya azaltabilirsiniz.
- Kredi limitini etkileyebilen bilgiler (sigorta ve garantiler hakkındaki bilgiler vb.) ekleyin.
- Müşterileri tek bir kredi limitini paylaşacak şekilde birbirine bağlayan müşteri kredi grupları oluşturun.
- Müşterilere risk puanları atayın ve daha sonra kredi limiti ayarlamalarıyla bu müşteriler için otomatik olarak kredi limitleri oluşturmada bu puanları kullanın.
- Risk, ödeme koşulları, kredi limitleri, vadesi geçmiş tutarlar ve kullanılmış kredi limiti yüzdesi gibi faktörlere bağlı olarak bir veya daha fazla deftere nakil işlemi sırasında siparişi beklemeye alan durdurma kuralları oluşturun.
- Beklemedeki satış siparişlerinin listesini yönetin, bekletme nedenlerini inceleyin ve sorunları çözün.
- Satış siparişlerini, deftere nakil işlemi üzerinden devam edecek şekilde serbest bırakın.
- Kredi limiti değişikliklerinin ve satış siparişi serbest bırakma işlemlerinin onayını yönetmek için bir iş akışı ayarlayın.

## <a name="collections-management"></a>Tahsilat yönetimi

**Tahsilatlar** sayfası, alacak hesapları tahsilat bilgilerinin yönetildiği tek bir merkezi görünüm sağlar. Tahsilat yöneticileri, tahsilatları yönetmek için bu merkezi görünümü kullanabilir. Tahsilat temsilcileri, tahsilat işlemine önceden tanımlanmış tahsilat ölçütlerini kullanarak oluşturulmuş müşteri listelerinden veya **Müşteriler** sayfasından başlayabilirler.

Tahsilatları ayarlamaya veya bunlar üzerinde çalışmaya başlamadan önce aşağıdaki kavramları anlamanız gerekir:

- Müşteri yaşlandırma anlık görüntüsü belirli bir zamandaki yaşlandırılmış bakiye bilgilerini içerir.
- Tahsilat müşteri havuzları işinizi organize etmenize yardımcı olur.
- Tahsilat temsilcilerinin kendi müşteri havuzları olabilir.
- Liste sayfaları tahsilat müşterilerini, etkinlikleri ve vakaları organize eder.
- Bir müşteriyle ilgili tüm tahsilat bilgileri tek bir sayfada bulunur ve bu sayfadan eylem gerçekleştirebilirsiniz.
- Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme işlemi tek bir adımda yapılabilir.
- Silme hareketleri tek bir adımda oluşturulabilir.
- Yetersiz fon (NSF) ödemeleri tek adımda işlenebilir.

Bu kavramların açıklamaları için bkz. [Tahsilat yönetimi temel kavramları](./cm-collections-concepts.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Müşteri kredi yönetimi parametreleri kurulumu](./cm-credit-mgmt-setup.md)

[Müşteri kredi yönetimi kurulum bilgileri](./cm-setup-information.md)

[Müşteri için alacak yönetimi bilgileri ekleme](./cm-add-credit-mgmt-information-customer.md)

[Müşteri alacak grupları](./cm-customer-credit-groups.md)

[Müşteri kredi limiti ayarlamaları](./cm-credit-limit-adjustments.md)

[Satış siparişleri için askıda krediler](./cm-sales-order-credit-holds.md)

[Müşteri kredi yönetimi periyodik görevleri](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]