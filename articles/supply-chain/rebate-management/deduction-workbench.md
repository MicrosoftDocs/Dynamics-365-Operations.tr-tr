---
title: Kesinti workbench'ini kullanarak kesintileri yönetme
description: Bu makalede, kesintileri içeren müşteri ödemelerini işlemek için kesinti workbench'inin nasıl kullanılacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 607ad528b56d1f0c9a78e113f67c920cdae6e620
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873622"
---
# <a name="manage-deductions-using-the-deduction-workbench"></a>Kesinti workbench'ini kullanarak kesintileri yönetme

[!include [banner](../includes/banner.md)]

Bu makalede, kesintileri içeren müşteri ödemelerini işlemek için kesinti workbench'inin nasıl kullanılacağı açıklanmaktadır.

İndirime sahip olan bir müşteri, indirim ödemesini beklememeye karar verebilir. Bunun yerine müşteri, indirim tutarı için kesinti içeren bir ödeme gönderebilir. Bu tür bir hareketi işlemek için kesintileri kredi hareketleri açma, kesintileri bölme, kesintileri reddetme ve kesintileri silme işlemleriyle eşleştirmek üzere kesinti workbench'ini kullanabilirsiniz.

> [!NOTE]
> Kesinti workbench'i uzun süredir Microsoft Dynamics 365 Supply Chain Management'ta satış ve pazarlama işlevinin bir parçası olmuştur. Şimdi ise daha yeni **İndirim yönetimi** modülüyle de çalışacak şekilde geliştirilmiştir. Bu makalede, kesinti workbench'inin eski özelliklerinin ve İndirim yönetimi özelliklerinin nasıl kullanılacağı açıklanmaktadır. Ancak [sisteminizde **İndirim yönetimi** modülünü açmadıysanız](rebate-management-enable.md) burada açıklanan işlevlerin bazılarını kullanamazsınız.

## <a name="prerequisites"></a>Önkoşullar

### <a name="set-up-the-old-deduction-management-system"></a>Eski kesinti yönetimi sistemini ayarlama

**İndirim yönetimi** modülünü kullanmasanız bile kesinti workbench'ini Supply Chain Management'ın eski kesinti yönetimi özellikleriyle birlikte kullanabilirsiniz. Ancak öncelikle sisteminizi bu bölümde açıklandığı gibi hazırlamanız gerekir.

Kesinti workbench'ini kullanmadan önce [Kesinti yönetimini ayarlama](/dynamicsax-2012/appuser-itpro/set-up-deduction-management) bölümünde açıklanan ayarlama görevlerini tamamlamanız gerekir. Ayrıca müşteri için [Müşteri indirimlerini ayarlama ve sürdürme](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates) bölümünde açıklandığı gibi bir müşteri indirimi veya bir ticari tahsisat indirimi şeklinde bir tür indirim sözleşmesi ayarlamış olmanız gerekir.

Müşteri indirimi için kesinti uyguluyorsanız şu görevleri tamamlamanız gerekir:

- [Müşteri indirimlerinizi ayarlama](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-customer-rebates).
- İndirim workbench'ini kullanabilmeniz için indirimi onaylayın ve işleyin.

Ticari tahsisat indirimi için kesinti uyguluyorsanız şu görevleri tamamlamanız gerekir:

- Sonradan faturalandırma indirimlerini ayarlayın.
- Sonradan faturalandırma indirimlerini uygulayın.

### <a name="configure-accounts-receivable-and-deductions"></a><a name="accounts-receivable-deductions"></a>Alacak hesapları ve kesintileri yapılandırma

Sistem, tüm kesinti olaylarını bir talep günlüğüne kaydeder. Bu nedenle sisteminizde bu amaçla kullanılabilecek bir günlük bulunmalıdır. Talep günlüğünüz yoksa şimdi ayarlayın. Bu günlük, kesintileri doğrudan kesinti workbench'inde, müşteri kapatma işlemlerinde veya müşteri sayfasında oluşturmak için gereklidir.

Kesintiler için yeni bir talep günlüğü oluşturmak üzere aşağıdaki adımları izleyin.

1. **Genel muhasebe \> Günlük ayarı \> Günlük adları**'na gidin.
1. **Yeni**'yi seçin ve yeni günlük adı için aşağıdaki alanları ayarlayın:

    - **Ad**: Talep günlüğü için benzersiz bir ad girin.
    - **Açıklama**: Yeni günlüğün açıklamasını girin.
    - **Günlük türü**: *Günlük* seçeneğini belirleyin.
    - **Fiş serisi**: Mevcut bir numara serisi atayın. Alternatif olarak, şirket kapsamının bulunduğu yeni bir numara serisi oluşturun ve bunu yeni günlük adına atayın.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Kesintiler** sekmesinde **Genel** hızlı sekmesinde, **Talep günlüğü adı** alanını yeni oluşturduğunuz günlük adı olarak ayarlayın.
1. **İade emri** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **İade emri oluştur**: Miktar tabanlı bir talep onaylandığında sistemin ne yapması gerektiğini belirtmek için bu seçeneği ayarlayın:

        - *Evet*: İade emri oluşturur.
        - *Hayır*: Eksi satış siparişi oluşturur.

    - **Ekli fatura olmadan oluşturma**: Miktar tabanlı bir talep onaylandığında ancak fatura eklenmediğinde sistemin ne yapması gerektiğini belirtmek için bir değer seçin:

        - *Kabul Et*: İade emri oluşturur.
        - *Uyarı*: İade emri oluşturur ancak şu uyarı iletisi gösterilir: "Talep bir faturaya eklenmemiş."
        - *Hata*: İade emri oluşturmaz ve şu hata iletisi gösterilir: "Talep bir faturaya eklenmemiş. Güncelleştirme iptal edildi."

    - **Kesinti onayından önce iade emri oluştur**: İade emirleri talep onaylanmadan önce oluşturulabiliyorsa bu seçeneği *Evet* olarak ayarlayın. Bu ayar yalnızca **İade emri oluştur** seçeneğinin *Evet* olarak ayarlandığı miktar tabanlı talepler için geçerlidir.

### <a name="configure-general-ledger-parameters"></a>Genel muhasebe parametrelerini yapılandırma

Sistem yeni bir kesinti için bir talep günlüğü oluşturduğunda iki yeni müşteri hareketi de oluşturur: Biri talep tutarını orijinal faturaya mahsup eder ve diğeri bir müşterinin borcunu talep tutarına kaydeder (talep henüz onaylanmadığından). Bu nedenle, sisteminizi tek bir fişte birden fazla müşteri satırı olacak şekilde ayarlamanız gerekir.

Tek bir fişte birden çok müşteri satırı olmasını sağlamak için aşağıdaki adımları izleyin.

1. **Genel muhasebe\> Genel muhasebe ayarı \> Genel muhasebe parametreleri**'ne gidin.
1. **Genel muhasebe** sekmesinde, **Genel** hızlı sekmesinde **Tek bir fiş içinde birden fazla harekete izin ver** seçeneğini *Evet* olarak ayarlayın.
1. Uyarı iletisi alırsanız değişikliği kabul etmek için **Kapat**'ı seçin.

### <a name="create-deduction-reasons"></a><a name="deduction-reasons"></a>Kesinti nedenleri oluşturma

Sistemde kullanıcıların doğrudan kesinti workbench'ine, müşteri kapatma işlemlerine veya müşteri sayfasına girdikleri her kesinti için bir neden belirtmeleri gerekir. Bu neden onaylandığında kesintinin nasıl işleneceğini belirler.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti nedenleri**'ne gidin.
1. Izgaraya satır eklemek için **Yeni**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

    - **Talep nedeni**: Neden için benzersiz bir ad girin.
    - **Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan neden açıklamasını girin.
    - **Talep esası**: Talep nedeni için bir talep esası seçin:

        - *Fiyat tabanlı*: Onaydan sonra serbest metinli bir alacak oluşturun.
        - *Miktar tabanlı*: Onaydan sonra eksi satış siparişi veya iade emri oluşturun.

    - **İade nedeni kodu**: İade emri için **İade nedeni kodu** değeri olarak uygulanacak bir iade nedeni kodu seçin.
    - **Tür**: Bir kesinti türü seçin. Kesinti veya talep oluşturulduğunda **Kesinti mahsubu** alanını ayarlamak için seçili türün **Kesinti mahsubu** değeri kullanılır. Kesinti türleri **Kesinti türleri** sayfasında (**Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti türleri**) tanımlanır.
    - **Deftere nakil hesabı talep et**: Bu alan yalnızca **Talep esası** alanı *Fiyat tabanlı* olarak ayarlandığında kullanılabilir. Fiyat tabanlı bir talep onaylandığında sistem burada seçtiğiniz genel muhasebe hesabını taslak serbest metinli alacak dekontu için **Ana hesap** değeri olarak atar.

### <a name="set-up-the-settle-approved-deductions-periodic-task"></a>Onaylanan kesintileri kapatma periyodik görevini ayarlama

Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintilerde eşleşen **Kesinti Kimliği** değerleri ve tutarları olan kesintileri ve kredileri otomatik olarak eşleştirmek için *Onaylanan kesintileri kapat* periyodik görevini ayarlayabilirsiniz.

Bu görevi zamanlamak için **Satış pazarlama \> Periyodik görevler \> Onaylanan kesintileri kapat**'a gidin ve diğer periyodik görev türlerinde olduğu gibi seçenekleri, filtreleri ve zamanlamayı ayarlayın.

> [!NOTE]
> **Otomatik kapatma** seçeneği **Alacak hesapları parametreleri** sayfasının (**Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**) **Kapatma** sekmesinde *Evet* olarak ayarlanırsa kredi otomatik olarak kapatılacağından *Onaylanan kesintileri kapat* periyodik görevi hiçbir işlem gerçekleştirmez.

## <a name="create-a-deduction"></a>Kesinti oluşturma

### <a name="create-a-deduction-journal-entry-by-using-the-customer-payment-journal"></a>Müşteri ödeme günlüğünü kullanarak bir kesinti günlüğü girişi oluşturma

Kesinti günlüğü girişi oluşturmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Ödemeler \> Müşteri ödeme günlüğü** seçeneğine gidin.
1. Izgaraya bir satır eklemek için **Yeni**'yi seçin.
1. Yeni satırın **Ad** alanında, günlüğün adını seçin.
1. Eylem Bölmesi'nde, **Satırlar**'ı seçin.
1. Tarihi, şirket hesabını ve müşteri hesap numarasını girin.
1. **Fatura** alanına kesintinin ilişkili olduğu faturayı seçin.
1. **Kredi** alanına müşterinin ödediği tutarı girin.
1. Tutarın işaretli hareketin toplam tutarından az olduğunu onaylamak için **Tamam**'ı seçin.
1. Mahsup hesap türünü ve mahsup hesabı seçin.
1. Izgaranın üzerindeki araç çubuğunda, **Kesintiler**'i seçin.
1. Eylem Bölmesinde, **Kesinti** sayfasında ızgaraya satır eklemek için **Yeni**'yi seçin. Yeni satırın **Kesinti Kimliği** alanı otomatik olarak ayarlanır.
1. **Tür** alanında kesinti türünü seçin.
1. **Tutar** alanına, kesinti listesinin altındaki **Bakiye** alanında gösterilen tutarı girin. Bu tutar, müşterinin ödemeden kestiği tutarı gösterir.
1. **Kesinti** sayfasını kapatın. Şimdi kesintinin yeni satırını gösteren **Müşteri ödemeleri** sayfasına geri dönersiniz.
1. Eylem Bölmesi'nde, **Doğrula \> Doğrula**'yı seçin. Şu iletiyi almanız gerekir: "Günlükte sorun yok."
1. Eylem Bölmesinde **Deftere naklet**'i seçin.

### <a name="create-a-deduction-by-using-the-deduction-workbench"></a>Kesinti workbench'ini kullanarak kesinti oluşturma

Kesinti workbench'inde yeni bir kesinti oluşturmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. Eylem Bölmesi'nde, **Yönet \> Yeni kesinti**'yi seçin.

    **Yeni kesinti** iletişim kutusunda, **Kesinti Kimliği** alanı **Ticari tahsisat yönetimi parametreleri** sayfasında (**Satış ve pazarlama \> Kurulum \> Ticari tahsisatlar \> Ticari tahsisat yönetimi parametreleri**) tanımlanan **Kesinti Kimliği** numara sırasına göre ayarlanır.

1. Aşağıdaki alanları ayarlayın:

    - **Müşteri hesabı**: Kesinti için geçerli olan müşteri hesabını seçin.
    - **Harici talep numarası**: Müşterinin talep başvurusunu girin.
    - **Talep tutarı**: Vergi dahil talep tutarını girin. Değer pozitif olmalıdır.
    - **Para Birimi**: Kesintinin para birimini seçin. Varsayılan değer, seçili müşteri hesabı için ayarlanan para birimidir.
    - **Talep esası**: Talep esasını seçin. Talep esası, kesinti veya talep onaylandıktan sonra oluşturulan kredi hareketinin türünü belirler.

        - *Fiyat tabanlı*: Taslak serbest metinli fatura oluşturulur.
        - *Miktar tabanlı*: Eksi satış siparişi veya iade emri oluşturulur.

    - **Talep tarihi**: Talebin tarihini seçin. Varsayılan değer, geçerli tarihtir.
    - **Talep nedeni**: Mevcut kesinti için geçerli olan neden kodunu seçin. Seçtiğiniz talep esası, geçerli seçenekleri etkiler. Burada seçim için kullanılabilir talep nedenlerini oluşturma ve yapılandırma hakkında daha fazla bilgi için bu makalenin önceki [Kesinti nedenleri oluşturma](#deduction-reasons) bölümüne bakın.
    - **Notlar**: Geçerli not ekleyin. Talep onaylandığında onaylayan, talebin notlarını düzenleyebilir veya bunlara ekleme yapabilir.
    - **Talep günlüğü oluştur**: Talep veya kesinti oluşturulduğunda talep günlüğünün oluşturulup oluşturulmayacağını belirtmek için bu seçeneği ayarlayın:

        - *Evet*: Sistem, **Alacak hesapları parametreleri** sayfasında ayarlanan talep günlüğünü kullanarak bir yevmiye defteri oluşturup deftere nakleder. (Daha fazla bilgi için bu makalenin önceki [Alacak hesapları ve kesintileri yapılandırma](#accounts-receivable-deductions) bölümüne bakın.) Talebe bir fatura eklendiğinde talep günlüğü, geçerli faturanın bakiyesini azaltmak için kullanılır. Daha sonra talep reddedilirse talep günlüğü ve kapatma işlemleri (fatura eklenmişse) tersine çevrilir.
        - *Hayır*: Bu durumda talep günlüğü oluşturulmaz. Talep günlüğü, talep onaylandığında oluşturulur. Talep günlüğü oluşturulmamış olsa bile yeni talebe bir fatura eklenebilir. Ancak talep günlüğü olmadan kapatma yapılamaz.

1. **Tamam**'ı seçin.

    Yeni bir kesinti oluşturulur. **Talep günlüğü oluştur** seçeneğini *Evet* olarak ayarlarsanız aşağıdaki hareketler deftere nakledilir:

    - **İki yeni müşteri hareketi**: Bir hareket, talep tutarını orijinal faturaya göre mahsup eder. Talep henüz onaylanmadığından diğer hareket bir müşterinin borcunu talep tutarına kaydeder. Eylem Bölmesi'nde **Yönet \> Fatura ekle**'yi seçerek faturayı eklediğinizde orijinal fatura hareketi ve mahsup talebi hareketi otomatik olarak kapatma olarak işaretlenir.
    - **İki mahsup hareketi**: Bu hareketler **Kesinti mahsubu** genel muhasebe hesabına nakledilir.
    - **Talep günlüğü**: Kesinti workbench'inde gösterilen her kesinti için talep günlüğünü görüntülemek üzere **Başvurular** sekmesini seçin. Talep günlüğü, **Günlük toplu iş numarası** alanında gösterilir. Talep günlüğünü **Kesinti olayları** sekmesinde de görüntüleyebilirsiniz. Burada, *Eşleştirme*'nin **Güncelleştirme türü** değerini alır.

### <a name="create-a-deduction-from-a-customer-settlement"></a>Müşteri kapatma işleminden kesinti oluşturma

Müşteri kapatma işleminden kesinti oluşturma işlemi, kesinti workbench'i aracılığıyla kesinti oluşturma işlemine benzer. Ancak müşteri ve fatura para birimi otomatik olarak ayarlanır ve fatura eklenir. Müşteri kapatma sayfası aracılığıyla bir talep veya kesinti oluşturduğunuzda Eylem Bölmesi'nde **Yönet \> Fatura ekle**'yi seçmeniz gerekmez.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Adına kesinti oluşturulacak müşteriyi seçin.
1. Eylem Bölmesinde **Tahsil Et** sekmesindeki **Kapatma** grubunda **Hareketleri kapat**'ı seçin.
1. **Hareketleri ayarlama** iletişim kutusunda, **Genel Bakış** sekmesinde kesintinin oluşturulacağı faturayı seçin.
1. Araç çubuğunda, **Kesintiler \> Yeni kesinti**'yi seçin.

    **Yeni kesinti** iletişim kutusunda, **Kesinti Kimliği** alanı **Ticari tahsisat yönetimi parametreleri** sayfasında (**Satış ve pazarlama \> Kurulum \> Ticari tahsisatlar \> Ticari tahsisat yönetimi parametreleri**) tanımlanan **Kesinti Kimliği** numara sırasına göre ayarlanır. **Müşteri hesabı** alanı kesinti için geçerli olan müşteri hesabı olarak ayarlanır.

1. Aşağıdaki alanları ayarlayın:

    - **Harici talep numarası**: Müşterinin talep başvurusunu girin.
    - **Talep tutarı**: Vergi dahil talep tutarını girin. Değer pozitif olmalıdır.
    - **Para Birimi**: Kesintinin para birimini seçin. Varsayılan değer, seçili müşteri hesabı için ayarlanan para birimidir.
    - **Talep esası**: Talep esasını seçin. Talep esası, kesinti veya talep onaylandıktan sonra oluşturulan kredi hareketinin türünü belirler.

        - *Fiyat tabanlı*: Taslak serbest metinli fatura oluşturulur.
        - *Miktar tabanlı*: Eksi satış siparişi veya iade emri oluşturulur.

    - **Talep tarihi**: Talebin tarihini seçin. Varsayılan değer, geçerli tarihtir.
    - **Talep nedeni**: Mevcut kesinti için geçerli olan neden kodunu seçin. Seçtiğiniz talep esası, geçerli seçenekleri etkiler. Burada seçim için kullanılabilir talep nedenlerini oluşturma ve yapılandırma hakkında daha fazla bilgi için bu makalenin önceki [Kesinti nedenleri oluşturma](#deduction-reasons) bölümüne bakın.
    - **Notlar**: Geçerli not ekleyin. Talep onaylandığında onaylayan, talebin notlarını düzenleyebilir veya bunlara ekleme yapabilir.
    - **Talep günlüğü oluştur**: Talep veya kesinti oluşturulduğunda talep günlüğünün oluşturulup oluşturulmayacağını belirtmek için bu seçeneği ayarlayın:

        - *Evet*: Sistem, **Alacak hesapları parametreleri** sayfasında ayarlanan talep günlüğünü kullanarak bir yevmiye defteri oluşturup deftere nakleder. (Daha fazla bilgi için bu makalenin önceki [Alacak hesapları ve kesintileri yapılandırma](#accounts-receivable-deductions) bölümüne bakın.) Talebe bir fatura eklendiğinde talep günlüğü, geçerli faturanın bakiyesini azaltmak için kullanılır. Daha sonra talep reddedilirse talep günlüğü ve kapatma işlemleri (fatura eklenmişse) tersine çevrilir.
        - *Hayır*: Bu durumda talep günlüğü oluşturulmaz. Talep günlüğü, talep onaylandığında oluşturulur. Talep günlüğü oluşturulmamış olsa bile yeni talebe bir fatura eklenebilir. Ancak talep günlüğü olmadan kapatma yapılamaz.

1. **Tamam**'ı seçin.

    Yeni bir kesinti oluşturulur. **Talep günlüğü oluştur** seçeneğini *Evet* olarak ayarlarsanız aşağıdaki hareketler deftere nakledilir:

    - **İki yeni müşteri hareketi**: Bir hareket, talep tutarını orijinal faturaya göre mahsup eder. Talep henüz onaylanmadığından diğer hareket bir müşterinin borcunu talep tutarına kaydeder. Eylem Bölmesi'nde **Yönet \> Fatura ekle**'yi seçerek faturayı eklediğinizde orijinal fatura hareketi ve mahsup talebi hareketi otomatik olarak kapatma olarak işaretlenir.
    - **İki mahsup hareketi**: Bu hareketler **Kesinti mahsubu** genel muhasebe hesabına nakledilir.
    - **Talep günlüğü**: Kesinti workbench'inde gösterilen her kesinti için talep günlüğünü görüntülemek üzere **Başvurular** sekmesini seçin. Talep günlüğü, **Günlük toplu iş numarası** alanında gösterilir. Talep günlüğünü **Kesinti olayları** sekmesinde de görüntüleyebilirsiniz. Burada, *Eşleştirme*'nin **Güncelleştirme türü** değerini alır.

    Bu aşamada seçili faturayı işaretli olarak gösteren **Hareketleri kapatma** sayfasına dönersiniz. **Deftere Naklet** düğmesi yalnızca **Talep günlüğü oluştur** seçeneği *Evet* olarak ayarlandığında kullanılabilir. Kullanılabilir durumdaysa faturadaki bakiyeyi **Talep tutarı** değeri kadar azaltmak için **Deftere Naklet**'i seçin.

### <a name="create-a-deduction-from-a-customer-page"></a>Müşteri sayfasından kesinti oluşturma

Müşteri sayfasından kesinti oluşturma, kesinti workbench'i aracılığıyla kesinti oluşturma işlemine benzerdir. Ancak müşteri otomatik olarak ayarlanır.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Adına kesinti oluşturulacak müşteriyi seçin.
1. Eylem Bölmesinde, **Tahsil Et** sekmesindeki **Kesintiler** grubunda **Kesinti oluştur**'u seçin.

    **Yeni kesinti** iletişim kutusunda, **Kesinti Kimliği** alanı **Ticari tahsisat yönetimi parametreleri** sayfasında (**Satış ve pazarlama \> Kurulum \> Ticari tahsisatlar \> Ticari tahsisat yönetimi parametreleri**) tanımlanan **Kesinti Kimliği** numara sırasına göre ayarlanır. **Müşteri hesabı** alanı kesinti için geçerli olan müşteri hesabı olarak ayarlanır.

1. Aşağıdaki alanları ayarlayın:

    - **Harici talep numarası**: Müşterinin talep başvurusunu girin.
    - **Talep tutarı**: Vergi dahil talep tutarını girin. Değer pozitif olmalıdır.
    - **Para Birimi**: Kesintinin para birimini seçin. Varsayılan değer, seçili müşteri hesabı için ayarlanan para birimidir.
    - **Talep esası**: Talep esasını seçin. Talep esası, kesinti veya talep onaylandıktan sonra oluşturulan kredi hareketinin türünü belirler.

        - *Fiyat tabanlı*: Taslak serbest metinli fatura oluşturulur.
        - *Miktar tabanlı*: Eksi satış siparişi veya iade emri oluşturulur.

    - **Talep tarihi**: Talebin tarihini seçin. Varsayılan değer, geçerli tarihtir.
    - **Talep nedeni**: Mevcut kesinti için geçerli olan neden kodunu seçin. Seçtiğiniz talep esası, geçerli seçenekleri etkiler. Burada seçim için kullanılabilir talep nedenlerini oluşturma ve yapılandırma hakkında daha fazla bilgi için bu makalenin önceki [Kesinti nedenleri oluşturma](#deduction-reasons) bölümüne bakın.
    - **Notlar**: Geçerli not ekleyin. Talep onaylandığında onaylayan, talebin notlarını düzenleyebilir veya bunlara ekleme yapabilir.
    - **Talep günlüğü oluştur**: Talep veya kesinti oluşturulduğunda talep günlüğünün oluşturulup oluşturulmayacağını belirtmek için bu seçeneği ayarlayın:

        - *Evet*: Sistem, **Alacak hesapları parametreleri** sayfasında ayarlanan talep günlüğünü kullanarak bir yevmiye defteri oluşturup deftere nakleder. (Daha fazla bilgi için bu makalenin önceki [Alacak hesapları ve kesintileri yapılandırma](#accounts-receivable-deductions) bölümüne bakın.) Talebe bir fatura eklendiğinde talep günlüğü, geçerli faturanın bakiyesini azaltmak için kullanılır. Daha sonra talep reddedilirse talep günlüğü ve kapatma işlemleri (fatura eklenmişse) tersine çevrilir.
        - *Hayır*: Bu durumda talep günlüğü oluşturulmaz. Talep günlüğü, talep onaylandığında oluşturulur. Talep günlüğü oluşturulmamış olsa bile yeni talebe bir fatura eklenebilir. Ancak talep günlüğü olmadan kapatma yapılamaz.

1. **Tamam**'ı seçin.

    Yeni bir kesinti oluşturulur. **Talep günlüğü oluştur** seçeneğini *Evet* olarak ayarlarsanız aşağıdaki hareketler deftere nakledilir:

    - **İki yeni müşteri hareketi**: Bir hareket, talep tutarını orijinal faturaya göre mahsup eder. Talep henüz onaylanmadığından diğer hareket bir müşterinin borcunu talep tutarına kaydeder. Eylem Bölmesi'nde **Yönet \> Fatura ekle**'yi seçerek faturayı eklediğinizde orijinal fatura hareketi ve mahsup talebi hareketi otomatik olarak kapatma olarak işaretlenir.
    - **İki mahsup hareketi**: Bu hareketler **Kesinti mahsubu** genel muhasebe hesabına nakledilir.
    - **Talep günlüğü**: Kesinti workbench'inde gösterilen her kesinti için talep günlüğünü görüntülemek üzere **Başvurular** sekmesini seçin. Talep günlüğü, **Günlük toplu iş numarası** alanında gösterilir. Talep günlüğünü **Kesinti olayları** sekmesinde de görüntüleyebilirsiniz. Burada, *Eşleştirme*'nin **Güncelleştirme türü** değerini alır.

## <a name="create-a-credit-note-for-a-customer"></a>Müşteri için alacak dekontu oluşturma

Müşteri için onaylanmış bir indirim mevcut olduğunda gerekirse indirimi göstermek için müşterinin hesabında bir alacak dekontu oluşturabilirsiniz. Ardından kredi bir kesinti ile eşleştirilebileceği kesinti workbench'inde görüntülenir.

Yeni bir alacak dekontu oluşturmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Müşteriyi seçin.
1. Eylem Bölmesinde **Tahsil Et** sekmesindeki **Kapatma** grubunda **Hareketleri kapat**'ı seçin.
1. **Hareketleri kapatma** iletişim kutusunda, indirimin uygulandığı hareketi seçin.
1. Araç çubuğunda, **İşlevler** menüsünde uygulanacak indirim programı türünü seçin.
1. **İndirim** sayfasında **Genel Bakış** sekmesinde ilgili indirim kimliğinin yanındaki **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **İşlevler \> Alacak dekontu oluştur**'u seçin.

## <a name="process-a-deduction-on-the-deduction-workbench"></a>Kesinti workbench'inde kesinti işleme

Kesinti workbench'inde, kesintileri kredi hareketleri açma, kesintileri bölme, kesintileri reddetme ve kesintileri silme işlemleriyle eşleştirebilirsiniz.

Kesintiyi nasıl işlemek istediğinize bağlı olarak, aşağıdaki alt bölümlerdeki yordamlardan birini veya birkaçını tamamlayın. Gerekirse yordamları birleştirebilirsiniz. Örneğin, bir kesintiyi iki parçaya bölebilir ve ardından bir parçayı alacakla eşleştirebilir ve sonra başka bir krediyle eşleştirilmesi için kalan parçayı workbench'te bırakabilirsiniz. Ayrıca bir kesintiyi, kesinti tutarından daha küçük bir krediyle eşleştirebilir ve ardından kesintinin kalan bakiyesini reddedebilir veya silebilirsiniz.

### <a name="match-a-deduction-to-a-credit"></a>Kesintiyi bir krediyle eşleştirme

Kesintiyi bir krediyle eşleştirmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. **Açık hareketler** bölümünde, indirimle eşleştirilecek kredi için **İşaretle** onay kutusunu seçin. Birden fazla kredi listeleniyorsa kesintiyle eşleştirmek için birden fazla kredi seçebilirsiniz. Sistemin, kesinti tutarına uygun kredileri otomatik olarak seçmesini isterseniz araç çubuğunda **Kesinti tutarı seçin** menüsünden uygun seçeneği belirleyin.
1. Eylem Bölmesi'nde **Yönet \> Eşleştir**'i seçin. Sistem, kesintiyi krediyle eşleştirir. Kesintide bakiye kalırsa **Kesintiler** sekmesinde **Kalan tutar** alanında gösterilir.

    > [!NOTE]
    > Kesinti workbench'inde, müşteri kapatma işlemlerinde veya müşteri sayfasında **Yeni kesinti** komutu kullanılarak oluşturulmuş kesintilerde yalnızca **Talep durumu** alanı *Kabul Edildi* olarak ayarlanırsa **Yönet \> Eşleştir** komutu kullanılabilir. Bu komut, fiyat tabanlı veya miktar tabanlı hareketi **Açık hareketler** bölümündeki ilişkili krediyle el ile eşleştirmek için kullanılabilir. Bu kredi, bu makalenin önceki [Kesintiyi onaylama işleminin dışında oluşturulan krediler](#credits-outside-approval) bölümünde açıklandığı gibi kesinti onaylandığında (**Yönet \> Kesintiyi onayla** komutu kullanılarak) veya mevcut bir krediye eklendiğinde oluşturulur. *Onaylanan kesintileri kapat* periyodik görevi (**Satış pazarlama \> Periyodik görevler \> Onaylanan kesintileri kapat**) eşleşen **Kesinti Kimliği** değerleri ve tutarları olan kesintileri ve kredileri otomatik olarak eşleştirmek için de kullanılabilir.

### <a name="split-a-deduction"></a>Kesintiyi bölme

Kesintiyi bölmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde **Yönet \> Böl**'ü seçin.
1. **Böl** iletişim kutusunda, **Tutarı böl** alanına ana kesintiden bölünecek tutarı girin. Daha sonra **Tamam**'ı seçin.
1. **Kesintiler** sekmesinde, bölünen tutar için yeni bir kayıt göründüğüne dikkat edin. Orijinal kesinti kaydı, kesinti bakiyesinin kalanını içerir. Artık orijinal indirimin iki parçasını ayrı ayrı yönetebilirsiniz.
1. Orijinal kesinti kaydını ve ardından **Başvurular** sekmesini seçin. **Bölünen tutar** alanı, orijinal tutardan bölünmüş tutarı gösterir.

### <a name="attach-an-invoice-to-a-deduction"></a>Kesintiye bir fatura ekleme

Kesinti, kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulduysa ve şu anda eklenmiş bir fatura yoksa (başka bir deyişle, **Fatura** sütunu boşsa) kesintiye bir fatura ekleyebilirsiniz.

Kesintiye bir fatura eklemek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **Yönet \> Fatura ekle**'yi seçin.
1. **Fatura ekle** iletişim kutusunda, bir fatura seçin ve ardından **Tamam**'ı seçin.
1. **Hareketleri kapat** iletişim kutusunda, kesinti oluşturulduğunda bir talep günlüğünün deftere nakledilip nakledilmediğine bağlı olarak şu adımlardan birini izleyin:

    - Talep günlüğü deftere nakledildiyse seçtiğiniz fatura ve talep günlüğünün müşteri kredisi hareketi **İşaretle** sütununda bir onay işareti gösterir. **Naklet**'i seçin. Eklenen faturada kalan bakiye, talep tutarı kadar azaltılır.
    - Talep günlüğü deftere nakledilemediğinden hiçbir hareket **İşaretle** sütununda bir onay işareti göstermez. Kesinti onaylanana kadar bir talep günlüğüne göre mahsup edemeyeceğinizden **İptal**'i seçin.

### <a name="detach-an-invoice-from-a-deduction"></a>Kesintiden bir faturayı ayırma

Kesinti, kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulduysa, şu anda eklenmiş bir fatura varsa (başka bir deyişle, **Fatura** sütununda bir fatura numarası gösteriliyorsa) ve **Talep durumu** alanı *Açık* olarak ayarlanmışsa kesintiden bir faturayı ayırabilirsiniz. Yanlış bir fatura eklendiğinden bu görevi tamamlayabilirsiniz. Fatura kesintiden kaldırılır ve fatura eklendiğinde azaltılmışsa kalan bakiyesi güncelleştirilir.

Faturayı ayırmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **Yönet \> Faturayı ayır**'ı seçin.

### <a name="approve-a-deduction"></a>Kesintiyi onaylama

Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintileri onaylayabilirsiniz. Ancak yalnızca **Talep durumu** alanının *Açık* olarak ayarlandığı kesintileri onaylayabilirsiniz.

Kesintiyi onaylamak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **Yönet \> Kesintiyi onayla**'yı seçin.
1. **Kesintiyi onayla** iletişim kutusunda, gerekirse bilgileri düzenleyin veya **Not** değerine ekleyin.
1. Kesinti fiyata tabanlıysa ve fatura eklenmemişse bir madde satış vergisi grubu seçin. Genel olarak, vergi madde grubu faturada ayarlanır. Bu nedenle, vergi madde kodu faturaya eklenmediyse belirtilmelidir.
1. **Tamam**'ı seçin.

    Bu noktada, kesintide başka bir değişiklik yapılamaz. Kesinti oluşturulduğunda **Talep günlüğü oluştur** seçeneği *Hayır* olarak ayarlanmışsa kesinti onaylandığında talep günlüğü oluşturulur ve deftere nakledilir. Kesinti onaylandıktan sonra kredi otomatik olarak oluşturulur ve açılır. Tür, kesintinin **Talep esası** değerine bağlıdır:

    - *Fiyat tabanlı*: Kesinti fiyat tabanlıysa müşteri hesabı için serbest metinli bir fatura oluşturulur. Açıklama ekleyebilir ve krediyi deftere nakledebilirsiniz. Taslak oluşturulduğunda kesintiye göre aşağıdaki alanlar doldurulur:

        - **Kesinti Kimliği**: Kesintide izlenebilirlik özelliğini yeniden etkinleştirmek için bu alan başlığa eklenir.
        - **Ana hesap**: Değer, kesintiye atanan kesinti nedeni için ayarlanan **Deftere nakil hesabı talep et** değerine göre belirlenir.
        - **Madde satış vergisi grubu**: Değer, ekli faturaya veya kesintiyi onayladığınızda seçtiğiniz değere göre belirlenir.
        - **Birim fiyat**: Değer, kesintinin talep tutarının kredisidir.
        - **Fatura metni**: Varsayılan olarak bu alan, kesintinin **Notlar** değeri olarak ayarlanır.

    - *Miktar tabanlı*: Kesinti miktar tabanlıysa açık satış siparişi veya iade emri oluşturulur. **[Alacak hesapları parametreleri](#accounts-receivable-deductions)** sayfasındaki **İade emri oluştur** ayarı, kesinti onaylandığında satış siparişi ya da iade emri oluşturulacağını belirler. **Siparişleri kopyala** sayfası görüntülenir ve **Fatura hesabı** alanının kesintinin müşteri hesabı olarak ayarlandığı satırları gösterecek şekilde filtrelenir. Aşağıdaki adımları izleyin:

        1. **Faturalar** hızlı sekmesinde **Başlıklar** bölümünde **Fatura hesabı** değerinin kesintinin müşteri hesabıyla eşleştiği satış faturaları görüntülenir. Geçerli bir satış faturası seçin.
        1. **Satırlar** bölümünde, seçili satış faturasındaki satırlar görüntülenir. Kopyalamak istediğiniz her satırın **Seçim** onay kutusunu işaretleyin. Alternatif olarak, **Başlıklar** bölümünde, tüm satırlarını seçmek için satış siparişinin **Tümünü seç** onay kutusunu işaretleyin.
        1. Gerekirse, bir veya daha fazla satır için **Miktar** değerini ayarlayın.

            Şimdiye kadar seçtiğiniz tüm satırlar **Seçilen satırlar veya başlık kopyalanacak** hızlı sekmesinde listelenir.

        1. Gerekirse, tüm gerekli satırlar **Seçilen satırlar veya başlık kopyalanacak** hızlı sekmesinde listelenene kadar önceki iki adımı tekrarlayın.
        1. **Tamam**'ı seçin.

            Yeni iade emri açılır ve aşağıdaki alanlar otomatik olarak ayarlanır:

            - **Kesinti Kimliği**: Kesintide izlenebilirlik özelliğini yeniden etkinleştirmek için bu alan başlığa eklenir.
            - **İade nedeni kodu**: Varsayılan olarak, bu alan kesintiye atanan kesinti nedeni için ayarlanan **İade nedeni kodu** değeri olarak ayarlanır.

Kredi faturalandırıldıktan sonra, **Kesinti Kimliği** değeri için kesinti workbench'inin **Açık hareketler** bölümünde görüntülenir ve **Talep türü** alanı *Diğer krediler* olarak ayarlanır. Kredi aşağıdaki yollardan biriyle kesinti yapılarak kapatılana kadar kullanılabilir:

- Bunu Eylem Bölmesi'nde **Yönet \> Eşleştir**'i seçerek el ile kapatabilirsiniz.
- *Onaylanan talepleri kapat* periyodik işi tarafından otomatik olarak kapatılır (**Satış ve pazarlama \> Periyodik görevler \> Onaylanan talepleri kapat**).
- **Alacak hesapları parametreleri** sayfasının **Kapatma** sekmesindeki **Otomatik kapatma** seçeneği *Evet* olarak ayarlandığından otomatik olarak kapatılır.

Kesinti onaylandığında oluşturulan krediyi görüntülemek için kesinti workbench'inin **Açık hareketler** bölümündeki **Açık kredi** düğmesini de kullanabilirsiniz.

### <a name="create-a-return-order"></a>Sipariş iadesi oluşturma

Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintiler için bir iade emri oluşturabilirsiniz. Ancak aşağıdaki koşulların tümünün karşılanması gerekir:

- **Talep esası** alanı *Miktar tabanlı* olarak ayarlanır.
- **Talep durumu** alanı *Açık* olarak ayarlanır.
- **[Alacak hesapları parametreleri](#accounts-receivable-deductions)** sayfasının **Kesintiler** sekmesindeki **İade emri oluştur** seçeneği *Evet* olarak ayarlanır.
- **[Alacak hesapları parametreleri](#accounts-receivable-deductions)** sayfasının **Kesintiler** sekmesindeki **Kesinti onayından önce iade emri oluştur** seçeneği *Evet* olarak ayarlanır.

İade emri oluşturmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **Yönet \> İade emri oluştur**'u seçin.
1. **Kesintiyi onayla** iletişim kutusunda, gerekirse bilgileri düzenleyin ve mevcut **Notlar** değerine ekleyin ve ardından **Tamam**'ı seçin.
1. **Siparişleri kopyala** iletişim kutusunda, **Faturalar** hızlı sekmesinde **Başlıklar** bölümünde **Fatura hesabı** değerinin kesintinin müşteri hesabıyla eşleştiği satış faturaları görüntülenir. Geçerli bir satış faturası seçin.
1. **Satırlar** bölümünde, seçili satış faturasındaki satırlar görüntülenir. Kopyalamak istediğiniz her satırın **Seçim** onay kutusunu işaretleyin. Alternatif olarak, **Başlıklar** bölümünde, tüm satırlarını seçmek için satış siparişinin **Tümünü seç** onay kutusunu işaretleyin.
1. Gerekirse, bir veya daha fazla satır için **Miktar** değerini ayarlayın.

    Şimdiye kadar seçtiğiniz tüm satırlar **Seçilen satırlar veya başlık kopyalanacak** hızlı sekmesinde listelenir.

1. Gerekirse, tüm gerekli satırlar **Seçilen satırlar veya başlık kopyalanacak** hızlı sekmesinde listelenene kadar önceki iki adımı tekrarlayın.
1. **Tamam**'ı seçin.

    Yeni iade emri açılır ve aşağıdaki alanlar otomatik olarak ayarlanır:

    - **Kesinti Kimliği**: Kesintide izlenebilirlik özelliğini yeniden etkinleştirmek için bu alan başlığa eklenir.
    - **İade nedeni kodu**: Varsayılan olarak, bu alan kesintiye atanan kesinti nedeni için ayarlanan **İade nedeni kodu** değeri olarak ayarlanır.

### <a name="deny-a-deduction"></a>Kesintiyi reddetme

Kesintiyi reddetmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde **Yönet \> Reddet**'i seçin.
1. **Reddet** iletişim kutusunda, reddetme nedeni kodunu seçin ve ardından **Tamam**'ı seçin.
1. Eylem Bölmesi'nin altındaki **Göster** alanında *Kapalı* seçeneğini belirleyin.

    **Kesintiler** sekmesinde reddedilen kesinti görüntülenir ve kesinti için **Kalan tutar** alanı *0,00* olarak ayarlanır.

    Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintilerde aşağıdaki olaylar oluşur:

    - **Başvurular** sekmesinde, **Reddetme** bölümündeki alanlar güncelleştirilir.
    - Kesinti oluşturulurken talep günlüğü oluşturmayı seçtiyseniz ve faturanın bakiyesini azaltan kesintiye bir fatura eklendiyse fatura ayrılır ve önceden eklenen faturanın kalan bakiyesi reddedilen talebin tutarı kadar artar.
    - Kesintinin **Durum** alanı *Kapalı* olarak ayarlanır.
    - Kesintinin **Talep durumu** alanı *Reddedildi* olarak ayarlanır.

Reddetme işlemini tersine çevirmek için aşağıdaki adımları izleyin.

1. **Kesintiler** sekmesinde, reddedilen bir kesintiyi seçin.
1. Eylem Bölmesi'nde, **Reddetmeyi tersine çevir**'i seçin.

    Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintilerde aşağıdaki olaylar oluşur:

    - **Başvurular** sekmesinde, **Reddetme** bölümündeki alanlar güncelleştirilir.
    - Kesintinin **Durum** alanı *Açık* olarak ayarlanır.
    - Kesintinin **Talep durumu** alanı *Açık* olarak ayarlanır.

### <a name="write-off-a-deduction"></a>Kesintiyi silme

Kesintiyi silmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesinti için **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde **Yönet \> Sil**'i seçin.
1. **Sil** iletişim kutusunda, silme nedeni kodunu seçin ve ardından **Tamam**'ı seçin.
1. **Göster** alanında *Kapalı*'yı seçin.

    **Kesintiler** sekmesinde silinen kesinti görüntülenir ve kesinti için **Kalan tutar** alanı *0,00* olarak ayarlanır.

    Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintilerde aşağıdaki olaylar oluşur:

    - **Başvurular** sekmesinde, **Sil** bölümündeki alanlar güncelleştirilir.
    - Kesinti oluşturulduğunda talep günlüğünü oluşturduysanız kesintinin silme nedeni kodu için bir talep günlüğü deftere nakledilir. Bu girişi *Sil* seçeneğinin **Güncelleştirme türü** değerinin bulunduğu **Kesinti olayları** sekmesinde görüntüleyebilirsiniz.
    - Kesintinin **Durum** alanı *Kapalı* olarak ayarlanır
    - Kesintinin **Talep durumu** alanı *Sil* olarak ayarlanır.

Silme işlemini tersine çevirmek için aşağıdaki adımları izleyin.

1. **Kesintiler** sekmesinde, reddedilen bir kesintiyi seçin.
1. Eylem Bölmesi'nde **Silmeyi tersine çevir**'i seçin.

    Kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintilerde aşağıdaki olaylar oluşur:

    - **Başvurular** sekmesinde, **Sil** bölümündeki alanlar güncelleştirilir.
    - Kesinti oluşturulduğunda talep günlüğünü oluşturduysanız kesintinin silme nedeni kodu için bir talep günlüğü deftere nakledilir. Bu girişi *Silmeyi tersine çevir* seçeneğinin **Güncelleştirme türü** değerinin bulunduğu **Kesinti olayları** sekmesinde görüntüleyebilirsiniz.
    - Kesintinin **Durum** alanı *Açık* olarak ayarlanır.
    - Kesintinin **Talep durumu** alanı *Açık* olarak ayarlanır.

## <a name="credits-created-outside-the-approve-deduction-process"></a><a name="credits-outside-approval"></a>Kesintiyi onaylama işlemi dışında oluşturulan krediler

Bu bölüm yalnızca kesinti workbench'i, müşteri kapatma işlemleri veya müşteri sayfasındaki **Yeni kesinti** komutu kullanılarak oluşturulan kesintiler için geçerlidir.

Farklı kullanıcılar, müşterinin talebi için **Kesintiyi onaylama** işleminin dışında bir serbest metinli fatura, iade emri veya eksi satış siparişi oluşturmuş olabilir. Mevcut kesinti, kesinti workbench'inde onaylandığında sistem otomatik olarak başka bir serbest metinli fatura, iade emri veya eksi satış siparişi oluşturur. Bu bölümde, yinelenen kredileri önlemeye yardımcı olmak için kesinti onaylanmadan önce mevcut kredilerin bir kesintiye nasıl ekleneceği açıklanmaktadır.

### <a name="attach-a-credit-to-deduction"></a>Krediyi kesintiye ekleme

Bu bölümde, bir krediyi krediden kesintiye nasıl ekleyebileceğiniz açıklanmaktadır.

Kredi kesintiye eklendikten sonra kesinti workbench'inin **Açık hareketler** bölümündeki araç çubuğunda **Açık kredi** düğmesini kullanarak krediyi görüntüleyebilirsiniz.

Kredi faturalandırıldıktan ve kesinti onaylandıktan sonra kredi, geçerli **Kesinti Kimliği** değeri için kesinti workbench'inin **Açık hareketler** bölümünde görüntülenir ve **Talep türü** alanı *Diğer krediler* olarak ayarlanır.

#### <a name="attach-a-free-text-invoice-to-a-deduction"></a>Kesintiye serbest metinli bir fatura ekleme

Kesintiye serbest metinli bir fatura eklemek için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.
1. Geçerli faturayı seçin.
1. Eylem Bölmesi'ndeki **Fatura** sekmesinde, **Krediyi kesintiye ekle**'yi seçin. Bu düğme yalnızca serbest metinli faturanın **Kesinti Kimliği** alanı boşsa kullanılabilir. Boş alan, serbest metinli faturanın henüz kesintiye eklenmemiş olduğunu gösterir.
1. **Krediyi kesintiye ekle** sayfasında, *bir* kesinti seçebilirsiniz. Seçim için yalnızca açık *fiyat tabanlı* kesintiler kullanılabilir.
1. **Tamam**'ı seçin. **Kesinti Kimliği** alanı serbest metinli faturanın başlığında ayarlanır.

#### <a name="attach-a-return-order-to-a-deduction"></a>Kesintiye bir iade emri ekleme

Kesintiye bir iade emri eklemek için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm iade emirlerine**'ne gidin.
1. Geçerli alınan veya açık iade mal yetki (RMA) numarasını seçin.
1. Eylem Bölmesi'ndeki **İade emri** sekmesinde, **Krediyi kesintiye ekle**'yi seçin. Bu düğme yalnızca iade emrinin **Kesinti Kimliği** alanı boşsa kullanılabilir. Boş alan, iade emrinin henüz kesintiye eklenmemiş olduğunu gösterir.
1. **Krediyi kesintiye ekle** sayfasında, *bir* kesinti seçebilirsiniz. Seçim için yalnızca açık *miktar tabanlı* kesintiler kullanılabilir.
1. **Tamam**'ı seçin. **Kesinti Kimliği** alanı iade emrinin başlığında ayarlanır.

#### <a name="attach-a-sales-order-to-a-deduction"></a>Kesintiye bir satış siparişi ekleme

Kesintiye bir satış siparişi eklemek için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.
1. Geçerli açık, teslim edilen veya faturalandırılmış satış siparişini seçin.
1. Eylem Bölmesi'ndeki **Fatura** sekmesinde, **Krediyi kesintiye ekle**'yi seçin. Bu düğme yalnızca satış siparişinin **Kesinti Kimliği** alanı boşsa kullanılabilir. Boş alan, satış siparişinin henüz kesintiye eklenmemiş olduğunu gösterir.
1. **Kesinti ekle** sayfasında, *bir* kesinti seçebilirsiniz. Seçim için yalnızca açık *miktar tabanlı* kesintiler kullanılabilir.
1. **Tamam**'ı seçin. **Kesinti Kimliği** alanı satış siparişinin başlığında ayarlanır.

#### <a name="detach-a-deduction-from-a-credit"></a>Kesintiyi bir krediden ayırma

Hatalı kesinti eklenmişse bu kesintiyi krediden ayırabilirsiniz. Ancak aşağıdaki koşulların tümünün karşılanması gerekir:

- Kredi kesintiye eklenir.
- **Talep durumu** alanı *Açık* olarak ayarlanır.

Kesintiyi bir krediden ayırmak için kredi türüne bağlı olarak şu adımlardan birini izleyin:

- **Serbest metinli faturalar:** **Tüm serbest metinli faturalar** sayfasında bir fatura seçin. Ardından Eylem Bölmesi'ndeki **Fatura** sekmesinde, **Krediyi kesintiden ayır**'ı seçin.
- **İade emirleri:** **Tüm iade emirleri** sayfasında bir emir seçin. Ardından Eylem Bölmesi'ndeki **İade emri** sekmesinde, **Krediyi kesintiden ayır**'ı seçin.
- **Satış siparişleri:** **Tüm satış siparişleri** sayfasında bir sipariş seçin. Ardından Eylem Bölmesi'ndeki **Fatura** sekmesinde, **Krediyi kesintiden ayır**'ı seçin.

### <a name="attach-a-deduction-to-a-credit"></a>Kesintiyi bir krediye ekleme

Bu bölümde, kesintiyi kesintiden bir krediye nasıl ekleyebileceğiniz açıklanmaktadır.

#### <a name="attach-a-deduction-to-a-free-text-return-order-or-sales-order-credit"></a>Serbest metin, iade emri veya satış siparişi kredisine bir kesinti ekleme

Serbest metin, iade emri veya satış siparişi kredisine bir kesinti eklemek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. Geçerli açık kesintiyi seçin.
1. Eylem Bölmesi'nde, **Yönet \> Kesintiyi krediye ekle**'yi seçin. Bu düğme yalnızca **Talep durumu** alanı *Açık* olarak ayarlandığında kullanılabilir.
1. **Kredi ekle** sayfasında, *bir* kredi seçebilirsiniz. Gösterilen kredi türü, kesintinin **Talep esası** değerine bağlıdır:

    - *Fiyat tabanlı*: Sayfada **Kesinti Kimliği** alanının boş olduğu müşteri hesabı için serbest metinli faturalar gösterilir. Serbest metinli fatura deftere nakledilmemiş olabileceğinden müşteri talepleri de gösterilir. Bu nedenle, başvurulabilecek bir numaraya sahip olmayabilir.
    - *Miktar tabanlı*: **[Alacak hesapları parametreleri](#accounts-receivable-deductions)** sayfasındaki **İade emri oluştur** seçeneğinin ayarına bağlı olarak gösterilen kredi türü:

        - *Evet*: Sayfada **Kesinti Kimliği** alanının boş olduğu müşteri hesabı için iade emirleri gösterilir.
        - *Hayır*: Sayfada **Kesinti Kimliği** alanının boş olduğu müşteri hesabı için satış siparişleri gösterilir.

1. **Tamam**'ı seçin. **Kesinti Kimliği** alanı kredinin başlığında ayarlanır.

Kredi kesintiye eklendikten sonra kesinti workbench'inin **Açık hareketler** bölümündeki araç çubuğunda **Açık kredi** düğmesini kullanarak krediyi görüntüleyebilirsiniz.

Kredi faturalandırıldıktan ve kesinti onaylandıktan sonra kredi, geçerli **Kesinti Kimliği** değeri için kesinti workbench'inin **Açık hareketler** bölümünde görüntülenir ve **Talep türü** alanı *Diğer krediler* olarak ayarlanır.

#### <a name="detach-a-credit-from-the-deduction"></a>Krediyi kesintiden ayırma

Hatalı kredi eklenmişse bu krediyi kesintiden ayırabilirsiniz. Eylem Bölmesi'nde, **Yönet** grubunda, **Kesintiyi krediden ayır**'ı seçin. **Kesinti Kimliği** değeri krediden kaldırılır.

**Kesintiyi krediden ayır** düğmesi yalnızca aşağıdaki koşullar karşılandığında kullanılabilir:

- Kredi kesintiye eklenir.
- **Talep durumu** alanı *Açık* olarak ayarlanır.

## <a name="create-a-one-time-promotion"></a>Tek seferlik promosyon oluşturma

Bazen, kesintiyle eşleştirebileceğiniz onaylanmış bir indiriminiz olmayabilir. Bu durumda, kesintiyi müşteriyle ilişkili bir ticari tahsisatla eşleştirmek için *tek seferlik promosyon* özelliğini kullanabilirsiniz. *Tek seferlik promosyon* özelliği, yeni bir ticari tahsisat sözleşmesi ve peşin ödeme emtia olayı oluşturur. Ardından peşin ödemeyi kesintiyle eşleştirir ve kesintiyi kapatmak için gerekli deftere nakil işlemlerini gerçekleştirir.

Bu özellik ticari tahsisatları kullandığınızda yararlıdır. Ticari tahsisatlar hakkında daha fazla bilgi için bkz. [Ticari tahsisat yönetimi](../sales-marketing/trade-allowance.md).

Öncelikle yeni ticari tahsisat sözleşmesini oluşturmak için kullanılabilecek bir şablon oluşturmanız gerekir. Şablonu ayarlamak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Şablonlar**'a gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Alanlara şablondan oluşturulan sözleşmelerde görüntülenmesi gereken bilgileri girin.
1. **Müşteriler** hızlı sekmesinde **Hiyerarşi** alanında bir hiyerarşi düzeyi seçin.
1. Hiyerarşi listesinde, eşleşmeyen kesintisi olan müşteriyi seçin ve ardından sağ ok düğmesini (**\>**) seçin. Müşteri **Ticari tahsisat sözleşmesi müşterileri** listesine eklenir.
1. Kalan alanları gerektiği gibi ayarlayın ve ardından sayfayı kapatın.
1. **Satış ve pazarlama \> Kurulum \> Ticari tahsisat \> Ticari tahsisat yönetimi parametreleri**'ne gidin.
1. **Genel Bakış** sekmesinde, **Tek seferlik promosyon şablonu** alanında, tek seferlik promosyonlar oluşturmak için kullanılacak şablonun adını seçin.

Ardından kesinti workbench'inde tek seferlik promosyon oluşturabilirsiniz. Tek seferlik promosyon oluşturmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. İşlenecek kesintinin yanındaki **İşaretle** onay kutusunu seçin.
1. Eylem Bölmesi'nde, **Yönet \> Kesintiyi tek seferlik promosyon olarak kapat**'ı seçin.
1. **Tek seferlik promosyon** iletişim kutusunda, kesintiyi bir veya daha fazla fonla ilişkilendirmek için şu adımları izleyin:

    1. **Yeni**'yi seçin ve ardından **Fon Kimliği** alanında bir fon kimliği seçin. Gereksinim duyduğunuz sayıda fon eklemek için bu adımı tekrarlayın.
    1. Her fon kimliğinin yanındaki **Yüzde** alanına fon için tahsis edilecek kesinti yüzdesini girin. **Yüzde** alanlarına girdiğiniz tutarların toplamı yüzde 100 olmalıdır.

1. **Tamam**'ı seçin. Sistem, peşin ödeme emtia olayının bulunduğu ve peşin ödemenin kesintiyle eşleştirildiği yeni bir ticari tahsisat sözleşmesi oluşturur.

## <a name="do-a-mass-update-of-deductions"></a>Kesintiler için toplu güncelleştirme yapma

Aynı değişikliği birden fazla kesintide yapmanız gerekiyorsa bu kesintileri seçerek alanları toplu olarak güncelleştirebilirsiniz.

Toplu güncelleştirme yapmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Ticari tahsisatlar \> Kesintiler \> Kesinti workbench'i**'ne gidin.
1. Eylem Bölmesi'nin altındaki **Göster** alanında, görüntülenecek kesinti türünü seçin.
1. Güncelleştirmek istediğiniz her kesintinin yanındaki onay kutusunu seçin. Ardından Eylem Bölmesi'nde, **Yönet \> Toplu güncelleştir**'i seçin.
1. **Toplu güncelleştirme** iletişim kutusunda seçili kesintiler gösterilir. Alanları gerektiği gibi güncelleştirin ve ardından değişiklikleri kabul etmek için **Tamam**'ı seçin.
