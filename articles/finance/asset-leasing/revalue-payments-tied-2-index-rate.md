---
title: Endeks oranına bağlı kira ödemelerini yeniden değerleme
description: Bu konu, endeks oranındaki bir değişiklik nedeniyle değişken kira ödemeleri değiştiğinde, kullanım hakkı (ROU) varlığı için kiralama yükümlülüğünde yapılan düzeltmeyi açıklamaktadır.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5abd1f5d265c6e8b53903e6df5c52a06b3468880
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968068"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Endeks oranına bağlı kira ödemelerini yeniden değerleme

[!include [banner](../includes/banner.md)]

Bu konu, endeks oranındaki bir değişiklik nedeniyle değişken kira ödemeleri değiştiğinde kullanım hakkı (ROU) varlığı için kiralama yükümlülüğünde yapılan düzeltmeyi açıklamaktadır. Kiralama yükümlülüğü ve ROU varlığı yeni ödeme tutarlarına göre düzeltilecektir. ABD'de Genel Kabul Görmüş Muhasebe İlkeleri'nde (ABD GAAP) standart olan Muhasebe Standartları Kodlaması Konu 842 (ACS 842) kapsamında, nakit akışlarında ek değişiklikler olmadıkça, endeks oranındaki değişiklik nedeniyle ödemeler arttığında veya azaldığında yalnızca değişken ödemeler değişir. Bu ek değişiklikler, faiz oranlarıyla ilgili kiralama koşullarında değişiklik içerebilir. Daha fazla bilgi için, ASC 842-10-55-225 ile Uluslararası Mali Raporlama Standardı 16 (IFRS 16) belgesinin 42(b) paragrafına bakın.

## <a name="adjust-lease-payments"></a>Kira ödemelerini düzeltme

Endeks oranına bağlı kira ödemelerini yeniden değerlemek için bu adımları izleyin.

1. Kira endeksi yeniden değerleme işlemini çalıştırmak için **Varlık kiralama \> Periyodik \> Endeks oranı yeniden değerleme** bölümüne gidin.

    **Endeks oranı yeniden değerleme** sayfası görüntülenir ve daha önce çalıştırılan tüm kira endeksi yeniden değerleme işlemlerini gösterir. Bu sayfadaki bilgiler arasında numarası sırası kurulumdan oluşturulan işlem kimliği, tüzel kişilik, düzeltilen kiralama defterlerinin sayısı, IFRS 16 kiralamaları için toplam yükümlülük düzeltmesi ve ASC 842 kiralamaları için düzeltilen toplam değişken ödemeler yer alır.

2. Yeniden değerlemeyi çalıştırmak için Eylem Bölmesinde **Kira endeksi yeniden değerlemesi**'ni seçin.

    **Endeks yeniden değerleme parametreleri** iletişim kutusu görüntülenir. Burada, yeniden değerlenecek kiraları seçerken kullanılması gereken kiralamaları, kiralama gruplarını ve diğer ölçütleri filtreleyebilir ve seçebilirsiniz. Ayrıca, **Arka planda çalıştır** sekmesinde, endeks yeniden değerleme işlemini toplu iş olarak çalıştırılması için ayarlayabilirsiniz.

4. Arka plan işlemine eklenmesi gereken kiraların seçilmesiyle ilgili filtreleri belirleyin ve ardından **Tamam**'ı seçin.

    **Endeks Oranı yeniden değerleme önizlemesi** iletişim kutusu görüntülenir ve yeniden değerlenecek kiralamaları gösterir. Ayrıca, varlık ve sorumluluk düzeltmelerini veya değişken ödeme ayarlamalarını gösterir.

5. Kiralamaların yeniden değerlemeye alınmasını önlemek için yeniden değerlenmesi **gereken** kiralamaları seçin. Hiçbir kiralama seçmezesniz tüm kiralamalar yeniden değerlenir. Bitirdiğinizde kira ödemelerini yeniden değerlemek için **Tamam**'ı seçin.
6. Belirli bir endeks yeniden değerleme işlemi için oluşturulan hareketleri görüntülemek için işlem kimliğini seçin ve ardından **Hareketler**'i seçin.

    Bir iletişim kutusu görünür ve işlem sırasında oluşturulan hareketlerin ayrıntılarını gösterir.

> [!NOTE]
> Yalnızca, yeniden değerleme tarihi sistem tarihinde veya öncesinde olan kiralamalar tekrar değerlenir. Sistem, yeniden değerleme tarihi sistem tarihinden daha ilerideki bir tarih olan tüm kiraları otomatik olarak yok sayar.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842 kiraları – Dizin yeniden değerlemesi

ASC 842 kiralamalarında kira yeniden değerleme işleminin etkilerini görmek için bir kiralamanın ödeme planını açın. Endeks yeniden değerlemesi nedeniyle sayfada yalnızca yeniden değerleme tarihinde veya daha sonra yapılan değişken ödemeler gösterilir. İtfa ve amortisman planları değişmeden kalır. Değişken ödemesi olan bir fatura oluşturduğunuzda, değişken ödeme Değişken ödeme deftere nakil hesabına borç olarak kaydedilir. Ayrıca değişken ödeme tutarı, kiralama defteri kurulumuna bağlı olarak doğrudan satıcıya nakledilen alacak girişine eklenir veya Senet borçları hesabına nakledilir.

Kiralama ayrıntıları sayfasındaki ödeme planı satırları yeni endeks oranını gösteren yeni bir satırla otomatik olarak güncelleştirilir. Ek olarak, bir sütun satırın el ile veya dizin yeniden değerleme işlemi ile oluşturulup oluşturulmadığını gösterir.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16 kiraları – Dizin yeniden değerlemesi

IFRS 16 kiralamalarında kira yeniden değerleme işleminin etkilerini görmek için düzeltilen bir kiralamanın kiralama ayrıntılarını açın. **Kiralama süresi** ve **Varlık faydalı ömrü** alanları, başlangıç tarihi veya değişiklik tarihinden yeniden değerleme tarihine kadar geçern süreyi yansıtacak şekilde güncelleştirilir. Ek olarak, ödeme planı satırları kiralamadaki yeni ödemeleri, yeni endeks oranını ve satırın oluşturulma şeklini yansıtacak şekilde güncelleştirilir.

Yeniden değerleme tarihinde başlatılan yeni oluşturulmuş ödeme planını görüntüleyebilir ve güncelleştirilmiş toplam ödeme tutarını gösterebilirsiniz. Ayarlanmış ödeme planını yansıtmak için yeni bir kiralama yükümlülüğü amortisman planı ve varlık amortisman planı da oluşturulur.

Günlük girişi, endeks yeniden değerlemesiyle ilgili olan kira ödemesi değişikliğini kaydetmek için düzeltme günlük girişini otomatik olarak deftere nakleder.

> [!NOTE]
> **Kira ayrıntıları** sayfasının **Genel** hızlı sekmesinde **Ödeme tutarı dökümü** seçeneği etkinleştirilmişse ve ilişkili defter, IFRS 16 ise dizin yeniden değerleme süreci **Ödeme tutarı dökümü** iletişim kutusunda otomatik olarak bir kayıt ekler. Dizin yeniden değerleme nedeniyle, tutar ödeme için yapılan değişikliği yansıtır. Kayıt, **IRFS 16 dizin yeniden değerlendirmesi için kullanıldı** olarak işaretlenir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
